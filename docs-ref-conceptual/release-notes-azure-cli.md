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
ms.contentlocale: sv-SE
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="ef975-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="ef975-104">Azure CLI 2.0 release notes</span></span>

## <a name="may-10-2017"></a><span data-ttu-id="ef975-105">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="ef975-105">May 10, 2017</span></span>

<span data-ttu-id="ef975-106">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="ef975-106">Version 2.0.6</span></span>

* <span data-ttu-id="ef975-107">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="ef975-107">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="ef975-108">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="ef975-108">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="ef975-109">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="ef975-109">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="ef975-110">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="ef975-110">Include Cognitive Services module.</span></span>
* <span data-ttu-id="ef975-111">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="ef975-111">Include Service Fabric module.</span></span>
* <span data-ttu-id="ef975-112">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="ef975-112">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="ef975-113">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="ef975-113">Add support for CDN commands.</span></span>
* <span data-ttu-id="ef975-114">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="ef975-114">Remove Container module.</span></span>
* <span data-ttu-id="ef975-115">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="ef975-115">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="ef975-116">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ef975-116">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="ef975-117">Kärna</span><span class="sxs-lookup"><span data-stu-id="ef975-117">Core</span></span>

* <span data-ttu-id="ef975-118">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="ef975-118">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="ef975-119">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="ef975-119">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="ef975-120">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="ef975-120">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="ef975-121">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="ef975-121">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="ef975-122">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="ef975-122">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="ef975-123">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="ef975-123">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="ef975-124">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="ef975-124">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="ef975-125">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="ef975-125">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="ef975-126">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="ef975-126">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="ef975-127">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="ef975-127">core: Improved performance</span></span>
* <span data-ttu-id="ef975-128">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="ef975-128">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="ef975-129">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ef975-129">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="ef975-130">ACS</span><span class="sxs-lookup"><span data-stu-id="ef975-130">ACS</span></span>

* <span data-ttu-id="ef975-131">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="ef975-131">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="ef975-132">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="ef975-132">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="ef975-133">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="ef975-133">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="ef975-134">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="ef975-134">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="ef975-135">AppService</span><span class="sxs-lookup"><span data-stu-id="ef975-135">AppService</span></span>

* <span data-ttu-id="ef975-136">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="ef975-136">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="ef975-137">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="ef975-137">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="ef975-138">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="ef975-138">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="ef975-139">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="ef975-139">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="ef975-140">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="ef975-140">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="ef975-141">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="ef975-141">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="ef975-142">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="ef975-142">support slot swap with preview</span></span>
* <span data-ttu-id="ef975-143">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="ef975-143">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="ef975-144">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="ef975-144">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ef975-145">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ef975-145">CosmosDB</span></span>

* <span data-ttu-id="ef975-146">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="ef975-146">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="ef975-147">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="ef975-147">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="ef975-148">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="ef975-148">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="ef975-149">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="ef975-149">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ef975-150">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ef975-150">Data Lake Analytics</span></span>

* <span data-ttu-id="ef975-151">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="ef975-151">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="ef975-152">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="ef975-152">Add support for new catalog item type: package.</span></span> <span data-ttu-id="ef975-153">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="ef975-153">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="ef975-154">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="ef975-154">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="ef975-155">Tabell</span><span class="sxs-lookup"><span data-stu-id="ef975-155">Table</span></span>
  * <span data-ttu-id="ef975-156">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="ef975-156">Table valued function</span></span>
  * <span data-ttu-id="ef975-157">Visa</span><span class="sxs-lookup"><span data-stu-id="ef975-157">View</span></span>
  * <span data-ttu-id="ef975-158">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="ef975-158">Table Statistics.</span></span> <span data-ttu-id="ef975-159">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="ef975-159">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ef975-160">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ef975-160">Data Lake Store</span></span>

* <span data-ttu-id="ef975-161">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="ef975-161">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="ef975-162">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ef975-162">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="ef975-163">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="ef975-163">missed help for access show.</span></span> <span data-ttu-id="ef975-164">läggs till.</span><span class="sxs-lookup"><span data-stu-id="ef975-164">adding it.</span></span> <span data-ttu-id="ef975-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="ef975-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="ef975-166">Hitta</span><span class="sxs-lookup"><span data-stu-id="ef975-166">Find</span></span>

