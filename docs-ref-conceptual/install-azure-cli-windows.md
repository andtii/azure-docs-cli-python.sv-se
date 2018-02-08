---
title: "Installera Azure CLI för Windows"
description: "Så här installerar du Azure CLI 2.0 i Windows"
keywords: Azure CLI,Install Azure CLI,azure install windows, azure cli windows, azure windows
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: fc84b80e44a994495ef97cf9d7ec4e4a79a5c5b3
ms.sourcegitcommit: b41c5ed4a26c771a1a32b4560131f7a65b80fd33
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/03/2018
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="2eaec-104">Installera Azure CLI 2.0 i Windows</span><span class="sxs-lookup"><span data-stu-id="2eaec-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="2eaec-105">På Windows installeras Azure CLI-binärfilen via en MSI, vilket ger dig åtkomst till CLI via Windows kommandotolk (CMD) eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2eaec-105">On Windows the Azure CLI binary is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="2eaec-106">Om du använder ett Windows-undersystem för Linux (WSL) finns paket tillgängliga för din Linux-distribution.</span><span class="sxs-lookup"><span data-stu-id="2eaec-106">If you are running Windows Subsystem for Linux (WSL), there are packages available for your Linux distribution.</span></span> <span data-ttu-id="2eaec-107">På den [primära installationssidan](install-azure-cli.md) finns en lista med pakethanterare som stöds eller instruktioner om hur du installerar manuellt under WSL.</span><span class="sxs-lookup"><span data-stu-id="2eaec-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="2eaec-108">Installera eller uppdatera</span><span class="sxs-lookup"><span data-stu-id="2eaec-108">Install or update</span></span>

<span data-ttu-id="2eaec-109">MSI-delen som kan distribueras används för installation, uppdatering och avinstallation av kommandot `az` i Windows.</span><span class="sxs-lookup"><span data-stu-id="2eaec-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="2eaec-110">Ladda ned MSI-installationsprogrammet</span><span class="sxs-lookup"><span data-stu-id="2eaec-110">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)

<span data-ttu-id="2eaec-111">När installationsprogrammet frågar om ändringar kan göras på din dator klickar du på ”Ja”.</span><span class="sxs-lookup"><span data-stu-id="2eaec-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="2eaec-112">Du kan nu köra Azure CLI med kommandot `az` från antingen kommandotolken i Windows eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2eaec-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="2eaec-113">PowerShell erbjuder vissa funktioner för tabbifyllning som inte är tillgängliga från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="2eaec-113">PowerShell offers some tab completion features not available from CMD.</span></span>

## <a name="uninstall"></a><span data-ttu-id="2eaec-114">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="2eaec-114">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="2eaec-115">Du kan avinstallera genom att köra MSI igen och välja alternativet ”Avinstallera”.</span><span class="sxs-lookup"><span data-stu-id="2eaec-115">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> 

> [!div class="nextstepaction"]
> [<span data-ttu-id="2eaec-116">Ladda ned MSI-installationsprogrammet</span><span class="sxs-lookup"><span data-stu-id="2eaec-116">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)
