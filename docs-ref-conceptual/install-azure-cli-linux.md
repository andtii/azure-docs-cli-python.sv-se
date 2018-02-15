---
title: "Installera Azure CLI 2.0 för Linux manuellt"
description: "Så här installerar du Azure CLI 2.0 på Linux manuellt"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 4ab1f70308810e045b9a1d923fd809ad9848f6c6
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="f5682-103">Installera Azure CLI 2.0 på Linux manuellt</span><span class="sxs-lookup"><span data-stu-id="f5682-103">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="f5682-104">Om du inte har ett paket för Azure CLI tillgängligt i din distribution så kan du alltid installera CLI manuellt genom att köra ett skript för installation.</span><span class="sxs-lookup"><span data-stu-id="f5682-104">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manually by running an installation script.</span></span>

> [!NOTE]
> <span data-ttu-id="f5682-105">Det rekommenderas starkt att du använder en pakethanterare för CLI.</span><span class="sxs-lookup"><span data-stu-id="f5682-105">It's strongly recommend that you use a package manager for the CLI.</span></span> <span data-ttu-id="f5682-106">Med en pakethanterare får du alltid de senaste uppdateringarna och kan vara säker på att CLI-komponenterna är stabila.</span><span class="sxs-lookup"><span data-stu-id="f5682-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="f5682-107">Kontrollera om det finns något paket för din distribution innan du installerar manuellt.</span><span class="sxs-lookup"><span data-stu-id="f5682-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5682-108">Nödvändiga komponenter</span><span class="sxs-lookup"><span data-stu-id="f5682-108">Prerequisites</span></span>

<span data-ttu-id="f5682-109">Följande programvara måste vara tillgänglig i systemet för att du ska kunna installera CLI:</span><span class="sxs-lookup"><span data-stu-id="f5682-109">In order to install the CLI, you need the following software available on your system:</span></span>

* [<span data-ttu-id="f5682-110">Python 2.7 eller Python 3.x</span><span class="sxs-lookup"><span data-stu-id="f5682-110">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="f5682-111">libffi</span><span class="sxs-lookup"><span data-stu-id="f5682-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="f5682-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f5682-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="f5682-113">Installera eller uppdatera</span><span class="sxs-lookup"><span data-stu-id="f5682-113">Install or update</span></span>

<span data-ttu-id="f5682-114">Oavsett om du installerar eller uppdaterar CLI så måste du utföra en fullständig installation.</span><span class="sxs-lookup"><span data-stu-id="f5682-114">Whether you are installing or updating the CLI, you need to perform a full installation.</span></span> <span data-ttu-id="f5682-115">När kraven är uppfyllda kan du installera CLI genom att köra `curl`.</span><span class="sxs-lookup"><span data-stu-id="f5682-115">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="f5682-116">Du kan även ladda ned skriptet och köra det lokalt istället.</span><span class="sxs-lookup"><span data-stu-id="f5682-116">You can also download the script and run it locally instead.</span></span> <span data-ttu-id="f5682-117">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="f5682-117">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="f5682-118">Efter installationen kör du CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f5682-118">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f5682-119">Felsökning</span><span class="sxs-lookup"><span data-stu-id="f5682-119">Troubleshooting</span></span>

<span data-ttu-id="f5682-120">Här är några vanliga problem som kan uppstå vid manuell installation.</span><span class="sxs-lookup"><span data-stu-id="f5682-120">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="f5682-121">Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="f5682-121">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>
### <a name="curl-object-moved-error"></a><span data-ttu-id="f5682-122">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="f5682-122">curl "Object Moved" error</span></span>

<span data-ttu-id="f5682-123">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="f5682-123">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="f5682-124">Det gick inte att hitta kommandot `az`</span><span class="sxs-lookup"><span data-stu-id="f5682-124">`az` command not found</span></span>

<span data-ttu-id="f5682-125">Om du inte kan köra kommandot efter installationen och använder `bash` eller `zsh` så kan du behöva rensa cacheminnet för gränssnittets kommando-hash</span><span class="sxs-lookup"><span data-stu-id="f5682-125">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="f5682-126">Kör</span><span class="sxs-lookup"><span data-stu-id="f5682-126">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="f5682-127">och kontrollera om problemet är löst.</span><span class="sxs-lookup"><span data-stu-id="f5682-127">and check if the problem is resolved.</span></span>

<span data-ttu-id="f5682-128">Det här problemet kan även inträffa om du inte startade om gränssnittet efter installationen.</span><span class="sxs-lookup"><span data-stu-id="f5682-128">The issue can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="f5682-129">Kontrollera att platsen för kommandot `az` är i `$PATH`.</span><span class="sxs-lookup"><span data-stu-id="f5682-129">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="f5682-130">`az`-kommandots plats är</span><span class="sxs-lookup"><span data-stu-id="f5682-130">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="f5682-131">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="f5682-131">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="f5682-132">Avinstallera CLI genom att ta bort filerna direkt från platsen som valts vid installationen.</span><span class="sxs-lookup"><span data-stu-id="f5682-132">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="f5682-133">Standardplatsen för installation är `$HOME`.</span><span class="sxs-lookup"><span data-stu-id="f5682-133">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="f5682-134">Ta bort de installerade CLI-filerna.</span><span class="sxs-lookup"><span data-stu-id="f5682-134">Remove the installed CLI files.</span></span>

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```
2. <span data-ttu-id="f5682-135">Ändra filen `$HOME/.bash_profile` för att ta bort följande rad:</span><span class="sxs-lookup"><span data-stu-id="f5682-135">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="f5682-136">Läs in gränssnittets kommandocacheminne om du använder `bash` eller `zsh`.</span><span class="sxs-lookup"><span data-stu-id="f5682-136">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

  ```bash
  hash -r
  ```
