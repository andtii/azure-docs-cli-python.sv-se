---
title: Installera Azure CLI 2.0
description: "Referensdokument för att installera Azure CLI 2.0"
keywords: Azure CLI 2.0, Azure CLI 2.0-referens, Installera Azure CLI 2.0, Azure Python CLI, Avinstallera Azure CLI 2.0
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 08/17/2017
ms.topic: "articleå"
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 432edac070e238a6f1be0ccd76b9b3582b082219
ms.sourcegitcommit: 2ec80224c6b831e31038b710d912c0dbb1ddfef6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/17/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="14c2e-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="14c2e-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="14c2e-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="14c2e-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="14c2e-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="14c2e-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="14c2e-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="14c2e-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="14c2e-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="14c2e-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-109">Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure CLI 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="14c2e-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="14c2e-110">macOS</span><span class="sxs-lookup"><span data-stu-id="14c2e-110">macOS</span></span>

> [!WARNING]
> <span data-ttu-id="14c2e-111">Homebrew-formeln för Azure CLI, `azure-cli`, är inaktuell. En tidigare version kommer att installeras.</span><span class="sxs-lookup"><span data-stu-id="14c2e-111">The Homebrew formula for the Azure CLI, `azure-cli`, is currently out of date and will install a previous version.</span></span>

1. <span data-ttu-id="14c2e-112">Installera Azure CLI 2.0 med ett `curl`-kommando.</span><span class="sxs-lookup"><span data-stu-id="14c2e-112">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="14c2e-113">Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="14c2e-113">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="14c2e-114">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-114">Run the CLI from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="14c2e-115">När du installerar med InstallAzureCli stöds inte [`az component update`](/cli/azure/component#update).</span><span class="sxs-lookup"><span data-stu-id="14c2e-115">When you install with InstallAzureCli, [`az component update`](/cli/azure/component#update) isn't supported.</span></span>
> <span data-ttu-id="14c2e-116">Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-116">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="14c2e-117">Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="14c2e-117">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="14c2e-118">Windows</span><span class="sxs-lookup"><span data-stu-id="14c2e-118">Windows</span></span>

<span data-ttu-id="14c2e-119">Du kan installera Azure CLI 2.0 med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med apt-get i Bash i Ubuntu för Windows.</span><span class="sxs-lookup"><span data-stu-id="14c2e-119">You can install Azure CLI 2.0 with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="14c2e-120">MSI för Windows-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="14c2e-120">MSI for the Windows command-line</span></span> 

