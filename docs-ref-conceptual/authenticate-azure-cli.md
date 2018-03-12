---
title: Logga in med Azure CLI 2.0
description: Logga in med Azure CLI 2.0 interaktivt eller med lokala autentiseringsuppgifter
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 92c96b7e969de686689ef02bf068392b9f565698
ms.sourcegitcommit: 29d7366a0902488f4f4d39c2cb0e89368d5186ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2018
---
# <a name="log-in-with-azure-cli-20"></a>Logga in med Azure CLI 2.0

Du kan logga in och autentisera med Azure CLI på flera olika sätt. Det enklaste sättet att komma igång är genom att logga in interaktivt via webbläsaren med hjälp av antingen Azure Cloud Shell eller kommandot `az login`.
Den rekommenderade metoden är att använda tjänstens huvudnamn som är konton som är begränsade via behörigheter. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem lämplig behörighet som krävs för ett huvudnamn för tjänsten.

Inga av dina privata autentiseringsuppgifter lagras lokalt. Istället skapas en autentiseringstoken av Azure och lagras. När du har loggat in är din inloggningstoken giltig till dess att det har gått 14 dagar utan att den använts. Då måste du autentisera på nytt.

När du har loggat in körs CLI-kommandon mot standardprenumerationen. Om du har mer än en prenumeration kan du [ändra din standardprenumeration](manage-azure-subscriptions-azure-cli.md).

## <a name="interactive-log-in"></a>Interaktiv inloggning

Logga in interaktivt från din webbläsare.

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>Kommandorad

Ange dina autentiseringsuppgifter på kommandoraden.

> [!Note]
> Den här metoden fungerar inte med Microsoft-konton eller konton som har tvåfaktorsautentisering aktiverad.

```azurecli
az login -u <username> -p <password>
```

## <a name="log-in-with-a-specific-tenant"></a>Logga in med en specifik klient

Om du arbetar med flera olika klienter kan du välja vilken klient som ska användas för inloggning med argumentet `--tenant`. Argumentets värde kan antingen vara en `.onmicrosoft.com`-domän eller objekt-ID:t för Azure för klienten. Du kan logga in interaktivt eller ange dina autentiseringsuppgifter med argumenten `--user` och `--password`. 

```
az login --tenant <tenant>
```

## <a name="logging-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn är konton som är inte kopplade till en viss användare och som kan ha behörigheter som tilldelats via fördefinierade roller. Det bästa sättet att skriva säkra skript eller program är att autentisera med ett huvudnamn för tjänsten eftersom du då kan använda både behörighetsbegränsningar och lokalt lagrade statiska autentiseringsuppgifter. Läs mer om tjänstens huvudnamn i informationen om att [skapa ett huvudnamn för tjänsten i Azure med Azure CLI](create-an-azure-service-principal-azure-cli.md).

Om du vill logga in med tjänstens huvudnamn anger du användarnamn, lösenord eller certifikatets PEM-fil samt klienten som är associerad med tjänstens huvudnamn:

```azurecli
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

Klientvärdet är den Azure Active Directory-klient som är associerad med tjänstens huvudnamn. Detta kan antingen vara en `.onmicrosoft.com`-domän eller objekt-ID:t för Azure för klienten.
Du kan skaffa klientens objekt-ID för din aktuella inloggning med följande kommando:

```azurecli
az account show --query 'tenantId' -o tsv
```
