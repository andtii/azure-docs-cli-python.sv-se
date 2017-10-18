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
ms.openlocfilehash: 2ea9daa558200204750f19b5d22685587ff097ef
ms.sourcegitcommit: 376bc0601aba890630dadd55908c1a65ddf40f5a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="7e8c1-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="7e8c1-104">Azure CLI 2.0 release notes</span></span>

## <a name="october-9-2017"></a><span data-ttu-id="7e8c1-105">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-105">October 9, 2017</span></span>

<span data-ttu-id="7e8c1-106">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="7e8c1-106">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="7e8c1-107">Kärna</span><span class="sxs-lookup"><span data-stu-id="7e8c1-107">Core</span></span>

* <span data-ttu-id="7e8c1-108">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-108">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-109">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-109">Appservice</span></span>

* <span data-ttu-id="7e8c1-110">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-110">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="7e8c1-111">Batch</span><span class="sxs-lookup"><span data-stu-id="7e8c1-111">Batch</span></span>

* <span data-ttu-id="7e8c1-112">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="7e8c1-112">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="7e8c1-113">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="7e8c1-113">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="7e8c1-114">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-114">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="7e8c1-115">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e8c1-115">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="7e8c1-116">Batchai</span><span class="sxs-lookup"><span data-stu-id="7e8c1-116">Batchai</span></span>

* <span data-ttu-id="7e8c1-117">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-117">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="7e8c1-118">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e8c1-118">Keyvault</span></span>

* <span data-ttu-id="7e8c1-119">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-119">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="7e8c1-120">(#4448)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-120">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="7e8c1-121">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-121">Network</span></span>

* <span data-ttu-id="7e8c1-122">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="7e8c1-122">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="7e8c1-123">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="7e8c1-123">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="7e8c1-124">Resurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-124">Resource</span></span>

* <span data-ttu-id="7e8c1-125">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-125">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="7e8c1-126">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="7e8c1-126">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="7e8c1-127">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="7e8c1-127">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="7e8c1-128">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="7e8c1-128">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="7e8c1-129">SQL</span><span class="sxs-lookup"><span data-stu-id="7e8c1-129">Sql</span></span>

* <span data-ttu-id="7e8c1-130">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="7e8c1-130">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="7e8c1-131">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="7e8c1-131">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="7e8c1-132">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-132">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-133">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-133">Storage</span></span>

* <span data-ttu-id="7e8c1-134">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-134">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-135">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-135">Vm</span></span>

* <span data-ttu-id="7e8c1-136">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="7e8c1-136">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="7e8c1-137">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-137">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="7e8c1-138">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-138">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="7e8c1-139">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-139">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="7e8c1-140">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-140">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="7e8c1-141">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-141">September 22, 2017</span></span>

<span data-ttu-id="7e8c1-142">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="7e8c1-142">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="7e8c1-143">Resurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-143">Resource</span></span>

* <span data-ttu-id="7e8c1-144">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="7e8c1-144">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="7e8c1-145">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="7e8c1-145">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="7e8c1-146">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-146">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="7e8c1-147">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-147">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-148">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-148">Network</span></span>

* <span data-ttu-id="7e8c1-149">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-149">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="7e8c1-150">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-150">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="7e8c1-151">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-151">Added `asg` application security group commands</span></span>
* <span data-ttu-id="7e8c1-152">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-152">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="7e8c1-153">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-153">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="7e8c1-154">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-154">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="7e8c1-155">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-155">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-156">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-156">Storage</span></span>

* <span data-ttu-id="7e8c1-157">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="7e8c1-157">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="7e8c1-158">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="7e8c1-158">Eventgrid</span></span>

* <span data-ttu-id="7e8c1-159">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="7e8c1-159">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="7e8c1-160">SQL</span><span class="sxs-lookup"><span data-stu-id="7e8c1-160">SQL</span></span>

* <span data-ttu-id="7e8c1-161">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-161">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="7e8c1-162">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-162">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="7e8c1-163">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-163">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="7e8c1-164">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e8c1-164">Keyvault</span></span>

* <span data-ttu-id="7e8c1-165">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="7e8c1-165">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-166">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-166">VM</span></span>

* <span data-ttu-id="7e8c1-167">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-167">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="7e8c1-168">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="7e8c1-168">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="7e8c1-169">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-169">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="7e8c1-170">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-170">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="7e8c1-171">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-171">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="7e8c1-172">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-172">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-173">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-173">ACS</span></span>

