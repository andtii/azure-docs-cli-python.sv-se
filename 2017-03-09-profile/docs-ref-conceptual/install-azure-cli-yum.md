---
title: Installera Azure CLI 2.0 med yum
description: "Så här installerar du Azure CLI 2.0 med yum"
keywords: Azure CLI,Install Azure CLI,azure yum,azure rhel, azure fedora, azure centos
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
ms.openlocfilehash: de695454c6f3109679b9eb9f6c0d77348d354518
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-yum"></a>Installera Azure CLI 2.0 med yum

Om du kör en distribution där `yum` ingår, till exempel RHEL, Fedora eller CentOS, så finns det ett paket för Azure CLI som du kan installera i systemet.

> [!NOTE]
> Du måste ha Python 2.7.x eller Python 3.x för att kunna använda CLI. Om distributionen inte har ett paket för någon av dessa kan du [installera Python](https://www.python.org/downloads/).

## <a name="install"></a>Installera 

1. Importera nyckeln för Microsoft-lagringsplatsen:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Skapa information om lokal `azure-cli`-lagringsplats:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. Uppdatera `yum`-paketindexet och installera:

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

Kör Azure CLI med kommandot `az`.

## <a name="update"></a>Uppdatering

Uppdatera Azure CLI med kommandot `yum update`.

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a>Avinstallera

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

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
