---
title: 履行销售协议
description: 此过程向您显示如何通过将销售订单与销售协议关联来履行销售协议。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3a35c7140b886f931df48e583b1582201b6547
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982009"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="a25ee-103">履行销售协议</span><span class="sxs-lookup"><span data-stu-id="a25ee-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a25ee-104">此过程向您显示如何通过将销售订单与销售协议关联来履行销售协议。</span><span class="sxs-lookup"><span data-stu-id="a25ee-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="a25ee-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="a25ee-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a25ee-106">在开始本指南前，请确保您具有有效的类型为“产品价值承诺”的销售协议。</span><span class="sxs-lookup"><span data-stu-id="a25ee-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="a25ee-107">或者，您可以运行名为“创建销售协议”的任务指南。</span><span class="sxs-lookup"><span data-stu-id="a25ee-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="a25ee-108">发布协议的销售订单</span><span class="sxs-lookup"><span data-stu-id="a25ee-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="a25ee-109">转到“销售和市场”>“销售协议”>“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="a25ee-110">在列表中，打开您要发布该订单的协议。</span><span class="sxs-lookup"><span data-stu-id="a25ee-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="a25ee-111">在“操作窗格”上单击“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="a25ee-112">单击“发布订单”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-112">Click Release order.</span></span>
    * <span data-ttu-id="a25ee-113">如“创建发布订单”页顶部的文本所指出的，销售订单行所需的详细信息根据协议是否根据数量或价值而有变化。</span><span class="sxs-lookup"><span data-stu-id="a25ee-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="a25ee-114">此指南的协议属于“产品价值承诺”类型。</span><span class="sxs-lookup"><span data-stu-id="a25ee-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="a25ee-115">这是本页的“行”部分为空白的原因。</span><span class="sxs-lookup"><span data-stu-id="a25ee-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="a25ee-116">如果承诺是基于数量，则行信息需从协议中复制。</span><span class="sxs-lookup"><span data-stu-id="a25ee-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="a25ee-117">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-117">Click Create.</span></span>
    * <span data-ttu-id="a25ee-118">消息通知您，已创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="a25ee-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="a25ee-119">由于订单不包含任何行，您必须添加订单行详细信息，以完成下达流程。</span><span class="sxs-lookup"><span data-stu-id="a25ee-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="a25ee-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-120">Close the page.</span></span>
7. <span data-ttu-id="a25ee-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-121">Close the page.</span></span>
8. <span data-ttu-id="a25ee-122">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="a25ee-123">在列表中，查找并打开在前一任务中发布的订单。</span><span class="sxs-lookup"><span data-stu-id="a25ee-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="a25ee-124">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-124">Click Add line.</span></span>
11. <span data-ttu-id="a25ee-125">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a25ee-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a25ee-126">在“物料编号”字段中，键入或选择在相关销售协议中指定的物料。</span><span class="sxs-lookup"><span data-stu-id="a25ee-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="a25ee-127">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a25ee-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a25ee-128">确保您输入的数量带来的“净额”低于相关销售协议的值。</span><span class="sxs-lookup"><span data-stu-id="a25ee-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="a25ee-129">请注意，由于销售订单与协议关联，协商的折扣百分比适用于该订单行。</span><span class="sxs-lookup"><span data-stu-id="a25ee-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="a25ee-130">单击“更新行”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-130">Click Update line.</span></span>
15. <span data-ttu-id="a25ee-131">单击“已附加”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-131">Click Attached.</span></span>
    * <span data-ttu-id="a25ee-132">“附加的协议”页显示 ID 以及协议期间，此为行发布时间。</span><span class="sxs-lookup"><span data-stu-id="a25ee-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="a25ee-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-133">Close the page.</span></span>
17. <span data-ttu-id="a25ee-134">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="a25ee-135">单击“附加销售协议”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="a25ee-136">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="a25ee-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="a25ee-137">单击“履行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="a25ee-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="a25ee-138">“履行”选型卡显示与此承诺相关的销售订单行及其履行状态和尚未发布的金额和数量的汇总。</span><span class="sxs-lookup"><span data-stu-id="a25ee-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="a25ee-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-139">Close the page.</span></span>
22. <span data-ttu-id="a25ee-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-140">Close the page.</span></span>
23. <span data-ttu-id="a25ee-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a25ee-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="a25ee-142">将销售协议应用于订购过程</span><span class="sxs-lookup"><span data-stu-id="a25ee-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="a25ee-143">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="a25ee-144">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-144">Click New.</span></span>
3. <span data-ttu-id="a25ee-145">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a25ee-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a25ee-146">在列表中，查找并选择销售协议所指定的客户。</span><span class="sxs-lookup"><span data-stu-id="a25ee-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="a25ee-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a25ee-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a25ee-148">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="a25ee-148">Expand the General section.</span></span>
7. <span data-ttu-id="a25ee-149">在“销售协议 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a25ee-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a25ee-150">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a25ee-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a25ee-151">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-151">Click Yes.</span></span>
10. <span data-ttu-id="a25ee-152">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-152">Click OK.</span></span>
11. <span data-ttu-id="a25ee-153">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a25ee-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="a25ee-154">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a25ee-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a25ee-155">在“物料编号”字段中，键入或选择在相关销售协议中指定的物料。</span><span class="sxs-lookup"><span data-stu-id="a25ee-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="a25ee-156">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a25ee-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a25ee-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-157">Click Save.</span></span>
16. <span data-ttu-id="a25ee-158">在操作窗格中，单击“领料和装箱”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="a25ee-159">单击“将装箱单过帐”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="a25ee-160">展开“参数”部分。</span><span class="sxs-lookup"><span data-stu-id="a25ee-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="a25ee-161">在“过帐”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="a25ee-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-162">Click OK.</span></span>
21. <span data-ttu-id="a25ee-163">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-163">Click OK.</span></span>
22. <span data-ttu-id="a25ee-164">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="a25ee-165">单击“附加销售协议”。</span><span class="sxs-lookup"><span data-stu-id="a25ee-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="a25ee-166">单击“履行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="a25ee-166">Click the Fulfillment tab.</span></span>

