---
title: "Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0"
description: "Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure CLI 2.0."
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: 0ee794d5a732c6e8d2d52fca5810a874827930ae
ms.sourcegitcommit: 5a04b7fbb73a5f10c4021963ecd6ebe234cc3b61
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="6b5ad-104">Skapa Azure-tjänstens huvudnamn med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="6b5ad-104">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="6b5ad-105">Om du planerar att hantera appen eller tjänsten med Azure CLI 2.0 bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-105">If you plan to manage your app or service with Azure CLI 2.0, you should run it under an Azure Active Directory (AAD) service principal rather than your own credentials.</span></span>
<span data-ttu-id="6b5ad-106">Den här artikeln vägleder dig genom att skapa en säkerhetsprincip med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-106">This topic steps you through creating a security principal with Azure CLI 2.0.</span></span>

> [!NOTE]
> <span data-ttu-id="6b5ad-107">Du kan också skapa ett huvudnamn för tjänsten via Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-107">You can also create a service principal through the Azure portal.</span></span>
> <span data-ttu-id="6b5ad-108">Läs [Använd portalen för att skapa Active Directory-program och ett huvudnamn för tjänsten som får åtkomst till resurser](/azure/azure-resource-manager/resource-group-create-service-principal-portal) för mer information.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="6b5ad-109">Vad är ett huvudnamn för tjänsten?</span><span class="sxs-lookup"><span data-stu-id="6b5ad-109">What is a 'service principal'?</span></span>

<span data-ttu-id="6b5ad-110">Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="6b5ad-111">Se det som en användaridentitet (inloggning och lösenord eller certifikat) med en viss roll och väl kontrollerad behörighet att komma åt dina resurser.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-111">Think of it as a 'user identity' (login and password or certificate) with a specific role, and tightly controlled permissions to access your resources.</span></span> <span data-ttu-id="6b5ad-112">Den behöver bara kunna utföra vissa åtgärder, till skillnad från en allmän användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="6b5ad-113">Det ger bättre säkerhet om du bara ger den lägsta behörighetsnivån som krävs för att den ska kunna utföra sina administrativa uppgifter.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span> 

<span data-ttu-id="6b5ad-114">För närvarande stöder bara Azure CLI 2.0 skapande av lösenordsbaserade autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-114">Right now, Azure CLI 2.0 only supports the creation of password-based authentication credentials.</span></span> <span data-ttu-id="6b5ad-115">I det här avsnittet tar vi upp hur du skapar ett huvudnamn för tjänsten med ett specifikt lösenord och också hur du kan tilldela den specifika roller.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-115">In this topic, we cover creating a service principal with a specific password, and optionally assigning specific roles to it.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="6b5ad-116">Kontrollera din egen behörighetsnivå</span><span class="sxs-lookup"><span data-stu-id="6b5ad-116">Verify your own permission level</span></span>

<span data-ttu-id="6b5ad-117">Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-117">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="6b5ad-118">Du måste specifikt kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-118">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span> 

<span data-ttu-id="6b5ad-119">Det enklaste sättet att kontrollera om kontot har tillräcklig behörighet är via portalen.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-119">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="6b5ad-120">Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal.md#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="6b5ad-120">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal.md#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="6b5ad-121">Skapa ett huvudnamn för tjänsten för programmet</span><span class="sxs-lookup"><span data-stu-id="6b5ad-121">Create a service principal for your application</span></span>

<span data-ttu-id="6b5ad-122">Du måste ha något av följande för att identifiera appen du vill skapa tjänstens huvudnamn för:</span><span class="sxs-lookup"><span data-stu-id="6b5ad-122">You must have one of the following to identify the app you want to create a service principal for:</span></span>

  * <span data-ttu-id="6b5ad-123">Det unika namnet eller URI:n för den distribuerade appen (t.ex. "MyDemoWebApp" i följande exempel), eller</span><span class="sxs-lookup"><span data-stu-id="6b5ad-123">The unique name or URI of your deployed app (such as "MyDemoWebApp" in the examples), or</span></span>
  * <span data-ttu-id="6b5ad-124">program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet</span><span class="sxs-lookup"><span data-stu-id="6b5ad-124">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

<span data-ttu-id="6b5ad-125">Värdena identifierar ditt program när du skapar ett namn på huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-125">These values identify your application when creating a service principal.</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="6b5ad-126">Hämta information om programmet</span><span class="sxs-lookup"><span data-stu-id="6b5ad-126">Get information about your application</span></span>

<span data-ttu-id="6b5ad-127">Hämta identietsinformation om ditt program med `az ad app list`.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-127">Get identity information about your application with the `az ad app list`.</span></span>

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

<span data-ttu-id="6b5ad-128">Alternativet `--display-name` filtrerar den returnerade listan med appar för att vissa att dem med `displayName` börjar med MyDemoWebApp.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-128">The `--display-name` option filters the returned list of apps to show those with `displayName` starting with MyDemoWebApp.</span></span>

### <a name="create-the-service-principal"></a><span data-ttu-id="6b5ad-129">Skapa huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="6b5ad-129">Create the service principal</span></span>

