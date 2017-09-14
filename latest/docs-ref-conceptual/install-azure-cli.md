---
title: Installera Azure CLI 2.0
description: "Referensdokument för installation av Azure CLI 2.0"
keywords: Azure CLI 2.0, Azure CLI 2.0-referens, Installera Azure CLI 2.0, Azure Python CLI, Avinstallera Azure CLI 2.0, Azure CLI, Installera Azure CLI, Azure CLI-referens
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
ms.openlocfilehash: 00d5b555975007d7e57f04ce5d69f4f29e6d0219
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/04/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="54821-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="54821-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="54821-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="54821-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="54821-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="54821-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="54821-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="54821-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="54821-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="54821-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="54821-109">Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure CLI 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="54821-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="54821-110"><a name="macOS"/>Installera i Mac OS</span><span class="sxs-lookup"><span data-stu-id="54821-110"><a name="macOS"/>Install on macOS</span></span>

1. <span data-ttu-id="54821-111">Installera Azure CLI 2.0 med `curl`.</span><span class="sxs-lookup"><span data-stu-id="54821-111">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="54821-112">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="54821-112">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="54821-113">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="54821-113">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="54821-114">Installera i Windows</span><span class="sxs-lookup"><span data-stu-id="54821-114">Install on Windows</span></span>

