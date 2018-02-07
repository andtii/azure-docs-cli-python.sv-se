---
title: "Installera Azure CLI för macOS"
description: "Så här installerar du Azure CLI 2.0 på macOS"
keywords: "Azure CLI, Installera Azure CLI, azure macos, installera azure för macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 36fd2604677db0b7f820ee11884bf790fb1d75cb
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="2c220-104">Installera Azure CLI 2.0 på macOS</span><span class="sxs-lookup"><span data-stu-id="2c220-104">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="2c220-105">På macOS-plattformen kan du installera Azure CLI via [pakethanteraren Homebrew](http://brew.sh).</span><span class="sxs-lookup"><span data-stu-id="2c220-105">For the macOS platform, you can install the Azure CLI either through the [homebrew package manager](http://brew.sh).</span></span> <span data-ttu-id="2c220-106">Med Homebrew är det enkelt att se till att installationen av CLI alltid är uppdaterad.</span><span class="sxs-lookup"><span data-stu-id="2c220-106">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="2c220-107">CLI-paketet har testats på macOS-versionerna 10.9 och senare.</span><span class="sxs-lookup"><span data-stu-id="2c220-107">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="2c220-108">Installera</span><span class="sxs-lookup"><span data-stu-id="2c220-108">Install</span></span>

<span data-ttu-id="2c220-109">CLI-installationen hanteras enklast med Homebrew.</span><span class="sxs-lookup"><span data-stu-id="2c220-109">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="2c220-110">Homebrew erbjuder ett bekvämt sätt att installera, uppdatera och avinstallera.</span><span class="sxs-lookup"><span data-stu-id="2c220-110">It provides convenient ways to install, update, and uninstall.</span></span> <span data-ttu-id="2c220-111">Om du inte har Homebrew i systemet kan du [installera Homebrew](https://docs.brew.sh/Installation.html) innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="2c220-111">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="2c220-112">Du kan installera CLI genom att uppdatera informationen om brew-lagringsplatsen och sedan köra kommandot `install`:</span><span class="sxs-lookup"><span data-stu-id="2c220-112">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="2c220-113">Sedan kan du köra Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="2c220-113">You can then run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2c220-114">Felsökning</span><span class="sxs-lookup"><span data-stu-id="2c220-114">Troubleshooting</span></span>

<span data-ttu-id="2c220-115">Om du stötte på problem när du installerade CLI med Homebrew så är det här några vanliga fel som kan uppstå.</span><span class="sxs-lookup"><span data-stu-id="2c220-115">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="2c220-116">Om ditt problem inte visas här så kan du [öppna ett github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="2c220-116">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="2c220-117">Det gick inte att hitta Python eller installerade paket</span><span class="sxs-lookup"><span data-stu-id="2c220-117">Unable to find Python or installed packages</span></span>

<span data-ttu-id="2c220-118">Om installationen inte kunde hitta Python eller installerade paket så kan det bero på en versionskonflikt eller något annat problem som uppstod under installationen av Homebrew.</span><span class="sxs-lookup"><span data-stu-id="2c220-118">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue that occurred during homebrew installation.</span></span> <span data-ttu-id="2c220-119">Eftersom CLI inte använder en virtuell Python-miljö så är det viktigt att det går att hitta rätt version av Python.</span><span class="sxs-lookup"><span data-stu-id="2c220-119">Since the CLI does not use a Python virtual environment, it relies on being able to find correct Python version.</span></span> <span data-ttu-id="2c220-120">Du kan åtgärda de här problemen genom att länka till Python-installationen igen.</span><span class="sxs-lookup"><span data-stu-id="2c220-120">You may be able to fix these issues by relinking your Python installation.</span></span>

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="2c220-121">CLI-version 1.x har installerats</span><span class="sxs-lookup"><span data-stu-id="2c220-121">CLI version 1.x is installed</span></span>

<span data-ttu-id="2c220-122">Om en inaktuell version installerades kan det bero på en föråldrad homebrew-cache.</span><span class="sxs-lookup"><span data-stu-id="2c220-122">If an out-of-date version was installed, it could be due to a stale homebrew cache.</span></span> <span data-ttu-id="2c220-123">Följ anvisningarna för [uppdateringen](#Update).</span><span class="sxs-lookup"><span data-stu-id="2c220-123">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="2c220-124">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="2c220-124">Update</span></span>

<span data-ttu-id="2c220-125">CLI uppdateras regelbundet med felkorrigeringar, förbättringar, nya funktioner och förhandsgranskningsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="2c220-125">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="2c220-126">En ny version blir tillgänglig ungefär varannan vecka.</span><span class="sxs-lookup"><span data-stu-id="2c220-126">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="2c220-127">Uppdatera informationen om din lokala lagringsplats och uppgradera sedan `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="2c220-127">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="2c220-128">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="2c220-128">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="2c220-129">Använd Homebrew för att avinstallera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="2c220-129">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```