* <span data-ttu-id="7e8c1-174">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="7e8c1-174">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-175">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-175">Appservice</span></span>

* <span data-ttu-id="7e8c1-176">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-176">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="7e8c1-177">Säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="7e8c1-177">Backup</span></span>

* <span data-ttu-id="7e8c1-178">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="7e8c1-178">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="7e8c1-179">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-179">September 11, 2017</span></span>

<span data-ttu-id="7e8c1-180">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="7e8c1-180">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="7e8c1-181">Kärna</span><span class="sxs-lookup"><span data-stu-id="7e8c1-181">Core</span></span>

* <span data-ttu-id="7e8c1-182">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="7e8c1-182">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="7e8c1-183">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="7e8c1-183">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-184">Acs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-184">Acs</span></span>

* <span data-ttu-id="7e8c1-185">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-185">Added `acs list-locations` command</span></span>
* <span data-ttu-id="7e8c1-186">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="7e8c1-186">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-187">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-187">Appservice</span></span>

* <span data-ttu-id="7e8c1-188">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-188">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="7e8c1-189">CDN</span><span class="sxs-lookup"><span data-stu-id="7e8c1-189">CDN</span></span>

* <span data-ttu-id="7e8c1-190">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-190">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="7e8c1-191">Anknytning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-191">Extension</span></span>

* <span data-ttu-id="7e8c1-192">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-192">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="7e8c1-193">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e8c1-193">Keyvault</span></span>

* <span data-ttu-id="7e8c1-194">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-194">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-195">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-195">Network</span></span>

* <span data-ttu-id="7e8c1-196">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-196">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="7e8c1-197">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-197">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="7e8c1-198">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-198">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="7e8c1-199">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-199">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="7e8c1-200">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-200">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="7e8c1-201">Resurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-201">Resource</span></span>

* <span data-ttu-id="7e8c1-202">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-202">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="7e8c1-203">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-203">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="7e8c1-204">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="7e8c1-204">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="7e8c1-205">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-205">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="7e8c1-206">SQL</span><span class="sxs-lookup"><span data-stu-id="7e8c1-206">SQL</span></span>

* <span data-ttu-id="7e8c1-207">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-207">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-208">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-208">VM</span></span>

* <span data-ttu-id="7e8c1-209">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="7e8c1-209">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="7e8c1-210">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="7e8c1-210">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="7e8c1-211">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-211">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="7e8c1-212">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-212">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="7e8c1-213">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="7e8c1-213">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="7e8c1-214">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-214">August 31, 2017</span></span>

<span data-ttu-id="7e8c1-215">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="7e8c1-215">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="7e8c1-216">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e8c1-216">Keyvault</span></span>

* <span data-ttu-id="7e8c1-217">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-217">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="7e8c1-218">Sf</span><span class="sxs-lookup"><span data-stu-id="7e8c1-218">Sf</span></span>

* <span data-ttu-id="7e8c1-219">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-219">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-220">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-220">Storage</span></span>

* <span data-ttu-id="7e8c1-221">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-221">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="7e8c1-222">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="7e8c1-222">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="7e8c1-223">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-223">August 28, 2017</span></span>

<span data-ttu-id="7e8c1-224">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="7e8c1-224">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="7e8c1-225">CLI</span><span class="sxs-lookup"><span data-stu-id="7e8c1-225">CLI</span></span>

* <span data-ttu-id="7e8c1-226">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-226">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-227">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-227">ACS</span></span>

* <span data-ttu-id="7e8c1-228">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-228">Corrected preview regions.</span></span>
* <span data-ttu-id="7e8c1-229">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-229">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="7e8c1-230">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-230">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-231">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-231">Appservice</span></span>

* <span data-ttu-id="7e8c1-232">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-232">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="7e8c1-233">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-233">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="7e8c1-234">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-234">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="7e8c1-235">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="7e8c1-235">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="7e8c1-236">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-236">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="7e8c1-237">IoT</span><span class="sxs-lookup"><span data-stu-id="7e8c1-237">IoT</span></span>

* <span data-ttu-id="7e8c1-238">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="7e8c1-238">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-239">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-239">Network</span></span>

