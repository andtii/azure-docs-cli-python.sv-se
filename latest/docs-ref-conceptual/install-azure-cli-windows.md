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
ms.openlocfilehash: 96a123575226f281accf125cb5bb29ee7d14ef2a
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-windows"></a>Installera Azure CLI 2.0 i Windows

I Windows kan du installera en intern binärfil från en MSI som du kan använda via kommandotolken i Windows eller PowerShell. Om du använder ett Windows-undersystem för Linux (WSL) finns paket tillgängliga för den distribution som du kör. På den [primära installationssidan](install-azure-cli.md) finns en lista med pakethanterare som stöds eller instruktioner om hur du installerar manuellt under WSL.

## <a name="install-or-update-with-msi"></a>Installera eller uppdatera med MSI

MSI-delen som kan distribueras används för installation, uppdatering och avinstallation av kommandot `az` i Windows. Du kan [ladda ned MSI-installationsprogrammet](https://aka.ms/InstallAzureCliWindows) och sedan köra det för att installera eller uppdatera.

När installationsprogrammet frågar om ändringar kan göras på din dator klickar du på ”Ja”.

Du kan nu köra Azure CLI med kommandot `az` från antingen kommandotolken i Windows eller PowerShell.

## <a name="uninstall-with-msi"></a>Avinstallera med MSI

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

Avinstallation kan utföras genom att köra MSI igen och välja alternativet ”Avinstallera”. Du kan [ladda ned MSI-installationsprogrammet](https://aka.ms/InstallAzureCliWindows) om du inte längre har det på din dator.
