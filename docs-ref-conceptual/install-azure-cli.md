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
ms.contentlocale: sv-SE
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="d5578-104">Installera Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="d5578-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="d5578-105">Installera den nya versionen av Azure CLI idag!</span><span class="sxs-lookup"><span data-stu-id="d5578-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="d5578-106">Vi har förbättrat och uppdaterat den för att tillhandahålla den bästa möjliga interna kommandoraden för att hantera Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="d5578-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="d5578-107">Den kan användas i Mac OS, Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="d5578-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="d5578-108">Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="d5578-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d5578-109">Om du behöver den tidigare versionen av Azure CLI gör du så här för att [installera Azure 1.0](/azure/cli-install-nodejs).</span><span class="sxs-lookup"><span data-stu-id="d5578-109">If you need the previous version of the Azure CLI, here's how to [install Azure 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="d5578-110">macOS</span><span class="sxs-lookup"><span data-stu-id="d5578-110">macOS</span></span>

1. <span data-ttu-id="d5578-111">Installera Azure CLI 2.0 med ett `curl`-kommando.</span><span class="sxs-lookup"><span data-stu-id="d5578-111">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="d5578-112">Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="d5578-112">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="d5578-113">Kör Azure CLI 2.0 från kommandotolken med `az`-kommandot.</span><span class="sxs-lookup"><span data-stu-id="d5578-113">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="d5578-114">När du installerar med InstallAzureCli stöds inte `az component update`.</span><span class="sxs-lookup"><span data-stu-id="d5578-114">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="d5578-115">Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.</span><span class="sxs-lookup"><span data-stu-id="d5578-115">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="d5578-116">Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5578-116">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="d5578-117">Windows</span><span class="sxs-lookup"><span data-stu-id="d5578-117">Windows</span></span>

<span data-ttu-id="d5578-118">Du kan installera CLI med MSI och använda det på kommandoraden i Windows, eller så kan du installera CLI med apt-get i Bash i Ubuntu för Windows.</span><span class="sxs-lookup"><span data-stu-id="d5578-118">You can install the CLI with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="d5578-119">MSI för Windows-kommandoraden</span><span class="sxs-lookup"><span data-stu-id="d5578-119">MSI for the Windows command-line</span></span> 