* <span data-ttu-id="7e8c1-240">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-240">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="7e8c1-241">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-241">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="7e8c1-242">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-242">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="7e8c1-243">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-243">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="7e8c1-244">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-244">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="7e8c1-245">Profil</span><span class="sxs-lookup"><span data-stu-id="7e8c1-245">Profile</span></span>

* <span data-ttu-id="7e8c1-246">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-246">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7e8c1-247">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7e8c1-247">Service Fabric</span></span>

* <span data-ttu-id="7e8c1-248">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="7e8c1-248">Preview release</span></span>
* <span data-ttu-id="7e8c1-249">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="7e8c1-249">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="7e8c1-250">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-250">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="7e8c1-251">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-251">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-252">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-252">Storage</span></span>

* <span data-ttu-id="7e8c1-253">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="7e8c1-253">Enabled setting blob tier</span></span>
* <span data-ttu-id="7e8c1-254">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="7e8c1-254">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="7e8c1-255">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-255">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="7e8c1-256">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-256">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="7e8c1-257">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-257">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="7e8c1-258">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="7e8c1-258">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-259">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-259">VM</span></span>

* <span data-ttu-id="7e8c1-260">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-260">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="7e8c1-261">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-261">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="7e8c1-262">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-262">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="7e8c1-263">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-263">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="7e8c1-264">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-264">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="7e8c1-265">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-265">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="7e8c1-266">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-266">August 15, 2017</span></span>

<span data-ttu-id="7e8c1-267">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="7e8c1-267">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-268">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-268">ACS</span></span>

* <span data-ttu-id="7e8c1-269">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-269">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-270">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-270">Appservice</span></span>

* <span data-ttu-id="7e8c1-271">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-271">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="7e8c1-272">Event Grid</span><span class="sxs-lookup"><span data-stu-id="7e8c1-272">Event Grid</span></span>

* <span data-ttu-id="7e8c1-273">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-273">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="7e8c1-274">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-274">August 11, 2017</span></span>

<span data-ttu-id="7e8c1-275">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="7e8c1-275">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-276">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-276">ACS</span></span>

* <span data-ttu-id="7e8c1-277">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-277">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="7e8c1-278">Batch</span><span class="sxs-lookup"><span data-stu-id="7e8c1-278">Batch</span></span>

* <span data-ttu-id="7e8c1-279">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7e8c1-279">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="7e8c1-280">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e8c1-280">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="7e8c1-281">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-281">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="7e8c1-282">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="7e8c1-282">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="7e8c1-283">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e8c1-283">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="7e8c1-284">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="7e8c1-284">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="7e8c1-285">Komponent</span><span class="sxs-lookup"><span data-stu-id="7e8c1-285">Component</span></span>

* <span data-ttu-id="7e8c1-286">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="7e8c1-286">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="7e8c1-287">Behållare</span><span class="sxs-lookup"><span data-stu-id="7e8c1-287">Container</span></span>

* <span data-ttu-id="7e8c1-288">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="7e8c1-288">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="7e8c1-289">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7e8c1-289">Data Lake Store</span></span>

* <span data-ttu-id="7e8c1-290">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="7e8c1-290">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="7e8c1-291">Event Grid</span><span class="sxs-lookup"><span data-stu-id="7e8c1-291">Event Grid</span></span>

* <span data-ttu-id="7e8c1-292">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="7e8c1-292">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-293">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-293">Network</span></span>

* <span data-ttu-id="7e8c1-294">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="7e8c1-294">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="7e8c1-295">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="7e8c1-295">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="7e8c1-296">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-296">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="7e8c1-297">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-297">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="7e8c1-298">Profil</span><span class="sxs-lookup"><span data-stu-id="7e8c1-298">Profile</span></span>

* <span data-ttu-id="7e8c1-299">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="7e8c1-299">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-300">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-300">Storage</span></span>

* <span data-ttu-id="7e8c1-301">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="7e8c1-301">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-302">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-302">VM</span></span>

* <span data-ttu-id="7e8c1-303">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-303">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="7e8c1-304">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-304">Exposed `list-skus` command</span></span>
* <span data-ttu-id="7e8c1-305">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-305">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="7e8c1-306">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="7e8c1-306">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="7e8c1-307">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e8c1-307">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="7e8c1-308">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-308">July 28, 2017</span></span>

<span data-ttu-id="7e8c1-309">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="7e8c1-309">Version 2.0.12</span></span>

