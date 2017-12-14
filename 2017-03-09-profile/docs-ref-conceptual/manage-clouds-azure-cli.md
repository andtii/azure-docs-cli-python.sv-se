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
ms.openlocfilehash: 0eb07d2919f6e640e1d594db9e18f9ada4d9f59f
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>Hantera flera moln med Azure CLI 2.0

Om du arbetar över olika regioner eller använder [Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/user/) kan du behöva använda mer än ett moln. Microsoft tillhandahåller moln för efterlevnad av regionala lagar som är tillgängliga för dig. I den här artikeln får du veta hur du skaffar information om moln som är tillgängliga för ditt konto, ändrar ditt aktuella moln och registrerar eller avregistrerar nya moln för användning med Azure Stack.

## <a name="listing-clouds"></a>Visa en lista över tillgängliga moln

Du kan visa en lista över dina tillgängliga moln med kommandot [cloud list](/cli/azure/cloud#list). På så sätt ser du vilket moln som är aktivt för närvarande och dess aktuella profil. Du får också information om regionala suffix och värdnamn.

Så här gör du för att hämta det aktiva molnet och en lista över alla tillgängliga moln:

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

Det aktiva molnet har `True` i kolumnen `IsActive`. Endast ett moln kan vara aktivt när som helst. Om du vill ha mer detaljerad information om ett moln, däribland slutpunkterna som molnet använder för Azure-tjänster, väljer du kommandot `cloud show`:

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

## <a name="switching-the-active-cloud"></a>Byta aktivt moln

Om du vill byta aktivt moln kör du kommandot [cloud set](/cli/azure/cloud#set). Det här kommandot kräver ett argument, namnet på molnet.

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> Om autentiseringen för det aktiverade molnet har upphört att gälla måste du autentisera igen innan du utför andra CLI-uppgifter. Om det är första gången du växlar till det nya molnet måste du också ange aktiv prenumeration.
> Mer information om autentisering finns i [Logga in med Azure CLI 2.0](authenticate-azure-cli.md). Mer information om prenumerationshantering finns i [Hantera Azure-prenumerationer med Azure CLI 2.0](manage-azure-subscriptions-azure-cli.md)

## <a name="register-a-cloud"></a>Registrera ett moln

Registrera ett nytt moln om du har egna slutpunkter för Azure Stack. Du registrerar ett nytt moln med kommandot [cloud register](/cli/azure/cloud#register). Det här kommandot kräver ett namn och en uppsättning funktioner med associerade slutpunkter. Mer information om hur du registrerar ett moln för användning med Azure Stack finns i [Install and configure CLI for use with Azure Stack](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack) (Installera och konfigurera CLI för användning med Azure Stack).

Du behöver inte registrera ditt eget moln för Kina, amerikanska myndigheter eller tyska regioner. Dessa hanteras av Microsoft och är tillgängliga som standard.  Mer information om alla tillgängliga inställningar för slutpunkter finns i [dokumentationen för `az cloud register`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register).

Registrering av ett moln innebär inte att man växlar till det automatiskt. Använd kommandot `az cloud set` för att välja det nyligen skapade molnet som beskrivs ovan.

## <a name="update-an-existing-cloud"></a>Uppdatera ett befintligt moln

Om du har behörighet kan du även uppdatera ett befintligt moln. Gör det när du måste växla till en annan Azure-profil, lägga till en slutpunkt eller ändra en slutpunkt.
Det gör du med kommandot `az cloud update`, som använder samma argument som `az cloud register`. Mer information finns i [dokumentationen för `az cloud update`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update).

## <a name="unregister-a-cloud"></a>Avregistrera ett moln

Om du inte längre behöver ett registrerat moln kan du avregistrera det med kommandot [cloud unregister](/cli/azure/cloud#unregister):

```azurecli
az cloud unregister --name MyCloud
```
