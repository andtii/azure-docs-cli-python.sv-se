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
ms.openlocfilehash: 429b099dabd27d9356e88791f955ec52acd2a5f9
ms.sourcegitcommit: 9b36c15dc0e10024e23b8018604f5ef63c025de1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/24/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="24203-104">Viktig information om Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="24203-104">Azure CLI 2.0 release notes</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="24203-105">24 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="24203-105">October 24, 2017</span></span>

<span data-ttu-id="24203-106">Version 2.0.20</span><span class="sxs-lookup"><span data-stu-id="24203-106">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="24203-107">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-107">Core</span></span>

* <span data-ttu-id="24203-108">`2017-03-09-profile` har uppdaterats för att använda `MGMT_STORAGE`, API-version `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="24203-108">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="24203-109">ACR</span><span class="sxs-lookup"><span data-stu-id="24203-109">ACR</span></span>

* <span data-ttu-id="24203-110">Resurshanteringen har uppdaterats för att peka på API-version `2017-10-01`</span><span class="sxs-lookup"><span data-stu-id="24203-110">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="24203-111">SKU:n för BYOS ("bring your own storage") har ändrats till klassisk</span><span class="sxs-lookup"><span data-stu-id="24203-111">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="24203-112">Register-SKU:erna har bytt namn till Basic, Standard och Premium</span><span class="sxs-lookup"><span data-stu-id="24203-112">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="24203-113">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-113">ACS</span></span>

* <span data-ttu-id="24203-114">[FÖRHANDSVERSION] `az aks`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-114">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="24203-115">Kubernetes `get-credentials` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-115">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-116">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-116">Appservice</span></span>

* <span data-ttu-id="24203-117">Problem med att nedladdade `webapp`-loggar kunde vara ogiltiga har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-117">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="24203-118">Komponent</span><span class="sxs-lookup"><span data-stu-id="24203-118">Component</span></span>

* <span data-ttu-id="24203-119">Ett tydligare utfasningsmeddelande har lagts till för alla installationsprogram och bekräftelsefrågor</span><span class="sxs-lookup"><span data-stu-id="24203-119">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="24203-120">Övervaka</span><span class="sxs-lookup"><span data-stu-id="24203-120">Monitor</span></span>

* <span data-ttu-id="24203-121">`action-group`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-121">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="24203-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-122">Resource</span></span>

* <span data-ttu-id="24203-123">Inkompatibilitet med den senaste versionen av msrest-beroende i `group export` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-123">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="24203-124">`policy assignment create` har åtgärdats så att det fungerar med inbyggda principdefinitioner och principuppsättningsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="24203-124">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="24203-125">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-125">VM</span></span>

* <span data-ttu-id="24203-126">Argumentet `--accelerated-networking` har lagts till för `vmss create`</span><span class="sxs-lookup"><span data-stu-id="24203-126">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="24203-127">9 oktober 2017</span><span class="sxs-lookup"><span data-stu-id="24203-127">October 9, 2017</span></span>

<span data-ttu-id="24203-128">Version 2.0.19</span><span class="sxs-lookup"><span data-stu-id="24203-128">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="24203-129">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-129">Core</span></span>

* <span data-ttu-id="24203-130">Hantering av URL:er för ADFS-utfärdare med ett avslutande snedstreck till Azure Stack har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-130">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-131">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-131">Appservice</span></span>

* <span data-ttu-id="24203-132">Generisk uppdatering med nytt kommando `webapp update` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-132">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="24203-133">Batch</span><span class="sxs-lookup"><span data-stu-id="24203-133">Batch</span></span>

* <span data-ttu-id="24203-134">Har uppdaterats till Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="24203-134">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="24203-135">Alternativet `--image` har uppdaterats för att VirtualMachineConfiguration ska ha stöd för ARM-avbildningsreferenser utöver publish:offer:sku:version</span><span class="sxs-lookup"><span data-stu-id="24203-135">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="24203-136">Stöd för den nya CLI-tilläggsmodellen för kommandon för batchtillägg har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-136">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="24203-137">Batch-stöd från komponentmodellen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="24203-137">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="24203-138">Batchai</span><span class="sxs-lookup"><span data-stu-id="24203-138">Batchai</span></span>

* <span data-ttu-id="24203-139">Första versionen av Batch AI-modulen</span><span class="sxs-lookup"><span data-stu-id="24203-139">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="24203-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="24203-140">Keyvault</span></span>

* <span data-ttu-id="24203-141">Autentiseringsproblem med Key Vault har åtgärdats vid användning av ADFS på Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="24203-141">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="24203-142">(#4448)</span><span class="sxs-lookup"><span data-stu-id="24203-142">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="24203-143">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-143">Network</span></span>

* <span data-ttu-id="24203-144">Argumentet `--server` för `application-gateway address-pool create` har ändrats så att det är frivilligt, vilket möjliggör tomma adresspooler</span><span class="sxs-lookup"><span data-stu-id="24203-144">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="24203-145">`traffic-manager` har uppdaterats så att de senaste funktionerna stöds</span><span class="sxs-lookup"><span data-stu-id="24203-145">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="24203-146">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-146">Resource</span></span>

* <span data-ttu-id="24203-147">Stöd har lagts till för alternativ för `--resource-group/-g` för resursgruppnamnet till `group`</span><span class="sxs-lookup"><span data-stu-id="24203-147">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="24203-148">Kommandon har lagts till för `account lock` så att de fungerar med lås på prenumerationsnivån</span><span class="sxs-lookup"><span data-stu-id="24203-148">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="24203-149">Kommandon har lagts till för `group lock` så att de fungerar med lås på gruppnivån</span><span class="sxs-lookup"><span data-stu-id="24203-149">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="24203-150">Kommandon har lagts till för `resource lock` så att de fungerar med lås på resursnivån</span><span class="sxs-lookup"><span data-stu-id="24203-150">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="24203-151">SQL</span><span class="sxs-lookup"><span data-stu-id="24203-151">Sql</span></span>

* <span data-ttu-id="24203-152">Stöd har lagts till för transparent datakryptering med SQL och transparent datakryptering med Bring Your Own Key</span><span class="sxs-lookup"><span data-stu-id="24203-152">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="24203-153">Kommandot `db list-deleted` och parametern `db restore --deleted-time` har lagts till, vilket gör att det går att hitta och återställa borttagna databaser</span><span class="sxs-lookup"><span data-stu-id="24203-153">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="24203-154">`db op list` och `db op cancel` har lagts till, vilket gör det möjligt att lista och avbryta åtgärder som pågår på databasen</span><span class="sxs-lookup"><span data-stu-id="24203-154">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="24203-155">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-155">Storage</span></span>

* <span data-ttu-id="24203-156">Stöd har lagts till för ögonblicksbild av filresurs</span><span class="sxs-lookup"><span data-stu-id="24203-156">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="24203-157">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-157">Vm</span></span>

* <span data-ttu-id="24203-158">Ett bugg har åtgärdats i `vm show` där användning av `-d` orsakade en krasch på privata IP-adresser som saknas</span><span class="sxs-lookup"><span data-stu-id="24203-158">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="24203-159">[FÖRHANDSVERSION] Stöd har lagts till för löpande uppgradering till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="24203-159">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="24203-160">Stöd har lagts till för att uppdatera krypteringsinställningar med `vm encryption enable`</span><span class="sxs-lookup"><span data-stu-id="24203-160">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="24203-161">Parametern `--os-disk-size-gb` har lagts till i `vm create`</span><span class="sxs-lookup"><span data-stu-id="24203-161">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="24203-162">Parametern `--license-type` har lagts till för Windows till `vmss create`</span><span class="sxs-lookup"><span data-stu-id="24203-162">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="24203-163">22 september 2017</span><span class="sxs-lookup"><span data-stu-id="24203-163">September 22, 2017</span></span>

<span data-ttu-id="24203-164">Version 2.0.18</span><span class="sxs-lookup"><span data-stu-id="24203-164">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="24203-165">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-165">Resource</span></span>

* <span data-ttu-id="24203-166">Stöd har lagts till för att visa inbyggda principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="24203-166">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="24203-167">Stödlägesparametern har lagts till för att skapa principdefinitioner</span><span class="sxs-lookup"><span data-stu-id="24203-167">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="24203-168">Stöd har lagts till för UI-definitioner och mallar till `managedapp definition create`</span><span class="sxs-lookup"><span data-stu-id="24203-168">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="24203-169">[VIKTIG ÄNDRING] Resurstypen `managedapp` har ändrats från `appliances` till `applications` och `applianceDefinitions` till `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="24203-169">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="24203-170">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-170">Network</span></span>

