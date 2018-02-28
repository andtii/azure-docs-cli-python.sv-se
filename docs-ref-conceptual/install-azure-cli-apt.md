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
ms.openlocfilehash: 840e5e7d6531fe92d30235f621e381589266d1d3
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/19/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="2ba91-103">Installera Azure CLI 2.0 med apt</span><span class="sxs-lookup"><span data-stu-id="2ba91-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="2ba91-104">Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett 64-bitars paket tillgängligt för Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="2ba91-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="2ba91-105">Det här paketet har testats med:</span><span class="sxs-lookup"><span data-stu-id="2ba91-105">This package has been tested with:</span></span>

* <span data-ttu-id="2ba91-106">Ubuntu trusty, xenial och artful</span><span class="sxs-lookup"><span data-stu-id="2ba91-106">Ubuntu trusty, xenial, and artful</span></span>
* <span data-ttu-id="2ba91-107">Debian wheezy, jessie och stretch</span><span class="sxs-lookup"><span data-stu-id="2ba91-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="2ba91-108">Installera</span><span class="sxs-lookup"><span data-stu-id="2ba91-108">Install</span></span>

1. <span data-ttu-id="2ba91-109">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="2ba91-109">Modify your sources list:</span></span>

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="2ba91-110">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="2ba91-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="2ba91-111">Du kan köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="2ba91-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2ba91-112">Felsökning</span><span class="sxs-lookup"><span data-stu-id="2ba91-112">Troubleshooting</span></span>

<span data-ttu-id="2ba91-113">Här är några vanliga problem som kan uppstå vid installation med `apt`.</span><span class="sxs-lookup"><span data-stu-id="2ba91-113">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="2ba91-114">Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="2ba91-114">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="2ba91-115">apt-key misslyckas: "Ingen dirmngr"</span><span class="sxs-lookup"><span data-stu-id="2ba91-115">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="2ba91-116">När du kör kommandot `apt-key` kanske ett felmeddelande i stil med följande visas:</span><span class="sxs-lookup"><span data-stu-id="2ba91-116">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="2ba91-117">Det här felet beror på att en komponent som krävs av `apt-key` saknas.</span><span class="sxs-lookup"><span data-stu-id="2ba91-117">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="2ba91-118">Du kan lösa problemet genom att installera `dirmngr`-paketet.</span><span class="sxs-lookup"><span data-stu-id="2ba91-118">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="2ba91-119">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="2ba91-119">Update</span></span>

<span data-ttu-id="2ba91-120">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="2ba91-120">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="2ba91-121">Med det här kommandot uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="2ba91-121">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="2ba91-122">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="2ba91-122">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="2ba91-123">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="2ba91-123">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="2ba91-124">Avinstallera med `apt-get remove`.</span><span class="sxs-lookup"><span data-stu-id="2ba91-124">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="2ba91-125">Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="2ba91-125">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="2ba91-126">Ta bort eventuella onödiga paket.</span><span class="sxs-lookup"><span data-stu-id="2ba91-126">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
