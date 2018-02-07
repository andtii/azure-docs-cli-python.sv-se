---
title: Viktig information om Azure CLI 2.0
description: "Lär dig mer om de senaste uppdateringarna till Azure CLI 2.0"
keywords: Viktig information om Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/17/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 86babea3030ea932de1858a391014e5d0bba7f73
ms.sourcegitcommit: cae66f994cb7b7f829f75ac528093fdb6851f64e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="87e1a-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="87e1a-104">Azure CLI 2.0 release notes</span></span>

## <a name="january-17-2018"></a><span data-ttu-id="87e1a-105">17 januari 2018</span><span class="sxs-lookup"><span data-stu-id="87e1a-105">January 17, 2018</span></span>

<span data-ttu-id="87e1a-106">Version 2.0.25</span><span class="sxs-lookup"><span data-stu-id="87e1a-106">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="87e1a-107">ACR</span><span class="sxs-lookup"><span data-stu-id="87e1a-107">ACR</span></span>

* <span data-ttu-id="87e1a-108">ACR-inloggningsåterställning för fel med Windows-autentiseringsuppgifter har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-108">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="87e1a-109">Registerloggar har aktiverats</span><span class="sxs-lookup"><span data-stu-id="87e1a-109">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-110">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-110">ACS</span></span>

* <span data-ttu-id="87e1a-111">Kommandot `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-111">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="87e1a-112">Krav för SPN-roll har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-112">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-113">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-113">Appservice</span></span>

* <span data-ttu-id="87e1a-114">Bugg med `config ssl upload` där `hosting_environment_profile` var null har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-114">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="87e1a-115">Stöd har lagts till för anpassade webbadresser för `browse`</span><span class="sxs-lookup"><span data-stu-id="87e1a-115">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="87e1a-116">Platsstöd har åtgärdats för `log tail`</span><span class="sxs-lookup"><span data-stu-id="87e1a-116">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="87e1a-117">Backup</span><span class="sxs-lookup"><span data-stu-id="87e1a-117">Backup</span></span>

* <span data-ttu-id="87e1a-118">Alternativet `--container-name` för `backup item list` har ändrats så att det är valfritt</span><span class="sxs-lookup"><span data-stu-id="87e1a-118">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="87e1a-119">Alternativ för lagringskonton har lagts till i `backup restore restore-disks`</span><span class="sxs-lookup"><span data-stu-id="87e1a-119">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="87e1a-120">Platsincheckning i `backup protection enable-for-vm` har åtgärdats till skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="87e1a-120">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="87e1a-121">Problem där kommandon misslyckades på grund av ett ogiltigt behållarnamn har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-121">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="87e1a-122">`backup item list` har ändrats så att Hälsostatus ingår som standard</span><span class="sxs-lookup"><span data-stu-id="87e1a-122">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="87e1a-123">Batch</span><span class="sxs-lookup"><span data-stu-id="87e1a-123">Batch</span></span>

* <span data-ttu-id="87e1a-124">`batch login` har ändrats så att information om autentiseringsuppgifter returneras</span><span class="sxs-lookup"><span data-stu-id="87e1a-124">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="87e1a-125">Molnet</span><span class="sxs-lookup"><span data-stu-id="87e1a-125">Cloud</span></span>

* <span data-ttu-id="87e1a-126">Slutpunkter krävs inte längre när du anger `--profile` i ett moln</span><span class="sxs-lookup"><span data-stu-id="87e1a-126">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="87e1a-127">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="87e1a-127">Consumption</span></span>

* <span data-ttu-id="87e1a-128">Nya kommandon för reservationer har lagts till: `consumption reservations summaries` och`consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="87e1a-128">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="87e1a-129">Event Grid</span><span class="sxs-lookup"><span data-stu-id="87e1a-129">Event Grid</span></span>

* <span data-ttu-id="87e1a-130">[VIKTIG ÄNDRING] Kommandona `az eventgrid topic event-subscription` har flyttats till `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="87e1a-130">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="87e1a-131">[VIKTIG ÄNDRING] Kommandona `az eventgrid resource event-subscription` har flyttats till `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="87e1a-131">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="87e1a-132">[VIKTIG ÄNDRING] Kommandot `eventgrid event-subscription show-endpoint-url` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="87e1a-132">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="87e1a-133">Använd `eventgrid event-subscription show --include-full-endpoint-url` istället</span><span class="sxs-lookup"><span data-stu-id="87e1a-133">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="87e1a-134">Kommandot `eventgrid topic update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-134">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="87e1a-135">Kommandot `eventgrid event-subscription update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-135">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="87e1a-136">Parametern `--ids` har lagts till för `eventgrid topic`-kommandon</span><span class="sxs-lookup"><span data-stu-id="87e1a-136">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="87e1a-137">Stöd för tabbifyllning för avsnittsnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-137">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="87e1a-138">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="87e1a-138">Interactive</span></span>

* <span data-ttu-id="87e1a-139">Ett problem där interaktivt läge inte fungerade med Python 2.x har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-139">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="87e1a-140">Fel vid start har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-140">Fixed errors on startup</span></span>
* <span data-ttu-id="87e1a-141">Problem där vissa kommandon inte kördes i interaktivt läge har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-141">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="87e1a-142">IoT</span><span class="sxs-lookup"><span data-stu-id="87e1a-142">IoT</span></span>

* <span data-ttu-id="87e1a-143">Stöd för enhetsetableringstjänst har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-143">Added support for device provisioning service</span></span>
* <span data-ttu-id="87e1a-144">Utfasningsmeddelanden i kommandon och kommandohjälp har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-144">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="87e1a-145">IoT-kontroll för att informera användare om IoT-tillägget har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-145">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-146">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-146">Monitor</span></span>

* <span data-ttu-id="87e1a-147">Stöd för flera diagnostikinställningar har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-147">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="87e1a-148">Parametern `--name` krävs nu för `az monitor diagnostic-settings create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-148">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="87e1a-149">Kommandot `monitor diagnostic-settings categories` har lagts till för att hämta diagnostikinställningskategorin</span><span class="sxs-lookup"><span data-stu-id="87e1a-149">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span> 

### <a name="network"></a><span data-ttu-id="87e1a-150">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-150">Network</span></span>

* <span data-ttu-id="87e1a-151">Ett problem som uppstod vid försök att ändra till eller från aktivt standby-läge med `vnet-gateway update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-151">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="87e1a-152">Stöd för HTTP2 för `application-gateway [create|update]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-152">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="87e1a-153">Profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-153">Profile</span></span>

* <span data-ttu-id="87e1a-154">Stöd för inloggning med användartilldelade identiteter har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-154">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="87e1a-155">Roll</span><span class="sxs-lookup"><span data-stu-id="87e1a-155">Role</span></span>

* <span data-ttu-id="87e1a-156">Argumentet `--assignee-object-id` till `role assignment create` för att kringgå diagramfråga har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-156">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="87e1a-157">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="87e1a-157">Service Fabric</span></span>

* <span data-ttu-id="87e1a-158">Detaljerade fel till verifieringssvar när du skapar kluster har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-158">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="87e1a-159">Problem med klient som saknades har åtgärdats med flera kommandon</span><span class="sxs-lookup"><span data-stu-id="87e1a-159">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-160">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-160">VM</span></span>

