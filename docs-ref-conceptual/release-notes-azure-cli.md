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
ms.openlocfilehash: 39e4710a29ac57730919b82ab76b9c9a4b9ca786
ms.sourcegitcommit: 43d4f838d132ab9bcfa59dbda3b544c06373b6a9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/22/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="ce3be-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="ce3be-104">Azure CLI 2.0 release notes</span></span>

## <a name="august-15-2017"></a><span data-ttu-id="ce3be-105">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-105">August 15, 2017</span></span>

<span data-ttu-id="ce3be-106">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="ce3be-106">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="ce3be-107">ACS</span><span class="sxs-lookup"><span data-stu-id="ce3be-107">ACS</span></span>

* <span data-ttu-id="ce3be-108">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ce3be-108">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="ce3be-109">App Service</span><span class="sxs-lookup"><span data-stu-id="ce3be-109">Appservice</span></span>

* <span data-ttu-id="ce3be-110">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ce3be-110">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="ce3be-111">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ce3be-111">Event Grid</span></span>

* <span data-ttu-id="ce3be-112">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-112">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="ce3be-113">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-113">August 11, 2017</span></span>

<span data-ttu-id="ce3be-114">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="ce3be-114">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="ce3be-115">ACS</span><span class="sxs-lookup"><span data-stu-id="ce3be-115">ACS</span></span>

* <span data-ttu-id="ce3be-116">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="ce3be-116">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="ce3be-117">Batch</span><span class="sxs-lookup"><span data-stu-id="ce3be-117">Batch</span></span>

* <span data-ttu-id="ce3be-118">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ce3be-118">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="ce3be-119">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="ce3be-119">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="ce3be-120">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ce3be-120">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="ce3be-121">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://”-prefix</span><span class="sxs-lookup"><span data-stu-id="ce3be-121">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="ce3be-122">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="ce3be-122">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="ce3be-123">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="ce3be-123">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="ce3be-124">Komponent</span><span class="sxs-lookup"><span data-stu-id="ce3be-124">Component</span></span>

* <span data-ttu-id="ce3be-125">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="ce3be-125">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="ce3be-126">Behållare</span><span class="sxs-lookup"><span data-stu-id="ce3be-126">Container</span></span>

* <span data-ttu-id="ce3be-127">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="ce3be-127">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="ce3be-128">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ce3be-128">Data Lake Store</span></span>

* <span data-ttu-id="ce3be-129">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="ce3be-129">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="ce3be-130">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ce3be-130">Event Grid</span></span>

* <span data-ttu-id="ce3be-131">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="ce3be-131">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="ce3be-132">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ce3be-132">Network</span></span>

* <span data-ttu-id="ce3be-133">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="ce3be-133">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="ce3be-134">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="ce3be-134">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="ce3be-135">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="ce3be-135">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="ce3be-136">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="ce3be-136">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="ce3be-137">Profil</span><span class="sxs-lookup"><span data-stu-id="ce3be-137">Profile</span></span>

* <span data-ttu-id="ce3be-138">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="ce3be-138">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="ce3be-139">Lagring</span><span class="sxs-lookup"><span data-stu-id="ce3be-139">Storage</span></span>

* <span data-ttu-id="ce3be-140">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="ce3be-140">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="ce3be-141">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ce3be-141">VM</span></span>

* <span data-ttu-id="ce3be-142">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ce3be-142">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="ce3be-143">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ce3be-143">Exposed `list-skus` command</span></span>
* <span data-ttu-id="ce3be-144">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="ce3be-144">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="ce3be-145">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="ce3be-145">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="ce3be-146">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ce3be-146">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="ce3be-147">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-147">July 28, 2017</span></span>

<span data-ttu-id="ce3be-148">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="ce3be-148">Version 2.0.12</span></span>

