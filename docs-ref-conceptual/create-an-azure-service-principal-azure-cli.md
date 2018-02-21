---
title: "Använda Azure-tjänstens huvudnamn med Azure CLI 2.0"
description: "Lär dig hur du skapar och använder ett huvudnamn för tjänsten med Azure CLI 2.0."
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/12/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: b46c735a14240bddd07659475ada1c33c75a1e67
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0

Om du vill skapa en separat inloggning med åtkomstbegränsningar så kan du göra det via tjänstens huvudnamn. Tjänstens huvudnamn är separata identiteter som kan associeras med ett konto. Tjänstens huvudnamn är användbara för att arbeta med program och uppgifter som måste automatiseras. I den artikeln får du stegvisa anvisningar för att skapa ett huvudnamn för tjänsten.

## <a name="create-the-service-principal"></a>Skapa huvudnamn för tjänsten

Skapa ett huvudnamn för tjänsten med kommandot [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac). Tjänstens huvudnamn inte är kopplat till ett befintligt program eller användarnamn. Du kan skapa ett huvudnamn för tjänsten med alla typer av autentisering.

* `--password` används för lösenordsbaserad autentisering. Se till att du skapar ett starkt lösenord genom att följa [reglerna och begränsningarna för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy). Om du inte anger något lösenord skapas ett automatiskt.

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD
  ```

* `--cert` används för certifikatbaserad autentisering för ett befintligt certifikat, antingen som en offentlig PEM- eller DER-sträng eller `@{file}` för att läsa in en fil.

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile} 
  ```

  Argumentet `--keyvault` kan läggas till för att visa att certifikatet lagras i Azure Key Vault. I det här fallet refererar värdet `--cert` till namnet på certifikatet i Key Vault.

* `--create-cert` skapar ett _självsignerat_ certifikat för autentisering. Argumentet `--keyvault` kan läggas till för att lagra certifikatet i Azure Key Vault.

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

Om ett argument som anger autentiseringstypen inte ingår används `--password` som standard.

Kommandot `create-for-rbac` ger utdata i följande format:

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

Värdena `appId`, `tenant` och `password` används för autentisering. `displayName` används när du söker efter ett befintligt huvudnamn för tjänsten.

> [!NOTE]
> Om ditt konto inte har rätt behörigheter för att skapa ett huvudnamn för tjänsten så visas ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden. Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.

## <a name="manage-service-principal-roles"></a>Hantera roller för tjänstens huvudnamn 

Azure CLI 2.0 tillhandahåller följande kommandon för att hantera rolltilldelningar.

* [az-rolltilldelningslista](/cli/azure/role/assignment#list)
* [skapa az-rolltilldelning](/cli/azure/role/assignment#create)
* [ta bort az-rolltilldelning](/cli/azure/role/assignment#delete)

Standardrollen för tjänstens huvudnamn är **Deltagare**. Den här rollen har fullständiga behörigheter att läsa och skriva till ett Azure-konto och är vanligtvis inte lämplig för program. Rollen **Läsare** är mer begränsad och tillhandahåller endast åtkomst för att läsa.  Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).

I det här exemplet lägger vi till rollen **Läsare** och tar bort rollen **Deltagare**.

```azurecli
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

När en roll läggs till ändras _inte_ eventuella tidigare tilldelade behörigheter. När du begränsar behörigheter för tjänstens huvudnamn bör rollen __Deltagare__ alltid tas bort.

Ändringarna kan bekräftas genom att ange de roller som är tilldelade.

```azurecli
az role assignment list --assignee APP_ID
```

> [!NOTE] 
> Om ditt konto inte har behörigheter att tilldela en roll så visas ett felmeddelande om att ditt konto "inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write" för omfånget "/subscriptions/{guid}". Kontakta Azure Active Directory-administratören om du vill hantera roller.

## <a name="log-in-using-the-service-principal"></a>Logga in med tjänstens huvudnamn

Du kan testa inloggningen för den nya tjänstens huvudnamn och dess behörigheter genom att logga in med den i Azure CLI. Logga in med det nya huvudnamnet för tjänsten med hjälp av `appId`, `tenant` och autentiseringsuppgifterna. Autentiseringsinformationen som du anger ändras beroende på om du har valt att skapa tjänstens huvudnamn med ett lösenord eller med ett certifikat.

Om du vill logga in med ett lösenord anger du det som en parameter i argumentet.

```azurecli
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

Om du vill logga in med ett certifikat så måste det vara tillgängligt lokalt som en PEM- eller DER-fil.

```azurecli
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```
## <a name="reset-credentials"></a>Återställ autentiseringsuppgifter

Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten så kan de återställas med kommandot [az ad sp reset-credentials](https://docs.microsoft.com/en-us/cli/azure/ad/sp?view=azure-cli-latest#az_ad_sp_reset_credentials). Samma begränsningar och alternativ för att skapa ett nytt huvudnamn för tjänsten gäller även här.

```azurecli
az ad sp reset-credentials --name APP_ID --password NEW_PASSWORD
```
