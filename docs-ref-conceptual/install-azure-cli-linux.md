---
title: "Installera Azure CLI 2.0 för Linux manuellt"
description: "Så här installerar du Azure CLI 2.0 på Linux manuellt"
keywords: "Azure CLI, Installera Azure CLI, azure linux, installera Azure för linux"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: d8c88d111c50a3cbb6b643a14dcd2a9773699657
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a>Installera Azure CLI 2.0 på Linux manuellt

Om du inte har ett paket för Azure CLI tillgängligt i din distribution så kan du alltid installera CLI manuellt genom att köra ett skript för installation.

> [!NOTE]
> Det rekommenderas starkt att du använder en pakethanterare för CLI. Med en pakethanterare får du alltid de senaste uppdateringarna och kan vara säker på att CLI-komponenterna är stabila. Kontrollera om det finns något paket för din distribution innan du installerar manuellt.

## <a name="prerequisites"></a>Nödvändiga komponenter

Följande programvara måste vara tillgänglig i systemet för att du ska kunna installera CLI:

* [Python 2.7 eller Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update"></a>Installera eller uppdatera 

Oavsett om du installerar eller uppdaterar CLI så måste du utföra en fullständig installation. När kraven är uppfyllda kan du installera CLI genom att köra `curl`.

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

Du kan även ladda ned skriptet och köra det lokalt istället. Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla. Efter installationen kör du CLI med kommandot `az`.

## <a name="troubleshooting"></a>Felsökning

Här är några vanliga problem som kan uppstå vid manuell installation. Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).
### <a name="curl-object-moved-error"></a>Fel: curl "Object Moved"

Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>Det gick inte att hitta kommandot `az`

Om du inte kan köra kommandot efter installationen och använder `bash` eller `zsh` så kan du behöva rensa cacheminnet för gränssnittets kommando-hash Kör

```bash
hash -r
```

och kontrollera om problemet är löst.

Det här problemet kan även inträffa om du inte startade om gränssnittet efter installationen. Kontrollera att platsen för kommandot `az` är i `$PATH`. `az`-kommandots plats är

```bash
<install path>/bin
```

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

Avinstallera CLI genom att ta bort filerna direkt från platsen som valts vid installationen. Standardplatsen för installation är `$HOME`.

1. Ta bort de installerade CLI-filerna.
  
  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```
2. Ändra filen `$HOME/.bash_profile` för att ta bort följande rad:
  
  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. Läs in gränssnittets kommandocacheminne om du använder `bash` eller `zsh`.
  
  ```bash
  hash -r
  ```
