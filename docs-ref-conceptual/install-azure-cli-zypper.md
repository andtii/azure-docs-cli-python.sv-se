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
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="4b8dd-104">Installera Azure CLI 2.0 med zypper</span><span class="sxs-lookup"><span data-stu-id="4b8dd-104">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="4b8dd-105">Om du kör en distribution där `zypper` ingår, till exempel openSUSE eller SLES, så finns det ett paket tillgängligt för Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-105">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="4b8dd-106">Det här paketet har testats med openSUSE 42.2 och SLES 12 SP 2.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-106">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="4b8dd-107">Installera</span><span class="sxs-lookup"><span data-stu-id="4b8dd-107">Install</span></span>

1. <span data-ttu-id="4b8dd-108">Installera `curl`:</span><span class="sxs-lookup"><span data-stu-id="4b8dd-108">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="4b8dd-109">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="4b8dd-109">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="4b8dd-110">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="4b8dd-110">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="4b8dd-111">Uppdatera `zypper`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="4b8dd-111">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="4b8dd-112">Du kan köra CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-112">You can run the CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="4b8dd-113">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="4b8dd-113">Update</span></span>

<span data-ttu-id="4b8dd-114">Du kan uppdatera paketet med kommandot `zypper update`.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-114">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="4b8dd-115">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="4b8dd-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="4b8dd-116">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-116">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="4b8dd-117">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-117">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="4b8dd-118">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-118">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

