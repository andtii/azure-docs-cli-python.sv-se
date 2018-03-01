---
title: Azure CLI 2.0
description: "Översikt över Azure CLI 2.0."
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5f3d514200b138d498043e0efb2cf5c2f478d108
ms.sourcegitcommit: f3ab5da6019083ef2482b62c7355817e6170dcfb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/28/2018
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 är Azures nya kommandoradsmiljö för att hantera Azure-resurser.
Du kan använda den i din webbläsare med [Azure Cloud Shell](/azure/cloud-shell/overview) eller [installera](install-azure-cli.md) den på macOS, Linux och Windows och köra den från kommandoraden.

Azure CLI 2.0 är optimerad för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager. Med Azure CLI 2.0 kan du skapa virtuella datorer i Azure genom att bara skriva följande kommando:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra CLI i webbläsaren eller [installera](install-azure-cli.md) det på macOS, Linux eller Windows.
Läs artikeln [Kom igång](get-started-with-azure-cli.md) för att komma igång med CLI.
Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).

Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure CLI 2.0:
- [Virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

Det finns även en tillgänglig detaljerad [referens](/cli/azure/) som dokumenterar hur du ska använda varje enskilt kommando i Azure CLI 2.0.

[Kom igång](get-started-with-azure-cli.md) med Azure CLI 2.0 nu.


> [!NOTE]
> Om du använder den tidigare versionen av CLI (Azure CLI), kan du fortsätta att använda den.
> Om du använder båda CLI:erna ska du komma ihåg att `azure` är den gamla CLI:n – Azure CLI, och att `az` är den nya – Azure CLI 2.0.
