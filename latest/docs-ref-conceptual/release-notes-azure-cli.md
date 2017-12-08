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
ms.openlocfilehash: e02b84891f4bf60cde12591b8e85987f4b3c9e79
ms.sourcegitcommit: a3c8e15eafac1ddc2289110d513b39714a23353b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/07/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="56ec2-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="56ec2-104">Azure CLI 2.0 release notes</span></span>

## <a name="december-5-2017"></a><span data-ttu-id="56ec2-105">5 december 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-105">December 5, 2017</span></span>

<span data-ttu-id="56ec2-106">Version 2.0.22</span><span class="sxs-lookup"><span data-stu-id="56ec2-106">Version 2.0.22</span></span>

* <span data-ttu-id="56ec2-107">`az component` kommandon har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="56ec2-107">Removed `az component` commands.</span></span> <span data-ttu-id="56ec2-108">Använd `az extension` istället</span><span class="sxs-lookup"><span data-stu-id="56ec2-108">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="56ec2-109">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-109">Core</span></span>
* <span data-ttu-id="56ec2-110">`AZURE_US_GOV_CLOUD` AAD-utfärdarslutpunkten har ändrats från login.microsoftonline.com till login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="56ec2-110">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="56ec2-111">Felet med att telemetri kontinuerligt skickades på nytt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-111">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-112">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-112">ACS</span></span>

* <span data-ttu-id="56ec2-113">Kommandona `aks install-connector` och `aks remove-connector` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-113">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="56ec2-114">Förbättrad felrapportering för `acs create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-114">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="56ec2-115">Användning av `aks get-credentials -f` utan fullständig sökväg har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-115">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="56ec2-116">Advisor</span><span class="sxs-lookup"><span data-stu-id="56ec2-116">Advisor</span></span>

* <span data-ttu-id="56ec2-117">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="56ec2-117">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-118">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-118">Appservice</span></span>

* <span data-ttu-id="56ec2-119">Skapande av certifikatnamn med `webapp config ssl upload` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-119">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="56ec2-120">`webapp [list|show]` och `functionapp [list|show]` har åtgärdats för att visa rätt appar</span><span class="sxs-lookup"><span data-stu-id="56ec2-120">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="56ec2-121">Standardvärde har lagts till för `WEBSITE_NODE_DEFAULT_VERSION`</span><span class="sxs-lookup"><span data-stu-id="56ec2-121">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="56ec2-122">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="56ec2-122">Consumption</span></span>

* <span data-ttu-id="56ec2-123">Stöd för API-versionen 2017-11-30 har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-123">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="56ec2-124">Behållare</span><span class="sxs-lookup"><span data-stu-id="56ec2-124">Container</span></span>

* <span data-ttu-id="56ec2-125">Regression till standardportar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-125">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="56ec2-126">Övervaka</span><span class="sxs-lookup"><span data-stu-id="56ec2-126">Monitor</span></span>

* <span data-ttu-id="56ec2-127">Flerdimensionellt stöd för måttkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-127">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-128">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-128">Resource</span></span>

* <span data-ttu-id="56ec2-129">Argumentet `--include-response-body` har lagts till för `resource show`</span><span class="sxs-lookup"><span data-stu-id="56ec2-129">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="56ec2-130">Roll</span><span class="sxs-lookup"><span data-stu-id="56ec2-130">Role</span></span>

* <span data-ttu-id="56ec2-131">Visning av standardtilldelningar för "klassiska" administratörer till `role assignment list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-131">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="56ec2-132">Stöd har lagts till för `ad sp reset-credentials` för att lägga till autentiseringsuppgifter istället för att skriva över</span><span class="sxs-lookup"><span data-stu-id="56ec2-132">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="56ec2-133">Förbättrad felrapportering för `ad sp create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="56ec2-133">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-134">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-134">SQL</span></span>

* <span data-ttu-id="56ec2-135">Kommandona `sql db list-usages` och `sql db show-usage` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-135">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="56ec2-136">Kommandona `sql server conn-policy show` och `sql server conn-policy update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-136">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-137">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-137">VM</span></span>

* <span data-ttu-id="56ec2-138">Zoninformation har lagts till i `az vm list-skus`</span><span class="sxs-lookup"><span data-stu-id="56ec2-138">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="56ec2-139">14 november 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-139">November 14, 2017</span></span>

<span data-ttu-id="56ec2-140">Version 2.0.21</span><span class="sxs-lookup"><span data-stu-id="56ec2-140">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="56ec2-141">ACR</span><span class="sxs-lookup"><span data-stu-id="56ec2-141">ACR</span></span>

* <span data-ttu-id="56ec2-142">Stöd för att skapa webhooks i replikeringsregioner har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-142">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="56ec2-143">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-143">ACS</span></span>

* <span data-ttu-id="56ec2-144">Alla ”agent” till ”nod” har ändrats i AKS</span><span class="sxs-lookup"><span data-stu-id="56ec2-144">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="56ec2-145">Föråldrat `--orchestrator-release`-alternativ för `acs create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-145">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="56ec2-146">Standardstorleken för virtuella datorer för AKS till `Standard_D1_v2` har ändrats</span><span class="sxs-lookup"><span data-stu-id="56ec2-146">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="56ec2-147">Åtgärdade `az aks browse` i Windows</span><span class="sxs-lookup"><span data-stu-id="56ec2-147">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="56ec2-148">Åtgärdade `az aks get-credentials` i Windows</span><span class="sxs-lookup"><span data-stu-id="56ec2-148">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-149">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-149">Appservice</span></span>

* <span data-ttu-id="56ec2-150">Distributionskälla `config-zip` för webappar och funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-150">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="56ec2-151">`--docker-container-logging`-alternativ till `az webapp log config` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-151">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="56ec2-152">Alternativet `storage` från parametern `--web-server-logging` av `az webapp log config` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="56ec2-152">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="56ec2-153">Förbättrade felmeddelanden för `deployment user set`</span><span class="sxs-lookup"><span data-stu-id="56ec2-153">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="56ec2-154">Stöd för att skapa Linux-funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-154">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="56ec2-155">Åtgärdade `list-locations`</span><span class="sxs-lookup"><span data-stu-id="56ec2-155">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="56ec2-156">Batch</span><span class="sxs-lookup"><span data-stu-id="56ec2-156">Batch</span></span>

* <span data-ttu-id="56ec2-157">En bugg har åtgärdats i kommandot för skapande av pool när ett resurs-ID användes med flaggan `--image`</span><span class="sxs-lookup"><span data-stu-id="56ec2-157">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="56ec2-158">Batchai</span><span class="sxs-lookup"><span data-stu-id="56ec2-158">Batchai</span></span>

* <span data-ttu-id="56ec2-159">Ett kort alternativ har lagts till, `-s`, för `--vm-size` VM-storlek i kommandot `file-server create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-159">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="56ec2-160">Kontonamn och nyckelargument har lagts till för `cluster create`-parametrar</span><span class="sxs-lookup"><span data-stu-id="56ec2-160">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="56ec2-161">Dokumentation har skapats för `job list-files` och `job stream-file`</span><span class="sxs-lookup"><span data-stu-id="56ec2-161">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="56ec2-162">Ett kort alternativ har lagts till, `-r`, för `--cluster-name` när klusternamn anges med kommandot `job create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-162">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="56ec2-163">Molnet</span><span class="sxs-lookup"><span data-stu-id="56ec2-163">Cloud</span></span>