<span data-ttu-id="54821-115">Du kan installera Azure CLI 2.0 med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med `apt-get` i Bash i Ubuntu för Windows.</span><span class="sxs-lookup"><span data-stu-id="54821-115">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with `apt-get` on Bash on Ubuntu on Windows.</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="54821-116">Installera med MSI för kommandoraden i Windows</span><span class="sxs-lookup"><span data-stu-id="54821-116">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="54821-117">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [MSI](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="54821-117">To install the CLI on Windows and use it in the Windows command-line, download and run the [MSI](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="54821-118">Installera med apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="54821-118">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="54821-119">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="54821-119">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="54821-120">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="54821-120">Open the Bash shell.</span></span>

3. <span data-ttu-id="54821-121">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="54821-121">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="54821-122">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="54821-122">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="54821-123">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="54821-123">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="54821-124">Installera i Debian/Ubuntu med apt-get</span><span class="sxs-lookup"><span data-stu-id="54821-124">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="54821-125">Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.</span><span class="sxs-lookup"><span data-stu-id="54821-125">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="54821-126">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="54821-126">Modify your sources list.</span></span>
 
   - <span data-ttu-id="54821-127">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="54821-127">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="54821-128">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="54821-128">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="54821-129">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="54821-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="54821-130">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="54821-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="54821-131">Installera med Docker</span><span class="sxs-lookup"><span data-stu-id="54821-131">Install with Docker</span></span>

<span data-ttu-id="54821-132">Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="54821-132">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="54821-133">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="54821-133">Install the CLI using `docker run`.</span></span>

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

<span data-ttu-id="54821-134">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="54821-134">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="54821-135">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="54821-135">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="54821-136">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="54821-136">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="54821-137"><a name="Linux"/>Installera i Linux utan apt-get</span><span class="sxs-lookup"><span data-stu-id="54821-137"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="54821-138">Vi rekommenderar att du installerar CLI med `apt-get` om möjligt.</span><span class="sxs-lookup"><span data-stu-id="54821-138">It is recommended that you install the CLI with `apt-get` if you are able to.</span></span> <span data-ttu-id="54821-139">För distributioner som inte använder `apt`-pakethanteraren kan du installera manuellt.</span><span class="sxs-lookup"><span data-stu-id="54821-139">For distributions which do not use the `apt` package manager, you can manually install.</span></span>

1. <span data-ttu-id="54821-140">Kontrollera att din Linux-distribution uppfyller alla förhandskrav.</span><span class="sxs-lookup"><span data-stu-id="54821-140">Install the prerequisites based on your Linux distribution.</span></span>

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

<span data-ttu-id="54821-141">Om din distribution inte visas i listan ovan måste du installera [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/) och [OpenSSL](https://www.openssl.org/source/).</span><span class="sxs-lookup"><span data-stu-id="54821-141">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="54821-142">Installera CLI med `curl`.</span><span class="sxs-lookup"><span data-stu-id="54821-142">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="54821-143">Du kan behöva starta om gränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="54821-143">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="54821-144">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="54821-144">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="54821-145">Felsökning</span><span class="sxs-lookup"><span data-stu-id="54821-145">Troubleshooting</span></span>

<span data-ttu-id="54821-146">Om det uppstår problem under CLI-installationen läser du det här avsnittet för att se om ditt problem tas upp.</span><span class="sxs-lookup"><span data-stu-id="54821-146">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="54821-147">Om du inte hittar ditt problem här [öppnar du ett Github-supportärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="54821-147">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="54821-148">Fel: curl "Object Moved"</span><span class="sxs-lookup"><span data-stu-id="54821-148">curl "Object Moved" error</span></span>

<span data-ttu-id="54821-149">Om `curl` returnerar ett fel relaterat till `-L`-parametern, eller ett felmeddelande som innehåller texten ”Object Moved”, provar du att använda den fullständiga URL-adressen i stället för `aka.ms`-omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="54821-149">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a><span data-ttu-id="54821-150">Homebrew i Mac OS installerar äldre version</span><span class="sxs-lookup"><span data-stu-id="54821-150">Homebrew on macOS installing older version</span></span>

<span data-ttu-id="54821-151">Homebrew-formeln `azure-cli` som är tillgänglig för Mac OS är föråldrad och installerar en 1.x-version av CLI.</span><span class="sxs-lookup"><span data-stu-id="54821-151">The Homebrew `azure-cli` formula available for macOS is currently out of date, and will install a 1.x version of the CLI.</span></span> <span data-ttu-id="54821-152">Du kan se när den uppdateras genom att köra `brew info azure-cli`.</span><span class="sxs-lookup"><span data-stu-id="54821-152">You can see when it is updated by checking `brew info azure-cli`.</span></span>

<span data-ttu-id="54821-153">Tills dess [avinstallerar du den äldre versionen](#uninstall_brew) och följer [installationsanvisningarna för Mac OS](#macOS).</span><span class="sxs-lookup"><span data-stu-id="54821-153">Until then, [uninstall the older version](#uninstall_brew) and follow the [macOS install instructions](#macOS).</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="54821-154">Avinstallera CLI 1.x-versioner</span><span class="sxs-lookup"><span data-stu-id="54821-154">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="54821-155">Om du har en tidigare CLI 1.x-version på datorn kan du avinstallera den baserat på den typ av installation du använde för att installera versionen.</span><span class="sxs-lookup"><span data-stu-id="54821-155">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="54821-156">Avinstallera med npm</span><span class="sxs-lookup"><span data-stu-id="54821-156">Uninstall with npm</span></span>

<span data-ttu-id="54821-157">Ta bort den äldre CLI-versionen med `npm uninstall`.</span><span class="sxs-lookup"><span data-stu-id="54821-157">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><span data-ttu-id="54821-158"><a name="uninstall_brew"/>Avinstallera med Homebrew i Mac OS</span><span class="sxs-lookup"><span data-stu-id="54821-158"><a name="uninstall_brew"/>Uninstall with Homebrew on macOS</span></span>

<span data-ttu-id="54821-159">Ta bort den äldre CLI-versionen med `brew uninstall`.</span><span class="sxs-lookup"><span data-stu-id="54821-159">Remove the older CLI with `brew uninstall`.</span></span>

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="54821-160">Avinstallera med distributable</span><span class="sxs-lookup"><span data-stu-id="54821-160">Uninstall with distributable</span></span>

<span data-ttu-id="54821-161">Om du installerade via [MSI](http://aka.ms/webpi-azure-cli) eller ett [Mac OS-paket](http://aka.ms/mac-azure-cli) använder du samma verktyg för att ta bort installationen.</span><span class="sxs-lookup"><span data-stu-id="54821-161">If you installed via [MSI](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="54821-162">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="54821-162">Uninstall with Docker</span></span>

<span data-ttu-id="54821-163">Om du installerade en Docker-avbildning för att använda den tidigare CLI-versionen tar du bort avbildningen och eventuella associerade behållare.</span><span class="sxs-lookup"><span data-stu-id="54821-163">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="54821-164">Du kan sedan återskapa behållarna när du har installerat den nya Docker-avbildningen genom att följa installationsanvisningarna.</span><span class="sxs-lookup"><span data-stu-id="54821-164">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="54821-165">Uppdatera CLI</span><span class="sxs-lookup"><span data-stu-id="54821-165">Update the CLI</span></span>

<span data-ttu-id="54821-166">Uppdatera Azure CLI genom att använda samma metod som du använde för att installera det.</span><span class="sxs-lookup"><span data-stu-id="54821-166">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-msi"></a><span data-ttu-id="54821-167">Uppdatera med MSI</span><span class="sxs-lookup"><span data-stu-id="54821-167">Update with MSI</span></span>

<span data-ttu-id="54821-168">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="54821-168">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="54821-169">Uppdatera med apt-get</span><span class="sxs-lookup"><span data-stu-id="54821-169">Update with apt-get</span></span>

<span data-ttu-id="54821-170">Använd `apt-get upgrade` för att uppdatera CLI-paketet.</span><span class="sxs-lookup"><span data-stu-id="54821-170">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="54821-171">När du gör det uppgraderas alla installerade paket på datorn som ingen beroendeändring gjorts för.</span><span class="sxs-lookup"><span data-stu-id="54821-171">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="54821-172">Om du bara vill uppgradera CLI använder du `apt-get install`.</span><span class="sxs-lookup"><span data-stu-id="54821-172">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="54821-173">Uppdatera med Docker</span><span class="sxs-lookup"><span data-stu-id="54821-173">Update with Docker</span></span>

1. <span data-ttu-id="54821-174">Uppdatera den lokala avbildningen med `docker pull`.</span><span class="sxs-lookup"><span data-stu-id="54821-174">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="54821-175">Hämta behållarna som för närvarande använder CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="54821-175">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="54821-176">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="54821-176">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="54821-177">Stoppa och återskapa behållarna.</span><span class="sxs-lookup"><span data-stu-id="54821-177">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="54821-178">Uppdatera manuellt</span><span class="sxs-lookup"><span data-stu-id="54821-178">Update manually</span></span>

<span data-ttu-id="54821-179">Uppdatera genom att följa anvisningarna för manuell installation för [Mac OS](#macOS) eller [Linux](#Linux).</span><span class="sxs-lookup"><span data-stu-id="54821-179">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="54821-180">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="54821-180">Uninstall</span></span>

<span data-ttu-id="54821-181">Vi tycker det är tråkigt om du väljer att avinstallera CLI.</span><span class="sxs-lookup"><span data-stu-id="54821-181">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="54821-182">Du bör avinstallera med samma metod som du använde för att installera CLI.</span><span class="sxs-lookup"><span data-stu-id="54821-182">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-msi"></a><span data-ttu-id="54821-183">Avinstallera med MSI</span><span class="sxs-lookup"><span data-stu-id="54821-183">Uninstall with MSI</span></span>

<span data-ttu-id="54821-184">Kör [MSI](https://aka.ms/InstallAzureCliWindows) igen och välj Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="54821-184">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="54821-185">Avinstallera med apt-get</span><span class="sxs-lookup"><span data-stu-id="54821-185">Uninstall with apt-get</span></span>

<span data-ttu-id="54821-186">Avinstallera via `apt-get remove`:</span><span class="sxs-lookup"><span data-stu-id="54821-186">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="54821-187">Avinstallera med Docker</span><span class="sxs-lookup"><span data-stu-id="54821-187">Uninstall with Docker</span></span>

<span data-ttu-id="54821-188">Om du installerade en Docker-avbildning måste du ta bort eventuella behållare som kör den, och sedan ta bort den lokala avbildningen.</span><span class="sxs-lookup"><span data-stu-id="54821-188">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="54821-189">Hämta behållarna som kör azure-cli-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="54821-189">Get the containers which are running the azure-cli image.</span></span>

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. <span data-ttu-id="54821-190">Ta bort alla behållare som kör CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="54821-190">Delete any containers with the CLI image.</span></span>

  ```bash
  docker rm 34a868beb2ab
  ```

3. <span data-ttu-id="54821-191">Ta bort den lokalt installerade CLI-avbildningen.</span><span class="sxs-lookup"><span data-stu-id="54821-191">Remove the locally installed CLI image.</span></span>

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> <span data-ttu-id="54821-192">Om du installerade en specifik version av avbildningen måste du lägga till `:<version>` i slutet av avbildningens namn.</span><span class="sxs-lookup"><span data-stu-id="54821-192">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

### <a name="uninstall-manually"></a><span data-ttu-id="54821-193">Avinstallera manuellt</span><span class="sxs-lookup"><span data-stu-id="54821-193">Uninstall manually</span></span>

<span data-ttu-id="54821-194">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="54821-194">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="54821-195">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="54821-195">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="54821-196">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="54821-196">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="54821-197">Standardplatsen för installation är `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="54821-197">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="54821-198">Rapportera problem med CLI och lämna feedback</span><span class="sxs-lookup"><span data-stu-id="54821-198">Report CLI issues and feedback</span></span>

<span data-ttu-id="54821-199">Om du stöter på buggar med verktyget kan du rapportera problemet i avsnittet [Problem](https://github.com/Azure/azure-cli/issues) i vår GitHub-databas.</span><span class="sxs-lookup"><span data-stu-id="54821-199">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="54821-200">Om du vill skicka feedback från kommandoraden använder du kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="54821-200">To provide feedback from the command line, use the `az feedback` command.</span></span>
