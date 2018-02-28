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
ms.openlocfilehash: ec96d1cb21b32cd982dbec5e4bf38110f8686c25
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/19/2018
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="464b2-103">Utdataformat för Azure CLI 2.0-kommandon</span><span class="sxs-lookup"><span data-stu-id="464b2-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="464b2-104">Azure CLI 2.0 använder json som standardalternativ för utdata, men erbjuder olika sätt för att formatera utdata från olika kommandon.</span><span class="sxs-lookup"><span data-stu-id="464b2-104">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="464b2-105">Använd parametrarna `--output` (eller `--out` eller `-o`) för att formatera kommandots utdata till någon av de utdatatyper som anges i följande tabell:</span><span class="sxs-lookup"><span data-stu-id="464b2-105">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table:</span></span>

<span data-ttu-id="464b2-106">--resultat</span><span class="sxs-lookup"><span data-stu-id="464b2-106">--output</span></span> | <span data-ttu-id="464b2-107">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="464b2-107">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="464b2-108">JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="464b2-108">JSON string.</span></span> <span data-ttu-id="464b2-109">Den här inställningen är standardinställningen.</span><span class="sxs-lookup"><span data-stu-id="464b2-109">This setting is the default.</span></span>
`jsonc`  | <span data-ttu-id="464b2-110">Färglagd JSON.</span><span class="sxs-lookup"><span data-stu-id="464b2-110">Colorized JSON.</span></span>
`table`  | <span data-ttu-id="464b2-111">ASCII-tabell med nycklar som kolumnrubriker.</span><span class="sxs-lookup"><span data-stu-id="464b2-111">ASCII table with keys as column headings.</span></span>
`tsv`    | <span data-ttu-id="464b2-112">Tabbavgränsade värden, utan nycklar</span><span class="sxs-lookup"><span data-stu-id="464b2-112">Tab-separated values, with no keys</span></span>

## <a name="json-output-format"></a><span data-ttu-id="464b2-113">Format för JSON-utdata</span><span class="sxs-lookup"><span data-stu-id="464b2-113">JSON output format</span></span>

<span data-ttu-id="464b2-114">Följande exempel visar en lista över virtuella datorer i dina prenumerationer i standardformatet json.</span><span class="sxs-lookup"><span data-stu-id="464b2-114">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli
az vm list --output json
```

<span data-ttu-id="464b2-115">I följande utdata har vissa fält utelämnats av utrymmesskäl och identifieringsinformation har ersatts.</span><span class="sxs-lookup"><span data-stu-id="464b2-115">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/.../resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
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

## <a name="table-output-format"></a><span data-ttu-id="464b2-116">Format för tabellutdata</span><span class="sxs-lookup"><span data-stu-id="464b2-116">Table output format</span></span>

<span data-ttu-id="464b2-117">Utdataformatet `table` innehåller vanliga utdata som har formaterats som rader och kolumner med sorterade data, vilket gör det enkelt att läsa och söka igenom.</span><span class="sxs-lookup"><span data-stu-id="464b2-117">The `table` output format provides plain output formatted as rows and columns of collated data, making it easy to read and scan.</span></span> <span data-ttu-id="464b2-118">Kapslade objekt ingår inte i tabellutdata, men kan fortfarande filtreras som en del av en fråga.</span><span class="sxs-lookup"><span data-stu-id="464b2-118">Nested objects are not included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="464b2-119">Vissa fält utelämnas också från tabellinformationen så det här formatet passar bäst när du vill ha en snabb översikt över dina data.</span><span class="sxs-lookup"><span data-stu-id="464b2-119">Some fields are also omitted from the table data, so this format is best when you want a quick, human-searchable overview of data.</span></span>

```azurecli
az vm list --out table
```

```output
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```
<span data-ttu-id="464b2-120">Du kan använda parametern `--query` för att anpassa egenskaperna och kolumnerna du vill visa i bland listans utdata.</span><span class="sxs-lookup"><span data-stu-id="464b2-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="464b2-121">I följande exempel visas hur du ska välja bara VM-namnets och resursgruppens namn i kommandot `list`.</span><span class="sxs-lookup"><span data-stu-id="464b2-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli
az vm list --query "[].{resource:resourceGroup, name:name}" -o table
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

> [!NOTE]
> <span data-ttu-id="464b2-122">Vissa nycklar filtreras bort och skrivs inte ut i tabellvyn.</span><span class="sxs-lookup"><span data-stu-id="464b2-122">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="464b2-123">Dessa är `id`, `type` och `etag`.</span><span class="sxs-lookup"><span data-stu-id="464b2-123">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="464b2-124">Om du behöver se dessa i dina utdata kan du använda JMESPath-nyckelfunktionen för att ändra nyckelnamnet och undvika filtrering.</span><span class="sxs-lookup"><span data-stu-id="464b2-124">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="464b2-125">Mer information om hur du använder frågor för att filtrera data finns i [Använda JMESPath-frågor med Azure CLI 2.0](/cli/azure/query-azure-cli).</span><span class="sxs-lookup"><span data-stu-id="464b2-125">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI 2.0](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="464b2-126">Format för TSV-utdata</span><span class="sxs-lookup"><span data-stu-id="464b2-126">TSV output format</span></span>

<span data-ttu-id="464b2-127">`tsv`-utdataformatet returnerar tabbavgränsade värden och radmatningsavgränsade värden utan ytterligare formatering, nycklar eller andra symboler.</span><span class="sxs-lookup"><span data-stu-id="464b2-127">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="464b2-128">I det här formatet är det enkelt att använda utdata i andra kommandon och verktyg som behöver bearbeta texten i någon form.</span><span class="sxs-lookup"><span data-stu-id="464b2-128">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="464b2-129">I likhet med `table`-formatet skriver inte `tsv`-utdataalternativet ut kapslade objekt.</span><span class="sxs-lookup"><span data-stu-id="464b2-129">Like the `table` format, the `tsv` output option does not print nested objects.</span></span>

<span data-ttu-id="464b2-130">Om du använder följande exempel med alternativet `tsv` matas det tabbavgränsade resultatet ut.</span><span class="sxs-lookup"><span data-stu-id="464b2-130">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli
az vm list --out tsv
```