* <span data-ttu-id="56ec2-164">`cloud [register|update]` har ändrats för att förhindra att moln registreras som saknar slutpunkter som krävs</span><span class="sxs-lookup"><span data-stu-id="56ec2-164">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="56ec2-165">Behållare</span><span class="sxs-lookup"><span data-stu-id="56ec2-165">Container</span></span>

* <span data-ttu-id="56ec2-166">Stöd för att öppna flera portar har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-166">Added support to open multiple ports</span></span>
* <span data-ttu-id="56ec2-167">Princip för omstart av behållargrupp har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-167">Added container group restart policy</span></span>
* <span data-ttu-id="56ec2-168">Stöd för att montera Azure-filresurs som volym har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-168">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="56ec2-169">Hjälpdokument har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="56ec2-169">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="56ec2-170">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="56ec2-170">Data Lake Analytics</span></span>

* <span data-ttu-id="56ec2-171">`[job|account] list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="56ec2-171">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="56ec2-172">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="56ec2-172">Data Lake Store</span></span>

* <span data-ttu-id="56ec2-173">`account list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="56ec2-173">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="56ec2-174">Anknytning</span><span class="sxs-lookup"><span data-stu-id="56ec2-174">Extension</span></span>

* <span data-ttu-id="56ec2-175">`extension list-available` har lagts till för att tillåta lista över officiella Microsoft-tillägg</span><span class="sxs-lookup"><span data-stu-id="56ec2-175">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="56ec2-176">`--name` har lagts till för `extension [add|update]` för att tillåta installation av tillägg via namn</span><span class="sxs-lookup"><span data-stu-id="56ec2-176">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="56ec2-177">IoT</span><span class="sxs-lookup"><span data-stu-id="56ec2-177">IoT</span></span>

* <span data-ttu-id="56ec2-178">Stöd för certifikatutfärdare (CA) och certifikatkedjor har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-178">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="56ec2-179">Övervaka</span><span class="sxs-lookup"><span data-stu-id="56ec2-179">Monitor</span></span>

* <span data-ttu-id="56ec2-180">`activity-log alert`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-180">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-181">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-181">Network</span></span>

* <span data-ttu-id="56ec2-182">Stöd för CAA DNS-poster har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-182">Added support for CAA DNS records</span></span>
* <span data-ttu-id="56ec2-183">Problem där slutpunkter inte kunde uppdateras med `traffic-manager profile update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-183">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="56ec2-184">Problem där `vnet update --dns-servers` inte fungerade beroende på hur VNET skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-184">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="56ec2-185">Problem där relativa DNS-namn hade importerats felaktigt av `dns zone import` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-185">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="56ec2-186">Reservationer</span><span class="sxs-lookup"><span data-stu-id="56ec2-186">Reservations</span></span>

* <span data-ttu-id="56ec2-187">Inledande förhandsversion</span><span class="sxs-lookup"><span data-stu-id="56ec2-187">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-188">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-188">Resource</span></span>

* <span data-ttu-id="56ec2-189">Stöd för resurs-ID till parametern `--resource` och lås på resursnivå har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-189">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-190">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-190">SQL</span></span>

* <span data-ttu-id="56ec2-191">Parametern `--ignore-missing-vnet-service-endpoint` har lagts till i `sql server vnet-rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-191">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-192">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-192">Storage</span></span>

* <span data-ttu-id="56ec2-193">`storage account create` har ändrats för att använda SKU `Standard_RAGRS` som standard</span><span class="sxs-lookup"><span data-stu-id="56ec2-193">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="56ec2-194">Buggar när fil-/blob-namn som innehåller icke-ASCII-tecken hanteras har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-194">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="56ec2-195">Bugg som förhindrade användning av `--source-uri` med `storage [blob|file] copy start-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-195">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="56ec2-196">Kommandon för blob och borttagning av flera objekt med `storage [blob|file] delete-batch` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-196">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="56ec2-197">Problem vid aktivering av mått med `storage metrics update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-197">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="56ec2-198">Problem med filer över 200 GB vid användning av `storage blob upload-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-198">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="56ec2-199">Problem där `--bypass` och `--default-action` ignorerades av `storage account [create|update]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-199">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-200">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-200">VM</span></span>

* <span data-ttu-id="56ec2-201">En bugg med `vmss create` som förhindrade användning med storleksnivån `Basic` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-201">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="56ec2-202">`--plan` argument till `[vm|vmss] create` för anpassade avbildningar med faktureringsinformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-202">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="56ec2-203">Kommandona `vm secret `[add|remove|list] har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-203">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="56ec2-204">`vm format-secret` har bytt namn till `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="56ec2-204">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="56ec2-205">Argumentet `--encrypt format` har lagts till för `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="56ec2-205">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="56ec2-206">24 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-206">October 24, 2017</span></span>

<span data-ttu-id="56ec2-207">Version 2.0.20</span><span class="sxs-lookup"><span data-stu-id="56ec2-207">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="56ec2-208">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-208">Core</span></span>

