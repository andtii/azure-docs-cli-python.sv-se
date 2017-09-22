---
title: Installera Azure CLI 2.0
description: "Referensdokument för installation av Azure CLI 2.0"
keywords: Azure CLI,Install Azure CLI,Azure Python CLI,Azure CLI Reference
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 08/17/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 580438bfc66f3ed0b4dad504258eab453b1b9183
ms.sourcegitcommit: c1df7794ad42adb8640b51b630e4275f4a791ac2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="f7185-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f7185-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="f7185-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="f7185-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="f7185-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="f7185-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="f7185-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="f7185-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="f7185-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="f7185-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f7185-109">Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure CLI 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="f7185-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="f7185-110"><a name="macOS"/>Installera i Mac OS</span><span class="sxs-lookup"><span data-stu-id="f7185-110"><a name="macOS"/>Install on macOS</span></span>

<span data-ttu-id="f7185-111">I macOS kan du installera antingen med [Homebrew](https://brew.sh/) eller manuellt.</span><span class="sxs-lookup"><span data-stu-id="f7185-111">On macOS, you are able to install either with [Homebrew](https://brew.sh/) or manually.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="f7185-112">Installera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="f7185-112">Install with Homebrew</span></span>

1. <span data-ttu-id="f7185-113">Om du inte redan har Homebrew installerar du det genom att följa [anvisningarna för att installera Homebrew](https://docs.brew.sh/Installation.html).</span><span class="sxs-lookup"><span data-stu-id="f7185-113">If you don't have it already, install Homebrew by following the [Homebrew installation instructions](https://docs.brew.sh/Installation.html).</span></span>

2. <span data-ttu-id="f7185-114">Uppdatera din lokala Homebrew-lagringsplats.</span><span class="sxs-lookup"><span data-stu-id="f7185-114">Update your local Homebrew repositories.</span></span>

   ```bash
   brew update
   ```

3. <span data-ttu-id="f7185-115">Installera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="f7185-115">Install the `azure-cli` package.</span></span>

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> <span data-ttu-id="f7185-116">Om du tidigare har installerat Azure CLI 1.0 med Homebrew kan du istället för att installera paketet hämta CLI 2.0 via den vanliga Homebrew-uppgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f7185-116">If you previously installed the Azure CLI 1.0 with Homebrew, instead of installing the package you can get CLI 2.0 through the regular Homebrew upgrade process.</span></span>
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a><span data-ttu-id="f7185-117">Installera manuellt</span><span class="sxs-lookup"><span data-stu-id="f7185-117">Install manually</span></span>

1. <span data-ttu-id="f7185-118">Installera Azure CLI 2.0 med `curl`.</span><span class="sxs-lookup"><span data-stu-id="f7185-118">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="f7185-119">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="f7185-119">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="f7185-120">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-120">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="f7185-121">Installera i Windows</span><span class="sxs-lookup"><span data-stu-id="f7185-121">Install on Windows</span></span>

<span data-ttu-id="f7185-122">Du kan installera Azure CLI 2.0 med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med `apt-get` i Bash i Ubuntu för Windows.</span><span class="sxs-lookup"><span data-stu-id="f7185-122">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="f7185-123">Installera med MSI för kommandoraden i Windows</span><span class="sxs-lookup"><span data-stu-id="f7185-123">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="f7185-124">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="f7185-124">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="f7185-125">Installera med apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="f7185-125">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="f7185-126">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="f7185-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="f7185-127">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="f7185-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="f7185-128">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="f7185-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="f7185-129">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="f7185-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="f7185-130">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="f7185-131">Installera i Debian/Ubuntu med apt-get</span><span class="sxs-lookup"><span data-stu-id="f7185-131">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="f7185-132">Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.</span><span class="sxs-lookup"><span data-stu-id="f7185-132">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="f7185-133">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="f7185-133">Modify your sources list:</span></span>
 
   - <span data-ttu-id="f7185-134">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="f7185-134">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="f7185-135">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="f7185-135">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="f7185-136">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="f7185-136">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="f7185-137">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-137">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a><span data-ttu-id="f7185-138">Installera på RHEL, Fedora och CentOS med yum</span><span class="sxs-lookup"><span data-stu-id="f7185-138">Install on RHEL, Fedora, and CentOS with yum</span></span>

<span data-ttu-id="f7185-139">För distributioner som bygger på RedHat och innehåller `yum`-pakethanteraren kan du installera Azure CLI 2.0 via `yum`.</span><span class="sxs-lookup"><span data-stu-id="f7185-139">For any distribution which is based off of RedHat and contains the `yum` package manager, you can install Azure CLI 2.0 via `yum`.</span></span>

1. <span data-ttu-id="f7185-140">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="f7185-140">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="f7185-141">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="f7185-141">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="f7185-142">Uppdatera `yum`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="f7185-142">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="f7185-143">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-143">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-opensuse-and-sle-with-zypper"></a><span data-ttu-id="f7185-144">Installera på openSUSE och SLE med zypper</span><span class="sxs-lookup"><span data-stu-id="f7185-144">Install on openSUSE and SLE with zypper</span></span>

1. <span data-ttu-id="f7185-145">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="f7185-145">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="f7185-146">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="f7185-146">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="f7185-147">Uppdatera `zypper`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="f7185-147">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="f7185-148">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-148">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="f7185-149">Installera med Docker</span><span class="sxs-lookup"><span data-stu-id="f7185-149">Install with Docker</span></span>

<span data-ttu-id="f7185-150">Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="f7185-150">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="f7185-151">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="f7185-151">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="f7185-152">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="f7185-152">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="f7185-153">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="f7185-153">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="f7185-154">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="f7185-154">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="f7185-155"><a name="Linux"/>Installera i Linux utan apt-get</span><span class="sxs-lookup"><span data-stu-id="f7185-155"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="f7185-156">Om det är möjligt rekommenderar vi att du installerar CLI med en pakethanterare.</span><span class="sxs-lookup"><span data-stu-id="f7185-156">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="f7185-157">För distributioner som inte har någon pakethanterare kan du installera manuellt.</span><span class="sxs-lookup"><span data-stu-id="f7185-157">For distributions which do not have a package provided for them, you can manually install.</span></span>

1. <span data-ttu-id="f7185-158">Kontrollera att din Linux-distribution uppfyller alla förhandskrav.</span><span class="sxs-lookup"><span data-stu-id="f7185-158">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="f7185-159">Om din distribution inte visas i listan ovan måste du installera [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/) och [OpenSSL](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="f7185-159">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="f7185-160">Installera CLI med `curl`.</span><span class="sxs-lookup"><span data-stu-id="f7185-160">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="f7185-161">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="f7185-161">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="f7185-162">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="f7185-162">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f7185-163">Felsökning</span><span class="sxs-lookup"><span data-stu-id="f7185-163">Troubleshooting</span></span>

<span data-ttu-id="f7185-164">Om det uppstår problem under CLI-installationen läser du det här avsnittet för att se om ditt problem tas upp.</span><span class="sxs-lookup"><span data-stu-id="f7185-164">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="f7185-165">Om du inte hittar ditt problem här [öppnar du ett Github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="f7185-165">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="f7185-166">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="f7185-166">curl "Object Moved" error</span></span>

<span data-ttu-id="f7185-167">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="f7185-167">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="f7185-168">Avinstallera CLI 1.x-versioner</span><span class="sxs-lookup"><span data-stu-id="f7185-168">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="f7185-169">Om du har en tidigare CLI 1.x-version på datorn kan du avinstallera den baserat på den typ av installation du använde för att installera versionen.</span><span class="sxs-lookup"><span data-stu-id="f7185-169">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="f7185-170">Avinstallera med npm</span><span class="sxs-lookup"><span data-stu-id="f7185-170">Uninstall with npm</span></span>

<span data-ttu-id="f7185-171">Ta bort den äldre CLI-versionen med `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="f7185-171">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="f7185-172">Avinstallera med distributable</span><span class="sxs-lookup"><span data-stu-id="f7185-172">Uninstall with distributable</span></span>

<span data-ttu-id="f7185-173">Om du installerade via [MSI](http://aka.ms/webpi-azure-cli) eller ett [Mac OS-paket](http://aka.ms/mac-azure-cli) använder du samma verktyg för att ta bort installationen.</span><span class="sxs-lookup"><span data-stu-id="f7185-173">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="f7185-174">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="f7185-174">Uninstall with Docker</span></span>

<span data-ttu-id="f7185-175">Om du installerade en Docker-avbildning för att använda den tidigare CLI-versionen tar du bort avbildningen och eventuella associerade behållare.</span><span class="sxs-lookup"><span data-stu-id="f7185-175">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="f7185-176">Du kan sedan återskapa behållarna när du har installerat den nya Docker-avbildningen genom att följa installationsanvisningarna.</span><span class="sxs-lookup"><span data-stu-id="f7185-176">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="f7185-177">Uppdatera CLI</span><span class="sxs-lookup"><span data-stu-id="f7185-177">Update the CLI</span></span>

<span data-ttu-id="f7185-178">Uppdatera Azure CLI genom att använda samma metod som du använde för att installera det.</span><span class="sxs-lookup"><span data-stu-id="f7185-178">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="f7185-179">Uppdatera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="f7185-179">Update with Homebrew</span></span>

1. <span data-ttu-id="f7185-180">Uppdatera informationen om din lokala Homebrew-lagringsplats.</span><span class="sxs-lookup"><span data-stu-id="f7185-180">Update your local Homebrew repository information.</span></span>

   ```bash
   brew update
   ```

2. <span data-ttu-id="f7185-181">Uppgradera dina installerade paket.</span><span class="sxs-lookup"><span data-stu-id="f7185-181">Upgrade your installed packages.</span></span>

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a><span data-ttu-id="f7185-182">Uppdatera med MSI</span><span class="sxs-lookup"><span data-stu-id="f7185-182">Update with MSI</span></span>

<span data-ttu-id="f7185-183">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="f7185-183">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="f7185-184">Uppdatera med apt-get</span><span class="sxs-lookup"><span data-stu-id="f7185-184">Update with apt-get</span></span>

<span data-ttu-id="f7185-185">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="f7185-185">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="f7185-186">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="f7185-186">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="f7185-187">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="f7185-187">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="f7185-188">Uppdatera med Docker</span><span class="sxs-lookup"><span data-stu-id="f7185-188">Update with Docker</span></span>

1. <span data-ttu-id="f7185-189">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="f7185-189">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="f7185-190">Hämta behållarna som för närvarande använder CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="f7185-190">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="f7185-191">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="f7185-191">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="f7185-192">Stoppa och återskapa behållarna.</span><span class="sxs-lookup"><span data-stu-id="f7185-192">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="f7185-193">Uppdatera manuellt</span><span class="sxs-lookup"><span data-stu-id="f7185-193">Update manually</span></span>

<span data-ttu-id="f7185-194">Uppdatera genom att följa anvisningarna för manuell installation för [Mac OS](#macOS) eller [Linux](#Linux).</span><span class="sxs-lookup"><span data-stu-id="f7185-194">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="f7185-195">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="f7185-195">Uninstall</span></span>

<span data-ttu-id="f7185-196">Vi tycker det är tråkigt om du väljer att avinstallera CLI.</span><span class="sxs-lookup"><span data-stu-id="f7185-196">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f7185-197">Du bör avinstallera med samma metod som du använde för att installera CLI.</span><span class="sxs-lookup"><span data-stu-id="f7185-197">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="f7185-198">Avinstallera med Homebrew</span><span class="sxs-lookup"><span data-stu-id="f7185-198">Uninstall with Homebrew</span></span>

<span data-ttu-id="f7185-199">Avinstallera `azure-cli`-paketet.</span><span class="sxs-lookup"><span data-stu-id="f7185-199">Uninstall the `azure-cli` package.</span></span>

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a><span data-ttu-id="f7185-200">Avinstallera med MSI</span><span class="sxs-lookup"><span data-stu-id="f7185-200">Uninstall with MSI</span></span>

<span data-ttu-id="f7185-201">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen och välj Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="f7185-201">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="f7185-202">Avinstallera med apt-get</span><span class="sxs-lookup"><span data-stu-id="f7185-202">Uninstall with apt-get</span></span>

<span data-ttu-id="f7185-203">Avinstallera via `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="f7185-203">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="f7185-204">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="f7185-204">Uninstall with Docker</span></span>

<span data-ttu-id="f7185-205">Om du installerade en Docker-avbildning måste du ta bort eventuella behållare som kör den, och sedan ta bort den lokala avbildningen.</span><span class="sxs-lookup"><span data-stu-id="f7185-205">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="f7185-206">Hämta behållarna som kör azure-cli-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="f7185-206">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="f7185-207">Ta bort alla behållare som kör CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="f7185-207">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="f7185-208">Ta bort den lokalt installerade CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="f7185-208">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="f7185-209">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="f7185-209">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="f7185-210">Avinstallera manuellt</span><span class="sxs-lookup"><span data-stu-id="f7185-210">Uninstall manually</span></span>

<span data-ttu-id="f7185-211">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="f7185-211">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="f7185-212">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="f7185-212">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="f7185-213">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="f7185-213">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="f7185-214">Standardplatsen för installation är `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="f7185-214">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="f7185-215">Rapportera problem med CLI och lämna feedback</span><span class="sxs-lookup"><span data-stu-id="f7185-215">Report CLI issues and feedback</span></span>

<span data-ttu-id="f7185-216">Om du stöter på buggar med verktyget kan du rapportera problemet i avsnittet [Problem](https://github.com/Azure/azure-cli/issues) i vår GitHub-databas.</span><span class="sxs-lookup"><span data-stu-id="f7185-216">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="f7185-217">Om du vill skicka feedback från kommandoraden använder du kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="f7185-217">To provide feedback from the command line, use the `az feedback` command.</span></span>