* <span data-ttu-id="ef975-167">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="ef975-167">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="ef975-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ef975-168">KeyVault</span></span>

* <span data-ttu-id="ef975-169">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="ef975-169">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="ef975-170">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef975-170">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="ef975-171">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="ef975-171">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="ef975-172">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="ef975-172">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="ef975-173">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="ef975-173">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="ef975-174">Labb</span><span class="sxs-lookup"><span data-stu-id="ef975-174">Lab</span></span>

* <span data-ttu-id="ef975-175">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ef975-175">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="ef975-176">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ef975-176">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="ef975-177">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ef975-177">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="ef975-178">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="ef975-178">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="ef975-179">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="ef975-179">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="ef975-180">Övervaka</span><span class="sxs-lookup"><span data-stu-id="ef975-180">Monitor</span></span>

* <span data-ttu-id="ef975-181">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="ef975-181">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="ef975-182">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="ef975-182">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="ef975-183">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ef975-183">Network</span></span>

* <span data-ttu-id="ef975-184">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="ef975-184">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="ef975-185">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="ef975-185">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="ef975-186">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ef975-186">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="ef975-187">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ef975-187">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="ef975-188">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef975-188">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="ef975-189">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="ef975-189">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="ef975-190">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="ef975-190">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="ef975-191">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="ef975-191">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="ef975-192">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="ef975-192">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="ef975-193">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="ef975-193">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="ef975-194">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="ef975-194">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="ef975-195">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="ef975-195">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="ef975-196">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="ef975-196">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="ef975-197">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="ef975-197">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="ef975-198">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="ef975-198">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="ef975-199">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="ef975-199">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="ef975-200">Profil</span><span class="sxs-lookup"><span data-stu-id="ef975-200">Profile</span></span>

* <span data-ttu-id="ef975-201">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="ef975-201">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="ef975-202">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="ef975-202">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="ef975-203">Redis</span><span class="sxs-lookup"><span data-stu-id="ef975-203">Redis</span></span>

* <span data-ttu-id="ef975-204">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="ef975-204">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="ef975-205">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="ef975-205">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="ef975-206">Resurs</span><span class="sxs-lookup"><span data-stu-id="ef975-206">Resource</span></span>

* <span data-ttu-id="ef975-207">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="ef975-207">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="ef975-208">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="ef975-208">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="ef975-209">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="ef975-209">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="ef975-210">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="ef975-210">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="ef975-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="ef975-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="ef975-212">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="ef975-212">Add docs for az lock update.</span></span> <span data-ttu-id="ef975-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="ef975-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="ef975-214">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="ef975-214">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="ef975-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="ef975-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="ef975-216">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="ef975-216">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="ef975-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="ef975-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="ef975-218">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="ef975-218">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="ef975-219">Roll</span><span class="sxs-lookup"><span data-stu-id="ef975-219">Role</span></span>

* <span data-ttu-id="ef975-220">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="ef975-220">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="ef975-221">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="ef975-221">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="ef975-222">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="ef975-222">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="ef975-223">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="ef975-223">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="ef975-224">SQL</span><span class="sxs-lookup"><span data-stu-id="ef975-224">SQL</span></span>

* <span data-ttu-id="ef975-225">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ef975-225">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="ef975-226">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="ef975-226">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="ef975-227">Lagring</span><span class="sxs-lookup"><span data-stu-id="ef975-227">Storage</span></span>

* <span data-ttu-id="ef975-228">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="ef975-228">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="ef975-229">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="ef975-229">Add support for incremental blob copy</span></span>
* <span data-ttu-id="ef975-230">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="ef975-230">Add support for large block blob upload</span></span>
* <span data-ttu-id="ef975-231">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="ef975-231">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="ef975-232">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ef975-232">VM</span></span>

* <span data-ttu-id="ef975-233">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="ef975-233">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="ef975-234">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="ef975-234">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="ef975-235">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="ef975-235">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="ef975-236">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="ef975-236">az vm/vmss disk</span></span>
  3. <span data-ttu-id="ef975-237">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="ef975-237">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="ef975-238">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="ef975-238">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="ef975-239">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="ef975-239">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="ef975-240">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="ef975-240">April 3, 2017</span></span>

<span data-ttu-id="ef975-241">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="ef975-241">Version 2.0.2</span></span>

