---
title: "Installera Azure CLI 2.0 på Linux med zypper"
description: "Så här installerar du Azure CLI 2.0 med zypper"
keywords: azure cli, azure cli install, azure cli zypper, azure cli opensuse, azure cli sle
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: c0b566f96e47d34d20f7bf85db0fae32913ed596
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-zypper"></a>Installera Azure CLI 2.0 med zypper

Om du kör en distribution där `zypper` ingår, till exempel openSUSE eller SLES, så finns det ett paket tillgängligt för Azure CLI. Det här paketet har testats med openSUSE 42.2 och SLES 12 SP 2.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>Installera

1. Installera `curl`:

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. Importera nyckeln för Microsoft-lagringsplatsen:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. Skapa information om lokal `azure-cli`-lagringsplats:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. Uppdatera `zypper`-paketindexet och installera:

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

Du kan köra CLI med kommandot `az`.

## <a name="update"></a>Uppdatering

Du kan uppdatera paketet med kommandot `zypper update`.

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. Ta bort paketet från datorn.

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. Ta bort lagringsinformationen om du inte tänker installera om CLI.

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

