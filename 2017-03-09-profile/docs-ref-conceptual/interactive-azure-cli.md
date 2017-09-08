---
title: "Azure CLI 2.0 i interaktivt läge"
description: "Använd Azure CLI 2.0 i interaktivt läge."
keywords: Azure CLI 2.0, interactive mode
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 
ms.openlocfilehash: de6a366b84efa5475fd6146ff29c32e32dfe4672
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/04/2017
---
# <a name="interactive-azure-cli-20"></a>Interaktivt Azure CLI 2.0

Du kan använda Azure CLI 2.0 i interaktivt läge genom att köra kommandot `az interactive`.
När du gör det öppnas ett interaktivt gränssnitt där dina kommandon kompletteras automatisk och där du kan komma åt beskrivningar av kommandon och deras parametrar och kommandoexempel.

![interaktivt läge](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> Vi använder inte standardformatet här eftersom det är svårläst mot en svart bakgrund.

Om du inte redan är inloggad på ditt konto loggar du in med kommandot `login`.

## <a name="configure"></a>Konfigurera

I interaktivt läge kan du välja att visa kommandobeskrivningar, parameterbeskrivningar och kommandoexempel.
Du kan aktivera och inaktivera beskrivningar och exempel med `F1`.

![beskrivningar och exempel](./media/interactive-azure-cli/descriptions-and-examples.png)

Du kan aktivera och inaktivera visningen av standardvärden för parametrar med `F2`.

![standardvärden](./media/interactive-azure-cli/defaults.png)

`F3` aktiverar eller inaktiverar visningen av vissa tangentfunktioner.

![tangentfunktioner](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a>Omfång

Du kan begränsa det interaktiva läget till en specifik kommandogrupp som `vm` eller `vm image`.
Om du gör det tolkas alla kommandon i det omfånget.
Det är en bra genväg om du utför allt arbete i den kommandogruppen.

I stället för att skriva följande kommandon:

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

Kan du begränsa omfånget till vm command-gruppen och skriva dessa kommandon:

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

Du kan även begränsa omfånget till kommandon på lägre nivå.
Du kan till exempel begränsa omfånget till `vm image` med hjälp av `%%vm image`.
I detta fall, eftersom vi redan har begränsat omfånget till `vm`, använder vi `%%image`.

```azurecli
az vm>> %%image
az vm image>>
```

Därifrån kan vi ändra tillbaka omfånget till `vm` med hjälp av `%%..`, eller använda roten som omfång med bara `%%`.

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a>Fråga

Du kan köra en JMESPath-fråga mot resultatet från det sista kommandot som du körde.
Till exempel kan du när du har skapat en virtuell dator kontrollera att den har etablerats.

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

Mer information om hur du skickar frågor mot resultatet från kommandon finns i [Använda JMESPath-frågor med Azure CLI 2.0](query-azure-cli.md).

## <a name="bash-commands"></a>Bash-kommandon

Du kan köra shell-kommandon utan att lämna interaktivt läge med hjälp av `#[cmd]`.

```azurecli
az>> #dir
```

## <a name="examples"></a>Exempel

Vissa kommandon har flera exempel.
Du kan bläddra till nästa sida med exempel med `CTRL-N` och till föregående sida med `CTRL-Y`.

![exempel](./media/interactive-azure-cli/examples.png)

Du kan också visa ett specifikt exempel med `::#`.

```azurecli
az>> vm create ::8
```
