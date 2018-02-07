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
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="8c305-104">Installera Azure CLI 2.0 med apt</span><span class="sxs-lookup"><span data-stu-id="8c305-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="8c305-105">Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket tillgängligt för Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="8c305-105">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="8c305-106">Det här paketet har testats med Ubuntu Wheezy och Ubuntu Xenial.</span><span class="sxs-lookup"><span data-stu-id="8c305-106">This package has been tested with Ubuntu Wheezy and Ubuntu Xenial.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="8c305-107">Installera</span><span class="sxs-lookup"><span data-stu-id="8c305-107">Install</span></span>

1. <span data-ttu-id="8c305-108">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="8c305-108">Modify your sources list:</span></span>

   - <span data-ttu-id="8c305-109">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="8c305-109">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="8c305-110">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="8c305-110">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="8c305-111">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="8c305-111">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="8c305-112">Du kan köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="8c305-112">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8c305-113">Felsökning</span><span class="sxs-lookup"><span data-stu-id="8c305-113">Troubleshooting</span></span>

<span data-ttu-id="8c305-114">Här är några vanliga problem som kan uppstå vid installation med `apt`.</span><span class="sxs-lookup"><span data-stu-id="8c305-114">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="8c305-115">Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="8c305-115">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="8c305-116">apt-key misslyckas: "Ingen dirmngr"</span><span class="sxs-lookup"><span data-stu-id="8c305-116">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="8c305-117">När du kör kommandot `apt-key` kanske ett felmeddelande i stil med följande visas:</span><span class="sxs-lookup"><span data-stu-id="8c305-117">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="8c305-118">Det här felet beror på att en komponent som krävs av `apt-key` saknas.</span><span class="sxs-lookup"><span data-stu-id="8c305-118">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="8c305-119">Du kan lösa problemet genom att installera `dirmngr`-paketet.</span><span class="sxs-lookup"><span data-stu-id="8c305-119">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="8c305-120">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="8c305-120">Update</span></span>

<span data-ttu-id="8c305-121">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="8c305-121">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="8c305-122">Med det här kommandot uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="8c305-122">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="8c305-123">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="8c305-123">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="8c305-124">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="8c305-124">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="8c305-125">Avinstallera med `apt-get remove`.</span><span class="sxs-lookup"><span data-stu-id="8c305-125">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="8c305-126">Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="8c305-126">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="8c305-127">Ta bort eventuella onödiga paket.</span><span class="sxs-lookup"><span data-stu-id="8c305-127">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
