---
title: "Frågekommandoutdata med Azure CLI 2.0"
description: "Lär dig hur du utför JMESPath-frågor för utdata för Azure CLI 2.0-kommandon."
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 98bc35c1e8136231011a2303901f42c68c9a7758
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="aa50c-103">Använda JMESPath-frågor med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="aa50c-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="aa50c-104">Azure CLI 2.0 använder parametern `--query` för att genomföra en [JMESPath-fråga](http://jmespath.org) på resultatet från `az`-kommandot.</span><span class="sxs-lookup"><span data-stu-id="aa50c-104">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="aa50c-105">JMESPath är ett kraftfullt frågespråk för JSON-utdata.</span><span class="sxs-lookup"><span data-stu-id="aa50c-105">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="aa50c-106">Om du inte är bekant med JMESPath-frågor finns det en självstudie på [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span><span class="sxs-lookup"><span data-stu-id="aa50c-106">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="aa50c-107">Parametern `Query` stöds av alla resurstyper (behållartjänster, webbappar, VM etc.) i Azure CLI 2.0 och kan användas i många olika syften.</span><span class="sxs-lookup"><span data-stu-id="aa50c-107">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="aa50c-108">Vi har angett flera exempel nedan.</span><span class="sxs-lookup"><span data-stu-id="aa50c-108">We have listed several examples below.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="aa50c-109">Välja enkla egenskaper</span><span class="sxs-lookup"><span data-stu-id="aa50c-109">Select simple properties</span></span>

<span data-ttu-id="aa50c-110">Det enkla kommandot `list` med `table`-utdataformat returnerar en granskad uppsättning av de vanligaste enkla egenskaperna för varje resurstyp i ett lättläst tabellformat.</span><span class="sxs-lookup"><span data-stu-id="aa50c-110">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

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

<span data-ttu-id="aa50c-111">Du kan använda parametern `--query` för att endast visa resursgruppnamnet och VM-namnet för alla virtuella maskiner i din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="aa50c-111">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query "[].[name, resourceGroup]" --out table
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

<span data-ttu-id="aa50c-112">I föregående exempel ser du att kolumnrubrikerna är "Column1" och "Column2".</span><span class="sxs-lookup"><span data-stu-id="aa50c-112">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="aa50c-113">Du kan också lägga till egna etiketter eller namn på egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="aa50c-113">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="aa50c-114">I följande exempel vi har lagt till etiketterna "VMName" och "RGName" till de valda egenskaperna ”name" och "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="aa50c-114">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


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

## <a name="select-complex-nested-properties"></a><span data-ttu-id="aa50c-115">Välja komplexa kapslade egenskaper</span><span class="sxs-lookup"><span data-stu-id="aa50c-115">Select complex nested properties</span></span>

<span data-ttu-id="aa50c-116">Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen.</span><span class="sxs-lookup"><span data-stu-id="aa50c-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="aa50c-117">Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp från kommandot för listan över virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="aa50c-117">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

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

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="aa50c-118">Filtrera med contains-funktionen</span><span class="sxs-lookup"><span data-stu-id="aa50c-118">Filter with the contains function</span></span>

<span data-ttu-id="aa50c-119">Du kan använda JMESPath-funktionen `contains` för att förfina resultatet som returneras i frågan.</span><span class="sxs-lookup"><span data-stu-id="aa50c-119">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="aa50c-120">I följande exempel väljer kommandot endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="aa50c-120">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>

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

<span data-ttu-id="aa50c-121">Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1”.</span><span class="sxs-lookup"><span data-stu-id="aa50c-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

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

## <a name="filter-with-grep"></a><span data-ttu-id="aa50c-122">Filtrera med grep</span><span class="sxs-lookup"><span data-stu-id="aa50c-122">Filter with grep</span></span>

<span data-ttu-id="aa50c-123">Utdataformatet `tsv` är tabbavgränsad text utan rubriker.</span><span class="sxs-lookup"><span data-stu-id="aa50c-123">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="aa50c-124">De kan skickas till kommandon som `grep` och `cut` för att ytterligare parsa specifika värden från `list`-utdata.</span><span class="sxs-lookup"><span data-stu-id="aa50c-124">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="aa50c-125">I följande exempel väljer kommandot `grep` endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="aa50c-125">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="aa50c-126">Kommandot `cut` väljer endast att visa det åttonde fältvärdet (tabbavgränsat) i utdata.</span><span class="sxs-lookup"><span data-stu-id="aa50c-126">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="aa50c-127">Utforska med jpterm</span><span class="sxs-lookup"><span data-stu-id="aa50c-127">Explore with jpterm</span></span>

<span data-ttu-id="aa50c-128">Du kan också skicka kommandoutdata till [JMESPath-terminalen](https://github.com/jmespath/jmespath.terminal) och experimentera med din JMESPath-fråga där.</span><span class="sxs-lookup"><span data-stu-id="aa50c-128">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

