---
title: "Kom igång med Azure CLI 2.0"
description: "Kom igång med Azure CLI 2.0 på Linux, Mac eller Windows."
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 11153c13fb9868897b0bb21dac9d64072c3af16e
ms.sourcegitcommit: 70c4d7a14591e5b761e261105cd2d376753f2a54
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2017
---
# <a name="get-started-with-azure-cli-20"></a>Kom igång med Azure CLI 2.0

Azure CLI 2.0 är Azures nya kommandoradsmiljö för att hantera Azure-resurser.
Du kan använda den i din webbläsare med [Azure Cloud Shell](/azure/cloud-shell/overview) eller [installera](install-azure-cli.md) den på macOS, Linux och Windows och köra den från kommandoraden.

Azure CLI 2.0 är optimerad för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager.
Den här artikeln hjälper dig att komma igång med att använda det och lär dig grundbegreppen bakom.

Information om den senaste versionen finns i [viktig information](release-notes-azure-cli.md).

## <a name="connect"></a>Anslut

Det enklaste sättet att komma igång är att [starta Cloud Shell](/azure/cloud-shell/quickstart).

1. Starta Cloud Shell från det övre navigeringsfältet i Azure Portal.

   ![Shell-ikon](media/get-started-with-azure-cli/shell-icon.png)

2. Välj den prenumeration du vill använda och skapa ett lagringskonto.

   ![skapar ett lagringskonto](media/get-started-with-azure-cli/storage-prompt.png)

Du kan även [installera](install-azure-cli.md) CLI och köra det lokalt från kommandoraden. När du har installerat CLI kör du `az login` för att logga in med din standardprenumeration.

## <a name="create-a-resource-group"></a>Skapa en resursgrupp

Nu när allt har konfigurerats ska vi använda Azure CLI för att skapa resurser i Azure.

Skapa först en resursgrupp.  Resursgrupper i Azure är ett sätt att hantera flera logiskt grupperade resurser.  Du kan till exempel skapa en resursgrupp för ett program eller projekt och lägga till en virtuell dator, en databas och en CDN-tjänst inom den.

Vi ska skapa en resursgrupp med namnet "MyResourceGroup" i regionen *westus2* för Azure.  Ange följande kommando:

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

När resursgruppen har skapas ger kommandot `az group create` flera egenskaper för den nyligen skapade resursen:

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a>Skapa en virtuell Linux-dator

Nu när vi har en resursgrupp kan vi skapa en virtuell Linux-dator i den.

Du kan skapa en virtuell Linux-dator med den populära UbuntuLTS-avbildningen med två anslutna lagringsdiskar på 10 GB och 20 GB med följande kommando:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

När du kör föregående kommando letar Azure CLI 2.0 efter ett SSH-nyckelpar som är lagrat under katalogen ~/.ssh.  Om du inte redan har ett SSH-nyckelpar lagrat där kan du be att Azure CLI automatiskt skapar en åt dig genom att skicka parametern --generate-ssh-keys:

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

Kommandot `az vm create` ger resultat när den virtuella datorn har skapats färdigt och är redo att nås och användas. Utdata innehåller flera egenskaper för den nyligen skapade virtuella datorn inklusive dess offentliga IP-adress:

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

Nu när den virtuella datorn har skapats kan du logga in på den nya virtuella Linux-datorn med hjälp av **SSH** med den offentliga IP-adressen för den virtuella dator du skapade:

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a>Skapa en virtuell Windows Server-dator

Nu ska vi skapa en Windows Server 2016 Datacenter-baserad virtuell dator med kommandot `az vm create` och lägga till den i samma ”MyResourceGroup”-resursgrupp som vi använde för vår virtuella Linux-dator.  Precis som i exemplet med den virtuella Linux-datorn ansluter vi två lagringsdiskar med parmetern `--data-disk-sizes-gb`.

Azure kräver att du undviker att använda användarnamn/lösenord som är lätta att lista ut. Det finns särskilda regler för vilka tecken som kan användas och minimilängd för både användarnamn och lösenord.  

