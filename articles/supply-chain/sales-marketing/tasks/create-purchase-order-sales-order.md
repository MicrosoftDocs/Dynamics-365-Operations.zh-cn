--- 
title: "基于销售订单创建采购订单"
description: "此过程向您显示如何创建基于销售订单的采购订单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1a840324862a7d3e279fce49288771d202527b77
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="a7294-103">基于销售订单创建采购订单</span><span class="sxs-lookup"><span data-stu-id="a7294-103">Create a purchase order from a sales order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7294-104">此过程向您显示如何创建基于销售订单的采购订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="a7294-105">采购订单上的产品数量将指定以履行源销售订单的需求。</span><span class="sxs-lookup"><span data-stu-id="a7294-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="a7294-106">这一履行销售需求的方法是更全面、优化的方法“分配需求计划”的替代方法。</span><span class="sxs-lookup"><span data-stu-id="a7294-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="a7294-107">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="a7294-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="a7294-108">基于销售订单创建采购订单</span><span class="sxs-lookup"><span data-stu-id="a7294-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="a7294-109">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="a7294-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="a7294-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a7294-110">Click New.</span></span>
3. <span data-ttu-id="a7294-111">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a7294-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a7294-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a7294-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a7294-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a7294-113">Click OK.</span></span>
6. <span data-ttu-id="a7294-114">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a7294-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a7294-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a7294-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a7294-116">如果您正在使用 USMF，可以选择 D0001。</span><span class="sxs-lookup"><span data-stu-id="a7294-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="a7294-117">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a7294-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="a7294-118">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="a7294-118">Click Add line.</span></span>
10. <span data-ttu-id="a7294-119">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a7294-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a7294-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a7294-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a7294-121">如果您正在使用 USMF，可以选择 T0020。</span><span class="sxs-lookup"><span data-stu-id="a7294-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="a7294-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a7294-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="a7294-123">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a7294-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="a7294-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a7294-124">Click Save.</span></span>
15. <span data-ttu-id="a7294-125">在操作窗格上，单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="a7294-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="a7294-126">单击“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="a7294-126">Click Purchase order.</span></span>
    * <span data-ttu-id="a7294-127">“创建采购订单”页面列出所有从销售订单复制的未结销售订单行。</span><span class="sxs-lookup"><span data-stu-id="a7294-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="a7294-128">您可以查看订单的详细信息，并可根据需要修改所选详细信息，例如创建直接采购前的采购数量和价格条款。</span><span class="sxs-lookup"><span data-stu-id="a7294-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="a7294-129">选择“包括所有选项”。</span><span class="sxs-lookup"><span data-stu-id="a7294-129">Select the Include all option.</span></span>
    * <span data-ttu-id="a7294-130">如果您想要生成仅销售订单行的一个子集的采购订单，则单独选择这些。</span><span class="sxs-lookup"><span data-stu-id="a7294-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="a7294-131">“供应商帐户”字段可能填充也可能不填充供应商编号。</span><span class="sxs-lookup"><span data-stu-id="a7294-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="a7294-132">如果已为产品设置默认供应商（在相关物料范围），则此供应商将会复制到该行。</span><span class="sxs-lookup"><span data-stu-id="a7294-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="a7294-133">否则，您必须手动输入供应商。</span><span class="sxs-lookup"><span data-stu-id="a7294-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="a7294-134">在此指南中，无论“供应商帐户”字段是否含有一个值，下一步骤将引导您选择与每一行不同的新供应商。</span><span class="sxs-lookup"><span data-stu-id="a7294-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="a7294-135">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a7294-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="a7294-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a7294-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="a7294-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a7294-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="a7294-138">选择第二订单行。</span><span class="sxs-lookup"><span data-stu-id="a7294-138">Select the second order line.</span></span>
22. <span data-ttu-id="a7294-139">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a7294-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="a7294-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a7294-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="a7294-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a7294-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="a7294-142">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="a7294-142">Click Validate.</span></span>
26. <span data-ttu-id="a7294-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="a7294-143">Click OK.</span></span>
    * <span data-ttu-id="a7294-144">消息通知您，已创建一个或多个采购订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="a7294-145">系统将为您已为其指定销售订单行的每一供应商生成单独的采购订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="a7294-146">这意味着，如果多个销售订单行由相同供应商供应，将会生成具有多行的单个采购订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="a7294-147">检查从销售订单创建的采购订单</span><span class="sxs-lookup"><span data-stu-id="a7294-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="a7294-148">在操作窗格上，单击“常规”。</span><span class="sxs-lookup"><span data-stu-id="a7294-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="a7294-149">单击“相关订单”。</span><span class="sxs-lookup"><span data-stu-id="a7294-149">Click Related orders.</span></span>
    * <span data-ttu-id="a7294-150">“相关订单”页面列出所有从销售订单创建的所有订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="a7294-151">在此示例中，有两个为各自不同供应商生成的采购订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="a7294-152">单击以访问“采购订单”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="a7294-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="a7294-153">每个采购订单行都与引发采购的销售订单行关联。</span><span class="sxs-lookup"><span data-stu-id="a7294-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="a7294-154">销售订单的关系在“产品”选项卡、“行详细信息”快速选项卡上、“参考类型”、“参考编号”和“参考批次”字段上有说明。</span><span class="sxs-lookup"><span data-stu-id="a7294-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="a7294-155">展开或折叠“行详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="a7294-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="a7294-156">单击“产品”选项卡。</span><span class="sxs-lookup"><span data-stu-id="a7294-156">Click the Product tab.</span></span>
    * <span data-ttu-id="a7294-157">“参考批次”可确保在附加的销售订单中对当前采购的成本计费。</span><span class="sxs-lookup"><span data-stu-id="a7294-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="a7294-158">您可以通过打开“参考编号”字段中的链接导航到源销售订单。</span><span class="sxs-lookup"><span data-stu-id="a7294-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  


