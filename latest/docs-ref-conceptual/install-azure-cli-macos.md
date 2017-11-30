---
title: "Installera Azure CLI för macOS"
description: "Så här installerar du Azure CLI 2.0 på macOS"
keywords: Azure CLI,Install Azure CLI,azure macos, azure install macos
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e615d2b3ab3b1307e982cb1d4d456633440afdf6
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="726d1-104">Installera Azure CLI 2.0 på macOS</span><span class="sxs-lookup"><span data-stu-id="726d1-104">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="726d1-105">På macOS-plattformen kan du installera Azure CLI via antingen [pakethanteraren Homebrew](http://brew.sh) eller manuellt.</span><span class="sxs-lookup"><span data-stu-id="726d1-105">For the macOS platform, you can install the Azure CLI either through the [homebrew package manager](http://brew.sh) or manually.</span></span> <span data-ttu-id="726d1-106">Vi rekommenderar att du installerar via Homebrew. Då blir det enklare att installera, hämta uppdateringar och avinstallera om du skulle behöva det.</span><span class="sxs-lookup"><span data-stu-id="726d1-106">The preferred installation method is through homebrew, so that it's easier to install, get updates, and uninstall if you need to.</span></span>

## <a name="use-homebrew-to-install"></a><span data-ttu-id="726d1-107">Använda Homebrew för att installera</span><span class="sxs-lookup"><span data-stu-id="726d1-107">Use homebrew to install</span></span>

<span data-ttu-id="726d1-108">CLI-installationen hanteras enklast med Homebrew.</span><span class="sxs-lookup"><span data-stu-id="726d1-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="726d1-109">Homebrew erbjuder ett bekvämt sätt att installera, uppdatera och avinstallera.</span><span class="sxs-lookup"><span data-stu-id="726d1-109">It provides convenient ways to install, update, and uninstall.</span></span> <span data-ttu-id="726d1-110">Det påminner om andra pakethanterare, till exempel `apt` och `yum`.</span><span class="sxs-lookup"><span data-stu-id="726d1-110">It's similar to other package managers such as `apt` or `yum`.</span></span>
<span data-ttu-id="726d1-111">Om du inte har Homebrew i systemet kan du [installera Homebrew](https://docs.brew.sh/Installation.html) innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="726d1-111">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="726d1-112">Installera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="726d1-112">Install with homebrew</span></span>

<span data-ttu-id="726d1-113">Du kan installera CLI genom att uppdatera informationen om brew-lagringsplatsen och sedan köra kommandot `install`:</span><span class="sxs-lookup"><span data-stu-id="726d1-113">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="726d1-114">Sedan kan du köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="726d1-114">You can then run the Azure CLI with the `az` command.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="726d1-115">Uppdatera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="726d1-115">Update with homebrew</span></span>

<span data-ttu-id="726d1-116">CLI uppdateras regelbundet med felkorrigeringar, förbättringar, nya funktioner och förhandsgranskningsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="726d1-116">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="726d1-117">En ny version blir tillgänglig ungefär varannan vecka.</span><span class="sxs-lookup"><span data-stu-id="726d1-117">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="726d1-118">Om du vill uppdatera CLI-paketet måste du uppdatera informationen om din lokala lagringsplats.</span><span class="sxs-lookup"><span data-stu-id="726d1-118">You will need to update your local repository information, and then update the CLI package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a><span data-ttu-id="726d1-119">Felsökning</span><span class="sxs-lookup"><span data-stu-id="726d1-119">Troubleshooting</span></span>

<span data-ttu-id="726d1-120">Stötte du på problem när du installerade eller uppdaterade CLI med Homebrew?</span><span class="sxs-lookup"><span data-stu-id="726d1-120">Did you encounter a problem when installing or updating the CLI with homebrew?</span></span> <span data-ttu-id="726d1-121">Här är några vanliga fel som kan uppstå, samt sätt att diagnostisera och lösa dem.</span><span class="sxs-lookup"><span data-stu-id="726d1-121">Here are some common errors that might occur, and ways to diagnose and resolve them.</span></span>

#### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="726d1-122">Det gick inte att hitta Python eller installerade paket</span><span class="sxs-lookup"><span data-stu-id="726d1-122">Unable to find Python or installed packages</span></span>

<span data-ttu-id="726d1-123">Om installationen inte kunde hitta Python eller installerade paket så kan detta bero på en versionskonflikt eller något annat problem som uppstod under installationen av Homebrew.</span><span class="sxs-lookup"><span data-stu-id="726d1-123">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue which occurred during homebrew installation.</span></span> <span data-ttu-id="726d1-124">Eftersom CLI inte använder en virtuell miljö måste det gå att hitta rätt versioner av Python som har installerats av Homebrew.</span><span class="sxs-lookup"><span data-stu-id="726d1-124">Since the CLI does not use a virtualenv, it relies on being able to find correct versions of Python installed by homebrew.</span></span> <span data-ttu-id="726d1-125">Du kan åtgärda dessa problem genom att länka till Python-installationen igen:</span><span class="sxs-lookup"><span data-stu-id="726d1-125">You may be able to fix these issues by re-linking your Python installation:</span></span>

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a><span data-ttu-id="726d1-126">CLI-versionen är inaktuell</span><span class="sxs-lookup"><span data-stu-id="726d1-126">The CLI version is out of date</span></span>

<span data-ttu-id="726d1-127">Om du tror att den installerade versionen av CLI kan vara inaktuell så kan du köra kommandot `brew update` följt av `brew upgrade azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="726d1-127">If you think that your installed CLI version might be out of date, you will need to run a `brew update` command, followed by `brew upgrade azure-cli`.</span></span> <span data-ttu-id="726d1-128">Tänk på att Homebrew-paket kan släppas långsammare än allmänna versioner om CLI inte uppdateras.</span><span class="sxs-lookup"><span data-stu-id="726d1-128">If this does not update the CLI, be aware that homebrew packages may roll out more slowly than general releases.</span></span> <span data-ttu-id="726d1-129">Om du behöver de absolut senaste installationerna av CLI så bör du [installera manuellt](#manage-the-cli-manually).</span><span class="sxs-lookup"><span data-stu-id="726d1-129">If you require bleeding-edge installs of the CLI, then you should [install manually](#manage-the-cli-manually).</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="726d1-130">Avinstallera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="726d1-130">Uninstall with homebrew</span></span>

<span data-ttu-id="726d1-131">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="726d1-131">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="726d1-132">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="726d1-132">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="726d1-133">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="726d1-133">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="726d1-134">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="726d1-134">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="726d1-135">Om du installerade med Homebrew så bör du även använda det för att avinstallera.</span><span class="sxs-lookup"><span data-stu-id="726d1-135">If you installed with homebrew, you should also use it to uninstall.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a><span data-ttu-id="726d1-136">Installera CLI manuellt</span><span class="sxs-lookup"><span data-stu-id="726d1-136">Install the CLI manually</span></span>

<span data-ttu-id="726d1-137">Om du inte kan eller inte vill använda Homebrew för att utföra CLI-installationen så kan du installera manuellt.</span><span class="sxs-lookup"><span data-stu-id="726d1-137">If you can't or don't want to rely on homebrew to manage the CLI install for you, then you can manually install.</span></span>

<span data-ttu-id="726d1-138">Följ anvisningarna för [manuell installation på Linux](install-azure-cli-linux.md) för att installera manuellt på macOS.</span><span class="sxs-lookup"><span data-stu-id="726d1-138">Follow the [manual Linux installation instructions](install-azure-cli-linux.md) to install manually on macOS.</span></span> <span data-ttu-id="726d1-139">macOS-version 10.9 och senare bör innehålla alla nödvändiga beroenden.</span><span class="sxs-lookup"><span data-stu-id="726d1-139">macOS versions 10.9 and later should include all of the required dependencies.</span></span>
