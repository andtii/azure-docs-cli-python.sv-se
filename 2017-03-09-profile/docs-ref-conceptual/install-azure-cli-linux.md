---
title: "Installera Azure CLI 2.0 för Linux manuellt"
description: "Så här installerar du Azure CLI 2.0 på Linux manuellt"
keywords: Azure CLI,Install Azure CLI,azure linux, azure install linux
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
ms.openlocfilehash: cf1405cae70762146f63bc6629edc0dd1d949fff
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="5d721-104">Installera Azure CLI 2.0 på Linux manuellt</span><span class="sxs-lookup"><span data-stu-id="5d721-104">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="5d721-105">Om du inte har ett paket för Azure CLI tillgängligt i din distribution så kan du alltid installera CLI manuellt genom att köra ett skript för installation.</span><span class="sxs-lookup"><span data-stu-id="5d721-105">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manualy by running an installation script.</span></span> <span data-ttu-id="5d721-106">Om du har ett tillgängligt paket så är det alltid den rekommenderade installationsmetoden.</span><span class="sxs-lookup"><span data-stu-id="5d721-106">If you do have a package available, that is always the recommended installation method.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5d721-107">Krav</span><span class="sxs-lookup"><span data-stu-id="5d721-107">Prerequisites</span></span>

<span data-ttu-id="5d721-108">Följande programvara måste vara tillgänglig i systemet för att du ska kunna installera CLI:</span><span class="sxs-lookup"><span data-stu-id="5d721-108">In order to install the CLI, you will need the following software available on your system:</span></span>

* [<span data-ttu-id="5d721-109">Python 2.7 eller Python 3.x</span><span class="sxs-lookup"><span data-stu-id="5d721-109">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="5d721-110">libffi</span><span class="sxs-lookup"><span data-stu-id="5d721-110">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="5d721-111">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="5d721-111">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a><span data-ttu-id="5d721-112">Installera eller uppdatera manuellt</span><span class="sxs-lookup"><span data-stu-id="5d721-112">Install or update manually</span></span>

<span data-ttu-id="5d721-113">Oavsett om du installerar eller uppdaterar CLI så måste du utföra en fullständig installation.</span><span class="sxs-lookup"><span data-stu-id="5d721-113">Whether you are installing or updating the CLI, you will need to perform a full installation.</span></span> <span data-ttu-id="5d721-114">När kraven är uppfyllda kan du installera CLI genom att köra `curl`.</span><span class="sxs-lookup"><span data-stu-id="5d721-114">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="5d721-115">Om du inte har `curl` i systemet så kan du ladda ned skriptet och köra det lokalt i stället.</span><span class="sxs-lookup"><span data-stu-id="5d721-115">If you would prefer, or do not have `curl` on your system, you can download the script and run it locally instead.</span></span> <span data-ttu-id="5d721-116">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="5d721-116">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="5d721-117">Efter installationen kör du CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="5d721-117">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5d721-118">Felsökning</span><span class="sxs-lookup"><span data-stu-id="5d721-118">Troubleshooting</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="5d721-119">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="5d721-119">curl "Object Moved" error</span></span>

<span data-ttu-id="5d721-120">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="5d721-120">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="5d721-121">Det gick inte att hitta kommandot `az`</span><span class="sxs-lookup"><span data-stu-id="5d721-121">`az` command not found</span></span>

<span data-ttu-id="5d721-122">Om du inte kan köra kommandot efter installationen kan du behöva rensa cacheminnet för gränssnittets kommando-hash.</span><span class="sxs-lookup"><span data-stu-id="5d721-122">After installation if you can't run the command, you may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="5d721-123">Kör</span><span class="sxs-lookup"><span data-stu-id="5d721-123">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="5d721-124">och se om problemet är löst.</span><span class="sxs-lookup"><span data-stu-id="5d721-124">and see if the problem is resolved.</span></span>

<span data-ttu-id="5d721-125">Det här kan även inträffa om du inte startade om gränssnittet efter installationen.</span><span class="sxs-lookup"><span data-stu-id="5d721-125">This can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="5d721-126">Kontrollera att platsen för kommandot `az` är i `$PATH`.</span><span class="sxs-lookup"><span data-stu-id="5d721-126">Make sure that the location of the `az` command is in your `$PATH`.</span></span>

<span data-ttu-id="5d721-127">Om du körde installationsskriptet så är det följande:</span><span class="sxs-lookup"><span data-stu-id="5d721-127">If you ran the installation script, this will be:</span></span>

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a><span data-ttu-id="5d721-128">Avinstallera manuellt</span><span class="sxs-lookup"><span data-stu-id="5d721-128">Unstinall manually</span></span>

<span data-ttu-id="5d721-129">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="5d721-129">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="5d721-130">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="5d721-130">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="5d721-131">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="5d721-131">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="5d721-132">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="5d721-132">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="5d721-133">Du kan avinstallera CLI genom att ta bort filerna direkt från installationsplatsen.</span><span class="sxs-lookup"><span data-stu-id="5d721-133">You can uninstall the CLI by directly deleting the files from the install location.</span></span> <span data-ttu-id="5d721-134">Din installationsplats bör ha valts när installationen utfördes om du installerade via skriptet `https://aka.ms/InstallAzureCLI`.</span><span class="sxs-lookup"><span data-stu-id="5d721-134">Your install location should have been chosen at the time of install, if you installed via the `https://aka.ms/InstallAzureCLI` script.</span></span> <span data-ttu-id="5d721-135">Standardplatsen för installation är `$HOME`.</span><span class="sxs-lookup"><span data-stu-id="5d721-135">The default installation location is `$HOME`.</span></span>

<span data-ttu-id="5d721-136">Ta först bort de installerade CLI-filerna:</span><span class="sxs-lookup"><span data-stu-id="5d721-136">First, remove the installed CLI files:</span></span>

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

<span data-ttu-id="5d721-137">Ändra filen `$HOME/.bash_profile` för att ta bort raden:</span><span class="sxs-lookup"><span data-stu-id="5d721-137">Then modify your `$HOME/.bash_profile` file to remove the line:</span></span>

```
<install location>/lib/azure-cli/az.completion
```

<span data-ttu-id="5d721-138">Läs slutligen in gränssnittets kommandocacheminne igen om det används.</span><span class="sxs-lookup"><span data-stu-id="5d721-138">And finally, reload your shell's command cache if it uses one.</span></span> <span data-ttu-id="5d721-139">Användare av `bash` och `zsh` måste utföra det här steget:</span><span class="sxs-lookup"><span data-stu-id="5d721-139">`bash` and `zsh` users will need to perform this step:</span></span>

```bash
hash -r
```
