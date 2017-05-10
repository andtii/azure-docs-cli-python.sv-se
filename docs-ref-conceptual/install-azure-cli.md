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
ms.openlocfilehash: b7c0b7c50794333b28c034de9b41f1e506053e25
ms.sourcegitcommit: 663d4188ccc4be425d3d551fe32613fafd05a764
ms.translationtype: HT
ms.contentlocale: sv-SE
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

Azure CLI 2.0 stöder Bash-kommandosyntax, vilket innebär att Bash på Ubuntu i Windows är ett bra sätt att använda CLI.
Om du inte använder Bash kan du installera och använda CLI i Windows-kommandotolken.

### <a name="bash-on-ubuntu-on-windows"></a>Bash på Ubuntu i Windows

1. Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).

2. Öppna Bash-gränssnittet.

3. Om du inte har Python installerar du det.

   ```bash
   sudo apt-get install python3
   ```

   > [!NOTE]
   > Om du vill se om du har Python installerat kör du `python --version`.

4. Ändra listan med källor.

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

5. Kör följande sudo-kommandon:

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

### <a name="windows-command-line"></a>Windows-kommandorad 

1. Gå till Python-webbplatsen och [ladda ned Python](https://www.python.org/downloads/) för Windows.
   Se till att installera Pip-komponenten när du installerar Python.
   När installationen är klar kan du lägga till Python i miljövariabeln PATH (installationsprogrammet uppmanar dig).

2. Kontrollera Python-installationen från kommandotolken.

   ```bash
   python --version
   ```

3. Installera Azure CLI 2.0 med `pip`.

   ```bash
   pip install --user azure-cli
   ```

4. Lägg till mappen som innehåller az.bat till sökvägen.
   CLI `az.bat` kan installeras i `%USERPROFILE%\AppData\Roaming\Python\Scripts` eller `%USERPROFILE%\AppData\Roaming\Python\PythonXY\Scripts` där `XY` är Python-versionen (till exempel `%USERPROFILE%\AppData\Roaming\Python\Python27\Scripts`).
   Lägg till mappen som innehåller `az.bat` till sökvägen.
   
4. Kör Azure CLI 2.0 från kommandotolken med `az`-kommandot.

> [!NOTE]
> Om du redan har installerat Azure CLI 2.0 och du vill se om du har den senaste versionen kan du använda `az --version` för att se vilken version du har.
> Jämför med den senaste versionen som är tillgänglig på [https://pypi.python.org/pypi/azure-cli](https://pypi.python.org/pypi/azure-cli).
> 
> Kör `az component update` för att uppdatera till den senaste versionen av CLI.
> 
> Kör `pip uninstall azure-cli` för att avinstallera CLI.

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
-------------------------------

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


### <a name="errors-on-install-with-cffi-or-cryptography"></a>Fel vid installation med `cffi` eller kryptografi

Om fel uppstår vid installation på OS X bör du uppgradera `pip`.

```bash
pip install --upgrade --force-reinstall pip
```

Om fel uppstår vid installation på **Debian** eller **Ubuntu**, som dessa exempel, kan du installera `libssl-dev` och `libffi-dev`.

```bash
sudo apt-get update
sudo apt-get install -y libssl-dev libffi-dev
```

Installera även Python Dev för din version av Python.

Python 2:

```bash
sudo apt-get install -y python-dev
```

Python 3:

```bash
sudo apt-get install -y python3-dev
```

Ubuntu 15 kanske även kräver `build-essential`:

```bash
sudo apt-get install -y build-essential
```

### <a name="example-errors"></a>Exempelfel

```
Downloading cffi-1.5.2.tar.gz (388kB)
    100% |################################| 389kB 3.9MB/s
    Complete output from command python setup.py egg_info:

        No working compiler found, or bogus compiler options
        passed to the compiler from Python's distutils module.
        See the error messages above.
        (If they are about -mno-fused-madd and you are on OS/X 10.8,
        see http://stackoverflow.com/questions/22313407/ .)

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-77i2fido/cffi/
```

```
#include <openssl/e_os2.h>
                            ^
compilation terminated.
error: command 'x86_64-linux-gnu-gcc' failed with exit status 1

Failed building wheel for cryptography
```

Se fråga om Stack Overflow – [Det gick inte att installera kryptografipaketet för Python med PIP och setup.py](http://stackoverflow.com/questions/22073516/failed-to-install-python-cryptography-package-with-pip-and-setup-py)

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

Om du använde pip, apt-get eller Docker för att installera CLI så kan du använda samma verktyg för att avinstallera.

## <a name="reporting-issues-and-feedback"></a>Rapportera problem och feedback

Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-cli/issues)-delen av vårt GitHub-repo.
Om du vill ge feedback från kommandoraden kan du prova kommandot `az feedback`.
