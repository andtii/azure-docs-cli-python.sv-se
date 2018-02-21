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
ms.openlocfilehash: c2758922d74080d3a3110b1e3a507ddf0f8d85d1
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="get-started-with-azure-cli-20"></a>Kom igång med Azure CLI 2.0

Välkommen till Azure CLI 2.0! CLI är ett verktyg som är utformat för att du ska kunna arbeta snabbt och effektivt med Azure-tjänster, med fokus på automatisering. I den här artikeln beskrivs funktionerna i CLI och du får länkar till resurser som hjälper dig vara produktiv.

## <a name="install-and-log-in"></a>Installera och logga in

Om du inte redan har gjort det så kan du [installera CLI](install-azure-cli.md) eller testa [Azure Cloud Shell](/azure/cloud-shell/overview).

Innan du använder CLI-kommandon med en lokal installation måste du logga in med [az login](/cli/azure/index#az_login).

```azurecli
az login
```

Med det här kommandot kan du logga in med en autentiseringskod via en webbplats. Det finns några olika sätt att logga in som inte är interaktiva. Läs mer i [Logga in med Azure CLI 2.0](authenticate-azure-cli.md).

## <a name="common-commands"></a>Vanliga kommandon

Den här tabellen innehåller några vanliga kommandon som används i CLI-länkarna till dokumentationssidorna i referensen.
Du hittar alla underkommandon i de här grupperna och deras dokumentation i onlinereferenserna eller med argumentet `--help`.

| Resurstyp | Azure CLI-kommandogruppen |
|---------------|-------------------------|
| [Resursgrupp](/azure/azure-resource-manager/resource-group-overview) | [az group](/cli/azure/group) |
| [Virtuella datorer](/azure/virtual-machines) | [az vm](/cli/azure/vm) |
| [Lagringskonton](/azure/storage/common/storage-introduction) | [az storage account](/cli/azure/storage/account) |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [az keyvault](/cli/azure/keyvault) |
| [Webbprogram](/azure/ap-service) | [az webapp](/cli/azure/webapp) |
| [SQL-databaser](/azure/sql-database) | [az sql server](/cli/azure/sql/server) |
| [CosmosDB](/azure/cosmos-db) | [az cosmosdb](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a>Hitta kommandon

Kommandon i CLI tillhandahålls som _underkommandon_ av _grupper_.
Varje grupp representerar en tjänst som tillhandahålls av Azure och undergrupperna delar upp kommandon för de här tjänsterna i logiska grupper.

Använd [az find](/cli/azure/index#az_find) om du vill söka efter kommandon. Om du till exempel vill söka efter kommandonamn som innehåller `secret` kan du använda följande kommando:

```azurecli
az find -q secret
```

Om du vet vilken grupp av kommandon som du vill arbeta med kan argumentet `--help` vara ett bättre alternativ. Det visar inte bara detaljerad information om ett kommando, utan visar även alla tillgängliga underkommandon när det används med en kommandogrupp. Om du till exempel arbetar med nätverkssäkerhetsgrupper (NSG) kan du hitta de tillgängliga NSG-undergrupperna och kommandona.

```azurecli
az network nsg --help
```

CLI har en funktion för tabbifyllning för kommandon under Bash-gränssnittet.

## <a name="globally-available-arguments"></a>Globalt tillgängliga argument

Det finns vissa argument som är tillgängliga för varje kommando.

* `--help` skriver ut CLI-referensinformation om kommandon och deras argument samt visar en lista över tillgängliga undergrupper och kommandon.
* `--output` ändrar utdataformat. De tillgängliga utdataformaten är `json`, `jsonc` (färglagd JSON) `tsv` (tabbavgränsade värden) och `table` (läsbara ASCII-tabeller). Som standard matar CLI ut `json`. Om du vill lära dig mer om andra utdataformat kan du läsa informationen i [Utdataformat för Azure CLI 2.0](format-output-azure-cli.md).
* `--query` använder [JMESPath-frågespråket](http://jmespath.org/) för att filtrera utdata som returneras från Azure-tjänster. Mer information om hur du skickar frågor finns i [Använda JMESPath-frågor med Azure CLI 2.0](query-azure-cli.md) och [självstudien för JMESPath](http://jmespath.org/tutorial.html).
* `--verbose` skriver ut information om resurser som skapats i Azure när en åtgärd utförs och annan användbar information.
* `--debug` skriver ut mer information om CLI-åtgärder som kan användas för felsökning. Om en bugg uppstår kan du tillhandahålla utdata som genererats med flaggan `--debug` när du skickar en felrapport.


## <a name="interactive-mode"></a>Interaktivt läge

CLI erbjuder ett interaktivt läge som automatiskt visar hjälpinformation och gör det lättare att välja underkommandon. Du aktiverar det interaktiva läget med kommandot `az interactive`. Mer information om det interaktiva läget och hur det hjälper dig att använda CLI finns i informationen om det [interaktiva läget i Azure CLI 2.0](interactive-azure-cli.md).

Det finns även ett [plugin-program för Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) som ger en interaktiv upplevelse med automatisk komplettering och dokumentation som du kan hovra över.



## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a>Lär dig grunderna i CLI med snabbstarter och självstudier

Om du vill komma igång med Azure CLI 2.0 kan du titta närmare på en djupgående självstudie som hjälper dig att konfigurera virtuella datorer och använda CLI för att fråga Azure-resurser.

> [!div class="nextstepaction"]
> [Självstudie för att skapa en virtuell dator med Azure CLI 2.0](azure-cli-vm-tutorial.yml)

Om du istället vill fokusera på andra tjänster så finns det en mängd olika snabbstarter för Azure-tjänster som använder CLI.

* [Skapa ett lagringskonto med Azure CLI](/azure/storage/common/storage-quickstart-create-storage-account-cl)
* [Överföra objekt till och från Azure Blob Storage med hjälp av CLI](/storage/blobs/storage-quickstart-blobs-cli)
* [Skapa en enskild Azure SQL-databas med Azure CLI](/azure/sql-database/sql-database-get-started-cli)
* [Skapa en Azure Database for MySQL-server med Azure CLI](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [Skapa en Azure Database for PostgreSQL med hjälp av Azure-CLI:n](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [Skapa en Python-webbapp i Azure](/azure/app-service/app-service-web-get-started-python)
* [Kör en anpassad Docker Hub-avbildning i Azure Web Apps for Containers](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a>Ge feedback

Vi uppskattar din feedback om CLI som hjälper oss att göra förbättringar och korrigera buggar. Du kan [öppna ett Github-supportärende](https://github.com/azure/azure-cli/issues) eller använda de inbyggda funktionerna i CLI för att lämna allmän feedback med kommandot `az feedback`.

```azurecli
az feedback
```