<span data-ttu-id="ef975-242">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="ef975-242">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="ef975-243">Kärna</span><span class="sxs-lookup"><span data-stu-id="ef975-243">Core</span></span>

* <span data-ttu-id="ef975-244">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="ef975-244">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="ef975-245">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="ef975-245">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="ef975-246">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="ef975-246">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="ef975-247">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ef975-247">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ef975-248">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="ef975-248">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="ef975-249">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="ef975-249">Add prompting for missing template parameters.</span></span> <span data-ttu-id="ef975-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="ef975-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="ef975-251">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="ef975-251">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="ef975-252">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="ef975-252">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="ef975-253">ACS</span><span class="sxs-lookup"><span data-stu-id="ef975-253">ACS</span></span>

* [<span data-ttu-id="ef975-254">ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554</span><span class="sxs-lookup"><span data-stu-id="ef975-254">ACS] Adding support for configuring a default ACS cluster ([#2554</span></span>](https://github.com/Azure/azure-cli/pull/2554))
* <span data-ttu-id="ef975-255">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="ef975-255">Add support for ssh key password prompting.</span></span> <span data-ttu-id="ef975-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="ef975-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="ef975-257">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="ef975-257">Add support for windows clusters.</span></span> <span data-ttu-id="ef975-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="ef975-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="ef975-259">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="ef975-259">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="ef975-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="ef975-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="ef975-261">AppService</span><span class="sxs-lookup"><span data-stu-id="ef975-261">AppService</span></span>

* <span data-ttu-id="ef975-262">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="ef975-262">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="ef975-263">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="ef975-263">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="ef975-264">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="ef975-264">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="ef975-265">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="ef975-265">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="ef975-266">DataLake</span><span class="sxs-lookup"><span data-stu-id="ef975-266">DataLake</span></span>

* <span data-ttu-id="ef975-267">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="ef975-267">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="ef975-268">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="ef975-268">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="ef975-269">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="ef975-269">DocuemntDB</span></span>

* <span data-ttu-id="ef975-270">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="ef975-270">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="ef975-271">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ef975-271">VM</span></span>

* [<span data-ttu-id="ef975-272">Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570</span><span class="sxs-lookup"><span data-stu-id="ef975-272">Compute] Add AppGateway support to virtual machine scale set create ([#2570</span></span>](https://github.com/Azure/azure-cli/pull/2570))
* [<span data-ttu-id="ef975-273">VM/VMSS] Förbättrat stöd för cachelagring ([#2522</span><span class="sxs-lookup"><span data-stu-id="ef975-273">VM/VMSS] Improved disk caching support ([#2522</span></span>](https://github.com/Azure/azure-cli/pull/2522))
* <span data-ttu-id="ef975-274">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="ef975-274">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="ef975-275">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ef975-275">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ef975-276">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="ef975-276">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="ef975-277">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="ef975-277">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="ef975-278">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="ef975-278">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="ef975-279">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="ef975-279">February 27, 2017</span></span>

<span data-ttu-id="ef975-280">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="ef975-280">Version 2.0.0</span></span>

<span data-ttu-id="ef975-281">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="ef975-281">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="ef975-282">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="ef975-282">General availability applies to these command modules:</span></span>
- <span data-ttu-id="ef975-283">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="ef975-283">Container Service (acs)</span></span>
- <span data-ttu-id="ef975-284">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="ef975-284">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="ef975-285">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ef975-285">Networking</span></span>
- <span data-ttu-id="ef975-286">Storage</span><span class="sxs-lookup"><span data-stu-id="ef975-286">Storage</span></span>

<span data-ttu-id="ef975-287">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="ef975-287">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="ef975-288">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="ef975-288">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="ef975-289">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ef975-289">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
<span data-ttu-id="ef975-290">Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="ef975-290">You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="ef975-291">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="ef975-291">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="ef975-292">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="ef975-292">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="ef975-293">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="ef975-293">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="ef975-294">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="ef975-294">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="ef975-295">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="ef975-295">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="ef975-296">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="ef975-296">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="ef975-297">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="ef975-297">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="ef975-298">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="ef975-298">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="ef975-299">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="ef975-299">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="ef975-300">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ef975-300">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="ef975-301">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="ef975-301">Provide feedback from the command line with the `az feedback` command.</span></span>

