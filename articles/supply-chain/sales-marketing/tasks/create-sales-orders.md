---
title: 创建销售订单
description: 此过程说明如何创建销售订单。
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9aa353ad771844abc0860f06d9bc22b9f4adce92
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982057"
---
# <a name="create-sales-orders"></a><span data-ttu-id="5ec83-103">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="5ec83-103">Create sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ec83-104">此过程说明如何创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="5ec83-104">This procedure shows you how to create a sales order.</span></span> <span data-ttu-id="5ec83-105">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="5ec83-105">You can use the procedure in demo data company USMF.</span></span> <span data-ttu-id="5ec83-106">销售订单通常由销售订单处理器创建。</span><span class="sxs-lookup"><span data-stu-id="5ec83-106">Sales orders are typically created by a sales order processor.</span></span> 

## <a name="enter-sales-order-header-details"></a><span data-ttu-id="5ec83-107">输入销售订单抬头详细信息</span><span class="sxs-lookup"><span data-stu-id="5ec83-107">Enter sales order header details</span></span>
1. <span data-ttu-id="5ec83-108">转到**导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-108">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="5ec83-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-109">Select **New**.</span></span>
3. <span data-ttu-id="5ec83-110">在**客户帐户**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5ec83-110">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ec83-111">在列表中，找到并选择客户记录。</span><span class="sxs-lookup"><span data-stu-id="5ec83-111">In the list, find and select the customer record.</span></span>
    - <span data-ttu-id="5ec83-112">在本示例中，选择客户编号 US-004。</span><span class="sxs-lookup"><span data-stu-id="5ec83-112">For this example, select customer number US-004.</span></span>  
5. <span data-ttu-id="5ec83-113">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-113">Select **OK**.</span></span>

## <a name="enter-sales-order-line-details"></a><span data-ttu-id="5ec83-114">输入销售订单行详细信息</span><span class="sxs-lookup"><span data-stu-id="5ec83-114">Enter sales order line details</span></span>
    
<span data-ttu-id="5ec83-115">您的公司销售的产品可能款式不同，可以不同维度区分，例如配置、颜色、大小和样式。</span><span class="sxs-lookup"><span data-stu-id="5ec83-115">The products sold by your organization may come in variants differentiated by dimensions, such as configuration, color, size, and style.</span></span> <span data-ttu-id="5ec83-116">此外，产品可以设置为使用存储维度，如站点、仓库、托盘和货架维度，例如批号和序列号。</span><span class="sxs-lookup"><span data-stu-id="5ec83-116">Also, products may be set up to use storage dimensions, such as site, warehouse, and pallet, and racking dimensions, such as batch and serial numbers.</span></span> <span data-ttu-id="5ec83-117">在分配这些维度时，您必须在订单行选择维度的数值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-117">When these dimensions are assigned, you must select the values for those dimensions on the order line.</span></span> <span data-ttu-id="5ec83-118">为了提高订单输入效率，您可能要添加各自的维度字段到订单网格中。</span><span class="sxs-lookup"><span data-stu-id="5ec83-118">To improve order entry efficiency, you may want to add the respective dimension fields to the order grid.</span></span>
    
1. <span data-ttu-id="5ec83-119">在**销售订单行**部分下，选择**销售订单行**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-119">Under the **Sales order lines** section, select the **Sales order line**.</span></span>
2. <span data-ttu-id="5ec83-120">选择**维度**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-120">Select **Dimensions**.</span></span>
    
    <span data-ttu-id="5ec83-121">在本示例中，选择颜色、位置和仓库维度。</span><span class="sxs-lookup"><span data-stu-id="5ec83-121">For this example, select the Color, Site and Warehouse dimensions.</span></span> <span data-ttu-id="5ec83-122">您选择的维度将显示在订单网格中。</span><span class="sxs-lookup"><span data-stu-id="5ec83-122">The dimensions you select here will appear in the sales order grid.</span></span> <span data-ttu-id="5ec83-123">如果想要保存您的选择，则将**保存设置**选项设为“是”。</span><span class="sxs-lookup"><span data-stu-id="5ec83-123">If you want your selections to persist, set the **Save setup** option to Yes.</span></span>
    
3. <span data-ttu-id="5ec83-124">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-124">Select **OK**.</span></span>
4. <span data-ttu-id="5ec83-125">在**物料编号**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5ec83-125">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5ec83-126">在本示例中，单击“物料编号 T0004”。</span><span class="sxs-lookup"><span data-stu-id="5ec83-126">For this example, select item number T0004.</span></span>
    - <span data-ttu-id="5ec83-127">如果物料是销售类别的一部分，物料名称将在“销售类别”字段自动显示。</span><span class="sxs-lookup"><span data-stu-id="5ec83-127">If the item is part of a sales category, the item name will automatically appear in the Sales category field.</span></span>  
    - <span data-ttu-id="5ec83-128">如果产品维度字段已包含一个值，则该值是从定义为默认产品维度的产品记录中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="5ec83-128">If product dimension fields already contain a value, this is because the value was copied from the product record where it is defined as a default product dimension.</span></span> <span data-ttu-id="5ec83-129">您可以随时更改默认值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-129">You can change the default value at any time.</span></span>   
