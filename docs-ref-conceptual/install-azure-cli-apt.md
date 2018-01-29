---
title: Installera Azure CLI 2.0 med apt
description: "Så här installerar du Azure CLI 2.0 med apt-pakethanteraren"
keywords: Azure CLI,Install Azure CLI,azure apt, azure debian, azure ubuntu
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
ms.openlocfilehash: 65e8e78275b0f40a2298934fe8bc9368bbf796a7
ms.sourcegitcommit: 59f0b667f2202bae8914e6fc8dc5c9dc79fef91c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/25/2018
---
# <a name="install-azure-cli-20-with-apt"></a>Installera Azure CLI 2.0 med apt

Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket för Azure CLI som du kan installera i systemet.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>Installera

1. Ändra listan med källor:

   - 32-bitarssystem

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64-bitarssystem

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. Kör följande sudo-kommandon:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

Du kan köra Azure CLI med kommandot `az`.

## <a name="troubleshooting"></a>Felsökning

### <a name="apt-key-fails-with-no-dirmngr"></a>apt-key misslyckas: "Ingen dirmngr"

När du kör kommandot `apt-key` kanske ett felmeddelande i stil med följande visas.

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

Detta beror på att en komponent saknas som krävs av `apt-key`. Du kan lösa detta genom att installera `dirmngr`-paketet.

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a>Uppdatering

Använd `apt-get upgrade` för att uppdatera CLI-paketet.

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.
> Om du bara vill uppgradera CLI använder du `apt-get install`.
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a>Avinstallera

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

1. Avinstallera med `apt-get remove`.

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. Ta bort eventuella onödiga paket.

   ```bash
   sudo apt autoremove
   ```
