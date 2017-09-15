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
ms.openlocfilehash: a61f47076854d0ff0a7056f82240794b7533fe3e
ms.sourcegitcommit: 3db5fb207db551a0d3fe0a88fe09e8f5e2ec184d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/14/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="282be-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="282be-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="282be-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="282be-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="282be-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="282be-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="282be-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="282be-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="282be-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="282be-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="282be-109">Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure CLI 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="282be-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="282be-110"><a name="macOS"/>Installera i Mac OS</span><span class="sxs-lookup"><span data-stu-id="282be-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="282be-111">Installera Azure CLI 2.0 med `curl`.</span><span class="sxs-lookup"><span data-stu-id="282be-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="282be-112">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="282be-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="282be-113">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="282be-114">Installera i Windows</span><span class="sxs-lookup"><span data-stu-id="282be-114">Install on Windows</span></span>

<span data-ttu-id="282be-115">Du kan installera Azure CLI 2.0 med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med `apt-get` i Bash i Ubuntu för Windows.</span><span class="sxs-lookup"><span data-stu-id="282be-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="282be-116">Installera med MSI för kommandoraden i Windows</span><span class="sxs-lookup"><span data-stu-id="282be-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="282be-117">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="282be-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="282be-118">Installera med apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="282be-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="282be-119">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="282be-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="282be-120">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="282be-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="282be-121">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="282be-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="282be-122">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="282be-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="282be-123">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="282be-124">Installera i Debian/Ubuntu med apt-get</span><span class="sxs-lookup"><span data-stu-id="282be-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="282be-125">Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.</span><span class="sxs-lookup"><span data-stu-id="282be-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="282be-126">Ändra listan med källor:</span><span class="sxs-lookup"><span data-stu-id="282be-126">Modify your sources list:</span></span>
 
   - <span data-ttu-id="282be-127">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="282be-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="282be-128">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="282be-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="282be-129">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="282be-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="282be-130">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a><span data-ttu-id="282be-131">Installera på RHEL, Fedora och CentOS med yum</span><span class="sxs-lookup"><span data-stu-id="282be-131">Install on RHEL, Fedora, and CentOS with yum</span></span>

<span data-ttu-id="282be-132">För distributioner som bygger på RedHat och innehåller `yum`-pakethanteraren kan du installera Azure CLI 2.0 via `yum`.</span><span class="sxs-lookup"><span data-stu-id="282be-132">For any distribution which is based off of RedHat and contains the `yum` package manager, you can install Azure CLI 2.0 via `yum`.</span></span>

1. <span data-ttu-id="282be-133">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="282be-133">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="282be-134">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="282be-134">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="282be-135">Uppdatera `yum`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="282be-135">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="282be-136">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-136">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-opensuse-and-sle-with-zypper"></a><span data-ttu-id="282be-137">Installera på openSUSE och SLE med zypper</span><span class="sxs-lookup"><span data-stu-id="282be-137">Install on openSUSE and SLE with zypper</span></span>

1. <span data-ttu-id="282be-138">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="282be-138">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="282be-139">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="282be-139">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="282be-140">Uppdatera `zypper`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="282be-140">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="282be-141">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-141">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="282be-142">Installera med Docker</span><span class="sxs-lookup"><span data-stu-id="282be-142">Install with Docker</span></span>

<span data-ttu-id="282be-143">Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="282be-143">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="282be-144">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="282be-144">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="282be-145">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="282be-145">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="282be-146">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="282be-146">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="282be-147">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="282be-147">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="282be-148"><a name="Linux"/>Installera i Linux utan apt-get</span><span class="sxs-lookup"><span data-stu-id="282be-148"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="282be-149">Om det är möjligt rekommenderar vi att du installerar CLI med en pakethanterare.</span><span class="sxs-lookup"><span data-stu-id="282be-149">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="282be-150">För distributioner som inte har någon pakethanterare kan du installera manuellt.</span><span class="sxs-lookup"><span data-stu-id="282be-150">For distributions which do not have a package provided for them, you can manually install.</span></span>

