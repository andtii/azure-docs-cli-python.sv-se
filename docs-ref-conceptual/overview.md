---
title: Azure CLI 2.0
description: "Översikt över Azure CLI 2.0."
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 92079f3fa17f69a560e937101aa9e6f09c3080eb
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2018
---
# <a name="azure-cli-20"></a><span data-ttu-id="9616b-104">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="9616b-104">Azure CLI 2.0</span></span>

<span data-ttu-id="9616b-105">Azure CLI 2.0 är Azures nya kommandoradsmiljö för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="9616b-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="9616b-106">Du kan använda den i din webbläsare med [Azure Cloud Shell](/azure/cloud-shell/overview) eller [installera](install-azure-cli.md) den på macOS, Linux och Windows och köra den från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="9616b-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="9616b-107">Azure CLI 2.0 är optimerad för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9616b-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="9616b-108">Med Azure CLI 2.0 kan du skapa virtuella datorer i Azure genom att bara skriva följande kommando:</span><span class="sxs-lookup"><span data-stu-id="9616b-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="9616b-109">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra CLI i webbläsaren eller [installera](install-azure-cli.md) det på macOS, Linux eller Windows.</span><span class="sxs-lookup"><span data-stu-id="9616b-109">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="9616b-110">Läs artikeln [Kom igång](get-started-with-azure-cli.md) för att komma igång med CLI.</span><span class="sxs-lookup"><span data-stu-id="9616b-110">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="9616b-111">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="9616b-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="9616b-112">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure CLI 2.0:</span><span class="sxs-lookup"><span data-stu-id="9616b-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="9616b-113">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="9616b-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9616b-114">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="9616b-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9616b-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="9616b-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9616b-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="9616b-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="9616b-117">Det finns även en tillgänglig detaljerad [referens](/cli/azure/) som dokumenterar hur du ska använda varje enskilt kommando i Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="9616b-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="9616b-118">[Kom igång](get-started-with-azure-cli.md) med Azure CLI 2.0 nu.</span><span class="sxs-lookup"><span data-stu-id="9616b-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="9616b-119">Om du använder den tidigare versionen av CLI (Azure CLI), kan du fortsätta att använda den.</span><span class="sxs-lookup"><span data-stu-id="9616b-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="9616b-120">Om du använder båda CLI:erna ska du komma ihåg att `azure` är den gamla CLI:n – Azure CLI, och att `az` är den nya – Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="9616b-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>