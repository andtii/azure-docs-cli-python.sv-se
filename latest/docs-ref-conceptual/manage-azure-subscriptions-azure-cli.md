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
# <a name="manage-multiple-azure-subscriptions"></a>Hantera flera Azure-prenumerationer

Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration.
Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer.
I så fall kan du konfigurera Azure CLI 2.0 för att köra kommandon mot en viss prenumeration.

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. Hämta en lista över alla prenumerationer i ditt konto.

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

1. Ange standard.
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > Parametern `--subscription` tar antingen prenumerationsnamnet eller prenumerations-ID:t.

Du kan verifiera ändringen genom att köra kommandot `az account list --output table` igen.

När du ställer in din standardprenumeration körs alla efterföljande Azure CLI-kommandon mot den här prenumerationen.