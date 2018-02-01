---
title: "Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0"
description: "Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure CLI 2.0."
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 10/12/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: e473b7289f3b72dc23a1f747e15cea1b88aa89e9
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2018
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0

Om du planerar att hantera appen eller tjänsten med Azure CLI 2.0 bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter.
Den här artikeln vägleder dig genom att skapa en säkerhetsprincip med Azure CLI 2.0.

> [!NOTE]
> Du kan också skapa ett huvudnamn för tjänsten via Azure Portal.
> Läs [Använd portalen för att skapa Active Directory-program och ett huvudnamn för tjänsten som får åtkomst till resurser](/azure/azure-resource-manager/resource-group-create-service-principal-portal) för mer information.

## <a name="what-is-a-service-principal"></a>Vad är ett huvudnamn för tjänsten?

Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser. Se det som en användaridentitet (inloggning och lösenord eller certifikat) med en viss roll och väl kontrollerad behörighet att komma åt dina resurser. Den behöver bara kunna utföra vissa åtgärder, till skillnad från en allmän användaridentitet. Det ger bättre säkerhet om du bara ger den lägsta behörighetsnivån som krävs för att den ska kunna utföra sina administrativa uppgifter.

Azure CLI 2.0 har stöd för att skapa lösenordsbaserade autentiseringsuppgifter och autentiseringsuppgifter för certifikat. Det här avsnittet handlar om båda typerna av autentiseringsuppgifter.

## <a name="verify-your-own-permission-level"></a>Kontrollera din egen behörighetsnivå

Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen. Du måste specifikt kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.

Det enklaste sättet att kontrollera om kontot har tillräcklig behörighet är via portalen. Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-application"></a>Skapa ett huvudnamn för tjänsten för programmet

Du måste ha något av följande för att identifiera appen du vill skapa tjänstens huvudnamn för:

  * Det unika namnet eller URI:n för den distribuerade appen (t.ex. "MyDemoWebApp" i följande exempel), eller
  * program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet

Värdena identifierar ditt program när du skapar ett namn på huvudtjänsten.

### <a name="get-information-about-your-application"></a>Hämta information om programmet

Hämta identietsinformation om ditt program med `az ad app list`.

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

```azurecli-interactive
az ad app list --display-name MyDemoWebApp
```

```json
{
    "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "appPermissions": null,
    "availableToOtherTenants": false,
    "displayName": "MyDemoWebApp",
    "homepage": "http://MyDemoWebApp.azurewebsites.net",
    "identifierUris": [
      "http://MyDemoWebApp"
    ],
    "objectId": "bd07205b-629f-4a2e-945e-1ee5dadf610b9",
    "objectType": "Application",
    "replyUrls": []
  }
```

Alternativet `--display-name` filtrerar den returnerade listan med appar för att vissa att dem med `displayName` börjar med MyDemoWebApp.

### <a name="create-a-service-principal-with-a-password"></a>Skapa ett huvudnamn för tjänsten med ett lösenord

Använd [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) och parametern `--password` för att skapa tjänstens huvudnamn med ett lösenord. Om du inte anger någon roll eller något omfång så blir standardinställningen rollen **Deltagare** för den aktuella prenumerationen. Om du skapar ett huvudnamn för tjänsten utan att använda vare sig `--password` eller parametern `--cert` används lösenordsautentisering och ett lösenord skapas för dig.