> [!NOTE]
> Du ombeds ange ditt användarnamn och lösenord när du kör det här kommandot.

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

Kommandot `az vm create` ger resultat när den virtuella datorn har skapats färdigt och är redo att nås och användas.

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

Logga nu in på den virtuella Windows Server-dator som har skapats med hjälp av Fjärrskrivbord och den virtuella datorns offentliga IP-adress (som returneras i resultatet från `az vm create`).  
Om du använder ett Windows-baserat system kan du göra detta från kommandoraden med `mstsc`-kommandot:

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

Ange samma kombination av användarnamn/lösenord för att logga in som du använde när du skapade den virtuella datorn.

## <a name="creating-other-resources-in-azure"></a>Skapa andra resurser i Azure

Vi har nu gått igenom hur du skapar en resursgrupp, en virtuell Linux-dator och en virtuell Windows Server-dator. Du kan även skapa många andra typer av Azure-resurser.  

Alla nya resurser skapas med ett konsekvent `az <resource type name> create`-namngivningsmönster.  Om du till exempel vill skapa en belastningsutjämnare för Azure-nätverk som vi sedan kan koppla till de virtuella datorer vi precis har skapat kan vi använda följande kommando för att skapa:

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

Vi kan också skapa ett nytt privat virtuellt nätverk (som ofta kallas ett "VNet" i Azure) för infrastrukturen med följande kommando för skapande:

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

Det som gör Azure och Azure CLI så kraftfulla är att vi kan använda dem inte bara för att få molnbaserad infrastruktur, utan också för att skapa hanterade plattformstjänster.  De hanterade plattformstjänsterna kan också kombineras med infrastruktur för att skapa ännu mer kraftfulla lösningar.

Du kan till exempel använda Azure CLI för att skapa en Azure AppService.  Azure AppService är en hanterad plattformstjänst som ger ett utmärkt sätt att agera värd för webbappar utan att behöva bekymra sig över infrastruktur.  När du har skapat Azure AppService kan du skapa två nya Azure-webbappar i AppService med hjälp av följande kommandon för skapande:

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

När du förstår grunderna i `az <resource type name> create`-mönstret blir det lätt att skapa vad som helst. Här följer några populära Azure-resurstyper och motsvarande Azure CLI-create-kommandon för att skapa dem:

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

Besök [Referensdokumentation](/cli/azure) för att läsa om de ytterligare resursspecifika parametrarna du kan skicka till vart och ett av de föregående kommandona och resurstyperna du kan skapa. 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a>Användbart tips: Optimera skapandeåtgärder med hjälp av --no-wait

Som standard när du skapar resurser med Azure CLI 2.0 väntar kommandot `az <resource type name> create` tills resursen har skapats och är klar att användas.  Om du exempelvis skapar en virtuell dator returnerar inte kommandot `az vm create` som standard förrän den virtuella datorn är skapad och klar att användas med SSH eller RDP.

Vi använder den här metoden eftersom det gör det enklare att skriva automatiseringsskript som innehåller flera steg med beroenden (och som behöver ha en föregående uppgift slutförd innan det går att fortsätta).

Om du inte behöver vänta på att skapa en resurs innan du fortsätter kan du använda alternativet `no-wait` för att påbörja en skapandeåtgärd i bakgrunden. Du kan fortsätta att använda CLI:n för andra kommandon.

Till exempel startar följande användning av `az vm create` en VM-distribution och returnerar sedan mycket snabbare (och innan den virtuella datorn har startats fullständigt):

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

Med metoden `--no-wait` kan du få hjälp att optimera prestanda för dina automatiseringsskript avsevärt.

## <a name="listing-resources-and-formatting-output"></a>Lista över resurser och formatering av utdata

Du kan använda kommandot `list` i Azure CLI för att söka efter och lista de resurser som körs i Azure. 

Precis som med kommandot create kan du lista resurser med Azure CLI 2.0 med ett vanligt `az <resource type name> list`-namngivningsmönster som är konsekvent för alla resurstyper.  Det finns olika utdataformat och frågealternativ för att filtrera och sortera resurslistan som du önskar.

