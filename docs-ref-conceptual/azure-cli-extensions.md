---
title: "Azure CLI 2.0-tillägg"
description: "Använda tillägg med Azure CLI 2.0"
keywords: Azure CLI, Extensions
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a76e58c4430a184d133cca0ef0623f325aeb2f27
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/06/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="17f94-104">Använda tillägg med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="17f94-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="17f94-105">Tillägg är enskilda moduler som inte levereras med själva Azure CLI och som gör att du kan lägga till funktioner via nya kommandon.</span><span class="sxs-lookup"><span data-stu-id="17f94-105">Extensions are individual modules not shipped with the Azure CLI itself that allow you to add functionality through new commands.</span></span> <span data-ttu-id="17f94-106">Detta kan vara experimentella versioner eller förhandsversioner, särskilda verktyg som Microsoft har för dina behov, eller till och med tillägg som du har skrivit själv.</span><span class="sxs-lookup"><span data-stu-id="17f94-106">These might be experimental or pre-release offerings, specialized tools that Microsoft has for your needs, or even extensions that you yourself have written.</span></span> <span data-ttu-id="17f94-107">Tillägg möjliggör viss flexibilitet med CLI så att du kan ändra det efter dina behov, utan att behöva skicka en massa extra paket som inte anses vara en del av grundfunktionsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="17f94-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="17f94-108">Den här artikeln hjälper dig att förstå hur du installerar, uppdaterar och tar bort tillägg för CLI.</span><span class="sxs-lookup"><span data-stu-id="17f94-108">This article will help you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="17f94-109">Den bör också besvara vanliga frågor om tilläggens funktioner.</span><span class="sxs-lookup"><span data-stu-id="17f94-109">It should also answer common questions about extension behavior.</span></span>

## <a name="finding-extensions"></a><span data-ttu-id="17f94-110">Hitta tillägg</span><span class="sxs-lookup"><span data-stu-id="17f94-110">Finding extensions</span></span>

<span data-ttu-id="17f94-111">Om du vill veta vilka tillägg som finns tillgängliga kan du använda `az extension list-available`.</span><span class="sxs-lookup"><span data-stu-id="17f94-111">In order to know what extensions are available, you can use `az extension list-available`.</span></span> <span data-ttu-id="17f94-112">Det här kommandot visar de tillgängliga officiella tillägg som tillhandahålls och stöds av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17f94-112">This command lists the available, official extensions which are provided and supported by Microsoft.</span></span>

## <a name="installing-extensions"></a><span data-ttu-id="17f94-113">Installera tillägg</span><span class="sxs-lookup"><span data-stu-id="17f94-113">Installing extensions</span></span>

