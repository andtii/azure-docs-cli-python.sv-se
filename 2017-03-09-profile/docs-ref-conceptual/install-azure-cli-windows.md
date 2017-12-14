---
title: "Installera Azure CLI för Windows"
description: "Så här installerar du Azure CLI 2.0 i Windows"
keywords: Azure CLI,Install Azure CLI,azure install windows, azure cli windows, azure windows
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
ms.openlocfilehash: 247ae43813ca9ca7b7b98ebd8e933e02989c6649
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="f2373-104">Installera Azure CLI 2.0 i Windows</span><span class="sxs-lookup"><span data-stu-id="f2373-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="f2373-105">I Windows kan du installera en intern binärfil från en MSI som du kan använda via kommandotolken i Windows eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f2373-105">On Windows, you can install a native binary from an MSI, which you can use through the Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="f2373-106">Om du använder ett Windows-undersystem för Linux (WSL) finns paket tillgängliga för den distribution som du kör.</span><span class="sxs-lookup"><span data-stu-id="f2373-106">If you are running Windows Subsystem for Linux (WSL) there are packages available for the distribution you are running.</span></span> <span data-ttu-id="f2373-107">På den [primära installationssidan](install-azure-cli.md) finns en lista med pakethanterare som stöds eller instruktioner om hur du installerar manuellt under WSL.</span><span class="sxs-lookup"><span data-stu-id="f2373-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update-with-msi"></a><span data-ttu-id="f2373-108">Installera eller uppdatera med MSI</span><span class="sxs-lookup"><span data-stu-id="f2373-108">Install or update with MSI</span></span>

<span data-ttu-id="f2373-109">MSI-delen som kan distribueras används för installation, uppdatering och avinstallation av kommandot `az` i Windows.</span><span class="sxs-lookup"><span data-stu-id="f2373-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span> <span data-ttu-id="f2373-110">Du kan [ladda ned MSI-installationsprogrammet](https://aka.ms/InstallAzureCliWindows) och sedan köra det för att installera eller uppdatera.</span><span class="sxs-lookup"><span data-stu-id="f2373-110">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) and then run it to install or update.</span></span>

<span data-ttu-id="f2373-111">När installationsprogrammet frågar om ändringar kan göras på din dator klickar du på ”Ja”.</span><span class="sxs-lookup"><span data-stu-id="f2373-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="f2373-112">Du kan nu köra Azure CLI med kommandot `az` från antingen kommandotolken i Windows eller PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f2373-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span>

## <a name="uninstall-with-msi"></a><span data-ttu-id="f2373-113">Avinstallera med MSI</span><span class="sxs-lookup"><span data-stu-id="f2373-113">Uninstall with MSI</span></span>

<span data-ttu-id="f2373-114">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="f2373-114">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f2373-115">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="f2373-115">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="f2373-116">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="f2373-116">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="f2373-117">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="f2373-117">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="f2373-118">Du kan avinstallera genom att köra MSI igen och välja alternativet ”Avinstallera”.</span><span class="sxs-lookup"><span data-stu-id="f2373-118">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> <span data-ttu-id="f2373-119">Du kan [ladda ned MSI-installationsprogrammet](https://aka.ms/InstallAzureCliWindows) om du inte längre har det på din dator.</span><span class="sxs-lookup"><span data-stu-id="f2373-119">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) if you no longer have it available.</span></span>
