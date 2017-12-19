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
# <a name="install-azure-cli-20"></a><span data-ttu-id="1efe4-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="1efe4-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="1efe4-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="1efe4-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="1efe4-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="1efe4-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="1efe4-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="1efe4-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="1efe4-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="1efe4-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1efe4-109">Om du använder ASM-modellen (Azure Service Management) [ installerar du Azure CLI 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="1efe4-109">If you are using the Azure Service Management (ASM) model, [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="1efe4-110"><a name="macOS"/>Installera i Mac OS</span><span class="sxs-lookup"><span data-stu-id="1efe4-110"><a name="macOS"/>Install on macOS</span></span>

<span data-ttu-id="1efe4-111">I macOS kan du installera antingen med [Homebrew](https://brew.sh/) eller manuellt.</span><span class="sxs-lookup"><span data-stu-id="1efe4-111">On macOS, you are able to install either with [Homebrew](https://brew.sh/) or manually.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="1efe4-112">Installera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="1efe4-112">Install with Homebrew</span></span>

1. <span data-ttu-id="1efe4-113">Om du inte redan har Homebrew installerar du det genom att följa [anvisningarna för att installera Homebrew](https://docs.brew.sh/Installation.html).</span><span class="sxs-lookup"><span data-stu-id="1efe4-113">If you don't have it already, install Homebrew by following the [Homebrew installation instructions](https://docs.brew.sh/Installation.html).</span></span>

2. <span data-ttu-id="1efe4-114">Om du tidigare har installerat CLI manuellt följer du anvisningarna för [manuell avinstallation](#UninstallManually).</span><span class="sxs-lookup"><span data-stu-id="1efe4-114">If you have previously installed the CLI manually, follow the [manual uninstall](#UninstallManually) instructions.</span></span>

3. <span data-ttu-id="1efe4-115">Uppdatera din lokala Homebrew-lagringsplats.</span><span class="sxs-lookup"><span data-stu-id="1efe4-115">Update your local Homebrew repositories.</span></span>

   ```bash
   brew update
   ```

4. <span data-ttu-id="1efe4-116">Installera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="1efe4-116">Install the `azure-cli` package.</span></span>

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> <span data-ttu-id="1efe4-117">Om du tidigare har installerat Azure CLI 1.0 med Homebrew kan du istället för att installera paketet hämta CLI 2.0 via den vanliga Homebrew-uppgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-117">If you previously installed the Azure CLI 1.0 with Homebrew, instead of installing the package you can get CLI 2.0 through the regular Homebrew upgrade process.</span></span>
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a><span data-ttu-id="1efe4-118">Installera manuellt</span><span class="sxs-lookup"><span data-stu-id="1efe4-118">Install manually</span></span>

1. <span data-ttu-id="1efe4-119">Installera Azure CLI 2.0 med `curl`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-119">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="1efe4-120">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="1efe4-120">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

3. <span data-ttu-id="1efe4-121">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-121">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="1efe4-122">Installera i Windows</span><span class="sxs-lookup"><span data-stu-id="1efe4-122">Install on Windows</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="1efe4-123">Installera med MSI för kommandoraden i Windows</span><span class="sxs-lookup"><span data-stu-id="1efe4-123">Install with MSI for the Windows command-line</span></span>

<span data-ttu-id="1efe4-124">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [Azure CLI-installationsprogrammet (MSI)](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="1efe4-124">To install the CLI on Windows and use it in the Windows command-line, download and run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="1efe4-125">Installera med apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="1efe4-125">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="1efe4-126">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="1efe4-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="1efe4-127">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="1efe4-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="1efe4-128">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="1efe4-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="1efe4-129">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="1efe4-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="1efe4-130">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-apt-package-manager"></a><span data-ttu-id="1efe4-131">Installera med apt-pakethanteraren</span><span class="sxs-lookup"><span data-stu-id="1efe4-131">Install with apt package manager</span></span>

<span data-ttu-id="1efe4-132">För distributioner som använder `apt`-pakethanteraren, t.ex. Ubuntu eller Debian, kan du installera Azure CLI 2.0 via `apt-get`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-132">For distributions using the `apt` package manager such as Ubuntu or Debian, you can install Azure CLI 2.0 via `apt-get`.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. <span data-ttu-id="1efe4-133">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="1efe4-133">Modify your sources list:</span></span>

   - <span data-ttu-id="1efe4-134">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="1efe4-134">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="1efe4-135">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="1efe4-135">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="1efe4-136">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="1efe4-136">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="1efe4-137">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-137">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-yum-package-manager"></a><span data-ttu-id="1efe4-138">Installera med yum-pakethanteraren</span><span class="sxs-lookup"><span data-stu-id="1efe4-138">Install with yum package manager</span></span>

<span data-ttu-id="1efe4-139">För distributioner som använder `yum`-pakethanteraren, t.ex. Red Hat Enterprise Linux (RHEL), Fedora eller CentOS, kan du installera Azure CLI 2.0 via `yum`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-139">For distributions which use the `yum` package manager such as Red Hat Enterprise Linux (RHEL), Fedora, or CentOS, you can install Azure CLI 2.0 via `yum`.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. <span data-ttu-id="1efe4-140">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="1efe4-140">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="1efe4-141">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="1efe4-141">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="1efe4-142">Uppdatera `yum`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="1efe4-142">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="1efe4-143">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-143">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-zypper-package-manager"></a><span data-ttu-id="1efe4-144">Installera med zypper-pakethanteraren</span><span class="sxs-lookup"><span data-stu-id="1efe4-144">Install with zypper package manager</span></span>

<span data-ttu-id="1efe4-145">För distributioner som använder `zypper`-pakethanteraren, t.ex. OpenSUSE eller SLE, kan du installera Azure CLI 2.0 via `zypper`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-145">For distributions which use the `zypper` package manager such as OpenSUSE or SLE, you can install Azure CLI 2.0 via `zypper`.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. <span data-ttu-id="1efe4-146">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="1efe4-146">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="1efe4-147">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="1efe4-147">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="1efe4-148">Uppdatera `zypper`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="1efe4-148">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="1efe4-149">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-149">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="1efe4-150">Installera med Docker</span><span class="sxs-lookup"><span data-stu-id="1efe4-150">Install with Docker</span></span>

<span data-ttu-id="1efe4-151">Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="1efe4-151">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="1efe4-152">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-152">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="1efe4-153">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="1efe4-153">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="1efe4-154">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-154">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="1efe4-155">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-155">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><span data-ttu-id="1efe4-156"><a name="Linux"/>Installera på Linux utan en pakethanterare</span><span class="sxs-lookup"><span data-stu-id="1efe4-156"><a name="Linux"/>Install on Linux without a package manager</span></span>

<span data-ttu-id="1efe4-157">Om det är möjligt rekommenderar vi att du installerar CLI med en pakethanterare.</span><span class="sxs-lookup"><span data-stu-id="1efe4-157">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="1efe4-158">Om du inte vill lägga till Microsofts lagringsplatser eller arbetar med en distribution som saknar tillhandahållet paket kan du installera CLI manuellt.</span><span class="sxs-lookup"><span data-stu-id="1efe4-158">If you do not want to add Microsoft's repositories, or are working with a distribution which does not have a provided package, you can manually install the CLI.</span></span>

1. <span data-ttu-id="1efe4-159">Kontrollera att din Linux-distribution uppfyller alla förhandskrav.</span><span class="sxs-lookup"><span data-stu-id="1efe4-159">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="1efe4-160">Om distributionen inte finns med i listan ovan måste du installera [Python 2.7 eller senare](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/) och [OpenSSL 1.0.2](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="1efe4-160">If your distribution is not listed above, you will need to install [Python 2.7 or later](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL 1.0.2](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="1efe4-161">Installera CLI med `curl`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-161">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="1efe4-162">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="1efe4-162">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="1efe4-163">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-163">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1efe4-164">Felsökning</span><span class="sxs-lookup"><span data-stu-id="1efe4-164">Troubleshooting</span></span>

<span data-ttu-id="1efe4-165">Om det uppstår problem under CLI-installationen läser du det här avsnittet för att se om ditt problem tas upp.</span><span class="sxs-lookup"><span data-stu-id="1efe4-165">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="1efe4-166">Om du inte hittar ditt problem här [öppnar du ett Github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="1efe4-166">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="1efe4-167">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="1efe4-167">curl "Object Moved" error</span></span>

<span data-ttu-id="1efe4-168">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="1efe4-168">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="1efe4-169">Det gick inte att hitta kommandot `az`</span><span class="sxs-lookup"><span data-stu-id="1efe4-169">`az` command not found</span></span>

<span data-ttu-id="1efe4-170">Du kan behöva rensa cacheminnet för gränssnittets kommando-hash.</span><span class="sxs-lookup"><span data-stu-id="1efe4-170">You may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="1efe4-171">Kör</span><span class="sxs-lookup"><span data-stu-id="1efe4-171">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="1efe4-172">och se om problemet är löst.</span><span class="sxs-lookup"><span data-stu-id="1efe4-172">and see if the problem is resolved.</span></span> <span data-ttu-id="1efe4-173">Kommandot kanske inte finns i `$PATH`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-173">The command may also not be in your `$PATH`.</span></span> <span data-ttu-id="1efe4-174">Se till att `<install path>/bin` visas i `$PATH`, och starta om gränssnittet vid behov.</span><span class="sxs-lookup"><span data-stu-id="1efe4-174">Make sure that `<install path>/bin` appears in your `$PATH`, and restart your shell if necessary.</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="1efe4-175">Avinstallera CLI 1.x-versioner</span><span class="sxs-lookup"><span data-stu-id="1efe4-175">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="1efe4-176">Om du har en tidigare CLI 1.x-version på datorn kan du avinstallera den baserat på den typ av installation du använde för att installera versionen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-176">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="1efe4-177">Avinstallera med npm</span><span class="sxs-lookup"><span data-stu-id="1efe4-177">Uninstall with npm</span></span>

<span data-ttu-id="1efe4-178">Ta bort den äldre CLI-versionen med `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-178">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="1efe4-179">Avinstallera med distributable</span><span class="sxs-lookup"><span data-stu-id="1efe4-179">Uninstall with distributable</span></span>

<span data-ttu-id="1efe4-180">Om du installerade via [Azure CLI-installationsprogrammet (MSI)](http://aka.ms/webpi-azure-cli) eller ett [macOS-paket](http://aka.ms/mac-azure-cli) använder du samma verktyg för att ta bort installationen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-180">If you installed via the [Azure CLI Installer (MSI)](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="1efe4-181">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="1efe4-181">Uninstall with Docker</span></span>

<span data-ttu-id="1efe4-182">Om du installerade en Docker-avbildning för att använda den tidigare CLI-versionen tar du bort avbildningen och eventuella associerade behållare.</span><span class="sxs-lookup"><span data-stu-id="1efe4-182">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="1efe4-183">Du kan sedan återskapa behållarna när du har installerat den nya Docker-avbildningen genom att följa installationsanvisningarna.</span><span class="sxs-lookup"><span data-stu-id="1efe4-183">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="1efe4-184">Uppdatera CLI</span><span class="sxs-lookup"><span data-stu-id="1efe4-184">Update the CLI</span></span>

<span data-ttu-id="1efe4-185">Uppdatera Azure CLI genom att använda samma metod som du använde för att installera det.</span><span class="sxs-lookup"><span data-stu-id="1efe4-185">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="1efe4-186">Uppdatera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="1efe4-186">Update with Homebrew</span></span>

1. <span data-ttu-id="1efe4-187">Om du tidigare har installerat manuellt följer du anvisningarna för att [installera med Homebrew](#macOS).</span><span class="sxs-lookup"><span data-stu-id="1efe4-187">If you previously installed manually, follow the [install with Homebrew](#macOS) instructions.</span></span>

2. <span data-ttu-id="1efe4-188">Uppdatera informationen om din lokala Homebrew-lagringsplats.</span><span class="sxs-lookup"><span data-stu-id="1efe4-188">Update your local Homebrew repository information.</span></span>

   ```bash
   brew update
   ```

3. <span data-ttu-id="1efe4-189">Uppgradera dina installerade paket.</span><span class="sxs-lookup"><span data-stu-id="1efe4-189">Upgrade your installed packages.</span></span>

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a><span data-ttu-id="1efe4-190">Uppdatera med MSI</span><span class="sxs-lookup"><span data-stu-id="1efe4-190">Update with MSI</span></span>

<span data-ttu-id="1efe4-191">Kör [Azure CLI-installationsprogrammet (MSI)](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-191">Run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt"></a><span data-ttu-id="1efe4-192">Uppdatera med apt</span><span class="sxs-lookup"><span data-stu-id="1efe4-192">Update with apt</span></span>

<span data-ttu-id="1efe4-193">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="1efe4-193">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="1efe4-194">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="1efe4-194">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="1efe4-195">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-195">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-yum"></a><span data-ttu-id="1efe4-196">Uppdatera med yum</span><span class="sxs-lookup"><span data-stu-id="1efe4-196">Update with yum</span></span>

<span data-ttu-id="1efe4-197">Uppdatera Azure CLI med kommandot `yum update`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-197">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a><span data-ttu-id="1efe4-198">Uppdatera med zypper</span><span class="sxs-lookup"><span data-stu-id="1efe4-198">Update with zypper</span></span>

<span data-ttu-id="1efe4-199">Du kan uppdatera paketet med kommandot `zypper update`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-199">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

### <a name="update-with-docker"></a><span data-ttu-id="1efe4-200">Uppdatera med Docker</span><span class="sxs-lookup"><span data-stu-id="1efe4-200">Update with Docker</span></span>

1. <span data-ttu-id="1efe4-201">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-201">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="1efe4-202">Hämta behållarna som för närvarande använder CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-202">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="1efe4-203">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="1efe4-203">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="1efe4-204">Stoppa och återskapa behållarna.</span><span class="sxs-lookup"><span data-stu-id="1efe4-204">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="1efe4-205">Uppdatera manuellt</span><span class="sxs-lookup"><span data-stu-id="1efe4-205">Update manually</span></span>

<span data-ttu-id="1efe4-206">Uppdatera genom att följa anvisningarna för manuell installation för [Mac OS](#macOS) eller [Linux](#Linux).</span><span class="sxs-lookup"><span data-stu-id="1efe4-206">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="1efe4-207">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="1efe4-207">Uninstall</span></span>

<span data-ttu-id="1efe4-208">Vi tycker det är tråkigt om du väljer att avinstallera CLI.</span><span class="sxs-lookup"><span data-stu-id="1efe4-208">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="1efe4-209">Du bör avinstallera med samma metod som du använde för att installera CLI.</span><span class="sxs-lookup"><span data-stu-id="1efe4-209">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="1efe4-210">Avinstallera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="1efe4-210">Uninstall with Homebrew</span></span>

<span data-ttu-id="1efe4-211">Avinstallera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="1efe4-211">Uninstall the `azure-cli` package.</span></span>

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a><span data-ttu-id="1efe4-212">Avinstallera med MSI</span><span class="sxs-lookup"><span data-stu-id="1efe4-212">Uninstall with MSI</span></span>

<span data-ttu-id="1efe4-213">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen och välj Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="1efe4-213">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt"></a><span data-ttu-id="1efe4-214">Avinstallera med apt</span><span class="sxs-lookup"><span data-stu-id="1efe4-214">Uninstall with apt</span></span>

<span data-ttu-id="1efe4-215">Avinstallera via `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="1efe4-215">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a><span data-ttu-id="1efe4-216">Avinstallera med yum</span><span class="sxs-lookup"><span data-stu-id="1efe4-216">Uninstall with yum</span></span>

1. <span data-ttu-id="1efe4-217">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="1efe4-217">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="1efe4-218">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="1efe4-218">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="1efe4-219">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="1efe4-219">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a><span data-ttu-id="1efe4-220">Avinstallera med zypper</span><span class="sxs-lookup"><span data-stu-id="1efe4-220">Uninstall with zypper</span></span>

1. <span data-ttu-id="1efe4-221">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="1efe4-221">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="1efe4-222">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="1efe4-222">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="1efe4-223">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="1efe4-223">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="1efe4-224">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="1efe4-224">Uninstall with Docker</span></span>

<span data-ttu-id="1efe4-225">Om du installerade en Docker-avbildning måste du ta bort eventuella behållare som kör den, och sedan ta bort den lokala avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-225">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="1efe4-226">Hämta behållarna som kör azure-cli-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-226">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="1efe4-227">Ta bort alla behållare som kör CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-227">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="1efe4-228">Ta bort den lokalt installerade CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="1efe4-228">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="1efe4-229">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="1efe4-229">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><span data-ttu-id="1efe4-230"><a name="UninstallManually"/>Avinstallera manuellt</span><span class="sxs-lookup"><span data-stu-id="1efe4-230"><a name="UninstallManually"/>Uninstall manually</span></span>

<span data-ttu-id="1efe4-231">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="1efe4-231">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="1efe4-232">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="1efe4-232">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="1efe4-233">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-233">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

3. <span data-ttu-id="1efe4-234">Om gränssnittet använder kommandocache läser du in det på nytt.</span><span class="sxs-lookup"><span data-stu-id="1efe4-234">If your shell uses a command cache, reload it.</span></span>

   ```bash
   hash -r
   ```

> [!Note]
> <span data-ttu-id="1efe4-235">Standardplatsen för installation är `/Users/<username>` för macOS och `/home/<username>` för Linux.</span><span class="sxs-lookup"><span data-stu-id="1efe4-235">The default install location is `/Users/<username>` for macOS and `/home/<username>` for Linux.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="1efe4-236">Rapportera problem med CLI och lämna feedback</span><span class="sxs-lookup"><span data-stu-id="1efe4-236">Report CLI issues and feedback</span></span>

<span data-ttu-id="1efe4-237">Om du stöter på buggar med verktyget kan du rapportera problemet i avsnittet [Problem](https://github.com/Azure/azure-cli/issues) i vår GitHub-databas.</span><span class="sxs-lookup"><span data-stu-id="1efe4-237">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="1efe4-238">Om du vill skicka feedback från kommandoraden använder du kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="1efe4-238">To provide feedback from the command line, use the `az feedback` command.</span></span>
