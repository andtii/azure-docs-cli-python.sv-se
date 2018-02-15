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
ms.openlocfilehash: 4b92499d2cb81f64bfbb13215428365711b07874
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="b9862-103">Installera Azure CLI 2.0 med yum</span><span class="sxs-lookup"><span data-stu-id="b9862-103">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="b9862-104">Om du kör en distribution där `yum` ingår, till exempel RHEL, Fedora eller CentOS, så finns det ett paket tillgängligt för Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="b9862-104">If you are running a distribution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="b9862-105">Det här paketet har testats med RHEL 7, Fedora 19 och senare samt CentOS 7.</span><span class="sxs-lookup"><span data-stu-id="b9862-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="b9862-106">Installera</span><span class="sxs-lookup"><span data-stu-id="b9862-106">Install</span></span>

1. <span data-ttu-id="b9862-107">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="b9862-107">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="b9862-108">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="b9862-108">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="b9862-109">Uppdatera `yum`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="b9862-109">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="b9862-110">Kör Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="b9862-110">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="b9862-111">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="b9862-111">Update</span></span>

<span data-ttu-id="b9862-112">Uppdatera Azure CLI med kommandot `yum update`.</span><span class="sxs-lookup"><span data-stu-id="b9862-112">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="b9862-113">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="b9862-113">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="b9862-114">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="b9862-114">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="b9862-115">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="b9862-115">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="b9862-116">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="b9862-116">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