<span data-ttu-id="d5578-120">Om du vill installera CLI i Windows och använda det på Windows-kommandoraden laddar du ned och kör [msi](https://aka.ms/InstallAzureCliWindows).</span><span class="sxs-lookup"><span data-stu-id="d5578-120">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="d5578-121">`az component` stöds inte om du installerar med msi.</span><span class="sxs-lookup"><span data-stu-id="d5578-121">When you install with the msi, `az component` isn't supported.</span></span>
> <span data-ttu-id="d5578-122">Om du vill uppdatera till den senaste versionen av CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen.</span><span class="sxs-lookup"><span data-stu-id="d5578-122">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="d5578-123">Om du vill avinstallera CLI kör du [msi](https://aka.ms/InstallAzureCliWindows) igen och väljer Avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5578-123">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="d5578-124">apt-get för Bash i Ubuntu för Windows</span><span class="sxs-lookup"><span data-stu-id="d5578-124">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="d5578-125">Om du inte har Bash på Windows [installerar du det](https://msdn.microsoft.com/commandline/wsl/install_guide).</span><span class="sxs-lookup"><span data-stu-id="d5578-125">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="d5578-126">Öppna Bash-gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d5578-126">Open the Bash shell.</span></span>

3. <span data-ttu-id="d5578-127">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="d5578-127">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="d5578-128">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="d5578-128">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="d5578-129">När du installerar med apt-get stöds inte `az component`.</span><span class="sxs-lookup"><span data-stu-id="d5578-129">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="d5578-130">Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.</span><span class="sxs-lookup"><span data-stu-id="d5578-130">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="d5578-131">Kör `sudo apt-get remove azure-cli` för att avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5578-131">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux"></a><span data-ttu-id="d5578-132">Linux</span><span class="sxs-lookup"><span data-stu-id="d5578-132">Linux</span></span>

1. <span data-ttu-id="d5578-133">På Linux kan du behöva installera specifika [förutsättningar](#linux-prerequisites).</span><span class="sxs-lookup"><span data-stu-id="d5578-133">On Linux, you may need to install specific [prerequisites](#linux-prerequisites).</span></span>

2. <span data-ttu-id="d5578-134">Installera Azure CLI 2.0 med ett `curl`-kommando.</span><span class="sxs-lookup"><span data-stu-id="d5578-134">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="d5578-135">Du kan behöva starta om kommandogränssnittet för att vissa ändringar ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="d5578-135">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="d5578-136">Kör Azure CLI 2.0 från kommandotolken med `az`-kommandot.</span><span class="sxs-lookup"><span data-stu-id="d5578-136">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="d5578-137">När du installerar med InstallAzureCli stöds inte `az component update`.</span><span class="sxs-lookup"><span data-stu-id="d5578-137">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="d5578-138">Om du vill uppdatera till den senaste versionen av CLI kör du `curl -L https://aka.ms/InstallAzureCli | bash` igen.</span><span class="sxs-lookup"><span data-stu-id="d5578-138">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="d5578-139">Läs de [manuella instruktionerna för att avinstallera](#uninstall) om du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5578-139">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="docker"></a><span data-ttu-id="d5578-140">Docker</span><span class="sxs-lookup"><span data-stu-id="d5578-140">Docker</span></span>

<span data-ttu-id="d5578-141">Vi underhåller en Docker-avbildning som är förkonfigurerad med Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="d5578-141">We maintain a Docker image preconfigured with the Azure CLI.</span></span>

<span data-ttu-id="d5578-142">Installera Azure CLI med `docker run`.</span><span class="sxs-lookup"><span data-stu-id="d5578-142">Install the Azure CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="d5578-143">Se våra [Docker-taggar](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) för tillgängliga versioner.</span><span class="sxs-lookup"><span data-stu-id="d5578-143">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="d5578-144">Om du vill hämta SSH-nycklarna från användarmiljön så kan du använda `-v ${HOME}:/root` för att montera $HOME som `/root`.</span><span class="sxs-lookup"><span data-stu-id="d5578-144">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> <span data-ttu-id="d5578-145">Docker-avbildningen stöder inte [`component`-funktionen](/cli/azure/component).</span><span class="sxs-lookup"><span data-stu-id="d5578-145">The Docker image does not support the [`component` feature](/cli/azure/component).</span></span>
> <span data-ttu-id="d5578-146">Använd `docker run` för att installera den senaste avbildningen eller en specifik avbildning som du vill ha för att uppdatera Azure CLI 2.0.</span><span class="sxs-lookup"><span data-stu-id="d5578-146">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="apt-get"></a><span data-ttu-id="d5578-147">apt-get</span><span class="sxs-lookup"><span data-stu-id="d5578-147">apt-get</span></span>

<span data-ttu-id="d5578-148">Du kan installera Azure CLI 2.0 via `apt-get` på Debian/Ubuntu-baserade system.</span><span class="sxs-lookup"><span data-stu-id="d5578-148">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="d5578-149">Ändra listan med källor.</span><span class="sxs-lookup"><span data-stu-id="d5578-149">Modify your sources list.</span></span>

   - <span data-ttu-id="d5578-150">32-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="d5578-150">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="d5578-151">64-bitarssystem</span><span class="sxs-lookup"><span data-stu-id="d5578-151">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="d5578-152">Kör följande sudo-kommandon:</span><span class="sxs-lookup"><span data-stu-id="d5578-152">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="d5578-153">När du installerar med apt-get stöds inte `az component`.</span><span class="sxs-lookup"><span data-stu-id="d5578-153">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="d5578-154">Om du vill uppdatera CLI kör du `sudo apt-get update && sudo apt-get install azure-cli` igen.</span><span class="sxs-lookup"><span data-stu-id="d5578-154">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="d5578-155">Kör `sudo apt-get remove azure-cli` för att avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5578-155">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux-prerequisites"></a><span data-ttu-id="d5578-156">Linux-förutsättningar</span><span class="sxs-lookup"><span data-stu-id="d5578-156">Linux Prerequisites</span></span>

1. <span data-ttu-id="d5578-157">Om du inte har [Python](https://www.python.org/downloads) kan du installera det.</span><span class="sxs-lookup"><span data-stu-id="d5578-157">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="d5578-158">Installera de nödvändiga förutsättningarna beroende på vilken Linux-distribution du har.</span><span class="sxs-lookup"><span data-stu-id="d5578-158">Depending on your Linux distribution, install the prerequisites.</span></span>

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

## <a name="troubleshooting"></a><span data-ttu-id="d5578-159">Felsökning</span><span class="sxs-lookup"><span data-stu-id="d5578-159">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="d5578-160">Fel vid omdirigering av curl</span><span class="sxs-lookup"><span data-stu-id="d5578-160">Errors with curl redirection</span></span>

<span data-ttu-id="d5578-161">Om du får ett fel från `curl`-kommandot angående `-L`-parametern eller ett fel som hänvisar till "Object Moved" så kan du försöka använda en fullständig URL i stället för URL:en aka.ms:</span><span class="sxs-lookup"><span data-stu-id="d5578-161">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

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

## <a name="uninstall"></a><span data-ttu-id="d5578-162">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="d5578-162">Uninstall</span></span>

<span data-ttu-id="d5578-163">Om du använder skriptet på https://aka.ms/InstallAzureCli för att installera CLI kan du avinstallera det med dessa anvisningar.</span><span class="sxs-lookup"><span data-stu-id="d5578-163">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="d5578-164">Ta bort de installerade filerna.</span><span class="sxs-lookup"><span data-stu-id="d5578-164">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="d5578-165">Ta bort raden `<install location>/lib/azure-cli/az.completion` från `<install location>/.bash_profile`.</span><span class="sxs-lookup"><span data-stu-id="d5578-165">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="d5578-166">Standardplatsen för installation är `/Users/<username>`.</span><span class="sxs-lookup"><span data-stu-id="d5578-166">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="d5578-167">Om du använde apt-get, Docker eller msi för att installera CLI använder du samma verktyg för att avinstallera det.</span><span class="sxs-lookup"><span data-stu-id="d5578-167">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="d5578-168">Rapportera problem och feedback</span><span class="sxs-lookup"><span data-stu-id="d5578-168">Reporting issues and feedback</span></span>

<span data-ttu-id="d5578-169">Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-cli/issues)-delen av vårt GitHub-repo.</span><span class="sxs-lookup"><span data-stu-id="d5578-169">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="d5578-170">Om du vill ge feedback från kommandoraden kan du prova kommandot `az feedback`.</span><span class="sxs-lookup"><span data-stu-id="d5578-170">To provide feedback from the command line, try the `az feedback` command.</span></span>
