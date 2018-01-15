---
title: "Installera Azure CLI för macOS"
description: "Så här installerar du Azure CLI 2.0 på macOS"
keywords: Azure CLI,Install Azure CLI,azure macos, azure install macos
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e615d2b3ab3b1307e982cb1d4d456633440afdf6
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-macos"></a>Installera Azure CLI 2.0 på macOS

På macOS-plattformen kan du installera Azure CLI via antingen [pakethanteraren Homebrew](http://brew.sh) eller manuellt. Vi rekommenderar att du installerar via Homebrew. Då blir det enklare att installera, hämta uppdateringar och avinstallera om du skulle behöva det.

## <a name="use-homebrew-to-install"></a>Använda Homebrew för att installera

CLI-installationen hanteras enklast med Homebrew. Homebrew erbjuder ett bekvämt sätt att installera, uppdatera och avinstallera. Det påminner om andra pakethanterare, till exempel `apt` och `yum`.
Om du inte har Homebrew i systemet kan du [installera Homebrew](https://docs.brew.sh/Installation.html) innan du fortsätter.

### <a name="install-with-homebrew"></a>Installera med Homebrew

Du kan installera CLI genom att uppdatera informationen om brew-lagringsplatsen och sedan köra kommandot `install`:

```bash
brew update && brew install azure-cli
```

Sedan kan du köra Azure CLI med kommandot `az`.

### <a name="update-with-homebrew"></a>Uppdatera med Homebrew

CLI uppdateras regelbundet med felkorrigeringar, förbättringar, nya funktioner och förhandsgranskningsmöjligheter. En ny version blir tillgänglig ungefär varannan vecka. Om du vill uppdatera CLI-paketet måste du uppdatera informationen om din lokala lagringsplats.

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a>Felsökning

Stötte du på problem när du installerade eller uppdaterade CLI med Homebrew? Här är några vanliga fel som kan uppstå, samt sätt att diagnostisera och lösa dem.

#### <a name="unable-to-find-python-or-installed-packages"></a>Det gick inte att hitta Python eller installerade paket

Om installationen inte kunde hitta Python eller installerade paket så kan detta bero på en versionskonflikt eller något annat problem som uppstod under installationen av Homebrew. Eftersom CLI inte använder en virtuell miljö måste det gå att hitta rätt versioner av Python som har installerats av Homebrew. Du kan åtgärda dessa problem genom att länka till Python-installationen igen:

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a>CLI-versionen är inaktuell

Om du tror att den installerade versionen av CLI kan vara inaktuell så kan du köra kommandot `brew update` följt av `brew upgrade azure-cli`. Tänk på att Homebrew-paket kan släppas långsammare än allmänna versioner om CLI inte uppdateras. Om du behöver de absolut senaste installationerna av CLI så bör du [installera manuellt](#manage-the-cli-manually).

### <a name="uninstall-with-homebrew"></a>Avinstallera med Homebrew

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

Om du installerade med Homebrew så bör du även använda det för att avinstallera.

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a>Installera CLI manuellt

Om du inte kan eller inte vill använda Homebrew för att utföra CLI-installationen så kan du installera manuellt.

Följ anvisningarna för [manuell installation på Linux](install-azure-cli-linux.md) för att installera manuellt på macOS. macOS-version 10.9 och senare bör innehålla alla nödvändiga beroenden.
