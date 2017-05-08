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
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 är Azures nya kommandoradsmiljö för att hantera Azure-resurser.  Den kan användas i Mac OS, Linux och Windows. 

Azure CLI 2.0 är optimerad för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager. Med Azure CLI 2.0 kan du skapa virtuella datorer i Azure genom att bara skriva följande kommando:

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

Läs [installationsartikeln](install-azure-cli.md) för att komma igång med Azure CLI 2.0 på datorn. Läs artikeln [Kom igång](get-started-with-azure-cli.md) för att börja använda programmet.
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