* <span data-ttu-id="7e8c1-310">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-310">Added container commands</span></span>
* <span data-ttu-id="7e8c1-311">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-311">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="7e8c1-312">Kärna</span><span class="sxs-lookup"><span data-stu-id="7e8c1-312">Core</span></span>

* <span data-ttu-id="7e8c1-313">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="7e8c1-313">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="7e8c1-314">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-314">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="7e8c1-315">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="7e8c1-315">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="7e8c1-316">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-316">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="7e8c1-317">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-317">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="7e8c1-318">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-318">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="7e8c1-319">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-319">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="7e8c1-320">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-320">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="7e8c1-321">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-321">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="7e8c1-322">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="7e8c1-322">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="7e8c1-323">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-323">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="7e8c1-324">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-324">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="7e8c1-325">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="7e8c1-325">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="7e8c1-326">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="7e8c1-326">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="7e8c1-327">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="7e8c1-327">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="7e8c1-328">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-328">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="7e8c1-329">ACR</span><span class="sxs-lookup"><span data-stu-id="7e8c1-329">ACR</span></span>

* <span data-ttu-id="7e8c1-330">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="7e8c1-330">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="7e8c1-331">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="7e8c1-331">Support SKU update for managed registries</span></span>
* <span data-ttu-id="7e8c1-332">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-332">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="7e8c1-333">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="7e8c1-333">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="7e8c1-334">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="7e8c1-334">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="7e8c1-335">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-335">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-336">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-336">ACS</span></span>

* <span data-ttu-id="7e8c1-337">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="7e8c1-337">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-338">App Service</span><span class="sxs-lookup"><span data-stu-id="7e8c1-338">Appservice</span></span>

* <span data-ttu-id="7e8c1-339">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="7e8c1-339">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="7e8c1-340">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="7e8c1-340">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="7e8c1-341">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-341">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="7e8c1-342">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-342">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="7e8c1-343">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-343">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="7e8c1-344">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-344">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="7e8c1-345">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-345">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="7e8c1-346">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-346">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="7e8c1-347">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-347">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="7e8c1-348">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="7e8c1-348">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="7e8c1-349">Batch</span><span class="sxs-lookup"><span data-stu-id="7e8c1-349">Batch</span></span>

* <span data-ttu-id="7e8c1-350">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="7e8c1-350">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="7e8c1-351">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-351">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="7e8c1-352">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-352">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="7e8c1-353">CDN</span><span class="sxs-lookup"><span data-stu-id="7e8c1-353">CDN</span></span>

* <span data-ttu-id="7e8c1-354">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-354">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="7e8c1-355">Molnet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-355">Cloud</span></span>

* <span data-ttu-id="7e8c1-356">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="7e8c1-356">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="7e8c1-357">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="7e8c1-357">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="7e8c1-358">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="7e8c1-358">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="7e8c1-359">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-359">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="7e8c1-360">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-360">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7e8c1-361">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7e8c1-361">CosmosDB</span></span>

* <span data-ttu-id="7e8c1-362">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="7e8c1-362">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="7e8c1-363">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-363">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="7e8c1-364">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="7e8c1-364">Data Lake Analytics</span></span>

* <span data-ttu-id="7e8c1-365">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-365">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="7e8c1-366">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-366">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="7e8c1-367">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-367">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="7e8c1-368">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7e8c1-368">Data Lake Store</span></span>

* <span data-ttu-id="7e8c1-369">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-369">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="7e8c1-370">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7e8c1-370">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="7e8c1-371">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-371">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="7e8c1-372">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="7e8c1-372">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="7e8c1-373">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="7e8c1-373">Interactive</span></span>

* <span data-ttu-id="7e8c1-374">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="7e8c1-374">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="7e8c1-375">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-375">Increased test coverage</span></span>
* <span data-ttu-id="7e8c1-376">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="7e8c1-376">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="7e8c1-377">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-377">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="7e8c1-378">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-378">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="7e8c1-379">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-379">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="7e8c1-380">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-380">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="7e8c1-381">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-381">Added `--progress` flag</span></span>
* <span data-ttu-id="7e8c1-382">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="7e8c1-382">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="7e8c1-383">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-383">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="7e8c1-384">IoT</span><span class="sxs-lookup"><span data-stu-id="7e8c1-384">IoT</span></span>

