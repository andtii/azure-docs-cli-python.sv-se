---
title: Hantera Azure-prenumerationer med Azure CLI 2.0
description: "Hantera Azure-prenumerationer med Azure CLI 2.0 på Linux, Mac eller Windows."
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, prenumeration
author: kamaljit
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: 383fb6ebd90ac79f60869187b402d53d4f1791fd
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/05/2017
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="efb1d-104">Hantera flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="efb1d-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="efb1d-105">Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="efb1d-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="efb1d-106">Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="efb1d-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="efb1d-107">I så fall kan du konfigurera Azure CLI 2.0 för att köra kommandon mot en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="efb1d-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. <span data-ttu-id="efb1d-108">Hämta en lista över alla prenumerationer i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="efb1d-108">Get a list of all subscriptions in your account.</span></span>

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

1. <span data-ttu-id="efb1d-109">Ange standard.</span><span class="sxs-lookup"><span data-stu-id="efb1d-109">Set the default.</span></span>
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > <span data-ttu-id="efb1d-110">Parametern `--subscription` tar antingen prenumerationsnamnet eller prenumerations-ID:t.</span><span class="sxs-lookup"><span data-stu-id="efb1d-110">The `--subscription` parameter takes either the subscription name or the subscription ID.</span></span>

<span data-ttu-id="efb1d-111">Du kan verifiera ändringen genom att köra kommandot `az account list --output table` igen.</span><span class="sxs-lookup"><span data-stu-id="efb1d-111">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="efb1d-112">När du ställer in din standardprenumeration körs alla efterföljande Azure CLI-kommandon mot den här prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="efb1d-112">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>