---
title: "Installera Azure CLI 2.0 för Linux manuellt"
description: "Så här installerar du Azure CLI 2.0 på Linux manuellt"
keywords: Azure CLI,Install Azure CLI,azure linux, azure install linux
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf1405cae70762146f63bc6629edc0dd1d949fff
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-on-linux-manually"></a>Installera Azure CLI 2.0 på Linux manuellt

Om du inte har ett paket för Azure CLI tillgängligt i din distribution så kan du alltid installera CLI manuellt genom att köra ett skript för installation. Om du har ett tillgängligt paket så är det alltid den rekommenderade installationsmetoden.

## <a name="prerequisites"></a>Krav

Följande programvara måste vara tillgänglig i systemet för att du ska kunna installera CLI:

* [Python 2.7 eller Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a>Installera eller uppdatera manuellt

Oavsett om du installerar eller uppdaterar CLI så måste du utföra en fullständig installation. När kraven är uppfyllda kan du installera CLI genom att köra `curl`.

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

Om du inte har `curl` i systemet så kan du ladda ned skriptet och köra det lokalt i stället. Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla. Efter installationen kör du CLI med kommandot `az`.

## <a name="troubleshooting"></a>Felsökning

### <a name="curl-object-moved-error"></a>Fel: curl "Object Moved"

Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>Det gick inte att hitta kommandot `az`

Om du inte kan köra kommandot efter installationen kan du behöva rensa cacheminnet för gränssnittets kommando-hash. Kör

```bash
hash -r
```

och se om problemet är löst.

Det här kan även inträffa om du inte startade om gränssnittet efter installationen. Kontrollera att platsen för kommandot `az` är i `$PATH`.

Om du körde installationsskriptet så är det följande:

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a>Avinstallera manuellt

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

Du kan avinstallera CLI genom att ta bort filerna direkt från installationsplatsen. Din installationsplats bör ha valts när installationen utfördes om du installerade via skriptet `https://aka.ms/InstallAzureCLI`. Standardplatsen för installation är `$HOME`.

Ta först bort de installerade CLI-filerna:

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

Ändra filen `$HOME/.bash_profile` för att ta bort raden:

```
<install location>/lib/azure-cli/az.completion
```

Läs slutligen in gränssnittets kommandocacheminne igen om det används. Användare av `bash` och `zsh` måste utföra det här steget:

```bash
hash -r
```