* <span data-ttu-id="7e8c1-385">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-385">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="7e8c1-386">(#3934)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-386">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="7e8c1-387">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="7e8c1-387">Key vault</span></span>

* <span data-ttu-id="7e8c1-388">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-388">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="7e8c1-389">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-389">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="7e8c1-390">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-390">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="7e8c1-391">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-391">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="7e8c1-392">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-392">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="7e8c1-393">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-393">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="7e8c1-394">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-394">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="7e8c1-395">(#3307)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-395">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="7e8c1-396">Labb</span><span class="sxs-lookup"><span data-stu-id="7e8c1-396">Lab</span></span>

* <span data-ttu-id="7e8c1-397">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-397">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="7e8c1-398">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-398">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="7e8c1-399">Övervaka</span><span class="sxs-lookup"><span data-stu-id="7e8c1-399">Monitor</span></span>

* <span data-ttu-id="7e8c1-400">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-400">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="7e8c1-401">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-401">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="7e8c1-402">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-402">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="7e8c1-403">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-403">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="7e8c1-404">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-404">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="7e8c1-405">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-405">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="7e8c1-406">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="7e8c1-406">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="7e8c1-407">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="7e8c1-407">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="7e8c1-408">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="7e8c1-408">`location` no longer required</span></span>
  * <span data-ttu-id="7e8c1-409">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="7e8c1-409">Add name and ID support for target</span></span>
  * <span data-ttu-id="7e8c1-410">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e8c1-410">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="7e8c1-411">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="7e8c1-411">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="7e8c1-412">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="7e8c1-412">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="7e8c1-413">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-413">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="7e8c1-414">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="7e8c1-414">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="7e8c1-415">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-415">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-416">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-416">Network</span></span>

* <span data-ttu-id="7e8c1-417">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-417">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="7e8c1-418">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-418">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="7e8c1-419">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="7e8c1-419">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="7e8c1-420">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-420">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="7e8c1-421">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-421">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="7e8c1-422">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-422">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="7e8c1-423">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-423">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="7e8c1-424">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-424">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="7e8c1-425">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-425">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="7e8c1-426">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-426">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="7e8c1-427">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-427">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="7e8c1-428">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-428">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="7e8c1-429">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-429">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="7e8c1-430">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-430">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="7e8c1-431">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-431">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="7e8c1-432">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-432">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="7e8c1-433">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-433">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="7e8c1-434">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-434">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="7e8c1-435">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-435">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="7e8c1-436">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-436">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="7e8c1-437">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-437">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="7e8c1-438">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="7e8c1-438">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="7e8c1-439">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-439">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="7e8c1-440">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="7e8c1-440">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="7e8c1-441">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="7e8c1-441">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="7e8c1-442">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="7e8c1-442">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="7e8c1-443">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="7e8c1-443">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="7e8c1-444">Profil</span><span class="sxs-lookup"><span data-stu-id="7e8c1-444">Profile</span></span>

* <span data-ttu-id="7e8c1-445">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-445">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="7e8c1-446">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="7e8c1-446">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="7e8c1-447">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="7e8c1-447">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="7e8c1-448">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="7e8c1-448">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="7e8c1-449">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="7e8c1-449">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="7e8c1-450">RDBMS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-450">RDBMS</span></span>

* <span data-ttu-id="7e8c1-451">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-451">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="7e8c1-452">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-452">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="7e8c1-453">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-453">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="7e8c1-454">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-454">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="7e8c1-455">Resurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-455">Resource</span></span>

* <span data-ttu-id="7e8c1-456">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-456">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="7e8c1-457">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="7e8c1-457">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="7e8c1-458">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-458">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="7e8c1-459">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-459">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="7e8c1-460">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-460">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="7e8c1-461">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-461">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="7e8c1-462">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-462">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="7e8c1-463">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="7e8c1-463">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="7e8c1-464">Roll</span><span class="sxs-lookup"><span data-stu-id="7e8c1-464">Role</span></span>

* <span data-ttu-id="7e8c1-465">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-465">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="7e8c1-466">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-466">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="7e8c1-467">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="7e8c1-467">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="7e8c1-468">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="7e8c1-468">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="7e8c1-469">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-469">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="7e8c1-470">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7e8c1-470">Service Fabric</span></span>
* <span data-ttu-id="7e8c1-471">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-471">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="7e8c1-472">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-472">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="7e8c1-473">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-473">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="7e8c1-474">SQL</span><span class="sxs-lookup"><span data-stu-id="7e8c1-474">SQL</span></span>

