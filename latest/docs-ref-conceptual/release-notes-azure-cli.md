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
ms.openlocfilehash: 761bd61474e7c72fb2daeb756828f00196b56c3a
ms.sourcegitcommit: bb649ebd7e7fce8fb5008ac1e2e2c33481a45df9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/16/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="8c6d2-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="8c6d2-104">Azure CLI 2.0 release notes</span></span>

## <a name="november-14-2017"></a><span data-ttu-id="8c6d2-105">14 november 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-105">November 14, 2017</span></span>

<span data-ttu-id="8c6d2-106">Version 2.0.21</span><span class="sxs-lookup"><span data-stu-id="8c6d2-106">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="8c6d2-107">ACR</span><span class="sxs-lookup"><span data-stu-id="8c6d2-107">ACR</span></span>

* <span data-ttu-id="8c6d2-108">Stöd för att skapa webhooks i replikeringsregioner har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-108">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="8c6d2-109">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-109">ACS</span></span>

* <span data-ttu-id="8c6d2-110">Alla ”agent” till ”nod” har ändrats i AKS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-110">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="8c6d2-111">Föråldrat `--orchestrator-release`-alternativ för `acs create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-111">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="8c6d2-112">Standardstorleken för virtuella datorer för AKS till `Standard_D1_v2` har ändrats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-112">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="8c6d2-113">Åtgärdade `az aks browse` i Windows</span><span class="sxs-lookup"><span data-stu-id="8c6d2-113">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="8c6d2-114">Åtgärdade `az aks get-credentials` i Windows</span><span class="sxs-lookup"><span data-stu-id="8c6d2-114">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-115">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-115">Appservice</span></span>

* <span data-ttu-id="8c6d2-116">Distributionskälla `config-zip` för webappar och funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-116">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="8c6d2-117">`--docker-container-logging`-alternativ till `az webapp log config` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-117">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="8c6d2-118">Alternativet `storage` från parametern `--web-server-logging` av `az webapp log config` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8c6d2-118">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="8c6d2-119">Förbättrade felmeddelanden för `deployment user set`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-119">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="8c6d2-120">Stöd för att skapa Linux-funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-120">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="8c6d2-121">Åtgärdade `list-locations`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-121">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="8c6d2-122">Batch</span><span class="sxs-lookup"><span data-stu-id="8c6d2-122">Batch</span></span>

* <span data-ttu-id="8c6d2-123">En bugg har åtgärdats i kommandot för skapande av pool när ett resurs-ID användes med flaggan `--image`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-123">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="8c6d2-124">Batchai</span><span class="sxs-lookup"><span data-stu-id="8c6d2-124">Batchai</span></span>

* <span data-ttu-id="8c6d2-125">Ett kort alternativ har lagts till, `-s`, för `--vm-size` VM-storlek i kommandot `file-server create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-125">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="8c6d2-126">Kontonamn och nyckelargument har lagts till för `cluster create`-parametrar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-126">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="8c6d2-127">Dokumentation har skapats för `job list-files` och `job stream-file`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-127">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="8c6d2-128">Ett kort alternativ har lagts till, `-r`, för `--cluster-name` när klusternamn anges med kommandot `job create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-128">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="8c6d2-129">Molnet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-129">Cloud</span></span>

* <span data-ttu-id="8c6d2-130">`cloud [register|update]` har ändrats för att förhindra att moln registreras som saknar slutpunkter som krävs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-130">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="8c6d2-131">Behållare</span><span class="sxs-lookup"><span data-stu-id="8c6d2-131">Container</span></span>

* <span data-ttu-id="8c6d2-132">Stöd för att öppna flera portar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-132">Added support to open multiple ports</span></span>
* <span data-ttu-id="8c6d2-133">Princip för omstart av behållargrupp har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-133">Added container group restart policy</span></span>
* <span data-ttu-id="8c6d2-134">Stöd för att montera Azure-filresurs som volym har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-134">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="8c6d2-135">Hjälpdokument har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-135">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8c6d2-136">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8c6d2-136">Data Lake Analytics</span></span>

* <span data-ttu-id="8c6d2-137">`[job|account] list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="8c6d2-137">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8c6d2-138">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8c6d2-138">Data Lake Store</span></span>

* <span data-ttu-id="8c6d2-139">`account list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="8c6d2-139">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="8c6d2-140">Anknytning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-140">Extension</span></span>

* <span data-ttu-id="8c6d2-141">`extension list-available` har lagts till för att tillåta lista över officiella Microsoft-tillägg</span><span class="sxs-lookup"><span data-stu-id="8c6d2-141">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="8c6d2-142">`--name` har lagts till för `extension [add|update]` för att tillåta installation av tillägg via namn</span><span class="sxs-lookup"><span data-stu-id="8c6d2-142">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="8c6d2-143">IoT</span><span class="sxs-lookup"><span data-stu-id="8c6d2-143">IoT</span></span>

* <span data-ttu-id="8c6d2-144">Stöd för certifikatutfärdare (CA) och certifikatkedjor har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-144">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="8c6d2-145">Övervaka</span><span class="sxs-lookup"><span data-stu-id="8c6d2-145">Monitor</span></span>

* <span data-ttu-id="8c6d2-146">`activity-log alert`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-146">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-147">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-147">Network</span></span>