* <span data-ttu-id="56ec2-209">`2017-03-09-profile` har uppdaterats för att använda `MGMT_STORAGE`, API-version `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="56ec2-209">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="56ec2-210">ACR</span><span class="sxs-lookup"><span data-stu-id="56ec2-210">ACR</span></span>

* <span data-ttu-id="56ec2-211">Resurshanteringen har uppdaterats för att peka på API-version `2017-10-01`</span><span class="sxs-lookup"><span data-stu-id="56ec2-211">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="56ec2-212">SKU:n för BYOS ("bring your own storage") har ändrats till klassisk</span><span class="sxs-lookup"><span data-stu-id="56ec2-212">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="56ec2-213">Register-SKU:erna har bytt namn till Basic, Standard och Premium</span><span class="sxs-lookup"><span data-stu-id="56ec2-213">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-214">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-214">ACS</span></span>

* <span data-ttu-id="56ec2-215">[FÖRHANDSVERSION] `az aks`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-215">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="56ec2-216">Kubernetes `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-216">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-217">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-217">Appservice</span></span>

* <span data-ttu-id="56ec2-218">Problem med att nedladdade `webapp`-loggar kunde vara ogiltiga har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-218">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="56ec2-219">Komponent</span><span class="sxs-lookup"><span data-stu-id="56ec2-219">Component</span></span>

* <span data-ttu-id="56ec2-220">Ett tydligare utfasningsmeddelande har lagts till för alla installationsprogram och bekräftelsefrågor</span><span class="sxs-lookup"><span data-stu-id="56ec2-220">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="56ec2-221">Övervaka</span><span class="sxs-lookup"><span data-stu-id="56ec2-221">Monitor</span></span>

* <span data-ttu-id="56ec2-222">`action-group`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-222">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-223">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-223">Resource</span></span>

* <span data-ttu-id="56ec2-224">Inkompatibilitet med den senaste versionen av msrest-beroende i `group export` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-224">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="56ec2-225">`policy assignment create` har åtgärdats så att det fungerar med inbyggda principdefinitioner och principuppsättningsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="56ec2-225">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-226">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-226">VM</span></span>

