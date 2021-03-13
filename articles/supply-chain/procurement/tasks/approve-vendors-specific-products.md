---
title: 审核特定产品的供应商
description: 此过程显示如何审核特定产品的供应商。
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cc7d8a93bdbdb5a1446fc34beff4b74aa9d11a0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016645"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="c5dd4-103">审核特定产品的供应商</span><span class="sxs-lookup"><span data-stu-id="c5dd4-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5dd4-104">此过程显示如何审核特定产品的供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="c5dd4-105">这允许您控制使在产品添加到采购订单时可以使用哪个供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="c5dd4-106">您可以使用演示数据公司 USMF 或您自己的数据使用该程序。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="c5dd4-107">此任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="c5dd4-108">在导航窗格中，转到 **模块 > 产品信息管理 > 产品 > 已发放产品**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c5dd4-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c5dd4-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c5dd4-111">展开 **采购** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="c5dd4-112">如果在 **供应商** 字段中显示主供应商，则您需要在以下步骤中添加此供应商为核准供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="c5dd4-113">如果显示了供应商编号，请记下该编号。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="c5dd4-114">在“操作窗格”上，单击 **采购**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="c5dd4-115">单击 **设置**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-115">Click **Setup**.</span></span>
7. <span data-ttu-id="c5dd4-116">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-116">Click **Add**.</span></span>
8. <span data-ttu-id="c5dd4-117">在“供应商”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="c5dd4-118">选择核准供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-118">Select the approved vendor.</span></span> <span data-ttu-id="c5dd4-119">如果在产品记录中有一个供应商，至少有一个行必须是主供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="c5dd4-120">如果您之前记录了供应商编号，请在此处选择它。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="c5dd4-121">在 **截止日期** 字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="c5dd4-122">选择数月前的日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="c5dd4-123">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-123">Click **Add**.</span></span>
11. <span data-ttu-id="c5dd4-124">在 **供应商** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="c5dd4-125">在 **截止日期** 字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="c5dd4-126">选择与以前的到期日期不同的日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="c5dd4-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-127">Close the page.</span></span>
14. <span data-ttu-id="c5dd4-128">在操作窗格上，单击 **核准供应商**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="c5dd4-129">在 **截止日期** 字段，输入日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="c5dd4-130">此日期用作筛选器，这样您可以看到直到某一日期谁是核准供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="c5dd4-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-131">Close the page.</span></span>
17. <span data-ttu-id="c5dd4-132">在操作窗格上，单击 **有效期**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="c5dd4-133">在 **显示供应商到期日期** 字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="c5dd4-134">您可以使用此页来标识审核状态将在某一日期之后到期的供应商。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="c5dd4-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-135">Close the page.</span></span>
20. <span data-ttu-id="c5dd4-136">单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-136">Click **Edit**.</span></span>
21. <span data-ttu-id="c5dd4-137">在 **核准供应商检查方法** 字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="c5dd4-138">如果产品添加到供应商不是核准供应商的采购订单行，此字段可为应发生的情况选择策略。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="c5dd4-139">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-139">Click **Save**.</span></span>
23. <span data-ttu-id="c5dd4-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-140">Close the page.</span></span>
24. <span data-ttu-id="c5dd4-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-141">Close the page.</span></span>
25. <span data-ttu-id="c5dd4-142">在导航窗格中，转到 **模块 > 采购 > 供应商 > 供应商/物料关联 > 按物料显示的核准供应商列表**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="c5dd4-143">此页为您提供所有产品和核准供应商的概览。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="c5dd4-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-144">Close the page.</span></span>
27. <span data-ttu-id="c5dd4-145">在导航窗格中，转到 **模块 > 采购 > 供应商 > 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="c5dd4-146">您还可以从供应商开始，然后转到该供应商帐户的已审核产品的列表。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="c5dd4-147">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="c5dd4-148">在操作窗格上，单击 **采购**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="c5dd4-149">单击 **按供应商显示的核准供应商列表**。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="c5dd4-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-150">Close the page.</span></span>
32. <span data-ttu-id="c5dd4-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5dd4-151">Close the page.</span></span>