<span data-ttu-id="17f94-114">När du har hittat ett tillägg som du vill installera använder du `az extension add` för att hämta det.</span><span class="sxs-lookup"><span data-stu-id="17f94-114">Once you have found an extension to install, use `az extension add` to get it.</span></span> <span data-ttu-id="17f94-115">Om tillägget är ett officiellt Microsoft-tillägg som finns i listan i `az extension list-available` kan du installera tillägget efter dess namn.</span><span class="sxs-lookup"><span data-stu-id="17f94-115">If the extension is an official Microsoft extension listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli
az extension add --name <extension-name>
```

<span data-ttu-id="17f94-116">Om tillägget kommer från en extern resurs eller om du har en direktlänk till det kan du ange käll-URL eller lokal sökväg.</span><span class="sxs-lookup"><span data-stu-id="17f94-116">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="17f94-117">Detta _måste_ vara en kompilerad Python WHL-fil.</span><span class="sxs-lookup"><span data-stu-id="17f94-117">This _must_ be a compiled Python wheel file.</span></span>

```azurecli
az extension add --source <URL-or-path>
```

<span data-ttu-id="17f94-118">När du har installerat ett tillägg finns det under värdet för `$AZURE_EXTENSION_DIR`-gränssnittsvariabeln.</span><span class="sxs-lookup"><span data-stu-id="17f94-118">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="17f94-119">Om den här variabeln är odefinierad blir värdet som standard `$HOME/.azure/cliextensions` på Linux och macOS, och `%USERPROFILE%\.azure\cliextensions` på Windows.</span><span class="sxs-lookup"><span data-stu-id="17f94-119">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="updating-extensions"></a><span data-ttu-id="17f94-120">Uppdatera tillägg</span><span class="sxs-lookup"><span data-stu-id="17f94-120">Updating extensions</span></span>

<span data-ttu-id="17f94-121">Tillägg kan bara uppdateras efter namnet:</span><span class="sxs-lookup"><span data-stu-id="17f94-121">Extensions can only be updated by name:</span></span>

```azurecli
az extension update --name <extension-name>
```

<span data-ttu-id="17f94-122">Installera om tillägget för att uppdatera det om ett tilläggsnamn av någon orsak inte kan lösas av CLI.</span><span class="sxs-lookup"><span data-stu-id="17f94-122">If an extension name cannot be resolved by the CLI for whatever reason, reinstall the extension to update it.</span></span> <span data-ttu-id="17f94-123">Det kan också hända att tillägget inte längre är en förhandsversion och har blivit ett inbyggt kommando för CLI.</span><span class="sxs-lookup"><span data-stu-id="17f94-123">There is also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="17f94-124">I så fall uppdaterar du CLI och avinstallerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="17f94-124">In that case, update the CLI and uninstall the extension.</span></span>

## <a name="uninstalling-extensions"></a><span data-ttu-id="17f94-125">Avinstallera tillägg</span><span class="sxs-lookup"><span data-stu-id="17f94-125">Uninstalling extensions</span></span>

<span data-ttu-id="17f94-126">Om du inte längre behöver ett tillägg går det att ta bort det med `az extension remove`.</span><span class="sxs-lookup"><span data-stu-id="17f94-126">If you no longer need an extension, it can be removed with `az extension remove`,</span></span>

```azurecli
az extension remove --name <extension-name>
```

<span data-ttu-id="17f94-127">Du kan även ta bort ett tillägg manuellt genom att ta bort det från den plats där det har installerats.</span><span class="sxs-lookup"><span data-stu-id="17f94-127">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="17f94-128">Det här är värdet för `$AZURE_EXTENSION_DIR`-gränssnittsvariabeln.</span><span class="sxs-lookup"><span data-stu-id="17f94-128">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="17f94-129">Om den här variabeln är odefinierad blir värdet som standard `$HOME/.azure/cliextensions` på Linux och macOS, och `%USERPROFILE%\.azure\cliextensions` på Windows.</span><span class="sxs-lookup"><span data-stu-id="17f94-129">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="17f94-130">Vi rekommenderar att du avinstallerar med `az extension remove`.</span><span class="sxs-lookup"><span data-stu-id="17f94-130">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="17f94-131">VANLIGA FRÅGOR OCH SVAR</span><span class="sxs-lookup"><span data-stu-id="17f94-131">FAQ</span></span>

<span data-ttu-id="17f94-132">Följande är några svar på andra vanliga frågor om CLI-tillägg.</span><span class="sxs-lookup"><span data-stu-id="17f94-132">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="17f94-133">Vilka filformat är tillåtna för installation?</span><span class="sxs-lookup"><span data-stu-id="17f94-133">What file formats are allowed for installation?</span></span>

<span data-ttu-id="17f94-134">För närvarande kan endast kompilerade Python WHL-filer installeras som tillägg.</span><span class="sxs-lookup"><span data-stu-id="17f94-134">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="17f94-135">Kan tillägg ersätta befintliga kommandon?</span><span class="sxs-lookup"><span data-stu-id="17f94-135">Can extensions replace existing commands?</span></span>

<span data-ttu-id="17f94-136">Ja.</span><span class="sxs-lookup"><span data-stu-id="17f94-136">Yes.</span></span> <span data-ttu-id="17f94-137">Tillägg kan ersätta befintliga kommandon, men innan du kör ett kommando som har ersatts kommer CLI att visa en varning.</span><span class="sxs-lookup"><span data-stu-id="17f94-137">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="17f94-138">Hur vet jag om ett tillägg är en förhandsversion?</span><span class="sxs-lookup"><span data-stu-id="17f94-138">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="17f94-139">I tilläggets egen dokumentation och version bör det synas om det är en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="17f94-139">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="17f94-140">Det är också vanligt att Microsoft släpper kommandon som är förhandsversioner för CLI som tillägg, där planen är att lägga till dem i det huvudsakliga CLI-gränssnittet när produkten inte längre är en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="17f94-140">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="17f94-141">Kan tillägg vara beroende av varandra?</span><span class="sxs-lookup"><span data-stu-id="17f94-141">Can extensions depend upon each other?</span></span>

<span data-ttu-id="17f94-142">Nej.</span><span class="sxs-lookup"><span data-stu-id="17f94-142">No.</span></span> <span data-ttu-id="17f94-143">Tillägg måste vara enskilda paket som inte förlitar sig på varandra.</span><span class="sxs-lookup"><span data-stu-id="17f94-143">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="17f94-144">Det beror på att CLI inte ger någon garanti om när tillägg läses in, så det går inte att garantera att beroenden uppfylls.</span><span class="sxs-lookup"><span data-stu-id="17f94-144">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="17f94-145">När ett tillägg installeras är det bara det tillägget som installeras, och det bör fortsätta att fungera även om du tar bort andra tillägg.</span><span class="sxs-lookup"><span data-stu-id="17f94-145">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="17f94-146">Uppdateras tillägg tillsammans med CLI?</span><span class="sxs-lookup"><span data-stu-id="17f94-146">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="17f94-147">Nej.</span><span class="sxs-lookup"><span data-stu-id="17f94-147">No.</span></span> <span data-ttu-id="17f94-148">Tillägg måste uppdateras separat, enligt beskrivningen i avsnittet [Uppdatera tillägg](#updating-extensions).</span><span class="sxs-lookup"><span data-stu-id="17f94-148">Extensions must be updated separately, as described in the [Updating extensions](#updating-extensions) section.</span></span>
