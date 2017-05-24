---
title: Installera Azure CLI 2.0
description: "Referensdokument för Azure CLI 2.0"
keywords: Azure CLI 2.0, Azure CLI 2.0-referens, Installera Azure CLI 2.0, Azure Python CLI, Avinstallera Azure CLI 2.0
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 7065ed5270ef9bfc70beea81d0bc442a7b4df38c
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a>Installera Azure CLI 2.0

Installera den nya versionen av Azure CLI idag!
Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.
Den kan användas i Mac OS, Linux och Windows.
Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).

> [!NOTE]
> Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure 1.0](/azure/cli-install-nodejs).

## <a name="macos"></a>macOS

1. Installera Azure CLI 2.0 med ett `curl`-kommando.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.

   ```bash
   exec -l $SHELL
   ```
   
3. Kör Azure CLI 2.0 från kommandotolken med `az`-kommandot.

> [!Note]
> När du installerar med InstallAzureCli stöds inte `az component update`.
> Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.
> 
> Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.

## <a name="windows"></a>Windows

Du kan installera CLI med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med apt-get i Bash i Ubuntu för Windows.

### <a name="msi-for-the-windows-command-line"></a>MSI för Windows-kommandoraden 

Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [msi](https://aka.ms/InstallAzureCliWindows).

> [!NOTE]
> `az component` stöds inte om du installerar med msi.
> Om du vill uppdatera till den senaste versionen av CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen.
> 
> Om du vill avinstallera CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen och väljer Avinstallera.

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a>apt-get för Bash i Ubuntu för Windows

1. Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).

2. Öppna Bash-gränssnittet.

3. Ändra listan med källor.

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. Kör följande sudo-kommandon:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> När du installerar med apt-get stöds inte `az component`.
> Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.
> 
> Kör `sudo apt-get remove azure-cli` för att avinstallera.

## <a name="linux"></a>Linux

1. På Linux kan du behöva installera specifika [förutsättningar](#linux-prerequisites).

2. Installera Azure CLI 2.0 med ett `curl`-kommando.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.

   ```bash
   exec -l $SHELL
   ```

4. Kör Azure CLI 2.0 från kommandotolken med `az`-kommandot.

> [!Note]
> När du installerar med InstallAzureCli stöds inte `az component update`.
> Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.
> 
> Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.

## <a name="docker"></a>Docker

Vi underhåller en Docker-avbildning som är förkonfigurerad med Azure CLI.

Installera Azure CLI med `docker run`.

```bash
docker run azuresdk/azure-cli-python:<version>
```

Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.

> [!NOTE]
> Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> Docker-avbildningen stöder inte [`component`-funktionen](/cli/azure/component).
> Använd `docker run` för att installera den senaste avbildningen eller en specifik avbildning som du vill ha för att uppdatera Azure CLI 2.0.

## <a name="apt-get"></a>apt-get

Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.

1. Ändra listan med källor.

   - 32-bitarssystem

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64-bitarssystem

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. Kör följande sudo-kommandon:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> När du installerar med apt-get stöds inte `az component`.
> Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.
> 
> Kör `sudo apt-get remove azure-cli` för att avinstallera.

## <a name="linux-prerequisites"></a>Linux-förutsättningar

1. Om du inte har [Python](https://www.python.org/downloads) kan du installera det.

2. Installera de nödvändiga förutsättningarna beroende på vilken Linux-distribution du har.

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a>Felsökning

### <a name="errors-with-curl-redirection"></a>Fel vid omdirigering av curl

Om du får ett fel från `curl`-kommandot angående `-L`-parametern eller ett fel som hänvisar till "Object Moved" så kan du försöka använda en fullständig URL i stället för URL:en aka.ms:

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a>Avinstallera

Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.

1. Ta bort de installerade filerna.

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.

> [!Note]
> Standardplatsen för installation är `/Users/<username>`.

Om du använde apt-get, Docker eller msi för att installera CLI använder du samma verktyg för att avinstallera det.

## <a name="reporting-issues-and-feedback"></a>Rapportera problem och feedback

Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-cli/issues)-delen av vårt GitHub-repo.
Om du vill ge feedback från kommandoraden kan du prova kommandot `az feedback`.
