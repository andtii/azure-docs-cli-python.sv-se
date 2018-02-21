---
title: "Installera Azure CLI för macOS"
description: "Så här installerar du Azure CLI 2.0 på macOS"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 0295846abc2fe6091940824c6efc47b8fd64ce9f
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="b8957-103">Installera Azure CLI 2.0 på macOS</span><span class="sxs-lookup"><span data-stu-id="b8957-103">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="b8957-104">På macOS-plattformen kan du installera Azure CLI med [Homebrew-pakethanteraren](http://brew.sh).</span><span class="sxs-lookup"><span data-stu-id="b8957-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](http://brew.sh).</span></span> <span data-ttu-id="b8957-105">Med Homebrew är det enkelt att se till att installationen av CLI alltid är uppdaterad.</span><span class="sxs-lookup"><span data-stu-id="b8957-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="b8957-106">CLI-paketet har testats på macOS-versionerna 10.9 och senare.</span><span class="sxs-lookup"><span data-stu-id="b8957-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="b8957-107">Installera</span><span class="sxs-lookup"><span data-stu-id="b8957-107">Install</span></span>

<span data-ttu-id="b8957-108">CLI-installationen hanteras enklast med Homebrew.</span><span class="sxs-lookup"><span data-stu-id="b8957-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="b8957-109">Homebrew erbjuder ett bekvämt sätt att installera, uppdatera och avinstallera.</span><span class="sxs-lookup"><span data-stu-id="b8957-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="b8957-110">Om du inte har Homebrew i systemet kan du [installera Homebrew](https://docs.brew.sh/Installation.html) innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="b8957-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="b8957-111">Du kan installera CLI genom att uppdatera informationen om brew-lagringsplatsen och sedan köra kommandot `install`:</span><span class="sxs-lookup"><span data-stu-id="b8957-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="b8957-112">Sedan kan du köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="b8957-112">You can then run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b8957-113">Felsökning</span><span class="sxs-lookup"><span data-stu-id="b8957-113">Troubleshooting</span></span>

<span data-ttu-id="b8957-114">Om du stötte på problem när du installerade CLI med Homebrew så är det här några vanliga fel som kan uppstå.</span><span class="sxs-lookup"><span data-stu-id="b8957-114">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="b8957-115">Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="b8957-115">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="b8957-116">Det gick inte att hitta Python eller installerade paket</span><span class="sxs-lookup"><span data-stu-id="b8957-116">Unable to find Python or installed packages</span></span>

<span data-ttu-id="b8957-117">Om installationen inte kunde hitta Python eller installerade paket så kan det bero på en versionskonflikt eller något annat problem som uppstod under installationen av Homebrew.</span><span class="sxs-lookup"><span data-stu-id="b8957-117">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue that occurred during homebrew installation.</span></span> <span data-ttu-id="b8957-118">Eftersom CLI inte använder en virtuell Python-miljö så är det viktigt att det går att hitta rätt version av Python.</span><span class="sxs-lookup"><span data-stu-id="b8957-118">Since the CLI does not use a Python virtual environment, it relies on being able to find correct Python version.</span></span> <span data-ttu-id="b8957-119">Du kan åtgärda de här problemen genom att länka till Python-installationen igen.</span><span class="sxs-lookup"><span data-stu-id="b8957-119">You may be able to fix these issues by relinking your Python installation.</span></span>

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="b8957-120">CLI-version 1.x har installerats</span><span class="sxs-lookup"><span data-stu-id="b8957-120">CLI version 1.x is installed</span></span>

<span data-ttu-id="b8957-121">Om en inaktuell version installerades kan det bero på en föråldrad homebrew-cache.</span><span class="sxs-lookup"><span data-stu-id="b8957-121">If an out-of-date version was installed, it could be due to a stale homebrew cache.</span></span> <span data-ttu-id="b8957-122">Följ anvisningarna för [uppdateringen](#Update).</span><span class="sxs-lookup"><span data-stu-id="b8957-122">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="b8957-123">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="b8957-123">Update</span></span>

<span data-ttu-id="b8957-124">CLI uppdateras regelbundet med felkorrigeringar, förbättringar, nya funktioner och förhandsgranskningsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="b8957-124">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="b8957-125">En ny version blir tillgänglig ungefär varannan vecka.</span><span class="sxs-lookup"><span data-stu-id="b8957-125">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="b8957-126">Uppdatera informationen om din lokala lagringsplats och uppgradera sedan `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="b8957-126">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="b8957-127">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="b8957-127">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="b8957-128">Använd Homebrew för att avinstallera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="b8957-128">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```
