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
ms.openlocfilehash: 930073324d68f9719ce5035388120e7b6ac41a98
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/18/2017
---
# <a name="using-extensions-with-the-azure-cli-20"></a>Använda tillägg med Azure CLI 2.0

Tillägg är enskilda moduler som inte levereras med själva Azure CLI och som gör att du kan lägga till funktioner via nya kommandon. Detta kan vara experimentella versioner eller förhandsversioner, särskilda verktyg som Microsoft har för dina behov, eller till och med tillägg som du har skrivit själv. Tillägg möjliggör viss flexibilitet med CLI så att du kan ändra det efter dina behov, utan att behöva skicka en massa extra paket som inte anses vara en del av grundfunktionsuppsättningen.

Den här artikeln hjälper dig att förstå hur du installerar, uppdaterar och tar bort tillägg för CLI. Den bör också besvara vanliga frågor om tilläggens funktioner.

## <a name="finding-extensions"></a>Hitta tillägg

Om du vill veta vilka tillägg som finns tillgängliga kan du använda `az extension list-available`. Det här kommandot visar de tillgängliga officiella tillägg som tillhandahålls och stöds av Microsoft.

## <a name="installing-extensions"></a>Installera tillägg

När du har hittat ett tillägg som du vill installera använder du `az extension add` för att hämta det. Om tillägget är ett officiellt Microsoft-tillägg som finns i listan i `az extension list-available` kan du installera tillägget efter dess namn.

```azurecli
az extension add --name <extension-name>
```

Om tillägget kommer från en extern resurs eller om du har en direktlänk till det kan du ange käll-URL eller lokal sökväg. Detta _måste_ vara en kompilerad Python WHL-fil.

```azurecli
az extension add --source <URL-or-path>
```

När du har installerat ett tillägg finns det under värdet för `$AZURE_EXTENSION_DIR`-gränssnittsvariabeln. Om den här variabeln är odefinierad blir värdet som standard `$HOME/.azure/cliextensions` på Linux och macOS, och `%USERPROFILE%\.azure\cliextensions` på Windows.

## <a name="updating-extensions"></a>Uppdatera tillägg

Tillägg kan bara uppdateras efter namnet:

```azurecli
az extension update --name <extension-name>
```

Installera om tillägget för att uppdatera det om ett tilläggsnamn av någon orsak inte kan lösas av CLI. Det kan också hända att tillägget inte längre är en förhandsversion och har blivit ett inbyggt kommando för CLI. I så fall uppdaterar du CLI och avinstallerar tillägget.

## <a name="uninstalling-extensions"></a>Avinstallera tillägg

Om du inte längre behöver ett tillägg går det att ta bort det med `az extension remove`.

```azurecli
az extension remove --name <extension-name>
```

Du kan även ta bort ett tillägg manuellt genom att ta bort det från den plats där det har installerats. Det här är värdet för `$AZURE_EXTENSION_DIR`-gränssnittsvariabeln. Om den här variabeln är odefinierad blir värdet som standard `$HOME/.azure/cliextensions` på Linux och macOS, och `%USERPROFILE%\.azure\cliextensions` på Windows.

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

Vi rekommenderar att du avinstallerar med `az extension remove`.

## <a name="faq"></a>VANLIGA FRÅGOR OCH SVAR

Följande är några svar på andra vanliga frågor om CLI-tillägg.

### <a name="what-file-formats-are-allowed-for-installation"></a>Vilka filformat är tillåtna för installation?

För närvarande kan endast kompilerade Python WHL-filer installeras som tillägg.

### <a name="can-extensions-replace-existing-commands"></a>Kan tillägg ersätta befintliga kommandon?

Ja. Tillägg kan ersätta befintliga kommandon, men innan du kör ett kommando som har ersatts kommer CLI att visa en varning.

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a>Hur vet jag om ett tillägg är en förhandsversion?

I tilläggets egen dokumentation och version bör det synas om det är en förhandsversion. Det är också vanligt att Microsoft släpper kommandon som är förhandsversioner för CLI som tillägg, där planen är att lägga till dem i det huvudsakliga CLI-gränssnittet när produkten inte längre är en förhandsversion.

### <a name="can-extensions-depend-upon-each-other"></a>Kan tillägg vara beroende av varandra?

Nej. Tillägg måste vara enskilda paket som inte förlitar sig på varandra. Det beror på att CLI inte ger någon garanti om när tillägg läses in, så det går inte att garantera att beroenden uppfylls. När ett tillägg installeras är det bara det tillägget som installeras, och det bör fortsätta att fungera även om du tar bort andra tillägg.

### <a name="are-extensions-updated-along-with-the-cli"></a>Uppdateras tillägg tillsammans med CLI?

Nej. Tillägg måste uppdateras separat, enligt beskrivningen i avsnittet [Uppdatera tillägg](#updating-extensions).
