---
title: "Frågekommandoutdata med Azure CLI 2.0"
description: "Lär dig hur du utför JMESPath-frågor för utdata för Azure CLI 2.0-kommandon."
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/22/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 96092c0cced4e0f88aa8898525bc3dd348550407
ms.sourcegitcommit: 29d7366a0902488f4f4d39c2cb0e89368d5186ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="1e970-103">Använda JMESPath-frågor med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="1e970-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="1e970-104">Azure CLI 2.0 använder argumentet `--query` för att utföra en [JMESPath-fråga](http://jmespath.org) på resultaten från kommandon.</span><span class="sxs-lookup"><span data-stu-id="1e970-104">The Azure CLI 2.0 uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="1e970-105">JMESPath är ett frågespråk för JSON som ger dig möjlighet att välja och visa data från CLI-utdata.</span><span class="sxs-lookup"><span data-stu-id="1e970-105">JMESPath is a query language for JSON, giving you the ability to select and present data from CLI output.</span></span> <span data-ttu-id="1e970-106">De här frågorna körs på JSON-utdata innan någon annan visningsformatering utförs.</span><span class="sxs-lookup"><span data-stu-id="1e970-106">These queries are executed on the JSON output, before performing any other display formatting.</span></span>

<span data-ttu-id="1e970-107">Argumentet `--query` stöds av alla kommandon i Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="1e970-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="1e970-108">Exemplen i den här artikeln beskriver vanliga användarsituationer och visar hur du använder funktionerna för JMESPath.</span><span class="sxs-lookup"><span data-stu-id="1e970-108">This article's examples cover common use cases and demonstrate how to use the features of JMESPath.</span></span>

## <a name="work-with-dictionary-output"></a><span data-ttu-id="1e970-109">Arbeta med ordlisteutdata</span><span class="sxs-lookup"><span data-stu-id="1e970-109">Work with dictionary output</span></span>

<span data-ttu-id="1e970-110">Kommandon som returnerar en JSON-ordlista kan endast undersökas efter nyckelnamn.</span><span class="sxs-lookup"><span data-stu-id="1e970-110">Commands that return a JSON dictionary can be explored by their key names alone.</span></span> <span data-ttu-id="1e970-111">Nyckelsökvägen använder `.`-tecken som avgränsare.</span><span class="sxs-lookup"><span data-stu-id="1e970-111">Key paths use the `.` character as a separator.</span></span> <span data-ttu-id="1e970-112">I följande exempel hämtas en lista över de offentliga SSH-nycklar som kan ansluta till en virtuell Linux-dator:</span><span class="sxs-lookup"><span data-stu-id="1e970-112">The following example pulls a list of the public SSH keys allowed to connect to a Linux VM:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

<span data-ttu-id="1e970-113">Du kan även få flera värden genom att placera dem i en sorterad matris.</span><span class="sxs-lookup"><span data-stu-id="1e970-113">You can also get multiple values, putting them in an ordered array.</span></span> <span data-ttu-id="1e970-114">Matrisen har inte någon viktig information men ordningen för matrisens element matchar ordningen på de efterfrågade nycklarna.</span><span class="sxs-lookup"><span data-stu-id="1e970-114">The array doesn't have any key information, but the order of the array's elements matches the order of the queried keys.</span></span> <span data-ttu-id="1e970-115">Följande exempel visar hur du hämtar erbjudandenamnet för Azure-avbildningen och storleken på operativsystemdisken:</span><span class="sxs-lookup"><span data-stu-id="1e970-115">The following example shows how to retrieve the Azure image offering name and the size of the OS disk:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

