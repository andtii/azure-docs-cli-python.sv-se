---
title: Installera Azure CLI med Docker
description: "Så här installerar du en dockerbehållare med Azure CLI 2.0"
keywords: Azure CLI,Install Azure CLI,azure docker,azure docker image,
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 76ecf2c9cd0e6e694a31ac160112d1348863f118
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-docker"></a>Installera Azure CLI 2.0 med Docker

Du kan använda Docker för att installera en fristående Linux-behållare med Azure CLI 2.0 redan installerat. Det här gör att du snabbt kan komma igång med en miljö där du kan prova CLI för att avgöra om det är rätt för dig. Du kan även använda det här exemplet som en basavbildning.

## <a name="install-with-docker"></a>Installera med Docker

Installera CLI med `docker run`.

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.

CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.

> [!NOTE]
> Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

### <a name="update-with-docker"></a>Uppdatera med Docker

Om du vill uppdatera med Docker måste du hämta den nya avbildningen och återskapa alla befintliga behållare. Därför bör du försöka undvika att använda en behållare som är värd för CLI som ett datalager.

1. Uppdatera den lokala avbildningen med `docker pull`.

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. Hämta behållarna som för närvarande använder CLI-avbildningen.

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

  > [!NOTE]
  > Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.

3. Stoppa och återskapa behållarna.

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="uninstall-with-docker"></a>Avinstallera med Docker

Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI. Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar. Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt. Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).

Om du vill avinstallera CLI Docker-avbildningen fullständigt måste du ta bort eventuella behållare som kör den och sedan ta bort den lokala avbildningen.

1. Hämta behållarna som kör azure-cli-avbildningen.

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```
  > [!NOTE]
  > Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.

2. Ta bort alla behållare som kör CLI-avbildningen.

   ```bash
   docker rm 34a868beb2ab
   ```

3. Ta bort den lokalt installerade CLI-avbildningen.

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

