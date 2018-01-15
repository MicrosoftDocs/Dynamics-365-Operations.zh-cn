---
title: "采购申请概览"
description: "此主题介绍了采购申请工作流和采购申请可能具有的不同状态。"
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 577204b49355a470769237eb46ad74e7f319a55e
ms.openlocfilehash: a05a0aeff7ade7d370303fdf68147a57d3f7285f
ms.contentlocale: zh-cn
ms.lasthandoff: 01/15/2018

---

# <a name="purchase-requisition-overview"></a><span data-ttu-id="03d39-103">采购申请概览</span><span class="sxs-lookup"><span data-stu-id="03d39-103">Purchase requisition overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="03d39-104">此主题介绍了采购申请工作流和采购申请可能具有的不同状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-104">This topic describes the purchase requisition workflow and the different statuses that a purchase requisition can have.</span></span>

<span data-ttu-id="03d39-105">根据您的组织的设置，您可以创建您组织使用的产品的采购申请。</span><span class="sxs-lookup"><span data-stu-id="03d39-105">Depending on the setup of your organization, you can create purchase requisitions for products that your organization uses.</span></span> <span data-ttu-id="03d39-106">采购申请是授权采购部门购买物料或服务的内部文档。</span><span class="sxs-lookup"><span data-stu-id="03d39-106">A purchase requisition is an internal document that authorizes the Purchasing department to buy items or services.</span></span>  

<span data-ttu-id="03d39-107">在审核采购申请后，其可用于生成采购订单。</span><span class="sxs-lookup"><span data-stu-id="03d39-107">After a purchase requisition is approved, it can be used to generate a purchase order.</span></span> <span data-ttu-id="03d39-108">采购订单是采购部门提交给供应商的外部文档。</span><span class="sxs-lookup"><span data-stu-id="03d39-108">Purchase orders are the external documents that the Purchasing department submits to vendors.</span></span>

## <a name="creating-purchase-requisitions"></a><span data-ttu-id="03d39-109">创建采购申请</span><span class="sxs-lookup"><span data-stu-id="03d39-109">Creating purchase requisitions</span></span>
<span data-ttu-id="03d39-110">您可以在**我的采购申请**页上创建采购申请并选择您所需的物料和服务。</span><span class="sxs-lookup"><span data-stu-id="03d39-110">You can create a purchase requisition on the **My purchase requisitions** page, and select the items and services that you require.</span></span> <span data-ttu-id="03d39-111">通过选择采购类别和输入产品详细信息，您可以从组织创建的采购目录中选择物料，或请求目录中未找到的物料。</span><span class="sxs-lookup"><span data-stu-id="03d39-111">You can select items from a procurement catalog that your organization has created, or you can request items that aren't found in a catalog by selecting a procurement category and entering the product details.</span></span>  

<span data-ttu-id="03d39-112">在可提交采购申请供查看前，必须在 Microsoft Dynamics 365 for Finance and Operations 客户端配置工作流。</span><span class="sxs-lookup"><span data-stu-id="03d39-112">Before you can submit a purchase requisition for review, workflows must be configured in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="03d39-113">您使用工作流通过审核流程移动采购申请，从**草稿**的初始状态到**已审核**最终状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-113">You use a workflow to move a purchase requisition through the review process, from an initial status of **Draft** to a final status of **Approved**.</span></span>

### <a name="purchase-requisition-statuses"></a><span data-ttu-id="03d39-114">采购申请状态</span><span class="sxs-lookup"><span data-stu-id="03d39-114">Purchase requisition statuses</span></span>

<span data-ttu-id="03d39-115">当您创建了一个采购申请时，为它分配一个状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-115">When you create a purchase requisition, a status is assigned to it.</span></span> <span data-ttu-id="03d39-116">您添加到采购申请的每个行也会获分配状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-116">A status is also assigned to every line that you add to a purchase requisition.</span></span> <span data-ttu-id="03d39-117">当您提交采购申请到工作流以供审核时，在这些行在工作流程中移动时更新采购申请的状态和每一行的状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-117">When you submit a purchase requisition to a workflow for review, the status of the purchase requisition and the status of each line are updated as the lines move through the workflow process.</span></span>  

