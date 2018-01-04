---
title: Hantera flera moln med Azure CLI 2.0
description: Skapa, logga in och hantera flera moln med Azure CLI 2.0.
keywords: Azure CLI 2.0, Azure, clouds, datacenters, government, region, china, germany
author: sptramer
manager: routlaw
ms.author: sttramer
ms.date: 10/20/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 6f4cfec45becc0c4940e9066af53396b41db779d
ms.sourcegitcommit: 16426a08c0f2f62d0b9dca3df8132cece659acff
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/21/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="0bef9-104">Hantera flera moln med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="0bef9-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="0bef9-105">Om du arbetar över olika regioner eller använder [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/) kan du behöva använda mer än ett moln.</span><span class="sxs-lookup"><span data-stu-id="0bef9-105">If you work across different regions or use [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/), you may need to use more than one cloud.</span></span> <span data-ttu-id="0bef9-106">Microsoft tillhandahåller moln för efterlevnad av regionala lagar som är tillgängliga för dig.</span><span class="sxs-lookup"><span data-stu-id="0bef9-106">Microsoft provides clouds for compliance with regional laws, which are available for your use.</span></span> <span data-ttu-id="0bef9-107">I den här artikeln får du veta hur du skaffar information om moln som är tillgängliga för ditt konto, ändrar ditt aktuella moln och registrerar eller avregistrerar nya moln för användning med Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0bef9-107">This article shows you how to get information on clouds available to your account, change the current cloud, and register or unregister new clouds for use with Azure Stack.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="0bef9-108">Visa en lista över tillgängliga moln</span><span class="sxs-lookup"><span data-stu-id="0bef9-108">Listing clouds</span></span>

