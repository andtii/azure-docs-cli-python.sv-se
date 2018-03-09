---
title: "Kom igång med Azure CLI 2.0"
description: "Kom igång med Azure CLI 2.0 genom att lära dig grunderna om kommandon."
keywords: Azure CLI, CLI help, Azure help, query, automation,
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/05/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 3f5fe1b01a8ce691846126a6c03e7222e9b20e0d
ms.sourcegitcommit: 29d7366a0902488f4f4d39c2cb0e89368d5186ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2018
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="fbd37-104">Kom igång med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="fbd37-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="fbd37-105">Välkommen till Azure CLI 2.0!</span><span class="sxs-lookup"><span data-stu-id="fbd37-105">Welcome to the Azure CLI 2.0!</span></span> <span data-ttu-id="fbd37-106">CLI är ett verktyg som är utformat för att du ska kunna arbeta snabbt och effektivt med Azure-tjänster, med fokus på automatisering.</span><span class="sxs-lookup"><span data-stu-id="fbd37-106">The CLI is a tool designed to get you working quickly and efficiently with Azure services, with an emphasis on automation.</span></span> <span data-ttu-id="fbd37-107">I den här artikeln beskrivs funktionerna i CLI och du får länkar till resurser som hjälper dig vara produktiv.</span><span class="sxs-lookup"><span data-stu-id="fbd37-107">This article introduces features of the CLI and links out to resources that help you be productive.</span></span>

## <a name="install-and-log-in"></a><span data-ttu-id="fbd37-108">Installera och logga in</span><span class="sxs-lookup"><span data-stu-id="fbd37-108">Install and log in</span></span>