6. <span data-ttu-id="5ec83-130">在**颜色**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="5ec83-130">In the **Color** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5ec83-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="5ec83-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5ec83-132">在**数量**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="5ec83-132">In the **Quantity** field, enter a number.</span></span>
    - <span data-ttu-id="5ec83-133">如果物料销售单位与采购、生产和存储单位不同，且测量单位在产品记录中有设置，则该值将在**单位**字段显示。</span><span class="sxs-lookup"><span data-stu-id="5ec83-133">If the item is sold in different units than when it's purchased, produced, and stored, and a sales unit of measure is set on the product record, this value will be shown in the **Unit** field.</span></span> <span data-ttu-id="5ec83-134">您可以随时更改该值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-134">You can change the value at any time.</span></span>   
    - <span data-ttu-id="5ec83-135">如果**站点**字段已包含一个值，则该值是从订单抬头或产品相关的订单设置中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="5ec83-135">If the **Site** field already contains a value, the value was copied from the order header or from the order settings that are associated with the product.</span></span> <span data-ttu-id="5ec83-136">您可以随时更改该值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-136">You can change the value at any time.</span></span> <span data-ttu-id="5ec83-137">如果此字段为空，则选择一个值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-137">If the field is empty, select a value.</span></span>   
    - <span data-ttu-id="5ec83-138">如果**单价**字段已包含一个值，则该值是从有效贸易协议或产品记录中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="5ec83-138">If the **Unit price** field already contains a value, the value was copied from a valid trade agreement, or from the product record.</span></span> <span data-ttu-id="5ec83-139">（单价还可来自销售协议，但是销售协议的销售订单创建流程与此处显示的不同。）如果此字段为空，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-139">(The unit price can also originate from a sales agreement, but the process for creating sales orders from sales agreements is different to the one shown here.) If the field is empty, enter a value.</span></span>   
    - <span data-ttu-id="5ec83-140">**折扣**字段包含一个产品单位的折扣金额。</span><span class="sxs-lookup"><span data-stu-id="5ec83-140">The **Discount** field contains a discount amount per product unit.</span></span> <span data-ttu-id="5ec83-141">若要计算总折扣金额，应用单行折扣值乘以行数。</span><span class="sxs-lookup"><span data-stu-id="5ec83-141">To calculate the total line discount amount, the discount value is multiplied by line quantity.</span></span> <span data-ttu-id="5ec83-142">如果**折扣**字段已包含一个值，则该值是从有效贸易协议中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="5ec83-142">If the **Discount** field already contains a value, the value was copied from a valid trade agreement.</span></span> <span data-ttu-id="5ec83-143">如果此字段为空，且您想给该客户行折扣，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-143">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    - <span data-ttu-id="5ec83-144">**折扣百分比**字段包含计算全部行总额时减去的百分比值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-144">The **Discount percent** field contains a percentage value by which the total line gross amount is to be reduced.</span></span>  <span data-ttu-id="5ec83-145">如果**折扣百分比**字段已包含一个值，则该值是从有效贸易协议中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="5ec83-145">If the **Discount percent** field already contains a value, it was copied from a valid trade agreement.</span></span> <span data-ttu-id="5ec83-146">如果此字段为空，且您想给该客户行折扣，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-146">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span> 
    - <span data-ttu-id="5ec83-147">**净额**字段包含根据行数和折扣调整后单价计算的值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-147">The **Net** amount field contains a value that is calculated based on the line's quantity and unit price adjusted by discounts.</span></span>  <span data-ttu-id="5ec83-148">您可以用另外的值覆盖该计算值。</span><span class="sxs-lookup"><span data-stu-id="5ec83-148">You can override the calculated value to a different one.</span></span>  

## <a name="review-the-order-totals"></a><span data-ttu-id="5ec83-149">查看订单总计</span><span class="sxs-lookup"><span data-stu-id="5ec83-149">Review the order totals</span></span>
1. <span data-ttu-id="5ec83-150">在**操作窗格**上，选择**销售订单**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-150">On the **Action Pane**, select **Sales order**.</span></span>
2. <span data-ttu-id="5ec83-151">选择**合计**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-151">Select **Totals**.</span></span>
    
    <span data-ttu-id="5ec83-152">**合计**页面显示整个订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5ec83-152">The **Totals** page displays details about the entire order.</span></span> <span data-ttu-id="5ec83-153">这包括小计金额（最后单行折扣调整后所有行净额的总和）、总发票金额（最后订单折扣调整后的小计金额）、费用、销售税、客户信用额度情况和其他信息。</span><span class="sxs-lookup"><span data-stu-id="5ec83-153">This includes the subtotal amount, which is a sum of all line net amounts adjusted for eventual line discounts, the total invoice amount, which is a subtotal amount adjusted for eventual order-level discount, charges, and sales tax, the customer credit limit situation, and more.</span></span> <span data-ttu-id="5ec83-154">发票金额是显示在客户的发票单据上的金额。</span><span class="sxs-lookup"><span data-stu-id="5ec83-154">The invoice amount is the amount that will appear on the customer's invoice document.</span></span>  
    
3. <span data-ttu-id="5ec83-155">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5ec83-155">Select **OK**.</span></span>