* <span data-ttu-id="7e8c1-475">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7e8c1-475">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="7e8c1-476">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="7e8c1-476">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="7e8c1-477">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="7e8c1-477">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-478">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-478">Storage</span></span>

* <span data-ttu-id="7e8c1-479">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-479">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="7e8c1-480">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-480">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="7e8c1-481">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-481">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="7e8c1-482">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-482">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="7e8c1-483">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-483">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="7e8c1-484">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-484">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-485">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-485">VM</span></span>

* <span data-ttu-id="7e8c1-486">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="7e8c1-486">Support configuring nsg</span></span>
* <span data-ttu-id="7e8c1-487">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-487">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="7e8c1-488">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="7e8c1-488">Support managed service identities</span></span>
* <span data-ttu-id="7e8c1-489">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-489">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="7e8c1-490">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="7e8c1-490">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="7e8c1-491">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-491">May 10, 2017</span></span>

<span data-ttu-id="7e8c1-492">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="7e8c1-492">Version 2.0.6</span></span>

* <span data-ttu-id="7e8c1-493">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="7e8c1-493">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="7e8c1-494">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-494">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="7e8c1-495">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-495">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="7e8c1-496">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-496">Include Cognitive Services module.</span></span>
* <span data-ttu-id="7e8c1-497">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-497">Include Service Fabric module.</span></span>
* <span data-ttu-id="7e8c1-498">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="7e8c1-498">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="7e8c1-499">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-499">Add support for CDN commands.</span></span>
* <span data-ttu-id="7e8c1-500">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-500">Remove Container module.</span></span>
* <span data-ttu-id="7e8c1-501">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-501">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="7e8c1-502">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-502">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="7e8c1-503">Kärna</span><span class="sxs-lookup"><span data-stu-id="7e8c1-503">Core</span></span>

* <span data-ttu-id="7e8c1-504">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-504">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="7e8c1-505">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-505">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="7e8c1-506">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-506">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="7e8c1-507">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-507">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="7e8c1-508">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-508">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="7e8c1-509">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-509">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="7e8c1-510">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-510">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="7e8c1-511">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-511">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="7e8c1-512">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-512">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="7e8c1-513">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="7e8c1-513">core: Improved performance</span></span>
* <span data-ttu-id="7e8c1-514">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="7e8c1-514">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="7e8c1-515">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="7e8c1-515">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="7e8c1-516">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-516">ACS</span></span>

* <span data-ttu-id="7e8c1-517">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-517">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="7e8c1-518">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="7e8c1-518">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="7e8c1-519">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-519">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="7e8c1-520">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-520">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="7e8c1-521">AppService</span><span class="sxs-lookup"><span data-stu-id="7e8c1-521">AppService</span></span>

* <span data-ttu-id="7e8c1-522">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-522">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="7e8c1-523">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="7e8c1-523">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="7e8c1-524">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-524">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="7e8c1-525">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="7e8c1-525">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="7e8c1-526">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="7e8c1-526">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="7e8c1-527">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-527">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="7e8c1-528">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="7e8c1-528">support slot swap with preview</span></span>
* <span data-ttu-id="7e8c1-529">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-529">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="7e8c1-530">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-530">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="7e8c1-531">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="7e8c1-531">CosmosDB</span></span>

* <span data-ttu-id="7e8c1-532">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-532">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="7e8c1-533">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="7e8c1-533">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="7e8c1-534">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="7e8c1-534">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="7e8c1-535">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="7e8c1-535">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="7e8c1-536">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="7e8c1-536">Data Lake Analytics</span></span>

* <span data-ttu-id="7e8c1-537">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-537">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="7e8c1-538">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-538">Add support for new catalog item type: package.</span></span> <span data-ttu-id="7e8c1-539">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-539">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="7e8c1-540">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="7e8c1-540">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="7e8c1-541">Tabell</span><span class="sxs-lookup"><span data-stu-id="7e8c1-541">Table</span></span>
  * <span data-ttu-id="7e8c1-542">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="7e8c1-542">Table valued function</span></span>
  * <span data-ttu-id="7e8c1-543">Visa</span><span class="sxs-lookup"><span data-stu-id="7e8c1-543">View</span></span>
  * <span data-ttu-id="7e8c1-544">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-544">Table Statistics.</span></span> <span data-ttu-id="7e8c1-545">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-545">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="7e8c1-546">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7e8c1-546">Data Lake Store</span></span>

