---
title: "Frågekommandoutdata med Azure CLI 2.0"
description: "Använd --query för att utföra JMESPath-frågor för utdata för Azure CLI 2.0-kommandon."
keywords: "Azure CLI 2.0, JMESPath, fråga, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 5979acc5-21a5-41e2-a4b6-3183bfe6aa22
ms.openlocfilehash: 8ab4a5e38f06199c5f044b8526c581828ba61927
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/18/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a>Använda JMESPath-frågor med Azure CLI 2.0

Azure CLI 2.0 använder parametern `--query` för att genomföra en [JMESPath-fråga](http://jmespath.org) på resultatet från `az`-kommandot. JMESPath är ett kraftfullt frågespråk för JSON-utdata.  Om du inte är bekant med JMESPath-frågor finns det en självstudie på [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).

Parametern `Query` stöds av alla resurstyper (behållartjänster, webbappar, VM etc.) i Azure CLI 2.0 och kan användas i många olika syften.  Vi har angett flera exempel nedan.

## <a name="selecting-simple-properties"></a>Välja enkla egenskaper

Det enkla kommandot `list` med `table`-utdataformat returnerar en granskad uppsättning av de vanligaste enkla egenskaperna för varje resurstyp i ett lättläst tabellformat.

```azurecli-interactive
az vm list --out table
```

```
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

Du kan använda parametern `--query` för att endast visa resursgruppnamnet och VM-namnet för alla virtuella maskiner i din prenumeration.

```azurecli-interactive
az vm list \
  --query [*].[name, resourceGroup] --out table
```

```
Column1     Column2
---------   -----------
DemoVM010   DEMORG1
demovm111   DEMORG1
demovm211   DEMORG1
demovm212   DEMORG1
demovm213   DEMORG1
demovm214   DEMORG1
demovm222   DEMORG1
KBDemo001VM RGDEMO001
KBDemo020   RGDEMO001
```

I föregående exempel ser du att kolumnrubrikerna är "Column1" och "Column2".  Du kan också lägga till egna etiketter eller namn på egenskaperna.  I följande exempel vi har lagt till etiketterna "VMName" och "RGName" till de valda egenskaperna ”name" och "resourceGroup".


```azurecli-interactive
az vm list \
  --query "[].{RGName:resourceGroup, VMName:name}" --out table
```

```
RGName     VMName
---------  -----------
DEMORG1    DemoVM010
DEMORG1    demovm111
DEMORG1    demovm211
DEMORG1    demovm212
DEMORG1    demovm213
DEMORG1    demovm214
DEMORG1    demovm222
RGDEMO001  KBDemo001VM
RGDEMO001  KBDemo020
```

## <a name="selecting-complex-nested-properties"></a>Välja komplexa kapslade egenskaper

Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen. Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp från kommandot för listan över virtuella datorer.

```azurecli-interactive
az vm list \
  --query "[].{VMName:name, OSType:storageProfile.osDisk.osType}" --out table
```

```
VMName       OSType
-----------  --------
DemoVM010    Linux
demovm111    Linux
demovm211    Linux
demovm212    Linux
demovm213    Linux
demovm214    Linux
demovm222    Linux
KBDemo001VM  Linux
KBDemo020    Linux
```

## <a name="filter-with-the-contains-function"></a>Filtrera med contains-funktionen

Du kan använda JMESPath-funktionen `contains` för att förfina resultatet som returneras i frågan.
I följande exempel väljer kommandot endast virtuella datorer som har texten "RGD" i sina namn.  

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup, 'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1”.

```azurecli-interactive
az vm list \
  --query "[?contains(hardwareProfile.vmSize, 'Standard_DS1')]" --out table
```

```
ResourceGroup    VMName     VmId                                  Location    ProvisioningState
---------------  ---------  ------------------------------------  ----------  -------------------
DEMORG1          DemoVM010  cbd56d9b-9340-44bc-a722-25f15b578444  westus      Succeeded
DEMORG1          demovm111  c1c024eb-3837-4075-9117-bfbc212fa7da  westus      Succeeded
DEMORG1          demovm211  95eda642-417f-4036-9475-67246ac0f0d0  westus      Succeeded
DEMORG1          demovm212  4bdac85d-c2f7-410f-9907-ca7921d930b4  westus      Succeeded
DEMORG1          demovm213  2131c664-221a-4b7f-9653-f6d542fbfa34  westus      Succeeded
DEMORG1          demovm214  48f419af-d27a-4df0-87f3-9481007c2e5a  westus      Succeeded
DEMORG1          demovm222  e0f59516-1d69-4d54-b8a2-f6c4a5d031de  westus      Succeeded
```

## <a name="filter-with-grep"></a>Filtrera med grep

Utdataformatet `tsv` är tabbavgränsad text utan rubriker. De kan skickas till kommandon som `grep` och `cut` för att ytterligare parsa specifika värden från `list`-utdata. I följande exempel väljer kommandot `grep` endast virtuella datorer som har texten "RGD" i sina namn.  Kommandot `cut` väljer endast att visa det åttonde fältvärdet (tabbavgränsat) i utdata.

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a>Utforska med jpterm

Du kan också skicka kommandoutdata till [JMESPath-terminalen](https://github.com/jmespath/jmespath.terminal) och experimentera med din JMESPath-fråga där.

```bash
pip install jmespath-terminal
az vm list | jpterm
```

