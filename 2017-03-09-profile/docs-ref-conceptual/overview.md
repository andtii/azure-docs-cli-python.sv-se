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
ms.openlocfilehash: 2f4f9950dd663ae85f41bf4efe114b15770ace5d
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: sv-SE
---
# <a name="azure-cli-20"></a><span data-ttu-id="a548f-104">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="a548f-104">Azure CLI 2.0</span></span>

<span data-ttu-id="a548f-105">Azure CLI 2.0 är Azures nya kommandoradsmiljö för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="a548f-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>  <span data-ttu-id="a548f-106">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="a548f-106">It can be used on macOS, Linux, and Windows.</span></span> 

<span data-ttu-id="a548f-107">Azure CLI 2.0 är optimerad för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a548f-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="a548f-108">Med Azure CLI 2.0 kan du skapa virtuella datorer i Azure genom att bara skriva följande kommando:</span><span class="sxs-lookup"><span data-stu-id="a548f-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="a548f-109">Läs [installationsartikeln](install-azure-cli.md) för att komma igång med Azure CLI 2.0 på datorn.</span><span class="sxs-lookup"><span data-stu-id="a548f-109">Review the [Install article](install-azure-cli.md) to get Azure CLI 2.0 up and running on your system.</span></span> <span data-ttu-id="a548f-110">Läs artikeln [Kom igång](get-started-with-azure-cli.md) för att börja använda programmet.</span><span class="sxs-lookup"><span data-stu-id="a548f-110">Then read the [Get Started](get-started-with-azure-cli.md) article to begin using it.</span></span>
<span data-ttu-id="a548f-111">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="a548f-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="a548f-112">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure CLI 2.0:</span><span class="sxs-lookup"><span data-stu-id="a548f-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="a548f-113">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="a548f-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a548f-114">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="a548f-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a548f-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="a548f-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a548f-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="a548f-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="a548f-117">Det finns även en tillgänglig detaljerad [referens](/cli/azure/) som dokumenterar hur du ska använda varje enskilt kommando i Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="a548f-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="a548f-118">[Kom igång](get-started-with-azure-cli.md) med Azure CLI 2.0 nu.</span><span class="sxs-lookup"><span data-stu-id="a548f-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="a548f-119">Om du använder den tidigare versionen av CLI (Azure CLI), kan du fortsätta att använda den.</span><span class="sxs-lookup"><span data-stu-id="a548f-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="a548f-120">Om du använder båda CLI:erna ska du komma ihåg att `azure` är den gamla CLI:n – Azure CLI, och att `az` är den nya – Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="a548f-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 