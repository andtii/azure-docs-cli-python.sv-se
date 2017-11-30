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
ms.openlocfilehash: 93d947d91973def1c05e2f5b2e7511bc1c5704a2
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="2fc7c-104">Installera Azure CLI 2.0 med apt</span><span class="sxs-lookup"><span data-stu-id="2fc7c-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="2fc7c-105">Om du kör en distribution där `apt` ingår, till exempel Ubuntu eller Debian, så finns det ett paket för Azure CLI som du kan installera i systemet.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="2fc7c-106">Du måste ha Python 2.7.x eller Python 3.x för att kunna använda CLI.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="2fc7c-107">Om distributionen inte har ett paket för någon av dessa kan du [installera Python](https://www.python.org/downloads/).</span><span class="sxs-lookup"><span data-stu-id="2fc7c-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="2fc7c-108">Installera</span><span class="sxs-lookup"><span data-stu-id="2fc7c-108">Install</span></span>

1. <span data-ttu-id="2fc7c-109">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="2fc7c-109">Modify your sources list:</span></span>
 
   - <span data-ttu-id="2fc7c-110">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="2fc7c-110">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="2fc7c-111">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="2fc7c-111">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="2fc7c-112">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="2fc7c-112">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="2fc7c-113">Du kan köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-113">You can run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="2fc7c-114">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="2fc7c-114">Update</span></span>

<span data-ttu-id="2fc7c-115">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-115">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="2fc7c-116">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-116">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="2fc7c-117">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-117">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="2fc7c-118">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="2fc7c-118">Uninstall</span></span>

<span data-ttu-id="2fc7c-119">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-119">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="2fc7c-120">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-120">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="2fc7c-121">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-121">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="2fc7c-122">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="2fc7c-122">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="2fc7c-123">Avinstallera med `apt-get remove`.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-123">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="2fc7c-124">Ta bort Azure CLI-lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-124">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="2fc7c-125">Ta bort eventuella onödiga paket.</span><span class="sxs-lookup"><span data-stu-id="2fc7c-125">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
