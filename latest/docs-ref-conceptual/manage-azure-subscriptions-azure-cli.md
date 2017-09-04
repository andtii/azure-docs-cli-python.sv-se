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
ms.openlocfilehash: c3538077e05d61f3c40880bb8b804226eb99dc85
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: sv-SE
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="23ea0-104">Hantera flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="23ea0-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="23ea0-105">Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="23ea0-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="23ea0-106">Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="23ea0-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="23ea0-107">I så fall kan du konfigurera Azure CLI 2.0 för att köra kommandon mot en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="23ea0-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="23ea0-108">Hämta en lista över alla prenumerationer i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="23ea0-108">Get a list of all subscriptions in your account.</span></span>

   ```azurecli
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. <span data-ttu-id="23ea0-109">Ange standard.</span><span class="sxs-lookup"><span data-stu-id="23ea0-109">Set the default.</span></span>
 
   ```azurecli
   az account set --subscription "My Demos"
   ```

<span data-ttu-id="23ea0-110">Du kan verifiera ändringen genom att köra kommandot `az account list --output table` igen.</span><span class="sxs-lookup"><span data-stu-id="23ea0-110">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="23ea0-111">När du ställer in din standardprenumeration körs alla efterföljande Azure CLI-kommandon mot den här prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="23ea0-111">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>