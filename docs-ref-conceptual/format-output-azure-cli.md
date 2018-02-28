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
# <a name="output-formats-for-azure-cli-20-commands"></a>Utdataformat för Azure CLI 2.0-kommandon

Azure CLI 2.0 använder json som standardalternativ för utdata, men erbjuder olika sätt för att formatera utdata från olika kommandon.  Använd parametrarna `--output` (eller `--out` eller `-o`) för att formatera kommandots utdata till någon av de utdatatyper som anges i följande tabell:

--resultat | Beskrivning
---------|-------------------------------
`json`   | JSON-sträng. Den här inställningen är standardinställningen.
`jsonc`  | Färglagd JSON.
`table`  | ASCII-tabell med nycklar som kolumnrubriker.
`tsv`    | Tabbavgränsade värden, utan nycklar

## <a name="json-output-format"></a>Format för JSON-utdata

Följande exempel visar en lista över virtuella datorer i dina prenumerationer i standardformatet json.

```azurecli
az vm list --output json
```

I följande utdata har vissa fält utelämnats av utrymmesskäl och identifieringsinformation har ersatts.

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

## <a name="table-output-format"></a>Format för tabellutdata

Utdataformatet `table` innehåller vanliga utdata som har formaterats som rader och kolumner med sorterade data, vilket gör det enkelt att läsa och söka igenom. Kapslade objekt ingår inte i tabellutdata, men kan fortfarande filtreras som en del av en fråga. Vissa fält utelämnas också från tabellinformationen så det här formatet passar bäst när du vill ha en snabb översikt över dina data.

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
Du kan använda parametern `--query` för att anpassa egenskaperna och kolumnerna du vill visa i bland listans utdata. I följande exempel visas hur du ska välja bara VM-namnets och resursgruppens namn i kommandot `list`.

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
> Vissa nycklar filtreras bort och skrivs inte ut i tabellvyn. Dessa är `id`, `type` och `etag`. Om du behöver se dessa i dina utdata kan du använda JMESPath-nyckelfunktionen för att ändra nyckelnamnet och undvika filtrering.
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

Mer information om hur du använder frågor för att filtrera data finns i [Använda JMESPath-frågor med Azure CLI 2.0](/cli/azure/query-azure-cli).

## <a name="tsv-output-format"></a>Format för TSV-utdata

`tsv`-utdataformatet returnerar tabbavgränsade värden och radmatningsavgränsade värden utan ytterligare formatering, nycklar eller andra symboler. I det här formatet är det enkelt att använda utdata i andra kommandon och verktyg som behöver bearbeta texten i någon form. I likhet med `table`-formatet skriver inte `tsv`-utdataalternativet ut kapslade objekt.

Om du använder följande exempel med alternativet `tsv` matas det tabbavgränsade resultatet ut.

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

I nästa exempel visas hur `tsv`-utdata kan skickas till andra kommandon på UNIX-system för att extrahera mer specifika data. Kommandot `grep` väljer objekt som innehåller texten "RGD", och sedan väljer kommandot `cut` det åttonde fältet (tabbavgränsat) för att visa namnet på den virtuella datorn i utdata.

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

För att det ska gå lättare att bearbeta tabbavgränsade fält är värdena i samma ordning som de visas i det utskrivna JSON-objektet. Den här ordningen är garanterat enhetlig mellan körningar av kommandot.

## <a name="set-the-default-output-format"></a>Ange standardutdataformatet

Använd det interaktiva kommandot `az configure` för att konfigurera din miljö och upprätta standardinställningar för utdataformat. Standardutdataformatet är `json`. 

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

Läs mer om hur du konfigurerar din miljö i informationen om [Azure CLI 2.0-konfiguration](/cli/azure/azure-cli-configuration).
