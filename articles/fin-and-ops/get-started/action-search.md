---
title: "操作搜索"
description: "本文介绍了 Microsoft Dynamics 365 for Finance and Operations 中的操作搜索功能。 操作搜索可以帮助您在页面中找到操作并运行。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 960c715c487fbda5d93630327f07380e6d8fbd3c
ms.contentlocale: zh-cn
ms.lasthandoff: 12/18/2018

---

# <a name="action-search"></a><span data-ttu-id="b0b05-104">操作搜索</span><span class="sxs-lookup"><span data-stu-id="b0b05-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0b05-105">本文介绍了 Microsoft Dynamics 365 for Finance and Operations 中的操作搜索功能。</span><span class="sxs-lookup"><span data-stu-id="b0b05-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b0b05-106">操作搜索可以帮助您在页面中找到操作并运行。</span><span class="sxs-lookup"><span data-stu-id="b0b05-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="b0b05-107">简介</span><span class="sxs-lookup"><span data-stu-id="b0b05-107">Introduction</span></span>

<span data-ttu-id="b0b05-108">Microsoft Dynamics 365 for Finance and Operations 中的页面主要在操作窗格（页面顶部显示的标准操作窗格和页面各部分中显示的工具栏）中显示命令。</span><span class="sxs-lookup"><span data-stu-id="b0b05-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="b0b05-109">在以前版本中，“键提示”功能能够让您通过按下 Alt 键和一系列字母的方式快速访问“操作窗格”上的任何按钮。</span><span class="sxs-lookup"><span data-stu-id="b0b05-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="b0b05-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="b0b05-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="b0b05-111">但是，在 Finance and Operations 的最新版本中，“键提示”不再可用，已经替换为操作搜索功能。</span><span class="sxs-lookup"><span data-stu-id="b0b05-111">However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="b0b05-112">这一新的功能允许您迅速搜索和运行所有可见操作窗格中的按钮。</span><span class="sxs-lookup"><span data-stu-id="b0b05-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="b0b05-113">使用操作搜索</span><span class="sxs-lookup"><span data-stu-id="b0b05-113">Using action search</span></span>

<span data-ttu-id="b0b05-114">若要使用操作搜索功能，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b0b05-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="b0b05-115">在操作窗格上，单击**操作搜索**字段。</span><span class="sxs-lookup"><span data-stu-id="b0b05-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="b0b05-116">（**操作搜索**字段包含一个放大镜图标。）</span><span class="sxs-lookup"><span data-stu-id="b0b05-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="b0b05-117">键入您要运行的按钮的全部或部分名称。</span><span class="sxs-lookup"><span data-stu-id="b0b05-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="b0b05-118">您还可以使用按钮“路径”的字词进行搜索。</span><span class="sxs-lookup"><span data-stu-id="b0b05-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="b0b05-119">（有关详细信息，请参阅本文的下一个部分。）通常，在您键入了两个到四个字符后，按钮将出现在结果列表的顶部附近。</span><span class="sxs-lookup"><span data-stu-id="b0b05-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="b0b05-120">在结果列表中查找和运行按钮（通过使用您的鼠标或键盘）。</span><span class="sxs-lookup"><span data-stu-id="b0b05-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="b0b05-121">该按钮运行后，焦点返回到您在页面的最后一个位置，以便您可以继续工作。</span><span class="sxs-lookup"><span data-stu-id="b0b05-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="b0b05-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="b0b05-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="b0b05-123">您还可以通过按 Ctrl+/ 或 Alt+Q 开始操作搜索。</span><span class="sxs-lookup"><span data-stu-id="b0b05-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="b0b05-124">再次按键盘快捷方式将焦点返回到您在页面上的最后一个位置。</span><span class="sxs-lookup"><span data-stu-id="b0b05-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="b0b05-125">了解结果列表</span><span class="sxs-lookup"><span data-stu-id="b0b05-125">Understanding the results list</span></span>