<span data-ttu-id="1e970-116">Om du vill använda nycklar i dina utdata kan du använda en annan syntax för ordlistan.</span><span class="sxs-lookup"><span data-stu-id="1e970-116">If you want keys in your output, you can use an alternate dictionary syntax.</span></span> <span data-ttu-id="1e970-117">Många elementval i en ordlista använder formatet `{displayKey:keyPath, ...}` för att filtrera på JMESPath-uttrycket `keyPath`.</span><span class="sxs-lookup"><span data-stu-id="1e970-117">Multiple element selection into a dictionary uses the format `{displayKey:keyPath, ...}` to filter on the `keyPath` JMESPath expression.</span></span> <span data-ttu-id="1e970-118">Det här visas i utdata som `{displayKey: value}`.</span><span class="sxs-lookup"><span data-stu-id="1e970-118">This displays in the output as `{displayKey: value}`.</span></span> <span data-ttu-id="1e970-119">Nästa exempel tar det senaste exemplets fråga och gör den tydligare genom att tilldela nycklar till dess utdata:</span><span class="sxs-lookup"><span data-stu-id="1e970-119">The next example takes the last example's query, and makes it clearer by assigning keys to the output:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

<span data-ttu-id="1e970-120">När du visar informationen i utdataformatet `table` är ordlistevyn särskilt användbar.</span><span class="sxs-lookup"><span data-stu-id="1e970-120">When displaying information in the `table` output format, dictionary display is especially useful.</span></span> <span data-ttu-id="1e970-121">Det här gör det möjligt att ställa in egna kolumnrubriker och gör det ännu enklare att läsa utdata.</span><span class="sxs-lookup"><span data-stu-id="1e970-121">This allows for setting your own column headers, making output even easier to read.</span></span> <span data-ttu-id="1e970-122">Mer information om utdataformat finns i [Utdataformat för Azure CLI 2.0-kommandon](/cli/azure/format-output-azure-cli).</span><span class="sxs-lookup"><span data-stu-id="1e970-122">For more information on output formats, see [Output formats for Azure CLI 2.0 commands](/cli/azure/format-output-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="1e970-123">Vissa nycklar filtreras bort och skrivs inte ut i tabellvyn.</span><span class="sxs-lookup"><span data-stu-id="1e970-123">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="1e970-124">De här nycklarna är `id`, `type` och `etag`.</span><span class="sxs-lookup"><span data-stu-id="1e970-124">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="1e970-125">Om du behöver se den här informationen kan du ändra nyckelnamnet och undvika filtrering.</span><span class="sxs-lookup"><span data-stu-id="1e970-125">If you need to see this information, you can change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a><span data-ttu-id="1e970-126">Arbeta med utdata från lista</span><span class="sxs-lookup"><span data-stu-id="1e970-126">Work with list output</span></span>

<span data-ttu-id="1e970-127">CLI-kommandon som kan returnera fler än ett värde returnerar alltid en matris.</span><span class="sxs-lookup"><span data-stu-id="1e970-127">CLI commands that may return more than one value always return an array.</span></span> <span data-ttu-id="1e970-128">Matrisernas element kan användas av index, men det finns aldrig en ordningsgaranti från CLI.</span><span class="sxs-lookup"><span data-stu-id="1e970-128">Arrays can have their elements accessed by index, but there's never an order guarantee from the CLI.</span></span> <span data-ttu-id="1e970-129">Det bästa sättet att fråga en matris med värden är att platta ut dem med operatorn `[]`.</span><span class="sxs-lookup"><span data-stu-id="1e970-129">The best way to query an array of values is to flatten them with the `[]` operator.</span></span> <span data-ttu-id="1e970-130">Operatorn skrivs efter nyckeln för matrisen eller som det första elementet i uttrycket.</span><span class="sxs-lookup"><span data-stu-id="1e970-130">The operator is written after the key for the array, or as the first element in the expression.</span></span> <span data-ttu-id="1e970-131">Genom att platta ut körs frågan efter den mot varje enskilt element i matrisen och resultatvärdena placeras i en ny matris.</span><span class="sxs-lookup"><span data-stu-id="1e970-131">Flattening runs the query following it against each individual element in the array, and places the resulting values into a new array.</span></span> <span data-ttu-id="1e970-132">Följande exempel skriver ut namnet och operativsystemet som körs på varje virtuell dator i en resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="1e970-132">The following example prints out the name and OS running on each VM in a resource group.</span></span> 

```azurecli
az vm list -g QueryDemo --query '[].{name:name, image:storageProfile.imageReference.offer}'
```

```json
[
  {
    "image": "CentOS",
    "name": "CentBox"
  },
  {
    "image": "openSUSE-Leap",
    "name": "SUSEBox"
  },
  {
    "image": "UbuntuServer",
    "name": "TestVM"
  },
  {
    "image": "UbuntuServer",
    "name": "Test2"
  },
  {
    "image": "WindowsServer",
    "name": "WinServ"
  }
]
```

<span data-ttu-id="1e970-133">Matriser som ingår i en nyckelsökväg kan också plattas ut.</span><span class="sxs-lookup"><span data-stu-id="1e970-133">Arrays that are part of a key path can be flattened as well.</span></span> <span data-ttu-id="1e970-134">Det här exemplet visar en fråga som hämtar ID för Azure-objekt för de nätverkskort som en virtuell dator är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="1e970-134">This example demonstrates a query that gets the Azure object IDs for the NICs a VM is connected to.</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a><span data-ttu-id="1e970-135">Filtrera matrisutdata med predikat</span><span class="sxs-lookup"><span data-stu-id="1e970-135">Filter array output with predicates</span></span>

<span data-ttu-id="1e970-136">JMESPath erbjuder [filtreringsuttryck](http://jmespath.org/specification.html#filterexpressions) för att filtrera bort de data som visas.</span><span class="sxs-lookup"><span data-stu-id="1e970-136">JMESPath offers [filtering expressions](http://jmespath.org/specification.html#filterexpressions) to filter out the data displayed.</span></span> <span data-ttu-id="1e970-137">De här uttrycken är kraftfulla, särskilt när de kombineras med [inbyggda JMESPath-funktioner](http://jmespath.org/specification.html#built-in-functions) för att utföra delmatchningar eller ändra data till ett standardformat.</span><span class="sxs-lookup"><span data-stu-id="1e970-137">These expressions are powerful, especially when combined with [JMESPath built-in functions](http://jmespath.org/specification.html#built-in-functions) to perform partial matches or manipulate data into a standard format.</span></span> <span data-ttu-id="1e970-138">Det går endast att filtrera uttryck på matrisdata och när metoden används i andra fall returneras värdet `null`.</span><span class="sxs-lookup"><span data-stu-id="1e970-138">Filtering expressions only work on array data, and when used in any other situation, return the `null` value.</span></span> <span data-ttu-id="1e970-139">Du kan till exempel ta utdata från kommandon som `vm list` och filtrera på dem för att söka efter specifika typer av virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="1e970-139">For example, you can take the output of commands like `vm list` and filter on it to look for specific types of VMs.</span></span> <span data-ttu-id="1e970-140">Följande exempel utvecklar det tidigare exemplet genom att filtrera bort VM-typen för att endast visa virtuella Windows-datorer och skriva ut deras namn.</span><span class="sxs-lookup"><span data-stu-id="1e970-140">The following example expands on the previous by filtering out the VM type to capture only Windows VMs and print their name.</span></span>

```azurecli
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="1e970-141">Experimentera med frågor interaktivt</span><span class="sxs-lookup"><span data-stu-id="1e970-141">Experiment with queries interactively</span></span>

<span data-ttu-id="1e970-142">Om du vill experimentera med JMESPath-uttryck kanske du vill arbeta på ett sätt där du snabbt kan redigera frågor och inspektera utdata.</span><span class="sxs-lookup"><span data-stu-id="1e970-142">To experiment with JMESPath expressions, you might want to work in a way where you can quickly edit queries and inspect the output.</span></span> <span data-ttu-id="1e970-143">Med [JMESPath-terminalens](https://github.com/jmespath/jmespath.terminal) Python-paket får du en interaktiv miljö där du kan dirigera data som indata och sedan skriva frågor i programmet för att extrahera data.</span><span class="sxs-lookup"><span data-stu-id="1e970-143">An interactive environment is offered by the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package, which allows for piping data as input and then writing in-program queries to extract the data.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
