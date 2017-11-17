---
title: Hantera flera moln med Azure CLI 2.0
description: Skapa, logga in och hantera flera moln med Azure CLI 2.0.
keywords: Azure CLI 2.0, Azure, clouds, datacenters, government, region, china, germany
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="ec9fb-104">Hantera flera moln med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="ec9fb-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="ec9fb-105">Om du har flera prenumerationer som är associerade med Azure kan du ha mer än ett moln.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-105">If you have multiple subscriptions associated with Azure, you may have more than one cloud available.</span></span> <span data-ttu-id="ec9fb-106">Varje moln har sina egna associerade slutpunkter och funktioner, och är ofta kopplat till en viss region som har andra standarder eller krav vad gäller dataskydd.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-106">Each cloud has its own associated endpoints and capabilities, and is often associated with a particular region that has different data protection standards or requirements.</span></span>

<span data-ttu-id="ec9fb-107">För att effektivt arbeta med flera moln måste du kunna växla mellan dem, och ha möjlighet att skapa nya moln om det behövs.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-107">To effectively work with multiple clouds, you will need to be able to switch between which is currently active, and possibly create new clouds.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="ec9fb-108">Visa en lista över tillgängliga moln</span><span class="sxs-lookup"><span data-stu-id="ec9fb-108">Listing clouds</span></span>

<span data-ttu-id="ec9fb-109">Du kan visa en lista över dina tillgängliga moln med kommandot [cloud list](/cli/azure/cloud#list).</span><span class="sxs-lookup"><span data-stu-id="ec9fb-109">You may list your available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="ec9fb-110">På så sätt ser du vilket moln som är aktivt för närvarande och dess aktuella profil. Du får också information om regionala suffix och värdnamn.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-110">This will tell you which cloud is currently active, what its current profile is, and can provide information on regional suffixes and host names.</span></span>

<span data-ttu-id="ec9fb-111">Så här visar du dina tillgängliga moln och det moln som är aktivt för närvarande:</span><span class="sxs-lookup"><span data-stu-id="ec9fb-111">To get a list of the available clouds and the currently active one:</span></span>

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

## <a name="switching-the-active-cloud"></a><span data-ttu-id="ec9fb-112">Byta aktivt moln</span><span class="sxs-lookup"><span data-stu-id="ec9fb-112">Switching the active cloud</span></span>

<span data-ttu-id="ec9fb-113">Om du vill byta aktivt moln köra du kommandot [cloud set](/cli/azure/cloud#set).</span><span class="sxs-lookup"><span data-stu-id="ec9fb-113">In order to switch the currently active cloud, you run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="ec9fb-114">Det här kommandot kräver ett argument, namnet på molnet.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-114">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="ec9fb-115">Om du aldrig har autentiserat dig mot det aktiva molnet, måste du göra det innan du utför andra åtgärder i kommandoradsgränssnittet.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-115">If you have never authenticated for the active cloud, you will need to do so before performing any other CLI operations.</span></span> <span data-ttu-id="ec9fb-116">Mer information om autentisering finns i [Logga in med Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span><span class="sxs-lookup"><span data-stu-id="ec9fb-116">For instructions on authenticating, see [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="register-or-unregister-a-cloud"></a><span data-ttu-id="ec9fb-117">Registrera eller avregistrera ett moln</span><span class="sxs-lookup"><span data-stu-id="ec9fb-117">Register or unregister a cloud</span></span>

<span data-ttu-id="ec9fb-118">Registrera ett nytt moln om du har egna slutpunkter eller behöver en annan profil.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-118">Register a new cloud if you have your own endpoints or require a different profile.</span></span> <span data-ttu-id="ec9fb-119">Du registrerar ett nytt moln med kommandot [cloud register](/cli/azure/cloud#register).</span><span class="sxs-lookup"><span data-stu-id="ec9fb-119">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="ec9fb-120">Det här kommandot kräver ett namn. Om du vill kan du även ange en uppsättning funktioner och slutpunktsbeteckningar.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-120">This command requires a name, and optionally a set of capabilities and endpoint designations.</span></span>

<span data-ttu-id="ec9fb-121">Så här skapar du ett moln med en särskild slutpunkt för Resource Manager, och med en specifik profil:</span><span class="sxs-lookup"><span data-stu-id="ec9fb-121">To create a cloud with a specialized endpoint for the resource manager, with a specific profile:</span></span>

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

<span data-ttu-id="ec9fb-122">När du kör den här koden skapas molnet, men det väljs _inte_ automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-122">This creates the cloud, but does _not_ automatically select it.</span></span>

<span data-ttu-id="ec9fb-123">Om du inte längre behöver molnet som du skapat kan du avregistrera det med kommandot [cloud unregister](/cli/azure/cloud#unregister):</span><span class="sxs-lookup"><span data-stu-id="ec9fb-123">If you no longer require the created cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```

