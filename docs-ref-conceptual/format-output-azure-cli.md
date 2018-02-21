---
title: "Utdataformat för Azure CLI 2.0"
description: "Lär dig hur du formaterar utdata från Azure CLI 2.0-kommandon till tabeller, listor eller JSON."
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a5d629675b468421e3abee41b9c8bffd7e96e5b0
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="afe69-103">Utdataformat för Azure CLI 2.0-kommandon</span><span class="sxs-lookup"><span data-stu-id="afe69-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="afe69-104">Azure CLI 2.0 använder json som standardalternativ för utdata, men erbjuder olika sätt för att formatera utdata från olika kommandon.</span><span class="sxs-lookup"><span data-stu-id="afe69-104">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="afe69-105">Använd parametrarna `--output` (eller `--out` eller `-o`) för att formatera kommandots utdata till någon av de utdatatyper som anges i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="afe69-105">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table.</span></span>

<span data-ttu-id="afe69-106">--resultat</span><span class="sxs-lookup"><span data-stu-id="afe69-106">--output</span></span> | <span data-ttu-id="afe69-107">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="afe69-107">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="afe69-108">json-sträng.</span><span class="sxs-lookup"><span data-stu-id="afe69-108">json string.</span></span> <span data-ttu-id="afe69-109">`json` används som standard.</span><span class="sxs-lookup"><span data-stu-id="afe69-109">`json` is the default.</span></span>
`jsonc`  | <span data-ttu-id="afe69-110">färgad json-sträng.</span><span class="sxs-lookup"><span data-stu-id="afe69-110">colorized json string.</span></span>
`table`  | <span data-ttu-id="afe69-111">tabell med kolumnrubriker.</span><span class="sxs-lookup"><span data-stu-id="afe69-111">table with column headings.</span></span>
`tsv`    | <span data-ttu-id="afe69-112">tabbavgränsade värden.</span><span class="sxs-lookup"><span data-stu-id="afe69-112">tab-separated values.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a><span data-ttu-id="afe69-113">Använda json-alternativet</span><span class="sxs-lookup"><span data-stu-id="afe69-113">Using the json option</span></span>

<span data-ttu-id="afe69-114">Följande exempel visar en lista över virtuella datorer i dina prenumerationer i standardformatet json.</span><span class="sxs-lookup"><span data-stu-id="afe69-114">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="afe69-115">Resultatet är i det här formuläret (visar endast partiella utdata för att hålla det kortfattat).</span><span class="sxs-lookup"><span data-stu-id="afe69-115">The results are in this form (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "demorg1"
        }
      ]
    },
          ...
          ...
          ...
]
```

## <a name="using-the-table-option"></a><span data-ttu-id="afe69-116">Använda tabellalternativet</span><span class="sxs-lookup"><span data-stu-id="afe69-116">Using the table option</span></span>

<span data-ttu-id="afe69-117">Tabellalternativet ger en lättläst uppsättning utdata, men tänk på att kapslade objekt inte ingår i utdata med enkla `--output table`, till skillnad från föregående .json-exempel.</span><span class="sxs-lookup"><span data-stu-id="afe69-117">The table option provides an easy to read set of output, but note that nested objects are not included in the output with the simple `--output table`, unlike the preceding .json example.</span></span>  <span data-ttu-id="afe69-118">Om du använder samma exempel med ”tabell”-utdataformat får du en granskad lista över de vanligaste egenskapsvärdena.</span><span class="sxs-lookup"><span data-stu-id="afe69-118">Using the same example with 'table' output format provides a curated list of most common property values.</span></span>

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

<span data-ttu-id="afe69-119">Du kan använda parametern `--query` för att anpassa egenskaperna och kolumnerna du vill visa i bland listans utdata.</span><span class="sxs-lookup"><span data-stu-id="afe69-119">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="afe69-120">I följande exempel visas hur du ska välja bara VM-namnets och resursgruppens namn i kommandot `list`.</span><span class="sxs-lookup"><span data-stu-id="afe69-120">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli-interactive
az vm list --query "[].{ resource: resourceGroup, name: name }" -o table
```

```
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

## <a name="using-the-tsv-option"></a><span data-ttu-id="afe69-121">Använda tsv-alternativet</span><span class="sxs-lookup"><span data-stu-id="afe69-121">Using the tsv option</span></span>

<span data-ttu-id="afe69-122">”Tsv”-utdataformatet returnerar enkla, textbaserade och tabbavgränsade utdata utan rubriker och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="afe69-122">'tsv' output format returns a simple text-based and tab-separated output with no headings and dashes.</span></span> <span data-ttu-id="afe69-123">I det här formatet är det enkelt att använda utdata i andra kommandon och verktyg som behöver bearbeta texten i någon form.</span><span class="sxs-lookup"><span data-stu-id="afe69-123">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="afe69-124">Om du använder följande exempel med alternativet `tsv` matas det tabbavgränsade resultatet ut.</span><span class="sxs-lookup"><span data-stu-id="afe69-124">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus  DemoVM010           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus  demovm212           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus  demovm213           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus  KBDemo001VM         None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines   14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None   None    westus  KBDemo020           None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="afe69-125">I nästa exempel visas hur `tsv`-utdata kan skickas till kommandon som `grep` och `cut` för att ytterligare parsa specifika värden från `list`-utdata.</span><span class="sxs-lookup"><span data-stu-id="afe69-125">The next example shows how the `tsv` output can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="afe69-126">Kommandot `grep` väljer endast objekt som innehåller texten "RGD", och sedan väljer kommandot `cut` endast det åttonde fältvärdet (tabbavgränsat) för att visa det i utdata.</span><span class="sxs-lookup"><span data-stu-id="afe69-126">The `grep` command selects only items that have text "RGD" in them and then the `cut` command selects only the eighth field (separated by tabs) value to show in the output.</span></span>

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a><span data-ttu-id="afe69-127">Konfigurera format för standardutdata</span><span class="sxs-lookup"><span data-stu-id="afe69-127">Setting the default output format</span></span>

<span data-ttu-id="afe69-128">Med kommandot `az configure` kan du konfigurera din miljö eller upprätta inställningar som standardinställningar för utdataformat.</span><span class="sxs-lookup"><span data-stu-id="afe69-128">You can use the `az configure` command to set up your environment or establish preferences such as default settings for output formats.</span></span> <span data-ttu-id="afe69-129">För vanlig användning är det enklaste standardutdataformatet ”tabellformatet” – välj **3** som utdataformat när du uppmanas att välja.</span><span class="sxs-lookup"><span data-stu-id="afe69-129">For common use, the easiest output format default is the "table" format - select **3** when prompted for output format choices.</span></span>

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```