<span data-ttu-id="03d39-118">您可以将采购申请工作流流程配置为使采购申请以单个文档的形式通过审核流程。</span><span class="sxs-lookup"><span data-stu-id="03d39-118">You can configure the purchase requisition workflow process to route a purchase requisition through the review process as a single document.</span></span> <span data-ttu-id="03d39-119">或者，在采购申请上的行可单独传送给相应审核人。</span><span class="sxs-lookup"><span data-stu-id="03d39-119">Alternatively, the lines on a purchase requisition can be routed individually to the appropriate reviewers.</span></span> <span data-ttu-id="03d39-120">如果单独审查采购申请行，可以当该行在审查流程中移动时更新每个采购申请行的状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-120">If the purchase requisition lines are reviewed individually, the status of each purchase requisition line can be updated as the line moves through the review process.</span></span> <span data-ttu-id="03d39-121">当所有行完成了审查流程，而且采购申请没有剩余审查步骤时，将会更新整个采购申请的状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-121">When all lines have completed the review process and no review steps remain for the purchase requisition, the status of the whole purchase requisition is updated.</span></span>

### <a name="purchase-requisition-workflow"></a><span data-ttu-id="03d39-122">采购申请工作流</span><span class="sxs-lookup"><span data-stu-id="03d39-122">Purchase requisition workflow</span></span>

<span data-ttu-id="03d39-123">下图显示了分配给采购申请和采购申请行的状态（当它们在工作流程中移动时）。</span><span class="sxs-lookup"><span data-stu-id="03d39-123">The following diagram shows the statuses that are assigned to a purchase requisition and a purchase requisition line as they move through the workflow process.</span></span>  