<span data-ttu-id="fbd37-109">Om du inte redan har gjort det så kan du [installera CLI](install-azure-cli.md) eller testa [Azure Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="fbd37-109">If you haven't already, [install the CLI](install-azure-cli.md) or try out the [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>

<span data-ttu-id="fbd37-110">Innan du använder CLI-kommandon med en lokal installation måste du logga in med [az login](/cli/azure/reference-index#az_login).</span><span class="sxs-lookup"><span data-stu-id="fbd37-110">Before using any CLI commands with a local install, you need to log in with [az login](/cli/azure/reference-index#az_login).</span></span>

```azurecli
az login
```

<span data-ttu-id="fbd37-111">Med det här kommandot kan du logga in med en autentiseringskod via en webbplats.</span><span class="sxs-lookup"><span data-stu-id="fbd37-111">This command prompts you to log in with an authentication code via a website.</span></span> <span data-ttu-id="fbd37-112">Det finns några olika sätt att logga in som inte är interaktiva. Läs mer i [Logga in med Azure CLI 2.0](authenticate-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="fbd37-112">There are ways to log in non-interactively, which are covered in detail in [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="common-commands"></a><span data-ttu-id="fbd37-113">Vanliga kommandon</span><span class="sxs-lookup"><span data-stu-id="fbd37-113">Common commands</span></span>

<span data-ttu-id="fbd37-114">Den här tabellen innehåller några vanliga kommandon som används i CLI-länkarna till dokumentationssidorna i referensen.</span><span class="sxs-lookup"><span data-stu-id="fbd37-114">This table lists a few of the common commands used in the CLI links out to their documentation pages in the reference.</span></span>
<span data-ttu-id="fbd37-115">Du hittar alla underkommandon i de här grupperna och deras dokumentation i onlinereferenserna eller med argumentet `--help`.</span><span class="sxs-lookup"><span data-stu-id="fbd37-115">All subcommands of these groups and their documentation can be looked up in online reference or with the `--help` argument.</span></span>

| <span data-ttu-id="fbd37-116">Resurstyp</span><span class="sxs-lookup"><span data-stu-id="fbd37-116">Resource type</span></span> | <span data-ttu-id="fbd37-117">Azure CLI-kommandogruppen</span><span class="sxs-lookup"><span data-stu-id="fbd37-117">Azure CLI command group</span></span> |
|---------------|-------------------------|
| [<span data-ttu-id="fbd37-118">Resursgrupp</span><span class="sxs-lookup"><span data-stu-id="fbd37-118">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="fbd37-119">az group</span><span class="sxs-lookup"><span data-stu-id="fbd37-119">az group</span></span>](/cli/azure/group) |
| [<span data-ttu-id="fbd37-120">Virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="fbd37-120">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="fbd37-121">az vm</span><span class="sxs-lookup"><span data-stu-id="fbd37-121">az vm</span></span>](/cli/azure/vm) |
| [<span data-ttu-id="fbd37-122">Lagringskonton</span><span class="sxs-lookup"><span data-stu-id="fbd37-122">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="fbd37-123">az storage account</span><span class="sxs-lookup"><span data-stu-id="fbd37-123">az storage account</span></span>](/cli/azure/storage/account) |
| [<span data-ttu-id="fbd37-124">Key Vault</span><span class="sxs-lookup"><span data-stu-id="fbd37-124">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="fbd37-125">az keyvault</span><span class="sxs-lookup"><span data-stu-id="fbd37-125">az keyvault</span></span>](/cli/azure/keyvault) |
| [<span data-ttu-id="fbd37-126">Webbprogram</span><span class="sxs-lookup"><span data-stu-id="fbd37-126">Web applications</span></span>](/azure/ap-service) | [<span data-ttu-id="fbd37-127">az webapp</span><span class="sxs-lookup"><span data-stu-id="fbd37-127">az webapp</span></span>](/cli/azure/webapp) |
| [<span data-ttu-id="fbd37-128">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fbd37-128">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="fbd37-129">az sql server</span><span class="sxs-lookup"><span data-stu-id="fbd37-129">az sql server</span></span>](/cli/azure/sql/server) |
| [<span data-ttu-id="fbd37-130">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fbd37-130">CosmosDB</span></span>](/azure/cosmos-db) | [<span data-ttu-id="fbd37-131">az cosmosdb</span><span class="sxs-lookup"><span data-stu-id="fbd37-131">az cosmosdb</span></span>](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a><span data-ttu-id="fbd37-132">Hitta kommandon</span><span class="sxs-lookup"><span data-stu-id="fbd37-132">Finding commands</span></span>

<span data-ttu-id="fbd37-133">Kommandon i CLI tillhandahålls som _underkommandon_ av _grupper_.</span><span class="sxs-lookup"><span data-stu-id="fbd37-133">Commands in the CLI are provided as _subcommands_ of _groups_.</span></span>
<span data-ttu-id="fbd37-134">Varje grupp representerar en tjänst som tillhandahålls av Azure och undergrupperna delar upp kommandon för de här tjänsterna i logiska grupper.</span><span class="sxs-lookup"><span data-stu-id="fbd37-134">Each group represents a service provided by Azure, and the subgroups divide commands for these services into logical groupings.</span></span>

<span data-ttu-id="fbd37-135">Använd [az find](/cli/azure/reference-index#az_find) om du vill söka efter kommandon.</span><span class="sxs-lookup"><span data-stu-id="fbd37-135">To search for commands, use [az find](/cli/azure/reference-index#az_find).</span></span> <span data-ttu-id="fbd37-136">Om du till exempel vill söka efter kommandonamn som innehåller `secret` kan du använda följande kommando:</span><span class="sxs-lookup"><span data-stu-id="fbd37-136">For example, to search for command names containing `secret`, use the following command:</span></span>

```azurecli
az find -q secret
```

<span data-ttu-id="fbd37-137">Om du vet vilken grupp av kommandon som du vill arbeta med kan argumentet `--help` vara ett bättre alternativ.</span><span class="sxs-lookup"><span data-stu-id="fbd37-137">If you know which group of commands you want to work with, the `--help` argument may be a better choice.</span></span> <span data-ttu-id="fbd37-138">Det visar inte bara detaljerad information om ett kommando, utan visar även alla tillgängliga underkommandon när det används med en kommandogrupp.</span><span class="sxs-lookup"><span data-stu-id="fbd37-138">This displays not just detailed information for a command, but when used with a command group, displays all of the available subcommands.</span></span> <span data-ttu-id="fbd37-139">Om du till exempel arbetar med nätverkssäkerhetsgrupper (NSG) kan du hitta de tillgängliga NSG-undergrupperna och kommandona.</span><span class="sxs-lookup"><span data-stu-id="fbd37-139">For example, when working with Network Security Groups (NSGs) you can find the available NSG subgroups and commands.</span></span>

```azurecli
az network nsg --help
```

<span data-ttu-id="fbd37-140">CLI har en funktion för tabbifyllning för kommandon under Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="fbd37-140">The CLI has full tab completion for commands under the bash shell.</span></span>

## <a name="globally-available-arguments"></a><span data-ttu-id="fbd37-141">Globalt tillgängliga argument</span><span class="sxs-lookup"><span data-stu-id="fbd37-141">Globally available arguments</span></span>

<span data-ttu-id="fbd37-142">Det finns vissa argument som är tillgängliga för varje kommando.</span><span class="sxs-lookup"><span data-stu-id="fbd37-142">There are some arguments that are available for every command.</span></span>

* <span data-ttu-id="fbd37-143">`--help` skriver ut CLI-referensinformation om kommandon och deras argument samt visar en lista över tillgängliga undergrupper och kommandon.</span><span class="sxs-lookup"><span data-stu-id="fbd37-143">`--help` prints CLI reference information about commands and their arguments and lists available subgroups and commands.</span></span>
* <span data-ttu-id="fbd37-144">`--output` ändrar utdataformat.</span><span class="sxs-lookup"><span data-stu-id="fbd37-144">`--output` changes the output format.</span></span> <span data-ttu-id="fbd37-145">De tillgängliga utdataformaten är `json`, `jsonc` (färglagd JSON) `tsv` (tabbavgränsade värden) och `table` (läsbara ASCII-tabeller).</span><span class="sxs-lookup"><span data-stu-id="fbd37-145">The available output formats are `json`, `jsonc` (colorized JSON), `tsv` (Tab-Separated Values), and `table` (human-readable ASCII tables).</span></span> <span data-ttu-id="fbd37-146">Som standard matar CLI ut `json`.</span><span class="sxs-lookup"><span data-stu-id="fbd37-146">By default the CLI outputs `json`.</span></span> <span data-ttu-id="fbd37-147">Om du vill lära dig mer om andra utdataformat kan du läsa informationen i [Utdataformat för Azure CLI 2.0](format-output-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="fbd37-147">To learn more about the available output formats, see [Output formats for Azure CLI 2.0](format-output-azure-cli.md).</span></span>
* <span data-ttu-id="fbd37-148">`--query` använder [JMESPath-frågespråket](http://jmespath.org/) för att filtrera utdata som returneras från Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="fbd37-148">`--query` uses the [JMESPath query language](http://jmespath.org/) to filter the output returned from Azure services.</span></span> <span data-ttu-id="fbd37-149">Mer information om hur du skickar frågor finns i [Använda JMESPath-frågor med Azure CLI 2.0](query-azure-cli.md) och [självstudien för JMESPath](http://jmespath.org/tutorial.html).</span><span class="sxs-lookup"><span data-stu-id="fbd37-149">To learn To learn more about queries, see [Query command results with Azure CLI 2.0](query-azure-cli.md) and the [JMESPath tutorial](http://jmespath.org/tutorial.html).</span></span>
* <span data-ttu-id="fbd37-150">`--verbose` skriver ut information om resurser som skapats i Azure när en åtgärd utförs och annan användbar information.</span><span class="sxs-lookup"><span data-stu-id="fbd37-150">`--verbose` prints information about resources created in Azure during an operation, and other useful information.</span></span>
* <span data-ttu-id="fbd37-151">`--debug` skriver ut mer information om CLI-åtgärder som kan användas för felsökning.</span><span class="sxs-lookup"><span data-stu-id="fbd37-151">`--debug` prints even more information about CLI operations, used for debugging purposes.</span></span> <span data-ttu-id="fbd37-152">Om en bugg uppstår kan du tillhandahålla utdata som genererats med flaggan `--debug` när du skickar en felrapport.</span><span class="sxs-lookup"><span data-stu-id="fbd37-152">If you encounter a bug, provide output generated with the `--debug` flag on when submitting a bug report.</span></span>


## <a name="interactive-mode"></a><span data-ttu-id="fbd37-153">Interaktivt läge</span><span class="sxs-lookup"><span data-stu-id="fbd37-153">Interactive mode</span></span>

<span data-ttu-id="fbd37-154">CLI erbjuder ett interaktivt läge som automatiskt visar hjälpinformation och gör det lättare att välja underkommandon.</span><span class="sxs-lookup"><span data-stu-id="fbd37-154">The CLI offers an interactive mode that automatically displays help information and makes it easier to select subcommands.</span></span> <span data-ttu-id="fbd37-155">Du aktiverar det interaktiva läget med kommandot `az interactive`.</span><span class="sxs-lookup"><span data-stu-id="fbd37-155">You enter interactive mode with the `az interactive` command.</span></span> <span data-ttu-id="fbd37-156">Mer information om det interaktiva läget och hur det hjälper dig att använda CLI finns i informationen om det [interaktiva läget i Azure CLI 2.0](interactive-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="fbd37-156">For more information on interactive mode and how it helps you learn the CLI, see [Azure CLI 2.0 Interactive Mode](interactive-azure-cli.md).</span></span>

<span data-ttu-id="fbd37-157">Det finns även ett [plugin-program för Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) som ger en interaktiv upplevelse med automatisk komplettering och dokumentation som du kan hovra över.</span><span class="sxs-lookup"><span data-stu-id="fbd37-157">There is also a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) that offers an interactive experience, including autocomplete and mouse-over documentation.</span></span>



## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="fbd37-158">Lär dig grunderna i CLI med snabbstarter och självstudier</span><span class="sxs-lookup"><span data-stu-id="fbd37-158">Learn CLI basics with quickstarts and tutorials</span></span>

<span data-ttu-id="fbd37-159">Om du vill komma igång med Azure CLI 2.0 kan du titta närmare på en djupgående självstudie som hjälper dig att konfigurera virtuella datorer och använda CLI för att fråga Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="fbd37-159">To get you started with the Azure CLI 2.0, try an in-depth tutorial for setting up virtual machines and using the power of the CLI to query Azure resources.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="fbd37-160">Självstudie för att skapa en virtuell dator med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="fbd37-160">Create virtual machines with the Azure CLI 2.0 tutorial</span></span>](azure-cli-vm-tutorial.yml)

<span data-ttu-id="fbd37-161">Om du istället vill fokusera på andra tjänster så finns det en mängd olika snabbstarter för Azure-tjänster som använder CLI.</span><span class="sxs-lookup"><span data-stu-id="fbd37-161">If you would rather focus on other services, there are a variety of quickstarts for Azure services that use the CLI.</span></span>

* [<span data-ttu-id="fbd37-162">Skapa ett lagringskonto med Azure CLI</span><span class="sxs-lookup"><span data-stu-id="fbd37-162">Create a storage account using the Azure CLI</span></span>](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [<span data-ttu-id="fbd37-163">Överföra objekt till och från Azure Blob Storage med hjälp av CLI</span><span class="sxs-lookup"><span data-stu-id="fbd37-163">Transfer objects to/from Azure Blob storage using the CLI</span></span>](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [<span data-ttu-id="fbd37-164">Skapa en enskild Azure SQL-databas med Azure CLI</span><span class="sxs-lookup"><span data-stu-id="fbd37-164">Create a single Azure SQL database using the Azure CLI</span></span>](/azure/sql-database/sql-database-get-started-cli)
* [<span data-ttu-id="fbd37-165">Skapa en Azure Database for MySQL-server med Azure CLI</span><span class="sxs-lookup"><span data-stu-id="fbd37-165">Create an Azure Database for MySQL server using the Azure CLI</span></span>](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [<span data-ttu-id="fbd37-166">Skapa en Azure Database for PostgreSQL med hjälp av Azure-CLI:n</span><span class="sxs-lookup"><span data-stu-id="fbd37-166">Create an Azure Database for PostgreSQL using the Azure CLI</span></span>](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [<span data-ttu-id="fbd37-167">Skapa en Python-webbapp i Azure</span><span class="sxs-lookup"><span data-stu-id="fbd37-167">Create a Python web app in Azure</span></span>](/azure/app-service/app-service-web-get-started-python)
* [<span data-ttu-id="fbd37-168">Kör en anpassad Docker Hub-avbildning i Azure Web Apps for Containers</span><span class="sxs-lookup"><span data-stu-id="fbd37-168">Run a custom Docker Hub image in Azure Web Apps for Containers</span></span>](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a><span data-ttu-id="fbd37-169">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="fbd37-169">Give feedback</span></span>

<span data-ttu-id="fbd37-170">Vi uppskattar din feedback om CLI som hjälper oss att göra förbättringar och korrigera buggar.</span><span class="sxs-lookup"><span data-stu-id="fbd37-170">We welcome your feedback for the CLI to help us make improvements and resolve bugs.</span></span> <span data-ttu-id="fbd37-171">Du kan [öppna ett Github-supportärende](https://github.com/azure/azure-cli/issues) eller använda de inbyggda funktionerna i CLI för att lämna allmän feedback med kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="fbd37-171">You can [file an issue on Github](https://github.com/azure/azure-cli/issues) or use the built-in features of the CLI to leave general feedback with the `az feedback` command.</span></span>

```azurecli
az feedback
```