<span data-ttu-id="0bef9-109">Du kan visa en lista över dina tillgängliga moln med kommandot [cloud list](/cli/azure/cloud#list).</span><span class="sxs-lookup"><span data-stu-id="0bef9-109">You can list available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="0bef9-110">På så sätt ser du vilket moln som är aktivt för närvarande och dess aktuella profil. Du får också information om regionala suffix och värdnamn.</span><span class="sxs-lookup"><span data-stu-id="0bef9-110">This tells you which cloud is currently active, what its current profile is, and information on regional suffixes and host names.</span></span>

<span data-ttu-id="0bef9-111">Så här gör du för att hämta det aktiva molnet och en lista över alla tillgängliga moln:</span><span class="sxs-lookup"><span data-stu-id="0bef9-111">To get the active cloud and a list of all the available clouds:</span></span>

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

<span data-ttu-id="0bef9-112">Det aktiva molnet har `True` i kolumnen `IsActive`.</span><span class="sxs-lookup"><span data-stu-id="0bef9-112">The currently active cloud has `True` in the `IsActive` column.</span></span> <span data-ttu-id="0bef9-113">Endast ett moln kan vara aktivt när som helst.</span><span class="sxs-lookup"><span data-stu-id="0bef9-113">Only one cloud can be active at any time.</span></span> <span data-ttu-id="0bef9-114">Om du vill ha mer detaljerad information om ett moln, däribland slutpunkterna som molnet använder för Azure-tjänster, väljer du kommandot `cloud show`:</span><span class="sxs-lookup"><span data-stu-id="0bef9-114">To get more detailed information on a cloud, including the endpoints that it uses for Azure services, use the `cloud show` command:</span></span>

```azurecli
az cloud show --name AzureChinaCloud --output json
```

```output
{
  "endpoints": {
    "activeDirectory": "https://login.chinacloudapi.cn",
    "activeDirectoryDataLakeResourceId": null,
    "activeDirectoryGraphResourceId": "https://graph.chinacloudapi.cn/",
    "activeDirectoryResourceId": "https://management.core.chinacloudapi.cn/",
    "batchResourceId": "https://batch.chinacloudapi.cn/",
    "gallery": "https://gallery.chinacloudapi.cn/",
    "management": "https://management.core.chinacloudapi.cn/",
    "resourceManager": "https://management.chinacloudapi.cn",
    "sqlManagement": "https://management.core.chinacloudapi.cn:8443/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json"
  },
  "isActive": false,
  "name": "AzureChinaCloud",
  "profile": "latest",
  "suffixes": {
    "azureDatalakeAnalyticsCatalogAndJobEndpoint": null,
    "azureDatalakeStoreFileSystemEndpoint": null,
    "keyvaultDns": ".vault.azure.cn",
    "sqlServerHostname": ".database.chinacloudapi.cn",
    "storageEndpoint": "core.chinacloudapi.cn"
  }
}
```

## <a name="switching-the-active-cloud"></a><span data-ttu-id="0bef9-115">Byta aktivt moln</span><span class="sxs-lookup"><span data-stu-id="0bef9-115">Switching the active cloud</span></span>

<span data-ttu-id="0bef9-116">Om du vill byta aktivt moln kör du kommandot [cloud set](/cli/azure/cloud#set).</span><span class="sxs-lookup"><span data-stu-id="0bef9-116">To switch the currently active cloud, run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="0bef9-117">Det här kommandot kräver ett argument, namnet på molnet.</span><span class="sxs-lookup"><span data-stu-id="0bef9-117">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="0bef9-118">Om autentiseringen för det aktiverade molnet har upphört att gälla måste du autentisera igen innan du utför andra CLI-uppgifter.</span><span class="sxs-lookup"><span data-stu-id="0bef9-118">If your authentication for the activated cloud has expired, you need to re-authenticate before performing any other CLI tasks.</span></span> <span data-ttu-id="0bef9-119">Om det är första gången du växlar till det nya molnet måste du också ange aktiv prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0bef9-119">If this is your first time switching to the new cloud, you also need to set the active subscription.</span></span>
> <span data-ttu-id="0bef9-120">Mer information om autentisering finns i [Logga in med Azure CLI 2.0](authenticate-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="0bef9-120">For instructions on authenticating, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span> <span data-ttu-id="0bef9-121">Mer information om prenumerationshantering finns i [Hantera Azure-prenumerationer med Azure CLI 2.0](manage-azure-subscriptions-azure-cli.md)</span><span class="sxs-lookup"><span data-stu-id="0bef9-121">For information on subscription management, see [Manage Azure subscriptions with Azure CLI 2.0](manage-azure-subscriptions-azure-cli.md)</span></span>

## <a name="register-a-cloud"></a><span data-ttu-id="0bef9-122">Registrera ett moln</span><span class="sxs-lookup"><span data-stu-id="0bef9-122">Register a cloud</span></span>

<span data-ttu-id="0bef9-123">Registrera ett nytt moln om du har egna slutpunkter för Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0bef9-123">Register a new cloud if you have your own endpoints for Azure Stack.</span></span> <span data-ttu-id="0bef9-124">Du registrerar ett nytt moln med kommandot [cloud register](/cli/azure/cloud#register).</span><span class="sxs-lookup"><span data-stu-id="0bef9-124">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="0bef9-125">Det här kommandot kräver ett namn och en uppsättning funktioner med associerade slutpunkter.</span><span class="sxs-lookup"><span data-stu-id="0bef9-125">This command requires a name and a set of capabilities with associated endpoints.</span></span> <span data-ttu-id="0bef9-126">Mer information om hur du registrerar ett moln för användning med Azure Stack finns i [Install and configure CLI for use with Azure Stack](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack) (Installera och konfigurera CLI för användning med Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="0bef9-126">To learn how to register a cloud for use with Azure Stack, see [Install and configure CLI for use with Azure Stack](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack).</span></span>

<span data-ttu-id="0bef9-127">Du behöver inte registrera ditt eget moln för Kina, amerikanska myndigheter eller tyska regioner.</span><span class="sxs-lookup"><span data-stu-id="0bef9-127">You do not need to register your own cloud for China, US Government, or German regions.</span></span> <span data-ttu-id="0bef9-128">Dessa hanteras av Microsoft och är tillgängliga som standard.</span><span class="sxs-lookup"><span data-stu-id="0bef9-128">These are managed by Microsoft and available by default.</span></span>  <span data-ttu-id="0bef9-129">Mer information om alla tillgängliga inställningar för slutpunkter finns i [dokumentationen för `az cloud register`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register).</span><span class="sxs-lookup"><span data-stu-id="0bef9-129">For more information on all of the available endpoint settings, see the [documentation for `az cloud register`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register).</span></span>

<span data-ttu-id="0bef9-130">Registrering av ett moln innebär inte att man växlar till det automatiskt.</span><span class="sxs-lookup"><span data-stu-id="0bef9-130">Registering a cloud does not automatically switch to it.</span></span> <span data-ttu-id="0bef9-131">Använd kommandot `az cloud set` för att välja det nyligen skapade molnet som beskrivs ovan.</span><span class="sxs-lookup"><span data-stu-id="0bef9-131">Use the `az cloud set` command to select the newly created cloud as described above.</span></span>

## <a name="update-an-existing-cloud"></a><span data-ttu-id="0bef9-132">Uppdatera ett befintligt moln</span><span class="sxs-lookup"><span data-stu-id="0bef9-132">Update an existing cloud</span></span>

<span data-ttu-id="0bef9-133">Om du har behörighet kan du även uppdatera ett befintligt moln.</span><span class="sxs-lookup"><span data-stu-id="0bef9-133">If you have permissions, you can also update an existing cloud.</span></span> <span data-ttu-id="0bef9-134">Gör det när du måste växla till en annan Azure-profil, lägga till en slutpunkt eller ändra en slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="0bef9-134">Do this when you need to switch to a different Azure profile, add an endpoint, or change an endpoint.</span></span>
<span data-ttu-id="0bef9-135">Det gör du med kommandot `az cloud update`, som använder samma argument som `az cloud register`.</span><span class="sxs-lookup"><span data-stu-id="0bef9-135">You do this with the `az cloud update` command, which takes the same arguments as `az cloud register`.</span></span> <span data-ttu-id="0bef9-136">Mer information finns i [dokumentationen för `az cloud update`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update).</span><span class="sxs-lookup"><span data-stu-id="0bef9-136">For more information, see the [documentation for `az cloud update`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update).</span></span>

## <a name="unregister-a-cloud"></a><span data-ttu-id="0bef9-137">Avregistrera ett moln</span><span class="sxs-lookup"><span data-stu-id="0bef9-137">Unregister a cloud</span></span>

<span data-ttu-id="0bef9-138">Om du inte längre behöver ett registrerat moln kan du avregistrera det med kommandot [cloud unregister](/cli/azure/cloud#unregister):</span><span class="sxs-lookup"><span data-stu-id="0bef9-138">If you no longer require a registered cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```
