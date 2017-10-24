---
title: "供应商发票日记帐和发票审核日记帐的默认对方科目"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="74b57-102">供应商发票日记帐和发票审核日记帐的默认对方科目</span><span class="sxs-lookup"><span data-stu-id="74b57-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="74b57-103">在以下供应商发票日记帐页中使用默认的对方帐户：</span><span class="sxs-lookup"><span data-stu-id="74b57-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="74b57-104">发票日记帐</span><span class="sxs-lookup"><span data-stu-id="74b57-104">Invoice journal</span></span>
-   <span data-ttu-id="74b57-105">发票审核日记帐</span><span class="sxs-lookup"><span data-stu-id="74b57-105">Invoice approval journal</span></span>

<span data-ttu-id="74b57-106">使用下表帮助您决定应为发票日记帐分配的默认科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74b57-107">在此设置默认帐户</span><span class="sxs-lookup"><span data-stu-id="74b57-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="74b57-108">在此提供默认帐户</span><span class="sxs-lookup"><span data-stu-id="74b57-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="74b57-109">此选项如何影响处理</span><span class="sxs-lookup"><span data-stu-id="74b57-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="74b57-110">您应该在何时使用此选项</span><span class="sxs-lookup"><span data-stu-id="74b57-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74b57-111"><strong>供应商组</strong> – 在<strong>默认帐户设置</strong>页上为供应商组设置默认对方科目，此页可以从<strong>供应商组</strong>页打开。</span><span class="sxs-lookup"><span data-stu-id="74b57-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="74b57-112">供应商帐户</span><span class="sxs-lookup"><span data-stu-id="74b57-112">Vendor account</span></span></li>
<li><span data-ttu-id="74b57-113">没有为供应商帐户指定默认帐户情况下的供应商组中的供应商帐户的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="74b57-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="74b57-114">供应商组的默认对方科目在<strong>默认帐户设置</strong>页上显示为供应商的默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="74b57-115">您可以从列表页<strong>所有供应商</strong>打开此页。</span><span class="sxs-lookup"><span data-stu-id="74b57-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="74b57-116">如果随着时间的推移，您通常为同一供应商组的同类物品付款，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="74b57-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74b57-117"><strong>供应商帐户</strong> – 在<strong>默认帐户设置</strong>页上为供应商帐户设置默认帐户，此页可以从<strong>供应商</strong>页打开。</span><span class="sxs-lookup"><span data-stu-id="74b57-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="74b57-118">供应商帐户的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="74b57-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="74b57-119">供应商帐户的默认对方科目显示为供应商帐户的日记帐条目的默认抵销帐户。</span><span class="sxs-lookup"><span data-stu-id="74b57-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="74b57-120">如果随着时间的推移，您通常为同一供应商的同类物品付款，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="74b57-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74b57-121"><strong>日记帐名称</strong> – 在<strong>日记帐名称</strong>页设置日记帐的默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="74b57-122">选择<strong>固定对方科目</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="74b57-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="74b57-123">请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐名称指定默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="74b57-124">使用日记帐名称的日记帐标题</span><span class="sxs-lookup"><span data-stu-id="74b57-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="74b57-125">使用日记帐名称的日记帐中的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="74b57-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="74b57-126">如果选择<strong>日记帐名称</strong>页中的<strong>固定对方科目</strong>选项，则供应商或供应商组的默认对方科目被日记帐名称的对方科目覆盖。</span><span class="sxs-lookup"><span data-stu-id="74b57-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="74b57-127">使用此选项为计入到特定帐户的特定成本和费用设置日记帐，无论供应商属于哪个供应商或供应商组。</span><span class="sxs-lookup"><span data-stu-id="74b57-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74b57-128"><strong>日记帐名称</strong> – 在<strong>日记帐名称</strong>页设置日记帐的默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="74b57-129">清除<strong>固定对方科目</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="74b57-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="74b57-130">请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐名称指定默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="74b57-131">日记帐标题</span><span class="sxs-lookup"><span data-stu-id="74b57-131">Journal header</span></span></li>
<li><span data-ttu-id="74b57-132">使用日记帐名称的日记帐中的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="74b57-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="74b57-133">在日记帐标题页中使用这些默认条目，日记帐标题页中的对方科目在日记帐凭证页中用作默认条目。</span><span class="sxs-lookup"><span data-stu-id="74b57-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="74b57-134">只要默认科目不是为供应商帐户设置的，就使用<strong>日记帐名称</strong>页中的默认科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="74b57-135">当未分配默认的供应商对方科目时，使用此选项设置所使用的默认科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74b57-136"><strong>日记帐标题</strong> – 在日记帐凭证页中为日记帐设置默认对方科目用作默认条目。</span><span class="sxs-lookup"><span data-stu-id="74b57-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="74b57-137">请注意，如果日记帐名称的日记帐类型为<strong>发票登记簿</strong>或<strong>审核</strong>，您则不能在日记帐标题指定默认对方科目。</span><span class="sxs-lookup"><span data-stu-id="74b57-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="74b57-138">日记帐中的日记帐条目</span><span class="sxs-lookup"><span data-stu-id="74b57-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="74b57-139">日记帐的默认对方科目在日记帐凭证页中用作默认条目。</span><span class="sxs-lookup"><span data-stu-id="74b57-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="74b57-140">如果日记帐中的大多数条目拥有相同的对方科目，则使用此选项帮助提高输入数据的速度。</span><span class="sxs-lookup"><span data-stu-id="74b57-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






