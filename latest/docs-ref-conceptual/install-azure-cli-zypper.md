---
title: Installera Azure CLI 2.0 med zypper
description: "Så här installerar du Azure CLI 2.0 med zypper"
keywords: azure cli, azure cli install, azure cli zypper, azure cli opensuse, azure cli sle
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
ms.openlocfilehash: c01679ccb77880f1f628f4e48683d8ff030a568b
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-zypper"></a>Installera Azure CLI 2.0 med zypper

Om du kör en distribution där `zypper` ingår, till exempel OpenSUSE eller SLE, så finns det ett paket för Azure CLI som du kan installera i systemet.

> [!NOTE]
> Du måste ha Python 2.7.x eller Python 3.x för att kunna använda CLI. Om distributionen inte har ett paket för någon av dessa kan du [installera Python](https://www.python.org/downloads/).

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

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

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

