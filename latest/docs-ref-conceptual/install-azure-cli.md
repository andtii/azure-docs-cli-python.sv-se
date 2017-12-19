---
title: Installera Azure CLI 2.0
description: "Referensdokument för installation av Azure CLI 2.0"
keywords: Azure CLI,Install Azure CLI,Azure Python CLI,Azure CLI Reference
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 5a667ad8720100b45ff714601225535ef442545c
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20"></a>Installera Azure CLI 2.0

Installera den nya versionen av Azure CLI idag!
Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.
Den kan användas i Mac OS, Linux och Windows.
Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).

> [!NOTE]
> Om du använder ASM-modellen (Azure Service Management) [ installerar du Azure CLI 1.0](/azure/cli-install-nodejs).

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>Installera i Mac OS

I macOS kan du installera antingen med [Homebrew](https://brew.sh/) eller manuellt.

### <a name="install-with-homebrew"></a>Installera med Homebrew

1. Om du inte redan har Homebrew installerar du det genom att följa [anvisningarna för att installera Homebrew](https://docs.brew.sh/Installation.html).

2. Om du tidigare har installerat CLI manuellt följer du anvisningarna för [manuell avinstallation](#UninstallManually).

3. Uppdatera din lokala Homebrew-lagringsplats.

   ```bash
   brew update
   ```

4. Installera `azure-cli`-paketet.

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> Om du tidigare har installerat Azure CLI 1.0 med Homebrew kan du istället för att installera paketet hämta CLI 2.0 via den vanliga Homebrew-uppgraderingsprocessen.
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a>Installera manuellt

1. Installera Azure CLI 2.0 med `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.

   ```bash
   exec -l $SHELL
   ```

3. Kör CLI från kommandotolken med kommandot `az`.

## <a name="install-on-windows"></a>Installera i Windows

### <a name="install-with-msi-for-the-windows-command-line"></a>Installera med MSI för kommandoraden i Windows

Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [Azure CLI-installationsprogrammet (MSI)](https://aka.ms/InstallAzureCliWindows).

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a>Installera med apt-get för Bash i Ubuntu för Windows

1. Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).

2. Öppna Bash-gränssnittet.

3. Ändra listan med källor.

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. Kör följande sudo-kommandon:

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  Kör CLI från kommandotolken med kommandot `az`.

## <a name="install-with-apt-package-manager"></a>Installera med apt-pakethanteraren

För distributioner som använder `apt`-pakethanteraren, t.ex. Ubuntu eller Debian, kan du installera Azure CLI 2.0 via `apt-get`.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. Ändra listan med källor:

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
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  Kör CLI från kommandotolken med kommandot `az`.

## <a name="install-with-yum-package-manager"></a>Installera med yum-pakethanteraren

För distributioner som använder `yum`-pakethanteraren, t.ex. Red Hat Enterprise Linux (RHEL), Fedora eller CentOS, kan du installera Azure CLI 2.0 via `yum`.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. Importera nyckeln för Microsoft-lagringsplatsen:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Skapa information om lokal `azure-cli`-lagringsplats:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. Uppdatera `yum`-paketindexet och installera:

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. Kör CLI från kommandotolken med kommandot `az`.

## <a name="install-with-zypper-package-manager"></a>Installera med zypper-pakethanteraren

För distributioner som använder `zypper`-pakethanteraren, t.ex. OpenSUSE eller SLE, kan du installera Azure CLI 2.0 via `zypper`.

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. Importera nyckeln för Microsoft-lagringsplatsen:

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. Skapa information om lokal `azure-cli`-lagringsplats:

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. Uppdatera `zypper`-paketindexet och installera:

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. Kör CLI från kommandotolken med kommandot `az`.

## <a name="install-with-docker"></a>Installera med Docker

Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.

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

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><a name="Linux"/>Installera på Linux utan en pakethanterare

Om det är möjligt rekommenderar vi att du installerar CLI med en pakethanterare. Om du inte vill lägga till Microsofts lagringsplatser eller arbetar med en distribution som saknar tillhandahållet paket kan du installera CLI manuellt.

1. Kontrollera att din Linux-distribution uppfyller alla förhandskrav.

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

Om distributionen inte finns med i listan ovan måste du installera [Python 2.7 eller senare](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/) och [OpenSSL 1.0.2](https://www.openssl.org/source/).

2. Installera CLI med `curl`.

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.

   ```bash
   exec -l $SHELL
   ```

4. Kör CLI från kommandotolken med kommandot `az`.

## <a name="troubleshooting"></a>Felsökning

Om det uppstår problem under CLI-installationen läser du det här avsnittet för att se om ditt problem tas upp. Om du inte hittar ditt problem här [öppnar du ett Github-supportärende](https://github.com/Azure/azure-cli/issues).

### <a name="curl-object-moved-error"></a>Fel: curl "Object Moved"

Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>Det gick inte att hitta kommandot `az`

Du kan behöva rensa cacheminnet för gränssnittets kommando-hash. Kör

```bash
hash -r
```

och se om problemet är löst. Kommandot kanske inte finns i `$PATH`. Se till att `<install path>/bin` visas i `$PATH`, och starta om gränssnittet vid behov.

## <a name="uninstall-cli-1x-versions"></a>Avinstallera CLI 1.x-versioner

Om du har en tidigare CLI 1.x-version på datorn kan du avinstallera den baserat på den typ av installation du använde för att installera versionen.

### <a name="uninstall-with-npm"></a>Avinstallera med npm

Ta bort den äldre CLI-versionen med `npm uninstall`.

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a>Avinstallera med distributable

Om du installerade via [Azure CLI-installationsprogrammet (MSI)](http://aka.ms/webpi-azure-cli) eller ett [macOS-paket](http://aka.ms/mac-azure-cli) använder du samma verktyg för att ta bort installationen.

### <a name="uninstall-with-docker"></a>Avinstallera med Docker

Om du installerade en Docker-avbildning för att använda den tidigare CLI-versionen tar du bort avbildningen och eventuella associerade behållare. Du kan sedan återskapa behållarna när du har installerat den nya Docker-avbildningen genom att följa installationsanvisningarna.

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>Uppdatera CLI

Uppdatera Azure CLI genom att använda samma metod som du använde för att installera det.

### <a name="update-with-homebrew"></a>Uppdatera med Homebrew

1. Om du tidigare har installerat manuellt följer du anvisningarna för att [installera med Homebrew](#macOS).

2. Uppdatera informationen om din lokala Homebrew-lagringsplats.

   ```bash
   brew update
   ```

3. Uppgradera dina installerade paket.

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a>Uppdatera med MSI

Kör [Azure CLI-installationsprogrammet (MSI)](https://aka.ms/InstallAzureCliWindows) igen.

### <a name="update-with-apt"></a>Uppdatera med apt

Använd `apt-get upgrade` för att uppdatera CLI-paketet.

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.
> Om du bara vill uppgradera CLI använder du `apt-get install`.
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-yum"></a>Uppdatera med yum

Uppdatera Azure CLI med kommandot `yum update`.

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a>Uppdatera med zypper

Du kan uppdatera paketet med kommandot `zypper update`.

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

### <a name="update-with-docker"></a>Uppdatera med Docker

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

### <a name="update-manually"></a>Uppdatera manuellt

Uppdatera genom att följa anvisningarna för manuell installation för [Mac OS](#macOS) eller [Linux](#Linux).

## <a name="uninstall"></a>Avinstallera

Vi tycker det är tråkigt om du väljer att avinstallera CLI. Du bör avinstallera med samma metod som du använde för att installera CLI.

### <a name="uninstall-with-homebrew"></a>Avinstallera med Homebrew

Avinstallera `azure-cli`-paketet.

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a>Avinstallera med MSI

Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen och välj Avinstallera.

### <a name="uninstall-with-apt"></a>Avinstallera med apt

Avinstallera via `apt-get remove`:

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a>Avinstallera med yum

1. Ta bort paketet från datorn.

   ```bash
   sudo yum remove azure-cli
   ```

2. Ta bort lagringsinformationen om du inte tänker installera om CLI.

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a>Avinstallera med zypper

1. Ta bort paketet från datorn.

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. Ta bort lagringsinformationen om du inte tänker installera om CLI.

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-docker"></a>Avinstallera med Docker

Om du installerade en Docker-avbildning måste du ta bort eventuella behållare som kör den, och sedan ta bort den lokala avbildningen.

1. Hämta behållarna som kör azure-cli-avbildningen.

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. Ta bort alla behållare som kör CLI-avbildningen.

   ```bash
   docker rm 34a868beb2ab
   ```

3. Ta bort den lokalt installerade CLI-avbildningen.

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><a name="UninstallManually"/>Avinstallera manuellt

Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.

1. Ta bort de installerade filerna.

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.

3. Om gränssnittet använder kommandocache läser du in det på nytt.

   ```bash
   hash -r
   ```

> [!Note]
> Standardplatsen för installation är `/Users/<username>` för macOS och `/home/<username>` för Linux.

## <a name="report-cli-issues-and-feedback"></a>Rapportera problem med CLI och lämna feedback

Om du stöter på buggar med verktyget kan du rapportera problemet i avsnittet [Problem](https://github.com/Azure/azure-cli/issues) i vår GitHub-databas.
Om du vill skicka feedback från kommandoraden använder du kommandot `az feedback`.
