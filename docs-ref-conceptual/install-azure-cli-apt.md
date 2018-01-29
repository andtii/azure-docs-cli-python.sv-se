---
title: Installera Azure CLI 2.0 med apt
description: "Så här installerar du Azure CLI 2.0 med apt-pakethanteraren"
keywords: Azure CLI,Install Azure CLI,azure apt, azure debian, azure ubuntu
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
ms.openlocfilehash: 65e8e78275b0f40a2298934fe8bc9368bbf796a7
ms.sourcegitcommit: 59f0b667f2202bae8914e6fc8dc5c9dc79fef91c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/25/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="0bba1-104">Installera Azure CLI 2.0 med apt</span><span class="sxs-lookup"><span data-stu-id="0bba1-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="0bba1-105">Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket för Azure CLI som du kan installera i systemet.</span><span class="sxs-lookup"><span data-stu-id="0bba1-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="0bba1-106">Installera</span><span class="sxs-lookup"><span data-stu-id="0bba1-106">Install</span></span>

1. <span data-ttu-id="0bba1-107">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="0bba1-107">Modify your sources list:</span></span>

   - <span data-ttu-id="0bba1-108">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="0bba1-108">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="0bba1-109">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="0bba1-109">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="0bba1-110">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="0bba1-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="0bba1-111">Du kan köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="0bba1-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="0bba1-112">Felsökning</span><span class="sxs-lookup"><span data-stu-id="0bba1-112">Troubleshooting</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="0bba1-113">apt-key misslyckas: "Ingen dirmngr"</span><span class="sxs-lookup"><span data-stu-id="0bba1-113">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="0bba1-114">När du kör kommandot `apt-key` kanske ett felmeddelande i stil med följande visas.</span><span class="sxs-lookup"><span data-stu-id="0bba1-114">When running the `apt-key` command, you may see output similar to the following error.</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="0bba1-115">Detta beror på att en komponent saknas som krävs av `apt-key`.</span><span class="sxs-lookup"><span data-stu-id="0bba1-115">This is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="0bba1-116">Du kan lösa detta genom att installera `dirmngr`-paketet.</span><span class="sxs-lookup"><span data-stu-id="0bba1-116">You can resolve this by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="0bba1-117">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="0bba1-117">Update</span></span>

<span data-ttu-id="0bba1-118">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="0bba1-118">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="0bba1-119">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="0bba1-119">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="0bba1-120">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="0bba1-120">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="0bba1-121">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="0bba1-121">Uninstall</span></span>

<span data-ttu-id="0bba1-122">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="0bba1-122">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="0bba1-123">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="0bba1-123">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="0bba1-124">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="0bba1-124">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="0bba1-125">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="0bba1-125">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="0bba1-126">Avinstallera med `apt-get remove`.</span><span class="sxs-lookup"><span data-stu-id="0bba1-126">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="0bba1-127">Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="0bba1-127">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="0bba1-128">Ta bort eventuella onödiga paket.</span><span class="sxs-lookup"><span data-stu-id="0bba1-128">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
