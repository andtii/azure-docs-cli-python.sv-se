---
title: "Installera Azure CLI 2.0 på Linux med yum"
description: "Så här installerar du Azure CLI 2.0 med yum"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5b7afe999d1afe5be40c4957d9cd0f832b680099
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/19/2018
---
# <a name="install-azure-cli-20-with-yum"></a>Installera Azure CLI 2.0 med yum

Om du kör en distribution där `yum` ingår, till exempel RHEL, Fedora eller CentOS, så finns det ett paket tillgängligt för Azure CLI. Det här paketet har testats med RHEL 7, Fedora 19 och senare samt CentOS 7.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>Installera

1. Importera Microsoft-lagringsplatsnyckeln.

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Skapa information om lokal `azure-cli`-lagringsplats.

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. Installera med `yum install`-kommandot. 

   ```bash
   sudo yum install azure-cli
   ```

Kör Azure CLI med kommandot `az`.

## <a name="update"></a>Uppdatering

Uppdatera Azure CLI med kommandot `yum update`.

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. Ta bort paketet från datorn.

   ```bash
   sudo yum remove azure-cli
   ```

2. Ta bort lagringsinformationen om du inte tänker installera om CLI.

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