```output
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010 None    None    westus  DemoVM010           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212 None    None    westus  demovm212           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213 None    None    westus  demovm213           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM None    None    westus  KBDemo001VM         None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines   14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus  KBDemo020           None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines    36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="464b2-131">I nästa exempel visas hur `tsv`-utdata kan skickas till andra kommandon på UNIX-system för att extrahera mer specifika data.</span><span class="sxs-lookup"><span data-stu-id="464b2-131">The next example shows how the `tsv` output can be piped to other commands on UNIX systems to extract more specific data.</span></span> <span data-ttu-id="464b2-132">Kommandot `grep` väljer objekt som innehåller texten "RGD", och sedan väljer kommandot `cut` det åttonde fältet (tabbavgränsat) för att visa namnet på den virtuella datorn i utdata.</span><span class="sxs-lookup"><span data-stu-id="464b2-132">The `grep` command selects items that have text "RGD" in them, and then the `cut` command selects the eighth field (separated by tabs) to show the name of the VM in output.</span></span>

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

<span data-ttu-id="464b2-133">För att det ska gå lättare att bearbeta tabbavgränsade fält är värdena i samma ordning som de visas i det utskrivna JSON-objektet.</span><span class="sxs-lookup"><span data-stu-id="464b2-133">For the purposes of processing tab-separated fields, the values are in the same order that they appear in the printed JSON object.</span></span> <span data-ttu-id="464b2-134">Den här ordningen är garanterat enhetlig mellan körningar av kommandot.</span><span class="sxs-lookup"><span data-stu-id="464b2-134">This order is guaranteed to be consistent between runs of the command.</span></span>

## <a name="set-the-default-output-format"></a><span data-ttu-id="464b2-135">Ange standardutdataformatet</span><span class="sxs-lookup"><span data-stu-id="464b2-135">Set the default output format</span></span>

<span data-ttu-id="464b2-136">Använd det interaktiva kommandot `az configure` för att konfigurera din miljö och upprätta standardinställningar för utdataformat.</span><span class="sxs-lookup"><span data-stu-id="464b2-136">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="464b2-137">Standardutdataformatet är `json`.</span><span class="sxs-lookup"><span data-stu-id="464b2-137">The default output format is `json`.</span></span> 

```azurecli
az configure
```

```output
Welcome to the Azure CLI! This command will guide you through logging in and setting some default values.

Your settings can be found at /home/defaultuser/.azure/config
Your current configuration is as follows:

  ...

Do you wish to change your settings? (y/N): y

What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab- and Newline-delimited, great for GREP, AWK, etc.
Please enter a choice [1]:
```

<span data-ttu-id="464b2-138">Läs mer om hur du konfigurerar din miljö i informationen om [Azure CLI 2.0-konfiguration](/cli/azure/azure-cli-configuration).</span><span class="sxs-lookup"><span data-stu-id="464b2-138">To learn more about configuring your environment, see [Azure CLI 2.0 configuration](/cli/azure/azure-cli-configuration).</span></span>
