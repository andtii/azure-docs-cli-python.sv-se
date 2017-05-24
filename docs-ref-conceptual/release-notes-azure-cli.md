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
ms.openlocfilehash: 3bd4b9c059da3b841fc0757a11bc7ce78ec64b08
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a>Viktig information om Azure CLI 2.0

## <a name="may-10-2017"></a>10 maj 2017

Version 2.0.6

* documentdb byter namn till cosmosdb
* Lägg till rdbms (mysql, postgres)
* Ta med Data Lake Analytics- och Data Lake Store-moduler.
* Ta med Cognitive Services-modul.
* Ta med Service Fabric-modul.
* Ta med interaktiv modul (har bytt namn från az-shell).
* Lägg till stöd för CDN-kommandon.
* Ta bort behållarmodul.
* Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))
* Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))

```
azure-cli (2.0.6)

acr (2.0.4)
acs (2.0.6)
appservice (0.1.6)
batch (2.0.4)
cdn (0.0.2)
cloud (2.0.2)
cognitiveservices (0.1.2)
command-modules-nspkg (2.0.0)
component (2.0.4)
configure (2.0.6)
core (2.0.6)
cosmosdb (0.1.6)
dla (0.0.6)
dls (0.0.6)
feedback (2.0.2)
find (0.2.2)
interactive (0.3.1)
iot (0.1.5)
keyvault (2.0.4)
lab (0.0.4)
monitor (0.0.4)
network (2.0.6)
nspkg (3.0.0)
profile (2.0.4)
rdbms (0.0.1)
redis (0.2.3)
resource (2.0.6)
role (2.0.4)
sf (1.0.1)
sql (2.0.3)
storage (2.0.6)
vm (2.0.6)
```

### <a name="core"></a>Kärna

* kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt   
* prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))
* Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))
* Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))
* Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))
* inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))
* kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))
* kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))
* kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))
* kärna: Förbättrad prestanda
* kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel
* kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts

### <a name="acs"></a>ACS

* korrigera antalet huvudservrar och agenter till heltal istället för strängar
* gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande
* gör ”az acs create --validate” tillgänglig för testverifieringar
* ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))

### <a name="appservice"></a>AppService

* functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.
* Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"
* Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)
* Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas
* Gör "webapp list-runtimes" tillgänglig
* stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))
* stöd för växling med förhandsgranskning
* Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))
* Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))

### <a name="cosmosdb"></a>CosmosDB

* Ändra documentdb-modulen till cosmosdb.
* Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar
* Stöd har lagts till för att aktivera automatisk redundans på databaskonton
* Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip

### <a name="data-lake-analytics"></a>Data Lake Analytics

* Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.
* Lägg till stöd för ny objekttyp i katalog: paket. nås via: `az dla catalog package`
* Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):

  * Tabell
  * Tabellvärdesfunktion
  * Visa
  * Tabellstatistik. Detta kan även anges med ett schema, men utan att ange ett tabellnamn.

### <a name="data-lake-store"></a>Data Lake Store

* Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.
* Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))
* hjälp vid visning av åtkomst saknas. läggs till. ([#2743](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>Hitta

* förbättra sökresultat och tillåt versionshantering i sökindexet

### <a name="keyvault"></a>KeyVault

* BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen
* BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.
* Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy
* Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.
* korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>Labb

* Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.
* Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.
* Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.
* Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.
* Lägg till kommandon för att hantera hemligheter i ett laboratorium.

### <a name="monitor"></a>Övervaka

* Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))
* Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>Nätverk

* Lägg till kommandot `network watcher test-connectivity`.
* Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.
* Lägg till stöd för anslutningstömning för Application Gateway.
* Lägg till stöd för konfiguration av WAF-regler för Application Gateway.
* Lägg till stöd för vägfilter och regler för ExpressRoute.
* Lägg till stöd för geografisk routning för TrafficManager.
* Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.
* Lägg till stöd för IPSec-principer för VPN-anslutning.
* Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.
* Lägg till stöd för aktiva-aktiva VNet-gatewayer
* Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.
* BC: Åtgärda fel i utdata för `vpn-connection create` 
* Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.
* Åtgärda fel i `dns zone import` där poster inte importerades korrekt.
* Åtgärda fel där `traffic-manager endpoint update` inte fungerade.
* Lägg till kommandon för förhandsversionen för ”network watcher”.

### <a name="profile"></a>Profil

* Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))
* Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache
* Gör att kommandot ”update-settings” blir föråldrat.

### <a name="resource"></a>Resurs

* Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))
* Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))
* Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))
* Åtgärda resursparsning och sökning efter API-version. ([#2781](https://github.com/Azure/azure-cli/issues/2781))
* Lägg till dokument för låsningsuppdatering för az. ([#2702](https://github.com/Azure/azure-cli/issues/2702))
* Fel om du försöker skapa en lista med resurser för en grupp som inte finns. ([#2769](https://github.com/Azure/azure-cli/issues/2769))
* [Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM. ([#2773](https://github.com/Azure/azure-cli/issues/2773))
* Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))

### <a name="role"></a>Roll

* create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))
* RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))
* roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))
* create-for-rbac: kontrollera att lösenordet som användaren anger hämtas

### <a name="sql"></a>SQL

* Kommandona az sql server list-usages och az sql db list-usages har lagts till.
* SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>Lagring

* Standardplats för resursgruppens plats för `storage account create`.
* Lägg till stöd för inkrementell blob-kopia
* Lägg till stöd för uppladdning av stor blockblob
* Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB

### <a name="vm"></a>Virtuell dator

* avail-set: gör antalet UD- och FD-domäner valfritt

  Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:
  1. az disk/snapshot/image
  2. az vm/vmss disk
  3. Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera
* vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras
* vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))


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
Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).
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
> En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.
> De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.

Vi har också nattliga förhandsversioner av CLI.
Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).

Du kan anmäla problem med nattliga förhandsversioner på följande sätt:
- Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)
- Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).
- Ge feedback från kommandoraden med kommandot `az feedback`.