* <span data-ttu-id="87e1a-161">[FÖRHANDSVERSION] Stöd mellan zoner för `vmss`</span><span class="sxs-lookup"><span data-stu-id="87e1a-161">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="87e1a-162">[VIKTIG ÄNDRING] Standardinställningen för den enskilda zonen `vmss` har ändrats till "standard" för belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="87e1a-162">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="87e1a-163">[VIKTIG ÄNDRING] `externalIdentities` har ändrats till `userAssignedIdentities` för EMSI</span><span class="sxs-lookup"><span data-stu-id="87e1a-163">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="87e1a-164">[FÖRHANDSVERSION] Stöd har lagts till för växling mellan OS-diskar</span><span class="sxs-lookup"><span data-stu-id="87e1a-164">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="87e1a-165">Stöd har lagts till för användning av VM-avbildningar från andra prenumerationer</span><span class="sxs-lookup"><span data-stu-id="87e1a-165">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="87e1a-166">Argumenten `--plan-name`, `--plan-product`, `--plan-promotion-code` och `--plan-publisher` har lagts till för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-166">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="87e1a-167">Problem med `[vm|vmss] create` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-167">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="87e1a-168">För hög resursanvändning som orsakades av `vm image list --all` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-168">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="87e1a-169">19 december 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-169">December 19, 2017</span></span>

<span data-ttu-id="87e1a-170">Version 2.0.23</span><span class="sxs-lookup"><span data-stu-id="87e1a-170">Version 2.0.23</span></span>

* <span data-ttu-id="87e1a-171">Stöd för inloggning med användartilldelade identiteter har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-171">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="87e1a-172">Behållare</span><span class="sxs-lookup"><span data-stu-id="87e1a-172">Container</span></span>

* <span data-ttu-id="87e1a-173">Åtgärdade felaktig ordning för parametrar för behållarloggar</span><span class="sxs-lookup"><span data-stu-id="87e1a-173">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-174">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-174">Network</span></span>

