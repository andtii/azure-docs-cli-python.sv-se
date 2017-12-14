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
ms.openlocfilehash: 6b9a97e73f45c8271f1e8f19d5a8cf5f9f748d07
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="d397c-104">Installera Azure CLI 2.0 med zypper</span><span class="sxs-lookup"><span data-stu-id="d397c-104">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="d397c-105">Om du kör en distribution där `zypper` ingår, till exempel OpenSUSE eller SLE, så finns det ett paket för Azure CLI som du kan installera i systemet.</span><span class="sxs-lookup"><span data-stu-id="d397c-105">If you are running a distirbution that comes with `zypper`, such as OpenSUSE or SLE, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="d397c-106">Installera</span><span class="sxs-lookup"><span data-stu-id="d397c-106">Install</span></span>

1. <span data-ttu-id="d397c-107">Installera `curl`:</span><span class="sxs-lookup"><span data-stu-id="d397c-107">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="d397c-108">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="d397c-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="d397c-109">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="d397c-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="d397c-110">Uppdatera `zypper`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="d397c-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="d397c-111">Du kan köra CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="d397c-111">You can run the CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="d397c-112">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="d397c-112">Update</span></span>

<span data-ttu-id="d397c-113">Du kan uppdatera paketet med kommandot `zypper update`.</span><span class="sxs-lookup"><span data-stu-id="d397c-113">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="d397c-114">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="d397c-114">Uninstall</span></span>

<span data-ttu-id="d397c-115">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="d397c-115">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="d397c-116">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="d397c-116">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="d397c-117">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="d397c-117">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="d397c-118">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="d397c-118">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="d397c-119">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="d397c-119">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="d397c-120">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="d397c-120">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="d397c-121">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="d397c-121">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