<span data-ttu-id="6b5ad-130">Skapa huvudnamn för tjänsten med [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac).</span><span class="sxs-lookup"><span data-stu-id="6b5ad-130">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) to create the service principal.</span></span> 

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --password "{strong password}" 
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
 > <span data-ttu-id="6b5ad-131">Skapa inte ett osäkert lösenord.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-131">Don't create an insecure password.</span></span>  <span data-ttu-id="6b5ad-132">Följ vägledningen med [regler för lösenord och begränsningar i Azure AD](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="6b5ad-132">Follow the [Azure AD password rules and restrictions](/azure/active-directory/active-directory-passwords-policy) guidance.</span></span>

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="6b5ad-133">Hämta information om tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5ad-133">Get information about the service principal</span></span>

```azurecli-interactive
az ad sp show --id a487e0c1-82af-47d9-9a0b-af184eb87646d
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

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="6b5ad-134">Logga in med tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5ad-134">Sign in using the service principal</span></span>

<span data-ttu-id="6b5ad-135">Du kan nu logga in som det nya huvudnamnet för tjänsten för appen med hjälp av det *appId* och *lösenordet* från `az ad sp show`.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-135">You can now log in as the new service principal for your app using the *appId* and *password* from `az ad sp show`.</span></span>  <span data-ttu-id="6b5ad-136">Ange *klientvärdet* från resultatet av `az ad sp create-for-rbac`.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-136">Supply the *tenant* value from the results of `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password} --tenant {tenant}
``` 

<span data-ttu-id="6b5ad-137">Dessa utdata visas efter en lyckad inloggning:</span><span class="sxs-lookup"><span data-stu-id="6b5ad-137">You will see this output after a successful sign-on:</span></span>

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

<span data-ttu-id="6b5ad-138">Använd värdena `id`, `password` och `tenant` som autentiseringsuppgifter för att köra din app.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-138">Use the `id`, `password`, and `tenant` values as the credentials for running your app.</span></span> 

## <a name="managing-roles"></a><span data-ttu-id="6b5ad-139">Hantera roller</span><span class="sxs-lookup"><span data-stu-id="6b5ad-139">Managing roles</span></span> 

> [!NOTE]
> <span data-ttu-id="6b5ad-140">Rollbaserad åtkomst i Azure (RBAC) är en modell för att definiera och hantera roller för användar- och säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-140">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span>
> <span data-ttu-id="6b5ad-141">Rollerna är kopplade till en uppsättning med behörigheter, som avgör vilka resurser en princip kan läsa, få åtkomst till, skriva till eller hantera.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-141">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span>
> <span data-ttu-id="6b5ad-142">Mer information om RBAC och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="6b5ad-142">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="6b5ad-143">Azure CLI 2.0 tillhandahåller följande kommandon för att hantera rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="6b5ad-143">The Azure CLI 2.0 provides the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="6b5ad-144">az-rolltilldelningslista</span><span class="sxs-lookup"><span data-stu-id="6b5ad-144">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="6b5ad-145">skapa az-rolltilldelning</span><span class="sxs-lookup"><span data-stu-id="6b5ad-145">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="6b5ad-146">ta bort az-rolltilldelning</span><span class="sxs-lookup"><span data-stu-id="6b5ad-146">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="6b5ad-147">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-147">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="6b5ad-148">Det kanske inte är det bästa valet för appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-148">It may not be the best choice for an app's interactions with Azure services, given its broad permissions.</span></span> <span data-ttu-id="6b5ad-149">Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-149">The **Reader** role is more restrictive and is a good choice for read-only access.</span></span> <span data-ttu-id="6b5ad-150">Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-150">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="6b5ad-151">I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="6b5ad-151">In this example, add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

<span data-ttu-id="6b5ad-152">Bekräfta ändringarna genom att ange de roller som är tilldelade för närvarande:</span><span class="sxs-lookup"><span data-stu-id="6b5ad-152">Verify the changes by listing the currently assigned roles:</span></span>

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
> <span data-ttu-id="6b5ad-153">Om kontot inte har tillräcklig behörighet för att tilldela en roll får du ett felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-153">If your account does not have sufficient permissions to assign a role, you see an error message.</span></span>
> <span data-ttu-id="6b5ad-154">Meddelandet anger att ditt konto ”inte har behörighet att utföra åtgärden ”Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}”.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-154">The message states your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'."</span></span>
   
## <a name="change-the-credentials-of-a-security-principal"></a><span data-ttu-id="6b5ad-155">Ändra autentiseringsuppgifter för säkerhetsobjektet</span><span class="sxs-lookup"><span data-stu-id="6b5ad-155">Change the credentials of a security principal</span></span>

<span data-ttu-id="6b5ad-156">Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-156">It's a good security practice to review permissions and update passwords regularly.</span></span> <span data-ttu-id="6b5ad-157">Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-157">You may also want to manage and modify the security credentials as your app changes.</span></span>

### <a name="reset-a-service-principal-password"></a><span data-ttu-id="6b5ad-158">Återställa lösenord för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5ad-158">Reset a service principal password</span></span>

<span data-ttu-id="6b5ad-159">Återställ det aktuella lösenordet för tjänstens huvudnamn med `az ad sp reset-credentials`.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-159">Use `az ad sp reset-credentials` to reset the current password for the service principal.</span></span>

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

<span data-ttu-id="6b5ad-160">CLI genererar ett säkert lösenord om du hoppar över alternativet `--password`.</span><span class="sxs-lookup"><span data-stu-id="6b5ad-160">The CLI generates a secure password if you leave out the `--password` option.</span></span>