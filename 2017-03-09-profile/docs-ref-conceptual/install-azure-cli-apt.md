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
ms.openlocfilehash: 75c531a13a4b730158cd2e874cb6c5d581a27598
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="7be1f-104">Installera Azure CLI 2.0 med apt</span><span class="sxs-lookup"><span data-stu-id="7be1f-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="7be1f-105">Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket för Azure CLI som du kan installera i systemet.</span><span class="sxs-lookup"><span data-stu-id="7be1f-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="7be1f-106">Installera</span><span class="sxs-lookup"><span data-stu-id="7be1f-106">Install</span></span>

1. <span data-ttu-id="7be1f-107">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="7be1f-107">Modify your sources list:</span></span>

   - <span data-ttu-id="7be1f-108">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="7be1f-108">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="7be1f-109">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="7be1f-109">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="7be1f-110">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="7be1f-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="7be1f-111">Du kan köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="7be1f-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="7be1f-112">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="7be1f-112">Update</span></span>

<span data-ttu-id="7be1f-113">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="7be1f-113">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="7be1f-114">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="7be1f-114">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="7be1f-115">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="7be1f-115">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="7be1f-116">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="7be1f-116">Uninstall</span></span>

<span data-ttu-id="7be1f-117">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="7be1f-117">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="7be1f-118">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="7be1f-118">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="7be1f-119">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="7be1f-119">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="7be1f-120">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="7be1f-120">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="7be1f-121">Avinstallera med `apt-get remove`.</span><span class="sxs-lookup"><span data-stu-id="7be1f-121">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="7be1f-122">Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="7be1f-122">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="7be1f-123">Ta bort eventuella onödiga paket.</span><span class="sxs-lookup"><span data-stu-id="7be1f-123">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