<span data-ttu-id="b0b05-126">通常，在 Finance and Operations 中，必须知道按钮的位置和环境以充分了解该按钮的用途。</span><span class="sxs-lookup"><span data-stu-id="b0b05-126">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="b0b05-127">因此，每个物料的附加信息将显示在结果列表，可帮助您确切了解哪些按钮出现在列表中。</span><span class="sxs-lookup"><span data-stu-id="b0b05-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="b0b05-128">特别是按钮“路径”将显示。</span><span class="sxs-lookup"><span data-stu-id="b0b05-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="b0b05-129">该路径可能包括以下相关 UI 元素的标签：</span><span class="sxs-lookup"><span data-stu-id="b0b05-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="b0b05-130">“操作窗格”选项卡</span><span class="sxs-lookup"><span data-stu-id="b0b05-130">Action Pane tab</span></span>
- <span data-ttu-id="b0b05-131">按钮组</span><span class="sxs-lookup"><span data-stu-id="b0b05-131">Button group</span></span>
- <span data-ttu-id="b0b05-132">菜单按钮（如果按钮在菜单按钮内）</span><span class="sxs-lookup"><span data-stu-id="b0b05-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="b0b05-133">菜单分隔符（如果按钮在菜单按钮内的命名组内）</span><span class="sxs-lookup"><span data-stu-id="b0b05-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="b0b05-134">页面上的组或选项卡（例如，快速选项卡的名称）</span><span class="sxs-lookup"><span data-stu-id="b0b05-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="b0b05-135">例如，您在**操作搜索**字段中键入 **tot**，现在正在检查结果列表。</span><span class="sxs-lookup"><span data-stu-id="b0b05-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="b0b05-136">名为**总计**的按钮的第一个条目将高亮显示。</span><span class="sxs-lookup"><span data-stu-id="b0b05-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="b0b05-137">**销售订单** &gt; **查看**的按钮路径也将显示。</span><span class="sxs-lookup"><span data-stu-id="b0b05-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="b0b05-138">路径的**销售订单**部分与“操作窗格”中的**销售订单**选项卡对应，路径的**查看**部分与该选项卡上的**查看**组对应。同样，**总折扣**按钮的路径（**销售** &gt; **计算**）告知您此按钮位于“操作窗格”的**销售**选项卡上的**计算**组中。</span><span class="sxs-lookup"><span data-stu-id="b0b05-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="b0b05-139">因此，此信息帮助您确切了解哪个按钮将由操作搜索触发（如果您在结果列表中选择该按钮）。</span><span class="sxs-lookup"><span data-stu-id="b0b05-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="b0b05-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="b0b05-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="b0b05-141">在之前的示例中，操作搜索在页面顶部显示了标准操作窗格的结果。</span><span class="sxs-lookup"><span data-stu-id="b0b05-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="b0b05-142">但是，操作搜索还显示位于页面其他位置的可见工具栏的结果。</span><span class="sxs-lookup"><span data-stu-id="b0b05-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="b0b05-143">例如，您搜索位于**销售订单行**快速选项卡的**现有库存量**按钮。</span><span class="sxs-lookup"><span data-stu-id="b0b05-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b0b05-144">这种情况下，结果列表中的按钮路径（**销售订单行** &gt; **库存** &gt; **查看**）告知您此按钮位于**销售订单行**快速选项卡的**库存**菜单按钮上的**查看**标题下。</span><span class="sxs-lookup"><span data-stu-id="b0b05-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="b0b05-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="b0b05-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="b0b05-146">操作搜索与导航搜索</span><span class="sxs-lookup"><span data-stu-id="b0b05-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="b0b05-147">操作搜索用于在页面上查找和运行操作，而在 Finance and Operations 中查找和导航到页面存在单独的搜索机制。</span><span class="sxs-lookup"><span data-stu-id="b0b05-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="b0b05-148">有关该功能的详细信息，请参阅[导航搜索](navigation-search.md)一文。</span><span class="sxs-lookup"><span data-stu-id="b0b05-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
