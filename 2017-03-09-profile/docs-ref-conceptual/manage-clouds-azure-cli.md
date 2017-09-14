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
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>Hantera flera moln med Azure CLI 2.0

Om du har flera prenumerationer som är associerade med Azure kan du ha mer än ett moln. Varje moln har sina egna associerade slutpunkter och funktioner, och är ofta kopplat till en viss region som har andra standarder eller krav vad gäller dataskydd.

För att effektivt arbeta med flera moln måste du kunna växla mellan dem, och ha möjlighet att skapa nya moln om det behövs.

## <a name="listing-clouds"></a>Visa en lista över tillgängliga moln

Du kan visa en lista över dina tillgängliga moln med kommandot [cloud list](/cli/azure/cloud#list). På så sätt ser du vilket moln som är aktivt för närvarande och dess aktuella profil. Du får också information om regionala suffix och värdnamn.

Så här visar du dina tillgängliga moln och det moln som är aktivt för närvarande:

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

## <a name="switching-the-active-cloud"></a>Byta aktivt moln

Om du vill byta aktivt moln köra du kommandot [cloud set](/cli/azure/cloud#set). Det här kommandot kräver ett argument, namnet på molnet.

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> Om du aldrig har autentiserat dig mot det aktiva molnet, måste du göra det innan du utför andra åtgärder i kommandoradsgränssnittet. Mer information om autentisering finns i [Logga in med Azure CLI 2.0](/cli/azure/authenticate-azure-cli).

## <a name="register-or-unregister-a-cloud"></a>Registrera eller avregistrera ett moln

Registrera ett nytt moln om du har egna slutpunkter eller behöver en annan profil. Du registrerar ett nytt moln med kommandot [cloud register](/cli/azure/cloud#register). Det här kommandot kräver ett namn. Om du vill kan du även ange en uppsättning funktioner och slutpunktsbeteckningar.

Så här skapar du ett moln med en särskild slutpunkt för Resource Manager, och med en specifik profil:

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

När du kör den här koden skapas molnet, men det väljs _inte_ automatiskt.

Om du inte längre behöver molnet som du skapat kan du avregistrera det med kommandot [cloud unregister](/cli/azure/cloud#unregister):

```azurecli
az cloud unregister --name MyCloud
```