* <span data-ttu-id="ce3be-149">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-149">Added container commands</span></span>
* <span data-ttu-id="ce3be-150">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-150">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="ce3be-151">Kärna</span><span class="sxs-lookup"><span data-stu-id="ce3be-151">Core</span></span>

* <span data-ttu-id="ce3be-152">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="ce3be-152">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="ce3be-153">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ce3be-153">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="ce3be-154">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="ce3be-154">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="ce3be-155">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="ce3be-155">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="ce3be-156">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="ce3be-156">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="ce3be-157">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="ce3be-157">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="ce3be-158">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="ce3be-158">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ce3be-159">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="ce3be-159">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="ce3be-160">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="ce3be-160">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="ce3be-161">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="ce3be-161">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="ce3be-162">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="ce3be-162">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="ce3be-163">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="ce3be-163">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="ce3be-164">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="ce3be-164">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="ce3be-165">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="ce3be-165">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="ce3be-166">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="ce3be-166">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="ce3be-167">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="ce3be-167">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="ce3be-168">ACR</span><span class="sxs-lookup"><span data-stu-id="ce3be-168">ACR</span></span>

* <span data-ttu-id="ce3be-169">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="ce3be-169">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="ce3be-170">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="ce3be-170">Support SKU update for managed registries</span></span>
* <span data-ttu-id="ce3be-171">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-171">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="ce3be-172">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="ce3be-172">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="ce3be-173">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="ce3be-173">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="ce3be-174">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="ce3be-174">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="ce3be-175">ACS</span><span class="sxs-lookup"><span data-stu-id="ce3be-175">ACS</span></span>

* <span data-ttu-id="ce3be-176">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="ce3be-176">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="ce3be-177">App Service</span><span class="sxs-lookup"><span data-stu-id="ce3be-177">Appservice</span></span>

* <span data-ttu-id="ce3be-178">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="ce3be-178">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="ce3be-179">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="ce3be-179">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="ce3be-180">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="ce3be-180">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="ce3be-181">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="ce3be-181">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="ce3be-182">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="ce3be-182">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="ce3be-183">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="ce3be-183">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="ce3be-184">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="ce3be-184">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="ce3be-185">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="ce3be-185">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="ce3be-186">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="ce3be-186">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="ce3be-187">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="ce3be-187">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="ce3be-188">Batch</span><span class="sxs-lookup"><span data-stu-id="ce3be-188">Batch</span></span>

* <span data-ttu-id="ce3be-189">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="ce3be-189">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="ce3be-190">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="ce3be-190">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="ce3be-191">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-191">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="ce3be-192">CDN</span><span class="sxs-lookup"><span data-stu-id="ce3be-192">CDN</span></span>

* <span data-ttu-id="ce3be-193">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="ce3be-193">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="ce3be-194">Molnet</span><span class="sxs-lookup"><span data-stu-id="ce3be-194">Cloud</span></span>

* <span data-ttu-id="ce3be-195">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="ce3be-195">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="ce3be-196">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="ce3be-196">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="ce3be-197">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="ce3be-197">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="ce3be-198">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="ce3be-198">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="ce3be-199">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ce3be-199">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ce3be-200">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ce3be-200">CosmosDB</span></span>

* <span data-ttu-id="ce3be-201">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="ce3be-201">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="ce3be-202">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="ce3be-202">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ce3be-203">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ce3be-203">Data Lake Analytics</span></span>

* <span data-ttu-id="ce3be-204">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="ce3be-204">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="ce3be-205">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-205">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="ce3be-206">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-206">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ce3be-207">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ce3be-207">Data Lake Store</span></span>

* <span data-ttu-id="ce3be-208">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-208">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="ce3be-209">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="ce3be-209">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="ce3be-210">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ce3be-210">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="ce3be-211">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="ce3be-211">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="ce3be-212">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="ce3be-212">Interactive</span></span>

