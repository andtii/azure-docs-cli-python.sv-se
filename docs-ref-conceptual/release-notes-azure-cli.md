---
title: Viktig information om Azure CLI 2.0
description: "Lär dig mer om de senaste uppdateringarna till Azure CLI 2.0"
keywords: Viktig information om Azure CLI 2.0
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 56190b653ab9765017fffd1699056de7eae2db77
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: sv-SE
---
# <a name="azure-cli-20-release-notes"></a>Viktig information om Azure CLI 2.0

## <a name="april-3-2017"></a>3 april 2017

Version 2.0.2

Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.

```
azure-cli (2.0.2)
 
acr (2.0.0)
acs (2.0.2)
appservice (0.1.2)
batch (2.0.0)
cloud (2.0.0)
component (2.0.0)
configure (2.0.2)
container (0.1.2)
core (2.0.2)
documentdb (0.1.2)
feedback (2.0.0)
find (0.0.1b1)
iot (0.1.2)
keyvault (2.0.0)
lab (0.0.1)
monitor (0.0.1)
network (2.0.2)
nspkg (2.0.0)
profile (2.0.2)
redis (0.1.1b3)
resource (2.0.2)
role (2.0.1)
sql (2.0.0)
storage (2.0.2)
vm (2.0.2)
```

### <a name="core"></a>Kärna

* Lägg till acr, labb, övervaka och söka moduler i standardlistan.
* Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))
* inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))
* Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))
* Lägg till fråga om mallparametrar som saknas. ([#2364](https://github.com/Azure/azure-cli/pull/2364))
* Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm
* Stöder inloggning till specifik klient
 
### <a name="acs"></a>ACS

* [ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))
* Lägg till support för lösenordsfråga för ssh-nyckel. ([#2044](https://github.com/Azure/azure-cli/pull/2044))
* Lägg till stöd för Windows-kluster. ([#2211](https://github.com/Azure/azure-cli/pull/2211))
* Växla från rollen ägare till deltagare. ([#2321](https://github.com/Azure/azure-cli/pull/2321))
 
### <a name="appservice"></a>AppService

* appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))
* appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))
* appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))
* AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))
 
### <a name="datalake"></a>DataLake

* Första versionen av Data Lake Analytics-modulen.
* Första versionen av Data Lake Store-modulen.
 
### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>Virtuell dator

* [Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))
* Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>27 februari 2017

Version 2.0.0

Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".
Allmän tillgänglighet gäller för dessa kommandomoduler:
- Behållartjänst (acs)
- Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)
- Nätverk
- Storage

Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.
Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues).
Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
Du kan ge feedback från kommandoraden med kommandot `az feedback`.

Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.

Verifiera CLI-version med `az --version`.
Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.

```
azure-cli (2.0.0)

acs (2.0.0)
appservice (0.1.1b5)
batch (0.1.1b4)
cloud (2.0.0)
component (2.0.0)
configure (2.0.0)
container (0.1.1b4)
core (2.0.0)
documentdb (0.1.1b2)
feedback (2.0.0)
iot (0.1.1b3)
keyvault (0.1.1b5)
network (2.0.0)
nspkg (2.0.0)
profile (2.0.0)
redis (0.1.1b3)
resource (2.0.0)
role (2.0.0)
sql (0.1.1b5)
storage (2.0.0)
vm (2.0.0)
 
Python (Darwin) 2.7.10 (default, Jul 30 2016, 19:40:32) 
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]
```

> [!Note]
> En del av kommandomodulerna har postfixet "b*n*" eller "rc*n*".
> De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.

Vi har också nattliga förhandsversioner av CLI.
Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).

Du kan anmäla problem med nattliga förhandsversioner på följande sätt:
- Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues)
- Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
- Ge feedback från kommandoraden med kommandot `az feedback`.

