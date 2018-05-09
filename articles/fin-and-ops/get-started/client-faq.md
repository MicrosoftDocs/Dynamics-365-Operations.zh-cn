---
title: "Finance and Operations 客户端常见问题"
description: "本文提供对有关 Microsoft Dynamics 365 for Finance and Operations 客户端的常见问题的解答。"
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e1ee88c916890e26edc1c49aa2337749762a7cc7
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="finance-and-operations-client-faq"></a><span data-ttu-id="f2c47-103">Finance and Operations 客户端常见问题</span><span class="sxs-lookup"><span data-stu-id="f2c47-103">Finance and Operations client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2c47-104">本文提供对有关 Microsoft Dynamics 365 for Finance and Operations 客户端的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="f2c47-104">This article provides answers to frequently asked questions about the Microsoft Dynamics 365 for Finance and Operations client.</span></span>

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a><span data-ttu-id="f2c47-105">为何我在使用 Finance and Operations 时未加载符号？</span><span class="sxs-lookup"><span data-stu-id="f2c47-105">Why aren't symbols loaded when I use Finance and Operations?</span></span>
-----------------------------------------------------------------

<span data-ttu-id="f2c47-106">您的浏览器上的安全设置可能阻止了符号正确加载。</span><span class="sxs-lookup"><span data-stu-id="f2c47-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="f2c47-107">要解决此问题，请尝试执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="f2c47-107">To resolve this issue, try the following steps:</span></span>

-   <span data-ttu-id="f2c47-108">如果在 Internet Explorer 中遇到了此问题，请单击**工具**，然后单击 **Internet 选项**。</span><span class="sxs-lookup"><span data-stu-id="f2c47-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span>  <span data-ttu-id="f2c47-109">在“Internet 选项”对话框中的**隐私**选项卡上，单击**自定义级别**，然后确保已选中**字体下载**选项。</span><span class="sxs-lookup"><span data-stu-id="f2c47-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
-   <span data-ttu-id="f2c47-110">否则，您可能必须将 Finance and Operations 站点添加到受信任站点的列表。</span><span class="sxs-lookup"><span data-stu-id="f2c47-110">Otherwise, you might have to add the Finance and Operations site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="f2c47-111">我的 Dynamics AX 2012 中没有功能区。</span><span class="sxs-lookup"><span data-stu-id="f2c47-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="f2c47-112">我是否能将“操作窗格”上的选项卡一直保持在打开状态？</span><span class="sxs-lookup"><span data-stu-id="f2c47-112">Can I keep Action Pane tabs open all the time?</span></span>
<span data-ttu-id="f2c47-113">我们计划很快实现此功能。</span><span class="sxs-lookup"><span data-stu-id="f2c47-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="f2c47-114">用户随后将能够选择一直将“操作窗格”上的选项卡保持在打开状态。</span><span class="sxs-lookup"><span data-stu-id="f2c47-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="f2c47-115">如果不这样选择，这些选项卡在不使用时将被折叠，以便为页面腾出更多的屏幕空间。</span><span class="sxs-lookup"><span data-stu-id="f2c47-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="f2c47-116">为何我有时候在右键单击时看到不同的快捷菜单？</span><span class="sxs-lookup"><span data-stu-id="f2c47-116">Why do I sometimes see different shortcut menus when I right click?</span></span>
<span data-ttu-id="f2c47-117">如果您右键单击了可编辑字段（或者选择了文本），则会显示浏览器的快捷菜单。</span><span class="sxs-lookup"><span data-stu-id="f2c47-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="f2c47-118">此菜单使您可以访问**“剪切”**、**“复制”**和**“粘贴”**命令。</span><span class="sxs-lookup"><span data-stu-id="f2c47-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="f2c47-119">我们无法将这些命令嵌入到 Finance and Operations 快捷菜单中，因为出于安全原因，浏览器不允许我们以编程方式访问系统剪贴板。</span><span class="sxs-lookup"><span data-stu-id="f2c47-119">We can't embed these commands into the Finance and Operations shortcut menus because, for security reasons, browsers don’t allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="f2c47-120">如果您右键单击字段标签或右键单击只读控件的值，则会看到 Finance and Operations 快捷菜单。</span><span class="sxs-lookup"><span data-stu-id="f2c47-120">If you right-click a field label or the value of a read-only control, you'll see the Finance and Operations shortcut menu.</span></span>

<span data-ttu-id="f2c47-121">为了使键盘访问更加容易，我们计划在将来实施可打开 Finance and Operations 快捷菜单的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f2c47-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the Finance and Operations shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a><span data-ttu-id="f2c47-122">Finance and Operations 中的“查看详细信息”功能在何处？</span><span class="sxs-lookup"><span data-stu-id="f2c47-122">Where is the View details functionality in Finance and Operations?</span></span>
<span data-ttu-id="f2c47-123">**“查看详细信息”**选项可通过两种方式访问：</span><span class="sxs-lookup"><span data-stu-id="f2c47-123">The **View details** option is available in a couple of ways:</span></span>

-   <span data-ttu-id="f2c47-124">如果某个控件拥有**“查看详细信息”**功能，并且该控件具有值，该值将显示为超链接。</span><span class="sxs-lookup"><span data-stu-id="f2c47-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="f2c47-125">您可以单击超链接以打开包含其他详细信息的页面。</span><span class="sxs-lookup"><span data-stu-id="f2c47-125">You can click the hyperlink to open a page that contains additional details.</span></span>
-   <span data-ttu-id="f2c47-126">**查看详细信息**也是 Finance and Operations 快捷菜单上的选项。</span><span class="sxs-lookup"><span data-stu-id="f2c47-126">**View details** is also an option on Finance and Operations shortcut menus.</span></span> <span data-ttu-id="f2c47-127">有关在右键单击后何时显示 Finance and Operations 快捷菜单的详细信息，请参阅上一节。</span><span class="sxs-lookup"><span data-stu-id="f2c47-127">For more information about when Finance and Operations shortcut menus are displayed when you right-click, see the previous section.</span></span>





