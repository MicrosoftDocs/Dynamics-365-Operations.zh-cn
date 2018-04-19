---
title: "扩展 Microsoft Dynamics 365 for Talent 的功能"
description: "如果您创建了任何 Microsoft PowerApps，您可以从 Microsoft Dynamics 365 for Talent 内的链接启动那些应用程序。"
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fbd5335f64865dfe6122d88b3bc45ec614fc0677
ms.openlocfilehash: c01a8f0106ee1181e973da50d428b8fc5e6e5a06
ms.contentlocale: zh-cn
ms.lasthandoff: 04/19/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="c68a7-103">扩展 Microsoft Dynamics 365 for Talent 的功能</span><span class="sxs-lookup"><span data-stu-id="c68a7-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="c68a7-104">如果您创建了任何 Microsoft PowerApps，您可以从 Microsoft Dynamics 365 for Talent 内的链接启动那些应用程序。</span><span class="sxs-lookup"><span data-stu-id="c68a7-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="c68a7-105">若要设置对您的应用程序的访问，您需要在可以从**系统管理**工作区打开的配置页面上设置 Talent 中的一些信息。</span><span class="sxs-lookup"><span data-stu-id="c68a7-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="c68a7-106">配置 Talent 内嵌入的 PowerApps</span><span class="sxs-lookup"><span data-stu-id="c68a7-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="c68a7-107">使用**设置嵌入的 Microsoft PowerApps** 页面来将 Talent 页面配置为启动 PowerApps 应用程序。</span><span class="sxs-lookup"><span data-stu-id="c68a7-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="c68a7-108">若要打开**设置嵌入的 Microsoft PowerApps** 页面，请打开**系统管理**工作区，然后打开**链接**选项卡。从**设置**组选择 **Microsoft PowerApps**。</span><span class="sxs-lookup"><span data-stu-id="c68a7-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="c68a7-109">以下信息在此页上输入或设置：</span><span class="sxs-lookup"><span data-stu-id="c68a7-109">The following information is entered or set on this page:</span></span> 

 -  <span data-ttu-id="c68a7-110">每个 PowerApps 应用程序的描述性名称或标识符。</span><span class="sxs-lookup"><span data-stu-id="c68a7-110">A descriptive name or identifier for each PowerApps application.</span></span>
 -  <span data-ttu-id="c68a7-111">您添加到 Talent 页面的每个应用程序的唯一标识符 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="c68a7-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="c68a7-112">应用 ID 在 PowerApps 网站 [powerapps.com](http://powerapps.com/) 上可用。</span><span class="sxs-lookup"><span data-stu-id="c68a7-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
 -  <span data-ttu-id="c68a7-113">用户可以打开应用程序或报表的页面。</span><span class="sxs-lookup"><span data-stu-id="c68a7-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="c68a7-114">并非所有 Talent 页面都支持嵌入的 PowerApps 和 Power BI 报表。</span><span class="sxs-lookup"><span data-stu-id="c68a7-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="c68a7-115">输入页面的内部名称，而不是在页面顶部出现的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c68a7-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="c68a7-116">若要找到内部名称，打开您需要其内部名称的页面，右键单击页面的任何位置。</span><span class="sxs-lookup"><span data-stu-id="c68a7-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="c68a7-117">在菜单打开时，悬停在**窗体信息**项上。</span><span class="sxs-lookup"><span data-stu-id="c68a7-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="c68a7-118">内部窗体名称显示在菜单中**窗体信息**项的旁边。</span><span class="sxs-lookup"><span data-stu-id="c68a7-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
-   <span data-ttu-id="c68a7-119">指定应用程序可以从中检索上下文数据的窗体控件。</span><span class="sxs-lookup"><span data-stu-id="c68a7-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="c68a7-120">例如，应用程序可以使用工作人员的相关数据。</span><span class="sxs-lookup"><span data-stu-id="c68a7-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="c68a7-121">如果您在**上下文**字段中输入**工作人员**页面，在您启动应用程序时**工作人员**页面将打开。</span><span class="sxs-lookup"><span data-stu-id="c68a7-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="c68a7-122">在**上下文字段**中的输入是可选的。</span><span class="sxs-lookup"><span data-stu-id="c68a7-122">An entry in the **Context field** is optional.</span></span> 
-   <span data-ttu-id="c68a7-123">设置 PowerApps 应用程序将在其中运行的对话框的大小。</span><span class="sxs-lookup"><span data-stu-id="c68a7-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="c68a7-124">对话框被指定为“小”或“大”以优化应用程序分别在手机或更大设备上运行时的用户界面。</span><span class="sxs-lookup"><span data-stu-id="c68a7-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 


<span data-ttu-id="c68a7-125">您还可以指定可使用应用程序的法人，或者您可以让其对所有法人可用。</span><span class="sxs-lookup"><span data-stu-id="c68a7-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="c68a7-126">默认情况下，您的 PowerApps 应用程序可供所有法人使用。</span><span class="sxs-lookup"><span data-stu-id="c68a7-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="c68a7-127">打开应用程序</span><span class="sxs-lookup"><span data-stu-id="c68a7-127">Opening an application</span></span>
<span data-ttu-id="c68a7-128">在配置了嵌入的 PowerApps 应用程序后，指向您指定的应用程序的链接将被添加到 Talent 内的页面。</span><span class="sxs-lookup"><span data-stu-id="c68a7-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="c68a7-129">单击一个链接打开一个应用程序。</span><span class="sxs-lookup"><span data-stu-id="c68a7-129">Click a link to open an application.</span></span> 



