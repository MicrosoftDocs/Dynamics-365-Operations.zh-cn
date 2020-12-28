---
title: 客户端常见问题
description: 本文提供对有关 Finance and Operations 客户端的常见问题的解答。
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1925c23891a637ba9e9666538323274819692a06
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692910"
---
# <a name="client-faq"></a><span data-ttu-id="fe29b-103">客户端常见问题解答</span><span class="sxs-lookup"><span data-stu-id="fe29b-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe29b-104">本文提供对有关 Finance and Operations 客户端的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="fe29b-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="fe29b-105">符号为何未加载？</span><span class="sxs-lookup"><span data-stu-id="fe29b-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="fe29b-106">您的浏览器上的安全设置可能阻止了符号正确加载。</span><span class="sxs-lookup"><span data-stu-id="fe29b-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="fe29b-107">要解决此问题，请尝试执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="fe29b-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="fe29b-108">如果在 Internet Explorer 中遇到了此问题，请单击 **工具**，然后单击 **Internet 选项**。</span><span class="sxs-lookup"><span data-stu-id="fe29b-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="fe29b-109">在“Internet 选项”对话框中的 **隐私** 选项卡上，单击 **自定义级别**，然后确保已选中 **字体下载** 选项。</span><span class="sxs-lookup"><span data-stu-id="fe29b-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="fe29b-110">否则，您可能必须将应用站点添加受信任站点的列表。</span><span class="sxs-lookup"><span data-stu-id="fe29b-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="fe29b-111">我的 Dynamics AX 2012 中没有功能区。</span><span class="sxs-lookup"><span data-stu-id="fe29b-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="fe29b-112">我是否能将“操作窗格”上的选项卡一直保持在打开状态？</span><span class="sxs-lookup"><span data-stu-id="fe29b-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="fe29b-113">我们计划很快实现此功能。</span><span class="sxs-lookup"><span data-stu-id="fe29b-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="fe29b-114">用户随后将能够选择一直将“操作窗格”上的选项卡保持在打开状态。</span><span class="sxs-lookup"><span data-stu-id="fe29b-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="fe29b-115">如果不这样选择，这些选项卡在不使用时将被折叠，以便为页面腾出更多的屏幕空间。</span><span class="sxs-lookup"><span data-stu-id="fe29b-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="fe29b-116">为何我有时候在右键单击时看到不同的快捷菜单？</span><span class="sxs-lookup"><span data-stu-id="fe29b-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="fe29b-117">如果您右键单击了可编辑字段（或者选择了文本），则会显示浏览器的快捷菜单。</span><span class="sxs-lookup"><span data-stu-id="fe29b-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="fe29b-118">此菜单使您可以访问 **剪切**、**复制** 和 **粘贴** 命令。</span><span class="sxs-lookup"><span data-stu-id="fe29b-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="fe29b-119">我们无法将这些命令嵌入到快捷菜单中，因为出于安全原因，浏览器不允许我们以编程方式访问系统剪贴板。</span><span class="sxs-lookup"><span data-stu-id="fe29b-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="fe29b-120">如果您右键单击字段标签或右键单击只读控件的值，则会看到快捷菜单。</span><span class="sxs-lookup"><span data-stu-id="fe29b-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="fe29b-121">为了使键盘访问更加容易，我们计划在将来实施可打开快捷菜单的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe29b-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="fe29b-122">“查看详细信息”功能在何处？</span><span class="sxs-lookup"><span data-stu-id="fe29b-122">Where is the View details functionality?</span></span>

<span data-ttu-id="fe29b-123">**查看详细信息** 选项可通过两种方式访问：</span><span class="sxs-lookup"><span data-stu-id="fe29b-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="fe29b-124">如果某个控件拥有 **查看详细信息** 功能，并且该控件具有值，该值将显示为超链接。</span><span class="sxs-lookup"><span data-stu-id="fe29b-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="fe29b-125">您可以单击超链接以打开包含其他详细信息的页面。</span><span class="sxs-lookup"><span data-stu-id="fe29b-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="fe29b-126">**查看详细信息** 还是快捷菜单上的选项。</span><span class="sxs-lookup"><span data-stu-id="fe29b-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="fe29b-127">有关在右击单击后何时显示快捷菜单的详细信息，请参阅上一节。</span><span class="sxs-lookup"><span data-stu-id="fe29b-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>
