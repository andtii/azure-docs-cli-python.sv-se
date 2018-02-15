---
title: "Installera Azure CLI för Windows"
description: "Så här installerar du Azure CLI 2.0 i Windows"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 3e732ea7fae118ddb1564bed28d54d15bab4f7f0
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="4750f-103">Installera Azure CLI 2.0 i Windows</span><span class="sxs-lookup"><span data-stu-id="4750f-103">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="4750f-104">På Windows installeras Azure CLI-binärfilen via en MSI, vilket ger dig åtkomst till CLI via Windows kommandotolk (CMD) eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4750f-104">On Windows the Azure CLI binary is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="4750f-105">Om du använder ett Windows-undersystem för Linux (WSL) finns paket tillgängliga för din Linux-distribution.</span><span class="sxs-lookup"><span data-stu-id="4750f-105">If you are running Windows Subsystem for Linux (WSL), there are packages available for your Linux distribution.</span></span> <span data-ttu-id="4750f-106">På den [primära installationssidan](install-azure-cli.md) finns en lista med pakethanterare som stöds eller instruktioner om hur du installerar manuellt under WSL.</span><span class="sxs-lookup"><span data-stu-id="4750f-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="4750f-107">Installera eller uppdatera</span><span class="sxs-lookup"><span data-stu-id="4750f-107">Install or update</span></span>

<span data-ttu-id="4750f-108">MSI-delen som kan distribueras används för installation, uppdatering och avinstallation av kommandot `az` i Windows.</span><span class="sxs-lookup"><span data-stu-id="4750f-108">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4750f-109">Ladda ned MSI-installationsprogrammet</span><span class="sxs-lookup"><span data-stu-id="4750f-109">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)

<span data-ttu-id="4750f-110">När installationsprogrammet frågar om ändringar kan göras på din dator klickar du på ”Ja”.</span><span class="sxs-lookup"><span data-stu-id="4750f-110">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="4750f-111">Du kan nu köra Azure CLI med kommandot `az` från antingen kommandotolken i Windows eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4750f-111">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="4750f-112">PowerShell erbjuder vissa funktioner för tabbifyllning som inte är tillgängliga från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="4750f-112">PowerShell offers some tab completion features not available from CMD.</span></span>

## <a name="uninstall"></a><span data-ttu-id="4750f-113">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="4750f-113">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="4750f-114">Du kan avinstallera genom att köra MSI igen och välja alternativet ”Avinstallera”.</span><span class="sxs-lookup"><span data-stu-id="4750f-114">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4750f-115">Ladda ned MSI-installationsprogrammet</span><span class="sxs-lookup"><span data-stu-id="4750f-115">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)
