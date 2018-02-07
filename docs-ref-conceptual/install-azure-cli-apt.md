---
title: "Installera Azure CLI 2.0 på Linux med apt"
description: "Så här installerar du Azure CLI 2.0 med apt-pakethanteraren"
keywords: Azure CLI,Install Azure CLI,azure apt, azure debian, azure ubuntu
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: fdd9f0061d5d38ed5a349b11eb0f5f27786bc1ab
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-apt"></a>Installera Azure CLI 2.0 med apt

Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket tillgängligt för Azure CLI. Det här paketet har testats med Ubuntu Wheezy och Ubuntu Xenial.

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

Här är några vanliga problem som kan uppstå vid installation med `apt`. Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).

### <a name="apt-key-fails-with-no-dirmngr"></a>apt-key misslyckas: "Ingen dirmngr"

När du kör kommandot `apt-key` kanske ett felmeddelande i stil med följande visas:

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

Det här felet beror på att en komponent som krävs av `apt-key` saknas. Du kan lösa problemet genom att installera `dirmngr`-paketet.

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a>Uppdatering

Använd `apt-get upgrade` för att uppdatera CLI-paketet.

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> Med det här kommandot uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.
> Om du bara vill uppgradera CLI använder du `apt-get install`.
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

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
