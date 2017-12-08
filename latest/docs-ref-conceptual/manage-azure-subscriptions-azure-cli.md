---
title: Hantera Azure-prenumerationer med Azure CLI 2.0
description: "Hantera Azure-prenumerationer med Azure CLI 2.0 på Linux, Mac eller Windows."
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, prenumeration
author: kamaljit
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: b4544d75aa279b5477f8497257d39182472fae71
ms.sourcegitcommit: 5db22de971cf3983785cb209d92cbed1bbd69ecf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/14/2017
---
# <a name="manage-multiple-azure-subscriptions"></a>Hantera flera Azure-prenumerationer

De flesta Azure-användare har bara en enstaka prenumeration. Om du däremot är en del av flera organisationer eller om din organisation har delat upp åtkomst till vissa resurser i grupper kan du ha flera prenumerationer i Azure. Du kan enkelt hantera flera prenumerationer med CLI, och du kan utföra åtgärder genom att välja en prenumeration.

## <a name="tenants-users-and-subscriptions"></a>Klienter, användare och prenumerationer

Du kanske funderar över skillnaden mellan klienter, användare och prenumerationer i Azure. I allmänhet är en _klient_ den Azure Active Directory-entitet som omfattar hela organisationen. Klienten har minst en _prenumeration_ och _användare_. En användare är en person och är endast associerad till en klient, vilken är organisationen som användaren tillhör. Användare är de konton som loggar in på Azure för att etablera och använda resurser. En användare kan ha åtkomst till flera _prenumerationer_, som är avtal med Microsoft för användning av molntjänster, inklusive Azure. Varje resurs är associerad med en prenumeration.

Om du vill veta mer om skillnaderna mellan klienter, användare och prenumerationer kan du läsa [ordlistan för molnterminologi i Azure](/azure/azure-glossary-cloud-terminology).
Om du vill lära dig att lägga till en ny prenumeration till din Azure Active Directory-klient läser du [Så här lägger du till en prenumeration i din Azure Active Directory](/en-us/azure/active-directory/active-directory-how-subscriptions-associated-directory).

## <a name="working-with-multiple-subscriptions"></a>Arbeta med flera prenumerationer

För att komma åt de resurser som finns inom en prenumeration måste du byta aktiv prenumeration. Allt arbete med prenumerationer görs via kommandot `az account`, vilket hänvisar till serviceavtalet som en prenumeration representerar och inte ditt individuella konto.

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

När du ska börja arbeta med dina tillgängliga prenumerationer ska du skaffa en lista över dem som är tillgängliga för ditt konto:

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

Du kan använda `az account set` för att ändra aktiv prenumeration:

```azurecli-interactive
az account set --subscription "My Demos"
```

Du kan antingen använda prenumerations-ID eller prenumerationens namn för att välja prenumerationen.
