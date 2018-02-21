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
# <a name="output-formats-for-azure-cli-20-commands"></a>Utdataformat för Azure CLI 2.0-kommandon

Azure CLI 2.0 använder json som standardalternativ för utdata, men erbjuder olika sätt för att formatera utdata från olika kommandon.  Använd parametrarna `--output` (eller `--out` eller `-o`) för att formatera kommandots utdata till någon av de utdatatyper som anges i följande tabell.

--resultat | Beskrivning
---------|-------------------------------
`json`   | json-sträng. `json` används som standard.
`jsonc`  | färgad json-sträng.
`table`  | tabell med kolumnrubriker.
`tsv`    | tabbavgränsade värden.

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a>Använda json-alternativet

Följande exempel visar en lista över virtuella datorer i dina prenumerationer i standardformatet json.

```azurecli-interactive
az vm list --output json
```

Resultatet är i det här formuläret (visar endast partiella utdata för att hålla det kortfattat).

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

## <a name="using-the-table-option"></a>Använda tabellalternativet

Tabellalternativet ger en lättläst uppsättning utdata, men tänk på att kapslade objekt inte ingår i utdata med enkla `--output table`, till skillnad från föregående .json-exempel.  Om du använder samma exempel med ”tabell”-utdataformat får du en granskad lista över de vanligaste egenskapsvärdena.

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

Du kan använda parametern `--query` för att anpassa egenskaperna och kolumnerna du vill visa i bland listans utdata. I följande exempel visas hur du ska välja bara VM-namnets och resursgruppens namn i kommandot `list`.

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

## <a name="using-the-tsv-option"></a>Använda tsv-alternativet

”Tsv”-utdataformatet returnerar enkla, textbaserade och tabbavgränsade utdata utan rubriker och bindestreck. I det här formatet är det enkelt att använda utdata i andra kommandon och verktyg som behöver bearbeta texten i någon form. Om du använder följande exempel med alternativet `tsv` matas det tabbavgränsade resultatet ut.

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

I nästa exempel visas hur `tsv`-utdata kan skickas till kommandon som `grep` och `cut` för att ytterligare parsa specifika värden från `list`-utdata. Kommandot `grep` väljer endast objekt som innehåller texten "RGD", och sedan väljer kommandot `cut` endast det åttonde fältvärdet (tabbavgränsat) för att visa det i utdata.

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a>Konfigurera format för standardutdata

Med kommandot `az configure` kan du konfigurera din miljö eller upprätta inställningar som standardinställningar för utdataformat. För vanlig användning är det enklaste standardutdataformatet ”tabellformatet” – välj **3** som utdataformat när du uppmanas att välja.

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```
