---
title: "Kör Azure CLI 2.0 i en Docker-behållare"
description: "Så här kör du en Docker-behållare med en värdlösning för Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 3a09eb6d83bb5401628bd952d199a03ecbb8216e
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a><span data-ttu-id="bef31-103">Kör Azure CLI 2.0 i en Docker-behållare</span><span class="sxs-lookup"><span data-stu-id="bef31-103">Run Azure CLI 2.0 in a Docker container</span></span>

<span data-ttu-id="bef31-104">Du kan använda Docker för att köra en fristående Linux-behållare om Azure CLI 2.0 redan är installerat.</span><span class="sxs-lookup"><span data-stu-id="bef31-104">You can use Docker to run a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="bef31-105">Med Docker kan du snabbt komma igång med en miljö där du kan prova CLI för att avgöra om det är rätt för dig. Du kan även utgå från vår avbildning i din egen distribution.</span><span class="sxs-lookup"><span data-stu-id="bef31-105">Docker lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or use our image as a base for your own deployment.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="bef31-106">Kör i en Docker-behållare</span><span class="sxs-lookup"><span data-stu-id="bef31-106">Run in a Docker container</span></span>

<span data-ttu-id="bef31-107">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="bef31-107">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

<span data-ttu-id="bef31-108">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="bef31-108">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="bef31-109">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="bef31-109">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a><span data-ttu-id="bef31-110">Uppdatera Docker-avbildning</span><span class="sxs-lookup"><span data-stu-id="bef31-110">Update Docker image</span></span>

<span data-ttu-id="bef31-111">Om du vill uppdatera med Docker måste du hämta den nya avbildningen och återskapa alla befintliga behållare.</span><span class="sxs-lookup"><span data-stu-id="bef31-111">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="bef31-112">Därför bör du försöka undvika att använda en behållare som är värd för CLI som ett datalager.</span><span class="sxs-lookup"><span data-stu-id="bef31-112">For this reason you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="bef31-113">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="bef31-113">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="bef31-114">Avinstallera Docker-avbildning</span><span class="sxs-lookup"><span data-stu-id="bef31-114">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="bef31-115">När du har stoppat behållarna som körs i CLI-avbildningen kan du ta du bort dem.</span><span class="sxs-lookup"><span data-stu-id="bef31-115">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```
