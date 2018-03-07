---
title: Viktig information om Azure CLI 2.0
description: "Lär dig mer om de senaste uppdateringarna till Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 01078b7a3665f563f0a6b1d809c9a41f18d136d6
ms.sourcegitcommit: f3ab5da6019083ef2482b62c7355817e6170dcfb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/28/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="bd7fe-103">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="bd7fe-103">Azure CLI 2.0 release notes</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="bd7fe-104">27 februari 2018</span><span class="sxs-lookup"><span data-stu-id="bd7fe-104">February 27, 2018</span></span>

<span data-ttu-id="bd7fe-105">Version 2.0.28</span><span class="sxs-lookup"><span data-stu-id="bd7fe-105">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-106">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-106">Core</span></span>

* <span data-ttu-id="bd7fe-107">[#5184](https://github.com/Azure/azure-cli/issues/5184) har korrigerats: Installationsproblem för Homebrew</span><span class="sxs-lookup"><span data-stu-id="bd7fe-107">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="bd7fe-108">Stöd för tilläggstelemetri med anpassade nycklar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-108">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="bd7fe-109">HTTP-loggar för `--debug` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-109">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-110">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-110">ACS</span></span>

* <span data-ttu-id="bd7fe-111">Helm-diagrammet `virtual-kubelet-for-aks` för `aks install-connector` har ändrats så att det används som standard</span><span class="sxs-lookup"><span data-stu-id="bd7fe-111">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="bd7fe-112">Åtgärdat problem: Problem med otillräckliga behörigheter för tjänstens huvudnamn för att skapa ACI-behållargrupp</span><span class="sxs-lookup"><span data-stu-id="bd7fe-112">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="bd7fe-113">Parametrarna `--aci-container-group`, `--location` och `--image-tag` har lagts till i `aks install-connector`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-113">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="bd7fe-114">Utfasningsmeddelande har tagits bort från `aks get-versions`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-114">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-115">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-115">Appservice</span></span>

* <span data-ttu-id="bd7fe-116">Uppdateringar för ny SDK-version (azure-mgmt-web 0.35.0)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-116">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="bd7fe-117">[#5538](https://github.com/Azure/azure-cli/issues/5538) har korrigerats: `Free` rapporterad som ogiltig SKU</span><span class="sxs-lookup"><span data-stu-id="bd7fe-117">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="bd7fe-118">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="bd7fe-118">Cognitive Services</span></span>

* <span data-ttu-id="bd7fe-119">”Meddelandet” när du skapar ett nytt Cognitive Services-konto har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-119">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="bd7fe-120">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-120">Consumption</span></span>

* <span data-ttu-id="bd7fe-121">Nya kommandon har lagts till för prisdokument-API</span><span class="sxs-lookup"><span data-stu-id="bd7fe-121">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="bd7fe-122">De befintliga formaten för användningsinformation och information om reservation har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-122">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-123">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-123">Container</span></span>

* <span data-ttu-id="bd7fe-124">Argumenten `--secrets` och `--secrets-mount-path` har lagts till i `container create` för att använda hemligheter i ACI</span><span class="sxs-lookup"><span data-stu-id="bd7fe-124">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-125">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-125">Network</span></span>

* <span data-ttu-id="bd7fe-126">[#5559](https://github.com/Azure/azure-cli/issues/5559) har åtgärdats: Klient saknas i `network vnet-gateway vpn-client generate`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-126">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-127">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-127">Resource</span></span>

* <span data-ttu-id="bd7fe-128">`group deployment export` har ändrats för att visa en delmall och felmeddelanden vid fel</span><span class="sxs-lookup"><span data-stu-id="bd7fe-128">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-129">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-129">Role</span></span>

* <span data-ttu-id="bd7fe-130">`role assignment list-changelogs` har lagts till för att möjliggöra granskning av roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="bd7fe-130">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-131">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-131">SQL</span></span>

* <span data-ttu-id="bd7fe-132">Stöd för zonredundans har lagts till för databaser och elastiska pooler vid skapande och uppdatering</span><span class="sxs-lookup"><span data-stu-id="bd7fe-132">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-133">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-133">Storage</span></span>

* <span data-ttu-id="bd7fe-134">Stöd för att ange mål-sökväg/prefix för `storage blob [upload-batch|download-batch]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-134">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-135">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-135">VM</span></span>

* <span data-ttu-id="bd7fe-136">Stöd för att koppla/koppla från diskar på en enda VMSS-instans har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-136">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="bd7fe-137">13 februari 2018</span><span class="sxs-lookup"><span data-stu-id="bd7fe-137">February 13, 2018</span></span>

<span data-ttu-id="bd7fe-138">Version 2.0.27</span><span class="sxs-lookup"><span data-stu-id="bd7fe-138">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-139">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-139">Core</span></span>

* <span data-ttu-id="bd7fe-140">Autentiseringen har ändrats till nyckel för både prenumerations-ID och namn för MSI-inloggningen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-140">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-141">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-141">ACS</span></span>

* <span data-ttu-id="bd7fe-142">[VIKTIG ÄNDRING] `aks get-versions` har bytt namn till `aks get-upgrades` för noggrannhet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-142">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="bd7fe-143">`aks get-versions` har ändrats för att visa Kubernetes-versioner som är tillgängliga för `aks create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-143">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="bd7fe-144">`aks create`-standardvärden har ändrats för att låta servern välja version av Kubernetes</span><span class="sxs-lookup"><span data-stu-id="bd7fe-144">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="bd7fe-145">Hjälpmeddelanden som hänvisar till tjänstens huvudnamn som genererats av AKS har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-145">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="bd7fe-146">Nodstorlekar som är standard för `aks create` har ändrats från "Standard\_D1\_v2" till "Standard\_DS1\_v2"</span><span class="sxs-lookup"><span data-stu-id="bd7fe-146">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="bd7fe-147">Tillförlitligheten har förbättrats för att hitta instrumentpanelen för `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-147">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="bd7fe-148">`aks get-credentials` har åtgärdats för att hantera Unicode-fel vid inläsning av Kubernetes konfigurationsfiler</span><span class="sxs-lookup"><span data-stu-id="bd7fe-148">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="bd7fe-149">Ett meddelande för `az aks install-cli` har lagts till för att få hjälp med `kubectl` i `$PATH`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-149">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-150">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-150">Appservice</span></span>

* <span data-ttu-id="bd7fe-151">Problem har åtgärdats där `webapp [backup|restore]` misslyckades på grund av en null-referens</span><span class="sxs-lookup"><span data-stu-id="bd7fe-151">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="bd7fe-152">Stöd för standard-apptjänstplaner via `az configure --defaults appserviceplan=my-asp` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-152">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="bd7fe-153">CDN</span><span class="sxs-lookup"><span data-stu-id="bd7fe-153">CDN</span></span>

* <span data-ttu-id="bd7fe-154">`cdn custom-domain [enable-https|disable-https]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-154">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-155">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-155">Container</span></span>

* <span data-ttu-id="bd7fe-156">`--follow`-alternativ för `az container logs` för direktuppspelningsloggar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-156">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="bd7fe-157">`container attach`-kommando som bifogar lokala standard-utdata och felströmmar till en behållare i en behållargrupp har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-157">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="bd7fe-158">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-158">CosmosDB</span></span>

* <span data-ttu-id="bd7fe-159">Stöd har lagts till för att konfigurera funktioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-159">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="bd7fe-160">Anknytning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-160">Extension</span></span>

* <span data-ttu-id="bd7fe-161">Stöd för `--pip-proxy`-parameter för `az extension [add|update]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-161">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="bd7fe-162">Stöd för `--pip-extra-index-urls`-argument för `az extension [add|update]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-162">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="bd7fe-163">Feedback</span><span class="sxs-lookup"><span data-stu-id="bd7fe-163">Feedback</span></span>

* <span data-ttu-id="bd7fe-164">Tilläggsinformation för telemetridata har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-164">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="bd7fe-165">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="bd7fe-165">Interactive</span></span>

* <span data-ttu-id="bd7fe-166">Problem har åtgärdats där användaren uppmanades att logga in vid användning av interaktivt läge i Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="bd7fe-166">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="bd7fe-167">Regression med saknade kompletteringar för parametrar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-167">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="bd7fe-168">IoT</span><span class="sxs-lookup"><span data-stu-id="bd7fe-168">IoT</span></span>

* <span data-ttu-id="bd7fe-169">Problem har åtgärdats där `iot dps access policy [create|update]` returnerade fel i stil med "det gick inte att hitta" även när processen lyckades.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-169">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="bd7fe-170">Problem har åtgärdats där `iot dps linked-hub [create|update]` returnerade fel i stil med "det gick inte att hitta" även när processen lyckades.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-170">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="bd7fe-171">`--no-wait`-stöd har lagts till för `iot dps access policy [create|update]` och `iot dps linked-hub [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-171">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="bd7fe-172">`iot hub create` har ändrats för att tillåta att du anger antalet partitioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-172">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-173">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-173">Monitor</span></span>

* <span data-ttu-id="bd7fe-174">Kommandot `az monitor log-profiles create` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-174">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-175">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-175">Network</span></span>

* <span data-ttu-id="bd7fe-176">Alternativet `--tags` har korrigerats för följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-176">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="bd7fe-177">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-177">Profile</span></span>

* <span data-ttu-id="bd7fe-178">`az login` har aktiverats från interaktivt läge</span><span class="sxs-lookup"><span data-stu-id="bd7fe-178">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-179">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-179">Resource</span></span>

* <span data-ttu-id="bd7fe-180">`feature show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-180">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-181">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-181">Role</span></span>

* <span data-ttu-id="bd7fe-182">Argumentet `--available-to-other-tenants` har lagts till för `ad app update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-182">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-183">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-183">SQL</span></span>

* <span data-ttu-id="bd7fe-184">`sql server dns-alias`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-184">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="bd7fe-185">`sql db rename` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-185">Added `sql db rename`</span></span>
* <span data-ttu-id="bd7fe-186">Stöd för `--ids`-argumentet för alla SQL-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-186">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-187">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-187">Storage</span></span>

* <span data-ttu-id="bd7fe-188">Kommandona `storage blob service-properties delete-policy` och `storage blob undelete` har lagts till för att aktivera mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-188">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-189">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-189">VM</span></span>

* <span data-ttu-id="bd7fe-190">En krasch som inträffade när VM-krypteringen inte kunde initieras helt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-190">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="bd7fe-191">ID har lagts till för huvudnamnets utdata när du aktiverar MSI</span><span class="sxs-lookup"><span data-stu-id="bd7fe-191">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="bd7fe-192">Åtgärdade `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-192">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="bd7fe-193">31 januari 2018</span><span class="sxs-lookup"><span data-stu-id="bd7fe-193">January 31, 2018</span></span>

<span data-ttu-id="bd7fe-194">Version 2.0.26</span><span class="sxs-lookup"><span data-stu-id="bd7fe-194">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-195">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-195">Core</span></span>

* <span data-ttu-id="bd7fe-196">Stöd har lagts till för att hämta rådatatoken i MSI-kontexten</span><span class="sxs-lookup"><span data-stu-id="bd7fe-196">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="bd7fe-197">En sträng för avsökningsindikatorn vid slutföring av LRO på Windows cmd.exe har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-197">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="bd7fe-198">En varning som visas när du använder en konfigurerad standard som har ändrats till en post på INFO-nivå har lagts till.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-198">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="bd7fe-199">Använd `--verbose` för att se</span><span class="sxs-lookup"><span data-stu-id="bd7fe-199">Use `--verbose` to see</span></span>
* <span data-ttu-id="bd7fe-200">Lägga till en förloppsindikator för väntekommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-200">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-201">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-201">ACS</span></span>

* <span data-ttu-id="bd7fe-202">Argumentet `--disable-browser` har förtydligats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-202">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="bd7fe-203">Tabbifyllning för `--vm-size`-argument har förbättrats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-203">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-204">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-204">Appservice</span></span>

* <span data-ttu-id="bd7fe-205">Åtgärdade `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-205">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="bd7fe-206">Kontrollen `kind` har tagits bort för webbappar och funktioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-206">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="bd7fe-207">CDN</span><span class="sxs-lookup"><span data-stu-id="bd7fe-207">CDN</span></span>

* <span data-ttu-id="bd7fe-208">Problem med klient som saknades har åtgärdats med `cdn custom-domain create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-208">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="bd7fe-209">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-209">CosmosDB</span></span>

* <span data-ttu-id="bd7fe-210">Parameterbeskrivningen för redundansprinciper har korrigerats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-210">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="bd7fe-211">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="bd7fe-211">Interactive</span></span>

* <span data-ttu-id="bd7fe-212">Problem där kompletteringar för kommandoalternativ inte längre visades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-212">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-213">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-213">Network</span></span>

* <span data-ttu-id="bd7fe-214">Skydd för `--cert-password` till `application-gateway create` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-214">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="bd7fe-215">Problem med `application-gateway update` där `--sku` felaktigt applicerade ett standardvärde har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-215">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="bd7fe-216">Skydd för `--shared-key` till `--authorization-key` har lagts till i `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-216">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="bd7fe-217">Problem med klient som saknades har åtgärdats med `asg create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-217">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="bd7fe-218">Parametern `--file-name / -f` har lagts till för exporterade namn till `dns zone export`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-218">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="bd7fe-219">Följande problem med `dns zone export` har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-219">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="bd7fe-220">Problemet där långa TXT-poster exporterades felaktigt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-220">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="bd7fe-221">Problemet där citerade TXT-poster exporterades felaktigt utan citattecken med omvänt snedstreck framför har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-221">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="bd7fe-222">Problemet där vissa poster importerades två gånger med `dns zone import` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-222">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="bd7fe-223">Kommandona `vnet-gateway root-cert` och `vnet-gateway revoked-cert` har återställts</span><span class="sxs-lookup"><span data-stu-id="bd7fe-223">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-224">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-224">Profile</span></span>

* <span data-ttu-id="bd7fe-225">`get-access-token` har åtgärdats för att fungera i en virtuell dator med en identitet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-225">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-226">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-226">Resource</span></span>

* <span data-ttu-id="bd7fe-227">Bugg i `deployment [create|validate]` där en varning visades felaktigt när "type"-mallfältet innehöll värden i versaler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-227">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-228">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-228">Storage</span></span>

* <span data-ttu-id="bd7fe-229">Problem med att migrera Storage V1-konton till Storage V2 har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-229">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="bd7fe-230">Förloppsrapportering har lagts till för alla kommandon som används för att ladda upp eller ladda ned</span><span class="sxs-lookup"><span data-stu-id="bd7fe-230">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="bd7fe-231">Bugg som förhindrade arg-alternativet "-n" med `storage account check-name` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-231">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="bd7fe-232">En ögonblicksbildkolumn för tabellutdata har lagts till för `blob [list|show]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-232">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="bd7fe-233">Buggar med olika parametrar som var tvungna att tolkas som ints har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-233">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-234">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-234">VM</span></span>

* <span data-ttu-id="bd7fe-235">Kommandot `vm image accept-terms` har lagts till för att göra det möjligt att skapa virtuella datorer från avbildningar till ytterligare avgifter</span><span class="sxs-lookup"><span data-stu-id="bd7fe-235">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="bd7fe-236">`[vm|vmss create]` har åtgärdats så att kommandon kan köras genom proxy med osignerade certifikat</span><span class="sxs-lookup"><span data-stu-id="bd7fe-236">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="bd7fe-237">[FÖRHANDSVERSION] Stöd har lagts till för "låg" prioritet till VMSS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-237">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="bd7fe-238">Skydd för `--admin-password` till `[vm|vmss] create` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-238">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="bd7fe-239">17 januari 2018</span><span class="sxs-lookup"><span data-stu-id="bd7fe-239">January 17, 2018</span></span>

<span data-ttu-id="bd7fe-240">Version 2.0.25</span><span class="sxs-lookup"><span data-stu-id="bd7fe-240">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="bd7fe-241">ACR</span><span class="sxs-lookup"><span data-stu-id="bd7fe-241">ACR</span></span>

* <span data-ttu-id="bd7fe-242">ACR-inloggningsåterställning för fel med Windows-autentiseringsuppgifter har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-242">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="bd7fe-243">Registerloggar har aktiverats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-243">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-244">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-244">ACS</span></span>

* <span data-ttu-id="bd7fe-245">Kommandot `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-245">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="bd7fe-246">Krav för SPN-roll har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-246">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-247">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-247">Appservice</span></span>

* <span data-ttu-id="bd7fe-248">Bugg med `config ssl upload` där `hosting_environment_profile` var null har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-248">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="bd7fe-249">Stöd har lagts till för anpassade webbadresser för `browse`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-249">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="bd7fe-250">Platsstöd har åtgärdats för `log tail`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-250">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="bd7fe-251">Backup</span><span class="sxs-lookup"><span data-stu-id="bd7fe-251">Backup</span></span>

* <span data-ttu-id="bd7fe-252">Alternativet `--container-name` för `backup item list` har ändrats så att det är valfritt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-252">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="bd7fe-253">Alternativ för lagringskonton har lagts till i `backup restore restore-disks`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-253">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="bd7fe-254">Platsincheckning i `backup protection enable-for-vm` har åtgärdats till skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-254">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="bd7fe-255">Problem där kommandon misslyckades på grund av ett ogiltigt behållarnamn har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-255">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="bd7fe-256">`backup item list` har ändrats så att Hälsostatus ingår som standard</span><span class="sxs-lookup"><span data-stu-id="bd7fe-256">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="bd7fe-257">Batch</span><span class="sxs-lookup"><span data-stu-id="bd7fe-257">Batch</span></span>

* <span data-ttu-id="bd7fe-258">`batch login` har ändrats så att information om autentiseringsuppgifter returneras</span><span class="sxs-lookup"><span data-stu-id="bd7fe-258">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="bd7fe-259">Molnet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-259">Cloud</span></span>

* <span data-ttu-id="bd7fe-260">Slutpunkter krävs inte längre när du anger `--profile` i ett moln</span><span class="sxs-lookup"><span data-stu-id="bd7fe-260">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="bd7fe-261">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-261">Consumption</span></span>

* <span data-ttu-id="bd7fe-262">Nya kommandon för reservationer har lagts till: `consumption reservations summaries` och`consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-262">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="bd7fe-263">Event Grid</span><span class="sxs-lookup"><span data-stu-id="bd7fe-263">Event Grid</span></span>

* <span data-ttu-id="bd7fe-264">[VIKTIG ÄNDRING] Kommandona `az eventgrid topic event-subscription` har flyttats till `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-264">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="bd7fe-265">[VIKTIG ÄNDRING] Kommandona `az eventgrid resource event-subscription` har flyttats till `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-265">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="bd7fe-266">[VIKTIG ÄNDRING] Kommandot `eventgrid event-subscription show-endpoint-url` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-266">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="bd7fe-267">Använd `eventgrid event-subscription show --include-full-endpoint-url` istället</span><span class="sxs-lookup"><span data-stu-id="bd7fe-267">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="bd7fe-268">Kommandot `eventgrid topic update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-268">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="bd7fe-269">Kommandot `eventgrid event-subscription update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-269">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="bd7fe-270">Parametern `--ids` har lagts till för `eventgrid topic`-kommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-270">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="bd7fe-271">Stöd för tabbifyllning för avsnittsnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-271">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="bd7fe-272">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="bd7fe-272">Interactive</span></span>

* <span data-ttu-id="bd7fe-273">Ett problem där interaktivt läge inte fungerade med Python 2.x har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-273">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="bd7fe-274">Fel vid start har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-274">Fixed errors on startup</span></span>
* <span data-ttu-id="bd7fe-275">Problem där vissa kommandon inte kördes i interaktivt läge har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-275">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="bd7fe-276">IoT</span><span class="sxs-lookup"><span data-stu-id="bd7fe-276">IoT</span></span>

* <span data-ttu-id="bd7fe-277">Stöd för enhetsetableringstjänst har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-277">Added support for device provisioning service</span></span>
* <span data-ttu-id="bd7fe-278">Utfasningsmeddelanden i kommandon och kommandohjälp har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-278">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="bd7fe-279">IoT-kontroll för att informera användare om IoT-tillägget har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-279">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-280">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-280">Monitor</span></span>

* <span data-ttu-id="bd7fe-281">Stöd för flera diagnostikinställningar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-281">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="bd7fe-282">Parametern `--name` krävs nu för `az monitor diagnostic-settings create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-282">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="bd7fe-283">Kommandot `monitor diagnostic-settings categories` har lagts till för att hämta diagnostikinställningskategorin</span><span class="sxs-lookup"><span data-stu-id="bd7fe-283">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-284">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-284">Network</span></span>

* <span data-ttu-id="bd7fe-285">Ett problem som uppstod vid försök att ändra till eller från aktivt standby-läge med `vnet-gateway update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-285">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="bd7fe-286">Stöd för HTTP2 för `application-gateway [create|update]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-286">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-287">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-287">Profile</span></span>

* <span data-ttu-id="bd7fe-288">Stöd för inloggning med användartilldelade identiteter har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-288">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-289">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-289">Role</span></span>

* <span data-ttu-id="bd7fe-290">Argumentet `--assignee-object-id` till `role assignment create` för att kringgå diagramfråga har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-290">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="bd7fe-291">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="bd7fe-291">Service Fabric</span></span>

* <span data-ttu-id="bd7fe-292">Detaljerade fel till verifieringssvar när du skapar kluster har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-292">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="bd7fe-293">Problem med klient som saknades har åtgärdats med flera kommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-293">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-294">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-294">VM</span></span>

* <span data-ttu-id="bd7fe-295">[FÖRHANDSVERSION] Stöd mellan zoner för `vmss`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-295">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="bd7fe-296">[VIKTIG ÄNDRING] Standardinställningen för den enskilda zonen `vmss` har ändrats till "standard" för belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-296">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="bd7fe-297">[VIKTIG ÄNDRING] `externalIdentities` har ändrats till `userAssignedIdentities` för EMSI</span><span class="sxs-lookup"><span data-stu-id="bd7fe-297">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="bd7fe-298">[FÖRHANDSVERSION] Stöd har lagts till för växling mellan OS-diskar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-298">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="bd7fe-299">Stöd har lagts till för användning av VM-avbildningar från andra prenumerationer</span><span class="sxs-lookup"><span data-stu-id="bd7fe-299">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="bd7fe-300">Argumenten `--plan-name`, `--plan-product`, `--plan-promotion-code` och `--plan-publisher` har lagts till för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-300">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="bd7fe-301">Problem med `[vm|vmss] create` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-301">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="bd7fe-302">För hög resursanvändning som orsakades av `vm image list --all` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-302">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="bd7fe-303">19 december 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-303">December 19, 2017</span></span>

<span data-ttu-id="bd7fe-304">Version 2.0.23</span><span class="sxs-lookup"><span data-stu-id="bd7fe-304">Version 2.0.23</span></span>

* <span data-ttu-id="bd7fe-305">Stöd för inloggning med användartilldelade identiteter har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-305">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-306">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-306">Container</span></span>

* <span data-ttu-id="bd7fe-307">Åtgärdade felaktig ordning för parametrar för behållarloggar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-307">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-308">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-308">Network</span></span>

* <span data-ttu-id="bd7fe-309">Argumentet `--disable-bgp-route-propagation` har lagts till för `route-table [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-309">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="bd7fe-310">Argumentet `--ip-tags` har lagts till för `public-ip [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-310">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-311">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-311">Storage</span></span>

* <span data-ttu-id="bd7fe-312">Stöd har lagts till för lagring V2</span><span class="sxs-lookup"><span data-stu-id="bd7fe-312">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-313">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-313">VM</span></span>

* <span data-ttu-id="bd7fe-314">[FÖRHANDSVERSION] Ökad stöd för användartilldelade identiteter för virtuella datorer och VMSS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-314">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="bd7fe-315">5 december 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-315">December 5, 2017</span></span>

<span data-ttu-id="bd7fe-316">Version 2.0.22</span><span class="sxs-lookup"><span data-stu-id="bd7fe-316">Version 2.0.22</span></span>

* <span data-ttu-id="bd7fe-317">`az component` kommandon har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-317">Removed `az component` commands.</span></span> <span data-ttu-id="bd7fe-318">Använd `az extension` istället</span><span class="sxs-lookup"><span data-stu-id="bd7fe-318">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-319">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-319">Core</span></span>
* <span data-ttu-id="bd7fe-320">`AZURE_US_GOV_CLOUD` AAD-utfärdarslutpunkten har ändrats från login.microsoftonline.com till login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="bd7fe-320">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="bd7fe-321">Felet med att telemetri kontinuerligt skickades på nytt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-321">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-322">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-322">ACS</span></span>

* <span data-ttu-id="bd7fe-323">Kommandona `aks install-connector` och `aks remove-connector` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-323">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="bd7fe-324">Förbättrad felrapportering för `acs create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-324">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="bd7fe-325">Användning av `aks get-credentials -f` utan fullständig sökväg har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-325">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="bd7fe-326">Advisor</span><span class="sxs-lookup"><span data-stu-id="bd7fe-326">Advisor</span></span>

* <span data-ttu-id="bd7fe-327">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="bd7fe-327">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-328">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-328">Appservice</span></span>

* <span data-ttu-id="bd7fe-329">Skapande av certifikatnamn med `webapp config ssl upload` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-329">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="bd7fe-330">`webapp [list|show]` och `functionapp [list|show]` har åtgärdats för att visa rätt appar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-330">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="bd7fe-331">Standardvärde har lagts till för `WEBSITE_NODE_DEFAULT_VERSION`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-331">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="bd7fe-332">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-332">Consumption</span></span>

* <span data-ttu-id="bd7fe-333">Stöd för API-versionen 2017-11-30 har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-333">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-334">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-334">Container</span></span>

* <span data-ttu-id="bd7fe-335">Regression till standardportar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-335">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-336">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-336">Monitor</span></span>

* <span data-ttu-id="bd7fe-337">Flerdimensionellt stöd för måttkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-337">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-338">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-338">Resource</span></span>

* <span data-ttu-id="bd7fe-339">Argumentet `--include-response-body` har lagts till för `resource show`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-339">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-340">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-340">Role</span></span>

* <span data-ttu-id="bd7fe-341">Visning av standardtilldelningar för "klassiska" administratörer till `role assignment list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-341">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="bd7fe-342">Stöd har lagts till för `ad sp reset-credentials` för att lägga till autentiseringsuppgifter istället för att skriva över</span><span class="sxs-lookup"><span data-stu-id="bd7fe-342">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="bd7fe-343">Förbättrad felrapportering för `ad sp create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-343">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-344">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-344">SQL</span></span>

* <span data-ttu-id="bd7fe-345">Kommandona `sql db list-usages` och `sql db show-usage` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-345">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="bd7fe-346">Kommandona `sql server conn-policy show` och `sql server conn-policy update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-346">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-347">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-347">VM</span></span>

* <span data-ttu-id="bd7fe-348">Zoninformation har lagts till i `az vm list-skus`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-348">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="bd7fe-349">14 november 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-349">November 14, 2017</span></span>

<span data-ttu-id="bd7fe-350">Version 2.0.21</span><span class="sxs-lookup"><span data-stu-id="bd7fe-350">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="bd7fe-351">ACR</span><span class="sxs-lookup"><span data-stu-id="bd7fe-351">ACR</span></span>

* <span data-ttu-id="bd7fe-352">Stöd för att skapa webhooks i replikeringsregioner har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-352">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="bd7fe-353">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-353">ACS</span></span>

* <span data-ttu-id="bd7fe-354">Alla ”agent” till ”nod” har ändrats i AKS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-354">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="bd7fe-355">Föråldrat `--orchestrator-release`-alternativ för `acs create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-355">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="bd7fe-356">Standardstorleken för virtuella datorer för AKS till `Standard_D1_v2` har ändrats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-356">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="bd7fe-357">Åtgärdade `az aks browse` i Windows</span><span class="sxs-lookup"><span data-stu-id="bd7fe-357">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="bd7fe-358">Åtgärdade `az aks get-credentials` i Windows</span><span class="sxs-lookup"><span data-stu-id="bd7fe-358">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-359">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-359">Appservice</span></span>

* <span data-ttu-id="bd7fe-360">Distributionskälla `config-zip` för webappar och funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-360">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="bd7fe-361">`--docker-container-logging`-alternativ till `az webapp log config` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-361">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="bd7fe-362">Alternativet `storage` från parametern `--web-server-logging` av `az webapp log config` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-362">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="bd7fe-363">Förbättrade felmeddelanden för `deployment user set`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-363">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="bd7fe-364">Stöd för att skapa Linux-funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-364">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="bd7fe-365">Åtgärdade `list-locations`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-365">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="bd7fe-366">Batch</span><span class="sxs-lookup"><span data-stu-id="bd7fe-366">Batch</span></span>

* <span data-ttu-id="bd7fe-367">En bugg har åtgärdats i kommandot för skapande av pool när ett resurs-ID användes med flaggan `--image`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-367">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="bd7fe-368">Batchai</span><span class="sxs-lookup"><span data-stu-id="bd7fe-368">Batchai</span></span>

* <span data-ttu-id="bd7fe-369">Ett kort alternativ har lagts till, `-s`, för `--vm-size` VM-storlek i kommandot `file-server create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-369">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="bd7fe-370">Kontonamn och nyckelargument har lagts till för `cluster create`-parametrar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-370">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="bd7fe-371">Dokumentation har skapats för `job list-files` och `job stream-file`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-371">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="bd7fe-372">Ett kort alternativ har lagts till, `-r`, för `--cluster-name` när klusternamn anges med kommandot `job create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-372">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="bd7fe-373">Molnet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-373">Cloud</span></span>

* <span data-ttu-id="bd7fe-374">`cloud [register|update]` har ändrats för att förhindra att moln registreras som saknar slutpunkter som krävs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-374">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-375">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-375">Container</span></span>

* <span data-ttu-id="bd7fe-376">Stöd för att öppna flera portar har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-376">Added support to open multiple ports</span></span>
* <span data-ttu-id="bd7fe-377">Princip för omstart av behållargrupp har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-377">Added container group restart policy</span></span>
* <span data-ttu-id="bd7fe-378">Stöd för att montera Azure-filresurs som volym har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-378">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="bd7fe-379">Hjälpdokument har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-379">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="bd7fe-380">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bd7fe-380">Data Lake Analytics</span></span>

* <span data-ttu-id="bd7fe-381">`[job|account] list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="bd7fe-381">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="bd7fe-382">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd7fe-382">Data Lake Store</span></span>

* <span data-ttu-id="bd7fe-383">`account list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="bd7fe-383">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="bd7fe-384">Anknytning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-384">Extension</span></span>

* <span data-ttu-id="bd7fe-385">`extension list-available` har lagts till för att tillåta lista över officiella Microsoft-tillägg</span><span class="sxs-lookup"><span data-stu-id="bd7fe-385">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="bd7fe-386">`--name` har lagts till för `extension [add|update]` för att tillåta installation av tillägg via namn</span><span class="sxs-lookup"><span data-stu-id="bd7fe-386">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="bd7fe-387">IoT</span><span class="sxs-lookup"><span data-stu-id="bd7fe-387">IoT</span></span>

* <span data-ttu-id="bd7fe-388">Stöd för certifikatutfärdare (CA) och certifikatkedjor har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-388">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-389">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-389">Monitor</span></span>

* <span data-ttu-id="bd7fe-390">`activity-log alert`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-390">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-391">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-391">Network</span></span>

* <span data-ttu-id="bd7fe-392">Stöd för CAA DNS-poster har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-392">Added support for CAA DNS records</span></span>
* <span data-ttu-id="bd7fe-393">Problem där slutpunkter inte kunde uppdateras med `traffic-manager profile update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-393">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="bd7fe-394">Problem där `vnet update --dns-servers` inte fungerade beroende på hur VNET skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-394">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="bd7fe-395">Problem där relativa DNS-namn hade importerats felaktigt av `dns zone import` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-395">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="bd7fe-396">Reservationer</span><span class="sxs-lookup"><span data-stu-id="bd7fe-396">Reservations</span></span>

* <span data-ttu-id="bd7fe-397">Inledande förhandsversion</span><span class="sxs-lookup"><span data-stu-id="bd7fe-397">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-398">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-398">Resource</span></span>

* <span data-ttu-id="bd7fe-399">Stöd för resurs-ID till parametern `--resource` och lås på resursnivå har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-399">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-400">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-400">SQL</span></span>

* <span data-ttu-id="bd7fe-401">Parametern `--ignore-missing-vnet-service-endpoint` har lagts till i `sql server vnet-rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-401">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-402">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-402">Storage</span></span>

* <span data-ttu-id="bd7fe-403">`storage account create` har ändrats för att använda SKU `Standard_RAGRS` som standard</span><span class="sxs-lookup"><span data-stu-id="bd7fe-403">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="bd7fe-404">Buggar när fil-/blob-namn som innehåller icke-ASCII-tecken hanteras har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-404">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="bd7fe-405">Bugg som förhindrade användning av `--source-uri` med `storage [blob|file] copy start-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-405">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="bd7fe-406">Kommandon för blob och borttagning av flera objekt med `storage [blob|file] delete-batch` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-406">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="bd7fe-407">Problem vid aktivering av mått med `storage metrics update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-407">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="bd7fe-408">Problem med filer över 200 GB vid användning av `storage blob upload-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-408">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="bd7fe-409">Problem där `--bypass` och `--default-action` ignorerades av `storage account [create|update]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-409">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-410">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-410">VM</span></span>

* <span data-ttu-id="bd7fe-411">En bugg med `vmss create` som förhindrade användning med storleksnivån `Basic` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-411">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="bd7fe-412">`--plan` argument till `[vm|vmss] create` för anpassade avbildningar med faktureringsinformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-412">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="bd7fe-413">Kommandona `vm secret `[add|remove|list] har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-413">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="bd7fe-414">`vm format-secret` har bytt namn till `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-414">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="bd7fe-415">Argumentet `--encrypt format` har lagts till för `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-415">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="bd7fe-416">24 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-416">October 24, 2017</span></span>

<span data-ttu-id="bd7fe-417">Version 2.0.20</span><span class="sxs-lookup"><span data-stu-id="bd7fe-417">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-418">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-418">Core</span></span>

* <span data-ttu-id="bd7fe-419">`2017-03-09-profile` har uppdaterats för att använda `MGMT_STORAGE`, API-version `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-419">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="bd7fe-420">ACR</span><span class="sxs-lookup"><span data-stu-id="bd7fe-420">ACR</span></span>

* <span data-ttu-id="bd7fe-421">Resurshanteringen har uppdaterats för att peka på API-version `2017-10-01`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-421">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="bd7fe-422">SKU:n för BYOS ("bring your own storage") har ändrats till klassisk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-422">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="bd7fe-423">Register-SKU:erna har bytt namn till Basic, Standard och Premium</span><span class="sxs-lookup"><span data-stu-id="bd7fe-423">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-424">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-424">ACS</span></span>

* <span data-ttu-id="bd7fe-425">[FÖRHANDSVERSION] `az aks`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-425">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="bd7fe-426">Kubernetes `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-426">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-427">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-427">Appservice</span></span>

* <span data-ttu-id="bd7fe-428">Problem med att nedladdade `webapp`-loggar kunde vara ogiltiga har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-428">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="bd7fe-429">Komponent</span><span class="sxs-lookup"><span data-stu-id="bd7fe-429">Component</span></span>

* <span data-ttu-id="bd7fe-430">Ett tydligare utfasningsmeddelande har lagts till för alla installationsprogram och bekräftelsefrågor</span><span class="sxs-lookup"><span data-stu-id="bd7fe-430">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-431">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-431">Monitor</span></span>

* <span data-ttu-id="bd7fe-432">`action-group`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-432">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-433">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-433">Resource</span></span>

* <span data-ttu-id="bd7fe-434">Inkompatibilitet med den senaste versionen av msrest-beroende i `group export` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-434">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="bd7fe-435">`policy assignment create` har åtgärdats så att det fungerar med inbyggda principdefinitioner och principuppsättningsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-435">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-436">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-436">VM</span></span>

* <span data-ttu-id="bd7fe-437">Argumentet `--accelerated-networking` har lagts till för `vmss create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-437">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="bd7fe-438">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-438">October 9, 2017</span></span>

<span data-ttu-id="bd7fe-439">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="bd7fe-439">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-440">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-440">Core</span></span>

* <span data-ttu-id="bd7fe-441">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-441">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-442">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-442">Appservice</span></span>

* <span data-ttu-id="bd7fe-443">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-443">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="bd7fe-444">Batch</span><span class="sxs-lookup"><span data-stu-id="bd7fe-444">Batch</span></span>

* <span data-ttu-id="bd7fe-445">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="bd7fe-445">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="bd7fe-446">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="bd7fe-446">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="bd7fe-447">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-447">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="bd7fe-448">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-448">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="bd7fe-449">Batchai</span><span class="sxs-lookup"><span data-stu-id="bd7fe-449">Batchai</span></span>

* <span data-ttu-id="bd7fe-450">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-450">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd7fe-451">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7fe-451">Keyvault</span></span>

* <span data-ttu-id="bd7fe-452">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-452">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="bd7fe-453">(#4448)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-453">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="bd7fe-454">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-454">Network</span></span>

* <span data-ttu-id="bd7fe-455">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="bd7fe-455">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="bd7fe-456">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="bd7fe-456">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-457">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-457">Resource</span></span>

* <span data-ttu-id="bd7fe-458">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-458">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="bd7fe-459">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="bd7fe-459">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="bd7fe-460">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="bd7fe-460">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="bd7fe-461">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="bd7fe-461">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-462">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-462">Sql</span></span>

* <span data-ttu-id="bd7fe-463">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="bd7fe-463">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="bd7fe-464">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="bd7fe-464">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="bd7fe-465">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-465">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-466">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-466">Storage</span></span>

* <span data-ttu-id="bd7fe-467">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-467">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-468">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-468">Vm</span></span>

* <span data-ttu-id="bd7fe-469">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="bd7fe-469">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="bd7fe-470">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-470">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="bd7fe-471">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-471">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="bd7fe-472">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-472">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="bd7fe-473">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-473">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="bd7fe-474">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-474">September 22, 2017</span></span>

<span data-ttu-id="bd7fe-475">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="bd7fe-475">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-476">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-476">Resource</span></span>

* <span data-ttu-id="bd7fe-477">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-477">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="bd7fe-478">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-478">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="bd7fe-479">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-479">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="bd7fe-480">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-480">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-481">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-481">Network</span></span>

* <span data-ttu-id="bd7fe-482">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-482">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="bd7fe-483">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-483">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="bd7fe-484">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-484">Added `asg` application security group commands</span></span>
* <span data-ttu-id="bd7fe-485">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-485">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="bd7fe-486">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-486">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="bd7fe-487">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-487">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="bd7fe-488">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-488">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-489">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-489">Storage</span></span>

* <span data-ttu-id="bd7fe-490">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="bd7fe-490">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="bd7fe-491">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="bd7fe-491">Eventgrid</span></span>

* <span data-ttu-id="bd7fe-492">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="bd7fe-492">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-493">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-493">SQL</span></span>

* <span data-ttu-id="bd7fe-494">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-494">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="bd7fe-495">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-495">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="bd7fe-496">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-496">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd7fe-497">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7fe-497">Keyvault</span></span>

* <span data-ttu-id="bd7fe-498">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="bd7fe-498">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-499">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-499">VM</span></span>

* <span data-ttu-id="bd7fe-500">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-500">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="bd7fe-501">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="bd7fe-501">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="bd7fe-502">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-502">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="bd7fe-503">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-503">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="bd7fe-504">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-504">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="bd7fe-505">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-505">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-506">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-506">ACS</span></span>

* <span data-ttu-id="bd7fe-507">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="bd7fe-507">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-508">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-508">Appservice</span></span>

* <span data-ttu-id="bd7fe-509">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-509">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="bd7fe-510">Backup</span><span class="sxs-lookup"><span data-stu-id="bd7fe-510">Backup</span></span>

* <span data-ttu-id="bd7fe-511">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="bd7fe-511">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="bd7fe-512">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-512">September 11, 2017</span></span>

<span data-ttu-id="bd7fe-513">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="bd7fe-513">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="bd7fe-514">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-514">Core</span></span>

* <span data-ttu-id="bd7fe-515">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="bd7fe-515">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="bd7fe-516">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="bd7fe-516">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-517">Acs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-517">Acs</span></span>

* <span data-ttu-id="bd7fe-518">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-518">Added `acs list-locations` command</span></span>
* <span data-ttu-id="bd7fe-519">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="bd7fe-519">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-520">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-520">Appservice</span></span>

* <span data-ttu-id="bd7fe-521">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-521">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="bd7fe-522">CDN</span><span class="sxs-lookup"><span data-stu-id="bd7fe-522">CDN</span></span>

* <span data-ttu-id="bd7fe-523">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-523">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="bd7fe-524">Anknytning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-524">Extension</span></span>

* <span data-ttu-id="bd7fe-525">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-525">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd7fe-526">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7fe-526">Keyvault</span></span>

* <span data-ttu-id="bd7fe-527">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-527">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-528">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-528">Network</span></span>

* <span data-ttu-id="bd7fe-529">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-529">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="bd7fe-530">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-530">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="bd7fe-531">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-531">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="bd7fe-532">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-532">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="bd7fe-533">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-533">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-534">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-534">Resource</span></span>

* <span data-ttu-id="bd7fe-535">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-535">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="bd7fe-536">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-536">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="bd7fe-537">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="bd7fe-537">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="bd7fe-538">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-538">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-539">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-539">SQL</span></span>

* <span data-ttu-id="bd7fe-540">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-540">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-541">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-541">VM</span></span>

* <span data-ttu-id="bd7fe-542">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="bd7fe-542">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="bd7fe-543">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="bd7fe-543">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="bd7fe-544">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-544">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="bd7fe-545">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-545">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="bd7fe-546">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="bd7fe-546">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="bd7fe-547">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-547">August 31, 2017</span></span>

<span data-ttu-id="bd7fe-548">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="bd7fe-548">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd7fe-549">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7fe-549">Keyvault</span></span>

* <span data-ttu-id="bd7fe-550">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-550">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="bd7fe-551">Sf</span><span class="sxs-lookup"><span data-stu-id="bd7fe-551">Sf</span></span>

* <span data-ttu-id="bd7fe-552">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-552">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-553">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-553">Storage</span></span>

* <span data-ttu-id="bd7fe-554">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-554">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="bd7fe-555">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="bd7fe-555">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="bd7fe-556">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-556">August 28, 2017</span></span>

<span data-ttu-id="bd7fe-557">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="bd7fe-557">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="bd7fe-558">CLI</span><span class="sxs-lookup"><span data-stu-id="bd7fe-558">CLI</span></span>

* <span data-ttu-id="bd7fe-559">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-559">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-560">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-560">ACS</span></span>

* <span data-ttu-id="bd7fe-561">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-561">Corrected preview regions.</span></span>
* <span data-ttu-id="bd7fe-562">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-562">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="bd7fe-563">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-563">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-564">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-564">Appservice</span></span>

* <span data-ttu-id="bd7fe-565">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-565">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="bd7fe-566">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-566">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="bd7fe-567">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-567">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="bd7fe-568">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="bd7fe-568">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="bd7fe-569">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-569">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="bd7fe-570">IoT</span><span class="sxs-lookup"><span data-stu-id="bd7fe-570">IoT</span></span>

* <span data-ttu-id="bd7fe-571">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="bd7fe-571">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-572">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-572">Network</span></span>

* <span data-ttu-id="bd7fe-573">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-573">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="bd7fe-574">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-574">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="bd7fe-575">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-575">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="bd7fe-576">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-576">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="bd7fe-577">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-577">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-578">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-578">Profile</span></span>

* <span data-ttu-id="bd7fe-579">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-579">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="bd7fe-580">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="bd7fe-580">Service Fabric</span></span>

* <span data-ttu-id="bd7fe-581">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="bd7fe-581">Preview release</span></span>
* <span data-ttu-id="bd7fe-582">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="bd7fe-582">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="bd7fe-583">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-583">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="bd7fe-584">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-584">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-585">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-585">Storage</span></span>

* <span data-ttu-id="bd7fe-586">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="bd7fe-586">Enabled setting blob tier</span></span>
* <span data-ttu-id="bd7fe-587">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="bd7fe-587">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="bd7fe-588">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-588">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="bd7fe-589">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-589">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="bd7fe-590">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-590">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="bd7fe-591">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="bd7fe-591">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-592">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-592">VM</span></span>

* <span data-ttu-id="bd7fe-593">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-593">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="bd7fe-594">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-594">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="bd7fe-595">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-595">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="bd7fe-596">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-596">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="bd7fe-597">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-597">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="bd7fe-598">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-598">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="bd7fe-599">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-599">August 15, 2017</span></span>

<span data-ttu-id="bd7fe-600">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="bd7fe-600">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-601">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-601">ACS</span></span>

* <span data-ttu-id="bd7fe-602">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-602">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-603">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-603">Appservice</span></span>

* <span data-ttu-id="bd7fe-604">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-604">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="bd7fe-605">Event Grid</span><span class="sxs-lookup"><span data-stu-id="bd7fe-605">Event Grid</span></span>

* <span data-ttu-id="bd7fe-606">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-606">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="bd7fe-607">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-607">August 11, 2017</span></span>

<span data-ttu-id="bd7fe-608">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="bd7fe-608">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-609">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-609">ACS</span></span>

* <span data-ttu-id="bd7fe-610">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-610">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="bd7fe-611">Batch</span><span class="sxs-lookup"><span data-stu-id="bd7fe-611">Batch</span></span>

* <span data-ttu-id="bd7fe-612">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="bd7fe-612">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="bd7fe-613">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="bd7fe-613">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="bd7fe-614">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-614">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="bd7fe-615">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="bd7fe-615">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="bd7fe-616">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="bd7fe-616">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="bd7fe-617">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="bd7fe-617">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="bd7fe-618">Komponent</span><span class="sxs-lookup"><span data-stu-id="bd7fe-618">Component</span></span>

* <span data-ttu-id="bd7fe-619">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-619">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="bd7fe-620">Behållare</span><span class="sxs-lookup"><span data-stu-id="bd7fe-620">Container</span></span>

* <span data-ttu-id="bd7fe-621">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="bd7fe-621">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="bd7fe-622">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd7fe-622">Data Lake Store</span></span>

* <span data-ttu-id="bd7fe-623">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-623">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="bd7fe-624">Event Grid</span><span class="sxs-lookup"><span data-stu-id="bd7fe-624">Event Grid</span></span>

* <span data-ttu-id="bd7fe-625">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="bd7fe-625">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-626">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-626">Network</span></span>

* <span data-ttu-id="bd7fe-627">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="bd7fe-627">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="bd7fe-628">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="bd7fe-628">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="bd7fe-629">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-629">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="bd7fe-630">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-630">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-631">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-631">Profile</span></span>

* <span data-ttu-id="bd7fe-632">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="bd7fe-632">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-633">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-633">Storage</span></span>

* <span data-ttu-id="bd7fe-634">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="bd7fe-634">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-635">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-635">VM</span></span>

* <span data-ttu-id="bd7fe-636">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-636">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="bd7fe-637">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-637">Exposed `list-skus` command</span></span>
* <span data-ttu-id="bd7fe-638">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-638">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="bd7fe-639">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="bd7fe-639">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="bd7fe-640">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-640">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="bd7fe-641">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-641">July 28, 2017</span></span>

<span data-ttu-id="bd7fe-642">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="bd7fe-642">Version 2.0.12</span></span>

* <span data-ttu-id="bd7fe-643">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-643">Added container commands</span></span>
* <span data-ttu-id="bd7fe-644">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-644">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="bd7fe-645">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-645">Core</span></span>

* <span data-ttu-id="bd7fe-646">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="bd7fe-646">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="bd7fe-647">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-647">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="bd7fe-648">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="bd7fe-648">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="bd7fe-649">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-649">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="bd7fe-650">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-650">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="bd7fe-651">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-651">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="bd7fe-652">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-652">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="bd7fe-653">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-653">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="bd7fe-654">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-654">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="bd7fe-655">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-655">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="bd7fe-656">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-656">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="bd7fe-657">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-657">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="bd7fe-658">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="bd7fe-658">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="bd7fe-659">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="bd7fe-659">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="bd7fe-660">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="bd7fe-660">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="bd7fe-661">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-661">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="bd7fe-662">ACR</span><span class="sxs-lookup"><span data-stu-id="bd7fe-662">ACR</span></span>

* <span data-ttu-id="bd7fe-663">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="bd7fe-663">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="bd7fe-664">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="bd7fe-664">Support SKU update for managed registries</span></span>
* <span data-ttu-id="bd7fe-665">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-665">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="bd7fe-666">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="bd7fe-666">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="bd7fe-667">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="bd7fe-667">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="bd7fe-668">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-668">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-669">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-669">ACS</span></span>

* <span data-ttu-id="bd7fe-670">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="bd7fe-670">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-671">App Service</span><span class="sxs-lookup"><span data-stu-id="bd7fe-671">Appservice</span></span>

* <span data-ttu-id="bd7fe-672">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="bd7fe-672">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="bd7fe-673">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="bd7fe-673">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="bd7fe-674">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-674">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="bd7fe-675">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-675">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="bd7fe-676">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-676">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="bd7fe-677">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-677">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="bd7fe-678">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-678">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="bd7fe-679">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-679">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="bd7fe-680">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-680">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="bd7fe-681">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="bd7fe-681">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="bd7fe-682">Batch</span><span class="sxs-lookup"><span data-stu-id="bd7fe-682">Batch</span></span>

* <span data-ttu-id="bd7fe-683">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="bd7fe-683">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="bd7fe-684">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-684">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="bd7fe-685">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-685">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="bd7fe-686">CDN</span><span class="sxs-lookup"><span data-stu-id="bd7fe-686">CDN</span></span>

* <span data-ttu-id="bd7fe-687">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-687">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="bd7fe-688">Molnet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-688">Cloud</span></span>

* <span data-ttu-id="bd7fe-689">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="bd7fe-689">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="bd7fe-690">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="bd7fe-690">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="bd7fe-691">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="bd7fe-691">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="bd7fe-692">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-692">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="bd7fe-693">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-693">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="bd7fe-694">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-694">CosmosDB</span></span>

* <span data-ttu-id="bd7fe-695">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="bd7fe-695">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="bd7fe-696">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-696">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="bd7fe-697">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bd7fe-697">Data Lake Analytics</span></span>

* <span data-ttu-id="bd7fe-698">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-698">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="bd7fe-699">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-699">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="bd7fe-700">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-700">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="bd7fe-701">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd7fe-701">Data Lake Store</span></span>

* <span data-ttu-id="bd7fe-702">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-702">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="bd7fe-703">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="bd7fe-703">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="bd7fe-704">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-704">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="bd7fe-705">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="bd7fe-705">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="bd7fe-706">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="bd7fe-706">Interactive</span></span>

* <span data-ttu-id="bd7fe-707">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-707">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="bd7fe-708">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-708">Increased test coverage</span></span>
* <span data-ttu-id="bd7fe-709">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="bd7fe-709">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="bd7fe-710">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-710">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="bd7fe-711">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-711">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="bd7fe-712">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-712">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="bd7fe-713">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-713">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="bd7fe-714">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-714">Added `--progress` flag</span></span>
* <span data-ttu-id="bd7fe-715">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="bd7fe-715">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="bd7fe-716">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-716">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="bd7fe-717">IoT</span><span class="sxs-lookup"><span data-stu-id="bd7fe-717">IoT</span></span>

* <span data-ttu-id="bd7fe-718">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-718">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="bd7fe-719">(#3934)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-719">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="bd7fe-720">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="bd7fe-720">Key vault</span></span>

* <span data-ttu-id="bd7fe-721">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-721">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="bd7fe-722">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-722">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="bd7fe-723">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-723">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="bd7fe-724">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-724">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="bd7fe-725">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-725">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="bd7fe-726">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-726">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="bd7fe-727">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-727">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="bd7fe-728">(#3307)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-728">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="bd7fe-729">Labb</span><span class="sxs-lookup"><span data-stu-id="bd7fe-729">Lab</span></span>

* <span data-ttu-id="bd7fe-730">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-730">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="bd7fe-731">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-731">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-732">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-732">Monitor</span></span>

* <span data-ttu-id="bd7fe-733">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-733">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="bd7fe-734">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-734">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="bd7fe-735">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-735">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="bd7fe-736">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-736">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="bd7fe-737">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-737">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="bd7fe-738">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-738">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="bd7fe-739">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="bd7fe-739">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="bd7fe-740">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="bd7fe-740">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="bd7fe-741">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="bd7fe-741">`location` no longer required</span></span>
  * <span data-ttu-id="bd7fe-742">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="bd7fe-742">Add name and ID support for target</span></span>
  * <span data-ttu-id="bd7fe-743">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-743">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="bd7fe-744">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="bd7fe-744">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="bd7fe-745">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="bd7fe-745">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="bd7fe-746">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-746">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="bd7fe-747">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="bd7fe-747">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="bd7fe-748">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-748">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-749">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-749">Network</span></span>

* <span data-ttu-id="bd7fe-750">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-750">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="bd7fe-751">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-751">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="bd7fe-752">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="bd7fe-752">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="bd7fe-753">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-753">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="bd7fe-754">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-754">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="bd7fe-755">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-755">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="bd7fe-756">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-756">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="bd7fe-757">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-757">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="bd7fe-758">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-758">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="bd7fe-759">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-759">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="bd7fe-760">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-760">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="bd7fe-761">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-761">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="bd7fe-762">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-762">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="bd7fe-763">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-763">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="bd7fe-764">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-764">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="bd7fe-765">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-765">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="bd7fe-766">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-766">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="bd7fe-767">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-767">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="bd7fe-768">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-768">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="bd7fe-769">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-769">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="bd7fe-770">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-770">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="bd7fe-771">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="bd7fe-771">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="bd7fe-772">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-772">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="bd7fe-773">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="bd7fe-773">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="bd7fe-774">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="bd7fe-774">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="bd7fe-775">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="bd7fe-775">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="bd7fe-776">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="bd7fe-776">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-777">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-777">Profile</span></span>

* <span data-ttu-id="bd7fe-778">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-778">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="bd7fe-779">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="bd7fe-779">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="bd7fe-780">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="bd7fe-780">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="bd7fe-781">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="bd7fe-781">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="bd7fe-782">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="bd7fe-782">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="bd7fe-783">RDBMS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-783">RDBMS</span></span>

* <span data-ttu-id="bd7fe-784">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-784">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="bd7fe-785">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-785">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="bd7fe-786">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-786">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="bd7fe-787">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-787">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-788">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-788">Resource</span></span>

* <span data-ttu-id="bd7fe-789">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-789">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="bd7fe-790">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="bd7fe-790">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="bd7fe-791">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-791">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="bd7fe-792">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-792">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="bd7fe-793">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-793">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="bd7fe-794">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-794">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="bd7fe-795">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-795">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="bd7fe-796">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="bd7fe-796">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-797">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-797">Role</span></span>

* <span data-ttu-id="bd7fe-798">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-798">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="bd7fe-799">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-799">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="bd7fe-800">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="bd7fe-800">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="bd7fe-801">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="bd7fe-801">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="bd7fe-802">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-802">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="bd7fe-803">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="bd7fe-803">Service Fabric</span></span>
* <span data-ttu-id="bd7fe-804">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-804">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="bd7fe-805">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-805">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="bd7fe-806">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-806">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-807">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-807">SQL</span></span>

* <span data-ttu-id="bd7fe-808">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="bd7fe-808">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="bd7fe-809">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="bd7fe-809">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="bd7fe-810">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="bd7fe-810">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-811">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-811">Storage</span></span>

* <span data-ttu-id="bd7fe-812">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-812">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="bd7fe-813">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-813">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="bd7fe-814">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-814">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="bd7fe-815">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-815">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="bd7fe-816">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-816">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="bd7fe-817">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-817">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-818">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-818">VM</span></span>

* <span data-ttu-id="bd7fe-819">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="bd7fe-819">Support configuring nsg</span></span>
* <span data-ttu-id="bd7fe-820">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-820">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="bd7fe-821">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="bd7fe-821">Support managed service identities</span></span>
* <span data-ttu-id="bd7fe-822">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-822">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="bd7fe-823">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="bd7fe-823">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="bd7fe-824">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-824">May 10, 2017</span></span>

<span data-ttu-id="bd7fe-825">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="bd7fe-825">Version 2.0.6</span></span>

* <span data-ttu-id="bd7fe-826">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="bd7fe-826">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="bd7fe-827">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-827">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="bd7fe-828">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-828">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="bd7fe-829">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-829">Include Cognitive Services module.</span></span>
* <span data-ttu-id="bd7fe-830">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-830">Include Service Fabric module.</span></span>
* <span data-ttu-id="bd7fe-831">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="bd7fe-831">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="bd7fe-832">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-832">Add support for CDN commands.</span></span>
* <span data-ttu-id="bd7fe-833">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-833">Remove Container module.</span></span>
* <span data-ttu-id="bd7fe-834">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-834">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="bd7fe-835">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-835">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="bd7fe-836">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-836">Core</span></span>

* <span data-ttu-id="bd7fe-837">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-837">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="bd7fe-838">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-838">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="bd7fe-839">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-839">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="bd7fe-840">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-840">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="bd7fe-841">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-841">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="bd7fe-842">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-842">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="bd7fe-843">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-843">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="bd7fe-844">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-844">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="bd7fe-845">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-845">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="bd7fe-846">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="bd7fe-846">core: Improved performance</span></span>
* <span data-ttu-id="bd7fe-847">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="bd7fe-847">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="bd7fe-848">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="bd7fe-848">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-849">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-849">ACS</span></span>

* <span data-ttu-id="bd7fe-850">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-850">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="bd7fe-851">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="bd7fe-851">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="bd7fe-852">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-852">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="bd7fe-853">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-853">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-854">AppService</span><span class="sxs-lookup"><span data-stu-id="bd7fe-854">AppService</span></span>

* <span data-ttu-id="bd7fe-855">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-855">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="bd7fe-856">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="bd7fe-856">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="bd7fe-857">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-857">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="bd7fe-858">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="bd7fe-858">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="bd7fe-859">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="bd7fe-859">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="bd7fe-860">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-860">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="bd7fe-861">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="bd7fe-861">support slot swap with preview</span></span>
* <span data-ttu-id="bd7fe-862">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-862">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="bd7fe-863">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-863">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="bd7fe-864">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-864">CosmosDB</span></span>

* <span data-ttu-id="bd7fe-865">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-865">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="bd7fe-866">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="bd7fe-866">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="bd7fe-867">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="bd7fe-867">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="bd7fe-868">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="bd7fe-868">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="bd7fe-869">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bd7fe-869">Data Lake Analytics</span></span>

* <span data-ttu-id="bd7fe-870">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-870">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="bd7fe-871">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-871">Add support for new catalog item type: package.</span></span> <span data-ttu-id="bd7fe-872">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-872">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="bd7fe-873">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="bd7fe-873">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="bd7fe-874">Tabell</span><span class="sxs-lookup"><span data-stu-id="bd7fe-874">Table</span></span>
  * <span data-ttu-id="bd7fe-875">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="bd7fe-875">Table valued function</span></span>
  * <span data-ttu-id="bd7fe-876">Visa</span><span class="sxs-lookup"><span data-stu-id="bd7fe-876">View</span></span>
  * <span data-ttu-id="bd7fe-877">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-877">Table Statistics.</span></span> <span data-ttu-id="bd7fe-878">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-878">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="bd7fe-879">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bd7fe-879">Data Lake Store</span></span>

* <span data-ttu-id="bd7fe-880">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-880">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="bd7fe-881">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-881">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="bd7fe-882">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-882">missed help for access show.</span></span> <span data-ttu-id="bd7fe-883">läggs till.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-883">adding it.</span></span> <span data-ttu-id="bd7fe-884">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-884">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="bd7fe-885">Hitta</span><span class="sxs-lookup"><span data-stu-id="bd7fe-885">Find</span></span>

* <span data-ttu-id="bd7fe-886">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="bd7fe-886">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="bd7fe-887">KeyVault</span><span class="sxs-lookup"><span data-stu-id="bd7fe-887">KeyVault</span></span>

* <span data-ttu-id="bd7fe-888">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="bd7fe-888">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="bd7fe-889">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-889">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="bd7fe-890">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="bd7fe-890">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="bd7fe-891">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-891">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="bd7fe-892">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-892">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="bd7fe-893">Labb</span><span class="sxs-lookup"><span data-stu-id="bd7fe-893">Lab</span></span>

* <span data-ttu-id="bd7fe-894">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-894">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="bd7fe-895">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-895">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="bd7fe-896">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-896">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="bd7fe-897">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-897">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="bd7fe-898">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-898">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="bd7fe-899">Övervaka</span><span class="sxs-lookup"><span data-stu-id="bd7fe-899">Monitor</span></span>

* <span data-ttu-id="bd7fe-900">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-900">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="bd7fe-901">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-901">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="bd7fe-902">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-902">Network</span></span>

* <span data-ttu-id="bd7fe-903">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-903">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="bd7fe-904">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-904">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="bd7fe-905">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-905">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="bd7fe-906">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-906">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="bd7fe-907">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-907">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="bd7fe-908">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-908">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="bd7fe-909">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-909">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="bd7fe-910">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-910">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="bd7fe-911">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-911">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="bd7fe-912">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="bd7fe-912">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="bd7fe-913">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-913">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="bd7fe-914">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="bd7fe-914">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="bd7fe-915">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-915">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="bd7fe-916">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-916">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="bd7fe-917">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-917">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="bd7fe-918">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-918">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="bd7fe-919">Profil</span><span class="sxs-lookup"><span data-stu-id="bd7fe-919">Profile</span></span>

* <span data-ttu-id="bd7fe-920">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-920">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="bd7fe-921">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-921">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="bd7fe-922">Redis</span><span class="sxs-lookup"><span data-stu-id="bd7fe-922">Redis</span></span>

* <span data-ttu-id="bd7fe-923">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="bd7fe-923">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="bd7fe-924">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-924">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="bd7fe-925">Resurs</span><span class="sxs-lookup"><span data-stu-id="bd7fe-925">Resource</span></span>

* <span data-ttu-id="bd7fe-926">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-926">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="bd7fe-927">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-927">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="bd7fe-928">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-928">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="bd7fe-929">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-929">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="bd7fe-930">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-930">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="bd7fe-931">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-931">Add docs for az lock update.</span></span> <span data-ttu-id="bd7fe-932">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-932">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="bd7fe-933">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-933">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="bd7fe-934">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-934">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="bd7fe-935">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-935">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="bd7fe-936">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-936">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="bd7fe-937">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-937">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="bd7fe-938">Roll</span><span class="sxs-lookup"><span data-stu-id="bd7fe-938">Role</span></span>

* <span data-ttu-id="bd7fe-939">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-939">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="bd7fe-940">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-940">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="bd7fe-941">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-941">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="bd7fe-942">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="bd7fe-942">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="bd7fe-943">SQL</span><span class="sxs-lookup"><span data-stu-id="bd7fe-943">SQL</span></span>

* <span data-ttu-id="bd7fe-944">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-944">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="bd7fe-945">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-945">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="bd7fe-946">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-946">Storage</span></span>

* <span data-ttu-id="bd7fe-947">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-947">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="bd7fe-948">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="bd7fe-948">Add support for incremental blob copy</span></span>
* <span data-ttu-id="bd7fe-949">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="bd7fe-949">Add support for large block blob upload</span></span>
* <span data-ttu-id="bd7fe-950">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-950">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-951">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-951">VM</span></span>

* <span data-ttu-id="bd7fe-952">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="bd7fe-952">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="bd7fe-953">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-953">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="bd7fe-954">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="bd7fe-954">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="bd7fe-955">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-955">az vm/vmss disk</span></span>
  3. <span data-ttu-id="bd7fe-956">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="bd7fe-956">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="bd7fe-957">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="bd7fe-957">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="bd7fe-958">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-958">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="bd7fe-959">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-959">April 3, 2017</span></span>

<span data-ttu-id="bd7fe-960">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="bd7fe-960">Version 2.0.2</span></span>

<span data-ttu-id="bd7fe-961">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-961">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="bd7fe-962">Kärna</span><span class="sxs-lookup"><span data-stu-id="bd7fe-962">Core</span></span>

* <span data-ttu-id="bd7fe-963">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-963">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="bd7fe-964">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-964">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="bd7fe-965">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-965">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="bd7fe-966">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-966">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="bd7fe-967">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-967">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="bd7fe-968">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-968">Add prompting for missing template parameters.</span></span> <span data-ttu-id="bd7fe-969">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-969">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="bd7fe-970">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="bd7fe-970">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="bd7fe-971">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="bd7fe-971">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="bd7fe-972">ACS</span><span class="sxs-lookup"><span data-stu-id="bd7fe-972">ACS</span></span>

* <span data-ttu-id="bd7fe-973">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-973">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="bd7fe-974">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-974">Add support for ssh key password prompting.</span></span> <span data-ttu-id="bd7fe-975">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-975">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="bd7fe-976">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-976">Add support for windows clusters.</span></span> <span data-ttu-id="bd7fe-977">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-977">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="bd7fe-978">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-978">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="bd7fe-979">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-979">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="bd7fe-980">AppService</span><span class="sxs-lookup"><span data-stu-id="bd7fe-980">AppService</span></span>

* <span data-ttu-id="bd7fe-981">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-981">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="bd7fe-982">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-982">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="bd7fe-983">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-983">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="bd7fe-984">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-984">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="bd7fe-985">DataLake</span><span class="sxs-lookup"><span data-stu-id="bd7fe-985">DataLake</span></span>

* <span data-ttu-id="bd7fe-986">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-986">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="bd7fe-987">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-987">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="bd7fe-988">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="bd7fe-988">DocuemntDB</span></span>

* <span data-ttu-id="bd7fe-989">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-989">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="bd7fe-990">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd7fe-990">VM</span></span>

* <span data-ttu-id="bd7fe-991">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-991">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="bd7fe-992">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-992">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="bd7fe-993">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-993">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="bd7fe-994">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-994">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="bd7fe-995">VM-skalningsuppsättning: stöd \* för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-995">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="bd7fe-996">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-996">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="bd7fe-997">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="bd7fe-997">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="bd7fe-998">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="bd7fe-998">February 27, 2017</span></span>

<span data-ttu-id="bd7fe-999">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="bd7fe-999">Version 2.0.0</span></span>

<span data-ttu-id="bd7fe-1000">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1000">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="bd7fe-1001">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1001">General availability applies to these command modules:</span></span>
- <span data-ttu-id="bd7fe-1002">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1002">Container Service (acs)</span></span>
- <span data-ttu-id="bd7fe-1003">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1003">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="bd7fe-1004">Nätverk</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1004">Networking</span></span>
- <span data-ttu-id="bd7fe-1005">Lagring</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1005">Storage</span></span>

<span data-ttu-id="bd7fe-1006">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1006">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="bd7fe-1007">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1007">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="bd7fe-1008">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1008">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="bd7fe-1009">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1009">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="bd7fe-1010">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1010">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="bd7fe-1011">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1011">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="bd7fe-1012">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1012">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="bd7fe-1013">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1013">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="bd7fe-1014">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1014">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="bd7fe-1015">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1015">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="bd7fe-1016">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1016">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="bd7fe-1017">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1017">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="bd7fe-1018">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1018">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="bd7fe-1019">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="bd7fe-1019">Provide feedback from the command line with the `az feedback` command.</span></span>