1. <span data-ttu-id="282be-151">Kontrollera att din Linux-distribution uppfyller alla förhandskrav.</span><span class="sxs-lookup"><span data-stu-id="282be-151">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="282be-152">Om din distribution inte visas i listan ovan måste du installera [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/) och [OpenSSL](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="282be-152">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="282be-153">Installera CLI med `curl`.</span><span class="sxs-lookup"><span data-stu-id="282be-153">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="282be-154">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="282be-154">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="282be-155">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="282be-155">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="282be-156">Felsökning</span><span class="sxs-lookup"><span data-stu-id="282be-156">Troubleshooting</span></span>

<span data-ttu-id="282be-157">Om det uppstår problem under CLI-installationen läser du det här avsnittet för att se om ditt problem tas upp.</span><span class="sxs-lookup"><span data-stu-id="282be-157">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="282be-158">Om du inte hittar ditt problem här [öppnar du ett Github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="282be-158">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="282be-159">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="282be-159">curl "Object Moved" error</span></span>

<span data-ttu-id="282be-160">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="282be-160">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="282be-161">Homebrew i Mac OS installerar äldre version</span><span class="sxs-lookup"><span data-stu-id="282be-161">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="282be-162">Homebrew-formeln `azure-cli` som är tillgänglig för Mac OS är föråldrad och installerar en 1.x-version av CLI.</span><span class="sxs-lookup"><span data-stu-id="282be-162">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="282be-163">Du kan se när den uppdateras genom att köra `brew info azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="282be-163">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="282be-164">Tills dess [avinstallerar du den äldre versionen](#uninstall_brew) och följer [installationsanvisningarna för Mac OS](#macOS).</span><span class="sxs-lookup"><span data-stu-id="282be-164">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="282be-165">Avinstallera CLI 1.x-versioner</span><span class="sxs-lookup"><span data-stu-id="282be-165">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="282be-166">Om du har en tidigare CLI 1.x-version på datorn kan du avinstallera den baserat på den typ av installation du använde för att installera versionen.</span><span class="sxs-lookup"><span data-stu-id="282be-166">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="282be-167">Avinstallera med npm</span><span class="sxs-lookup"><span data-stu-id="282be-167">Uninstall with npm</span></span>

<span data-ttu-id="282be-168">Ta bort den äldre CLI-versionen med `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="282be-168">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="282be-169"><a name="uninstall_brew"/>Avinstallera med Homebrew i Mac OS</span><span class="sxs-lookup"><span data-stu-id="282be-169"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="282be-170">Ta bort den äldre CLI-versionen med `brew uninstall`.</span><span class="sxs-lookup"><span data-stu-id="282be-170">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="282be-171">Avinstallera med distributable</span><span class="sxs-lookup"><span data-stu-id="282be-171">Uninstall with distributable</span></span>

<span data-ttu-id="282be-172">Om du installerade via [MSI](http://aka.ms/webpi-azure-cli) eller ett [Mac OS-paket](http://aka.ms/mac-azure-cli) använder du samma verktyg för att ta bort installationen.</span><span class="sxs-lookup"><span data-stu-id="282be-172">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="282be-173">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="282be-173">Uninstall with Docker</span></span>

<span data-ttu-id="282be-174">Om du installerade en Docker-avbildning för att använda den tidigare CLI-versionen tar du bort avbildningen och eventuella associerade behållare.</span><span class="sxs-lookup"><span data-stu-id="282be-174">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="282be-175">Du kan sedan återskapa behållarna när du har installerat den nya Docker-avbildningen genom att följa installationsanvisningarna.</span><span class="sxs-lookup"><span data-stu-id="282be-175">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="282be-176">Uppdatera CLI</span><span class="sxs-lookup"><span data-stu-id="282be-176">Update the CLI</span></span>

<span data-ttu-id="282be-177">Uppdatera Azure CLI genom att använda samma metod som du använde för att installera det.</span><span class="sxs-lookup"><span data-stu-id="282be-177">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="282be-178">Uppdatera med MSI</span><span class="sxs-lookup"><span data-stu-id="282be-178">Update with MSI</span></span>

<span data-ttu-id="282be-179">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="282be-179">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="282be-180">Uppdatera med apt-get</span><span class="sxs-lookup"><span data-stu-id="282be-180">Update with apt-get</span></span>

<span data-ttu-id="282be-181">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="282be-181">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="282be-182">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="282be-182">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="282be-183">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="282be-183">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="282be-184">Uppdatera med Docker</span><span class="sxs-lookup"><span data-stu-id="282be-184">Update with Docker</span></span>

1. <span data-ttu-id="282be-185">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="282be-185">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="282be-186">Hämta behållarna som för närvarande använder CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="282be-186">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="282be-187">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="282be-187">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="282be-188">Stoppa och återskapa behållarna.</span><span class="sxs-lookup"><span data-stu-id="282be-188">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="282be-189">Uppdatera manuellt</span><span class="sxs-lookup"><span data-stu-id="282be-189">Update manually</span></span>

<span data-ttu-id="282be-190">Uppdatera genom att följa anvisningarna för manuell installation för [Mac OS](#macOS) eller [Linux](#Linux).</span><span class="sxs-lookup"><span data-stu-id="282be-190">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="282be-191">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="282be-191">Uninstall</span></span>

<span data-ttu-id="282be-192">Vi tycker det är tråkigt om du väljer att avinstallera CLI.</span><span class="sxs-lookup"><span data-stu-id="282be-192">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="282be-193">Du bör avinstallera med samma metod som du använde för att installera CLI.</span><span class="sxs-lookup"><span data-stu-id="282be-193">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="282be-194">Avinstallera med MSI</span><span class="sxs-lookup"><span data-stu-id="282be-194">Uninstall with MSI</span></span>

<span data-ttu-id="282be-195">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen och välj Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="282be-195">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="282be-196">Avinstallera med apt-get</span><span class="sxs-lookup"><span data-stu-id="282be-196">Uninstall with apt-get</span></span>

<span data-ttu-id="282be-197">Avinstallera via `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="282be-197">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="282be-198">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="282be-198">Uninstall with Docker</span></span>

<span data-ttu-id="282be-199">Om du installerade en Docker-avbildning måste du ta bort eventuella behållare som kör den, och sedan ta bort den lokala avbildningen.</span><span class="sxs-lookup"><span data-stu-id="282be-199">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="282be-200">Hämta behållarna som kör azure-cli-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="282be-200">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="282be-201">Ta bort alla behållare som kör CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="282be-201">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="282be-202">Ta bort den lokalt installerade CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="282be-202">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="282be-203">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="282be-203">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="282be-204">Avinstallera manuellt</span><span class="sxs-lookup"><span data-stu-id="282be-204">Uninstall manually</span></span>

<span data-ttu-id="282be-205">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="282be-205">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="282be-206">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="282be-206">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="282be-207">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="282be-207">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="282be-208">Standardplatsen för installation är `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="282be-208">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="282be-209">Rapportera problem med CLI och lämna feedback</span><span class="sxs-lookup"><span data-stu-id="282be-209">Report CLI issues and feedback</span></span>

<span data-ttu-id="282be-210">Om du stöter på buggar med verktyget kan du rapportera problemet i avsnittet [Problem](https://github.com/Azure/azure-cli/issues) i vår GitHub-databas.</span><span class="sxs-lookup"><span data-stu-id="282be-210">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="282be-211">Om du vill skicka feedback från kommandoraden använder du kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="282be-211">To provide feedback from the command line, use the `az feedback` command.</span></span>