* <span data-ttu-id="24203-171">Stöd har lagts till för tillgänglighetszonen till underkommandon `network lb` och `network public-ip`</span><span class="sxs-lookup"><span data-stu-id="24203-171">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="24203-172">Stöd har lagts till för IPv6 Microsoft-peering till `express-route`</span><span class="sxs-lookup"><span data-stu-id="24203-172">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="24203-173">Gruppkommandon för `asg`-programsäkerhet har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-173">Added `asg` application security group commands</span></span>
* <span data-ttu-id="24203-174">Argumentet `--application-security-groups` har lagts till för `nic [create|ip-config create|ip-config update]`</span><span class="sxs-lookup"><span data-stu-id="24203-174">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="24203-175">Argumenten `--source-asgs` och `--destination-asgs` har lagts till för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="24203-175">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="24203-176">Argumenten `--ddos-protection` och `--vm-protection` har lagts till för `vnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="24203-176">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="24203-177">`network [vnet-gateway|vpn-client|show-url]`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-177">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="24203-178">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-178">Storage</span></span>

* <span data-ttu-id="24203-179">Problem har åtgärdats där `storage account network-rule`-kommandon kan misslyckas efter uppdatering av SDK</span><span class="sxs-lookup"><span data-stu-id="24203-179">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="24203-180">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="24203-180">Eventgrid</span></span>

* <span data-ttu-id="24203-181">Azure Event Grid Python SDK har uppdaterats för att använda en senare API-version "2017-09-15-preview"</span><span class="sxs-lookup"><span data-stu-id="24203-181">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="24203-182">SQL</span><span class="sxs-lookup"><span data-stu-id="24203-182">SQL</span></span>

* <span data-ttu-id="24203-183">Argumentet `sql server list` för `--resource-group` har ändrats så att det är valfritt.</span><span class="sxs-lookup"><span data-stu-id="24203-183">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="24203-184">Om inget anges returneras alla sql-servrar i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="24203-184">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="24203-185">Parametern `--no-wait` har lagts till för `db [create|copy|restore|update|replica create|create|update]` och `dw [create|update]`</span><span class="sxs-lookup"><span data-stu-id="24203-185">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="24203-186">KeyVault</span><span class="sxs-lookup"><span data-stu-id="24203-186">Keyvault</span></span>

* <span data-ttu-id="24203-187">Stöd har lagts till för Keyvault-kommandon bakom en proxy</span><span class="sxs-lookup"><span data-stu-id="24203-187">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="24203-188">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-188">VM</span></span>

* <span data-ttu-id="24203-189">Stöd har lagts till för tillgänglighetszon till `[vm|vmss|disk] create`</span><span class="sxs-lookup"><span data-stu-id="24203-189">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="24203-190">Problem har åtgärdats där användning av `--app-gateway ID` med `vmss create` kunde orsaka fel</span><span class="sxs-lookup"><span data-stu-id="24203-190">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="24203-191">Argumentet `--asgs` har lagts till för `vm create`</span><span class="sxs-lookup"><span data-stu-id="24203-191">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="24203-192">Stöd har lagts till för att köra kommandon på virtuella datorer med `vm run-command`</span><span class="sxs-lookup"><span data-stu-id="24203-192">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="24203-193">[FÖRHANDSVERSION] Stöd har lagts till för VMSS-diskkryptering med `vmss encryption`</span><span class="sxs-lookup"><span data-stu-id="24203-193">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="24203-194">Stöd har lagts till för att utföra underhåll på virtuella datorer med `vm perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="24203-194">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="24203-195">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-195">ACS</span></span>

* <span data-ttu-id="24203-196">[FÖRHANDSVERSION] Argumentet `--orchestrator-release` har lagts till i `acs create` för ACS-förhandsversionsregioner</span><span class="sxs-lookup"><span data-stu-id="24203-196">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-197">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-197">Appservice</span></span>

* <span data-ttu-id="24203-198">Möjlighet att uppdatera och visa autentiseringsinställningar med `webapp auth [update|show]` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-198">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="24203-199">Säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="24203-199">Backup</span></span>

* <span data-ttu-id="24203-200">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="24203-200">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="24203-201">11 september 2017</span><span class="sxs-lookup"><span data-stu-id="24203-201">September 11, 2017</span></span>

<span data-ttu-id="24203-202">Version 2.0.17</span><span class="sxs-lookup"><span data-stu-id="24203-202">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="24203-203">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-203">Core</span></span>

* <span data-ttu-id="24203-204">Kommandomodulen kan ange eget korrelations-ID i telemetri</span><span class="sxs-lookup"><span data-stu-id="24203-204">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="24203-205">Åtgärdat JSON-dumpproblem när telemetri är angivet till diagnostikläge</span><span class="sxs-lookup"><span data-stu-id="24203-205">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="24203-206">Acs</span><span class="sxs-lookup"><span data-stu-id="24203-206">Acs</span></span>

* <span data-ttu-id="24203-207">Kommandot `acs list-locations` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-207">Added `acs list-locations` command</span></span>
* <span data-ttu-id="24203-208">Fick `ssh-key-file` att leverera förväntat standardvärde</span><span class="sxs-lookup"><span data-stu-id="24203-208">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-209">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-209">Appservice</span></span>

* <span data-ttu-id="24203-210">Möjlighet att skapa en webbapp i en annan resursgrupp än den som hör till den aktiva tjänstens plan har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-210">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="24203-211">CDN</span><span class="sxs-lookup"><span data-stu-id="24203-211">CDN</span></span>

* <span data-ttu-id="24203-212">"CustomDomain is not interable"-bugg för `cdn custom-domain create` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="24203-212">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="24203-213">Anknytning</span><span class="sxs-lookup"><span data-stu-id="24203-213">Extension</span></span>

* <span data-ttu-id="24203-214">Första versionen.</span><span class="sxs-lookup"><span data-stu-id="24203-214">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="24203-215">KeyVault</span><span class="sxs-lookup"><span data-stu-id="24203-215">Keyvault</span></span>

* <span data-ttu-id="24203-216">Problem där behörigheter var skifteslägeskänsliga för `keyvault set-policy` har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="24203-216">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="24203-217">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-217">Network</span></span>

* <span data-ttu-id="24203-218">`vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="24203-218">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="24203-219">Namn på `--private-access-services`-argument har bytts till `--service-endpoints` för `vnet subnet create/update`</span><span class="sxs-lookup"><span data-stu-id="24203-219">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="24203-220">Stöd för flera IP- och portintervall har lagts till för `nsg rule create/update`</span><span class="sxs-lookup"><span data-stu-id="24203-220">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="24203-221">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="24203-221">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="24203-222">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="24203-222">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="24203-223">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-223">Resource</span></span>

* <span data-ttu-id="24203-224">Tillåt att definitioner för resursprincipparametern anges i `policy definition create` och `policy definition update`</span><span class="sxs-lookup"><span data-stu-id="24203-224">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="24203-225">Tillåt att parametervärden anges för `policy assignment create`</span><span class="sxs-lookup"><span data-stu-id="24203-225">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="24203-226">Tillåt att JSON eller fil för alla parametrar anges</span><span class="sxs-lookup"><span data-stu-id="24203-226">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="24203-227">API-versionen har utökats</span><span class="sxs-lookup"><span data-stu-id="24203-227">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="24203-228">SQL</span><span class="sxs-lookup"><span data-stu-id="24203-228">SQL</span></span>

* <span data-ttu-id="24203-229">`sql server vnet-rule`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-229">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="24203-230">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-230">VM</span></span>

* <span data-ttu-id="24203-231">Åtgärdat: Tilldela inte åtkomst om inte `--scope` har angetts</span><span class="sxs-lookup"><span data-stu-id="24203-231">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="24203-232">Åtgärdat: Använd samma tilläggsnamn som portalen gör</span><span class="sxs-lookup"><span data-stu-id="24203-232">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="24203-233">`subscription` har tagits bort från `[vm|vmss] create`-utmatningen</span><span class="sxs-lookup"><span data-stu-id="24203-233">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="24203-234">Åtgärdat: SKU:n för `[vm|vmss] create`-lagring tillämpas inte på datadiskar med en avbildning</span><span class="sxs-lookup"><span data-stu-id="24203-234">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="24203-235">Åtgärdat: `vm format-secret --secrets` accepterade inte ID:n som skildes åt med ny rad</span><span class="sxs-lookup"><span data-stu-id="24203-235">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="24203-236">31 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="24203-236">August 31, 2017</span></span>

<span data-ttu-id="24203-237">Version 2.0.16</span><span class="sxs-lookup"><span data-stu-id="24203-237">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="24203-238">KeyVault</span><span class="sxs-lookup"><span data-stu-id="24203-238">Keyvault</span></span>

* <span data-ttu-id="24203-239">Bugg vid försök att automatiskt lösa hemlig kodning med `secret download` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-239">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="24203-240">Sf</span><span class="sxs-lookup"><span data-stu-id="24203-240">Sf</span></span>

* <span data-ttu-id="24203-241">Avveckla alla kommandon till förmån för Service Fabric CLI (sfctl)</span><span class="sxs-lookup"><span data-stu-id="24203-241">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="24203-242">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-242">Storage</span></span>

* <span data-ttu-id="24203-243">Problem där lagringskonton inte kunde skapas i regioner som inte stöder NetworkACLs-funktionen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-243">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="24203-244">Fastställ innehållstyp och innehållskodning under blob- och filuppladdning om varken innehållstyp eller innehållskodning har angetts</span><span class="sxs-lookup"><span data-stu-id="24203-244">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="24203-245">28 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="24203-245">August 28, 2017</span></span>

<span data-ttu-id="24203-246">Version 2.0.15</span><span class="sxs-lookup"><span data-stu-id="24203-246">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="24203-247">CLI</span><span class="sxs-lookup"><span data-stu-id="24203-247">CLI</span></span>

* <span data-ttu-id="24203-248">Tillkommen juridisk information för `--version`.</span><span class="sxs-lookup"><span data-stu-id="24203-248">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="24203-249">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-249">ACS</span></span>

* <span data-ttu-id="24203-250">Regioner i förhandsversionen har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="24203-250">Corrected preview regions.</span></span>
* <span data-ttu-id="24203-251">`dns_name_prefix`-standardprefixet har formaterats korrekt.</span><span class="sxs-lookup"><span data-stu-id="24203-251">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="24203-252">Utdata från acs-kommandot har optimerats.</span><span class="sxs-lookup"><span data-stu-id="24203-252">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-253">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-253">Appservice</span></span>

* <span data-ttu-id="24203-254">[VIKTIG ÄNDRING] Inkonsekvenser i utdata från `az webapp config appsettings [delete|set]` har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-254">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="24203-255">Ett nytt alias (`-i`) har lagts till för `az webapp config container set --docker-custom-image-name`</span><span class="sxs-lookup"><span data-stu-id="24203-255">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="24203-256">`az webapp log show` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="24203-256">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="24203-257">Nya argument har gjorts tillgängliga från `az webapp delete` så att App Service-planer, mått eller DNS-registreringar bevaras</span><span class="sxs-lookup"><span data-stu-id="24203-257">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="24203-258">Åtgärdat: Platsinställningar identifieras korrekt</span><span class="sxs-lookup"><span data-stu-id="24203-258">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="24203-259">IoT</span><span class="sxs-lookup"><span data-stu-id="24203-259">IoT</span></span>

* <span data-ttu-id="24203-260">Åtgärdat (#3934): Befintliga principer rensas inte längre när nya principer skapas</span><span class="sxs-lookup"><span data-stu-id="24203-260">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="24203-261">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-261">Network</span></span>

* <span data-ttu-id="24203-262">[VIKTIG ÄNDRING] `vnet list-private-access-services` har bytt namn till `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="24203-262">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="24203-263">[VIKTIG ÄNDRING] Alternativet `--private-access-services` har bytt namn till `--service-endpoints` för `vnet subnet [create|update]`</span><span class="sxs-lookup"><span data-stu-id="24203-263">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="24203-264">Stöd har lagts till för flera IP- och portintervall för `nsg rule [create|update]`</span><span class="sxs-lookup"><span data-stu-id="24203-264">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="24203-265">SKU-stöd har lagts till för `lb create`</span><span class="sxs-lookup"><span data-stu-id="24203-265">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="24203-266">SKU-stöd har lagts till för `public-ip create`</span><span class="sxs-lookup"><span data-stu-id="24203-266">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="24203-267">Profil</span><span class="sxs-lookup"><span data-stu-id="24203-267">Profile</span></span>

