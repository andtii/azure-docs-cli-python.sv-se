---
title: Logga in med Azure CLI 2.0
description: "Logga in med Azure 2.0 CLI på Linux, Mac eller Windows."
keywords: Azure CLI 2.0, inloggning, Azure CLI, autentisering, auktorisera, logga in
author: sptramer
ms.author: stttramer
manager: routlaw
ms.date: 11/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: dd05868f7378673836f47e743ed4088f2efd3dca
ms.sourcegitcommit: 5db22de971cf3983785cb209d92cbed1bbd69ecf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/14/2017
---
# <a name="log-in-with-azure-cli-20"></a>Logga in med Azure CLI 2.0

Du kan logga in och autentisera med Azure CLI på flera olika sätt. Det är enklast att komma igång genom att logga in interaktivt via webbläsaren eller att logga in på kommandoraden. Den rekommenderade metoden är att använda huvudnamn för tjänsten, vilket gör det möjligt för dig att skapa icke-interaktiva konton som du kan använda för att manipulera resurser. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem lämplig behörighet som krävs för ett huvudnamn för tjänsten. 

Inga av dina privata autentiseringsuppgifter lagras lokalt. Istället skapas en autentiseringstoken av Azure och lagras. När du loggat in är din lokala inloggningstoken giltig till dess att det går 14 dagar utan att den används. Då måste du autentisera på nytt.

När du har loggat in körs CLI-kommandon mot standardprenumerationen. Om du har mer än en prenumeration kanske du behöver [ändra din standardprenumeration](manage-azure-subscriptions-azure-cli.md).

## <a name="interactive-log-in"></a>Interaktiv inloggning

Logga in interaktivt från din webbläsare.

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>Kommandorad

Ange dina autentiseringsuppgifter på kommandoraden.

> [!Note]
> Den här metoden fungerar inte med Microsoft-konton eller konton som har tvåfaktorsautentisering aktiverad.

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory.
Autentisering med tjänstens huvudnamn är det bästa sätt att säkra användningen av dina Azure-resurser från antingen dina skript eller program som manipulerar resurser. Om tjänstens huvudnamn inte redan är tillgängligt och du vill skapa ett läser du [Create an Azure service principal with the Azure CLI](create-an-azure-service-principal-azure-cli.md) (Skapa tjänstens huvudnamn i Azure med Azure CLI).

Om du vill logga in med tjänstens huvudnamn anger du användarnamn, lösenord eller certifikatets PEM-fil samt klienten som är associerad med tjänstens huvudnamn:

```azurecli-interactive
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

Klientvärdet är den Azure Active Directory-klient som är associerad med tjänstens huvudnamn. Det kan antingen vara en .onmicrosoft.com-domän eller klientens objekt-ID i Azure.
Du kan skaffa klientens objekt-ID för din aktuella inloggning med följande kommando:

```azurecli
az account show --query 'tenanatId' -o tsv
```