* <span data-ttu-id="7e8c1-547">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-547">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="7e8c1-548">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-548">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="7e8c1-549">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-549">missed help for access show.</span></span> <span data-ttu-id="7e8c1-550">läggs till.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-550">adding it.</span></span> <span data-ttu-id="7e8c1-551">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-551">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="7e8c1-552">Hitta</span><span class="sxs-lookup"><span data-stu-id="7e8c1-552">Find</span></span>

* <span data-ttu-id="7e8c1-553">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="7e8c1-553">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="7e8c1-554">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e8c1-554">KeyVault</span></span>

* <span data-ttu-id="7e8c1-555">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="7e8c1-555">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="7e8c1-556">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-556">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="7e8c1-557">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="7e8c1-557">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="7e8c1-558">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-558">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="7e8c1-559">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-559">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="7e8c1-560">Labb</span><span class="sxs-lookup"><span data-stu-id="7e8c1-560">Lab</span></span>

* <span data-ttu-id="7e8c1-561">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-561">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="7e8c1-562">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-562">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="7e8c1-563">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-563">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="7e8c1-564">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-564">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="7e8c1-565">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-565">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="7e8c1-566">Övervaka</span><span class="sxs-lookup"><span data-stu-id="7e8c1-566">Monitor</span></span>

* <span data-ttu-id="7e8c1-567">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-567">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="7e8c1-568">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-568">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="7e8c1-569">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-569">Network</span></span>

* <span data-ttu-id="7e8c1-570">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-570">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="7e8c1-571">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-571">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="7e8c1-572">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-572">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="7e8c1-573">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-573">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="7e8c1-574">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-574">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="7e8c1-575">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-575">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="7e8c1-576">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-576">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="7e8c1-577">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-577">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="7e8c1-578">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-578">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="7e8c1-579">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="7e8c1-579">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="7e8c1-580">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-580">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="7e8c1-581">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="7e8c1-581">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="7e8c1-582">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-582">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="7e8c1-583">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-583">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="7e8c1-584">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-584">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="7e8c1-585">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-585">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="7e8c1-586">Profil</span><span class="sxs-lookup"><span data-stu-id="7e8c1-586">Profile</span></span>

* <span data-ttu-id="7e8c1-587">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-587">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="7e8c1-588">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-588">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="7e8c1-589">Redis</span><span class="sxs-lookup"><span data-stu-id="7e8c1-589">Redis</span></span>

* <span data-ttu-id="7e8c1-590">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="7e8c1-590">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="7e8c1-591">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-591">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="7e8c1-592">Resurs</span><span class="sxs-lookup"><span data-stu-id="7e8c1-592">Resource</span></span>

* <span data-ttu-id="7e8c1-593">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-593">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="7e8c1-594">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-594">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="7e8c1-595">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-595">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="7e8c1-596">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-596">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="7e8c1-597">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-597">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="7e8c1-598">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-598">Add docs for az lock update.</span></span> <span data-ttu-id="7e8c1-599">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-599">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="7e8c1-600">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-600">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="7e8c1-601">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-601">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="7e8c1-602">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-602">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="7e8c1-603">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-603">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="7e8c1-604">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-604">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="7e8c1-605">Roll</span><span class="sxs-lookup"><span data-stu-id="7e8c1-605">Role</span></span>

* <span data-ttu-id="7e8c1-606">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-606">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="7e8c1-607">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-607">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="7e8c1-608">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-608">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="7e8c1-609">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="7e8c1-609">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="7e8c1-610">SQL</span><span class="sxs-lookup"><span data-stu-id="7e8c1-610">SQL</span></span>

* <span data-ttu-id="7e8c1-611">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-611">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="7e8c1-612">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-612">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="7e8c1-613">Lagring</span><span class="sxs-lookup"><span data-stu-id="7e8c1-613">Storage</span></span>

* <span data-ttu-id="7e8c1-614">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-614">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="7e8c1-615">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="7e8c1-615">Add support for incremental blob copy</span></span>
* <span data-ttu-id="7e8c1-616">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="7e8c1-616">Add support for large block blob upload</span></span>
* <span data-ttu-id="7e8c1-617">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="7e8c1-617">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-618">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-618">VM</span></span>