<span data-ttu-id="14c2e-121">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [msi](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="14c2e-121">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-122">[`az component`](/cli/azure/component) stöds inte om du installerar med msi.</span><span class="sxs-lookup"><span data-stu-id="14c2e-122">When you install with the msi, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="14c2e-123">Om du vill uppdatera till den senaste versionen av CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-123">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="14c2e-124">Om du vill avinstallera CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen och väljer Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="14c2e-124">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="14c2e-125">apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="14c2e-125">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="14c2e-126">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="14c2e-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="14c2e-127">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="14c2e-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="14c2e-128">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="14c2e-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="14c2e-129">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="14c2e-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="14c2e-130">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-130">Run the CLI from the command prompt with the `az` command.</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-131">När du installerar med apt-get stöds inte [`az component`](/cli/azure/component).</span><span class="sxs-lookup"><span data-stu-id="14c2e-131">When you install with apt-get, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="14c2e-132">Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-132">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="14c2e-133">Kör `sudo apt-get remove azure-cli` för att avinstallera.</span><span class="sxs-lookup"><span data-stu-id="14c2e-133">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="apt-get-for-debianubuntu"></a><span data-ttu-id="14c2e-134">apt-get för Debian/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="14c2e-134">apt-get for Debian/Ubuntu</span></span>

<span data-ttu-id="14c2e-135">Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.</span><span class="sxs-lookup"><span data-stu-id="14c2e-135">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="14c2e-136">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="14c2e-136">Modify your sources list.</span></span>
 
   - <span data-ttu-id="14c2e-137">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="14c2e-137">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="14c2e-138">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="14c2e-138">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="14c2e-139">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="14c2e-139">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="14c2e-140">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-140">Run the CLI from the command prompt with the `az` command.</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-141">När du installerar med apt-get stöds inte [`az component`](/cli/azure/component).</span><span class="sxs-lookup"><span data-stu-id="14c2e-141">When you install with apt-get, [`az component`](/cli/azure/component) isn't supported.</span></span>
> <span data-ttu-id="14c2e-142">Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-142">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="14c2e-143">Kör `sudo apt-get remove azure-cli` för att avinstallera.</span><span class="sxs-lookup"><span data-stu-id="14c2e-143">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="docker"></a><span data-ttu-id="14c2e-144">Docker</span><span class="sxs-lookup"><span data-stu-id="14c2e-144">Docker</span></span>

<span data-ttu-id="14c2e-145">Vi tillhandahåller en Docker-avbildning som är förkonfigurerad med Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="14c2e-145">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="14c2e-146">Installera CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-146">Install the CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="14c2e-147">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="14c2e-147">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-148">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-148">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

>> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

<span data-ttu-id="14c2e-149">CLI installeras i avbildningen som `az`-kommandot i `/usr/local/bin`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-149">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="14c2e-150">Docker-avbildningen stöder inte [`az component`](/cli/azure/component)-funktionen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-150">The Docker image does not support the [`az component`](/cli/azure/component) feature.</span></span>
> <span data-ttu-id="14c2e-151">Använd `docker run` för att installera den senaste avbildningen eller en specifik avbildning som du vill ha för att uppdatera Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="14c2e-151">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="linux"></a><span data-ttu-id="14c2e-152">Linux</span><span class="sxs-lookup"><span data-stu-id="14c2e-152">Linux</span></span>

1. <span data-ttu-id="14c2e-153">Om du inte har [Python](https://www.python.org/downloads) kan du installera det.</span><span class="sxs-lookup"><span data-stu-id="14c2e-153">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="14c2e-154">Installera de nödvändiga förutsättningarna beroende på vilken Linux-distribution du har.</span><span class="sxs-lookup"><span data-stu-id="14c2e-154">Depending on your Linux distribution, install the prerequisites.</span></span>

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

3. <span data-ttu-id="14c2e-155">Installera CLI med ett `curl`-kommando.</span><span class="sxs-lookup"><span data-stu-id="14c2e-155">Install the CLI with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

4. <span data-ttu-id="14c2e-156">Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="14c2e-156">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

5. <span data-ttu-id="14c2e-157">Kör CLI från kommandotolken med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-157">Run the CLI from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="14c2e-158">När du installerar med InstallAzureCli stöds inte [`az component update`](/cli/azure/component#update).</span><span class="sxs-lookup"><span data-stu-id="14c2e-158">When you install with InstallAzureCli, [`az component update`](/cli/azure/component#update) isn't supported.</span></span>
> <span data-ttu-id="14c2e-159">Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.</span><span class="sxs-lookup"><span data-stu-id="14c2e-159">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="14c2e-160">Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="14c2e-160">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="14c2e-161">Felsökning</span><span class="sxs-lookup"><span data-stu-id="14c2e-161">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="14c2e-162">Fel vid omdirigering av curl</span><span class="sxs-lookup"><span data-stu-id="14c2e-162">Errors with curl redirection</span></span>

<span data-ttu-id="14c2e-163">Om du får ett fel från `curl`-kommandot angående `-L`-parametern eller ett fel som hänvisar till "Object Moved" så kan du försöka använda en fullständig URL i stället för URL:en aka.ms:</span><span class="sxs-lookup"><span data-stu-id="14c2e-163">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

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

## <a name="uninstall"></a><span data-ttu-id="14c2e-164">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="14c2e-164">Uninstall</span></span>

<span data-ttu-id="14c2e-165">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="14c2e-165">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="14c2e-166">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="14c2e-166">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="14c2e-167">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-167">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="14c2e-168">Standardplatsen för installation är `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-168">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="14c2e-169">Om du använde apt-get, Docker eller msi för att installera CLI använder du samma verktyg för att avinstallera det.</span><span class="sxs-lookup"><span data-stu-id="14c2e-169">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="14c2e-170">Rapportera problem och feedback</span><span class="sxs-lookup"><span data-stu-id="14c2e-170">Reporting issues and feedback</span></span>

<span data-ttu-id="14c2e-171">Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-cli/issues)-delen av vårt GitHub-repo.</span><span class="sxs-lookup"><span data-stu-id="14c2e-171">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="14c2e-172">Om du vill ge feedback från kommandoraden kan du prova kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="14c2e-172">To provide feedback from the command line, try the `az feedback` command.</span></span>