<span data-ttu-id="03d39-124">[![采购申请标题和行状态](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span><span class="sxs-lookup"><span data-stu-id="03d39-124">[![Purchase requisition header and line statuses](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span></span>

### <a name="purchase-requisition-header-and-line-status-relationships"></a><span data-ttu-id="03d39-125">采购申请标头和行状态关系</span><span class="sxs-lookup"><span data-stu-id="03d39-125">Purchase requisition header and line status relationships</span></span>

<span data-ttu-id="03d39-126">该采购申请的整体状态由采购申请行确定。</span><span class="sxs-lookup"><span data-stu-id="03d39-126">The overall status of a purchase requisition is determined by the status of the purchase requisition lines.</span></span> <span data-ttu-id="03d39-127">因此，在整个采购申请的审查流程完成前，必须完成所有采购申请行的审查流程。</span><span class="sxs-lookup"><span data-stu-id="03d39-127">Therefore, the review process must be completed for all purchase requisition lines before the review process for the whole purchase requisition can be completed.</span></span> <span data-ttu-id="03d39-128">下表描述了当采购申请在工作流程中移动时分配给采购申请标头和行的状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-128">The following table describes the statuses that are assigned to a purchase requisition header and lines as the purchase requisition moves through the workflow process.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="03d39-129">采购申请状态</span><span class="sxs-lookup"><span data-stu-id="03d39-129">Purchase requisition status</span></span></th>
<th><span data-ttu-id="03d39-130">采购申请行状态</span><span class="sxs-lookup"><span data-stu-id="03d39-130">Purchase requisition line status</span></span></th>
<th><span data-ttu-id="03d39-131">描述</span><span class="sxs-lookup"><span data-stu-id="03d39-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03d39-132">草案</span><span class="sxs-lookup"><span data-stu-id="03d39-132">Draft</span></span></td>
<td><span data-ttu-id="03d39-133">草案</span><span class="sxs-lookup"><span data-stu-id="03d39-133">Draft</span></span></td>
<td><span data-ttu-id="03d39-134">已创建采购申请和采购申请行，但是尚未提交以供审查。</span><span class="sxs-lookup"><span data-stu-id="03d39-134">The purchase requisition and purchase requisition line have been created, but they haven't been submitted for review.</span></span> <span data-ttu-id="03d39-135">可以修改具有状态<strong>草稿</strong>的采购申请和采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-135">Purchase requisitions and purchase requisition lines that have a status of <strong>Draft</strong> can be modified.</span></span> <span data-ttu-id="03d39-136">采购申请或采购申请行也可以具有状态<strong>草稿</strong>（如果它已被撤回，但未被提交以供审核）。</span><span class="sxs-lookup"><span data-stu-id="03d39-136">A purchase requisition or purchase requisition line also has a status of <strong>Draft</strong> if it has been recalled but hasn't been resubmitted for review.</span></span> <span data-ttu-id="03d39-137"><strong>注意：</strong>您可在单据级别提交或撤回采购申请。</span><span class="sxs-lookup"><span data-stu-id="03d39-137"><strong>Note:</strong> You can submit or recall a purchase requisition at the document level.</span></span> <span data-ttu-id="03d39-138">但是，您无法提交或撤回单个采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-138">However, you can't submit or recall a single purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03d39-139">正在审核</span><span class="sxs-lookup"><span data-stu-id="03d39-139">In review</span></span></td>
<td><ul>
<li><span data-ttu-id="03d39-140">正在审核</span><span class="sxs-lookup"><span data-stu-id="03d39-140">In review</span></span></li>
<li><span data-ttu-id="03d39-141">已拒绝</span><span class="sxs-lookup"><span data-stu-id="03d39-141">Rejected</span></span></li>
</ul></td>
<td><span data-ttu-id="03d39-142">如果已将工作流配置为将采购申请行传送给各个审核者，则每个行都可以具有状态<strong>正在审核</strong>或<strong>已拒绝</strong>。</span><span class="sxs-lookup"><span data-stu-id="03d39-142">If the workflow has been configured to route purchase requisition lines to individual reviewers, each line can have a status of <strong>In review</strong> or <strong>Rejected</strong>.</span></span> <span data-ttu-id="03d39-143">为所有采购申请行完成了审查流程，而且没有针对采购申请的剩余审查步骤时，将会更新该采购申请状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-143">The purchase requisition status is updated when the review process is completed for all purchase requisition lines and no review steps remain for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="03d39-144"><strong>正在审核</strong> – 已提交采购申请行以供审查。</span><span class="sxs-lookup"><span data-stu-id="03d39-144"><strong>In review</strong> – The purchase requisition lines have been submitted for review.</span></span> <span data-ttu-id="03d39-145">当为采购申请行完成了工作流流程时，该行将保持为状态<strong>正在审核</strong>，直到审查了所有其余采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-145">When the workflow process is completed for a purchase requisition line, the status of that line remains <strong>In review</strong> until all remaining purchase requisition lines have been reviewed.</span></span></li>
<li><span data-ttu-id="03d39-146"><strong>已拒绝</strong> – 已拒绝采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-146"><strong>Rejected</strong> – A purchase requisition line has been rejected.</span></span> <span data-ttu-id="03d39-147">已拒绝的采购申请行可以修改和重新提交。</span><span class="sxs-lookup"><span data-stu-id="03d39-147">Purchase requisition lines that are rejected can be modified and resubmitted.</span></span></li>
</ul>
<span data-ttu-id="03d39-148">如果您重新提交已被拒绝的采购申请行，将针对仍处于审核状态的采购申请行中的所有行重新开始审查流程。</span><span class="sxs-lookup"><span data-stu-id="03d39-148">If you resubmit a purchase requisition line that has been rejected, the review process starts over for all lines in the purchase requisition that are still in review.</span></span> <span data-ttu-id="03d39-149"><strong>注意：</strong>您可以撤回已提交的采购申请。</span><span class="sxs-lookup"><span data-stu-id="03d39-149"><strong>Note:</strong> You can recall a purchase requisition that has already been submitted.</span></span> <span data-ttu-id="03d39-150">当您撤回了某个采购申请时，也撤回了所有其他采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-150">When you recall a purchase requisition, all other purchase requisition lines are also recalled.</span></span> <span data-ttu-id="03d39-151">可以删除已被撤回的采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-151">Purchase requisition lines that have been recalled can be deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03d39-152">已拒绝</span><span class="sxs-lookup"><span data-stu-id="03d39-152">Rejected</span></span></td>
<td><span data-ttu-id="03d39-153">已拒绝</span><span class="sxs-lookup"><span data-stu-id="03d39-153">Rejected</span></span></td>
<td><span data-ttu-id="03d39-154">已拒绝采购申请和所有采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-154">The purchase requisition and all purchase requisition lines have been rejected.</span></span> <span data-ttu-id="03d39-155">可以重新提交已拒绝的采购申请和采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-155">Purchase requisitions and purchase requisition lines that have been rejected can be resubmitted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03d39-156">已审核</span><span class="sxs-lookup"><span data-stu-id="03d39-156">Approved</span></span></td>
<td><ul>
<li><span data-ttu-id="03d39-157">已审核</span><span class="sxs-lookup"><span data-stu-id="03d39-157">Approved</span></span></li>
<li><span data-ttu-id="03d39-158">已取消</span><span class="sxs-lookup"><span data-stu-id="03d39-158">Cancelled</span></span></li>
<li><span data-ttu-id="03d39-159">已结束</span><span class="sxs-lookup"><span data-stu-id="03d39-159">Closed</span></span></li>
</ul></td>
<td><span data-ttu-id="03d39-160">所有采购申请行都已完成了审查流程，并且针对该采购申请，没有更多的审查步骤。</span><span class="sxs-lookup"><span data-stu-id="03d39-160">All purchase requisition lines have completed the review process, and there are no more review steps for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="03d39-161"><strong>已审核</strong> – 已完成了采购申请行的审查流程，并已审核该行。</span><span class="sxs-lookup"><span data-stu-id="03d39-161"><strong>Approved</strong> – The review process for a purchase requisition line has been completed, and the line is approved.</span></span></li>
<li><span data-ttu-id="03d39-162"><strong>已取消</strong> – 该采购申请行已审核，但是因为不再需要它，所以已被取消。</span><span class="sxs-lookup"><span data-stu-id="03d39-162"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it's no longer required.</span></span> <span data-ttu-id="03d39-163">只取消进行审核的采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-163">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
<li><span data-ttu-id="03d39-164"><strong>已关闭</strong> – 已审核采购申请行，并且已根据申请用途生成单据。</span><span class="sxs-lookup"><span data-stu-id="03d39-164"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="03d39-165">如果申请目的是消耗量，则采购申请的采购订单已生成。</span><span class="sxs-lookup"><span data-stu-id="03d39-165">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="03d39-166">如果申请目的是补货，则已生成一个或多个履行文档。</span><span class="sxs-lookup"><span data-stu-id="03d39-166">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03d39-167">已取消</span><span class="sxs-lookup"><span data-stu-id="03d39-167">Cancelled</span></span></td>
<td><span data-ttu-id="03d39-168">已取消</span><span class="sxs-lookup"><span data-stu-id="03d39-168">Cancelled</span></span></td>
<td><span data-ttu-id="03d39-169">已取消采购申请和所有采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-169">The purchase requisition and all purchase requisition lines have been canceled.</span></span> <span data-ttu-id="03d39-170"><strong>注意：</strong>如果您不再需要在采购申请行上的物料，则您必须取消采购申请行（如果它已被审核）。</span><span class="sxs-lookup"><span data-stu-id="03d39-170"><strong>Note:</strong> If you no longer require an item that is on a purchase requisition line, you must cancel the purchase requisition line if it has already been approved.</span></span> <span data-ttu-id="03d39-171">只取消进行审核的采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-171">Only purchase requisition lines that have been approved can be canceled.</span></span> <span data-ttu-id="03d39-172">如果每个采购申请行都在审查中，则该采购申请也将拥有状态<strong>正在审核</strong>。</span><span class="sxs-lookup"><span data-stu-id="03d39-172">If any purchase requisition lines are in review, the purchase requisition will have a status of <strong>In review</strong>.</span></span> <span data-ttu-id="03d39-173">在这种情况下，您可以撤回该采购申请，并删除相应的采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-173">In this case, you can recall the purchase requisition and delete the appropriate purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03d39-174">已结束</span><span class="sxs-lookup"><span data-stu-id="03d39-174">Closed</span></span></td>
<td><ul>
<li><span data-ttu-id="03d39-175">已结束</span><span class="sxs-lookup"><span data-stu-id="03d39-175">Closed</span></span></li>
<li><span data-ttu-id="03d39-176">已取消</span><span class="sxs-lookup"><span data-stu-id="03d39-176">Cancelled</span></span></li>
</ul></td>
<td><span data-ttu-id="03d39-177">采购申请已关闭，并已生成一个或多个履行文档。</span><span class="sxs-lookup"><span data-stu-id="03d39-177">The purchase requisition is closed, and one or more fulfillment documents have been generated.</span></span>
<ul>
<li><span data-ttu-id="03d39-178"><strong>已关闭</strong> – 已审核采购申请行，并且已根据申请用途生成单据。</span><span class="sxs-lookup"><span data-stu-id="03d39-178"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="03d39-179">如果申请目的是消耗量，则采购申请的采购订单已生成。</span><span class="sxs-lookup"><span data-stu-id="03d39-179">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="03d39-180">如果申请目的是补货，则已生成一个或多个履行文档。</span><span class="sxs-lookup"><span data-stu-id="03d39-180">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
<li><span data-ttu-id="03d39-181"><strong>已取消</strong> – 该采购申请行已审核，但是因为不再需要它，所以已被取消。</span><span class="sxs-lookup"><span data-stu-id="03d39-181"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it's no longer required.</span></span> <span data-ttu-id="03d39-182">只取消进行审核的采购申请行。</span><span class="sxs-lookup"><span data-stu-id="03d39-182">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
</ul><span data-ttu-id="03d39-183">
<strong>注意：</strong>如果您不再需要已关闭的采购申请行上的物料，则您必须取消为采购申请行生成的履行文档上的行。</span><span class="sxs-lookup"><span data-stu-id="03d39-183">
<strong>Note:</strong> If you no longer require an item on a purchase requisition line that has been closed, you must cancel the line on the fulfillment document that was generated for the purchase requisition line.</span></span></td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a><span data-ttu-id="03d39-184">多个财务科目的分摊成本</span><span class="sxs-lookup"><span data-stu-id="03d39-184">Distributing costs to multiple financial accounts</span></span>
<span data-ttu-id="03d39-185">您可以将包括在采购申请中的产品的成本分摊到多个财务科目。</span><span class="sxs-lookup"><span data-stu-id="03d39-185">You can distribute the cost of a product that is included in a purchase requisition to multiple financial accounts.</span></span> <span data-ttu-id="03d39-186">如果您的组织使用维度，如成本中心和部门，则您可以将产品的成本分摊到财务账户的维度。</span><span class="sxs-lookup"><span data-stu-id="03d39-186">If your organization uses dimensions, such as cost centers and departments, you can distribute the cost of a product to dimensions for financial accounts.</span></span>

## <a name="requisition-purposes"></a><span data-ttu-id="03d39-187">申请用途</span><span class="sxs-lookup"><span data-stu-id="03d39-187">Requisition purposes</span></span>
<span data-ttu-id="03d39-188">申请用途让履行申请需求的流程更灵活。</span><span class="sxs-lookup"><span data-stu-id="03d39-188">Requisition purposes make the process of fulfilling requisition demand more flexible.</span></span> <span data-ttu-id="03d39-189">在您创建申请时，可以将两个目的之一分配给它：消耗量或补货。</span><span class="sxs-lookup"><span data-stu-id="03d39-189">When you create a requisition, you can assign one of two purposes to it: consumption or replenishment.</span></span> <span data-ttu-id="03d39-190">根据申请用途和您的组织设置，申请需求可通过采购订单、转移单、生产订单或看板履行。</span><span class="sxs-lookup"><span data-stu-id="03d39-190">Depending on the requisition purpose and the setup of your organization, requisition demand can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="03d39-191">在采购政策中，当为您的组织创建申请时，您可以控制可用的申请目的。</span><span class="sxs-lookup"><span data-stu-id="03d39-191">In the procurement policies, you can control the requisition purposes that are available when a requisition is created for your organization.</span></span>

### <a name="requisitions-that-have-a-purpose-of-consumption"></a><span data-ttu-id="03d39-192">申请具有消耗量的目标</span><span class="sxs-lookup"><span data-stu-id="03d39-192">Requisitions that have a purpose of consumption</span></span>

<span data-ttu-id="03d39-193">申请具有消耗量的目标表示将通过您的组织内部使用的物料或服务的需求。</span><span class="sxs-lookup"><span data-stu-id="03d39-193">A requisition that has a purpose of consumption represents demand for items or services that will be used internally by your organization.</span></span> <span data-ttu-id="03d39-194">通过此类型的申请创建需求始终按采购订单执行。</span><span class="sxs-lookup"><span data-stu-id="03d39-194">The demand that is created by this kind of requisition is always fulfilled by a purchase order.</span></span> <span data-ttu-id="03d39-195">如果 Microsoft Dynamics 365 for Finance and Operations 设置为自动生成采购订单，将在采购申请审核后创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="03d39-195">If Microsoft Dynamics 365 for Finance and Operations is set up to automatically generate purchase orders, purchase orders are created after the purchase requisition is approved.</span></span>

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a><span data-ttu-id="03d39-196">申请具有补货的目标</span><span class="sxs-lookup"><span data-stu-id="03d39-196">Requisitions that have a purpose of replenishment</span></span>

<span data-ttu-id="03d39-197">补货具有补货的目的表示需求以补充库存。</span><span class="sxs-lookup"><span data-stu-id="03d39-197">A requisition that has a purpose of replenishment represents demand to replenish inventory.</span></span> <span data-ttu-id="03d39-198">例如，您创建补货物料的申请，以便他们可以在特定的零售位置的指定时间销售。</span><span class="sxs-lookup"><span data-stu-id="03d39-198">For example, you create a requisition to replenish items so that they can be sold at a specific retail location at a specific time.</span></span> <span data-ttu-id="03d39-199">由此申请创建的需求可以按采购订单、转移单、生产订单或看板执行。</span><span class="sxs-lookup"><span data-stu-id="03d39-199">The demand that is created by this kind of requisition can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="03d39-200">当申请目的为补货时，需求表示为数量而不是货币金额。</span><span class="sxs-lookup"><span data-stu-id="03d39-200">When the requisition purpose is replenishment, demand is expressed as a quantity instead of a monetary amount.</span></span> <span data-ttu-id="03d39-201">因此，预留款核算、预算控制、固定资产确定的业务规则 (BRAD)，项目核算和任何相关的规则不适用。</span><span class="sxs-lookup"><span data-stu-id="03d39-201">Therefore, encumbrance accounting, budgetary control, business rules for fixed asset determination (BRAD), project accounting, and any related rules don't apply.</span></span> <span data-ttu-id="03d39-202">已存储和发放到指定法人的产品可以履行补货申请要求。</span><span class="sxs-lookup"><span data-stu-id="03d39-202">Only products that are stocked and released to the specified legal entity can fulfill replenishment requisition demand.</span></span> <span data-ttu-id="03d39-203">若要定义在申请用途是补货时可用的产品，请使用**补货类别访问政策规则**页。</span><span class="sxs-lookup"><span data-stu-id="03d39-203">To define the products that are available when the requisition purpose is replenishment, use the **Replenishment category access policy rule** page.</span></span>  

<span data-ttu-id="03d39-204">若要使用具有补货目的的采购申请，您必须将主计划编制设计为包括申请需求。</span><span class="sxs-lookup"><span data-stu-id="03d39-204">To use purchase requisitions that have a purpose of replenishment, you must set up master scheduling to include requisition demand.</span></span> <span data-ttu-id="03d39-205">将基于在您的组织中为物料设置的供应策略自动确定由此类申请创建的需求的履行方法，并通过使用主计划编制计划。</span><span class="sxs-lookup"><span data-stu-id="03d39-205">The fulfillment method for the demand that is created by this kind of requisition is then determined automatically, based on the supply policies that have been set up for the items in your organization and planned by using master scheduling.</span></span>

## <a name="purchase-requisitions-and-requests-for-quotation"></a><span data-ttu-id="03d39-206">采购申请和询价</span><span class="sxs-lookup"><span data-stu-id="03d39-206">Purchase requisitions and requests for quotation</span></span>
<span data-ttu-id="03d39-207">有时候，您必须开始询价 (RFQ) 流程以确定在采购申请中申请的产品的供应商和价格。</span><span class="sxs-lookup"><span data-stu-id="03d39-207">In some cases, you must start a request for quotation (RFQ) process to identify the vendor and price for products that are requested in a purchase requisition.</span></span> <span data-ttu-id="03d39-208">在采购申请正在审核时，可以生成询价。</span><span class="sxs-lookup"><span data-stu-id="03d39-208">An RFQ can be generated when the purchase requisition is in review.</span></span> <span data-ttu-id="03d39-209">当您接受出价时，有关供应商、价格等的信息将转移到申请。</span><span class="sxs-lookup"><span data-stu-id="03d39-209">When you accept a bid, information about the vendor, price, and so on, is transferred to the requisition.</span></span>  

<span data-ttu-id="03d39-210">您可以通过选中**采购申请详细信息**页上的**暂停**复选框来将采购申请置于暂停状态。</span><span class="sxs-lookup"><span data-stu-id="03d39-210">You can put a purchase requisition on hold by selecting the **On hold** check box on the **Purchase requisition details** page.</span></span> <span data-ttu-id="03d39-211">处理采购申请只能在您通过清除此复选框删除暂停后继续。</span><span class="sxs-lookup"><span data-stu-id="03d39-211">Processing of the purchase requisition can continue only after you remove the hold by clearing the check box.</span></span>  

<span data-ttu-id="03d39-212">**注意：**在电子采购中，您的采购申请的询价可能允许供应商添加备选行。</span><span class="sxs-lookup"><span data-stu-id="03d39-212">**Note:** In eProcurement, the RFQ for your purchase requisition might allow vendors to add alternate lines.</span></span> <span data-ttu-id="03d39-213">在此情况下，采购申请将反映已审核的备选项。</span><span class="sxs-lookup"><span data-stu-id="03d39-213">In this case, your purchase requisition will reflect approved alternates.</span></span>

## <a name="demand-consolidation"></a><span data-ttu-id="03d39-214">需求合并</span><span class="sxs-lookup"><span data-stu-id="03d39-214">Demand consolidation</span></span>
<span data-ttu-id="03d39-215">通过合并来自多个采购申请的采购申请行，您可以增加与您的供应商协商的能力，以实现更好的定价、更低的装运和处理的费用，并降低开销成本。</span><span class="sxs-lookup"><span data-stu-id="03d39-215">By consolidating purchase requisition lines from multiple purchase requisitions, you can increase your negotiating power with your vendors to achieve better pricing, lower shipping and handling costs, and reduced overhead costs.</span></span>  

<span data-ttu-id="03d39-216">仅当以下报表为真时，采购申请行才适用于需求合并：</span><span class="sxs-lookup"><span data-stu-id="03d39-216">Purchase requisition lines are eligible for demand consolidation only if the following statements are true:</span></span>

-   <span data-ttu-id="03d39-217">采购申请已审核。</span><span class="sxs-lookup"><span data-stu-id="03d39-217">The purchase requisition has been approved.</span></span>
-   <span data-ttu-id="03d39-218">采购申请符合手动进行处理和要求合并的采购策略规则条件。</span><span class="sxs-lookup"><span data-stu-id="03d39-218">The purchase requisition meets the purchasing policy rule criteria for manual processing and demand consolidation.</span></span>

<span data-ttu-id="03d39-219">符合手动处理条件的已审核的采购申请行在**发布已审核的采购申请**页列出。</span><span class="sxs-lookup"><span data-stu-id="03d39-219">Approved purchase requisition lines that meet the criteria for manual processing are listed on the **Release approved purchase requisitions** page.</span></span> <span data-ttu-id="03d39-220">如果采购申请行还满足需求合并的条件，可以将该行添加到“合并机会”。</span><span class="sxs-lookup"><span data-stu-id="03d39-220">If a purchase requisition line also meets the criteria for demand consolidation, the line can be added to a consolidation opportunity.</span></span>  

<span data-ttu-id="03d39-221">合并机会是一组组合在一起的采购申请行，以便该采购的专业人员可以与供应商协商最佳交易。</span><span class="sxs-lookup"><span data-stu-id="03d39-221">A consolidation opportunity is a set of purchase requisition lines that are grouped together, so that the purchasing professional can negotiate the best deal with vendors.</span></span> <span data-ttu-id="03d39-222">您为合并机会选择的采购申请行上显示在**采购申请合并**页。</span><span class="sxs-lookup"><span data-stu-id="03d39-222">Purchase requisition lines that you select for a consolidation opportunity appear on the **Purchase requisition consolidation** page.</span></span> <span data-ttu-id="03d39-223">如果需要更改，您可以在此页修改行。</span><span class="sxs-lookup"><span data-stu-id="03d39-223">You can modify the lines on this page, if changes are required.</span></span> <span data-ttu-id="03d39-224">您还可以为该合并机会添加新行或从中删除现有行。</span><span class="sxs-lookup"><span data-stu-id="03d39-224">You can also add new lines to the consolidation opportunity or remove existing lines.</span></span>  

<span data-ttu-id="03d39-225">在将申请行添加到合并机会并作出所需更改后，您可以为该合并采购申请行创建采购订单。</span><span class="sxs-lookup"><span data-stu-id="03d39-225">After you add requisition lines to a consolidation opportunity and make any changes that you require, you can create a purchase order for the consolidated purchase requisition lines.</span></span>  

<span data-ttu-id="03d39-226">**注意：**您为在**采购申请合并**页中的某一采购申请行做出的更改反映在您创建的采购订单上。</span><span class="sxs-lookup"><span data-stu-id="03d39-226">**Note:** Changes that you make to a purchase requisition line on the **Purchase requisition consolidation** page are reflected on the purchase order that you create.</span></span> <span data-ttu-id="03d39-227">但是在采购申请中，该行保持不变，以便保留其历史记录。</span><span class="sxs-lookup"><span data-stu-id="03d39-227">However, the line remains unchanged in the purchase requisition, so that its history is preserved.</span></span>  

<span data-ttu-id="03d39-228">若要为没有资格享受需求合并或没有为合并机会选择的采购申请行创建采购订单，您必须手动处理行。</span><span class="sxs-lookup"><span data-stu-id="03d39-228">To create a purchase order for purchase requisition lines that aren't eligible for demand consolidation or aren't selected for a consolidation opportunity, you must process the lines manually.</span></span>

### <a name="consolidating-purchase-requisition-lines"></a><span data-ttu-id="03d39-229">合并采购申请行</span><span class="sxs-lookup"><span data-stu-id="03d39-229">Consolidating purchase requisition lines</span></span>

<span data-ttu-id="03d39-230">在工作流中的采购申请审核时，以及如果为您的组织配置了预算控制，记录预算预留和预留款后，将启动要求合并的流程。</span><span class="sxs-lookup"><span data-stu-id="03d39-230">The process for demand consolidation starts when a purchase requisition is approved in a workflow and, if budget control is configured for your organization, when the budget reservations and pre-encumbrances have been recorded.</span></span> <span data-ttu-id="03d39-231">下图显示需求合并的流程。</span><span class="sxs-lookup"><span data-stu-id="03d39-231">The following diagram shows the process flow for demand consolidation.</span></span>  

<span data-ttu-id="03d39-232">[![需求合并的流程流](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span><span class="sxs-lookup"><span data-stu-id="03d39-232">[![Process flow for demand consolidation](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span></span>  

<span data-ttu-id="03d39-233">若要合并已审核的采购申请行，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="03d39-233">To consolidate approved purchase requisition lines, follow these steps:</span></span>

1.  <span data-ttu-id="03d39-234">查看已审查的申请行，这些申请行为手动处理持有并且适用于需求合并。</span><span class="sxs-lookup"><span data-stu-id="03d39-234">Review approved requisition lines that have been held for manual processing, and that are eligible for demand consolidation.</span></span>
2.  <span data-ttu-id="03d39-235">选择要添加到合并机会的行。</span><span class="sxs-lookup"><span data-stu-id="03d39-235">Select lines to add to a consolidation opportunity.</span></span>
3.  <span data-ttu-id="03d39-236">创建新的合并机会或将申请行添加到现有合并机会。</span><span class="sxs-lookup"><span data-stu-id="03d39-236">Create a new consolidation opportunity, or add requisition lines to an existing consolidation opportunity.</span></span>
4.  <span data-ttu-id="03d39-237">对申请行进行任何所需更改，然后移除您在合并机会中不再想要包含的申请行物料。</span><span class="sxs-lookup"><span data-stu-id="03d39-237">Make any required changes to the requisition lines, and remove requisition line items that you no longer want to include in the consolidation opportunity.</span></span>
5.  <span data-ttu-id="03d39-238">创建合并机会中的合并申请行或采购申请行的采购订单。</span><span class="sxs-lookup"><span data-stu-id="03d39-238">Create purchase orders for consolidated requisition lines or for purchase requisition lines in a consolidation opportunity.</span></span>


<a name="see-also"></a><span data-ttu-id="03d39-239">请参阅</span><span class="sxs-lookup"><span data-stu-id="03d39-239">See also</span></span>
--------

[<span data-ttu-id="03d39-240">创建消耗量申请（任务指南）</span><span class="sxs-lookup"><span data-stu-id="03d39-240">Create a requisition for consumption (Task guide)</span></span>](tasks/create-requisition-consumption.md)

[<span data-ttu-id="03d39-241">采购申请工作流</span><span class="sxs-lookup"><span data-stu-id="03d39-241">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