* <span data-ttu-id="24203-268">`--msi` och `--msi-port` har gjorts tillgängliga för inloggning med identiteten för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-268">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="24203-269">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="24203-269">Service Fabric</span></span>

* <span data-ttu-id="24203-270">Förhandsversion</span><span class="sxs-lookup"><span data-stu-id="24203-270">Preview release</span></span>
* <span data-ttu-id="24203-271">Förenklade användar- och lösenordsregler för registrering via kommando</span><span class="sxs-lookup"><span data-stu-id="24203-271">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="24203-272">Lösenordsprompten för användare även efter att parametern har angetts har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-272">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="24203-273">Stöd har lagts till för tomma `registry_cred`</span><span class="sxs-lookup"><span data-stu-id="24203-273">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="24203-274">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-274">Storage</span></span>

* <span data-ttu-id="24203-275">Stöd har lagts till för att ställa in blobbnivå</span><span class="sxs-lookup"><span data-stu-id="24203-275">Enabled setting blob tier</span></span>
* <span data-ttu-id="24203-276">Argumenten `--bypass` och `--default-action` har lagts till för `storage account [create|update]` för att ge stöd för händelsedirigering nedåt med tjänsten</span><span class="sxs-lookup"><span data-stu-id="24203-276">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="24203-277">Nya kommandon har gjorts tillgängliga för att lägga till VNET-regler och IP-baserade regler för `storage account network-rule`</span><span class="sxs-lookup"><span data-stu-id="24203-277">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="24203-278">Stöd har lagts till för tjänstkryptering med kundhanterade nycklar</span><span class="sxs-lookup"><span data-stu-id="24203-278">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="24203-279">[VIKTIG ÄNDRING] Alternativet `--encryption` har bytt namn till `--encryption-services` för kommandot `az storage account create and az storage account update`</span><span class="sxs-lookup"><span data-stu-id="24203-279">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="24203-280">Åtgärdat (#4220): `az storage account update encryption` – matchningsfel i syntax</span><span class="sxs-lookup"><span data-stu-id="24203-280">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="24203-281">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-281">VM</span></span>

* <span data-ttu-id="24203-282">Ett problem har åtgärdats som gjorde att extra, felaktig information visades för `vmss get-instance-view` när det användes med `--instance-id *`</span><span class="sxs-lookup"><span data-stu-id="24203-282">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="24203-283">Stöd har lagts till för `--lb-sku` för `vmss create`:</span><span class="sxs-lookup"><span data-stu-id="24203-283">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="24203-284">Namn på personer har tagits bort från svartlistan för administratörsnamn för `[vm|vmss] create`</span><span class="sxs-lookup"><span data-stu-id="24203-284">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="24203-285">Ett problem har åtgärdats som gjorde att `[vm|vmss] create` returnerade ett fel om det inte gick att extrahera planinformation från en avbildning</span><span class="sxs-lookup"><span data-stu-id="24203-285">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="24203-286">Kraschar som inträffade när en vmms-skalningsuppsättning skapades med en intern LB har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-286">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="24203-287">Ett problem har åtgärdats som gjorde att `--no-wait`-argumentet inte fungerade med `vm availability-set create`</span><span class="sxs-lookup"><span data-stu-id="24203-287">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="24203-288">15 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="24203-288">August 15, 2017</span></span>

<span data-ttu-id="24203-289">Version 2.0.14</span><span class="sxs-lookup"><span data-stu-id="24203-289">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="24203-290">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-290">ACS</span></span>

* <span data-ttu-id="24203-291">sshMaster0-portnumret för kubernetes har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-291">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-292">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-292">Appservice</span></span>

* <span data-ttu-id="24203-293">Undantaget som genererades när en ny git-baserad Linux-webbapp skapades har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-293">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="24203-294">Event Grid</span><span class="sxs-lookup"><span data-stu-id="24203-294">Event Grid</span></span>

* <span data-ttu-id="24203-295">SDK-beroenden har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-295">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="24203-296">11 augusti 2017</span><span class="sxs-lookup"><span data-stu-id="24203-296">August 11, 2017</span></span>

<span data-ttu-id="24203-297">Version 2.0.13</span><span class="sxs-lookup"><span data-stu-id="24203-297">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="24203-298">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-298">ACS</span></span>

* <span data-ttu-id="24203-299">Fler regioner har lagts till för förhandsversionen</span><span class="sxs-lookup"><span data-stu-id="24203-299">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="24203-300">Batch</span><span class="sxs-lookup"><span data-stu-id="24203-300">Batch</span></span>

* <span data-ttu-id="24203-301">Uppdaterat till Batch SDK 3.1.0 och Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="24203-301">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="24203-302">Ett nytt kommando har lagts till för att visa antalet uppgifter för ett jobb</span><span class="sxs-lookup"><span data-stu-id="24203-302">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="24203-303">En bugg i bearbetningen av SAS-URL:er för resursfiler har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-303">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="24203-304">Nu har slutpunkten för ett Batch-konto stöd för ett valfritt ”https://” -prefix</span><span class="sxs-lookup"><span data-stu-id="24203-304">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="24203-305">Stöd har lagts till för att lägga till listor med fler än 100 uppgifter i ett jobb</span><span class="sxs-lookup"><span data-stu-id="24203-305">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="24203-306">Felsökningsloggning har lagts till för inläsning av kommandomodulen Extensions</span><span class="sxs-lookup"><span data-stu-id="24203-306">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="24203-307">Komponent</span><span class="sxs-lookup"><span data-stu-id="24203-307">Component</span></span>

* <span data-ttu-id="24203-308">En utfasningsvarning har lagts till för ”az component”-kommandon</span><span class="sxs-lookup"><span data-stu-id="24203-308">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="24203-309">Behållare</span><span class="sxs-lookup"><span data-stu-id="24203-309">Container</span></span>

* <span data-ttu-id="24203-310">`create`: Ett problem har åtgärdats som gjorde att likhetstecken inte tilläts inuti en miljövariabel</span><span class="sxs-lookup"><span data-stu-id="24203-310">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="24203-311">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="24203-311">Data Lake Store</span></span>

* <span data-ttu-id="24203-312">Stöd har lagts till för förloppskontroll</span><span class="sxs-lookup"><span data-stu-id="24203-312">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="24203-313">Event Grid</span><span class="sxs-lookup"><span data-stu-id="24203-313">Event Grid</span></span>

* <span data-ttu-id="24203-314">Första utgåvan</span><span class="sxs-lookup"><span data-stu-id="24203-314">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="24203-315">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-315">Network</span></span>

* <span data-ttu-id="24203-316">`lb`: Ett problem har åtgärdats som gjorde att vissa namn på underordnade resurser inte matchades korrekt när de utelämnades</span><span class="sxs-lookup"><span data-stu-id="24203-316">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="24203-317">`application-gateway {subresource} delete`: Ett problem har åtgärdats som gjorde att `--no-wait` inte hanterades</span><span class="sxs-lookup"><span data-stu-id="24203-317">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="24203-318">`application-gateway http-settings update`: Ett problem har åtgärdats som gjorde att det inte gick att inaktivera `--connection-draining-timeout`-molnet</span><span class="sxs-lookup"><span data-stu-id="24203-318">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="24203-319">Ett fel har åtgärdats som returnerade fel på grund av ett oväntat lösenordsargument för `sa_data_size_kilobyes` med `az network vpn-connection ipsec-policy add`</span><span class="sxs-lookup"><span data-stu-id="24203-319">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="24203-320">Profil</span><span class="sxs-lookup"><span data-stu-id="24203-320">Profile</span></span>

* <span data-ttu-id="24203-321">`account list`: `--refresh` har lagts till för att synkronisera de senaste prenumerationerna från servern</span><span class="sxs-lookup"><span data-stu-id="24203-321">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="24203-322">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-322">Storage</span></span>

* <span data-ttu-id="24203-323">Stöd har lagts till för uppdatering av lagringskonton med systemtilldelade identiteter</span><span class="sxs-lookup"><span data-stu-id="24203-323">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="24203-324">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-324">VM</span></span>

* <span data-ttu-id="24203-325">`availability-set`: Antalet feldomäner vid konvertering har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="24203-325">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="24203-326">Kommandot `list-skus` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="24203-326">Exposed `list-skus` command</span></span>
* <span data-ttu-id="24203-327">Stöd har lagts till för tilldelning av identiteter med eller utan rolltilldelningar</span><span class="sxs-lookup"><span data-stu-id="24203-327">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="24203-328">Använd lagrings-SKU när datadiskar ansluts</span><span class="sxs-lookup"><span data-stu-id="24203-328">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="24203-329">Förvalt OS-disknamn och lagrings-SKU vid användning av hanterade diskar har tagits bort</span><span class="sxs-lookup"><span data-stu-id="24203-329">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="24203-330">28 juli 2017</span><span class="sxs-lookup"><span data-stu-id="24203-330">July 28, 2017</span></span>

<span data-ttu-id="24203-331">Version 2.0.12</span><span class="sxs-lookup"><span data-stu-id="24203-331">Version 2.0.12</span></span>

* <span data-ttu-id="24203-332">Behållarkommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-332">Added container commands</span></span>
* <span data-ttu-id="24203-333">Fakturerings- och förbrukningsmoduler har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-333">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="24203-334">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-334">Core</span></span>

* <span data-ttu-id="24203-335">Returnera SDK-autentiseringsinformation för tjänsthuvudnamn med certifikat</span><span class="sxs-lookup"><span data-stu-id="24203-335">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="24203-336">Undantag i distributionsförloppet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-336">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="24203-337">Använd ARM-slutpunkten från det aktuella molnet för att skapa prenumerationsklient</span><span class="sxs-lookup"><span data-stu-id="24203-337">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="24203-338">Förbättrad samtidig hantering av clouds.config-filen (#3636)</span><span class="sxs-lookup"><span data-stu-id="24203-338">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="24203-339">Uppdatera ID:t för klientbegäranden vid varje kommandokörning</span><span class="sxs-lookup"><span data-stu-id="24203-339">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="24203-340">Skapa prenumerationsklienter med rätt SDK-profil (#3635)</span><span class="sxs-lookup"><span data-stu-id="24203-340">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="24203-341">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="24203-341">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="24203-342">Stöd har lagts till för att välja fält för tabellutdata via en jmespath-fråga (#3581)</span><span class="sxs-lookup"><span data-stu-id="24203-342">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="24203-343">Förbättrad avstängning av parsningsargument och tilläggshistorik med gester (#3434)</span><span class="sxs-lookup"><span data-stu-id="24203-343">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="24203-344">Skapa prenumerationsklienter med rätt SDK-profil</span><span class="sxs-lookup"><span data-stu-id="24203-344">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="24203-345">Flytta alla befintliga registreringsfiler till den senaste mappen</span><span class="sxs-lookup"><span data-stu-id="24203-345">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="24203-346">Idempotens har åtgärdats för VM/VMSS-generering (#3586)</span><span class="sxs-lookup"><span data-stu-id="24203-346">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="24203-347">Kommandosökvägar är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="24203-347">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="24203-348">Vissa parametrar av boolesk typ är inte längre skiftlägeskänsliga</span><span class="sxs-lookup"><span data-stu-id="24203-348">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="24203-349">Stöd har lagts till för inloggning till ADFS på lokala servrar som Azure Stack</span><span class="sxs-lookup"><span data-stu-id="24203-349">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="24203-350">Ett problem med samtidiga skrivningar till clouds.config har åtgärdats (#3255)</span><span class="sxs-lookup"><span data-stu-id="24203-350">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="24203-351">ACR</span><span class="sxs-lookup"><span data-stu-id="24203-351">ACR</span></span>

* <span data-ttu-id="24203-352">Kommandot `show-usage` har lagts till för hanterade register</span><span class="sxs-lookup"><span data-stu-id="24203-352">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="24203-353">Stöd har lagts till för SKU-uppdatering för hanterade register</span><span class="sxs-lookup"><span data-stu-id="24203-353">Support SKU update for managed registries</span></span>
* <span data-ttu-id="24203-354">Hanterade register med hanterad SKU har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-354">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="24203-355">Webhooks har lagts till för hanterade register med komandomodulen acr webhook</span><span class="sxs-lookup"><span data-stu-id="24203-355">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="24203-356">AAD-autentisering har lagts till med kommandot acr login</span><span class="sxs-lookup"><span data-stu-id="24203-356">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="24203-357">Kommandot delete har lagts till för Docker-databaser, -manifest och -taggar</span><span class="sxs-lookup"><span data-stu-id="24203-357">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="24203-358">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-358">ACS</span></span>

* <span data-ttu-id="24203-359">Stöd för API-version 2017-07-01</span><span class="sxs-lookup"><span data-stu-id="24203-359">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-360">App Service</span><span class="sxs-lookup"><span data-stu-id="24203-360">Appservice</span></span>

* <span data-ttu-id="24203-361">En bugg har åtgärdats som gjorde att ingenting returnerades när en lista med Linux-webbappar skulle visas</span><span class="sxs-lookup"><span data-stu-id="24203-361">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="24203-362">Stöd har lagts till för att hämta autentiseringsuppgifter från ACR</span><span class="sxs-lookup"><span data-stu-id="24203-362">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="24203-363">Ta bort alla kommandon under `appservice web`</span><span class="sxs-lookup"><span data-stu-id="24203-363">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="24203-364">Maskera lösenord för Docker-register i kommandoutdata (#3656)</span><span class="sxs-lookup"><span data-stu-id="24203-364">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="24203-365">Kontrollera att standardwebbläsaren används i Mac OS utan fel (#3623)</span><span class="sxs-lookup"><span data-stu-id="24203-365">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="24203-366">Förbättra hjälpen för `webapp log tail` och `webapp log download` (#3624)</span><span class="sxs-lookup"><span data-stu-id="24203-366">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="24203-367">Kommandot `traffic-routing` har gjorts tillgängligt för konfigurering av statisk routning (#3566)</span><span class="sxs-lookup"><span data-stu-id="24203-367">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="24203-368">Tillförlitlighetskorrigeringar har lagts till för konfigurering av källkontroller (#3245)</span><span class="sxs-lookup"><span data-stu-id="24203-368">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="24203-369">`--node-version`-argumentet som inte stöds har tagits bort från `webapp config update` för Windows-webbappar.</span><span class="sxs-lookup"><span data-stu-id="24203-369">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="24203-370">Använd `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` i stället</span><span class="sxs-lookup"><span data-stu-id="24203-370">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="24203-371">Batch</span><span class="sxs-lookup"><span data-stu-id="24203-371">Batch</span></span>

* <span data-ttu-id="24203-372">Uppdaterat till Batch SDK 3.0.0 med stöd för virtuella datorer med låg prioritet i pooler</span><span class="sxs-lookup"><span data-stu-id="24203-372">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="24203-373">`pool create`-alternativet `--target-dedicated` har bytt namn till `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="24203-373">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="24203-374">`pool create`-alternativen `--target-low-priority-nodes` och `--application-licenses` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-374">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="24203-375">CDN</span><span class="sxs-lookup"><span data-stu-id="24203-375">CDN</span></span>

* <span data-ttu-id="24203-376">Ett bättre felmeddelande visas för `cdn endpoint list` när profilen som angetts av `--profile-name` inte finns.</span><span class="sxs-lookup"><span data-stu-id="24203-376">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="24203-377">Molnet</span><span class="sxs-lookup"><span data-stu-id="24203-377">Cloud</span></span>

* <span data-ttu-id="24203-378">API-versionen för slutpunkter för molnmetadata har ändrats till formatet ÅÅÅÅ-MM-DD</span><span class="sxs-lookup"><span data-stu-id="24203-378">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="24203-379">Slutpunkt för galleri krävs inte</span><span class="sxs-lookup"><span data-stu-id="24203-379">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="24203-380">Stöd har lagts till för att registrera moln med endast slutpunkten för ARM-resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="24203-380">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="24203-381">Ett alternativ har lagts till för `cloud set` så att profilen kan väljas när det aktuella molnet väljs</span><span class="sxs-lookup"><span data-stu-id="24203-381">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="24203-382">`endpoint_vm_image_alias_doc` har gjorts tillgängligt</span><span class="sxs-lookup"><span data-stu-id="24203-382">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="24203-383">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="24203-383">CosmosDB</span></span>

* <span data-ttu-id="24203-384">Ett problem har åtgärdats som gjorde att det inte gick att skapa en samling med en anpassad partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="24203-384">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="24203-385">Stöd har lagts till för standard-TTL för samlingar.</span><span class="sxs-lookup"><span data-stu-id="24203-385">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="24203-386">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="24203-386">Data Lake Analytics</span></span>

* <span data-ttu-id="24203-387">Kommandon har lagts till för hantering av beräkningsprinciper under `dla account compute-policy`-huvudet</span><span class="sxs-lookup"><span data-stu-id="24203-387">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="24203-388">`dla job pipeline show` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-388">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="24203-389">`dla job recurrence list` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-389">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="24203-390">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="24203-390">Data Lake Store</span></span>

* <span data-ttu-id="24203-391">Stöd har lagts till för nyckelrotation med användarhanterade nyckelvalv i `dls account update`</span><span class="sxs-lookup"><span data-stu-id="24203-391">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="24203-392">SDK-versionen för det underliggande Data Lake Store-filsystemet har uppdaterats; ett prestandaproblem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="24203-392">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="24203-393">Kommandot `dls enable-key-vault` har lagts till.</span><span class="sxs-lookup"><span data-stu-id="24203-393">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="24203-394">Det här kommandot försöker aktivera ett användardefinierat nyckelvalv för kryptering av data i ett Data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="24203-394">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="24203-395">Interaktiv</span><span class="sxs-lookup"><span data-stu-id="24203-395">Interactive</span></span>

* <span data-ttu-id="24203-396">Förbättrade starttider med hjälp av cachelagrade kommandon</span><span class="sxs-lookup"><span data-stu-id="24203-396">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="24203-397">Ökad täckning vid testning</span><span class="sxs-lookup"><span data-stu-id="24203-397">Increased test coverage</span></span>
* <span data-ttu-id="24203-398">”?”-gesten har förbättrats att även omfatta nästa kommando</span><span class="sxs-lookup"><span data-stu-id="24203-398">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="24203-399">Ett problem har åtgärdats som resulterade i interaktiva fel med profilen 2017-03-09-profile-preview (#3587)</span><span class="sxs-lookup"><span data-stu-id="24203-399">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="24203-400">`--version` tillåts som parameter för interaktivt läge (#3645)</span><span class="sxs-lookup"><span data-stu-id="24203-400">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="24203-401">Ett problem har åtgärdats som gjorde att verifieringar slutfördes med fel i interaktivt läge (#3570)</span><span class="sxs-lookup"><span data-stu-id="24203-401">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="24203-402">Förloppsrapportering för malldistributioner (#3510)</span><span class="sxs-lookup"><span data-stu-id="24203-402">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="24203-403">Flaggan `--progress` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-403">Added `--progress` flag</span></span>
* <span data-ttu-id="24203-404">`--debug` och `--verbose` har tagits bort från completion-händelser</span><span class="sxs-lookup"><span data-stu-id="24203-404">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="24203-405">`interactive` har tagits bort från completion-händelser (#3324)</span><span class="sxs-lookup"><span data-stu-id="24203-405">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="24203-406">IoT</span><span class="sxs-lookup"><span data-stu-id="24203-406">IoT</span></span>

* <span data-ttu-id="24203-407">Ett problem har åtgärdats som gjorde att befintliga principer rensades när nya principer skapades.</span><span class="sxs-lookup"><span data-stu-id="24203-407">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="24203-408">(#3934)</span><span class="sxs-lookup"><span data-stu-id="24203-408">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="24203-409">Nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="24203-409">Key vault</span></span>

* <span data-ttu-id="24203-410">Kommandon har lagts till för återställningsfunktioner för nyckelvalv:</span><span class="sxs-lookup"><span data-stu-id="24203-410">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="24203-411">`keyvault`-underkommandona `purge`, `recover`, `keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="24203-411">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="24203-412">`keyvault secret`-underkommandona `backup`, `restore`, `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="24203-412">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="24203-413">`keyvault certificate`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="24203-413">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="24203-414">`keyvault key`-underkommandona `purge`, `recover`, `list-deleted`</span><span class="sxs-lookup"><span data-stu-id="24203-414">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="24203-415">Integration av nyckelvalv för tjänsthuvudnamn har lagts till (#3133)</span><span class="sxs-lookup"><span data-stu-id="24203-415">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="24203-416">Dataplanen för nyckelvalv har uppdaterats till 0.3.2.</span><span class="sxs-lookup"><span data-stu-id="24203-416">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="24203-417">(#3307)</span><span class="sxs-lookup"><span data-stu-id="24203-417">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="24203-418">Labb</span><span class="sxs-lookup"><span data-stu-id="24203-418">Lab</span></span>

* <span data-ttu-id="24203-419">Stöd har lagts till för att begära valfri virtuell dator i labbet via `az lab vm claim`</span><span class="sxs-lookup"><span data-stu-id="24203-419">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="24203-420">Formateringsverktyg har lagts till för tabellutdata för `az lab vm list` och `az lab vm show`</span><span class="sxs-lookup"><span data-stu-id="24203-420">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="24203-421">Övervaka</span><span class="sxs-lookup"><span data-stu-id="24203-421">Monitor</span></span>

* <span data-ttu-id="24203-422">Korrigering för mallfiler med kommandot `monitor autoscale-settings get-parameters-template` (#3349)</span><span class="sxs-lookup"><span data-stu-id="24203-422">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="24203-423">`monitor alert-rule-incidents list` har bytt namn till `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="24203-423">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="24203-424">`monitor alert-rule-incidents show` har bytt namn till `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="24203-424">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="24203-425">`monitor metric-defintions list` har bytt namn till `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="24203-425">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="24203-426">`monitor alert-rules` har bytt namn till `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="24203-426">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="24203-427">`monitor alert create` har ändrats:</span><span class="sxs-lookup"><span data-stu-id="24203-427">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="24203-428">`condition`- och `action`-underkommandon accepterar inte längre JSON</span><span class="sxs-lookup"><span data-stu-id="24203-428">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="24203-429">Flera parametrar har lagts till för att förenkla genereringen av regler</span><span class="sxs-lookup"><span data-stu-id="24203-429">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="24203-430">`location` krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="24203-430">`location` no longer required</span></span>
  * <span data-ttu-id="24203-431">Namn- och ID-stöd har lagts till för mål</span><span class="sxs-lookup"><span data-stu-id="24203-431">Add name and ID support for target</span></span>
  * <span data-ttu-id="24203-432">`--alert-rule-resource-name` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="24203-432">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="24203-433">`is-enabled` har bytt namn till `enabled`; krävs inte längre</span><span class="sxs-lookup"><span data-stu-id="24203-433">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="24203-434">Nu baseras `description`-standardvärden på det angivna villkoret</span><span class="sxs-lookup"><span data-stu-id="24203-434">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="24203-435">Exempel har lagts till för att förtydliga det nya formatet</span><span class="sxs-lookup"><span data-stu-id="24203-435">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="24203-436">Stöd har lagts till för namn eller ID:n för `monitor metric`-kommandon</span><span class="sxs-lookup"><span data-stu-id="24203-436">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="24203-437">Bekvämlighetsargument och exempel har lagts till för `monitor alert rule update`</span><span class="sxs-lookup"><span data-stu-id="24203-437">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="24203-438">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-438">Network</span></span>

* <span data-ttu-id="24203-439">Kommandot `list-private-access-services` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-439">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="24203-440">Argumentet `--private-access-services` har lagts till för `vnet subnet create` och `vnet subnet update`</span><span class="sxs-lookup"><span data-stu-id="24203-440">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="24203-441">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config create` misslyckades</span><span class="sxs-lookup"><span data-stu-id="24203-441">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="24203-442">Ett problem har åtgärdats som gjorde att `application-gateway redirect-config update` inte fungerade med `--no-wait`</span><span class="sxs-lookup"><span data-stu-id="24203-442">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="24203-443">En bugg har åtgärdats som gjorde att argumentet `--servers` inte fungerade med `application-gateway address-pool create` och `application-gateway address-pool update`</span><span class="sxs-lookup"><span data-stu-id="24203-443">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="24203-444">`application-gateway redirect-config`-kommandon har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-444">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="24203-445">Kommandon har lagts till för `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span><span class="sxs-lookup"><span data-stu-id="24203-445">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="24203-446">Argument har lagts till för `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="24203-446">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="24203-447">Argument har lagts till för `application-gateway http-settings create` och `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span><span class="sxs-lookup"><span data-stu-id="24203-447">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="24203-448">Argument har lagts till för `application-gateway url-path-map create` och `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="24203-448">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="24203-449">Argumentet `--redirect-config` har lagts till för `application-gateway url-path-map rule create`</span><span class="sxs-lookup"><span data-stu-id="24203-449">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="24203-450">Stöd har lagts till för `--no-wait` för `application-gateway url-path-map rule delete`</span><span class="sxs-lookup"><span data-stu-id="24203-450">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="24203-451">Argument har lagts till för `application-gateway probe create` och `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="24203-451">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="24203-452">Argumentet `--redirect-config` har lagts till för `application-gateway rule create` och `application-gateway rule update`</span><span class="sxs-lookup"><span data-stu-id="24203-452">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="24203-453">Stöd har lagts till för `--accelerated-networking` för `nic create` och `nic update`</span><span class="sxs-lookup"><span data-stu-id="24203-453">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="24203-454">Argumentet `--internal-dns-name-suffix` har tagits bort från `nic create`</span><span class="sxs-lookup"><span data-stu-id="24203-454">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="24203-455">Stöd har lagts till för `--dns-servers` för `nic update` och `nic create`: Stöd för --dns-servers har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-455">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="24203-456">En bugg har åtgärdats som gjorde att `local-gateway create` ignorerade `--local-address-prefixes`</span><span class="sxs-lookup"><span data-stu-id="24203-456">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="24203-457">Stöd har lagts till för `--dns-servers` för `vnet update`</span><span class="sxs-lookup"><span data-stu-id="24203-457">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="24203-458">En bugg har åtgärdats som resulterade i fel när en peer-koppling utan vägfiltrering skapades med `express-route peering create`</span><span class="sxs-lookup"><span data-stu-id="24203-458">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="24203-459">En bugg har åtgärdats som gjorde att argumenten `--provider` och `--bandwidth` inte fungerade med `express-route update`</span><span class="sxs-lookup"><span data-stu-id="24203-459">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="24203-460">En bugg har åtgärdats som resulterade i fel med `network watcher show-topology`-standardlogik</span><span class="sxs-lookup"><span data-stu-id="24203-460">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="24203-461">Förbättrad formatering av utdata för `network list-usages`</span><span class="sxs-lookup"><span data-stu-id="24203-461">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="24203-462">Använd standard-IP-adressen för klienten för `application-gateway http-listener create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="24203-462">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="24203-463">Använd standardadresspoolen, HTTP-standardinställningarna och HTTP-standardlyssnaren för `application-gateway rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="24203-463">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="24203-464">Använd standard-IP-adressen för klienten och serverpoolen för `lb rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="24203-464">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="24203-465">Använd standard-IP-adressen för klienten för `lb inbound-nat-rule create` om det bara finns en</span><span class="sxs-lookup"><span data-stu-id="24203-465">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="24203-466">Profil</span><span class="sxs-lookup"><span data-stu-id="24203-466">Profile</span></span>

* <span data-ttu-id="24203-467">Stöd har lagts till för inloggning på en virtuell dator med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="24203-467">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="24203-468">Stöd har lagts till för `account show`-utdata i formatet för SDK-autentiseringsfiler</span><span class="sxs-lookup"><span data-stu-id="24203-468">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="24203-469">Visa utfasningsvarningar när ”--expanded-view” används</span><span class="sxs-lookup"><span data-stu-id="24203-469">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="24203-470">Kommandot `get-access-token` har lagts till för att tillhandahålla AAD-rådatatoken</span><span class="sxs-lookup"><span data-stu-id="24203-470">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="24203-471">Stöd har lagts till för inloggning med ett användarkonto utan associerade prenumerationer</span><span class="sxs-lookup"><span data-stu-id="24203-471">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="24203-472">RDBMS</span><span class="sxs-lookup"><span data-stu-id="24203-472">RDBMS</span></span>

* <span data-ttu-id="24203-473">Stöd har lagts till för att lista servrar i hela prenumerationen (#3417)</span><span class="sxs-lookup"><span data-stu-id="24203-473">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="24203-474">Ett problem har åtgärdats som gjorde att `%s` inte bearbetades när `% server_type` saknades (#3393)</span><span class="sxs-lookup"><span data-stu-id="24203-474">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="24203-475">Mappningen av datakällor har åtgärdats och en CI-uppgift har lagts till för verifiering (#3361)</span><span class="sxs-lookup"><span data-stu-id="24203-475">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="24203-476">MySQL- och PostgreSQL-hjälpen har åtgärdats (#3369)</span><span class="sxs-lookup"><span data-stu-id="24203-476">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="24203-477">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-477">Resource</span></span>

* <span data-ttu-id="24203-478">Förbättrade prompter för parametrar som saknas för `group deployment create`</span><span class="sxs-lookup"><span data-stu-id="24203-478">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="24203-479">Förbättrad parsning av `--parameters KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="24203-479">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="24203-480">Ett problem har åtgärdats som gjorde att `group deployment create`-parameterfiler inte längre identifierades av `@<file>`-syntaxen</span><span class="sxs-lookup"><span data-stu-id="24203-480">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="24203-481">Stöd har lagts till för argumentet `--ids` för kommandona `resource` och `managedapp`</span><span class="sxs-lookup"><span data-stu-id="24203-481">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="24203-482">En del parsnings- och felmeddelanden har åtgärdats (#3584)</span><span class="sxs-lookup"><span data-stu-id="24203-482">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="24203-483">Ett problem med `--resource-type`-parsningen har åtgärdats så att kommandot `lock` accepterar `<resource-namespace>` och `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="24203-483">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="24203-484">Parameterkontroll har lagts till för mallar med mallänkar (#3629)</span><span class="sxs-lookup"><span data-stu-id="24203-484">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="24203-485">Stöd har lagts till för distributionsparametrar med `KEY=VALUE`-syntax</span><span class="sxs-lookup"><span data-stu-id="24203-485">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="24203-486">Roll</span><span class="sxs-lookup"><span data-stu-id="24203-486">Role</span></span>

* <span data-ttu-id="24203-487">Stöd har lagts till för utdata i formatet för SDK-autentiseringsfiler för `create-for-rbac`</span><span class="sxs-lookup"><span data-stu-id="24203-487">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="24203-488">Rolltilldelningar och relaterade AAD-program rensas när ett huvudtjänstnamn tas bort (#3610)</span><span class="sxs-lookup"><span data-stu-id="24203-488">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="24203-489">Ta med tidsformat för `--start-date`- och `--end-date`-beskrivningar i `app create`-argument </span><span class="sxs-lookup"><span data-stu-id="24203-489">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="24203-490">Visa utfasningsvarningar när `--expanded-view` används</span><span class="sxs-lookup"><span data-stu-id="24203-490">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="24203-491">Integration med nyckelvalv har lagts till för kommandona `create-for-rbac` och `reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="24203-491">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="24203-492">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="24203-492">Service Fabric</span></span>
* <span data-ttu-id="24203-493">Ett problem har åtgärdats som gjorde att stora filer i program trunkerades vid uppladdning (#3666)</span><span class="sxs-lookup"><span data-stu-id="24203-493">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="24203-494">Tester har lagts till för Service Fabric-kommandon (#3424)</span><span class="sxs-lookup"><span data-stu-id="24203-494">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="24203-495">Flera Service Fabric-kommandon har åtgärdats (#3234)</span><span class="sxs-lookup"><span data-stu-id="24203-495">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="24203-496">SQL</span><span class="sxs-lookup"><span data-stu-id="24203-496">SQL</span></span>

* <span data-ttu-id="24203-497">Skadad `sql server create` `--identity`-parameter har tagits bort</span><span class="sxs-lookup"><span data-stu-id="24203-497">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="24203-498">Lösenordsvärden har tagits bort från `sql server create`- och `sql server update`-kommandoutdata</span><span class="sxs-lookup"><span data-stu-id="24203-498">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="24203-499">Kommandona `sql db list-editions` och `sql elastic-pool list-editions` har lagts till</span><span class="sxs-lookup"><span data-stu-id="24203-499">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="24203-500">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-500">Storage</span></span>

* <span data-ttu-id="24203-501">Alternativet `--marker` har tagits bort från kommandona `storage blob list`, `storage container list` och `storage share list` (#3745)</span><span class="sxs-lookup"><span data-stu-id="24203-501">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="24203-502">Stöd har lagts till för att skapa ett lagringskonto med endast HTTPS</span><span class="sxs-lookup"><span data-stu-id="24203-502">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="24203-503">Mått-, loggnings- och CORS-kommandon för lagring har uppdaterats (#3495)</span><span class="sxs-lookup"><span data-stu-id="24203-503">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="24203-504">Undantagsmeddelandet från CORS-tillägg har omformulerats (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="24203-504">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="24203-505">Generatorn har konverterats till en lista för kommandot download batch i kontrolläge (#3592)</span><span class="sxs-lookup"><span data-stu-id="24203-505">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="24203-506">Ett problem med kommandot download batch för blobbar i kontrolläge har åtgärdats (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="24203-506">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="24203-507">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-507">VM</span></span>

* <span data-ttu-id="24203-508">Stöd har lagts till för att konfigurera NSG</span><span class="sxs-lookup"><span data-stu-id="24203-508">Support configuring nsg</span></span>
* <span data-ttu-id="24203-509">En bugg har åtgärdats som gjorde att DNS-servern inte konfigurerades korrekt</span><span class="sxs-lookup"><span data-stu-id="24203-509">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="24203-510">Stöd har lagts till för hanterade tjänstidentiteter</span><span class="sxs-lookup"><span data-stu-id="24203-510">Support managed service identities</span></span>
* <span data-ttu-id="24203-511">Ett problem har åtgärdats som gjorde att `cmss create` med en befintlig belastningsutjämnare krävde `--backend-pool-name`.</span><span class="sxs-lookup"><span data-stu-id="24203-511">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="24203-512">Gör så att LUN för datadiskar som skapas med `vm image create` börjar med 0</span><span class="sxs-lookup"><span data-stu-id="24203-512">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="24203-513">10 maj 2017</span><span class="sxs-lookup"><span data-stu-id="24203-513">May 10, 2017</span></span>

<span data-ttu-id="24203-514">Version 2.0.6</span><span class="sxs-lookup"><span data-stu-id="24203-514">Version 2.0.6</span></span>

* <span data-ttu-id="24203-515">documentdb byter namn till cosmosdb</span><span class="sxs-lookup"><span data-stu-id="24203-515">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="24203-516">Lägg till rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="24203-516">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="24203-517">Ta med Data Lake Analytics- och Data Lake Store-moduler.</span><span class="sxs-lookup"><span data-stu-id="24203-517">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="24203-518">Ta med Cognitive Services-modul.</span><span class="sxs-lookup"><span data-stu-id="24203-518">Include Cognitive Services module.</span></span>
* <span data-ttu-id="24203-519">Ta med Service Fabric-modul.</span><span class="sxs-lookup"><span data-stu-id="24203-519">Include Service Fabric module.</span></span>
* <span data-ttu-id="24203-520">Ta med interaktiv modul (har bytt namn från az-shell).</span><span class="sxs-lookup"><span data-stu-id="24203-520">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="24203-521">Lägg till stöd för CDN-kommandon.</span><span class="sxs-lookup"><span data-stu-id="24203-521">Add support for CDN commands.</span></span>
* <span data-ttu-id="24203-522">Ta bort behållarmodul.</span><span class="sxs-lookup"><span data-stu-id="24203-522">Remove Container module.</span></span>
* <span data-ttu-id="24203-523">Lägg till ”az -v” som genväg för ”az --version” ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="24203-523">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="24203-524">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="24203-524">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="24203-525">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-525">Core</span></span>

* <span data-ttu-id="24203-526">kärna: fånga in undantag som orsakats av oregistrerad provider och registrera den automatiskt</span><span class="sxs-lookup"><span data-stu-id="24203-526">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="24203-527">prestanda: spara adal-token i cacheminnet tills processen avslutas ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="24203-527">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="24203-528">Åtgärda byte som returneras från hexadecimalt fingeravtryck -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="24203-528">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="24203-529">Förbättrad nedladdning av Key Vault-certifikat och AAD SP-integrering ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="24203-529">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="24203-530">Lägg till Python-plats till ”az —version” ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="24203-530">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="24203-531">inloggning: stöd för inloggning när prenumerationer saknas ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="24203-531">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="24203-532">kärna: åtgärda ett fel när tjänstens huvudnamn används två gånger vid inloggning ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="24203-532">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="24203-533">kärna: Tillåt filsökvägen för accessTokens.json att konfigurera via en miljövariabel ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="24203-533">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="24203-534">kärna: Tillåt konfigurerade standardinställningar att tillämpas på valfria argument ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="24203-534">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="24203-535">kärna: Förbättrad prestanda</span><span class="sxs-lookup"><span data-stu-id="24203-535">core: Improved performance</span></span>
* <span data-ttu-id="24203-536">kärnor: Anpassade CA-certifikat – Stöd för att ange inställningen REQUESTS_CA_BUNDLE som miljövariabel</span><span class="sxs-lookup"><span data-stu-id="24203-536">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="24203-537">kärna: Molnkonfiguration – använd slutpunkten för ”resource manager” om slutpunkten för ”hantering” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="24203-537">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="24203-538">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-538">ACS</span></span>

* <span data-ttu-id="24203-539">korrigera antalet huvudservrar och agenter till heltal istället för strängar</span><span class="sxs-lookup"><span data-stu-id="24203-539">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="24203-540">gör ”az acs create --no-wait” och ”az acs wait” tillgängliga för asynkront skapande</span><span class="sxs-lookup"><span data-stu-id="24203-540">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="24203-541">gör ”az acs create --validate” tillgänglig för testverifieringar</span><span class="sxs-lookup"><span data-stu-id="24203-541">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="24203-542">ta bort Windows-profilen före PUT-anrop för skalkommando ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="24203-542">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="24203-543">AppService</span><span class="sxs-lookup"><span data-stu-id="24203-543">AppService</span></span>

* <span data-ttu-id="24203-544">functionapp: lägg till fullständigt stöd för functionapp, inklusive funktioner för att skapa, visa, skapa listor, ta bort, värdnamn, ssl, osv.</span><span class="sxs-lookup"><span data-stu-id="24203-544">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="24203-545">Lägg till Team Services (vsts) som ett kontinuerligt leveransalternativ för "appservice web source-control config"</span><span class="sxs-lookup"><span data-stu-id="24203-545">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="24203-546">Skapa "az webapp" för att ersätta "az appservice web" (för bakåtkompatibilitet kommer "az appservice web" finnas kvar för två versioner)</span><span class="sxs-lookup"><span data-stu-id="24203-546">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="24203-547">Gör argument tillgängliga för att konfigurera distribution och "körningsstacks" när webbapp skapas</span><span class="sxs-lookup"><span data-stu-id="24203-547">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="24203-548">Gör "webapp list-runtimes" tillgänglig</span><span class="sxs-lookup"><span data-stu-id="24203-548">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="24203-549">stöd för konfigurering av anslutningssträngar ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="24203-549">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="24203-550">stöd för växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="24203-550">support slot swap with preview</span></span>
* <span data-ttu-id="24203-551">Korrigera fel från appservice-kommandon ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="24203-551">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="24203-552">Använd App Service-planens resursgrupp för certifieringsåtgärder ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="24203-552">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="24203-553">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="24203-553">CosmosDB</span></span>

* <span data-ttu-id="24203-554">Ändra documentdb-modulen till cosmosdb.</span><span class="sxs-lookup"><span data-stu-id="24203-554">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="24203-555">Stöd har lagts till för API:er för documentdb-dataplaner: hantering av databaser och samlingar</span><span class="sxs-lookup"><span data-stu-id="24203-555">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="24203-556">Stöd har lagts till för att aktivera automatisk redundans på databaskonton</span><span class="sxs-lookup"><span data-stu-id="24203-556">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="24203-557">Stöd har lagts till för ny ConsistentPrefix-konsekvensprincip</span><span class="sxs-lookup"><span data-stu-id="24203-557">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="24203-558">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="24203-558">Data Lake Analytics</span></span>

* <span data-ttu-id="24203-559">Åtgärda en bugg där filtrering på resultat och tillstånd för jobblistor genererar ett fel.</span><span class="sxs-lookup"><span data-stu-id="24203-559">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="24203-560">Lägg till stöd för ny objekttyp i katalog: paket.</span><span class="sxs-lookup"><span data-stu-id="24203-560">Add support for new catalog item type: package.</span></span> <span data-ttu-id="24203-561">nås via: `az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="24203-561">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="24203-562">Gjorde det möjligt att visa en lista över följande katalogobjekt från en databas (ingen specifikation av schema krävs):</span><span class="sxs-lookup"><span data-stu-id="24203-562">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="24203-563">Tabell</span><span class="sxs-lookup"><span data-stu-id="24203-563">Table</span></span>
  * <span data-ttu-id="24203-564">Tabellvärdesfunktion</span><span class="sxs-lookup"><span data-stu-id="24203-564">Table valued function</span></span>
  * <span data-ttu-id="24203-565">Visa</span><span class="sxs-lookup"><span data-stu-id="24203-565">View</span></span>
  * <span data-ttu-id="24203-566">Tabellstatistik.</span><span class="sxs-lookup"><span data-stu-id="24203-566">Table Statistics.</span></span> <span data-ttu-id="24203-567">Detta kan även anges med ett schema, men utan att ange ett tabellnamn.</span><span class="sxs-lookup"><span data-stu-id="24203-567">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="24203-568">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="24203-568">Data Lake Store</span></span>

* <span data-ttu-id="24203-569">Uppdatera versionen av den underliggande SDK:en för filsystemet, vilket ger bättre stöd för att hantera begränsningsscenarier på serversidan.</span><span class="sxs-lookup"><span data-stu-id="24203-569">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="24203-570">Förbättra prestanda för inläsning av paket och körning av kommando ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="24203-570">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="24203-571">hjälp vid visning av åtkomst saknas.</span><span class="sxs-lookup"><span data-stu-id="24203-571">missed help for access show.</span></span> <span data-ttu-id="24203-572">läggs till.</span><span class="sxs-lookup"><span data-stu-id="24203-572">adding it.</span></span> <span data-ttu-id="24203-573">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="24203-573">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="24203-574">Hitta</span><span class="sxs-lookup"><span data-stu-id="24203-574">Find</span></span>

* <span data-ttu-id="24203-575">förbättra sökresultat och tillåt versionshantering i sökindexet</span><span class="sxs-lookup"><span data-stu-id="24203-575">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="24203-576">KeyVault</span><span class="sxs-lookup"><span data-stu-id="24203-576">KeyVault</span></span>

* <span data-ttu-id="24203-577">BC:`az keyvault certificate download` ändra -e från sträng eller binär till PEM eller DER för att bättre motsvara alternativen</span><span class="sxs-lookup"><span data-stu-id="24203-577">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="24203-578">BC: Ta bort --expires och --not-before från `keyvault certificate create` eftersom dessa parametrar inte stöds av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="24203-578">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="24203-579">Lägger till parametern --validity till `keyvault certificate create` för att selektivt åsidosätta värdet i --policy</span><span class="sxs-lookup"><span data-stu-id="24203-579">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="24203-580">Åtgärdar problemet i `keyvault certificate get-default-policy` där ”expires” och ”not_before” var tillgängliga men ”validity_in_months” inte var det.</span><span class="sxs-lookup"><span data-stu-id="24203-580">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="24203-581">korrigering i keyvault för importering av pem och pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="24203-581">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="24203-582">Labb</span><span class="sxs-lookup"><span data-stu-id="24203-582">Lab</span></span>

* <span data-ttu-id="24203-583">Lägg till kommandon för att skapa, visa, ta bort och skapa lista för miljön i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="24203-583">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="24203-584">Lägg till kommandon för att visa och skapa lista för att se ARM-mallar i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="24203-584">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="24203-585">Lägg till --environment-flagga i `az lab vm list` för att filtrera virtuella datorer efter miljö i laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="24203-585">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="24203-586">Lägg till bekvämlighetskommandot `az lab formula export-artifacts` för att exportera artefaktram i en laboratoriumformel.</span><span class="sxs-lookup"><span data-stu-id="24203-586">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="24203-587">Lägg till kommandon för att hantera hemligheter i ett laboratorium.</span><span class="sxs-lookup"><span data-stu-id="24203-587">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="24203-588">Övervaka</span><span class="sxs-lookup"><span data-stu-id="24203-588">Monitor</span></span>

* <span data-ttu-id="24203-589">Felkorrigering: Modellera `--actions` av `az alert-rules create` för att förbruka JSON-sträng ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="24203-589">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="24203-590">Felkorrigering – diagnostikinställningar för att skapa accepterar inte loggar/mått från visningskommandon ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="24203-590">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="24203-591">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-591">Network</span></span>

* <span data-ttu-id="24203-592">Lägg till kommandot `network watcher test-connectivity`.</span><span class="sxs-lookup"><span data-stu-id="24203-592">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="24203-593">Lägg till stöd för parametern `--filters` för `network watcher packet-capture create`.</span><span class="sxs-lookup"><span data-stu-id="24203-593">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="24203-594">Lägg till stöd för anslutningstömning för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="24203-594">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="24203-595">Lägg till stöd för konfiguration av WAF-regler för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="24203-595">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="24203-596">Lägg till stöd för vägfilter och regler för ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="24203-596">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="24203-597">Lägg till stöd för geografisk routning för TrafficManager.</span><span class="sxs-lookup"><span data-stu-id="24203-597">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="24203-598">Lägg till stöd för trafikväljare med principbaserad VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="24203-598">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="24203-599">Lägg till stöd för IPSec-principer för VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="24203-599">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="24203-600">Åtgärda fel med `vpn-connection create` när du använder parametrarna `--no-wait` eller `--validate`.</span><span class="sxs-lookup"><span data-stu-id="24203-600">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="24203-601">Lägg till stöd för aktiva-aktiva VNet-gatewayer</span><span class="sxs-lookup"><span data-stu-id="24203-601">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="24203-602">Ta bort nullvärden från utdata för `network vpn-connection list/show`-kommandon.</span><span class="sxs-lookup"><span data-stu-id="24203-602">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="24203-603">BC: Åtgärda fel i utdata för `vpn-connection create`</span><span class="sxs-lookup"><span data-stu-id="24203-603">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="24203-604">Åtgärda fel där argumentet ”--key-length” för ”vpn-connection create” inte parsades korrekt.</span><span class="sxs-lookup"><span data-stu-id="24203-604">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="24203-605">Åtgärda fel i `dns zone import` där poster inte importerades korrekt.</span><span class="sxs-lookup"><span data-stu-id="24203-605">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="24203-606">Åtgärda fel där `traffic-manager endpoint update` inte fungerade.</span><span class="sxs-lookup"><span data-stu-id="24203-606">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="24203-607">Lägg till kommandon för förhandsversionen för ”network watcher”.</span><span class="sxs-lookup"><span data-stu-id="24203-607">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="24203-608">Profil</span><span class="sxs-lookup"><span data-stu-id="24203-608">Profile</span></span>

* <span data-ttu-id="24203-609">Stöd för inloggning när inga prenumerationer kan hittas ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="24203-609">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="24203-610">Stöd för korta parameternamn i az- kontogrupper --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="24203-610">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="24203-611">Redis</span><span class="sxs-lookup"><span data-stu-id="24203-611">Redis</span></span>

* <span data-ttu-id="24203-612">Lägg till ett uppdateringskommando som även lägger till möjligheten att skala för redis-cache</span><span class="sxs-lookup"><span data-stu-id="24203-612">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="24203-613">Gör att kommandot ”update-settings” blir föråldrat.</span><span class="sxs-lookup"><span data-stu-id="24203-613">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="24203-614">Resurs</span><span class="sxs-lookup"><span data-stu-id="24203-614">Resource</span></span>

* <span data-ttu-id="24203-615">Lägg till managedapp och definitionskommandon för managedapp ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="24203-615">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="24203-616">Stöd för ”provider operation”-kommandon ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="24203-616">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="24203-617">Stöd för att skapa allmän resurs ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="24203-617">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="24203-618">Åtgärda resursparsning och sökning efter API-version.</span><span class="sxs-lookup"><span data-stu-id="24203-618">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="24203-619">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="24203-619">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="24203-620">Lägg till dokument för låsningsuppdatering för az.</span><span class="sxs-lookup"><span data-stu-id="24203-620">Add docs for az lock update.</span></span> <span data-ttu-id="24203-621">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="24203-621">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="24203-622">Fel om du försöker skapa en lista med resurser för en grupp som inte finns.</span><span class="sxs-lookup"><span data-stu-id="24203-622">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="24203-623">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="24203-623">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="24203-624">[Compute] Korrigera problem med uppdatering av tillgänglighetsuppsättningar i VMSS och VM.</span><span class="sxs-lookup"><span data-stu-id="24203-624">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="24203-625">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="24203-625">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="24203-626">Korrigera funktionen för att skapa lås och ta bort om den överordnade resurssökvägen är None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="24203-626">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="24203-627">Roll</span><span class="sxs-lookup"><span data-stu-id="24203-627">Role</span></span>

* <span data-ttu-id="24203-628">create-for-rbac: kontrollera att slutdatumet för SP inte överstiger certifikatets förfallodatum ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="24203-628">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="24203-629">RBAC: lägg till fullständigt stöd för ”AD-grupp” ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="24203-629">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="24203-630">roll: åtgärda problem med uppdatering av rolldefinition ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="24203-630">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="24203-631">create-for-rbac: kontrollera att lösenordet som användaren anger hämtas</span><span class="sxs-lookup"><span data-stu-id="24203-631">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="24203-632">SQL</span><span class="sxs-lookup"><span data-stu-id="24203-632">SQL</span></span>

* <span data-ttu-id="24203-633">Kommandona az sql server list-usages och az sql db list-usages har lagts till.</span><span class="sxs-lookup"><span data-stu-id="24203-633">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="24203-634">SQL – förmåga att ansluta direkt till resursprovidern ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="24203-634">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="24203-635">Lagring</span><span class="sxs-lookup"><span data-stu-id="24203-635">Storage</span></span>

* <span data-ttu-id="24203-636">Standardplats för resursgruppens plats för `storage account create`.</span><span class="sxs-lookup"><span data-stu-id="24203-636">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="24203-637">Lägg till stöd för inkrementell blob-kopia</span><span class="sxs-lookup"><span data-stu-id="24203-637">Add support for incremental blob copy</span></span>
* <span data-ttu-id="24203-638">Lägg till stöd för uppladdning av stor blockblob</span><span class="sxs-lookup"><span data-stu-id="24203-638">Add support for large block blob upload</span></span>
* <span data-ttu-id="24203-639">Ändra blockstorlek till 100 MB när filen som ska laddas upp är större än 200 GB</span><span class="sxs-lookup"><span data-stu-id="24203-639">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="24203-640">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-640">VM</span></span>

* <span data-ttu-id="24203-641">avail-set: gör antalet UD- och FD-domäner valfritt</span><span class="sxs-lookup"><span data-stu-id="24203-641">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="24203-642">Obs: VM-kommandon i landsbaserade moln. Undvik funktioner som är relaterade till hanterade diskar, inklusive följande:</span><span class="sxs-lookup"><span data-stu-id="24203-642">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="24203-643">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="24203-643">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="24203-644">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="24203-644">az vm/vmss disk</span></span>
  3. <span data-ttu-id="24203-645">Använd "—use-unmanaged-disk" i "az vm/vmss create" för att undvika hanterade diskar. Andra kommandon bör fungera</span><span class="sxs-lookup"><span data-stu-id="24203-645">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="24203-646">vm/vmss: förbättra varningstexten när nyckelpar för ssh genereras</span><span class="sxs-lookup"><span data-stu-id="24203-646">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="24203-647">vm/vmss: stöd för att skapa från en marketplace-avbildning som kräver information om prenumerationsavtalet ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="24203-647">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="24203-648">3 april 2017</span><span class="sxs-lookup"><span data-stu-id="24203-648">April 3, 2017</span></span>

<span data-ttu-id="24203-649">Version 2.0.2</span><span class="sxs-lookup"><span data-stu-id="24203-649">Version 2.0.2</span></span>

<span data-ttu-id="24203-650">Vi lanserade komponenter för ACR, Batch, KeyVault och SQL i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="24203-650">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="24203-651">Kärna</span><span class="sxs-lookup"><span data-stu-id="24203-651">Core</span></span>

* <span data-ttu-id="24203-652">Lägg till acr, labb, övervaka och söka moduler i standardlistan.</span><span class="sxs-lookup"><span data-stu-id="24203-652">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="24203-653">Inloggning: hoppa över felaktig klient ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="24203-653">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="24203-654">inloggning: ställ in standardprenumeration till en med status ”Aktiverad” ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="24203-654">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="24203-655">Lägga till väntekommandon och --no-wait-support till fler kommandon ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="24203-655">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="24203-656">kärna: stöder inloggning med tjänstens huvudnamn med ett certifikat ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="24203-656">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="24203-657">Lägg till fråga om mallparametrar som saknas.</span><span class="sxs-lookup"><span data-stu-id="24203-657">Add prompting for missing template parameters.</span></span> <span data-ttu-id="24203-658">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="24203-658">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="24203-659">Stöder inställning av standardvärden för vanliga argument som standardresursgrupp, standardwebbplats, standard-vm</span><span class="sxs-lookup"><span data-stu-id="24203-659">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="24203-660">Stöder inloggning till specifik klient</span><span class="sxs-lookup"><span data-stu-id="24203-660">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="24203-661">ACS</span><span class="sxs-lookup"><span data-stu-id="24203-661">ACS</span></span>

* <span data-ttu-id="24203-662">[ACS] Lägga till stöd för att konfigurera ett ACS-standardkluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="24203-662">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="24203-663">Lägg till support för lösenordsfråga för ssh-nyckel.</span><span class="sxs-lookup"><span data-stu-id="24203-663">Add support for ssh key password prompting.</span></span> <span data-ttu-id="24203-664">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="24203-664">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="24203-665">Lägg till stöd för Windows-kluster.</span><span class="sxs-lookup"><span data-stu-id="24203-665">Add support for windows clusters.</span></span> <span data-ttu-id="24203-666">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="24203-666">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="24203-667">Växla från rollen ägare till deltagare.</span><span class="sxs-lookup"><span data-stu-id="24203-667">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="24203-668">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="24203-668">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="24203-669">AppService</span><span class="sxs-lookup"><span data-stu-id="24203-669">AppService</span></span>

* <span data-ttu-id="24203-670">appservice: stöd för att få extern ip-adress för DNS A-poster ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="24203-670">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="24203-671">appservice: stöd för certifikatbindning med jokertecken ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="24203-671">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="24203-672">appservice: stöd för lista med publiceringsprofiler ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="24203-672">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="24203-673">AppService – Utlöser källkontrollsynk efter konfig ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="24203-673">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="24203-674">DataLake</span><span class="sxs-lookup"><span data-stu-id="24203-674">DataLake</span></span>

* <span data-ttu-id="24203-675">Första versionen av Data Lake Analytics-modulen.</span><span class="sxs-lookup"><span data-stu-id="24203-675">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="24203-676">Första versionen av Data Lake Store-modulen.</span><span class="sxs-lookup"><span data-stu-id="24203-676">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="24203-677">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="24203-677">DocuemntDB</span></span>

* <span data-ttu-id="24203-678">DocumentDB: Lägger till stöd för att lista anslutningssträngar ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="24203-678">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="24203-679">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="24203-679">VM</span></span>

* <span data-ttu-id="24203-680">[Compute] Lägga till AppGateway-stöd till att skapa VM-skalningsuppsättning ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="24203-680">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="24203-681">[VM/VMSS] Förbättrat stöd för cachelagring ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="24203-681">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="24203-682">VM/VMSS: införliva validering av logik för autentiseringsuppgifter som används av portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="24203-682">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="24203-683">Lägga till väntekommandon och --no-wait-support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="24203-683">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="24203-684">VM-skalningsuppsättning: stöd * för att lista instansvy för virtuella datorer ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="24203-684">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="24203-685">Lägga till --secrets för virtuella datorer och VM-skalningsuppsättning ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="24203-685">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="24203-686">Tillåta att skapa virtuella datorer med specialiserad VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="24203-686">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="24203-687">27 februari 2017</span><span class="sxs-lookup"><span data-stu-id="24203-687">February 27, 2017</span></span>

<span data-ttu-id="24203-688">Version 2.0.0</span><span class="sxs-lookup"><span data-stu-id="24203-688">Version 2.0.0</span></span>

<span data-ttu-id="24203-689">Den här versionen av Azure CLI 2.0 är den första versionen som är "Allmänt tillgänglig".</span><span class="sxs-lookup"><span data-stu-id="24203-689">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="24203-690">Allmän tillgänglighet gäller för dessa kommandomoduler:</span><span class="sxs-lookup"><span data-stu-id="24203-690">General availability applies to these command modules:</span></span>
- <span data-ttu-id="24203-691">Behållartjänst (acs)</span><span class="sxs-lookup"><span data-stu-id="24203-691">Container Service (acs)</span></span>
- <span data-ttu-id="24203-692">Compute (inklusive Resource Manager, VM, VM-skalningsuppsättningar, Managed Disks)</span><span class="sxs-lookup"><span data-stu-id="24203-692">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="24203-693">Nätverk</span><span class="sxs-lookup"><span data-stu-id="24203-693">Networking</span></span>
- <span data-ttu-id="24203-694">Storage</span><span class="sxs-lookup"><span data-stu-id="24203-694">Storage</span></span>

<span data-ttu-id="24203-695">Dessa kommandomoduler kan användas i produktion och stöds av Microsofts vanliga SLA.</span><span class="sxs-lookup"><span data-stu-id="24203-695">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="24203-696">Du kan öppna problem direkt med Microsoft Support eller på vår [github-problemlista](https://github.com/azure/azure-cli/issues/).</span><span class="sxs-lookup"><span data-stu-id="24203-696">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="24203-697">Du kan ställa frågor på [StackOverflow med azure-cli-taggen](http://stackoverflow.com/questions/tagged/azure-cli) eller kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). Du kan ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="24203-697">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="24203-698">Kommandona i dessa moduler är stabila och syntaxen förväntas inte ändras i kommande lanseringar av den här versionen av Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="24203-698">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="24203-699">Verifiera CLI-version med `az --version`.</span><span class="sxs-lookup"><span data-stu-id="24203-699">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="24203-700">Utdata visar versionen av själva CLI (2.0.0 i den här versionen), de enskilda kommandomodulerna och de versioner av Python och GCC som du använder.</span><span class="sxs-lookup"><span data-stu-id="24203-700">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="24203-701">En del av kommandomodulerna har postfixet ”b*n*” eller ”rc*n*”.</span><span class="sxs-lookup"><span data-stu-id="24203-701">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="24203-702">De här kommandomodulerna är fortfarande i förhandsversion och blir allmänt tillgängliga i framtiden.</span><span class="sxs-lookup"><span data-stu-id="24203-702">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="24203-703">Vi har också nattliga förhandsversioner av CLI.</span><span class="sxs-lookup"><span data-stu-id="24203-703">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="24203-704">Mer information finns i de här instruktionerna för att [hämta nattförhandsversionerna](https://github.com/Azure/azure-cli#nightly-builds), och de här instruktionerna om [konfiguration för utvecklare och bidrag till kod](https://github.com/Azure/azure-cli#developer-setup).</span><span class="sxs-lookup"><span data-stu-id="24203-704">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="24203-705">Du kan anmäla problem med nattliga förhandsversioner på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="24203-705">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="24203-706">Anmäl problem i vår [github-problemlista](https://github.com/azure/azure-cli/issues/)</span><span class="sxs-lookup"><span data-stu-id="24203-706">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="24203-707">Kontakta produktteamet på [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="24203-707">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="24203-708">Ge feedback från kommandoraden med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="24203-708">Provide feedback from the command line with the `az feedback` command.</span></span>

