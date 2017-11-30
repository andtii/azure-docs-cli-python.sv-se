---
title: Installera Azure CLI 2.0 med yum
description: "Så här installerar du Azure CLI 2.0 med yum"
keywords: Azure CLI,Install Azure CLI,azure yum,azure rhel, azure fedora, azure centos
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: de695454c6f3109679b9eb9f6c0d77348d354518
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="1a5c7-104">Installera Azure CLI 2.0 med yum</span><span class="sxs-lookup"><span data-stu-id="1a5c7-104">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="1a5c7-105">Om du kör en distribution där `yum` ingår, till exempel RHEL, Fedora eller CentOS, så finns det ett paket för Azure CLI som du kan installera i systemet.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-105">If you are running a distirbution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="1a5c7-106">Du måste ha Python 2.7.x eller Python 3.x för att kunna använda CLI.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="1a5c7-107">Om distributionen inte har ett paket för någon av dessa kan du [installera Python](https://www.python.org/downloads/).</span><span class="sxs-lookup"><span data-stu-id="1a5c7-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="1a5c7-108">Installera</span><span class="sxs-lookup"><span data-stu-id="1a5c7-108">Install</span></span> 

1. <span data-ttu-id="1a5c7-109">Importera nyckeln för Microsoft-lagringsplatsen:</span><span class="sxs-lookup"><span data-stu-id="1a5c7-109">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="1a5c7-110">Skapa information om lokal `azure-cli`-lagringsplats:</span><span class="sxs-lookup"><span data-stu-id="1a5c7-110">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="1a5c7-111">Uppdatera `yum`-paketindexet och installera:</span><span class="sxs-lookup"><span data-stu-id="1a5c7-111">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="1a5c7-112">Kör Azure CLI med kommandot `az`.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-112">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="1a5c7-113">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="1a5c7-113">Update</span></span>

<span data-ttu-id="1a5c7-114">Uppdatera Azure CLI med kommandot `yum update`.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="1a5c7-115">Avinstallera</span><span class="sxs-lookup"><span data-stu-id="1a5c7-115">Uninstall</span></span>

<span data-ttu-id="1a5c7-116">Vi tycker det är tråkigt om du väljer att avinstallera Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-116">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="1a5c7-117">Använd kommandot `az feedback` för att ange några orsaker till varför du har valt att avinstallera och ge exempel på hur vi kan förbättra CLI-upplevelsen innan du avinstallerar.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-117">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="1a5c7-118">Vi vill se till att Azure CLI är så felfritt och användarvänligt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-118">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="1a5c7-119">Du kan även [skicka in ett github-ärende](https://github.com/Azure/azure-cli/issues).</span><span class="sxs-lookup"><span data-stu-id="1a5c7-119">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="1a5c7-120">Ta bort paketet från datorn.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-120">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="1a5c7-121">Ta bort lagringsinformationen om du inte tänker installera om CLI.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-121">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="1a5c7-122">Om du har tagit bort lagringsinformationen ska du också ta bort Microsoft GPG-signaturnyckeln.</span><span class="sxs-lookup"><span data-stu-id="1a5c7-122">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
