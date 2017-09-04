---
title: Logga in med Azure CLI 2.0
description: "Logga in med Azure 2.0 CLI på Linux, Mac eller Windows."
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
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: fea893ebd55811527e0e92375ffc081a52cdbb57
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: sv-SE
---
# <a name="log-in-with-azure-cli-20"></a><span data-ttu-id="1cfdc-104">Logga in med Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="1cfdc-104">Log in with Azure CLI 2.0</span></span>

<span data-ttu-id="1cfdc-105">Du kan logga in och autentisera med Azure CLI på flera olika sätt.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-105">There are several ways to log in and authenticate with the Azure CLI.</span></span> <span data-ttu-id="1cfdc-106">Det är enklast att komma igång genom att logga in interaktivt via webbläsaren eller att logga in på kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-106">The simplest way to get started is to log in interactively through your browser, or to log in at the command line.</span></span> <span data-ttu-id="1cfdc-107">Den rekommenderade metoden är att använda huvudnamn för tjänsten, vilket gör det möjligt för dig att skapa icke-interaktiva konton som du kan använda för att manipulera resurser.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-107">Our recommended approach is to use service principals, which provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="1cfdc-108">Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem lämplig behörighet som krävs för ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-108">By granting just the appropriate permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="1cfdc-109">Kommandon som du kör med CLI körs mot standardprenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-109">Commands that you run with the CLI are run against your default subscription.</span></span>  <span data-ttu-id="1cfdc-110">Om du har mer än en prenumeration kanske du behöver [bekräfta din standardprenumeration](manage-azure-subscriptions-azure-cli.md) och ändra den efter behov.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-110">If you have more than one subscription, you may want to [confirm your default subscription](manage-azure-subscriptions-azure-cli.md) and change it appropriately.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="1cfdc-111">Interaktiv inloggning</span><span class="sxs-lookup"><span data-stu-id="1cfdc-111">Interactive log-in</span></span>

<span data-ttu-id="1cfdc-112">Logga in interaktivt från din webbläsare.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-112">Log in interactively from your web browser.</span></span>

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a><span data-ttu-id="1cfdc-113">Kommandorad</span><span class="sxs-lookup"><span data-stu-id="1cfdc-113">Command line</span></span>

<span data-ttu-id="1cfdc-114">Ange dina autentiseringsuppgifter på kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-114">Provide your credentials on the command line.</span></span>

> [!Note]
> <span data-ttu-id="1cfdc-115">Den här metoden fungerar inte med Microsoft-konton eller konton som har tvåfaktorsautentisering aktiverad.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-115">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a><span data-ttu-id="1cfdc-116">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="1cfdc-116">Logging in with a service principal</span></span>

<span data-ttu-id="1cfdc-117">Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-117">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span>
<span data-ttu-id="1cfdc-118">Autentisering med tjänstens huvudnamn är det bästa sätt att säkra användningen av dina Azure-resurser från antingen dina skript eller program som manipulerar resurser.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-118">Authenticating with a service principal is the best way to secure the usage of your Azure resources from either your scripts or applications that manipulate resources.</span></span>
<span data-ttu-id="1cfdc-119">Du definierar de roller du vill använda via `az role`-uppsättningen med kommandon.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-119">You define the roles you want your users to have via the `az role` set of commands.</span></span>
<span data-ttu-id="1cfdc-120">Du kan läsa mer och se exempel på roller för tjänstens huvudnamn i våra [referensartiklar om az-roller](https://docs.microsoft.com/cli/azure/role.md).</span><span class="sxs-lookup"><span data-stu-id="1cfdc-120">You can learn more and see examples of service principal roles in our [az role reference articles](https://docs.microsoft.com/cli/azure/role.md).</span></span>

1. <span data-ttu-id="1cfdc-121">Om du inte redan har ett huvudnamn för tjänsten kan du [skapa ett](create-an-azure-service-principal-azure-cli.md).</span><span class="sxs-lookup"><span data-stu-id="1cfdc-121">If you don't already have a service principal, [create one](create-an-azure-service-principal-azure-cli.md).</span></span>

1. <span data-ttu-id="1cfdc-122">Logga in med huvudnamnet för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-122">Log in with the service principal.</span></span>

   ```azurecli
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   <span data-ttu-id="1cfdc-123">För att få din klient loggar du in interaktivt och sedan hämtar du klienten från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="1cfdc-123">To get your tenant, log in interactively and then get the tenantId from your subscription.</span></span>

   ```azurecli
   az login
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```