---
title: "Installera Azure CLI för macOS"
description: "Så här installerar du Azure CLI 2.0 på macOS"
keywords: "Azure CLI, Installera Azure CLI, azure macos, installera azure för macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 36fd2604677db0b7f820ee11884bf790fb1d75cb
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-macos"></a>Installera Azure CLI 2.0 på macOS

På macOS-plattformen kan du installera Azure CLI via [pakethanteraren Homebrew](http://brew.sh). Med Homebrew är det enkelt att se till att installationen av CLI alltid är uppdaterad. CLI-paketet har testats på macOS-versionerna 10.9 och senare.

## <a name="install"></a>Installera

CLI-installationen hanteras enklast med Homebrew. Homebrew erbjuder ett bekvämt sätt att installera, uppdatera och avinstallera. Om du inte har Homebrew i systemet kan du [installera Homebrew](https://docs.brew.sh/Installation.html) innan du fortsätter.

Du kan installera CLI genom att uppdatera informationen om brew-lagringsplatsen och sedan köra kommandot `install`:

```bash
brew update && brew install azure-cli
```

Sedan kan du köra Azure CLI med kommandot `az`.

## <a name="troubleshooting"></a>Felsökning

Om du stötte på problem när du installerade CLI med Homebrew så är det här några vanliga fel som kan uppstå. Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).

### <a name="unable-to-find-python-or-installed-packages"></a>Det gick inte att hitta Python eller installerade paket

Om installationen inte kunde hitta Python eller installerade paket så kan det bero på en versionskonflikt eller något annat problem som uppstod under installationen av Homebrew. Eftersom CLI inte använder en virtuell Python-miljö så är det viktigt att det går att hitta rätt version av Python. Du kan åtgärda de här problemen genom att länka till Python-installationen igen.

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a>CLI-version 1.x har installerats

Om en inaktuell version installerades kan det bero på en föråldrad homebrew-cache. Följ anvisningarna för [uppdateringen](#Update).

## <a name="update"></a>Uppdatering

CLI uppdateras regelbundet med felkorrigeringar, förbättringar, nya funktioner och förhandsgranskningsmöjligheter. En ny version blir tillgänglig ungefär varannan vecka. Uppdatera informationen om din lokala lagringsplats och uppgradera sedan `azure-cli`-paketet.

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

Använd Homebrew för att avinstallera `azure-cli`-paketet.

```bash
brew uninstall azure-cli
```