* <span data-ttu-id="87e1a-175">Argumentet `--disable-bgp-route-propagation` har lagts till för `route-table [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-175">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="87e1a-176">Argumentet `--ip-tags` har lagts till för `public-ip [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-176">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-177">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-177">Storage</span></span>

* <span data-ttu-id="87e1a-178">Stöd har lagts till för lagring V2</span><span class="sxs-lookup"><span data-stu-id="87e1a-178">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-179">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-179">VM</span></span>

* <span data-ttu-id="87e1a-180">[FÖRHANDSVERSION] Ökad stöd för användartilldelade identiteter för virtuella datorer och VMSS</span><span class="sxs-lookup"><span data-stu-id="87e1a-180">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="87e1a-181">5 december 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-181">December 5, 2017</span></span>

<span data-ttu-id="87e1a-182">Version 2.0.22</span><span class="sxs-lookup"><span data-stu-id="87e1a-182">Version 2.0.22</span></span>

* <span data-ttu-id="87e1a-183">`az component` kommandon har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="87e1a-183">Removed `az component` commands.</span></span> <span data-ttu-id="87e1a-184">Använd `az extension` istället</span><span class="sxs-lookup"><span data-stu-id="87e1a-184">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="87e1a-185">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-185">Core</span></span>
* <span data-ttu-id="87e1a-186">`AZURE_US_GOV_CLOUD` AAD-utfärdarslutpunkten har ändrats från login.microsoftonline.com till login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="87e1a-186">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="87e1a-187">Felet med att telemetri kontinuerligt skickades på nytt har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-187">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-188">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-188">ACS</span></span>

* <span data-ttu-id="87e1a-189">Kommandona `aks install-connector` och `aks remove-connector` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-189">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="87e1a-190">Förbättrad felrapportering för `acs create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-190">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="87e1a-191">Användning av `aks get-credentials -f` utan fullständig sökväg har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-191">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="87e1a-192">Advisor</span><span class="sxs-lookup"><span data-stu-id="87e1a-192">Advisor</span></span>

* <span data-ttu-id="87e1a-193">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="87e1a-193">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-194">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-194">Appservice</span></span>

* <span data-ttu-id="87e1a-195">Skapande av certifikatnamn med `webapp config ssl upload` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-195">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="87e1a-196">`webapp [list|show]` och `functionapp [list|show]` har åtgärdats för att visa rätt appar</span><span class="sxs-lookup"><span data-stu-id="87e1a-196">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="87e1a-197">Standardvärde har lagts till för `WEBSITE_NODE_DEFAULT_VERSION`</span><span class="sxs-lookup"><span data-stu-id="87e1a-197">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="87e1a-198">Förbrukning</span><span class="sxs-lookup"><span data-stu-id="87e1a-198">Consumption</span></span>

* <span data-ttu-id="87e1a-199">Stöd för API-versionen 2017-11-30 har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-199">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="87e1a-200">Behållare</span><span class="sxs-lookup"><span data-stu-id="87e1a-200">Container</span></span>

* <span data-ttu-id="87e1a-201">Regression till standardportar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-201">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-202">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-202">Monitor</span></span>

* <span data-ttu-id="87e1a-203">Flerdimensionellt stöd för måttkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-203">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-204">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-204">Resource</span></span>

* <span data-ttu-id="87e1a-205">Argumentet `--include-response-body` har lagts till för `resource show`</span><span class="sxs-lookup"><span data-stu-id="87e1a-205">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="87e1a-206">Roll</span><span class="sxs-lookup"><span data-stu-id="87e1a-206">Role</span></span>

* <span data-ttu-id="87e1a-207">Visning av standardtilldelningar för "klassiska" administratörer till `role assignment list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-207">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="87e1a-208">Stöd har lagts till för `ad sp reset-credentials` för att lägga till autentiseringsuppgifter istället för att skriva över</span><span class="sxs-lookup"><span data-stu-id="87e1a-208">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="87e1a-209">Förbättrad felrapportering för `ad sp create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="87e1a-209">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-210">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-210">SQL</span></span>

* <span data-ttu-id="87e1a-211">Kommandona `sql db list-usages` och `sql db show-usage` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-211">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="87e1a-212">Kommandona `sql server conn-policy show` och `sql server conn-policy update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-212">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-213">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-213">VM</span></span>

* <span data-ttu-id="87e1a-214">Zoninformation har lagts till i `az vm list-skus`</span><span class="sxs-lookup"><span data-stu-id="87e1a-214">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="87e1a-215">14 november 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-215">November 14, 2017</span></span>

<span data-ttu-id="87e1a-216">Version 2.0.21</span><span class="sxs-lookup"><span data-stu-id="87e1a-216">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="87e1a-217">ACR</span><span class="sxs-lookup"><span data-stu-id="87e1a-217">ACR</span></span>

* <span data-ttu-id="87e1a-218">Stöd för att skapa webhooks i replikeringsregioner har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-218">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="87e1a-219">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-219">ACS</span></span>

* <span data-ttu-id="87e1a-220">Alla ”agent” till ”nod” har ändrats i AKS</span><span class="sxs-lookup"><span data-stu-id="87e1a-220">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="87e1a-221">Föråldrat `--orchestrator-release`-alternativ för `acs create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-221">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="87e1a-222">Standardstorleken för virtuella datorer för AKS till `Standard_D1_v2` har ändrats</span><span class="sxs-lookup"><span data-stu-id="87e1a-222">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="87e1a-223">Åtgärdade `az aks browse` i Windows</span><span class="sxs-lookup"><span data-stu-id="87e1a-223">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="87e1a-224">Åtgärdade `az aks get-credentials` i Windows</span><span class="sxs-lookup"><span data-stu-id="87e1a-224">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-225">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-225">Appservice</span></span>

* <span data-ttu-id="87e1a-226">Distributionskälla `config-zip` för webappar och funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-226">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="87e1a-227">`--docker-container-logging`-alternativ till `az webapp log config` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-227">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="87e1a-228">Alternativet `storage` från parametern `--web-server-logging` av `az webapp log config` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-228">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="87e1a-229">Förbättrade felmeddelanden för `deployment user set`</span><span class="sxs-lookup"><span data-stu-id="87e1a-229">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="87e1a-230">Stöd för att skapa Linux-funktionsappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-230">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="87e1a-231">Åtgärdade `list-locations`</span><span class="sxs-lookup"><span data-stu-id="87e1a-231">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="87e1a-232">Batch</span><span class="sxs-lookup"><span data-stu-id="87e1a-232">Batch</span></span>

* <span data-ttu-id="87e1a-233">En bugg har åtgärdats i kommandot för skapande av pool när ett resurs-ID användes med flaggan `--image`</span><span class="sxs-lookup"><span data-stu-id="87e1a-233">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="87e1a-234">Batchai</span><span class="sxs-lookup"><span data-stu-id="87e1a-234">Batchai</span></span>

* <span data-ttu-id="87e1a-235">Ett kort alternativ har lagts till, `-s`, för `--vm-size` VM-storlek i kommandot `file-server create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-235">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="87e1a-236">Kontonamn och nyckelargument har lagts till för `cluster create`-parametrar</span><span class="sxs-lookup"><span data-stu-id="87e1a-236">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="87e1a-237">Dokumentation har skapats för `job list-files` och `job stream-file`</span><span class="sxs-lookup"><span data-stu-id="87e1a-237">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="87e1a-238">Ett kort alternativ har lagts till, `-r`, för `--cluster-name` när klusternamn anges med kommandot `job create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-238">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="87e1a-239">Molnet</span><span class="sxs-lookup"><span data-stu-id="87e1a-239">Cloud</span></span>

* <span data-ttu-id="87e1a-240">`cloud [register|update]` har ändrats för att förhindra att moln registreras som saknar slutpunkter som krävs</span><span class="sxs-lookup"><span data-stu-id="87e1a-240">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="87e1a-241">Behållare</span><span class="sxs-lookup"><span data-stu-id="87e1a-241">Container</span></span>

* <span data-ttu-id="87e1a-242">Stöd för att öppna flera portar har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-242">Added support to open multiple ports</span></span>
* <span data-ttu-id="87e1a-243">Princip för omstart av behållargrupp har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-243">Added container group restart policy</span></span>
* <span data-ttu-id="87e1a-244">Stöd för att montera Azure-filresurs som volym har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-244">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="87e1a-245">Hjälpdokument har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="87e1a-245">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="87e1a-246">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="87e1a-246">Data Lake Analytics</span></span>

* <span data-ttu-id="87e1a-247">`[job|account] list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="87e1a-247">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="87e1a-248">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="87e1a-248">Data Lake Store</span></span>

* <span data-ttu-id="87e1a-249">`account list` har ändrats för att ge mer kortfattad information</span><span class="sxs-lookup"><span data-stu-id="87e1a-249">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="87e1a-250">Anknytning</span><span class="sxs-lookup"><span data-stu-id="87e1a-250">Extension</span></span>

* <span data-ttu-id="87e1a-251">`extension list-available` har lagts till för att tillåta lista över officiella Microsoft-tillägg</span><span class="sxs-lookup"><span data-stu-id="87e1a-251">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="87e1a-252">`--name` har lagts till för `extension [add|update]` för att tillåta installation av tillägg via namn</span><span class="sxs-lookup"><span data-stu-id="87e1a-252">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="87e1a-253">IoT</span><span class="sxs-lookup"><span data-stu-id="87e1a-253">IoT</span></span>

* <span data-ttu-id="87e1a-254">Stöd för certifikatutfärdare (CA) och certifikatkedjor har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-254">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-255">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-255">Monitor</span></span>

* <span data-ttu-id="87e1a-256">`activity-log alert`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-256">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-257">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-257">Network</span></span>

* <span data-ttu-id="87e1a-258">Stöd för CAA DNS-poster har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-258">Added support for CAA DNS records</span></span>
* <span data-ttu-id="87e1a-259">Problem där slutpunkter inte kunde uppdateras med `traffic-manager profile update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-259">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="87e1a-260">Problem där `vnet update --dns-servers` inte fungerade beroende på hur VNET skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-260">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="87e1a-261">Problem där relativa DNS-namn hade importerats felaktigt av `dns zone import` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-261">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="87e1a-262">Reservationer</span><span class="sxs-lookup"><span data-stu-id="87e1a-262">Reservations</span></span>

* <span data-ttu-id="87e1a-263">Inledande förhandsversion</span><span class="sxs-lookup"><span data-stu-id="87e1a-263">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-264">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-264">Resource</span></span>

* <span data-ttu-id="87e1a-265">Stöd för resurs-ID till parametern `--resource` och lås på resursnivå har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-265">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-266">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-266">SQL</span></span>

* <span data-ttu-id="87e1a-267">Parametern `--ignore-missing-vnet-service-endpoint` har lagts till i `sql server vnet-rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-267">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-268">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-268">Storage</span></span>

* <span data-ttu-id="87e1a-269">`storage account create` har ändrats för att använda SKU `Standard_RAGRS` som standard</span><span class="sxs-lookup"><span data-stu-id="87e1a-269">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="87e1a-270">Buggar när fil-/blob-namn som innehåller icke-ASCII-tecken hanteras har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-270">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="87e1a-271">Bugg som förhindrade användning av `--source-uri` med `storage [blob|file] copy start-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-271">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="87e1a-272">Kommandon för blob och borttagning av flera objekt med `storage [blob|file] delete-batch` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-272">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="87e1a-273">Problem vid aktivering av mått med `storage metrics update` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-273">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="87e1a-274">Problem med filer över 200 GB vid användning av `storage blob upload-batch` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-274">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="87e1a-275">Problem där `--bypass` och `--default-action` ignorerades av `storage account [create|update]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-275">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-276">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-276">VM</span></span>

* <span data-ttu-id="87e1a-277">En bugg med `vmss create` som förhindrade användning med storleksnivån `Basic` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-277">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="87e1a-278">`--plan` argument till `[vm|vmss] create` för anpassade avbildningar med faktureringsinformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-278">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="87e1a-279">Kommandona `vm secret `[add|remove|list] har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-279">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="87e1a-280">`vm format-secret` har bytt namn till `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="87e1a-280">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="87e1a-281">Argumentet `--encrypt format` har lagts till för `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="87e1a-281">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="87e1a-282">24 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-282">October 24, 2017</span></span>

<span data-ttu-id="87e1a-283">Version 2.0.20</span><span class="sxs-lookup"><span data-stu-id="87e1a-283">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="87e1a-284">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-284">Core</span></span>

* <span data-ttu-id="87e1a-285">`2017-03-09-profile` har uppdaterats för att använda `MGMT_STORAGE`, API-version `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="87e1a-285">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="87e1a-286">ACR</span><span class="sxs-lookup"><span data-stu-id="87e1a-286">ACR</span></span>

* <span data-ttu-id="87e1a-287">Resurshanteringen har uppdaterats för att peka på API-version `2017-10-01`</span><span class="sxs-lookup"><span data-stu-id="87e1a-287">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="87e1a-288">SKU:n för BYOS ("bring your own storage") har ändrats till klassisk</span><span class="sxs-lookup"><span data-stu-id="87e1a-288">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="87e1a-289">Register-SKU:erna har bytt namn till Basic, Standard och Premium</span><span class="sxs-lookup"><span data-stu-id="87e1a-289">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-290">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-290">ACS</span></span>

* <span data-ttu-id="87e1a-291">[FÖRHANDSVERSION] `az aks`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-291">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="87e1a-292">Kubernetes `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-292">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-293">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-293">Appservice</span></span>

* <span data-ttu-id="87e1a-294">Problem med att nedladdade `webapp`-loggar kunde vara ogiltiga har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-294">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="87e1a-295">Komponent</span><span class="sxs-lookup"><span data-stu-id="87e1a-295">Component</span></span>

* <span data-ttu-id="87e1a-296">Ett tydligare utfasningsmeddelande har lagts till för alla installationsprogram och bekräftelsefrågor</span><span class="sxs-lookup"><span data-stu-id="87e1a-296">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-297">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-297">Monitor</span></span>

* <span data-ttu-id="87e1a-298">`action-group`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-298">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-299">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-299">Resource</span></span>

* <span data-ttu-id="87e1a-300">Inkompatibilitet med den senaste versionen av msrest-beroende i `group export` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-300">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="87e1a-301">`policy assignment create` har åtgärdats så att det fungerar med inbyggda principdefinitioner och principuppsättningsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="87e1a-301">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-302">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-302">VM</span></span>

* <span data-ttu-id="87e1a-303">Argumentet `--accelerated-networking` har lagts till för `vmss create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-303">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="87e1a-304">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-304">October 9, 2017</span></span>

<span data-ttu-id="87e1a-305">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="87e1a-305">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="87e1a-306">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-306">Core</span></span>

* <span data-ttu-id="87e1a-307">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-307">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-308">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-308">Appservice</span></span>

* <span data-ttu-id="87e1a-309">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-309">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="87e1a-310">Batch</span><span class="sxs-lookup"><span data-stu-id="87e1a-310">Batch</span></span>

* <span data-ttu-id="87e1a-311">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="87e1a-311">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="87e1a-312">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="87e1a-312">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="87e1a-313">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-313">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="87e1a-314">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-314">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="87e1a-315">Batchai</span><span class="sxs-lookup"><span data-stu-id="87e1a-315">Batchai</span></span>

* <span data-ttu-id="87e1a-316">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="87e1a-316">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="87e1a-317">KeyVault</span><span class="sxs-lookup"><span data-stu-id="87e1a-317">Keyvault</span></span>

* <span data-ttu-id="87e1a-318">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="87e1a-318">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="87e1a-319">(#4448)</span><span class="sxs-lookup"><span data-stu-id="87e1a-319">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="87e1a-320">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-320">Network</span></span>

* <span data-ttu-id="87e1a-321">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="87e1a-321">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="87e1a-322">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="87e1a-322">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-323">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-323">Resource</span></span>

* <span data-ttu-id="87e1a-324">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="87e1a-324">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="87e1a-325">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="87e1a-325">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="87e1a-326">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="87e1a-326">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="87e1a-327">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="87e1a-327">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-328">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-328">Sql</span></span>

* <span data-ttu-id="87e1a-329">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="87e1a-329">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="87e1a-330">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="87e1a-330">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="87e1a-331">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="87e1a-331">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-332">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-332">Storage</span></span>

* <span data-ttu-id="87e1a-333">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-333">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-334">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-334">Vm</span></span>

* <span data-ttu-id="87e1a-335">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="87e1a-335">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="87e1a-336">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-336">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="87e1a-337">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="87e1a-337">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="87e1a-338">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-338">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="87e1a-339">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-339">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="87e1a-340">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-340">September 22, 2017</span></span>

<span data-ttu-id="87e1a-341">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="87e1a-341">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-342">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-342">Resource</span></span>

* <span data-ttu-id="87e1a-343">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="87e1a-343">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="87e1a-344">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="87e1a-344">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="87e1a-345">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-345">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="87e1a-346">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="87e1a-346">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-347">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-347">Network</span></span>

* <span data-ttu-id="87e1a-348">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="87e1a-348">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="87e1a-349">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="87e1a-349">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="87e1a-350">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-350">Added `asg` application security group commands</span></span>
* <span data-ttu-id="87e1a-351">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-351">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="87e1a-352">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-352">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="87e1a-353">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-353">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="87e1a-354">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-354">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-355">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-355">Storage</span></span>

* <span data-ttu-id="87e1a-356">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="87e1a-356">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="87e1a-357">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="87e1a-357">Eventgrid</span></span>

* <span data-ttu-id="87e1a-358">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="87e1a-358">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-359">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-359">SQL</span></span>

* <span data-ttu-id="87e1a-360">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="87e1a-360">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="87e1a-361">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="87e1a-361">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="87e1a-362">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-362">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="87e1a-363">KeyVault</span><span class="sxs-lookup"><span data-stu-id="87e1a-363">Keyvault</span></span>

* <span data-ttu-id="87e1a-364">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="87e1a-364">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-365">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-365">VM</span></span>

* <span data-ttu-id="87e1a-366">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-366">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="87e1a-367">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="87e1a-367">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="87e1a-368">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-368">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="87e1a-369">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="87e1a-369">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="87e1a-370">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="87e1a-370">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="87e1a-371">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="87e1a-371">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-372">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-372">ACS</span></span>

* <span data-ttu-id="87e1a-373">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="87e1a-373">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-374">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-374">Appservice</span></span>

* <span data-ttu-id="87e1a-375">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-375">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="87e1a-376">Backup</span><span class="sxs-lookup"><span data-stu-id="87e1a-376">Backup</span></span>

* <span data-ttu-id="87e1a-377">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="87e1a-377">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="87e1a-378">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-378">September 11, 2017</span></span>

<span data-ttu-id="87e1a-379">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="87e1a-379">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="87e1a-380">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-380">Core</span></span>

* <span data-ttu-id="87e1a-381">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="87e1a-381">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="87e1a-382">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="87e1a-382">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-383">Acs</span><span class="sxs-lookup"><span data-stu-id="87e1a-383">Acs</span></span>

* <span data-ttu-id="87e1a-384">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-384">Added `acs list-locations` command</span></span>
* <span data-ttu-id="87e1a-385">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="87e1a-385">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-386">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-386">Appservice</span></span>

* <span data-ttu-id="87e1a-387">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-387">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="87e1a-388">CDN</span><span class="sxs-lookup"><span data-stu-id="87e1a-388">CDN</span></span>

* <span data-ttu-id="87e1a-389">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="87e1a-389">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="87e1a-390">Anknytning</span><span class="sxs-lookup"><span data-stu-id="87e1a-390">Extension</span></span>

* <span data-ttu-id="87e1a-391">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="87e1a-391">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="87e1a-392">KeyVault</span><span class="sxs-lookup"><span data-stu-id="87e1a-392">Keyvault</span></span>

* <span data-ttu-id="87e1a-393">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="87e1a-393">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-394">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-394">Network</span></span>

* <span data-ttu-id="87e1a-395">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="87e1a-395">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="87e1a-396">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-396">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="87e1a-397">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-397">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="87e1a-398">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-398">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="87e1a-399">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-399">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-400">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-400">Resource</span></span>

* <span data-ttu-id="87e1a-401">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-401">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="87e1a-402">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-402">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="87e1a-403">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="87e1a-403">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="87e1a-404">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="87e1a-404">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-405">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-405">SQL</span></span>

* <span data-ttu-id="87e1a-406">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-406">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-407">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-407">VM</span></span>

* <span data-ttu-id="87e1a-408">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="87e1a-408">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="87e1a-409">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="87e1a-409">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="87e1a-410">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="87e1a-410">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="87e1a-411">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="87e1a-411">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="87e1a-412">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="87e1a-412">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="87e1a-413">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-413">August 31, 2017</span></span>

<span data-ttu-id="87e1a-414">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="87e1a-414">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="87e1a-415">KeyVault</span><span class="sxs-lookup"><span data-stu-id="87e1a-415">Keyvault</span></span>

* <span data-ttu-id="87e1a-416">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-416">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="87e1a-417">Sf</span><span class="sxs-lookup"><span data-stu-id="87e1a-417">Sf</span></span>

* <span data-ttu-id="87e1a-418">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="87e1a-418">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-419">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-419">Storage</span></span>

* <span data-ttu-id="87e1a-420">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-420">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="87e1a-421">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="87e1a-421">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="87e1a-422">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-422">August 28, 2017</span></span>

<span data-ttu-id="87e1a-423">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="87e1a-423">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="87e1a-424">CLI</span><span class="sxs-lookup"><span data-stu-id="87e1a-424">CLI</span></span>

* <span data-ttu-id="87e1a-425">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-425">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-426">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-426">ACS</span></span>

* <span data-ttu-id="87e1a-427">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="87e1a-427">Corrected preview regions.</span></span>
* <span data-ttu-id="87e1a-428">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="87e1a-428">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="87e1a-429">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="87e1a-429">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-430">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-430">Appservice</span></span>

* <span data-ttu-id="87e1a-431">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-431">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="87e1a-432">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="87e1a-432">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="87e1a-433">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="87e1a-433">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="87e1a-434">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="87e1a-434">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="87e1a-435">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="87e1a-435">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="87e1a-436">IoT</span><span class="sxs-lookup"><span data-stu-id="87e1a-436">IoT</span></span>

* <span data-ttu-id="87e1a-437">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="87e1a-437">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-438">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-438">Network</span></span>

* <span data-ttu-id="87e1a-439">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="87e1a-439">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="87e1a-440">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-440">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="87e1a-441">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="87e1a-441">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="87e1a-442">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-442">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="87e1a-443">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-443">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="87e1a-444">Profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-444">Profile</span></span>

* <span data-ttu-id="87e1a-445">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-445">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="87e1a-446">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="87e1a-446">Service Fabric</span></span>

* <span data-ttu-id="87e1a-447">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="87e1a-447">Preview release</span></span>
* <span data-ttu-id="87e1a-448">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="87e1a-448">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="87e1a-449">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-449">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="87e1a-450">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="87e1a-450">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-451">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-451">Storage</span></span>

* <span data-ttu-id="87e1a-452">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="87e1a-452">Enabled setting blob tier</span></span>
* <span data-ttu-id="87e1a-453">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="87e1a-453">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="87e1a-454">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="87e1a-454">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="87e1a-455">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="87e1a-455">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="87e1a-456">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-456">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="87e1a-457">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="87e1a-457">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-458">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-458">VM</span></span>

* <span data-ttu-id="87e1a-459">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="87e1a-459">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="87e1a-460">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="87e1a-460">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="87e1a-461">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-461">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="87e1a-462">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="87e1a-462">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="87e1a-463">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-463">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="87e1a-464">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-464">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="87e1a-465">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-465">August 15, 2017</span></span>

<span data-ttu-id="87e1a-466">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="87e1a-466">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-467">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-467">ACS</span></span>

* <span data-ttu-id="87e1a-468">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-468">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-469">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-469">Appservice</span></span>

* <span data-ttu-id="87e1a-470">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-470">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="87e1a-471">Event Grid</span><span class="sxs-lookup"><span data-stu-id="87e1a-471">Event Grid</span></span>

* <span data-ttu-id="87e1a-472">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-472">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="87e1a-473">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-473">August 11, 2017</span></span>

<span data-ttu-id="87e1a-474">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="87e1a-474">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-475">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-475">ACS</span></span>

* <span data-ttu-id="87e1a-476">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="87e1a-476">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="87e1a-477">Batch</span><span class="sxs-lookup"><span data-stu-id="87e1a-477">Batch</span></span>

* <span data-ttu-id="87e1a-478">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="87e1a-478">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="87e1a-479">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="87e1a-479">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="87e1a-480">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-480">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="87e1a-481">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="87e1a-481">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="87e1a-482">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="87e1a-482">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="87e1a-483">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="87e1a-483">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="87e1a-484">Komponent</span><span class="sxs-lookup"><span data-stu-id="87e1a-484">Component</span></span>

* <span data-ttu-id="87e1a-485">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="87e1a-485">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="87e1a-486">Behållare</span><span class="sxs-lookup"><span data-stu-id="87e1a-486">Container</span></span>

* <span data-ttu-id="87e1a-487">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="87e1a-487">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="87e1a-488">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="87e1a-488">Data Lake Store</span></span>

* <span data-ttu-id="87e1a-489">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="87e1a-489">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="87e1a-490">Event Grid</span><span class="sxs-lookup"><span data-stu-id="87e1a-490">Event Grid</span></span>

* <span data-ttu-id="87e1a-491">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="87e1a-491">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-492">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-492">Network</span></span>

* <span data-ttu-id="87e1a-493">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="87e1a-493">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="87e1a-494">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="87e1a-494">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="87e1a-495">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="87e1a-495">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="87e1a-496">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="87e1a-496">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="87e1a-497">Profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-497">Profile</span></span>

* <span data-ttu-id="87e1a-498">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="87e1a-498">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-499">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-499">Storage</span></span>

* <span data-ttu-id="87e1a-500">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="87e1a-500">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-501">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-501">VM</span></span>

* <span data-ttu-id="87e1a-502">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="87e1a-502">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="87e1a-503">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="87e1a-503">Exposed `list-skus` command</span></span>
* <span data-ttu-id="87e1a-504">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="87e1a-504">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="87e1a-505">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="87e1a-505">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="87e1a-506">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-506">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="87e1a-507">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-507">July 28, 2017</span></span>

<span data-ttu-id="87e1a-508">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="87e1a-508">Version 2.0.12</span></span>

* <span data-ttu-id="87e1a-509">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-509">Added container commands</span></span>
* <span data-ttu-id="87e1a-510">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-510">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="87e1a-511">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-511">Core</span></span>

* <span data-ttu-id="87e1a-512">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="87e1a-512">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="87e1a-513">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-513">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="87e1a-514">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="87e1a-514">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="87e1a-515">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="87e1a-515">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="87e1a-516">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="87e1a-516">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="87e1a-517">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="87e1a-517">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="87e1a-518">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="87e1a-518">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="87e1a-519">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="87e1a-519">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="87e1a-520">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="87e1a-520">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="87e1a-521">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-521">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="87e1a-522">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="87e1a-522">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="87e1a-523">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="87e1a-523">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="87e1a-524">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="87e1a-524">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="87e1a-525">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="87e1a-525">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="87e1a-526">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="87e1a-526">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="87e1a-527">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="87e1a-527">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="87e1a-528">ACR</span><span class="sxs-lookup"><span data-stu-id="87e1a-528">ACR</span></span>

* <span data-ttu-id="87e1a-529">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="87e1a-529">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="87e1a-530">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="87e1a-530">Support SKU update for managed registries</span></span>
* <span data-ttu-id="87e1a-531">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-531">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="87e1a-532">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="87e1a-532">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="87e1a-533">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="87e1a-533">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="87e1a-534">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="87e1a-534">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-535">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-535">ACS</span></span>

* <span data-ttu-id="87e1a-536">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="87e1a-536">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-537">App Service</span><span class="sxs-lookup"><span data-stu-id="87e1a-537">Appservice</span></span>

* <span data-ttu-id="87e1a-538">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="87e1a-538">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="87e1a-539">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="87e1a-539">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="87e1a-540">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="87e1a-540">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="87e1a-541">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="87e1a-541">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="87e1a-542">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="87e1a-542">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="87e1a-543">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="87e1a-543">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="87e1a-544">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="87e1a-544">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="87e1a-545">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="87e1a-545">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="87e1a-546">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="87e1a-546">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="87e1a-547">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="87e1a-547">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="87e1a-548">Batch</span><span class="sxs-lookup"><span data-stu-id="87e1a-548">Batch</span></span>

* <span data-ttu-id="87e1a-549">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="87e1a-549">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="87e1a-550">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="87e1a-550">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="87e1a-551">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-551">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="87e1a-552">CDN</span><span class="sxs-lookup"><span data-stu-id="87e1a-552">CDN</span></span>

* <span data-ttu-id="87e1a-553">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="87e1a-553">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="87e1a-554">Molnet</span><span class="sxs-lookup"><span data-stu-id="87e1a-554">Cloud</span></span>

* <span data-ttu-id="87e1a-555">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="87e1a-555">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="87e1a-556">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="87e1a-556">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="87e1a-557">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="87e1a-557">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="87e1a-558">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="87e1a-558">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="87e1a-559">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="87e1a-559">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="87e1a-560">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="87e1a-560">CosmosDB</span></span>

* <span data-ttu-id="87e1a-561">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="87e1a-561">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="87e1a-562">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="87e1a-562">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="87e1a-563">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="87e1a-563">Data Lake Analytics</span></span>

* <span data-ttu-id="87e1a-564">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="87e1a-564">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="87e1a-565">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-565">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="87e1a-566">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-566">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="87e1a-567">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="87e1a-567">Data Lake Store</span></span>

* <span data-ttu-id="87e1a-568">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-568">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="87e1a-569">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="87e1a-569">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="87e1a-570">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="87e1a-570">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="87e1a-571">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="87e1a-571">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="87e1a-572">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="87e1a-572">Interactive</span></span>

* <span data-ttu-id="87e1a-573">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="87e1a-573">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="87e1a-574">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="87e1a-574">Increased test coverage</span></span>
* <span data-ttu-id="87e1a-575">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="87e1a-575">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="87e1a-576">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="87e1a-576">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="87e1a-577">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="87e1a-577">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="87e1a-578">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="87e1a-578">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="87e1a-579">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="87e1a-579">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="87e1a-580">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-580">Added `--progress` flag</span></span>
* <span data-ttu-id="87e1a-581">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="87e1a-581">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="87e1a-582">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="87e1a-582">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="87e1a-583">IoT</span><span class="sxs-lookup"><span data-stu-id="87e1a-583">IoT</span></span>

* <span data-ttu-id="87e1a-584">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="87e1a-584">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="87e1a-585">(#3934)</span><span class="sxs-lookup"><span data-stu-id="87e1a-585">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="87e1a-586">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="87e1a-586">Key vault</span></span>

* <span data-ttu-id="87e1a-587">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="87e1a-587">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="87e1a-588">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="87e1a-588">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="87e1a-589">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="87e1a-589">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="87e1a-590">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="87e1a-590">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="87e1a-591">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="87e1a-591">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="87e1a-592">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="87e1a-592">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="87e1a-593">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="87e1a-593">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="87e1a-594">(#3307)</span><span class="sxs-lookup"><span data-stu-id="87e1a-594">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="87e1a-595">Labb</span><span class="sxs-lookup"><span data-stu-id="87e1a-595">Lab</span></span>

* <span data-ttu-id="87e1a-596">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="87e1a-596">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="87e1a-597">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="87e1a-597">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-598">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-598">Monitor</span></span>

* <span data-ttu-id="87e1a-599">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="87e1a-599">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="87e1a-600">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="87e1a-600">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="87e1a-601">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="87e1a-601">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="87e1a-602">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="87e1a-602">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="87e1a-603">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="87e1a-603">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="87e1a-604">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="87e1a-604">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="87e1a-605">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="87e1a-605">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="87e1a-606">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="87e1a-606">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="87e1a-607">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="87e1a-607">`location` no longer required</span></span>
  * <span data-ttu-id="87e1a-608">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="87e1a-608">Add name and ID support for target</span></span>
  * <span data-ttu-id="87e1a-609">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-609">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="87e1a-610">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="87e1a-610">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="87e1a-611">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="87e1a-611">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="87e1a-612">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="87e1a-612">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="87e1a-613">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="87e1a-613">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="87e1a-614">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-614">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-615">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-615">Network</span></span>

* <span data-ttu-id="87e1a-616">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-616">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="87e1a-617">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-617">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="87e1a-618">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="87e1a-618">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="87e1a-619">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="87e1a-619">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="87e1a-620">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-620">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="87e1a-621">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-621">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="87e1a-622">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="87e1a-622">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="87e1a-623">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="87e1a-623">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="87e1a-624">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="87e1a-624">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="87e1a-625">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="87e1a-625">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="87e1a-626">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-626">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="87e1a-627">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="87e1a-627">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="87e1a-628">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="87e1a-628">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="87e1a-629">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-629">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="87e1a-630">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-630">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="87e1a-631">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-631">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="87e1a-632">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-632">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="87e1a-633">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="87e1a-633">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="87e1a-634">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-634">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="87e1a-635">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-635">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="87e1a-636">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="87e1a-636">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="87e1a-637">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="87e1a-637">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="87e1a-638">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="87e1a-638">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="87e1a-639">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="87e1a-639">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="87e1a-640">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="87e1a-640">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="87e1a-641">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="87e1a-641">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="87e1a-642">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="87e1a-642">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="87e1a-643">Profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-643">Profile</span></span>

* <span data-ttu-id="87e1a-644">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="87e1a-644">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="87e1a-645">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="87e1a-645">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="87e1a-646">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="87e1a-646">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="87e1a-647">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="87e1a-647">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="87e1a-648">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="87e1a-648">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="87e1a-649">RDBMS</span><span class="sxs-lookup"><span data-stu-id="87e1a-649">RDBMS</span></span>

* <span data-ttu-id="87e1a-650">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="87e1a-650">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="87e1a-651">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="87e1a-651">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="87e1a-652">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="87e1a-652">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="87e1a-653">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="87e1a-653">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-654">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-654">Resource</span></span>

* <span data-ttu-id="87e1a-655">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-655">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="87e1a-656">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="87e1a-656">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="87e1a-657">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="87e1a-657">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="87e1a-658">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="87e1a-658">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="87e1a-659">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="87e1a-659">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="87e1a-660">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="87e1a-660">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="87e1a-661">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="87e1a-661">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="87e1a-662">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="87e1a-662">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="87e1a-663">Roll</span><span class="sxs-lookup"><span data-stu-id="87e1a-663">Role</span></span>

* <span data-ttu-id="87e1a-664">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="87e1a-664">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="87e1a-665">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="87e1a-665">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="87e1a-666">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="87e1a-666">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="87e1a-667">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="87e1a-667">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="87e1a-668">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="87e1a-668">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="87e1a-669">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="87e1a-669">Service Fabric</span></span>
* <span data-ttu-id="87e1a-670">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="87e1a-670">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="87e1a-671">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="87e1a-671">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="87e1a-672">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="87e1a-672">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-673">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-673">SQL</span></span>

* <span data-ttu-id="87e1a-674">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="87e1a-674">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="87e1a-675">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="87e1a-675">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="87e1a-676">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="87e1a-676">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-677">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-677">Storage</span></span>

* <span data-ttu-id="87e1a-678">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="87e1a-678">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="87e1a-679">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="87e1a-679">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="87e1a-680">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="87e1a-680">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="87e1a-681">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="87e1a-681">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="87e1a-682">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="87e1a-682">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="87e1a-683">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="87e1a-683">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-684">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-684">VM</span></span>

* <span data-ttu-id="87e1a-685">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="87e1a-685">Support configuring nsg</span></span>
* <span data-ttu-id="87e1a-686">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="87e1a-686">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="87e1a-687">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="87e1a-687">Support managed service identities</span></span>
* <span data-ttu-id="87e1a-688">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-688">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="87e1a-689">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="87e1a-689">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="87e1a-690">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-690">May 10, 2017</span></span>

<span data-ttu-id="87e1a-691">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="87e1a-691">Version 2.0.6</span></span>

* <span data-ttu-id="87e1a-692">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="87e1a-692">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="87e1a-693">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="87e1a-693">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="87e1a-694">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="87e1a-694">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="87e1a-695">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="87e1a-695">Include Cognitive Services module.</span></span>
* <span data-ttu-id="87e1a-696">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="87e1a-696">Include Service Fabric module.</span></span>
* <span data-ttu-id="87e1a-697">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="87e1a-697">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="87e1a-698">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="87e1a-698">Add support for CDN commands.</span></span>
* <span data-ttu-id="87e1a-699">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="87e1a-699">Remove Container module.</span></span>
* <span data-ttu-id="87e1a-700">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="87e1a-700">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="87e1a-701">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="87e1a-701">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="87e1a-702">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-702">Core</span></span>

* <span data-ttu-id="87e1a-703">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="87e1a-703">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="87e1a-704">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="87e1a-704">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="87e1a-705">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="87e1a-705">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="87e1a-706">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="87e1a-706">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="87e1a-707">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="87e1a-707">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="87e1a-708">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="87e1a-708">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="87e1a-709">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="87e1a-709">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="87e1a-710">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="87e1a-710">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="87e1a-711">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="87e1a-711">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="87e1a-712">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="87e1a-712">core: Improved performance</span></span>
* <span data-ttu-id="87e1a-713">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="87e1a-713">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="87e1a-714">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="87e1a-714">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-715">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-715">ACS</span></span>

* <span data-ttu-id="87e1a-716">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="87e1a-716">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="87e1a-717">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="87e1a-717">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="87e1a-718">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="87e1a-718">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="87e1a-719">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="87e1a-719">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-720">AppService</span><span class="sxs-lookup"><span data-stu-id="87e1a-720">AppService</span></span>

* <span data-ttu-id="87e1a-721">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="87e1a-721">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="87e1a-722">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="87e1a-722">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="87e1a-723">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="87e1a-723">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="87e1a-724">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="87e1a-724">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="87e1a-725">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="87e1a-725">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="87e1a-726">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="87e1a-726">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="87e1a-727">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="87e1a-727">support slot swap with preview</span></span>
* <span data-ttu-id="87e1a-728">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="87e1a-728">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="87e1a-729">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="87e1a-729">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="87e1a-730">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="87e1a-730">CosmosDB</span></span>

* <span data-ttu-id="87e1a-731">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="87e1a-731">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="87e1a-732">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="87e1a-732">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="87e1a-733">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="87e1a-733">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="87e1a-734">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="87e1a-734">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="87e1a-735">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="87e1a-735">Data Lake Analytics</span></span>

* <span data-ttu-id="87e1a-736">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="87e1a-736">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="87e1a-737">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="87e1a-737">Add support for new catalog item type: package.</span></span> <span data-ttu-id="87e1a-738">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="87e1a-738">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="87e1a-739">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="87e1a-739">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="87e1a-740">Tabell</span><span class="sxs-lookup"><span data-stu-id="87e1a-740">Table</span></span>
  * <span data-ttu-id="87e1a-741">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="87e1a-741">Table valued function</span></span>
  * <span data-ttu-id="87e1a-742">Visa</span><span class="sxs-lookup"><span data-stu-id="87e1a-742">View</span></span>
  * <span data-ttu-id="87e1a-743">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="87e1a-743">Table Statistics.</span></span> <span data-ttu-id="87e1a-744">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="87e1a-744">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="87e1a-745">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="87e1a-745">Data Lake Store</span></span>

* <span data-ttu-id="87e1a-746">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="87e1a-746">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="87e1a-747">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="87e1a-747">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="87e1a-748">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="87e1a-748">missed help for access show.</span></span> <span data-ttu-id="87e1a-749">läggs till.</span><span class="sxs-lookup"><span data-stu-id="87e1a-749">adding it.</span></span> <span data-ttu-id="87e1a-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="87e1a-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="87e1a-751">Hitta</span><span class="sxs-lookup"><span data-stu-id="87e1a-751">Find</span></span>

* <span data-ttu-id="87e1a-752">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="87e1a-752">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="87e1a-753">KeyVault</span><span class="sxs-lookup"><span data-stu-id="87e1a-753">KeyVault</span></span>

* <span data-ttu-id="87e1a-754">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="87e1a-754">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="87e1a-755">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87e1a-755">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="87e1a-756">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="87e1a-756">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="87e1a-757">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="87e1a-757">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="87e1a-758">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="87e1a-758">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="87e1a-759">Labb</span><span class="sxs-lookup"><span data-stu-id="87e1a-759">Lab</span></span>

* <span data-ttu-id="87e1a-760">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="87e1a-760">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="87e1a-761">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="87e1a-761">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="87e1a-762">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="87e1a-762">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="87e1a-763">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="87e1a-763">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="87e1a-764">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="87e1a-764">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="87e1a-765">Övervaka</span><span class="sxs-lookup"><span data-stu-id="87e1a-765">Monitor</span></span>

* <span data-ttu-id="87e1a-766">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="87e1a-766">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="87e1a-767">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="87e1a-767">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="87e1a-768">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-768">Network</span></span>

* <span data-ttu-id="87e1a-769">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-769">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="87e1a-770">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-770">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="87e1a-771">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="87e1a-771">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="87e1a-772">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="87e1a-772">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="87e1a-773">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="87e1a-773">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="87e1a-774">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="87e1a-774">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="87e1a-775">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="87e1a-775">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="87e1a-776">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="87e1a-776">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="87e1a-777">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-777">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="87e1a-778">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="87e1a-778">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="87e1a-779">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="87e1a-779">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="87e1a-780">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="87e1a-780">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="87e1a-781">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="87e1a-781">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="87e1a-782">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="87e1a-782">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="87e1a-783">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="87e1a-783">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="87e1a-784">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="87e1a-784">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="87e1a-785">Profil</span><span class="sxs-lookup"><span data-stu-id="87e1a-785">Profile</span></span>

* <span data-ttu-id="87e1a-786">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="87e1a-786">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="87e1a-787">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="87e1a-787">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="87e1a-788">Redis</span><span class="sxs-lookup"><span data-stu-id="87e1a-788">Redis</span></span>

* <span data-ttu-id="87e1a-789">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="87e1a-789">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="87e1a-790">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="87e1a-790">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="87e1a-791">Resurs</span><span class="sxs-lookup"><span data-stu-id="87e1a-791">Resource</span></span>

* <span data-ttu-id="87e1a-792">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="87e1a-792">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="87e1a-793">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="87e1a-793">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="87e1a-794">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="87e1a-794">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="87e1a-795">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="87e1a-795">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="87e1a-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="87e1a-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="87e1a-797">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="87e1a-797">Add docs for az lock update.</span></span> <span data-ttu-id="87e1a-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="87e1a-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="87e1a-799">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="87e1a-799">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="87e1a-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="87e1a-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="87e1a-801">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="87e1a-801">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="87e1a-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="87e1a-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="87e1a-803">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="87e1a-803">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="87e1a-804">Roll</span><span class="sxs-lookup"><span data-stu-id="87e1a-804">Role</span></span>

* <span data-ttu-id="87e1a-805">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="87e1a-805">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="87e1a-806">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="87e1a-806">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="87e1a-807">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="87e1a-807">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="87e1a-808">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="87e1a-808">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="87e1a-809">SQL</span><span class="sxs-lookup"><span data-stu-id="87e1a-809">SQL</span></span>

* <span data-ttu-id="87e1a-810">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="87e1a-810">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="87e1a-811">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="87e1a-811">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="87e1a-812">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-812">Storage</span></span>

* <span data-ttu-id="87e1a-813">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-813">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="87e1a-814">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="87e1a-814">Add support for incremental blob copy</span></span>
* <span data-ttu-id="87e1a-815">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="87e1a-815">Add support for large block blob upload</span></span>
* <span data-ttu-id="87e1a-816">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="87e1a-816">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-817">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-817">VM</span></span>

* <span data-ttu-id="87e1a-818">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="87e1a-818">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="87e1a-819">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="87e1a-819">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="87e1a-820">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="87e1a-820">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="87e1a-821">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="87e1a-821">az vm/vmss disk</span></span>
  3. <span data-ttu-id="87e1a-822">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="87e1a-822">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="87e1a-823">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="87e1a-823">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="87e1a-824">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="87e1a-824">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="87e1a-825">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-825">April 3, 2017</span></span>

<span data-ttu-id="87e1a-826">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="87e1a-826">Version 2.0.2</span></span>

<span data-ttu-id="87e1a-827">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="87e1a-827">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="87e1a-828">Kärna</span><span class="sxs-lookup"><span data-stu-id="87e1a-828">Core</span></span>

* <span data-ttu-id="87e1a-829">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="87e1a-829">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="87e1a-830">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="87e1a-830">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="87e1a-831">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="87e1a-831">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="87e1a-832">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="87e1a-832">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="87e1a-833">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="87e1a-833">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="87e1a-834">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="87e1a-834">Add prompting for missing template parameters.</span></span> <span data-ttu-id="87e1a-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="87e1a-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="87e1a-836">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="87e1a-836">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="87e1a-837">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="87e1a-837">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="87e1a-838">ACS</span><span class="sxs-lookup"><span data-stu-id="87e1a-838">ACS</span></span>

* <span data-ttu-id="87e1a-839">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="87e1a-839">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="87e1a-840">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="87e1a-840">Add support for ssh key password prompting.</span></span> <span data-ttu-id="87e1a-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="87e1a-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="87e1a-842">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="87e1a-842">Add support for windows clusters.</span></span> <span data-ttu-id="87e1a-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="87e1a-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="87e1a-844">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="87e1a-844">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="87e1a-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="87e1a-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="87e1a-846">AppService</span><span class="sxs-lookup"><span data-stu-id="87e1a-846">AppService</span></span>

* <span data-ttu-id="87e1a-847">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="87e1a-847">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="87e1a-848">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="87e1a-848">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="87e1a-849">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="87e1a-849">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="87e1a-850">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="87e1a-850">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="87e1a-851">DataLake</span><span class="sxs-lookup"><span data-stu-id="87e1a-851">DataLake</span></span>

* <span data-ttu-id="87e1a-852">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="87e1a-852">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="87e1a-853">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="87e1a-853">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="87e1a-854">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="87e1a-854">DocuemntDB</span></span>

* <span data-ttu-id="87e1a-855">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="87e1a-855">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="87e1a-856">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="87e1a-856">VM</span></span>

* <span data-ttu-id="87e1a-857">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="87e1a-857">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="87e1a-858">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="87e1a-858">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="87e1a-859">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="87e1a-859">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="87e1a-860">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="87e1a-860">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="87e1a-861">VM-skalningsuppsättning: stöd \* för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="87e1a-861">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="87e1a-862">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="87e1a-862">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="87e1a-863">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="87e1a-863">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="87e1a-864">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="87e1a-864">February 27, 2017</span></span>

<span data-ttu-id="87e1a-865">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="87e1a-865">Version 2.0.0</span></span>

<span data-ttu-id="87e1a-866">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="87e1a-866">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="87e1a-867">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="87e1a-867">General availability applies to these command modules:</span></span>
- <span data-ttu-id="87e1a-868">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="87e1a-868">Container Service (acs)</span></span>
- <span data-ttu-id="87e1a-869">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="87e1a-869">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="87e1a-870">Nätverk</span><span class="sxs-lookup"><span data-stu-id="87e1a-870">Networking</span></span>
- <span data-ttu-id="87e1a-871">Lagring</span><span class="sxs-lookup"><span data-stu-id="87e1a-871">Storage</span></span>

<span data-ttu-id="87e1a-872">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="87e1a-872">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="87e1a-873">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="87e1a-873">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="87e1a-874">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-874">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="87e1a-875">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="87e1a-875">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="87e1a-876">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-876">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="87e1a-877">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="87e1a-877">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="87e1a-878">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="87e1a-878">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="87e1a-879">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="87e1a-879">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="87e1a-880">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="87e1a-880">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="87e1a-881">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="87e1a-881">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="87e1a-882">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="87e1a-882">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="87e1a-883">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="87e1a-883">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="87e1a-884">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="87e1a-884">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="87e1a-885">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="87e1a-885">Provide feedback from the command line with the `az feedback` command.</span></span>

