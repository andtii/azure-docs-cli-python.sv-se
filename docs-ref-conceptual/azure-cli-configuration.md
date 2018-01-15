---
title: "Konfigurationsalternativ för Azure CLI"
description: Konfigurera Azure CLI 2.0
keywords: "Azure CLI, konfiguration, inställningar, Azure"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 12/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 71d9f57846cb83591ca5e3d338735b3c525987af
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/06/2018
---
# <a name="azure-cli-20-configuration"></a>Azure CLI 2.0-konfiguration

Azure CLI 2.0 tillåter att användarkonfigurationen får åsidosätta interna inställningar som loggning och datainsamling, och tillhandahålla standardalternativ för vissa obligatoriska parametrar. CLI erbjuder ett bekvämlighetskommando för att hantera vissa av värdena, `az configure`, och andra värden som kan anges i en konfigurationsfil eller med miljövariabler.

Konfigurationsvärden som används av CLI utvärderas med följande prioritet, där poster som är högre upp på listan prioriteras.

1. Kommandoradsparametrar
2. Miljövariabler
3. Värdena i konfigurationsfilen eller -uppsättningen med `az configure`

## <a name="cli-configuration-with-az-configure"></a>CLI-konfiguration med az configure

Du anger standardvärden för CLI med kommandot [az configure](/cli/azure/?view=azure-cli-latest#az_configure).
Det här kommandot tar ett argument, `--defaults`, vilket är en blankstegsavgränsad lista över `key=value`-par. De angivna värdena används av CLI istället för obligatoriska argument. 

Följande är en lista över tillgängliga nycklar som du kan använda.

| Namn | Beskrivning |
|------|-------------|
| grupp | Standardresursgruppen som ska användas för alla kommandon. |
| location | Standardplatsen som ska användas för alla kommandon. |
| webb | Standardappnamnet som ska användas för alla `az webapp`-kommandon. |
| vm | Standardnamnet för VM som ska användas för alla `az vm`-kommandon. |
| vmss | Standardnamnet för VMSS som ska användas för alla `az vmss`-kommandon. |
| acr | Standardbehållarregistret som ska användas för alla `az acr`-kommandon. |
| acs | Standardbehållartjänsten som ska användas för alla `az acs`-kommandon. |

Här är ett exempel på hur du skulle ställa in standardresursgruppen och -platsen för alla kommandon.

```azurecli
az configure --defaults "location=westus2 group=MyResourceGroup"
```

## <a name="cli-configuration-file"></a>CLI-konfigurationsfil

CLI-konfigurationsfilen innehåller övriga inställningar som används för att hantera CLI-beteende. Själva konfigurationsfilen finns på `$AZURE_CONFIG_DIR/config`. Standardvärdet för `AZURE_CONFIG_DIR` är `$HOME/.azure/config` på Linux and macOS, och `%USERPROFILE%\.azure\config` för Windows. 

Konfigurationsfiler skrivs i INI-format. De här filerna består av avsnitt som börjar med en `[section-name]`-rubrik följd av en lista över `key=value`-poster. Avsnittsnamn är skiftlägeskänsliga, men nyckelnamnen är inte det.
Kommentarer är alla rader som börjar med `#` eller `;`. Infogade kommentarer tillåts inte. Booleska värden är skiftlägeskänsliga och representeras av följande värden.

* __Sant__: 1, ja, sant, på
* __Falskt__: 0, nej, falskt, av

Här är ett exempel på en CLI-konfigurationsfil som inaktiverar bekräftelseuppmaningar och ställer in loggning till katalogen `/var/log/azure`.

```
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

I nästa avsnitt finns information om alla tillgängliga konfigurationsvärden och vad de betyder. Fullständig information om INI-filformatet finns i [Python-dokumentationen om INI](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure).

## <a name="cli-configuration-values-and-environment-variables"></a>CLI-konfigurationsvärden och miljövariabler

I följande tabell finns alla avsnitt och alternativnamn som kan placera i en konfigurationsfil. Deras motsvarande miljövariabler kan anges som `AZURE_{section}_{name}`, i versaler. Du kan exempelvis ange `batchai`-avsnittets `storage_account`-standard i variabeln `AZURE_BATCHAI_STORAGE_ACCOUNT`.

Ett värde med en tillgänglig standard måste inte finnas i kommandoradsargumenten, även om det är obligatoriskt.

| Section | Namn      | Typ | Beskrivning|
|---------|-----------|------|------------|
| __kärna__ | utdata | sträng | Format för standardutdata. Kan vara något av `json`, `jsonc`, `tsv` eller `table`. |
| | inaktivera\_bekräfta\_uppmana | boolesk | Aktivera/inaktivera bekräftelsemeddelanden. |
| | samla in\_telemetri | boolesk | Tillåt att Microsoft samlar in anonyma data om CLI-användning. Sekretessinformation finns i [användningsvillkoren för Azure CLI 2.0](http://aka.ms/AzureCliLegal). |
| __loggning__ | aktivera\_loggfil\_ | boolesk | Slå på/av loggning. |
| | logg\_katalog | sträng | Katalogen som loggfiler ska skrivas i. Det är som standard `${AZURE_CONFIG_DIR}/logs`. |
| __lagring__ | anslutnings\_sträng | sträng | Standardanslutningssträngen för `az storage`-kommandon. |
| | konto | sträng | Standardkontonamnet för `az storage`-kommandon. |
| | key | sträng | Standardkontonyckeln för `az storage`-kommandon. |
| | sas\_token | sträng | SAS-standardtoken som ska användas för `az storage`-kommandon. |
| __batchai__ | lagrings\_konto | sträng | Standardlagringsnyckeln som ska användas för `az batchai`-kommandon. |
| | lagrings\_nyckel | sträng | Standardlagringsnyckeln som ska användas för `az batchai`-kommandon. |
| __batch__ | konto | sträng | Azure Batch-standardnamn som ska användas för `az batch`-kommandon. |
| | åtkomst\_nyckel | sträng | Standardåtkomstnyckeln som ska användas för `az batch`-kommandon. Ska endast användas med `aad`-auktorisering. |
| | slutpunkt | sträng | Standardslutpunkten att ansluta till för `az batch`-kommandon. |
| | ver\_läge | sträng | Verifieringsläge som ska användas för `az batch`-kommandon. Det kan vara `shared_key` eller `aad`. |

> [!NOTE]
> Det kan finnas andra värden i din konfigurationsfil, men de hanteras direkt via CLI-kommandon, däribland `az configure`. De som anges i tabellen ovan är den enda värden du bör ändra själv.
