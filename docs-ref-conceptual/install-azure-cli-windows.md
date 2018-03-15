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
ms.openlocfilehash: df1c2b33589c160525710845cc81d076082a9ecc
ms.sourcegitcommit: def1a07bfccf26a4178ba6dd836764a1df205929
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/09/2018
---
# <a name="install-azure-cli-20-on-windows"></a>Installera Azure CLI 2.0 i Windows

På Windows installeras Azure CLI-binärfilen via en MSI, vilket ger dig åtkomst till CLI via Windows kommandotolk (CMD) eller PowerShell.
Om du använder ett Windows-undersystem för Linux (WSL) finns paket tillgängliga för din Linux-distribution. På den [primära installationssidan](install-azure-cli.md) finns en lista med pakethanterare som stöds eller instruktioner om hur du installerar manuellt under WSL.

## <a name="install-or-update"></a>Installera eller uppdatera

MSI-delen som kan distribueras används för installation, uppdatering och avinstallation av kommandot `az` i Windows.

> [!div class="nextstepaction"]
> [Ladda ned MSI-installationsprogrammet](https://aka.ms/installazurecliwindows)

När installationsprogrammet frågar om ändringar kan göras på din dator klickar du på ”Ja”.

Du kan nu köra Azure CLI med kommandot `az` från antingen kommandotolken i Windows eller PowerShell. PowerShell erbjuder vissa funktioner för tabbifyllning som inte är tillgängliga från kommandoraden.

## <a name="uninstall"></a>Avinstallera

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

Du kan avinstallera genom att köra MSI igen och välja alternativet ”Avinstallera”.

> [!div class="nextstepaction"]
> [Ladda ned MSI-installationsprogrammet](https://aka.ms/installazurecliwindows)
