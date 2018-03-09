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
# <a name="use-jmespath-queries-with-azure-cli-20"></a>Använda JMESPath-frågor med Azure CLI 2.0

Azure CLI 2.0 använder argumentet `--query` för att utföra en [JMESPath-fråga](http://jmespath.org) på resultaten från kommandon. JMESPath är ett frågespråk för JSON som ger dig möjlighet att välja och visa data från CLI-utdata. De här frågorna körs på JSON-utdata innan någon annan visningsformatering utförs.

Argumentet `--query` stöds av alla kommandon i Azure CLI. Exemplen i den här artikeln beskriver vanliga användarsituationer och visar hur du använder funktionerna för JMESPath.

## <a name="work-with-dictionary-output"></a>Arbeta med ordlisteutdata

Kommandon som returnerar en JSON-ordlista kan endast undersökas efter nyckelnamn. Nyckelsökvägen använder `.`-tecken som avgränsare. I följande exempel hämtas en lista över de offentliga SSH-nycklar som kan ansluta till en virtuell Linux-dator:

```azurecli
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

Du kan även få flera värden genom att placera dem i en sorterad matris. Matrisen har inte någon viktig information men ordningen för matrisens element matchar ordningen på de efterfrågade nycklarna. Följande exempel visar hur du hämtar erbjudandenamnet för Azure-avbildningen och storleken på operativsystemdisken:

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

Om du vill använda nycklar i dina utdata kan du använda en annan syntax för ordlistan. Många elementval i en ordlista använder formatet `{displayKey:keyPath, ...}` för att filtrera på JMESPath-uttrycket `keyPath`. Det här visas i utdata som `{displayKey: value}`. Nästa exempel tar det senaste exemplets fråga och gör den tydligare genom att tilldela nycklar till dess utdata:

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

När du visar informationen i utdataformatet `table` är ordlistevyn särskilt användbar. Det här gör det möjligt att ställa in egna kolumnrubriker och gör det ännu enklare att läsa utdata. Mer information om utdataformat finns i [Utdataformat för Azure CLI 2.0-kommandon](/cli/azure/format-output-azure-cli).

> [!NOTE]
> Vissa nycklar filtreras bort och skrivs inte ut i tabellvyn. De här nycklarna är `id`, `type` och `etag`. Om du behöver se den här informationen kan du ändra nyckelnamnet och undvika filtrering.
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a>Arbeta med utdata från lista

CLI-kommandon som kan returnera fler än ett värde returnerar alltid en matris. Matrisernas element kan användas av index, men det finns aldrig en ordningsgaranti från CLI. Det bästa sättet att fråga en matris med värden är att platta ut dem med operatorn `[]`. Operatorn skrivs efter nyckeln för matrisen eller som det första elementet i uttrycket. Genom att platta ut körs frågan efter den mot varje enskilt element i matrisen och resultatvärdena placeras i en ny matris. Följande exempel skriver ut namnet och operativsystemet som körs på varje virtuell dator i en resursgrupp. 

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

Matriser som ingår i en nyckelsökväg kan också plattas ut. Det här exemplet visar en fråga som hämtar ID för Azure-objekt för de nätverkskort som en virtuell dator är ansluten till.

```azurecli
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a>Filtrera matrisutdata med predikat

JMESPath erbjuder [filtreringsuttryck](http://jmespath.org/specification.html#filterexpressions) för att filtrera bort de data som visas. De här uttrycken är kraftfulla, särskilt när de kombineras med [inbyggda JMESPath-funktioner](http://jmespath.org/specification.html#built-in-functions) för att utföra delmatchningar eller ändra data till ett standardformat. Det går endast att filtrera uttryck på matrisdata och när metoden används i andra fall returneras värdet `null`. Du kan till exempel ta utdata från kommandon som `vm list` och filtrera på dem för att söka efter specifika typer av virtuella datorer. Följande exempel utvecklar det tidigare exemplet genom att filtrera bort VM-typen för att endast visa virtuella Windows-datorer och skriva ut deras namn.

```azurecli
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a>Experimentera med frågor interaktivt

Om du vill experimentera med JMESPath-uttryck kanske du vill arbeta på ett sätt där du snabbt kan redigera frågor och inspektera utdata. Med [JMESPath-terminalens](https://github.com/jmespath/jmespath.terminal) Python-paket får du en interaktiv miljö där du kan dirigera data som indata och sedan skriva frågor i programmet för att extrahera data.

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
