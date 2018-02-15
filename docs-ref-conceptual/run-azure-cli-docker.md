---
title: "Kör Azure CLI 2.0 i en Docker-behållare"
description: "Så här kör du en Docker-behållare med en värdlösning för Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 3a09eb6d83bb5401628bd952d199a03ecbb8216e
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a>Kör Azure CLI 2.0 i en Docker-behållare

Du kan använda Docker för att köra en fristående Linux-behållare om Azure CLI 2.0 redan är installerat. Med Docker kan du snabbt komma igång med en miljö där du kan prova CLI för att avgöra om det är rätt för dig. Du kan även utgå från vår avbildning i din egen distribution.

## <a name="run-in-a-docker-container"></a>Kör i en Docker-behållare

Installera CLI med `docker run`.

   ```bash
   docker run -it microsoft/azure-cli
   ```

CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.

> [!NOTE]
> Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a>Uppdatera Docker-avbildning

Om du vill uppdatera med Docker måste du hämta den nya avbildningen och återskapa alla befintliga behållare. Därför bör du försöka undvika att använda en behållare som är värd för CLI som ett datalager.

Uppdatera den lokala avbildningen med `docker pull`.

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a>Avinstallera Docker-avbildning

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

När du har stoppat behållarna som körs i CLI-avbildningen kan du ta du bort dem.

```bash
docker rmi microsoft/azure-cli
```
