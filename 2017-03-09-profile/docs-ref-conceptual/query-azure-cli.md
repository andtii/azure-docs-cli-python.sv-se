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
ms.openlocfilehash: b086785f7b20622111e0a05e7cc7c27ddb5449b5
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="4ded3-104">Använda JMESPath-frågor med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="4ded3-104">Using JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="4ded3-105">Azure CLI 2.0 använder parametern `--query` för att genomföra en [JMESPath-fråga](http://jmespath.org) på resultatet från `az`-kommandot.</span><span class="sxs-lookup"><span data-stu-id="4ded3-105">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="4ded3-106">JMESPath är ett kraftfullt frågespråk för JSON-utdata.</span><span class="sxs-lookup"><span data-stu-id="4ded3-106">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="4ded3-107">Om du inte är bekant med JMESPath-frågor finns det en självstudie på [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span><span class="sxs-lookup"><span data-stu-id="4ded3-107">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="4ded3-108">Parametern `Query` stöds av alla resurstyper (behållartjänster, webbappar, VM etc.) i Azure CLI 2.0 och kan användas i många olika syften.</span><span class="sxs-lookup"><span data-stu-id="4ded3-108">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="4ded3-109">Vi har angett flera exempel nedan.</span><span class="sxs-lookup"><span data-stu-id="4ded3-109">We have listed several examples below.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="4ded3-110">Välja enkla egenskaper</span><span class="sxs-lookup"><span data-stu-id="4ded3-110">Selecting simple properties</span></span>

<span data-ttu-id="4ded3-111">Det enkla kommandot `list` med `table`-utdataformat returnerar en granskad uppsättning av de vanligaste enkla egenskaperna för varje resurstyp i ett lättläst tabellformat.</span><span class="sxs-lookup"><span data-stu-id="4ded3-111">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

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

<span data-ttu-id="4ded3-112">Du kan använda parametern `--query` för att endast visa resursgruppnamnet och VM-namnet för alla virtuella maskiner i din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4ded3-112">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

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

<span data-ttu-id="4ded3-113">I föregående exempel ser du att kolumnrubrikerna är "Column1" och "Column2".</span><span class="sxs-lookup"><span data-stu-id="4ded3-113">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="4ded3-114">Du kan också lägga till egna etiketter eller namn på egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="4ded3-114">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="4ded3-115">I följande exempel vi har lagt till etiketterna "VMName" och "RGName" till de valda egenskaperna ”name" och "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4ded3-115">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


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

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="4ded3-116">Välja komplexa kapslade egenskaper</span><span class="sxs-lookup"><span data-stu-id="4ded3-116">Selecting complex nested properties</span></span>

<span data-ttu-id="4ded3-117">Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4ded3-117">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="4ded3-118">Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp från kommandot för listan över virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="4ded3-118">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

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

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="4ded3-119">Filtrera med contains-funktionen</span><span class="sxs-lookup"><span data-stu-id="4ded3-119">Filter with the contains function</span></span>

<span data-ttu-id="4ded3-120">Du kan använda JMESPath-funktionen `contains` för att förfina resultatet som returneras i frågan.</span><span class="sxs-lookup"><span data-stu-id="4ded3-120">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="4ded3-121">I följande exempel väljer kommandot endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="4ded3-121">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>

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

<span data-ttu-id="4ded3-122">Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1”.</span><span class="sxs-lookup"><span data-stu-id="4ded3-122">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

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

## <a name="filter-with-grep"></a><span data-ttu-id="4ded3-123">Filtrera med grep</span><span class="sxs-lookup"><span data-stu-id="4ded3-123">Filter with grep</span></span>

<span data-ttu-id="4ded3-124">Utdataformatet `tsv` är tabbavgränsad text utan rubriker.</span><span class="sxs-lookup"><span data-stu-id="4ded3-124">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="4ded3-125">De kan skickas till kommandon som `grep` och `cut` för att ytterligare parsa specifika värden från `list`-utdata.</span><span class="sxs-lookup"><span data-stu-id="4ded3-125">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="4ded3-126">I följande exempel väljer kommandot `grep` endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="4ded3-126">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="4ded3-127">Kommandot `cut` väljer endast att visa det åttonde fältvärdet (tabbavgränsat) i utdata.</span><span class="sxs-lookup"><span data-stu-id="4ded3-127">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="4ded3-128">Utforska med jpterm</span><span class="sxs-lookup"><span data-stu-id="4ded3-128">Explore with jpterm</span></span>

<span data-ttu-id="4ded3-129">Du kan också skicka kommandoutdata till [JMESPath-terminalen](https://github.com/jmespath/jmespath.terminal) och experimentera med din JMESPath-fråga där.</span><span class="sxs-lookup"><span data-stu-id="4ded3-129">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

