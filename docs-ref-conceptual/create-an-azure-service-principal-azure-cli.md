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
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="f4e65-103">Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f4e65-103">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="f4e65-104">Om du vill skapa en separat inloggning med åtkomstbegränsningar så kan du göra det via tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="f4e65-104">If you want to create a separate login with access restrictions, you can do so through a service principal.</span></span> <span data-ttu-id="f4e65-105">Tjänstens huvudnamn är separata identiteter som kan associeras med ett konto.</span><span class="sxs-lookup"><span data-stu-id="f4e65-105">Service principals are separate identities that can be associated with an account.</span></span> <span data-ttu-id="f4e65-106">Tjänstens huvudnamn är användbara för att arbeta med program och uppgifter som måste automatiseras.</span><span class="sxs-lookup"><span data-stu-id="f4e65-106">Service principals are useful for working with applications and tasks that must be automated.</span></span> <span data-ttu-id="f4e65-107">I den artikeln får du stegvisa anvisningar för att skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4e65-107">This article runs you through the steps for creating a service principal.</span></span>

## <a name="create-the-service-principal"></a><span data-ttu-id="f4e65-108">Skapa huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="f4e65-108">Create the service principal</span></span>

<span data-ttu-id="f4e65-109">Skapa ett huvudnamn för tjänsten med kommandot [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac).</span><span class="sxs-lookup"><span data-stu-id="f4e65-109">Use the [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) command to create a service principal.</span></span> <span data-ttu-id="f4e65-110">Tjänstens huvudnamn inte är kopplat till ett befintligt program eller användarnamn.</span><span class="sxs-lookup"><span data-stu-id="f4e65-110">The Service Principal's name isn't tied to any existing application or user name.</span></span> <span data-ttu-id="f4e65-111">Du kan skapa ett huvudnamn för tjänsten med alla typer av autentisering.</span><span class="sxs-lookup"><span data-stu-id="f4e65-111">You can create a service principal with your choice of authentication type.</span></span>

