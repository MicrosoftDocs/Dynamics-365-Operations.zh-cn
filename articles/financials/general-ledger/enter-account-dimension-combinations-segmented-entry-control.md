---
title: "输入科目和维度组合（Segmented Entry 控件）"
description: "本文介绍如何输入帐户和维度组合或会计科目。 此输入经验通常称为 Segmented Entry 控件。"
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 610b21069d9f13a511f8017d0069fda0371abf10
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="9e18f-104">输入科目和维度组合（Segmented Entry 控件）</span><span class="sxs-lookup"><span data-stu-id="9e18f-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e18f-105">本文介绍如何输入帐户和维度组合或会计科目。</span><span class="sxs-lookup"><span data-stu-id="9e18f-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="9e18f-106">此输入经验通常称为 Segmented Entry 控件。</span><span class="sxs-lookup"><span data-stu-id="9e18f-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="9e18f-107">用户在不同的页面上输入科目和维度组合，如普通日记帐、预算和过帐定义的页面。</span><span class="sxs-lookup"><span data-stu-id="9e18f-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="9e18f-108">有效科目和维度组合取决于分配给分类帐的科目结构和分配给科目结构的高级规则。</span><span class="sxs-lookup"><span data-stu-id="9e18f-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="9e18f-109">在用户输入组合时，他们可以手动键入值或利用丰富的查找经验。</span><span class="sxs-lookup"><span data-stu-id="9e18f-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="9e18f-110">在您进入此字段后，可以开始键入，这样将搜索值和描述。</span><span class="sxs-lookup"><span data-stu-id="9e18f-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="9e18f-111">例如，如果键入 180，将搜索以该数字组合开头的任何值。</span><span class="sxs-lookup"><span data-stu-id="9e18f-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="9e18f-112">如果输入“现金”，将搜索描述以“现金”开头的任何值。</span><span class="sxs-lookup"><span data-stu-id="9e18f-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="9e18f-113">如果值或描述包含搜索条件，您还可以使用通配符，如“\*现金”或“\*180”进行搜索。</span><span class="sxs-lookup"><span data-stu-id="9e18f-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="9e18f-114">下表描述可在查找关闭时使用的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9e18f-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e18f-115">键盘快捷键</span><span class="sxs-lookup"><span data-stu-id="9e18f-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="9e18f-116">行为</span><span class="sxs-lookup"><span data-stu-id="9e18f-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e18f-117">Alt+向下箭头</span><span class="sxs-lookup"><span data-stu-id="9e18f-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="9e18f-118">打开查找。</span><span class="sxs-lookup"><span data-stu-id="9e18f-118">Open the lookup.</span></span> <span data-ttu-id="9e18f-119">如果您按 Alt+向下箭头，焦点移至浮出的段。</span><span class="sxs-lookup"><span data-stu-id="9e18f-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="9e18f-120">Enter 和 Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="9e18f-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="9e18f-121">会计科目表分隔符</span><span class="sxs-lookup"><span data-stu-id="9e18f-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="9e18f-122">右箭头和左箭头</span><span class="sxs-lookup"><span data-stu-id="9e18f-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="9e18f-123">移到下一个或上一个段。</span><span class="sxs-lookup"><span data-stu-id="9e18f-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e18f-124">制表符</span><span class="sxs-lookup"><span data-stu-id="9e18f-124">Tab</span></span></td>
<td><span data-ttu-id="9e18f-125">在网格中移到下一个字段。</span><span class="sxs-lookup"><span data-stu-id="9e18f-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9e18f-126">下表描述可在查找打开时使用的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9e18f-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e18f-127">键盘快捷键</span><span class="sxs-lookup"><span data-stu-id="9e18f-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="9e18f-128">行为</span><span class="sxs-lookup"><span data-stu-id="9e18f-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e18f-129">Esc</span><span class="sxs-lookup"><span data-stu-id="9e18f-129">Esc</span></span></td>
<td><span data-ttu-id="9e18f-130">关闭查找。</span><span class="sxs-lookup"><span data-stu-id="9e18f-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="9e18f-131">向上箭头和向下箭头</span><span class="sxs-lookup"><span data-stu-id="9e18f-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="9e18f-132">Page Up 和 Page Down</span><span class="sxs-lookup"><span data-stu-id="9e18f-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="9e18f-133">Home 和 End</span><span class="sxs-lookup"><span data-stu-id="9e18f-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="9e18f-134">移到列表中的上一个或下一个值，该值的上一个或下一个组，或者查找中的第一个或最后一个元素。</span><span class="sxs-lookup"><span data-stu-id="9e18f-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9e18f-135">会计科目表分隔符</span><span class="sxs-lookup"><span data-stu-id="9e18f-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="9e18f-136">右箭头和左箭头</span><span class="sxs-lookup"><span data-stu-id="9e18f-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="9e18f-137">移到下一个或上一个段。</span><span class="sxs-lookup"><span data-stu-id="9e18f-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e18f-138">选项卡</span><span class="sxs-lookup"><span data-stu-id="9e18f-138">Tab</span></span></td>
<td><span data-ttu-id="9e18f-139">在网格中移到下一个字段。</span><span class="sxs-lookup"><span data-stu-id="9e18f-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9e18f-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="9e18f-140">Alt+W</span></span></td>
<td><span data-ttu-id="9e18f-141">在<strong>显示全部</strong>和<strong>显示有效</strong>之间切换。</span><span class="sxs-lookup"><span data-stu-id="9e18f-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>

 



