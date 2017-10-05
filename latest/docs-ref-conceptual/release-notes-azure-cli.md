---
title: Viktig information om Azure CLI 2.0
description: "Lär dig mer om de senaste uppdateringarna till Azure CLI 2.0"
keywords: Viktig information om Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 72630c52b5e6afd69809ff19145717c0d65e0252
ms.sourcegitcommit: 3a490ae3a2a1b2e63a062806f9b720fa4c6be01e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/25/2017
---
# <a name="azure-cli-20-release-notes"></a>Viktig information om Azure CLI 2.0

## <a name="september-22-2017"></a>22 september 2017

Version 2.0.18

### <a name="resource"></a>Resurs

* Stöd har lagts till för att visa inbyggda principdefinitioner
* Stödlägesparametern har lagts till för att skapa principdefinitioner
* Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`
* [VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`

### <a name="network"></a>Nätverk

* Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`
* Stöd har lagts till för IPv6 Microsoft-peering till `express-route`
* Gruppkommandon för `asg`-programsäkerhet har lagts till
* Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`
* Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`
* Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`
* `network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till

### <a name="storage"></a>Lagring

* Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK

### <a name="eventgrid"></a>Eventgrid

* Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"

### <a name="sql"></a>SQL

* Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt. Om inget anges returneras alla sql-servrar i prenumerationen
* Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`

### <a name="keyvault"></a>KeyVault

* Stöd har lagts till för Keyvault-kommandon bakom en proxy

### <a name="vm"></a>Virtuell dator

* Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`
* Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel
* Argumentet `--asgs` har lagts till för `vm create`
* Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`
* [FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`
* Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`

### <a name="acs"></a>ACS

* [FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner

### <a name="appservice"></a>App Service

* Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till

### <a name="backup"></a>Säkerhetskopiering

* Förhandsversion


## <a name="september-11-2017"></a>11 september 2017

Version 2.0.17

### <a name="core"></a>Kärna

* Kommandomodulen kan ange eget korrelations-ID i telemetri
* Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge

### <a name="acs"></a>Acs

* Kommandot `acs list-locations` har lagts till
* Fick `ssh-key-file` att leverera förväntat standardvärde

### <a name="appservice"></a>App Service

* Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till

### <a name="cdn"></a>CDN

* "CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.

### <a name="extension"></a>Anknytning

* Första versionen.

### <a name="keyvault"></a>KeyVault

* Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.

### <a name="network"></a>Nätverk

* `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`
* Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`
* Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`
* SKU-stöd har lagts till för `lb create`
* SKU-stöd har lagts till för `public-ip create`

### <a name="resource"></a>Resurs

* Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`
* Tillåt att parametervärden anges för `policy assignment create`
* Tillåt att JSON eller fil för alla parametrar anges
* API-versionen har utökats

### <a name="sql"></a>SQL

* `sql server vnet-rule`-kommandon har lagts till

### <a name="vm"></a>Virtuell dator

* Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts
* Åtgärdat: Använd samma tilläggsnamn som portalen gör
* `subscription` har tagits bort från `[vm|vmss] create`-utmatningen
* Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning
* Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad

## <a name="august-31-2017"></a>31 augusti 2017

Version 2.0.16

### <a name="keyvault"></a>KeyVault

* Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats

### <a name="sf"></a>Sf

* Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)

### <a name="storage"></a>Lagring

* Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats
* Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts

## <a name="august-28-2017"></a>28 augusti 2017

Version 2.0.15

### <a name="cli"></a>CLI

* Tillkommen juridisk information för `--version`.

### <a name="acs"></a>ACS

* Regioner i förhandsversionen har korrigerats.
* `dns_name_prefix`-standardprefixet har formaterats korrekt.
* Utdata från acs-kommandot har optimerats.

### <a name="appservice"></a>App Service

* [VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats
* Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`
* `az webapp log show` har gjorts tillgängligt
* Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras
* Åtgärdat: Platsinställningar identifieras korrekt

### <a name="iot"></a>IoT

* Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas

### <a name="network"></a>Nätverk

* [VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`
* [VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`
* Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`
* SKU-stöd har lagts till för `lb create`
* SKU-stöd har lagts till för `public-ip create`

### <a name="profile"></a>Profil

* `--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator

### <a name="service-fabric"></a>Service Fabric

* Förhandsversion
* Förenklade användar- och lösenordsregler för registrering via kommando
* Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats
* Stöd har lagts till för tomma `registry_cred`

### <a name="storage"></a>Lagring

* Stöd har lagts till för att ställa in blobbnivå
* Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten
* Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`  
* Stöd har lagts till för tjänstkryptering med kundhanterade nycklar
* [VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`
* Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax

### <a name="vm"></a>Virtuell dator

* Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`
* Stöd har lagts till för `--lb-sku` för `vmss create`: 
* Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create` 
* Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning
* Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats
* Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`


## <a name="august-15-2017"></a>15 augusti 2017

Version 2.0.14

### <a name="acs"></a>ACS

* sshMaster0-portnumret för kubernetes har åtgärdats

### <a name="appservice"></a>App Service

* Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats

### <a name="event-grid"></a>Event Grid

* SDK-beroenden har lagts till

## <a name="august-11-2017"></a>11 augusti 2017

Version 2.0.13

### <a name="acs"></a>ACS

* Fler regioner har lagts till för förhandsversionen

### <a name="batch"></a>Batch

* Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0
* Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb
* En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats
* Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://”-prefix
* Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb
* Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions

### <a name="component"></a>Komponent

* En utfasningsvarning har lagts till för ”az component”-kommandon

### <a name="container"></a>Behållare

* `create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel


### <a name="data-lake-store"></a>Data Lake Store

* Stöd har lagts till för förloppskontroll

### <a name="event-grid"></a>Event Grid

* Första utgåvan

### <a name="network"></a>Nätverk

* `lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades
* `application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades
* `application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet
* Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`

### <a name="profile"></a>Profil

* `account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern

### <a name="storage"></a>Lagring

* Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter

### <a name="vm"></a>Virtuell dator

* `availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt
* Kommandot `list-skus` har gjorts tillgängligt
* Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar
* Använd lagrings-SKU när datadiskar ansluts
* Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort


## <a name="july-28-2017"></a>28 juli 2017

Version 2.0.12

* Behållarkommandon har lagts till
* Fakturerings- och förbrukningsmoduler har lagts till

```
azure-cli (2.0.12)  

acr (2.0.9)  
acs (2.0.11)  
appservice (0.1.11)  
batch (3.0.3)  
billing (0.1.3)  
cdn (0.0.6)  
cloud (2.0.7)  
cognitiveservices (0.1.6)  
command-modules-nspkg (2.0.1)  
component (2.0.6)  
configure (2.0.10)  
consumption (0.1.3)  
container (0.1.7)  
core (2.0.12)  
cosmosdb (0.1.11)  
dla (0.0.10)  
dls (0.0.11)  
feedback (2.0.6)  
find (0.2.6)  
interactive (0.3.7)  
iot (0.1.10)  
keyvault (2.0.8)  
lab (0.0.9)  
monitor (0.0.8)  
network (2.0.11)  
nspkg (3.0.1)  
profile (2.0.9)  
rdbms (0.0.5)  
redis (0.2.7)  
resource (2.0.11)  
role (2.0.9)  
sf (1.0.5)  
sql (2.0.8)  
storage (2.0.11)  
vm (2.0.11) 
```

### <a name="core"></a>Kärna

* Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat
* Undantag i distributionsförloppet har åtgärdats
* Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient
* Förbättrad samtidig hantering av clouds.config-filen (#3636)
* Uppdatera ID:t för klientbegäranden vid varje kommandokörning
* Skapa prenumerationsklienter med rätt SDK-profil (#3635)
* Förloppsrapportering för malldistributioner (#3510)
* Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)
* Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)
* Skapa prenumerationsklienter med rätt SDK-profil
* Flytta alla befintliga registreringsfiler till den senaste mappen
* Idempotens har åtgärdats för VM/VMSS-generering (#3586)
* Kommandosökvägar är inte längre skiftlägeskänsliga
* Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga
* Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack
* Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)

### <a name="acr"></a>ACR

* Kommandot `show-usage` har lagts till för hanterade register
* Stöd har lagts till för SKU-uppdatering för hanterade register
* Hanterade register med hanterad SKU har lagts till
* Webhooks har lagts till för hanterade register med komandomodulen acr webhook
* AAD-autentisering har lagts till med kommandot acr login
* Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar

### <a name="acs"></a>ACS

* Stöd för API-version 2017-07-01

### <a name="appservice"></a>App Service

* En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas
* Stöd har lagts till för att hämta autentiseringsuppgifter från ACR
* Ta bort alla kommandon under `appservice web`
* Maskera lösenord för Docker-register i kommandoutdata (#3656)
* Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)
* Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)
* Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)
* Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)
* `--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar. Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället

### <a name="batch"></a>Batch

* Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler
* `pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`
* `pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till

### <a name="cdn"></a>CDN

* Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.

### <a name="cloud"></a>Molnet

* API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD
* Slutpunkt för galleri krävs inte
* Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren
* Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs
* `endpoint_vm_image_alias_doc` har gjorts tillgängligt

### <a name="cosmosdb"></a>CosmosDB

* Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel
* Stöd har lagts till för standard-TTL för samlingar.

### <a name="data-lake-analytics"></a>Data Lake Analytics

* Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet
* `dla job pipeline show` har lagts till
* `dla job recurrence list` har lagts till

### <a name="data-lake-store"></a>Data Lake Store

* Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`
* SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats
* Kommandot `dls enable-key-vault` har lagts till. Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto

### <a name="interactive"></a>Interaktiv

* Förbättrade starttider med hjälp av cachelagrade kommandon
* Ökad täckning vid testning
* ”?”-gesten har förbättrats att även omfatta nästa kommando
* Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)
* `--version` tillåts som parameter för interaktivt läge (#3645)
* Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)
* Förloppsrapportering för malldistributioner (#3510)
* Flaggan `--progress` har lagts till
* `--debug` och `--verbose` har tagits bort från completion-händelser
* `interactive` har tagits bort från completion-händelser (#3324)

### <a name="iot"></a>IoT

* Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades. (#3934)

### <a name="key-vault"></a>Nyckelvalv

* Kommandon har lagts till för återställningsfunktioner för nyckelvalv:
  * `keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`
  * `keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`
  * `keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`
  * `keyvault key`-underkommandona `purge`, `recover`, `list-deleted`
* Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)
* Dataplanen för nyckelvalv har uppdaterats till 0.3.2. (#3307)

### <a name="lab"></a>Labb

* Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`
* Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`

### <a name="monitor"></a>Övervaka

* Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)
* `monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`
* `monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`
* `monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`
* `monitor alert-rules` har bytt namn till `monitor alert`
* `monitor alert create` har ändrats:
  * `condition`- och `action`-underkommandon accepterar inte längre JSON
  * Flera parametrar har lagts till för att förenkla genereringen av regler
  * `location` krävs inte längre
  * Namn- och ID-stöd har lagts till för mål
  * `--alert-rule-resource-name` har tagits bort
  * `is-enabled` har bytt namn till `enabled`; krävs inte längre
  * Nu baseras `description`-standardvärden på det angivna villkoret
  *  Exempel har lagts till för att förtydliga det nya formatet
* Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon
* Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`

### <a name="network"></a>Nätverk

* Kommandot `list-private-access-services` har lagts till
* Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`
* Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades
* Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`
* En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`
* `application-gateway redirect-config`-kommandon har lagts till
* Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`
* Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`
* Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`
* Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`
* Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`
* Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`
* Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`
* Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`
* Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`
* Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`
* Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till
* En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`
* Stöd har lagts till för `--dns-servers` för `vnet update`
* En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`
* En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`
* En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik
* Förbättrad formatering av utdata för `network list-usages`
* Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en
* Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en
* Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en
* Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en

### <a name="profile"></a>Profil

* Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet
* Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler
* Visa utfasningsvarningar när ”--expanded-view” används
* Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken
* Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer

### <a name="rdbms"></a>RDBMS

* Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)
* Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)
* Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)
* MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)

### <a name="resource"></a>Resurs

* Förbättrade prompter för parametrar som saknas för `group deployment create`
* Förbättrad parsning av `--parameters KEY=VALUE`-syntax
* Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen
* Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`
* En del parsnings- och felmeddelanden har åtgärdats (#3584)
* Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`
* Parameterkontroll har lagts till för mallar med mallänkar (#3629)
* Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax

### <a name="role"></a>Roll

* Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`
* Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)
* Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument 
* Visa utfasningsvarningar när `--expanded-view` används
* Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`

### <a name="service-fabric"></a>Service Fabric
* Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)
* Tester har lagts till för Service Fabric-kommandon (#3424)
* Flera Service Fabric-kommandon har åtgärdats (#3234)

### <a name="sql"></a>SQL

* Skadad `sql server create` `--identity`-parameter har tagits bort
* Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata
* Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till

### <a name="storage"></a>Lagring

* Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)
* Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS
* Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)
* Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)  
* Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592) 
* Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)

### <a name="vm"></a>Virtuell dator

* Stöd har lagts till för att konfigurera NSG
* En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt
* Stöd har lagts till för hanterade tjänstidentiteter
* Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.
* Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0


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
Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.

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

