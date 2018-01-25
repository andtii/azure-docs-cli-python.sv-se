---
title: Installera Azure CLI med Docker
description: "Så här installerar du en dockerbehållare med Azure CLI 2.0"
keywords: Azure CLI,Install Azure CLI,azure docker,azure docker image,
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7a12da712cd2aad5bb5fb56e27267a8e05df34a6
ms.sourcegitcommit: c95a0cde5819cfe8a4f6b058a52f09a8f87c9696
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/23/2018
---
# <a name="install-azure-cli-20-with-docker"></a><span data-ttu-id="eb8f2-104">Installera Azure CLI 2.0 med Docker</span><span class="sxs-lookup"><span data-stu-id="eb8f2-104">Install Azure CLI 2.0 with Docker</span></span>

<span data-ttu-id="eb8f2-105">Du kan använda Docker för att installera en fristående Linux-behållare med Azure CLI 2.0 redan installerat.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-105">You can use Docker to install a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="eb8f2-106">Det här gör att du snabbt kan komma igång med en miljö där du kan prova CLI för att avgöra om det är rätt för dig. Du kan även använda det här exemplet som en basavbildning.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-106">This lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or allows you to use this as a base image.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="eb8f2-107">Installera med Docker</span><span class="sxs-lookup"><span data-stu-id="eb8f2-107">Install with Docker</span></span>

<span data-ttu-id="eb8f2-108">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli:<version>
   ```

<span data-ttu-id="eb8f2-109">Se våra [Docker-taggar](https://hub.docker.com/r/microsoft/azure-cli/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-109">See our [Docker tags](https://hub.docker.com/r/microsoft/azure-cli/tags/) for available versions.</span></span>

<span data-ttu-id="eb8f2-110">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-110">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="eb8f2-111">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-111">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli:<version>
> ```

### <a name="update-with-docker"></a><span data-ttu-id="eb8f2-112">Uppdatera med Docker</span><span class="sxs-lookup"><span data-stu-id="eb8f2-112">Update with Docker</span></span>

<span data-ttu-id="eb8f2-113">Om du vill uppdatera med Docker måste du hämta den nya avbildningen och återskapa alla befintliga behållare.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-113">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="eb8f2-114">Därför bör du försöka undvika att använda en behållare som är värd för CLI som ett datalager.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-114">For this reason you should try and avoid using a container which hosts the CLI as a data store.</span></span>

1. <span data-ttu-id="eb8f2-115">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-115">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull microsoft/azure-cli
   ```

2. <span data-ttu-id="eb8f2-116">Hämta behållarna som för närvarande använder CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-116">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=microsoft/azure-cli'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        microsoft/azure-cli:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

  > [!NOTE]
  > <span data-ttu-id="eb8f2-117">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-117">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="eb8f2-118">Stoppa och återskapa behållarna.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-118">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run microsoft/azure-cli
   ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="eb8f2-119">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="eb8f2-119">Uninstall with Docker</span></span>

<span data-ttu-id="eb8f2-120">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-120">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="eb8f2-121">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-121">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="eb8f2-122">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-122">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="eb8f2-123">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="eb8f2-123">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="eb8f2-124">Om du vill avinstallera CLI Docker-avbildningen fullständigt måste du ta bort eventuella behållare som kör den och sedan ta bort den lokala avbildningen.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-124">To properly uninstall the CLI Docker image you need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="eb8f2-125">Hämta behållarna som kör azure-cli-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-125">Get the containers running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=microsoft/azure-cli'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        microsoft/azure-cli:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```
  > [!NOTE]
  > <span data-ttu-id="eb8f2-126">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-126">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

2. <span data-ttu-id="eb8f2-127">Ta bort alla behållare som kör CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-127">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="eb8f2-128">Ta bort den lokalt installerade CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="eb8f2-128">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi microsoft/azure-cli
   ```