* <span data-ttu-id="f4e65-112">`--password` används för lösenordsbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="f4e65-112">`--password` is used for password-based authentication.</span></span> <span data-ttu-id="f4e65-113">Se till att du skapar ett starkt lösenord genom att följa [reglerna och begränsningarna för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="f4e65-113">Make sure that you create a strong password by following the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="f4e65-114">Om du inte anger något lösenord skapas ett automatiskt.</span><span class="sxs-lookup"><span data-stu-id="f4e65-114">If you don't specify a password, one is created for you.</span></span>

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD
  ```

* <span data-ttu-id="f4e65-115">`--cert` används för certifikatbaserad autentisering för ett befintligt certifikat, antingen som en offentlig PEM- eller DER-sträng eller `@{file}` för att läsa in en fil.</span><span class="sxs-lookup"><span data-stu-id="f4e65-115">`--cert` is used for certificate-based authentication for an existing certificate, either as a PEM or DER public string, or `@{file}` to load a file.</span></span>

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile} 
  ```

  <span data-ttu-id="f4e65-116">Argumentet `--keyvault` kan läggas till för att visa att certifikatet lagras i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e65-116">The `--keyvault` argument can be added to indicate the cert is stored in Azure Key Vault.</span></span> <span data-ttu-id="f4e65-117">I det här fallet refererar värdet `--cert` till namnet på certifikatet i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e65-117">In this case, the `--cert` value refers to the name of the certificate in Key Vault.</span></span>

* <span data-ttu-id="f4e65-118">`--create-cert` skapar ett _självsignerat_ certifikat för autentisering.</span><span class="sxs-lookup"><span data-stu-id="f4e65-118">`--create-cert` creates a _self-signed_ certificate for authentication.</span></span> <span data-ttu-id="f4e65-119">Argumentet `--keyvault` kan läggas till för att lagra certifikatet i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e65-119">The `--keyvault` argument can be added to store the certificate in Azure Key Vault.</span></span>

  ```azurecli
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

<span data-ttu-id="f4e65-120">Om ett argument som anger autentiseringstypen inte ingår används `--password` som standard.</span><span class="sxs-lookup"><span data-stu-id="f4e65-120">If an argument indicating the authentication type isn't included, `--password` is used by default.</span></span>

<span data-ttu-id="f4e65-121">Kommandot `create-for-rbac` ger utdata i följande format:</span><span class="sxs-lookup"><span data-stu-id="f4e65-121">The output of the `create-for-rbac` command is in the following format:</span></span>

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="f4e65-122">Värdena `appId`, `tenant` och `password` används för autentisering.</span><span class="sxs-lookup"><span data-stu-id="f4e65-122">The `appId`, `tenant`, and `password` values are used for authentication.</span></span> <span data-ttu-id="f4e65-123">`displayName` används när du söker efter ett befintligt huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4e65-123">The `displayName` is used when searching for an existing service principal.</span></span>

> [!NOTE]
> <span data-ttu-id="f4e65-124">Om ditt konto inte har rätt behörigheter för att skapa ett huvudnamn för tjänsten så visas ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f4e65-124">If your account does not have sufficient permissions to create a service principal, you see an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="f4e65-125">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4e65-125">Contact your Azure Active Directory admin to create a service principal.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="f4e65-126">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="f4e65-126">Manage service principal roles</span></span> 

<span data-ttu-id="f4e65-127">Azure CLI 2.0 tillhandahåller följande kommandon för att hantera rolltilldelningar.</span><span class="sxs-lookup"><span data-stu-id="f4e65-127">The Azure CLI 2.0 provides the following commands to manage role assignments.</span></span>

* [<span data-ttu-id="f4e65-128">az-rolltilldelningslista</span><span class="sxs-lookup"><span data-stu-id="f4e65-128">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="f4e65-129">skapa az-rolltilldelning</span><span class="sxs-lookup"><span data-stu-id="f4e65-129">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="f4e65-130">ta bort az-rolltilldelning</span><span class="sxs-lookup"><span data-stu-id="f4e65-130">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="f4e65-131">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="f4e65-131">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="f4e65-132">Den här rollen har fullständiga behörigheter att läsa och skriva till ett Azure-konto och är vanligtvis inte lämplig för program.</span><span class="sxs-lookup"><span data-stu-id="f4e65-132">This role has full permissions to read and write to an Azure account, and is usually not appropriate for applications.</span></span> <span data-ttu-id="f4e65-133">Rollen **Läsare** är mer begränsad och tillhandahåller endast åtkomst för att läsa.</span><span class="sxs-lookup"><span data-stu-id="f4e65-133">The **Reader** role is more restrictive, providing read-only access.</span></span>  <span data-ttu-id="f4e65-134">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="f4e65-134">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="f4e65-135">I det här exemplet lägger vi till rollen **Läsare** och tar bort rollen **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="f4e65-135">This example adds the **Reader** role and deletes the **Contributor** one.</span></span>

```azurecli
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

<span data-ttu-id="f4e65-136">När en roll läggs till ändras _inte_ eventuella tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="f4e65-136">Adding a role does _not_ change any previously assigned permissions.</span></span> <span data-ttu-id="f4e65-137">När du begränsar behörigheter för tjänstens huvudnamn bör rollen __Deltagare__ alltid tas bort.</span><span class="sxs-lookup"><span data-stu-id="f4e65-137">When restricting a service principal's permissions, the __Contributor__ role should always be removed.</span></span>

<span data-ttu-id="f4e65-138">Ändringarna kan bekräftas genom att ange de roller som är tilldelade.</span><span class="sxs-lookup"><span data-stu-id="f4e65-138">The changes can be verified by listing the assigned roles.</span></span>

```azurecli
az role assignment list --assignee APP_ID
```

> [!NOTE] 
> <span data-ttu-id="f4e65-139">Om ditt konto inte har behörigheter att tilldela en roll så visas ett felmeddelande om att ditt konto "inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write" för omfånget "/subscriptions/{guid}". Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="f4e65-139">If your account doesn't have the permissions to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'." Contact your Azure Active Directory admin to manage roles.</span></span>

## <a name="log-in-using-the-service-principal"></a><span data-ttu-id="f4e65-140">Logga in med tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="f4e65-140">Log in using the service principal</span></span>

<span data-ttu-id="f4e65-141">Du kan testa inloggningen för den nya tjänstens huvudnamn och dess behörigheter genom att logga in med den i Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="f4e65-141">You can test the new service principal's login and permissions by logging in under it within the Azure CLI.</span></span> <span data-ttu-id="f4e65-142">Logga in med det nya huvudnamnet för tjänsten med hjälp av `appId`, `tenant` och autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="f4e65-142">Log in as the new service principal using the `appId`, `tenant`, and credentials values.</span></span> <span data-ttu-id="f4e65-143">Autentiseringsinformationen som du anger ändras beroende på om du har valt att skapa tjänstens huvudnamn med ett lösenord eller med ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="f4e65-143">The authentication information you provide changes based on whether you chose to create the service principal with a password, or a certificate.</span></span>

<span data-ttu-id="f4e65-144">Om du vill logga in med ett lösenord anger du det som en parameter i argumentet.</span><span class="sxs-lookup"><span data-stu-id="f4e65-144">To log in with a password, provide it as an argument parameter.</span></span>

```azurecli
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

<span data-ttu-id="f4e65-145">Om du vill logga in med ett certifikat så måste det vara tillgängligt lokalt som en PEM- eller DER-fil.</span><span class="sxs-lookup"><span data-stu-id="f4e65-145">To log in with a certificate, it must be available locally as a PEM or DER file.</span></span>

```azurecli
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```
## <a name="reset-credentials"></a><span data-ttu-id="f4e65-146">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="f4e65-146">Reset credentials</span></span>

<span data-ttu-id="f4e65-147">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten så kan de återställas med kommandot [az ad sp reset-credentials](https://docs.microsoft.com/en-us/cli/azure/ad/sp?view=azure-cli-latest#az_ad_sp_reset_credentials).</span><span class="sxs-lookup"><span data-stu-id="f4e65-147">In the event that you forget the credentials for a service principal, they can be reset with the [az ad sp reset-credentials](https://docs.microsoft.com/en-us/cli/azure/ad/sp?view=azure-cli-latest#az_ad_sp_reset_credentials) command.</span></span> <span data-ttu-id="f4e65-148">Samma begränsningar och alternativ för att skapa ett nytt huvudnamn för tjänsten gäller även här.</span><span class="sxs-lookup"><span data-stu-id="f4e65-148">The same restrictions and options for creating a new service principal also apply here.</span></span>

```azurecli
az ad sp reset-credentials --name APP_ID --password NEW_PASSWORD
```