* <span data-ttu-id="8c6d2-148">Stöd för CAA DNS-poster har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-148">Added support for CAA DNS records</span></span>
* <span data-ttu-id="8c6d2-149">Problem där slutpunkter inte kunde uppdateras med `traffic-manager profile update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-149">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="8c6d2-150">Problem där `vnet update --dns-servers` inte fungerade beroende på hur VNET skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-150">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="8c6d2-151">Problem där relativa DNS-namn hade importerats felaktigt av `dns zone import` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-151">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="8c6d2-152">Reservationer</span><span class="sxs-lookup"><span data-stu-id="8c6d2-152">Reservations</span></span>

* <span data-ttu-id="8c6d2-153">Inledande förhandsversion</span><span class="sxs-lookup"><span data-stu-id="8c6d2-153">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-154">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-154">Resource</span></span>

* <span data-ttu-id="8c6d2-155">Stöd för resurs-ID till parametern `--resource` och lås på resursnivå har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-155">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-156">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-156">SQL</span></span>

* <span data-ttu-id="8c6d2-157">Parametern `--ignore-missing-vnet-service-endpoint` har lagts till i `sql server vnet-rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-157">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-158">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-158">Storage</span></span>

* <span data-ttu-id="8c6d2-159">`storage account create` har ändrats för att använda SKU `Standard_RAGRS` som standard</span><span class="sxs-lookup"><span data-stu-id="8c6d2-159">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="8c6d2-160">Buggar när fil-/blob-namn som innehåller icke-ASCII-tecken hanteras har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-160">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="8c6d2-161">Bugg som förhindrade användning av `--source-uri` med `storage [blob|file] copy start-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-161">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="8c6d2-162">Kommandon för blob och borttagning av flera objekt med `storage [blob|file] delete-batch` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-162">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="8c6d2-163">Problem vid aktivering av mått med `storage metrics update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-163">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="8c6d2-164">Problem med filer över 200 GB vid användning av `storage blob upload-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-164">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="8c6d2-165">Problem där `--bypass` och `--default-action` ignorerades av `storage account [create|update]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-165">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-166">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-166">VM</span></span>

* <span data-ttu-id="8c6d2-167">En bugg med `vmss create` som förhindrade användning med storleksnivån `Basic` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-167">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="8c6d2-168">`--plan` argument till `[vm|vmss] create` för anpassade avbildningar med faktureringsinformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-168">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="8c6d2-169">Kommandona `vm secret `[add|remove|list] har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-169">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="8c6d2-170">`vm format-secret` har bytt namn till `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-170">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="8c6d2-171">Argumentet `--encrypt format` har lagts till för `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-171">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="8c6d2-172">24 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-172">October 24, 2017</span></span>

<span data-ttu-id="8c6d2-173">Version 2.0.20</span><span class="sxs-lookup"><span data-stu-id="8c6d2-173">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="8c6d2-174">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-174">Core</span></span>

* <span data-ttu-id="8c6d2-175">`2017-03-09-profile` har uppdaterats för att använda `MGMT_STORAGE`, API-version `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-175">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="8c6d2-176">ACR</span><span class="sxs-lookup"><span data-stu-id="8c6d2-176">ACR</span></span>

* <span data-ttu-id="8c6d2-177">Resurshanteringen har uppdaterats för att peka på API-version `2017-10-01`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-177">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="8c6d2-178">SKU:n för BYOS ("bring your own storage") har ändrats till klassisk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-178">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="8c6d2-179">Register-SKU:erna har bytt namn till Basic, Standard och Premium</span><span class="sxs-lookup"><span data-stu-id="8c6d2-179">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-180">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-180">ACS</span></span>

* <span data-ttu-id="8c6d2-181">[FÖRHANDSVERSION] `az aks`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-181">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="8c6d2-182">Kubernetes `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-182">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-183">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-183">Appservice</span></span>

* <span data-ttu-id="8c6d2-184">Problem med att nedladdade `webapp`-loggar kunde vara ogiltiga har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-184">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="8c6d2-185">Komponent</span><span class="sxs-lookup"><span data-stu-id="8c6d2-185">Component</span></span>

* <span data-ttu-id="8c6d2-186">Ett tydligare utfasningsmeddelande har lagts till för alla installationsprogram och bekräftelsefrågor</span><span class="sxs-lookup"><span data-stu-id="8c6d2-186">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="8c6d2-187">Övervaka</span><span class="sxs-lookup"><span data-stu-id="8c6d2-187">Monitor</span></span>

* <span data-ttu-id="8c6d2-188">`action-group`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-188">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-189">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-189">Resource</span></span>

* <span data-ttu-id="8c6d2-190">Inkompatibilitet med den senaste versionen av msrest-beroende i `group export` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-190">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="8c6d2-191">`policy assignment create` har åtgärdats så att det fungerar med inbyggda principdefinitioner och principuppsättningsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="8c6d2-191">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-192">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-192">VM</span></span>