* <span data-ttu-id="56ec2-227">Argumentet `--accelerated-networking` har lagts till för `vmss create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-227">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="56ec2-228">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-228">October 9, 2017</span></span>

<span data-ttu-id="56ec2-229">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="56ec2-229">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="56ec2-230">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-230">Core</span></span>

* <span data-ttu-id="56ec2-231">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-231">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-232">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-232">Appservice</span></span>

* <span data-ttu-id="56ec2-233">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-233">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="56ec2-234">Batch</span><span class="sxs-lookup"><span data-stu-id="56ec2-234">Batch</span></span>

* <span data-ttu-id="56ec2-235">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="56ec2-235">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="56ec2-236">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="56ec2-236">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="56ec2-237">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-237">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="56ec2-238">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="56ec2-238">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="56ec2-239">Batchai</span><span class="sxs-lookup"><span data-stu-id="56ec2-239">Batchai</span></span>

* <span data-ttu-id="56ec2-240">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="56ec2-240">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="56ec2-241">KeyVault</span><span class="sxs-lookup"><span data-stu-id="56ec2-241">Keyvault</span></span>

* <span data-ttu-id="56ec2-242">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="56ec2-242">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="56ec2-243">(#4448)</span><span class="sxs-lookup"><span data-stu-id="56ec2-243">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="56ec2-244">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-244">Network</span></span>

* <span data-ttu-id="56ec2-245">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="56ec2-245">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="56ec2-246">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="56ec2-246">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-247">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-247">Resource</span></span>

* <span data-ttu-id="56ec2-248">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="56ec2-248">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="56ec2-249">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="56ec2-249">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="56ec2-250">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="56ec2-250">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="56ec2-251">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="56ec2-251">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-252">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-252">Sql</span></span>

* <span data-ttu-id="56ec2-253">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="56ec2-253">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="56ec2-254">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="56ec2-254">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="56ec2-255">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="56ec2-255">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-256">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-256">Storage</span></span>

* <span data-ttu-id="56ec2-257">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-257">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-258">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-258">Vm</span></span>

* <span data-ttu-id="56ec2-259">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="56ec2-259">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="56ec2-260">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-260">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="56ec2-261">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="56ec2-261">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="56ec2-262">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-262">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="56ec2-263">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-263">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="56ec2-264">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-264">September 22, 2017</span></span>

<span data-ttu-id="56ec2-265">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="56ec2-265">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-266">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-266">Resource</span></span>

* <span data-ttu-id="56ec2-267">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="56ec2-267">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="56ec2-268">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="56ec2-268">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="56ec2-269">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-269">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="56ec2-270">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="56ec2-270">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-271">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-271">Network</span></span>

* <span data-ttu-id="56ec2-272">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="56ec2-272">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="56ec2-273">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="56ec2-273">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="56ec2-274">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-274">Added `asg` application security group commands</span></span>
* <span data-ttu-id="56ec2-275">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-275">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="56ec2-276">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-276">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="56ec2-277">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-277">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="56ec2-278">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-278">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-279">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-279">Storage</span></span>

* <span data-ttu-id="56ec2-280">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="56ec2-280">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="56ec2-281">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="56ec2-281">Eventgrid</span></span>

* <span data-ttu-id="56ec2-282">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="56ec2-282">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-283">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-283">SQL</span></span>

* <span data-ttu-id="56ec2-284">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="56ec2-284">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="56ec2-285">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="56ec2-285">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="56ec2-286">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-286">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="56ec2-287">KeyVault</span><span class="sxs-lookup"><span data-stu-id="56ec2-287">Keyvault</span></span>

* <span data-ttu-id="56ec2-288">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="56ec2-288">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-289">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-289">VM</span></span>

* <span data-ttu-id="56ec2-290">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-290">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="56ec2-291">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="56ec2-291">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="56ec2-292">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-292">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="56ec2-293">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="56ec2-293">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="56ec2-294">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="56ec2-294">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="56ec2-295">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="56ec2-295">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-296">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-296">ACS</span></span>

* <span data-ttu-id="56ec2-297">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="56ec2-297">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-298">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-298">Appservice</span></span>

* <span data-ttu-id="56ec2-299">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-299">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="56ec2-300">Säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="56ec2-300">Backup</span></span>

* <span data-ttu-id="56ec2-301">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="56ec2-301">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="56ec2-302">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-302">September 11, 2017</span></span>

<span data-ttu-id="56ec2-303">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="56ec2-303">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="56ec2-304">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-304">Core</span></span>

* <span data-ttu-id="56ec2-305">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="56ec2-305">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="56ec2-306">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="56ec2-306">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-307">Acs</span><span class="sxs-lookup"><span data-stu-id="56ec2-307">Acs</span></span>

* <span data-ttu-id="56ec2-308">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-308">Added `acs list-locations` command</span></span>
* <span data-ttu-id="56ec2-309">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="56ec2-309">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-310">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-310">Appservice</span></span>

* <span data-ttu-id="56ec2-311">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-311">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="56ec2-312">CDN</span><span class="sxs-lookup"><span data-stu-id="56ec2-312">CDN</span></span>

* <span data-ttu-id="56ec2-313">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="56ec2-313">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="56ec2-314">Anknytning</span><span class="sxs-lookup"><span data-stu-id="56ec2-314">Extension</span></span>

* <span data-ttu-id="56ec2-315">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="56ec2-315">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="56ec2-316">KeyVault</span><span class="sxs-lookup"><span data-stu-id="56ec2-316">Keyvault</span></span>

* <span data-ttu-id="56ec2-317">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="56ec2-317">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-318">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-318">Network</span></span>

* <span data-ttu-id="56ec2-319">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="56ec2-319">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="56ec2-320">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-320">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="56ec2-321">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-321">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="56ec2-322">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-322">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="56ec2-323">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-323">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-324">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-324">Resource</span></span>

* <span data-ttu-id="56ec2-325">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-325">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="56ec2-326">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-326">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="56ec2-327">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="56ec2-327">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="56ec2-328">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="56ec2-328">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-329">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-329">SQL</span></span>

* <span data-ttu-id="56ec2-330">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-330">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-331">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-331">VM</span></span>

* <span data-ttu-id="56ec2-332">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="56ec2-332">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="56ec2-333">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="56ec2-333">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="56ec2-334">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="56ec2-334">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="56ec2-335">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="56ec2-335">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="56ec2-336">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="56ec2-336">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="56ec2-337">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-337">August 31, 2017</span></span>

<span data-ttu-id="56ec2-338">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="56ec2-338">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="56ec2-339">KeyVault</span><span class="sxs-lookup"><span data-stu-id="56ec2-339">Keyvault</span></span>

* <span data-ttu-id="56ec2-340">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-340">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="56ec2-341">Sf</span><span class="sxs-lookup"><span data-stu-id="56ec2-341">Sf</span></span>

* <span data-ttu-id="56ec2-342">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="56ec2-342">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-343">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-343">Storage</span></span>

* <span data-ttu-id="56ec2-344">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-344">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="56ec2-345">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="56ec2-345">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="56ec2-346">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-346">August 28, 2017</span></span>

<span data-ttu-id="56ec2-347">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="56ec2-347">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="56ec2-348">CLI</span><span class="sxs-lookup"><span data-stu-id="56ec2-348">CLI</span></span>

* <span data-ttu-id="56ec2-349">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-349">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-350">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-350">ACS</span></span>

* <span data-ttu-id="56ec2-351">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="56ec2-351">Corrected preview regions.</span></span>
* <span data-ttu-id="56ec2-352">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="56ec2-352">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="56ec2-353">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="56ec2-353">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-354">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-354">Appservice</span></span>

* <span data-ttu-id="56ec2-355">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-355">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="56ec2-356">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="56ec2-356">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="56ec2-357">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="56ec2-357">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="56ec2-358">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="56ec2-358">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="56ec2-359">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="56ec2-359">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="56ec2-360">IoT</span><span class="sxs-lookup"><span data-stu-id="56ec2-360">IoT</span></span>

* <span data-ttu-id="56ec2-361">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="56ec2-361">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-362">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-362">Network</span></span>

* <span data-ttu-id="56ec2-363">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="56ec2-363">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="56ec2-364">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-364">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="56ec2-365">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="56ec2-365">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="56ec2-366">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-366">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="56ec2-367">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-367">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="56ec2-368">Profil</span><span class="sxs-lookup"><span data-stu-id="56ec2-368">Profile</span></span>

* <span data-ttu-id="56ec2-369">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-369">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="56ec2-370">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="56ec2-370">Service Fabric</span></span>

* <span data-ttu-id="56ec2-371">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="56ec2-371">Preview release</span></span>
* <span data-ttu-id="56ec2-372">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="56ec2-372">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="56ec2-373">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-373">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="56ec2-374">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="56ec2-374">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-375">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-375">Storage</span></span>

* <span data-ttu-id="56ec2-376">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="56ec2-376">Enabled setting blob tier</span></span>
* <span data-ttu-id="56ec2-377">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="56ec2-377">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="56ec2-378">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="56ec2-378">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="56ec2-379">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="56ec2-379">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="56ec2-380">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-380">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="56ec2-381">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="56ec2-381">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-382">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-382">VM</span></span>

* <span data-ttu-id="56ec2-383">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="56ec2-383">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="56ec2-384">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="56ec2-384">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="56ec2-385">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-385">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="56ec2-386">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="56ec2-386">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="56ec2-387">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-387">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="56ec2-388">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-388">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="56ec2-389">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-389">August 15, 2017</span></span>

<span data-ttu-id="56ec2-390">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="56ec2-390">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-391">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-391">ACS</span></span>

* <span data-ttu-id="56ec2-392">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-392">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-393">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-393">Appservice</span></span>

* <span data-ttu-id="56ec2-394">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-394">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="56ec2-395">Event Grid</span><span class="sxs-lookup"><span data-stu-id="56ec2-395">Event Grid</span></span>

* <span data-ttu-id="56ec2-396">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-396">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="56ec2-397">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-397">August 11, 2017</span></span>

<span data-ttu-id="56ec2-398">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="56ec2-398">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-399">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-399">ACS</span></span>

* <span data-ttu-id="56ec2-400">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="56ec2-400">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="56ec2-401">Batch</span><span class="sxs-lookup"><span data-stu-id="56ec2-401">Batch</span></span>

* <span data-ttu-id="56ec2-402">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="56ec2-402">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="56ec2-403">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="56ec2-403">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="56ec2-404">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-404">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="56ec2-405">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="56ec2-405">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="56ec2-406">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="56ec2-406">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="56ec2-407">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="56ec2-407">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="56ec2-408">Komponent</span><span class="sxs-lookup"><span data-stu-id="56ec2-408">Component</span></span>

* <span data-ttu-id="56ec2-409">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="56ec2-409">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="56ec2-410">Behållare</span><span class="sxs-lookup"><span data-stu-id="56ec2-410">Container</span></span>

* <span data-ttu-id="56ec2-411">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="56ec2-411">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="56ec2-412">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="56ec2-412">Data Lake Store</span></span>

* <span data-ttu-id="56ec2-413">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="56ec2-413">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="56ec2-414">Event Grid</span><span class="sxs-lookup"><span data-stu-id="56ec2-414">Event Grid</span></span>

* <span data-ttu-id="56ec2-415">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="56ec2-415">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-416">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-416">Network</span></span>

* <span data-ttu-id="56ec2-417">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="56ec2-417">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="56ec2-418">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="56ec2-418">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="56ec2-419">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="56ec2-419">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="56ec2-420">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="56ec2-420">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="56ec2-421">Profil</span><span class="sxs-lookup"><span data-stu-id="56ec2-421">Profile</span></span>

* <span data-ttu-id="56ec2-422">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="56ec2-422">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-423">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-423">Storage</span></span>

* <span data-ttu-id="56ec2-424">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="56ec2-424">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-425">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-425">VM</span></span>

* <span data-ttu-id="56ec2-426">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="56ec2-426">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="56ec2-427">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="56ec2-427">Exposed `list-skus` command</span></span>
* <span data-ttu-id="56ec2-428">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="56ec2-428">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="56ec2-429">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="56ec2-429">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="56ec2-430">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="56ec2-430">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="56ec2-431">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-431">July 28, 2017</span></span>

<span data-ttu-id="56ec2-432">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="56ec2-432">Version 2.0.12</span></span>

* <span data-ttu-id="56ec2-433">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-433">Added container commands</span></span>
* <span data-ttu-id="56ec2-434">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-434">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="56ec2-435">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-435">Core</span></span>

* <span data-ttu-id="56ec2-436">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="56ec2-436">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="56ec2-437">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-437">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="56ec2-438">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="56ec2-438">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="56ec2-439">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="56ec2-439">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="56ec2-440">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="56ec2-440">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="56ec2-441">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="56ec2-441">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="56ec2-442">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="56ec2-442">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="56ec2-443">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="56ec2-443">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="56ec2-444">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="56ec2-444">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="56ec2-445">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="56ec2-445">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="56ec2-446">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="56ec2-446">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="56ec2-447">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="56ec2-447">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="56ec2-448">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="56ec2-448">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="56ec2-449">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="56ec2-449">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="56ec2-450">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="56ec2-450">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="56ec2-451">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="56ec2-451">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="56ec2-452">ACR</span><span class="sxs-lookup"><span data-stu-id="56ec2-452">ACR</span></span>

* <span data-ttu-id="56ec2-453">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="56ec2-453">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="56ec2-454">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="56ec2-454">Support SKU update for managed registries</span></span>
* <span data-ttu-id="56ec2-455">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-455">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="56ec2-456">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="56ec2-456">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="56ec2-457">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="56ec2-457">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="56ec2-458">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="56ec2-458">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-459">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-459">ACS</span></span>

* <span data-ttu-id="56ec2-460">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="56ec2-460">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-461">App Service</span><span class="sxs-lookup"><span data-stu-id="56ec2-461">Appservice</span></span>

* <span data-ttu-id="56ec2-462">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="56ec2-462">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="56ec2-463">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="56ec2-463">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="56ec2-464">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="56ec2-464">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="56ec2-465">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="56ec2-465">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="56ec2-466">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="56ec2-466">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="56ec2-467">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="56ec2-467">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="56ec2-468">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="56ec2-468">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="56ec2-469">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="56ec2-469">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="56ec2-470">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="56ec2-470">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="56ec2-471">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="56ec2-471">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="56ec2-472">Batch</span><span class="sxs-lookup"><span data-stu-id="56ec2-472">Batch</span></span>

* <span data-ttu-id="56ec2-473">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="56ec2-473">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="56ec2-474">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="56ec2-474">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="56ec2-475">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-475">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="56ec2-476">CDN</span><span class="sxs-lookup"><span data-stu-id="56ec2-476">CDN</span></span>

* <span data-ttu-id="56ec2-477">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="56ec2-477">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="56ec2-478">Molnet</span><span class="sxs-lookup"><span data-stu-id="56ec2-478">Cloud</span></span>

* <span data-ttu-id="56ec2-479">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="56ec2-479">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="56ec2-480">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="56ec2-480">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="56ec2-481">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="56ec2-481">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="56ec2-482">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="56ec2-482">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="56ec2-483">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="56ec2-483">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="56ec2-484">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="56ec2-484">CosmosDB</span></span>

* <span data-ttu-id="56ec2-485">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="56ec2-485">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="56ec2-486">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="56ec2-486">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="56ec2-487">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="56ec2-487">Data Lake Analytics</span></span>

* <span data-ttu-id="56ec2-488">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="56ec2-488">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="56ec2-489">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-489">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="56ec2-490">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-490">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="56ec2-491">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="56ec2-491">Data Lake Store</span></span>

* <span data-ttu-id="56ec2-492">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-492">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="56ec2-493">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="56ec2-493">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="56ec2-494">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="56ec2-494">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="56ec2-495">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="56ec2-495">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="56ec2-496">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="56ec2-496">Interactive</span></span>

* <span data-ttu-id="56ec2-497">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="56ec2-497">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="56ec2-498">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="56ec2-498">Increased test coverage</span></span>
* <span data-ttu-id="56ec2-499">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="56ec2-499">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="56ec2-500">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="56ec2-500">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="56ec2-501">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="56ec2-501">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="56ec2-502">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="56ec2-502">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="56ec2-503">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="56ec2-503">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="56ec2-504">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-504">Added `--progress` flag</span></span>
* <span data-ttu-id="56ec2-505">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="56ec2-505">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="56ec2-506">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="56ec2-506">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="56ec2-507">IoT</span><span class="sxs-lookup"><span data-stu-id="56ec2-507">IoT</span></span>

* <span data-ttu-id="56ec2-508">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="56ec2-508">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="56ec2-509">(#3934)</span><span class="sxs-lookup"><span data-stu-id="56ec2-509">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="56ec2-510">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="56ec2-510">Key vault</span></span>

* <span data-ttu-id="56ec2-511">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="56ec2-511">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="56ec2-512">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="56ec2-512">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="56ec2-513">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="56ec2-513">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="56ec2-514">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="56ec2-514">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="56ec2-515">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="56ec2-515">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="56ec2-516">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="56ec2-516">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="56ec2-517">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="56ec2-517">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="56ec2-518">(#3307)</span><span class="sxs-lookup"><span data-stu-id="56ec2-518">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="56ec2-519">Labb</span><span class="sxs-lookup"><span data-stu-id="56ec2-519">Lab</span></span>

* <span data-ttu-id="56ec2-520">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="56ec2-520">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="56ec2-521">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="56ec2-521">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="56ec2-522">Övervaka</span><span class="sxs-lookup"><span data-stu-id="56ec2-522">Monitor</span></span>

* <span data-ttu-id="56ec2-523">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="56ec2-523">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="56ec2-524">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="56ec2-524">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="56ec2-525">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="56ec2-525">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="56ec2-526">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="56ec2-526">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="56ec2-527">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="56ec2-527">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="56ec2-528">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="56ec2-528">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="56ec2-529">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="56ec2-529">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="56ec2-530">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="56ec2-530">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="56ec2-531">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="56ec2-531">`location` no longer required</span></span>
  * <span data-ttu-id="56ec2-532">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="56ec2-532">Add name and ID support for target</span></span>
  * <span data-ttu-id="56ec2-533">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="56ec2-533">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="56ec2-534">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="56ec2-534">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="56ec2-535">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="56ec2-535">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="56ec2-536">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="56ec2-536">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="56ec2-537">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="56ec2-537">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="56ec2-538">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-538">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-539">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-539">Network</span></span>

* <span data-ttu-id="56ec2-540">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-540">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="56ec2-541">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-541">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="56ec2-542">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="56ec2-542">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="56ec2-543">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="56ec2-543">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="56ec2-544">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-544">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="56ec2-545">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-545">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="56ec2-546">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="56ec2-546">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="56ec2-547">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="56ec2-547">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="56ec2-548">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="56ec2-548">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="56ec2-549">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="56ec2-549">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="56ec2-550">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-550">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="56ec2-551">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="56ec2-551">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="56ec2-552">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="56ec2-552">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="56ec2-553">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-553">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="56ec2-554">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-554">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="56ec2-555">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-555">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="56ec2-556">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-556">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="56ec2-557">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="56ec2-557">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="56ec2-558">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-558">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="56ec2-559">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-559">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="56ec2-560">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="56ec2-560">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="56ec2-561">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="56ec2-561">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="56ec2-562">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="56ec2-562">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="56ec2-563">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="56ec2-563">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="56ec2-564">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="56ec2-564">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="56ec2-565">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="56ec2-565">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="56ec2-566">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="56ec2-566">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="56ec2-567">Profil</span><span class="sxs-lookup"><span data-stu-id="56ec2-567">Profile</span></span>

* <span data-ttu-id="56ec2-568">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="56ec2-568">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="56ec2-569">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="56ec2-569">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="56ec2-570">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="56ec2-570">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="56ec2-571">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="56ec2-571">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="56ec2-572">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="56ec2-572">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="56ec2-573">RDBMS</span><span class="sxs-lookup"><span data-stu-id="56ec2-573">RDBMS</span></span>

* <span data-ttu-id="56ec2-574">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="56ec2-574">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="56ec2-575">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="56ec2-575">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="56ec2-576">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="56ec2-576">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="56ec2-577">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="56ec2-577">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-578">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-578">Resource</span></span>

* <span data-ttu-id="56ec2-579">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-579">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="56ec2-580">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="56ec2-580">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="56ec2-581">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="56ec2-581">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="56ec2-582">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="56ec2-582">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="56ec2-583">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="56ec2-583">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="56ec2-584">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="56ec2-584">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="56ec2-585">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="56ec2-585">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="56ec2-586">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="56ec2-586">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="56ec2-587">Roll</span><span class="sxs-lookup"><span data-stu-id="56ec2-587">Role</span></span>

* <span data-ttu-id="56ec2-588">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="56ec2-588">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="56ec2-589">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="56ec2-589">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="56ec2-590">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="56ec2-590">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="56ec2-591">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="56ec2-591">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="56ec2-592">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="56ec2-592">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="56ec2-593">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="56ec2-593">Service Fabric</span></span>
* <span data-ttu-id="56ec2-594">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="56ec2-594">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="56ec2-595">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="56ec2-595">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="56ec2-596">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="56ec2-596">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-597">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-597">SQL</span></span>

* <span data-ttu-id="56ec2-598">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="56ec2-598">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="56ec2-599">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="56ec2-599">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="56ec2-600">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="56ec2-600">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-601">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-601">Storage</span></span>

* <span data-ttu-id="56ec2-602">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="56ec2-602">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="56ec2-603">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="56ec2-603">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="56ec2-604">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="56ec2-604">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="56ec2-605">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="56ec2-605">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="56ec2-606">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="56ec2-606">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="56ec2-607">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="56ec2-607">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-608">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-608">VM</span></span>

* <span data-ttu-id="56ec2-609">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="56ec2-609">Support configuring nsg</span></span>
* <span data-ttu-id="56ec2-610">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="56ec2-610">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="56ec2-611">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="56ec2-611">Support managed service identities</span></span>
* <span data-ttu-id="56ec2-612">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-612">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="56ec2-613">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="56ec2-613">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="56ec2-614">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-614">May 10, 2017</span></span>

<span data-ttu-id="56ec2-615">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="56ec2-615">Version 2.0.6</span></span>

* <span data-ttu-id="56ec2-616">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="56ec2-616">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="56ec2-617">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="56ec2-617">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="56ec2-618">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="56ec2-618">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="56ec2-619">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="56ec2-619">Include Cognitive Services module.</span></span>
* <span data-ttu-id="56ec2-620">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="56ec2-620">Include Service Fabric module.</span></span>
* <span data-ttu-id="56ec2-621">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="56ec2-621">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="56ec2-622">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="56ec2-622">Add support for CDN commands.</span></span>
* <span data-ttu-id="56ec2-623">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="56ec2-623">Remove Container module.</span></span>
* <span data-ttu-id="56ec2-624">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="56ec2-624">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="56ec2-625">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="56ec2-625">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="56ec2-626">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-626">Core</span></span>

* <span data-ttu-id="56ec2-627">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="56ec2-627">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="56ec2-628">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="56ec2-628">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="56ec2-629">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="56ec2-629">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="56ec2-630">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="56ec2-630">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="56ec2-631">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="56ec2-631">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="56ec2-632">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="56ec2-632">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="56ec2-633">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="56ec2-633">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="56ec2-634">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="56ec2-634">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="56ec2-635">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="56ec2-635">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="56ec2-636">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="56ec2-636">core: Improved performance</span></span>
* <span data-ttu-id="56ec2-637">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="56ec2-637">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="56ec2-638">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="56ec2-638">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-639">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-639">ACS</span></span>

* <span data-ttu-id="56ec2-640">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="56ec2-640">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="56ec2-641">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="56ec2-641">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="56ec2-642">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="56ec2-642">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="56ec2-643">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="56ec2-643">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-644">AppService</span><span class="sxs-lookup"><span data-stu-id="56ec2-644">AppService</span></span>

* <span data-ttu-id="56ec2-645">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="56ec2-645">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="56ec2-646">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="56ec2-646">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="56ec2-647">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="56ec2-647">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="56ec2-648">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="56ec2-648">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="56ec2-649">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="56ec2-649">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="56ec2-650">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="56ec2-650">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="56ec2-651">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="56ec2-651">support slot swap with preview</span></span>
* <span data-ttu-id="56ec2-652">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="56ec2-652">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="56ec2-653">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="56ec2-653">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="56ec2-654">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="56ec2-654">CosmosDB</span></span>

* <span data-ttu-id="56ec2-655">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="56ec2-655">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="56ec2-656">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="56ec2-656">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="56ec2-657">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="56ec2-657">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="56ec2-658">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="56ec2-658">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="56ec2-659">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="56ec2-659">Data Lake Analytics</span></span>

* <span data-ttu-id="56ec2-660">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="56ec2-660">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="56ec2-661">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="56ec2-661">Add support for new catalog item type: package.</span></span> <span data-ttu-id="56ec2-662">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="56ec2-662">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="56ec2-663">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="56ec2-663">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="56ec2-664">Tabell</span><span class="sxs-lookup"><span data-stu-id="56ec2-664">Table</span></span>
  * <span data-ttu-id="56ec2-665">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="56ec2-665">Table valued function</span></span>
  * <span data-ttu-id="56ec2-666">Visa</span><span class="sxs-lookup"><span data-stu-id="56ec2-666">View</span></span>
  * <span data-ttu-id="56ec2-667">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="56ec2-667">Table Statistics.</span></span> <span data-ttu-id="56ec2-668">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="56ec2-668">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="56ec2-669">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="56ec2-669">Data Lake Store</span></span>

* <span data-ttu-id="56ec2-670">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="56ec2-670">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="56ec2-671">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="56ec2-671">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="56ec2-672">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="56ec2-672">missed help for access show.</span></span> <span data-ttu-id="56ec2-673">läggs till.</span><span class="sxs-lookup"><span data-stu-id="56ec2-673">adding it.</span></span> <span data-ttu-id="56ec2-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="56ec2-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="56ec2-675">Hitta</span><span class="sxs-lookup"><span data-stu-id="56ec2-675">Find</span></span>

* <span data-ttu-id="56ec2-676">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="56ec2-676">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="56ec2-677">KeyVault</span><span class="sxs-lookup"><span data-stu-id="56ec2-677">KeyVault</span></span>

* <span data-ttu-id="56ec2-678">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="56ec2-678">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="56ec2-679">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="56ec2-679">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="56ec2-680">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="56ec2-680">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="56ec2-681">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="56ec2-681">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="56ec2-682">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="56ec2-682">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="56ec2-683">Labb</span><span class="sxs-lookup"><span data-stu-id="56ec2-683">Lab</span></span>

* <span data-ttu-id="56ec2-684">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="56ec2-684">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="56ec2-685">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="56ec2-685">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="56ec2-686">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="56ec2-686">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="56ec2-687">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="56ec2-687">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="56ec2-688">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="56ec2-688">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="56ec2-689">Övervaka</span><span class="sxs-lookup"><span data-stu-id="56ec2-689">Monitor</span></span>

* <span data-ttu-id="56ec2-690">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="56ec2-690">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="56ec2-691">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="56ec2-691">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="56ec2-692">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-692">Network</span></span>

* <span data-ttu-id="56ec2-693">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-693">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="56ec2-694">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-694">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="56ec2-695">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="56ec2-695">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="56ec2-696">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="56ec2-696">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="56ec2-697">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56ec2-697">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="56ec2-698">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="56ec2-698">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="56ec2-699">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="56ec2-699">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="56ec2-700">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="56ec2-700">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="56ec2-701">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-701">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="56ec2-702">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="56ec2-702">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="56ec2-703">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="56ec2-703">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="56ec2-704">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="56ec2-704">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="56ec2-705">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="56ec2-705">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="56ec2-706">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="56ec2-706">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="56ec2-707">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="56ec2-707">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="56ec2-708">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="56ec2-708">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="56ec2-709">Profil</span><span class="sxs-lookup"><span data-stu-id="56ec2-709">Profile</span></span>

* <span data-ttu-id="56ec2-710">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="56ec2-710">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="56ec2-711">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="56ec2-711">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="56ec2-712">Redis</span><span class="sxs-lookup"><span data-stu-id="56ec2-712">Redis</span></span>

* <span data-ttu-id="56ec2-713">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="56ec2-713">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="56ec2-714">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="56ec2-714">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="56ec2-715">Resurs</span><span class="sxs-lookup"><span data-stu-id="56ec2-715">Resource</span></span>

* <span data-ttu-id="56ec2-716">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="56ec2-716">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="56ec2-717">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="56ec2-717">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="56ec2-718">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="56ec2-718">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="56ec2-719">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="56ec2-719">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="56ec2-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="56ec2-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="56ec2-721">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="56ec2-721">Add docs for az lock update.</span></span> <span data-ttu-id="56ec2-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="56ec2-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="56ec2-723">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="56ec2-723">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="56ec2-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="56ec2-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="56ec2-725">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="56ec2-725">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="56ec2-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="56ec2-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="56ec2-727">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="56ec2-727">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="56ec2-728">Roll</span><span class="sxs-lookup"><span data-stu-id="56ec2-728">Role</span></span>

* <span data-ttu-id="56ec2-729">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="56ec2-729">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="56ec2-730">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="56ec2-730">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="56ec2-731">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="56ec2-731">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="56ec2-732">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="56ec2-732">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="56ec2-733">SQL</span><span class="sxs-lookup"><span data-stu-id="56ec2-733">SQL</span></span>

* <span data-ttu-id="56ec2-734">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="56ec2-734">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="56ec2-735">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="56ec2-735">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="56ec2-736">Lagring</span><span class="sxs-lookup"><span data-stu-id="56ec2-736">Storage</span></span>

* <span data-ttu-id="56ec2-737">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-737">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="56ec2-738">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="56ec2-738">Add support for incremental blob copy</span></span>
* <span data-ttu-id="56ec2-739">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="56ec2-739">Add support for large block blob upload</span></span>
* <span data-ttu-id="56ec2-740">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="56ec2-740">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-741">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-741">VM</span></span>

* <span data-ttu-id="56ec2-742">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="56ec2-742">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="56ec2-743">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="56ec2-743">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="56ec2-744">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="56ec2-744">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="56ec2-745">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="56ec2-745">az vm/vmss disk</span></span>
  3. <span data-ttu-id="56ec2-746">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="56ec2-746">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="56ec2-747">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="56ec2-747">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="56ec2-748">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="56ec2-748">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="56ec2-749">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-749">April 3, 2017</span></span>

<span data-ttu-id="56ec2-750">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="56ec2-750">Version 2.0.2</span></span>

<span data-ttu-id="56ec2-751">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="56ec2-751">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="56ec2-752">Kärna</span><span class="sxs-lookup"><span data-stu-id="56ec2-752">Core</span></span>

* <span data-ttu-id="56ec2-753">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="56ec2-753">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="56ec2-754">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="56ec2-754">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="56ec2-755">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="56ec2-755">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="56ec2-756">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="56ec2-756">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="56ec2-757">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="56ec2-757">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="56ec2-758">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="56ec2-758">Add prompting for missing template parameters.</span></span> <span data-ttu-id="56ec2-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="56ec2-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="56ec2-760">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="56ec2-760">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="56ec2-761">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="56ec2-761">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="56ec2-762">ACS</span><span class="sxs-lookup"><span data-stu-id="56ec2-762">ACS</span></span>

* <span data-ttu-id="56ec2-763">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="56ec2-763">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="56ec2-764">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="56ec2-764">Add support for ssh key password prompting.</span></span> <span data-ttu-id="56ec2-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="56ec2-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="56ec2-766">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="56ec2-766">Add support for windows clusters.</span></span> <span data-ttu-id="56ec2-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="56ec2-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="56ec2-768">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="56ec2-768">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="56ec2-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="56ec2-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="56ec2-770">AppService</span><span class="sxs-lookup"><span data-stu-id="56ec2-770">AppService</span></span>

* <span data-ttu-id="56ec2-771">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="56ec2-771">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="56ec2-772">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="56ec2-772">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="56ec2-773">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="56ec2-773">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="56ec2-774">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="56ec2-774">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="56ec2-775">DataLake</span><span class="sxs-lookup"><span data-stu-id="56ec2-775">DataLake</span></span>

* <span data-ttu-id="56ec2-776">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="56ec2-776">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="56ec2-777">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="56ec2-777">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="56ec2-778">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="56ec2-778">DocuemntDB</span></span>

* <span data-ttu-id="56ec2-779">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="56ec2-779">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="56ec2-780">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="56ec2-780">VM</span></span>

* <span data-ttu-id="56ec2-781">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="56ec2-781">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="56ec2-782">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="56ec2-782">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="56ec2-783">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="56ec2-783">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="56ec2-784">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="56ec2-784">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="56ec2-785">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="56ec2-785">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="56ec2-786">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="56ec2-786">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="56ec2-787">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="56ec2-787">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="56ec2-788">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="56ec2-788">February 27, 2017</span></span>

<span data-ttu-id="56ec2-789">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="56ec2-789">Version 2.0.0</span></span>

<span data-ttu-id="56ec2-790">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="56ec2-790">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="56ec2-791">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="56ec2-791">General availability applies to these command modules:</span></span>
- <span data-ttu-id="56ec2-792">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="56ec2-792">Container Service (acs)</span></span>
- <span data-ttu-id="56ec2-793">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="56ec2-793">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="56ec2-794">Nätverk</span><span class="sxs-lookup"><span data-stu-id="56ec2-794">Networking</span></span>
- <span data-ttu-id="56ec2-795">Storage</span><span class="sxs-lookup"><span data-stu-id="56ec2-795">Storage</span></span>

<span data-ttu-id="56ec2-796">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="56ec2-796">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="56ec2-797">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="56ec2-797">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="56ec2-798">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-798">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="56ec2-799">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="56ec2-799">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="56ec2-800">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-800">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="56ec2-801">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="56ec2-801">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="56ec2-802">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="56ec2-802">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="56ec2-803">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="56ec2-803">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="56ec2-804">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="56ec2-804">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="56ec2-805">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="56ec2-805">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="56ec2-806">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="56ec2-806">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="56ec2-807">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="56ec2-807">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="56ec2-808">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="56ec2-808">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="56ec2-809">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="56ec2-809">Provide feedback from the command line with the `az feedback` command.</span></span>