* <span data-ttu-id="7e8c1-619">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="7e8c1-619">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="7e8c1-620">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-620">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="7e8c1-621">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="7e8c1-621">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="7e8c1-622">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-622">az vm/vmss disk</span></span>
  3. <span data-ttu-id="7e8c1-623">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="7e8c1-623">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="7e8c1-624">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="7e8c1-624">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="7e8c1-625">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-625">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="7e8c1-626">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-626">April 3, 2017</span></span>

<span data-ttu-id="7e8c1-627">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="7e8c1-627">Version 2.0.2</span></span>

<span data-ttu-id="7e8c1-628">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-628">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="7e8c1-629">Kärna</span><span class="sxs-lookup"><span data-stu-id="7e8c1-629">Core</span></span>

* <span data-ttu-id="7e8c1-630">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-630">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="7e8c1-631">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-631">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="7e8c1-632">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-632">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="7e8c1-633">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-633">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="7e8c1-634">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-634">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="7e8c1-635">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-635">Add prompting for missing template parameters.</span></span> <span data-ttu-id="7e8c1-636">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-636">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="7e8c1-637">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="7e8c1-637">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="7e8c1-638">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="7e8c1-638">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="7e8c1-639">ACS</span><span class="sxs-lookup"><span data-stu-id="7e8c1-639">ACS</span></span>

* <span data-ttu-id="7e8c1-640">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-640">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="7e8c1-641">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-641">Add support for ssh key password prompting.</span></span> <span data-ttu-id="7e8c1-642">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-642">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="7e8c1-643">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-643">Add support for windows clusters.</span></span> <span data-ttu-id="7e8c1-644">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-644">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="7e8c1-645">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-645">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="7e8c1-646">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-646">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="7e8c1-647">AppService</span><span class="sxs-lookup"><span data-stu-id="7e8c1-647">AppService</span></span>

* <span data-ttu-id="7e8c1-648">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-648">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="7e8c1-649">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-649">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="7e8c1-650">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-650">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="7e8c1-651">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-651">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="7e8c1-652">DataLake</span><span class="sxs-lookup"><span data-stu-id="7e8c1-652">DataLake</span></span>

* <span data-ttu-id="7e8c1-653">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-653">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="7e8c1-654">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-654">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="7e8c1-655">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="7e8c1-655">DocuemntDB</span></span>

* <span data-ttu-id="7e8c1-656">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-656">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="7e8c1-657">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="7e8c1-657">VM</span></span>

* <span data-ttu-id="7e8c1-658">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-658">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="7e8c1-659">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-659">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="7e8c1-660">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-660">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="7e8c1-661">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-661">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="7e8c1-662">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-662">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="7e8c1-663">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-663">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="7e8c1-664">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="7e8c1-664">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="7e8c1-665">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="7e8c1-665">February 27, 2017</span></span>

<span data-ttu-id="7e8c1-666">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="7e8c1-666">Version 2.0.0</span></span>

<span data-ttu-id="7e8c1-667">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="7e8c1-667">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="7e8c1-668">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-668">General availability applies to these command modules:</span></span>
- <span data-ttu-id="7e8c1-669">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-669">Container Service (acs)</span></span>
- <span data-ttu-id="7e8c1-670">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-670">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="7e8c1-671">Nätverk</span><span class="sxs-lookup"><span data-stu-id="7e8c1-671">Networking</span></span>
- <span data-ttu-id="7e8c1-672">Storage</span><span class="sxs-lookup"><span data-stu-id="7e8c1-672">Storage</span></span>

<span data-ttu-id="7e8c1-673">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-673">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="7e8c1-674">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="7e8c1-674">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="7e8c1-675">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-675">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="7e8c1-676">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-676">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="7e8c1-677">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-677">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="7e8c1-678">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-678">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="7e8c1-679">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-679">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="7e8c1-680">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-680">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="7e8c1-681">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-681">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="7e8c1-682">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="7e8c1-682">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="7e8c1-683">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="7e8c1-683">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="7e8c1-684">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="7e8c1-684">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="7e8c1-685">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7e8c1-685">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="7e8c1-686">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="7e8c1-686">Provide feedback from the command line with the `az feedback` command.</span></span>

