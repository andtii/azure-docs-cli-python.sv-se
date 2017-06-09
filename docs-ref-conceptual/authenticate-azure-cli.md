---
title: Logga in med Azure CLI 2.0
description: "Logga in med Azure 2.0 CLI på Linux, Mac eller Windows."
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: 4ab4f0de38614eff00f55bad96ea886bb007f3c0
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/05/2017
---
# <a name="log-in-with-azure-cli-20"></a>Logga in med Azure CLI 2.0

Du kan logga in och autentisera med Azure CLI på flera olika sätt. Det är enklast att komma igång genom att logga in interaktivt via webbläsaren eller att logga in på kommandoraden. Den rekommenderade metoden är att använda huvudnamn för tjänsten, vilket gör det möjligt för dig att skapa icke-interaktiva konton som du kan använda för att manipulera resurser. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem lämplig behörighet som krävs för ett huvudnamn för tjänsten.

Kommandon som du kör med CLI körs mot standardprenumerationen.  Om du har mer än en prenumeration kanske du behöver [bekräfta din standardprenumeration](manage-azure-subscriptions-azure-cli.md) och ändra den efter behov.

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
Autentisering med tjänstens huvudnamn är det bästa sätt att säkra användningen av dina Azure-resurser från antingen dina skript eller program som manipulerar resurser.
Du definierar de roller du vill använda via `az role`-uppsättningen med kommandon.
Du kan läsa mer och se exempel på roller för tjänstens huvudnamn i våra [referensartiklar om az-roller](https://docs.microsoft.com/cli/azure/role.md).

1. Om du inte redan har ett huvudnamn för tjänsten kan du [skapa ett](create-an-azure-service-principal-azure-cli.md).

1. Logga in med huvudnamnet för tjänsten.

   ```azurecli-interactive
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   För att få din klient loggar du in interaktivt och sedan hämtar du klienten från din prenumeration.

   ```azurecli
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```