Till exempel visar `az vm list` listan över alla virtuella datorer du har.   

```azurecli-interactive
az vm list 
```
Värdena som returneras är som standard i JSON (visar endast partiella utdata för att hålla det kortfattat).

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...   
]
```

Du kan ändra utdataformat med alternativet `--output`.  Kör kommandot `az vm list` för att se både virtuella Linux- och Windows Server-datorer som skapats tidigare, tillsammans med de vanligaste egenskaperna hos en virtuell dator, med det lättlästa *tabellformatalternativet*:

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

Utdataalternativet *tsv* kan användas för att få textbaserade, tabbavgränsade utdata utan rubriker.  Det här formatet är praktiskt när du vill skicka utdata till något annat textbaserat verktyg som grep. 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
Läs artiklarna om [utdataformat](format-output-azure-cli.md) för att lära dig mer om fler sätt att lista resurser och formatera utdata.

## <a name="querying-resources-and-shaping-outputs"></a>Fråga efter resurser och bearbeta utdata

Ofta vill du kunna skicka frågor endast för de resurser som uppfyller ett visst villkor.  

Kommandot `list` har inbyggd support som gör det enkelt att filtrera resurser efter namnet på resursgruppen.  Du kan exempelvis skicka antingen en `--ResourceGroup`- eller `-g`-parameter till ett `list`-kommando för att endast hämta de resurserna i en specifik resursgrupp:


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

För ännu kraftfullare frågesupport kan du använda parametern `--query` för att uföra en JMESPath-fråga på resultatet för *valfritt* `az`-kommando.  Du kan använda JMESPath-frågor både för att filtrera och forma utdata från alla returnerade resultat.

Utför till exempel följande kommando för att söka efter en VM-resurs i en resursgrupp som innehåller bokstäverna "My":

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Vi kan sedan välja att förfina utdata genom att använda formningsfunktionerna för JMESPath-frågor för att också generera olika värden.  Till exempel hämtar följande kommando den typ av OS-disk som den virtuella datorn använder för att fastställa om operativsystemet är Linux- eller Windows-baserat:

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

JMESPath-stödet i Azure CLI är kraftfullt.  Mer information om hur du använder det finns i vår artikel om [frågor](query-azure-cli.md).

## <a name="deleting-resources"></a>Ta bort resurser

Du kan använda kommandona `delete` med Azure CLI för att ta bort de resurser du inte längre behöver. Du kan använda kommandot `delete` med vilken resurs som helst, precis som du kan med kommandot `create`.

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

Som standard uppmanar dig CLI att bekräfta borttagningen.  Du kan ignorera varningen för automatiserade skript.

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

Du kan också ta bort många resurser i taget med kommandot `delete`.  Följande kommando tar till exempel bort alla resurser i resursgruppen "MyResourceGroup" som vi har använt för alla exempel i denna handledning.

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a>Hämta exempel

Om du vill lära dig mer om att använda Azure CLI kan du ta en titt på våra vanligaste skript för [virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [webbappar](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) och [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).

## <a name="read-the-api-reference-docs"></a>Läs API-referensdokumenten

[API-referens](/cli/azure)

## <a name="get-help"></a>Få hjälp

Azure CLI har inbyggd hjälpdokumentation som matchar vår webbdokumentation som du kan köra från kommandoraden:

```azurecli-interactive
az [command-group [command]] -h
```

Om du till exempel vill se vilka kommandon och undergrupper som är tillgängliga för virtuella datorer använder du:

```azurecli-interactive
az vm -h
```

Om du vill få hjälp med kommandot för att skapa en virtuell dator använder du:

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a>Växla från Azure CLI 1.0

Om du redan vet hur du använder Azure CLI 1.0 (azure.js) kommer du att lägga märke till platser där kommandona inte riktigt är desamma.
Ibland är kommandon för att utföra en uppgift helt olika.
För att hjälpa dig att växla från Azure CLI 1.0 till Azure CLI 2.0 har vi startat den här [kommandomappningen](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).

## <a name="send-us-your-feedback"></a>Skicka feedback

```azurecli-interactive
az feedback
```
