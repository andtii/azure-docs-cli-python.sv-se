---
title: Hantera Azure-prenumerationer med Azure CLI 2.0
description: "Hantera Azure-prenumerationer med Azure CLI 2.0 på Linux, Mac eller Windows."
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 9f03e52fa72a8dbd5753904839a833db01ffb59b
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="85914-103">Hantera flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="85914-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="85914-104">De flesta Azure-användare har bara en enstaka prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85914-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="85914-105">Om du däremot är en del av flera organisationer eller om din organisation har delat upp åtkomst till vissa resurser i grupper kan du ha flera prenumerationer i Azure.</span><span class="sxs-lookup"><span data-stu-id="85914-105">However, if you are part of multiple organizations or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="85914-106">Du kan enkelt hantera flera prenumerationer med CLI, och du kan utföra åtgärder genom att välja en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85914-106">Multiple subscriptions can be easily managed with the CLI, and operations can be performed by selecting a subscription.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="85914-107">Klienter, användare och prenumerationer</span><span class="sxs-lookup"><span data-stu-id="85914-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="85914-108">Du kanske funderar över skillnaden mellan klienter, användare och prenumerationer i Azure.</span><span class="sxs-lookup"><span data-stu-id="85914-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="85914-109">I allmänhet är en _klient_ den Azure Active Directory-entitet som omfattar hela organisationen.</span><span class="sxs-lookup"><span data-stu-id="85914-109">In general, a _tenant_ is the Azure Active Directory entity which encompasses a whole organization.</span></span> <span data-ttu-id="85914-110">Klienten har minst en _prenumeration_ och _användare_.</span><span class="sxs-lookup"><span data-stu-id="85914-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="85914-111">En användare är en person och är endast associerad till en klient, vilken är organisationen som användaren tillhör.</span><span class="sxs-lookup"><span data-stu-id="85914-111">A user is an individual, and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="85914-112">Användare är de konton som loggar in på Azure för att etablera och använda resurser.</span><span class="sxs-lookup"><span data-stu-id="85914-112">Users are those accounts which log in to Azure to provision and use resources.</span></span> <span data-ttu-id="85914-113">En användare kan ha åtkomst till flera _prenumerationer_, som är avtal med Microsoft för användning av molntjänster, inklusive Azure.</span><span class="sxs-lookup"><span data-stu-id="85914-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="85914-114">Varje resurs är associerad med en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85914-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="85914-115">Om du vill veta mer om skillnaderna mellan klienter, användare och prenumerationer kan du läsa [ordlistan för molnterminologi i Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="85914-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>
<span data-ttu-id="85914-116">Om du vill lära dig att lägga till en ny prenumeration till din Azure Active Directory-klient läser du [Så här lägger du till en prenumeration i din Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="85914-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>

## <a name="working-with-multiple-subscriptions"></a><span data-ttu-id="85914-117">Arbeta med flera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="85914-117">Working with multiple subscriptions</span></span>

<span data-ttu-id="85914-118">För att komma åt de resurser som finns inom en prenumeration måste du byta aktiv prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85914-118">To access the resources contained within a subscription, you need to switch your active subscription.</span></span> <span data-ttu-id="85914-119">Allt arbete med prenumerationer görs via kommandot `az account`, vilket hänvisar till serviceavtalet som en prenumeration representerar och inte ditt individuella konto.</span><span class="sxs-lookup"><span data-stu-id="85914-119">All work with subscriptions is done through the `az account` command, which refers to the service agreement that a subscription represents and not your individual account.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

<span data-ttu-id="85914-120">När du ska börja arbeta med dina tillgängliga prenumerationer ska du skaffa en lista över dem som är tillgängliga för ditt konto:</span><span class="sxs-lookup"><span data-stu-id="85914-120">To start working with your available subscriptions, get a list of those available in your account:</span></span>

```azurecli-interactive
az account list --output table
```

```Output
Name                                         CloudName    SubscriptionId                        State     IsDefault
-------------------------------------------  -----------  ------------------------------------  --------  -----------
My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
```

<span data-ttu-id="85914-121">Du kan använda `az account set` för att ändra aktiv prenumeration:</span><span class="sxs-lookup"><span data-stu-id="85914-121">In order to change the active subscription, you can use `az account set`:</span></span>

```azurecli-interactive
az account set --subscription "My Demos"
```

<span data-ttu-id="85914-122">Du kan antingen använda prenumerations-ID eller prenumerationens namn för att välja prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="85914-122">You can use either the subscription ID or the subscription name to select the subscription.</span></span>