* <span data-ttu-id="ce3be-213">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="ce3be-213">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="ce3be-214">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="ce3be-214">Increased test coverage</span></span>
* <span data-ttu-id="ce3be-215">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="ce3be-215">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="ce3be-216">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="ce3be-216">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="ce3be-217">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="ce3be-217">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="ce3be-218">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="ce3be-218">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="ce3be-219">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="ce3be-219">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ce3be-220">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-220">Added `--progress` flag</span></span>
* <span data-ttu-id="ce3be-221">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="ce3be-221">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="ce3be-222">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="ce3be-222">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="ce3be-223">IoT</span><span class="sxs-lookup"><span data-stu-id="ce3be-223">IoT</span></span>

* <span data-ttu-id="ce3be-224">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="ce3be-224">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="ce3be-225">(#3934)</span><span class="sxs-lookup"><span data-stu-id="ce3be-225">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="ce3be-226">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="ce3be-226">Key vault</span></span>

* <span data-ttu-id="ce3be-227">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="ce3be-227">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="ce3be-228">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ce3be-228">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="ce3be-229">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ce3be-229">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ce3be-230">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ce3be-230">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ce3be-231">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ce3be-231">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="ce3be-232">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="ce3be-232">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="ce3be-233">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="ce3be-233">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="ce3be-234">(#3307)</span><span class="sxs-lookup"><span data-stu-id="ce3be-234">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="ce3be-235">Labb</span><span class="sxs-lookup"><span data-stu-id="ce3be-235">Lab</span></span>

* <span data-ttu-id="ce3be-236">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="ce3be-236">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="ce3be-237">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="ce3be-237">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="ce3be-238">Övervaka</span><span class="sxs-lookup"><span data-stu-id="ce3be-238">Monitor</span></span>

* <span data-ttu-id="ce3be-239">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="ce3be-239">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="ce3be-240">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="ce3be-240">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="ce3be-241">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="ce3be-241">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="ce3be-242">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="ce3be-242">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="ce3be-243">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="ce3be-243">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="ce3be-244">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="ce3be-244">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="ce3be-245">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="ce3be-245">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="ce3be-246">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="ce3be-246">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="ce3be-247">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="ce3be-247">`location` no longer required</span></span>
  * <span data-ttu-id="ce3be-248">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="ce3be-248">Add name and ID support for target</span></span>
  * <span data-ttu-id="ce3be-249">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ce3be-249">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="ce3be-250">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="ce3be-250">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="ce3be-251">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="ce3be-251">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="ce3be-252">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="ce3be-252">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="ce3be-253">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="ce3be-253">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="ce3be-254">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-254">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="ce3be-255">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ce3be-255">Network</span></span>

* <span data-ttu-id="ce3be-256">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-256">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="ce3be-257">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-257">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="ce3be-258">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="ce3be-258">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="ce3be-259">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="ce3be-259">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="ce3be-260">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-260">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="ce3be-261">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-261">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="ce3be-262">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="ce3be-262">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="ce3be-263">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="ce3be-263">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="ce3be-264">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="ce3be-264">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="ce3be-265">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="ce3be-265">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="ce3be-266">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="ce3be-266">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="ce3be-267">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="ce3be-267">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="ce3be-268">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="ce3be-268">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="ce3be-269">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-269">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="ce3be-270">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-270">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="ce3be-271">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="ce3be-271">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="ce3be-272">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-272">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="ce3be-273">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="ce3be-273">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="ce3be-274">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-274">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="ce3be-275">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="ce3be-275">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="ce3be-276">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="ce3be-276">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="ce3be-277">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="ce3be-277">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="ce3be-278">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="ce3be-278">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="ce3be-279">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="ce3be-279">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="ce3be-280">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="ce3be-280">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="ce3be-281">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="ce3be-281">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="ce3be-282">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="ce3be-282">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="ce3be-283">Profil</span><span class="sxs-lookup"><span data-stu-id="ce3be-283">Profile</span></span>

* <span data-ttu-id="ce3be-284">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="ce3be-284">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="ce3be-285">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="ce3be-285">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="ce3be-286">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="ce3be-286">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="ce3be-287">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="ce3be-287">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="ce3be-288">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="ce3be-288">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="ce3be-289">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ce3be-289">RDBMS</span></span>

* <span data-ttu-id="ce3be-290">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="ce3be-290">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="ce3be-291">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="ce3be-291">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="ce3be-292">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="ce3be-292">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="ce3be-293">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="ce3be-293">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="ce3be-294">Resurs</span><span class="sxs-lookup"><span data-stu-id="ce3be-294">Resource</span></span>

* <span data-ttu-id="ce3be-295">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="ce3be-295">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="ce3be-296">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="ce3be-296">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="ce3be-297">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="ce3be-297">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="ce3be-298">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="ce3be-298">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="ce3be-299">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="ce3be-299">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="ce3be-300">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="ce3be-300">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="ce3be-301">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="ce3be-301">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="ce3be-302">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="ce3be-302">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="ce3be-303">Roll</span><span class="sxs-lookup"><span data-stu-id="ce3be-303">Role</span></span>

* <span data-ttu-id="ce3be-304">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="ce3be-304">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="ce3be-305">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="ce3be-305">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="ce3be-306">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="ce3be-306">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="ce3be-307">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="ce3be-307">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="ce3be-308">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="ce3be-308">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ce3be-309">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ce3be-309">Service Fabric</span></span>
* <span data-ttu-id="ce3be-310">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="ce3be-310">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="ce3be-311">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="ce3be-311">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="ce3be-312">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="ce3be-312">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="ce3be-313">SQL</span><span class="sxs-lookup"><span data-stu-id="ce3be-313">SQL</span></span>

* <span data-ttu-id="ce3be-314">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ce3be-314">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="ce3be-315">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="ce3be-315">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="ce3be-316">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="ce3be-316">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="ce3be-317">Lagring</span><span class="sxs-lookup"><span data-stu-id="ce3be-317">Storage</span></span>

* <span data-ttu-id="ce3be-318">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="ce3be-318">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="ce3be-319">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="ce3be-319">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="ce3be-320">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="ce3be-320">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="ce3be-321">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="ce3be-321">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="ce3be-322">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="ce3be-322">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="ce3be-323">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="ce3be-323">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="ce3be-324">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ce3be-324">VM</span></span>

* <span data-ttu-id="ce3be-325">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="ce3be-325">Support configuring nsg</span></span>
* <span data-ttu-id="ce3be-326">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="ce3be-326">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="ce3be-327">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="ce3be-327">Support managed service identities</span></span>
* <span data-ttu-id="ce3be-328">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-328">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="ce3be-329">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="ce3be-329">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="ce3be-330">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-330">May 10, 2017</span></span>

<span data-ttu-id="ce3be-331">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="ce3be-331">Version 2.0.6</span></span>

* <span data-ttu-id="ce3be-332">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="ce3be-332">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="ce3be-333">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="ce3be-333">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="ce3be-334">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="ce3be-334">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="ce3be-335">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="ce3be-335">Include Cognitive Services module.</span></span>
* <span data-ttu-id="ce3be-336">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="ce3be-336">Include Service Fabric module.</span></span>
* <span data-ttu-id="ce3be-337">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="ce3be-337">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="ce3be-338">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="ce3be-338">Add support for CDN commands.</span></span>
* <span data-ttu-id="ce3be-339">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="ce3be-339">Remove Container module.</span></span>
* <span data-ttu-id="ce3be-340">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="ce3be-340">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="ce3be-341">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ce3be-341">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="ce3be-342">Kärna</span><span class="sxs-lookup"><span data-stu-id="ce3be-342">Core</span></span>

* <span data-ttu-id="ce3be-343">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="ce3be-343">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="ce3be-344">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="ce3be-344">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="ce3be-345">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="ce3be-345">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="ce3be-346">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="ce3be-346">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="ce3be-347">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="ce3be-347">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="ce3be-348">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="ce3be-348">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="ce3be-349">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="ce3be-349">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="ce3be-350">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="ce3be-350">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="ce3be-351">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="ce3be-351">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="ce3be-352">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="ce3be-352">core: Improved performance</span></span>
* <span data-ttu-id="ce3be-353">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="ce3be-353">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="ce3be-354">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="ce3be-354">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="ce3be-355">ACS</span><span class="sxs-lookup"><span data-stu-id="ce3be-355">ACS</span></span>

* <span data-ttu-id="ce3be-356">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="ce3be-356">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="ce3be-357">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="ce3be-357">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="ce3be-358">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="ce3be-358">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="ce3be-359">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="ce3be-359">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="ce3be-360">AppService</span><span class="sxs-lookup"><span data-stu-id="ce3be-360">AppService</span></span>

* <span data-ttu-id="ce3be-361">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="ce3be-361">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="ce3be-362">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="ce3be-362">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="ce3be-363">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="ce3be-363">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="ce3be-364">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="ce3be-364">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="ce3be-365">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="ce3be-365">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="ce3be-366">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="ce3be-366">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="ce3be-367">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="ce3be-367">support slot swap with preview</span></span>
* <span data-ttu-id="ce3be-368">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="ce3be-368">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="ce3be-369">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="ce3be-369">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ce3be-370">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ce3be-370">CosmosDB</span></span>

* <span data-ttu-id="ce3be-371">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="ce3be-371">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="ce3be-372">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="ce3be-372">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="ce3be-373">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="ce3be-373">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="ce3be-374">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="ce3be-374">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ce3be-375">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ce3be-375">Data Lake Analytics</span></span>

* <span data-ttu-id="ce3be-376">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="ce3be-376">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="ce3be-377">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="ce3be-377">Add support for new catalog item type: package.</span></span> <span data-ttu-id="ce3be-378">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="ce3be-378">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="ce3be-379">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="ce3be-379">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="ce3be-380">Tabell</span><span class="sxs-lookup"><span data-stu-id="ce3be-380">Table</span></span>
  * <span data-ttu-id="ce3be-381">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="ce3be-381">Table valued function</span></span>
  * <span data-ttu-id="ce3be-382">Visa</span><span class="sxs-lookup"><span data-stu-id="ce3be-382">View</span></span>
  * <span data-ttu-id="ce3be-383">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="ce3be-383">Table Statistics.</span></span> <span data-ttu-id="ce3be-384">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="ce3be-384">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ce3be-385">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ce3be-385">Data Lake Store</span></span>

* <span data-ttu-id="ce3be-386">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="ce3be-386">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="ce3be-387">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ce3be-387">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="ce3be-388">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="ce3be-388">missed help for access show.</span></span> <span data-ttu-id="ce3be-389">läggs till.</span><span class="sxs-lookup"><span data-stu-id="ce3be-389">adding it.</span></span> <span data-ttu-id="ce3be-390">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="ce3be-390">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="ce3be-391">Hitta</span><span class="sxs-lookup"><span data-stu-id="ce3be-391">Find</span></span>

* <span data-ttu-id="ce3be-392">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="ce3be-392">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="ce3be-393">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce3be-393">KeyVault</span></span>

* <span data-ttu-id="ce3be-394">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="ce3be-394">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="ce3be-395">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ce3be-395">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="ce3be-396">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="ce3be-396">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="ce3be-397">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="ce3be-397">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="ce3be-398">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="ce3be-398">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="ce3be-399">Labb</span><span class="sxs-lookup"><span data-stu-id="ce3be-399">Lab</span></span>

* <span data-ttu-id="ce3be-400">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ce3be-400">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="ce3be-401">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ce3be-401">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="ce3be-402">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="ce3be-402">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="ce3be-403">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="ce3be-403">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="ce3be-404">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="ce3be-404">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="ce3be-405">Övervaka</span><span class="sxs-lookup"><span data-stu-id="ce3be-405">Monitor</span></span>

* <span data-ttu-id="ce3be-406">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="ce3be-406">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="ce3be-407">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="ce3be-407">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="ce3be-408">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ce3be-408">Network</span></span>

* <span data-ttu-id="ce3be-409">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-409">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="ce3be-410">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-410">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="ce3be-411">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ce3be-411">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="ce3be-412">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ce3be-412">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="ce3be-413">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ce3be-413">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="ce3be-414">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="ce3be-414">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="ce3be-415">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="ce3be-415">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="ce3be-416">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="ce3be-416">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="ce3be-417">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-417">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="ce3be-418">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="ce3be-418">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="ce3be-419">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="ce3be-419">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="ce3be-420">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="ce3be-420">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="ce3be-421">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="ce3be-421">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="ce3be-422">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="ce3be-422">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="ce3be-423">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="ce3be-423">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="ce3be-424">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="ce3be-424">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="ce3be-425">Profil</span><span class="sxs-lookup"><span data-stu-id="ce3be-425">Profile</span></span>

* <span data-ttu-id="ce3be-426">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="ce3be-426">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="ce3be-427">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="ce3be-427">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="ce3be-428">Redis</span><span class="sxs-lookup"><span data-stu-id="ce3be-428">Redis</span></span>

* <span data-ttu-id="ce3be-429">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="ce3be-429">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="ce3be-430">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="ce3be-430">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="ce3be-431">Resurs</span><span class="sxs-lookup"><span data-stu-id="ce3be-431">Resource</span></span>

* <span data-ttu-id="ce3be-432">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="ce3be-432">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="ce3be-433">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="ce3be-433">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="ce3be-434">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="ce3be-434">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="ce3be-435">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="ce3be-435">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="ce3be-436">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="ce3be-436">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="ce3be-437">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="ce3be-437">Add docs for az lock update.</span></span> <span data-ttu-id="ce3be-438">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="ce3be-438">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="ce3be-439">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="ce3be-439">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="ce3be-440">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="ce3be-440">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="ce3be-441">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="ce3be-441">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="ce3be-442">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="ce3be-442">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="ce3be-443">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="ce3be-443">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="ce3be-444">Roll</span><span class="sxs-lookup"><span data-stu-id="ce3be-444">Role</span></span>

* <span data-ttu-id="ce3be-445">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="ce3be-445">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="ce3be-446">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="ce3be-446">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="ce3be-447">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="ce3be-447">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="ce3be-448">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="ce3be-448">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="ce3be-449">SQL</span><span class="sxs-lookup"><span data-stu-id="ce3be-449">SQL</span></span>

* <span data-ttu-id="ce3be-450">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ce3be-450">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="ce3be-451">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="ce3be-451">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="ce3be-452">Lagring</span><span class="sxs-lookup"><span data-stu-id="ce3be-452">Storage</span></span>

* <span data-ttu-id="ce3be-453">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-453">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="ce3be-454">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="ce3be-454">Add support for incremental blob copy</span></span>
* <span data-ttu-id="ce3be-455">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="ce3be-455">Add support for large block blob upload</span></span>
* <span data-ttu-id="ce3be-456">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="ce3be-456">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="ce3be-457">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ce3be-457">VM</span></span>

* <span data-ttu-id="ce3be-458">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="ce3be-458">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="ce3be-459">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="ce3be-459">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="ce3be-460">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="ce3be-460">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="ce3be-461">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="ce3be-461">az vm/vmss disk</span></span>
  3. <span data-ttu-id="ce3be-462">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="ce3be-462">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="ce3be-463">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="ce3be-463">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="ce3be-464">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="ce3be-464">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="ce3be-465">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-465">April 3, 2017</span></span>

<span data-ttu-id="ce3be-466">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="ce3be-466">Version 2.0.2</span></span>

<span data-ttu-id="ce3be-467">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="ce3be-467">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="ce3be-468">Kärna</span><span class="sxs-lookup"><span data-stu-id="ce3be-468">Core</span></span>

* <span data-ttu-id="ce3be-469">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="ce3be-469">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="ce3be-470">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="ce3be-470">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="ce3be-471">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="ce3be-471">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="ce3be-472">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ce3be-472">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ce3be-473">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="ce3be-473">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="ce3be-474">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="ce3be-474">Add prompting for missing template parameters.</span></span> <span data-ttu-id="ce3be-475">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="ce3be-475">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="ce3be-476">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="ce3be-476">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="ce3be-477">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="ce3be-477">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="ce3be-478">ACS</span><span class="sxs-lookup"><span data-stu-id="ce3be-478">ACS</span></span>

* <span data-ttu-id="ce3be-479">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="ce3be-479">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="ce3be-480">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="ce3be-480">Add support for ssh key password prompting.</span></span> <span data-ttu-id="ce3be-481">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="ce3be-481">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="ce3be-482">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="ce3be-482">Add support for windows clusters.</span></span> <span data-ttu-id="ce3be-483">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="ce3be-483">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="ce3be-484">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="ce3be-484">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="ce3be-485">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="ce3be-485">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="ce3be-486">AppService</span><span class="sxs-lookup"><span data-stu-id="ce3be-486">AppService</span></span>

* <span data-ttu-id="ce3be-487">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="ce3be-487">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="ce3be-488">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="ce3be-488">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="ce3be-489">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="ce3be-489">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="ce3be-490">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="ce3be-490">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="ce3be-491">DataLake</span><span class="sxs-lookup"><span data-stu-id="ce3be-491">DataLake</span></span>

* <span data-ttu-id="ce3be-492">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="ce3be-492">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="ce3be-493">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="ce3be-493">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="ce3be-494">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="ce3be-494">DocuemntDB</span></span>

* <span data-ttu-id="ce3be-495">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="ce3be-495">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="ce3be-496">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ce3be-496">VM</span></span>

* <span data-ttu-id="ce3be-497">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="ce3be-497">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="ce3be-498">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="ce3be-498">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="ce3be-499">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="ce3be-499">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="ce3be-500">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ce3be-500">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ce3be-501">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="ce3be-501">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="ce3be-502">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="ce3be-502">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="ce3be-503">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="ce3be-503">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="ce3be-504">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="ce3be-504">February 27, 2017</span></span>

<span data-ttu-id="ce3be-505">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="ce3be-505">Version 2.0.0</span></span>

<span data-ttu-id="ce3be-506">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="ce3be-506">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="ce3be-507">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="ce3be-507">General availability applies to these command modules:</span></span>
- <span data-ttu-id="ce3be-508">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="ce3be-508">Container Service (acs)</span></span>
- <span data-ttu-id="ce3be-509">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="ce3be-509">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="ce3be-510">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ce3be-510">Networking</span></span>
- <span data-ttu-id="ce3be-511">Storage</span><span class="sxs-lookup"><span data-stu-id="ce3be-511">Storage</span></span>

<span data-ttu-id="ce3be-512">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="ce3be-512">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="ce3be-513">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="ce3be-513">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="ce3be-514">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-514">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="ce3be-515">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="ce3be-515">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="ce3be-516">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-516">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="ce3be-517">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="ce3be-517">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="ce3be-518">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="ce3be-518">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="ce3be-519">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="ce3be-519">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="ce3be-520">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="ce3be-520">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="ce3be-521">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="ce3be-521">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="ce3be-522">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="ce3be-522">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="ce3be-523">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="ce3be-523">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="ce3be-524">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ce3be-524">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="ce3be-525">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="ce3be-525">Provide feedback from the command line with the `az feedback` command.</span></span>

