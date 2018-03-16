---
title: "Installera Azure CLI 2.0 på Linux med apt"
description: "Så här installerar du Azure CLI 2.0 med apt-pakethanteraren"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/06/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 188e7dfded21bb5c7036b3a950b3e4cb10bc1d33
ms.sourcegitcommit: 5c004b455eff196d853bfbe12901c6114a1652d7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2018
---
# <a name="install-azure-cli-20-with-apt"></a>Installera Azure CLI 2.0 med apt

Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett 64-bitars paket tillgängligt för Azure CLI. Det här paketet har testats med:

* Ubuntu trusty, xenial och artful
* Debian wheezy, jessie och stretch

## <a name="install"></a>Installera

1. Ändra listan med källor:

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
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

### <a name="apt-key-hangs"></a>apt-key hangs

Om brandväggen blockerar utgående anslutningar till port 11371 kan kommandot `apt-key` sluta svara på obestämd tid. Brandväggen kan behöva använda en HTTP-proxyserver för utgående anslutningar:

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

Kontakta systemadministratören om du inte vet om du har en proxyserver. Om proxyservern inte kräver inloggning kan du utelämna användare, lösenord och `@`-token.

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