* <span data-ttu-id="8c6d2-193">Argumentet `--accelerated-networking` har lagts till för `vmss create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-193">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="8c6d2-194">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-194">October 9, 2017</span></span>

<span data-ttu-id="8c6d2-195">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="8c6d2-195">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="8c6d2-196">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-196">Core</span></span>

* <span data-ttu-id="8c6d2-197">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-197">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-198">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-198">Appservice</span></span>

* <span data-ttu-id="8c6d2-199">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-199">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="8c6d2-200">Batch</span><span class="sxs-lookup"><span data-stu-id="8c6d2-200">Batch</span></span>

* <span data-ttu-id="8c6d2-201">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="8c6d2-201">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="8c6d2-202">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="8c6d2-202">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="8c6d2-203">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-203">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="8c6d2-204">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8c6d2-204">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="8c6d2-205">Batchai</span><span class="sxs-lookup"><span data-stu-id="8c6d2-205">Batchai</span></span>

* <span data-ttu-id="8c6d2-206">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-206">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c6d2-207">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c6d2-207">Keyvault</span></span>

* <span data-ttu-id="8c6d2-208">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-208">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="8c6d2-209">(#4448)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-209">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="8c6d2-210">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-210">Network</span></span>

* <span data-ttu-id="8c6d2-211">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="8c6d2-211">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="8c6d2-212">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="8c6d2-212">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-213">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-213">Resource</span></span>

* <span data-ttu-id="8c6d2-214">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-214">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="8c6d2-215">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="8c6d2-215">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="8c6d2-216">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="8c6d2-216">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="8c6d2-217">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="8c6d2-217">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-218">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-218">Sql</span></span>

* <span data-ttu-id="8c6d2-219">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="8c6d2-219">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="8c6d2-220">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="8c6d2-220">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="8c6d2-221">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-221">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-222">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-222">Storage</span></span>

* <span data-ttu-id="8c6d2-223">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-223">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-224">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-224">Vm</span></span>

* <span data-ttu-id="8c6d2-225">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="8c6d2-225">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="8c6d2-226">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-226">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="8c6d2-227">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-227">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="8c6d2-228">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-228">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="8c6d2-229">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-229">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="8c6d2-230">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-230">September 22, 2017</span></span>

<span data-ttu-id="8c6d2-231">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="8c6d2-231">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-232">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-232">Resource</span></span>

* <span data-ttu-id="8c6d2-233">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="8c6d2-233">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="8c6d2-234">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="8c6d2-234">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="8c6d2-235">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-235">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="8c6d2-236">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-236">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-237">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-237">Network</span></span>

* <span data-ttu-id="8c6d2-238">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-238">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="8c6d2-239">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-239">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="8c6d2-240">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-240">Added `asg` application security group commands</span></span>
* <span data-ttu-id="8c6d2-241">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-241">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="8c6d2-242">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-242">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8c6d2-243">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-243">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="8c6d2-244">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-244">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-245">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-245">Storage</span></span>

* <span data-ttu-id="8c6d2-246">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="8c6d2-246">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8c6d2-247">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="8c6d2-247">Eventgrid</span></span>

* <span data-ttu-id="8c6d2-248">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="8c6d2-248">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-249">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-249">SQL</span></span>

* <span data-ttu-id="8c6d2-250">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-250">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="8c6d2-251">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-251">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="8c6d2-252">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-252">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c6d2-253">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c6d2-253">Keyvault</span></span>

* <span data-ttu-id="8c6d2-254">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="8c6d2-254">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-255">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-255">VM</span></span>

* <span data-ttu-id="8c6d2-256">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-256">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="8c6d2-257">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="8c6d2-257">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="8c6d2-258">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-258">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="8c6d2-259">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-259">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="8c6d2-260">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-260">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="8c6d2-261">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-261">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-262">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-262">ACS</span></span>

* <span data-ttu-id="8c6d2-263">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="8c6d2-263">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-264">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-264">Appservice</span></span>

* <span data-ttu-id="8c6d2-265">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-265">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8c6d2-266">Säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="8c6d2-266">Backup</span></span>

* <span data-ttu-id="8c6d2-267">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="8c6d2-267">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="8c6d2-268">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-268">September 11, 2017</span></span>

<span data-ttu-id="8c6d2-269">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="8c6d2-269">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="8c6d2-270">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-270">Core</span></span>

* <span data-ttu-id="8c6d2-271">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="8c6d2-271">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="8c6d2-272">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="8c6d2-272">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-273">Acs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-273">Acs</span></span>

* <span data-ttu-id="8c6d2-274">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-274">Added `acs list-locations` command</span></span>
* <span data-ttu-id="8c6d2-275">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="8c6d2-275">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-276">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-276">Appservice</span></span>

* <span data-ttu-id="8c6d2-277">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-277">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="8c6d2-278">CDN</span><span class="sxs-lookup"><span data-stu-id="8c6d2-278">CDN</span></span>

* <span data-ttu-id="8c6d2-279">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-279">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="8c6d2-280">Anknytning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-280">Extension</span></span>

* <span data-ttu-id="8c6d2-281">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-281">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c6d2-282">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c6d2-282">Keyvault</span></span>

* <span data-ttu-id="8c6d2-283">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-283">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-284">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-284">Network</span></span>

* <span data-ttu-id="8c6d2-285">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-285">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8c6d2-286">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-286">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="8c6d2-287">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-287">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="8c6d2-288">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-288">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8c6d2-289">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-289">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-290">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-290">Resource</span></span>

* <span data-ttu-id="8c6d2-291">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-291">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="8c6d2-292">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-292">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="8c6d2-293">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="8c6d2-293">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="8c6d2-294">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-294">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-295">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-295">SQL</span></span>

* <span data-ttu-id="8c6d2-296">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-296">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-297">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-297">VM</span></span>

* <span data-ttu-id="8c6d2-298">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="8c6d2-298">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="8c6d2-299">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="8c6d2-299">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="8c6d2-300">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-300">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="8c6d2-301">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-301">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="8c6d2-302">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="8c6d2-302">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="8c6d2-303">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-303">August 31, 2017</span></span>

<span data-ttu-id="8c6d2-304">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="8c6d2-304">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c6d2-305">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c6d2-305">Keyvault</span></span>

* <span data-ttu-id="8c6d2-306">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-306">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="8c6d2-307">Sf</span><span class="sxs-lookup"><span data-stu-id="8c6d2-307">Sf</span></span>

* <span data-ttu-id="8c6d2-308">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-308">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-309">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-309">Storage</span></span>

* <span data-ttu-id="8c6d2-310">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-310">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="8c6d2-311">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="8c6d2-311">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="8c6d2-312">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-312">August 28, 2017</span></span>

<span data-ttu-id="8c6d2-313">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="8c6d2-313">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="8c6d2-314">CLI</span><span class="sxs-lookup"><span data-stu-id="8c6d2-314">CLI</span></span>

* <span data-ttu-id="8c6d2-315">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-315">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-316">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-316">ACS</span></span>

* <span data-ttu-id="8c6d2-317">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-317">Corrected preview regions.</span></span>
* <span data-ttu-id="8c6d2-318">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-318">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="8c6d2-319">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-319">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-320">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-320">Appservice</span></span>

* <span data-ttu-id="8c6d2-321">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-321">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="8c6d2-322">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-322">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="8c6d2-323">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-323">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="8c6d2-324">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="8c6d2-324">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="8c6d2-325">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-325">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="8c6d2-326">IoT</span><span class="sxs-lookup"><span data-stu-id="8c6d2-326">IoT</span></span>

* <span data-ttu-id="8c6d2-327">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="8c6d2-327">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-328">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-328">Network</span></span>

* <span data-ttu-id="8c6d2-329">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-329">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8c6d2-330">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-330">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="8c6d2-331">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-331">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8c6d2-332">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-332">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8c6d2-333">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-333">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="8c6d2-334">Profil</span><span class="sxs-lookup"><span data-stu-id="8c6d2-334">Profile</span></span>

* <span data-ttu-id="8c6d2-335">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-335">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8c6d2-336">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8c6d2-336">Service Fabric</span></span>

* <span data-ttu-id="8c6d2-337">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="8c6d2-337">Preview release</span></span>
* <span data-ttu-id="8c6d2-338">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="8c6d2-338">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="8c6d2-339">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-339">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="8c6d2-340">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-340">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-341">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-341">Storage</span></span>

* <span data-ttu-id="8c6d2-342">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="8c6d2-342">Enabled setting blob tier</span></span>
* <span data-ttu-id="8c6d2-343">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="8c6d2-343">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="8c6d2-344">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-344">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="8c6d2-345">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-345">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="8c6d2-346">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-346">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="8c6d2-347">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="8c6d2-347">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-348">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-348">VM</span></span>

* <span data-ttu-id="8c6d2-349">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-349">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="8c6d2-350">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-350">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="8c6d2-351">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-351">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="8c6d2-352">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-352">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="8c6d2-353">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-353">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="8c6d2-354">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-354">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="8c6d2-355">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-355">August 15, 2017</span></span>

<span data-ttu-id="8c6d2-356">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="8c6d2-356">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-357">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-357">ACS</span></span>

* <span data-ttu-id="8c6d2-358">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-358">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-359">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-359">Appservice</span></span>

* <span data-ttu-id="8c6d2-360">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-360">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="8c6d2-361">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8c6d2-361">Event Grid</span></span>

* <span data-ttu-id="8c6d2-362">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-362">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="8c6d2-363">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-363">August 11, 2017</span></span>

<span data-ttu-id="8c6d2-364">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="8c6d2-364">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-365">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-365">ACS</span></span>

* <span data-ttu-id="8c6d2-366">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-366">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="8c6d2-367">Batch</span><span class="sxs-lookup"><span data-stu-id="8c6d2-367">Batch</span></span>

* <span data-ttu-id="8c6d2-368">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8c6d2-368">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="8c6d2-369">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="8c6d2-369">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="8c6d2-370">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-370">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="8c6d2-371">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="8c6d2-371">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="8c6d2-372">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="8c6d2-372">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="8c6d2-373">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="8c6d2-373">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="8c6d2-374">Komponent</span><span class="sxs-lookup"><span data-stu-id="8c6d2-374">Component</span></span>

* <span data-ttu-id="8c6d2-375">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="8c6d2-375">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="8c6d2-376">Behållare</span><span class="sxs-lookup"><span data-stu-id="8c6d2-376">Container</span></span>

* <span data-ttu-id="8c6d2-377">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="8c6d2-377">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="8c6d2-378">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8c6d2-378">Data Lake Store</span></span>

* <span data-ttu-id="8c6d2-379">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="8c6d2-379">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="8c6d2-380">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8c6d2-380">Event Grid</span></span>

* <span data-ttu-id="8c6d2-381">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="8c6d2-381">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-382">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-382">Network</span></span>

* <span data-ttu-id="8c6d2-383">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="8c6d2-383">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="8c6d2-384">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="8c6d2-384">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="8c6d2-385">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-385">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="8c6d2-386">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-386">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="8c6d2-387">Profil</span><span class="sxs-lookup"><span data-stu-id="8c6d2-387">Profile</span></span>

* <span data-ttu-id="8c6d2-388">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="8c6d2-388">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-389">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-389">Storage</span></span>

* <span data-ttu-id="8c6d2-390">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="8c6d2-390">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-391">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-391">VM</span></span>

* <span data-ttu-id="8c6d2-392">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-392">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="8c6d2-393">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-393">Exposed `list-skus` command</span></span>
* <span data-ttu-id="8c6d2-394">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-394">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="8c6d2-395">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="8c6d2-395">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="8c6d2-396">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8c6d2-396">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="8c6d2-397">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-397">July 28, 2017</span></span>

<span data-ttu-id="8c6d2-398">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="8c6d2-398">Version 2.0.12</span></span>

* <span data-ttu-id="8c6d2-399">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-399">Added container commands</span></span>
* <span data-ttu-id="8c6d2-400">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-400">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="8c6d2-401">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-401">Core</span></span>

* <span data-ttu-id="8c6d2-402">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="8c6d2-402">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="8c6d2-403">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-403">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="8c6d2-404">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="8c6d2-404">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="8c6d2-405">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-405">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="8c6d2-406">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-406">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="8c6d2-407">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-407">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="8c6d2-408">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-408">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8c6d2-409">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-409">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="8c6d2-410">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-410">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="8c6d2-411">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="8c6d2-411">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="8c6d2-412">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-412">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="8c6d2-413">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-413">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="8c6d2-414">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="8c6d2-414">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="8c6d2-415">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="8c6d2-415">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="8c6d2-416">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="8c6d2-416">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="8c6d2-417">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-417">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="8c6d2-418">ACR</span><span class="sxs-lookup"><span data-stu-id="8c6d2-418">ACR</span></span>

* <span data-ttu-id="8c6d2-419">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="8c6d2-419">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="8c6d2-420">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="8c6d2-420">Support SKU update for managed registries</span></span>
* <span data-ttu-id="8c6d2-421">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-421">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="8c6d2-422">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="8c6d2-422">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="8c6d2-423">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="8c6d2-423">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="8c6d2-424">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-424">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-425">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-425">ACS</span></span>

* <span data-ttu-id="8c6d2-426">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="8c6d2-426">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-427">App Service</span><span class="sxs-lookup"><span data-stu-id="8c6d2-427">Appservice</span></span>

* <span data-ttu-id="8c6d2-428">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="8c6d2-428">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="8c6d2-429">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="8c6d2-429">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="8c6d2-430">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-430">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="8c6d2-431">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-431">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="8c6d2-432">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-432">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="8c6d2-433">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-433">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="8c6d2-434">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-434">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="8c6d2-435">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-435">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="8c6d2-436">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-436">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="8c6d2-437">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="8c6d2-437">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="8c6d2-438">Batch</span><span class="sxs-lookup"><span data-stu-id="8c6d2-438">Batch</span></span>

* <span data-ttu-id="8c6d2-439">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="8c6d2-439">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="8c6d2-440">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-440">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="8c6d2-441">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-441">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="8c6d2-442">CDN</span><span class="sxs-lookup"><span data-stu-id="8c6d2-442">CDN</span></span>

* <span data-ttu-id="8c6d2-443">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-443">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="8c6d2-444">Molnet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-444">Cloud</span></span>

* <span data-ttu-id="8c6d2-445">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="8c6d2-445">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="8c6d2-446">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="8c6d2-446">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="8c6d2-447">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="8c6d2-447">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="8c6d2-448">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-448">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="8c6d2-449">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-449">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8c6d2-450">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8c6d2-450">CosmosDB</span></span>

* <span data-ttu-id="8c6d2-451">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="8c6d2-451">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="8c6d2-452">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-452">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8c6d2-453">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8c6d2-453">Data Lake Analytics</span></span>

* <span data-ttu-id="8c6d2-454">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-454">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="8c6d2-455">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-455">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="8c6d2-456">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-456">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8c6d2-457">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8c6d2-457">Data Lake Store</span></span>

* <span data-ttu-id="8c6d2-458">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-458">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="8c6d2-459">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="8c6d2-459">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="8c6d2-460">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-460">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="8c6d2-461">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="8c6d2-461">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="8c6d2-462">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="8c6d2-462">Interactive</span></span>

* <span data-ttu-id="8c6d2-463">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="8c6d2-463">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="8c6d2-464">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-464">Increased test coverage</span></span>
* <span data-ttu-id="8c6d2-465">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="8c6d2-465">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="8c6d2-466">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-466">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="8c6d2-467">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-467">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="8c6d2-468">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-468">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="8c6d2-469">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-469">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8c6d2-470">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-470">Added `--progress` flag</span></span>
* <span data-ttu-id="8c6d2-471">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="8c6d2-471">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="8c6d2-472">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-472">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="8c6d2-473">IoT</span><span class="sxs-lookup"><span data-stu-id="8c6d2-473">IoT</span></span>

* <span data-ttu-id="8c6d2-474">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-474">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="8c6d2-475">(#3934)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-475">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="8c6d2-476">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="8c6d2-476">Key vault</span></span>

* <span data-ttu-id="8c6d2-477">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-477">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="8c6d2-478">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-478">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="8c6d2-479">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-479">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8c6d2-480">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-480">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8c6d2-481">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-481">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="8c6d2-482">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-482">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="8c6d2-483">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-483">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="8c6d2-484">(#3307)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-484">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="8c6d2-485">Labb</span><span class="sxs-lookup"><span data-stu-id="8c6d2-485">Lab</span></span>

* <span data-ttu-id="8c6d2-486">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-486">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="8c6d2-487">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-487">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="8c6d2-488">Övervaka</span><span class="sxs-lookup"><span data-stu-id="8c6d2-488">Monitor</span></span>

* <span data-ttu-id="8c6d2-489">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-489">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="8c6d2-490">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-490">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="8c6d2-491">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-491">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="8c6d2-492">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-492">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="8c6d2-493">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-493">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="8c6d2-494">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-494">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="8c6d2-495">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="8c6d2-495">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="8c6d2-496">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="8c6d2-496">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="8c6d2-497">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="8c6d2-497">`location` no longer required</span></span>
  * <span data-ttu-id="8c6d2-498">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="8c6d2-498">Add name and ID support for target</span></span>
  * <span data-ttu-id="8c6d2-499">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8c6d2-499">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="8c6d2-500">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="8c6d2-500">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="8c6d2-501">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="8c6d2-501">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="8c6d2-502">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-502">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="8c6d2-503">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="8c6d2-503">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="8c6d2-504">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-504">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-505">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-505">Network</span></span>

* <span data-ttu-id="8c6d2-506">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-506">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="8c6d2-507">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-507">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="8c6d2-508">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="8c6d2-508">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="8c6d2-509">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-509">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="8c6d2-510">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-510">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="8c6d2-511">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-511">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="8c6d2-512">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-512">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="8c6d2-513">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-513">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="8c6d2-514">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-514">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="8c6d2-515">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-515">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="8c6d2-516">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-516">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="8c6d2-517">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-517">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="8c6d2-518">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-518">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="8c6d2-519">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-519">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="8c6d2-520">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-520">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="8c6d2-521">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-521">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="8c6d2-522">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-522">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="8c6d2-523">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-523">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="8c6d2-524">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-524">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="8c6d2-525">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-525">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="8c6d2-526">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-526">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="8c6d2-527">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="8c6d2-527">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="8c6d2-528">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-528">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="8c6d2-529">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="8c6d2-529">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="8c6d2-530">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="8c6d2-530">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="8c6d2-531">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="8c6d2-531">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="8c6d2-532">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="8c6d2-532">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="8c6d2-533">Profil</span><span class="sxs-lookup"><span data-stu-id="8c6d2-533">Profile</span></span>

* <span data-ttu-id="8c6d2-534">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-534">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="8c6d2-535">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="8c6d2-535">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="8c6d2-536">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="8c6d2-536">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="8c6d2-537">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="8c6d2-537">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="8c6d2-538">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="8c6d2-538">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="8c6d2-539">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-539">RDBMS</span></span>

* <span data-ttu-id="8c6d2-540">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-540">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="8c6d2-541">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-541">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="8c6d2-542">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-542">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="8c6d2-543">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-543">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-544">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-544">Resource</span></span>

* <span data-ttu-id="8c6d2-545">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-545">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="8c6d2-546">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="8c6d2-546">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="8c6d2-547">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-547">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="8c6d2-548">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-548">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="8c6d2-549">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-549">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="8c6d2-550">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-550">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="8c6d2-551">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-551">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="8c6d2-552">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="8c6d2-552">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="8c6d2-553">Roll</span><span class="sxs-lookup"><span data-stu-id="8c6d2-553">Role</span></span>

* <span data-ttu-id="8c6d2-554">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-554">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="8c6d2-555">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-555">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="8c6d2-556">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="8c6d2-556">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="8c6d2-557">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="8c6d2-557">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="8c6d2-558">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-558">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8c6d2-559">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8c6d2-559">Service Fabric</span></span>
* <span data-ttu-id="8c6d2-560">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-560">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="8c6d2-561">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-561">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="8c6d2-562">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-562">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-563">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-563">SQL</span></span>

* <span data-ttu-id="8c6d2-564">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="8c6d2-564">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="8c6d2-565">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="8c6d2-565">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="8c6d2-566">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="8c6d2-566">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-567">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-567">Storage</span></span>

* <span data-ttu-id="8c6d2-568">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-568">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="8c6d2-569">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-569">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="8c6d2-570">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-570">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="8c6d2-571">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-571">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="8c6d2-572">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-572">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="8c6d2-573">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-573">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-574">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-574">VM</span></span>

* <span data-ttu-id="8c6d2-575">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="8c6d2-575">Support configuring nsg</span></span>
* <span data-ttu-id="8c6d2-576">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-576">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="8c6d2-577">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="8c6d2-577">Support managed service identities</span></span>
* <span data-ttu-id="8c6d2-578">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-578">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="8c6d2-579">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="8c6d2-579">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="8c6d2-580">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-580">May 10, 2017</span></span>

<span data-ttu-id="8c6d2-581">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="8c6d2-581">Version 2.0.6</span></span>

* <span data-ttu-id="8c6d2-582">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="8c6d2-582">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="8c6d2-583">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-583">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="8c6d2-584">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-584">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="8c6d2-585">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-585">Include Cognitive Services module.</span></span>
* <span data-ttu-id="8c6d2-586">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-586">Include Service Fabric module.</span></span>
* <span data-ttu-id="8c6d2-587">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="8c6d2-587">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="8c6d2-588">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-588">Add support for CDN commands.</span></span>
* <span data-ttu-id="8c6d2-589">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-589">Remove Container module.</span></span>
* <span data-ttu-id="8c6d2-590">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-590">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="8c6d2-591">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-591">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="8c6d2-592">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-592">Core</span></span>

* <span data-ttu-id="8c6d2-593">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-593">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="8c6d2-594">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-594">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="8c6d2-595">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-595">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="8c6d2-596">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-596">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="8c6d2-597">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-597">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="8c6d2-598">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-598">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="8c6d2-599">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-599">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="8c6d2-600">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-600">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="8c6d2-601">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-601">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="8c6d2-602">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="8c6d2-602">core: Improved performance</span></span>
* <span data-ttu-id="8c6d2-603">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="8c6d2-603">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="8c6d2-604">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="8c6d2-604">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="8c6d2-605">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-605">ACS</span></span>

* <span data-ttu-id="8c6d2-606">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-606">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="8c6d2-607">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="8c6d2-607">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="8c6d2-608">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-608">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="8c6d2-609">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-609">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="8c6d2-610">AppService</span><span class="sxs-lookup"><span data-stu-id="8c6d2-610">AppService</span></span>

* <span data-ttu-id="8c6d2-611">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-611">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="8c6d2-612">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="8c6d2-612">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="8c6d2-613">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-613">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="8c6d2-614">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="8c6d2-614">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="8c6d2-615">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="8c6d2-615">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="8c6d2-616">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-616">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="8c6d2-617">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="8c6d2-617">support slot swap with preview</span></span>
* <span data-ttu-id="8c6d2-618">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-618">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="8c6d2-619">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-619">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8c6d2-620">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8c6d2-620">CosmosDB</span></span>

* <span data-ttu-id="8c6d2-621">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-621">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="8c6d2-622">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="8c6d2-622">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="8c6d2-623">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="8c6d2-623">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="8c6d2-624">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="8c6d2-624">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8c6d2-625">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8c6d2-625">Data Lake Analytics</span></span>

* <span data-ttu-id="8c6d2-626">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-626">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="8c6d2-627">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-627">Add support for new catalog item type: package.</span></span> <span data-ttu-id="8c6d2-628">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-628">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="8c6d2-629">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="8c6d2-629">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="8c6d2-630">Tabell</span><span class="sxs-lookup"><span data-stu-id="8c6d2-630">Table</span></span>
  * <span data-ttu-id="8c6d2-631">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="8c6d2-631">Table valued function</span></span>
  * <span data-ttu-id="8c6d2-632">Visa</span><span class="sxs-lookup"><span data-stu-id="8c6d2-632">View</span></span>
  * <span data-ttu-id="8c6d2-633">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-633">Table Statistics.</span></span> <span data-ttu-id="8c6d2-634">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-634">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8c6d2-635">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8c6d2-635">Data Lake Store</span></span>

* <span data-ttu-id="8c6d2-636">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-636">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="8c6d2-637">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-637">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="8c6d2-638">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-638">missed help for access show.</span></span> <span data-ttu-id="8c6d2-639">läggs till.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-639">adding it.</span></span> <span data-ttu-id="8c6d2-640">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-640">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="8c6d2-641">Hitta</span><span class="sxs-lookup"><span data-stu-id="8c6d2-641">Find</span></span>

* <span data-ttu-id="8c6d2-642">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="8c6d2-642">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c6d2-643">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c6d2-643">KeyVault</span></span>

* <span data-ttu-id="8c6d2-644">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="8c6d2-644">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="8c6d2-645">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-645">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="8c6d2-646">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="8c6d2-646">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="8c6d2-647">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-647">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="8c6d2-648">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-648">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="8c6d2-649">Labb</span><span class="sxs-lookup"><span data-stu-id="8c6d2-649">Lab</span></span>

* <span data-ttu-id="8c6d2-650">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-650">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="8c6d2-651">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-651">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="8c6d2-652">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-652">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="8c6d2-653">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-653">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="8c6d2-654">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-654">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="8c6d2-655">Övervaka</span><span class="sxs-lookup"><span data-stu-id="8c6d2-655">Monitor</span></span>

* <span data-ttu-id="8c6d2-656">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-656">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="8c6d2-657">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-657">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="8c6d2-658">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-658">Network</span></span>

* <span data-ttu-id="8c6d2-659">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-659">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="8c6d2-660">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-660">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="8c6d2-661">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-661">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="8c6d2-662">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-662">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="8c6d2-663">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-663">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="8c6d2-664">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-664">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="8c6d2-665">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-665">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="8c6d2-666">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-666">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="8c6d2-667">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-667">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="8c6d2-668">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="8c6d2-668">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="8c6d2-669">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-669">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="8c6d2-670">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="8c6d2-670">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="8c6d2-671">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-671">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="8c6d2-672">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-672">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="8c6d2-673">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-673">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="8c6d2-674">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-674">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="8c6d2-675">Profil</span><span class="sxs-lookup"><span data-stu-id="8c6d2-675">Profile</span></span>

* <span data-ttu-id="8c6d2-676">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-676">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="8c6d2-677">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-677">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="8c6d2-678">Redis</span><span class="sxs-lookup"><span data-stu-id="8c6d2-678">Redis</span></span>

* <span data-ttu-id="8c6d2-679">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="8c6d2-679">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="8c6d2-680">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-680">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="8c6d2-681">Resurs</span><span class="sxs-lookup"><span data-stu-id="8c6d2-681">Resource</span></span>

* <span data-ttu-id="8c6d2-682">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-682">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="8c6d2-683">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-683">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="8c6d2-684">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-684">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="8c6d2-685">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-685">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="8c6d2-686">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-686">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="8c6d2-687">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-687">Add docs for az lock update.</span></span> <span data-ttu-id="8c6d2-688">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-688">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="8c6d2-689">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-689">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="8c6d2-690">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-690">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="8c6d2-691">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-691">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="8c6d2-692">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-692">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="8c6d2-693">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-693">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="8c6d2-694">Roll</span><span class="sxs-lookup"><span data-stu-id="8c6d2-694">Role</span></span>

* <span data-ttu-id="8c6d2-695">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-695">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="8c6d2-696">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-696">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="8c6d2-697">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-697">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="8c6d2-698">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="8c6d2-698">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="8c6d2-699">SQL</span><span class="sxs-lookup"><span data-stu-id="8c6d2-699">SQL</span></span>

* <span data-ttu-id="8c6d2-700">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-700">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="8c6d2-701">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-701">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="8c6d2-702">Lagring</span><span class="sxs-lookup"><span data-stu-id="8c6d2-702">Storage</span></span>

* <span data-ttu-id="8c6d2-703">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-703">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="8c6d2-704">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="8c6d2-704">Add support for incremental blob copy</span></span>
* <span data-ttu-id="8c6d2-705">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="8c6d2-705">Add support for large block blob upload</span></span>
* <span data-ttu-id="8c6d2-706">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="8c6d2-706">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-707">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-707">VM</span></span>

* <span data-ttu-id="8c6d2-708">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="8c6d2-708">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="8c6d2-709">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-709">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="8c6d2-710">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="8c6d2-710">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="8c6d2-711">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-711">az vm/vmss disk</span></span>
  3. <span data-ttu-id="8c6d2-712">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="8c6d2-712">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="8c6d2-713">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="8c6d2-713">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="8c6d2-714">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-714">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="8c6d2-715">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-715">April 3, 2017</span></span>

<span data-ttu-id="8c6d2-716">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="8c6d2-716">Version 2.0.2</span></span>

<span data-ttu-id="8c6d2-717">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-717">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="8c6d2-718">Kärna</span><span class="sxs-lookup"><span data-stu-id="8c6d2-718">Core</span></span>

* <span data-ttu-id="8c6d2-719">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-719">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="8c6d2-720">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-720">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="8c6d2-721">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-721">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="8c6d2-722">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-722">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8c6d2-723">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-723">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="8c6d2-724">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-724">Add prompting for missing template parameters.</span></span> <span data-ttu-id="8c6d2-725">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-725">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="8c6d2-726">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="8c6d2-726">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="8c6d2-727">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="8c6d2-727">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="8c6d2-728">ACS</span><span class="sxs-lookup"><span data-stu-id="8c6d2-728">ACS</span></span>

* <span data-ttu-id="8c6d2-729">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-729">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="8c6d2-730">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-730">Add support for ssh key password prompting.</span></span> <span data-ttu-id="8c6d2-731">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-731">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="8c6d2-732">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-732">Add support for windows clusters.</span></span> <span data-ttu-id="8c6d2-733">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-733">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="8c6d2-734">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-734">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="8c6d2-735">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-735">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="8c6d2-736">AppService</span><span class="sxs-lookup"><span data-stu-id="8c6d2-736">AppService</span></span>

* <span data-ttu-id="8c6d2-737">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-737">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="8c6d2-738">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-738">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="8c6d2-739">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-739">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="8c6d2-740">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-740">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="8c6d2-741">DataLake</span><span class="sxs-lookup"><span data-stu-id="8c6d2-741">DataLake</span></span>

* <span data-ttu-id="8c6d2-742">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-742">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="8c6d2-743">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-743">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="8c6d2-744">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="8c6d2-744">DocuemntDB</span></span>

* <span data-ttu-id="8c6d2-745">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-745">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="8c6d2-746">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8c6d2-746">VM</span></span>

* <span data-ttu-id="8c6d2-747">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-747">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="8c6d2-748">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-748">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="8c6d2-749">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-749">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="8c6d2-750">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-750">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8c6d2-751">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-751">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="8c6d2-752">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-752">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="8c6d2-753">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="8c6d2-753">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="8c6d2-754">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="8c6d2-754">February 27, 2017</span></span>

<span data-ttu-id="8c6d2-755">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="8c6d2-755">Version 2.0.0</span></span>

<span data-ttu-id="8c6d2-756">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="8c6d2-756">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="8c6d2-757">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-757">General availability applies to these command modules:</span></span>
- <span data-ttu-id="8c6d2-758">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-758">Container Service (acs)</span></span>
- <span data-ttu-id="8c6d2-759">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-759">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="8c6d2-760">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8c6d2-760">Networking</span></span>
- <span data-ttu-id="8c6d2-761">Storage</span><span class="sxs-lookup"><span data-stu-id="8c6d2-761">Storage</span></span>

<span data-ttu-id="8c6d2-762">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-762">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="8c6d2-763">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="8c6d2-763">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="8c6d2-764">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-764">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="8c6d2-765">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-765">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="8c6d2-766">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-766">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="8c6d2-767">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-767">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="8c6d2-768">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-768">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="8c6d2-769">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-769">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="8c6d2-770">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-770">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="8c6d2-771">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="8c6d2-771">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="8c6d2-772">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="8c6d2-772">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="8c6d2-773">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="8c6d2-773">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="8c6d2-774">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="8c6d2-774">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="8c6d2-775">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="8c6d2-775">Provide feedback from the command line with the `az feedback` command.</span></span>