```azurecli-interactive
az ad sp create-for-rbac --name {appName} --password "{strong password}"
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "name": "http://MyDemoWebApp",
  "password": {strong password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

 > [!WARNING]
 > Skapa inte ett osäkert lösenord.  Följ vägledningen med [regler för lösenord och begränsningar i Azure AD](/azure/active-directory/active-directory-passwords-policy).

### <a name="create-a-service-principal-with-a-self-signed-certificate"></a>Skapa ett huvudnamn för tjänsten med ett självsignerat certifikat

Använd [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) och parametern `--create-cert` för att skapa ett självsignerat certifikat.

```azurecli-interactive
az ad sp create-for-rbac --name {appName} --create-cert
```

```json
{
  "appId": "c495db57-82e0-4e2e-9369-069dff176858",
  "displayName": "azure-cli-2017-10-12-22-15-38",
  "fileWithCertAndPrivateKey": "<path>/<file-name>.pem",
  "name": "http://MyDemoWebApp",
  "password": null,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

Kopiera värdet för svaret `fileWithCertAndPrivateKey`. Det här är certifikatfilen som kommer att användas för autentisering.

I [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) finns fler alternativ när du använder certifikat.

### <a name="get-information-about-the-service-principal"></a>Hämta information om tjänstens huvudnamn

```azurecli-interactive
az ad sp show --id {appID}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "objectId": "0ceae62e-1a1a-446f-aa56-2300d176659bde",
  "objectType": "ServicePrincipal",
  "servicePrincipalNames": [
    "http://MyDemoWebApp",
    "a487e0c1-82af-47d9-9a0b-af184eb87646d"
  ]
}
```

### <a name="sign-in-using-the-service-principal"></a>Logga in med tjänstens huvudnamn

Du kan nu logga in som det nya huvudnamnet för tjänsten för appen med *appId* från `az ad sp show` och antingen *lösenordet* eller sökvägen till det skapade certifikatet.  Ange *klientvärdet* från resultatet av `az ad sp create-for-rbac`.

```azurecli-interactive
az login --service-principal -u {appID} --password {password-or-path-to-cert} --tenant {tenant}
```

Dessa utdata visas efter en lyckad inloggning:

```json
[
  {
    "cloudName": "AzureCloud",
    "id": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "isDefault": true,
    "state": "Enabled",
    "tenantId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "user": {
      "name": "https://MyDemoWebApp",
      "type": "servicePrincipal"
    }
  }
]
```

Använd värdena `id`, `password` och `tenant` som autentiseringsuppgifter för att köra din app.

## <a name="managing-roles"></a>Hantera roller

> [!NOTE]
> Rollbaserad åtkomst i Azure (RBAC) är en modell för att definiera och hantera roller för användar- och säkerhetsobjekt.
> Rollerna är kopplade till en uppsättning med behörigheter, som avgör vilka resurser en princip kan läsa, få åtkomst till, skriva till eller hantera.
> Mer information om RBAC och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).

Azure CLI 2.0 tillhandahåller följande kommandon för att hantera rolltilldelningar:

* [az-rolltilldelningslista](/cli/azure/role/assignment#list)
* [skapa az-rolltilldelning](/cli/azure/role/assignment#create)
* [ta bort az-rolltilldelning](/cli/azure/role/assignment#delete)

Standardrollen för tjänstens huvudnamn är **Deltagare**. Det kanske inte är det bästa valet för appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet. Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar. Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.

I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

Bekräfta ändringarna genom att ange de roller som är tilldelade för närvarande:

```azurecli-interactive
az role assignment list --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
    "id": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleAssignments/c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "name": "c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "properties": {
      "principalId": "790525226-46f9-4051-b439-7079e41dfa31",
      "principalName": "http://MyDemoWebApp",
      "roleDefinitionId": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7",
      "roleDefinitionName": "Reader",
      "scope": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac"
    },
    "type": "Microsoft.Authorization/roleAssignments"
}
```

> [!NOTE]
> Om kontot inte har tillräcklig behörighet för att tilldela en roll får du ett felmeddelanden.
> Meddelandet anger att ditt konto ”inte har behörighet att utföra åtgärden ”Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}”.

## <a name="change-the-credentials-of-a-security-principal"></a>Ändra autentiseringsuppgifter för säkerhetsobjektet

Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet. Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras.

### <a name="reset-a-service-principal-password"></a>Återställa lösenord för tjänstens huvudnamn

Återställ det aktuella lösenordet för tjänstens huvudnamn med `az ad sp reset-credentials`.

```azurecli-interactive
az ad sp reset-credentials --name 20bce7de-3cd7-49f4-ab64-bb5b443838c3 --password {new-password}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "name": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "password": {new-password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

CLI genererar ett säkert lösenord om du hoppar över alternativet `--password`.
