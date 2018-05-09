--- 
title: "创建销售订单"
description: "此过程说明如何创建销售订单。"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 65a91c64c7a622fda2e2358b3a2d46cb05b9bf3a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="create-sales-orders"></a><span data-ttu-id="d984f-103">创建销售订单</span><span class="sxs-lookup"><span data-stu-id="d984f-103">Create sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d984f-104">此过程说明如何创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="d984f-104">This procedure shows you how to create a sales order.</span></span> <span data-ttu-id="d984f-105">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="d984f-105">You can use the procedure in demo data company USMF.</span></span> <span data-ttu-id="d984f-106">销售订单通常由销售订单处理器创建。</span><span class="sxs-lookup"><span data-stu-id="d984f-106">Sales orders are typically created by a sales order processor.</span></span> 




## <a name="enter-sales-order-header-details"></a><span data-ttu-id="d984f-107">输入销售订单抬头详细信息</span><span class="sxs-lookup"><span data-stu-id="d984f-107">Enter sales order header details</span></span>
1. <span data-ttu-id="d984f-108">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="d984f-108">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="d984f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d984f-109">Click New.</span></span>
3. <span data-ttu-id="d984f-110">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d984f-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d984f-111">在列表中，找到并选择客户记录。</span><span class="sxs-lookup"><span data-stu-id="d984f-111">In the list, find and select the customer record.</span></span>
    * <span data-ttu-id="d984f-112">在本示例中，选择客户编号 US-004。</span><span class="sxs-lookup"><span data-stu-id="d984f-112">For this example, select customer number US-004.</span></span>  
5. <span data-ttu-id="d984f-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d984f-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d984f-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d984f-114">Click OK.</span></span>

## <a name="enter-sales-order-line-details"></a><span data-ttu-id="d984f-115">输入销售订单行详细信息</span><span class="sxs-lookup"><span data-stu-id="d984f-115">Enter sales order line details</span></span>
    * <span data-ttu-id="d984f-116">您的公司销售的产品可能款式不同，可以不同维度区分，例如配置、颜色、大小和样式。</span><span class="sxs-lookup"><span data-stu-id="d984f-116">The products sold by your organization may come in variants differentiated by dimensions, such as configuration, color, size, and style.</span></span> <span data-ttu-id="d984f-117">此外，产品可以设置为使用存储维度，如站点、仓库、托盘和货架维度，例如批号和序列号。</span><span class="sxs-lookup"><span data-stu-id="d984f-117">Also, products may be set up to use storage dimensions, such as site, warehouse, and pallet, and racking dimensions, such as batch and serial numbers.</span></span> <span data-ttu-id="d984f-118">在分配这些维度时，您必须在订单行选择维度的数值。</span><span class="sxs-lookup"><span data-stu-id="d984f-118">When these dimensions are assigned, you must select the values for those dimensions on the order line.</span></span> <span data-ttu-id="d984f-119">为了提高订单输入效率，您可能要添加各自的维度字段到订单网格中。</span><span class="sxs-lookup"><span data-stu-id="d984f-119">To improve order entry efficiency, you may want to add the respective dimension fields to the order grid.</span></span>  
1. <span data-ttu-id="d984f-120">单击“销售订单行”。</span><span class="sxs-lookup"><span data-stu-id="d984f-120">Click Sales order line.</span></span>
2. <span data-ttu-id="d984f-121">单击“维度”。</span><span class="sxs-lookup"><span data-stu-id="d984f-121">Click Dimensions.</span></span>
    * <span data-ttu-id="d984f-122">在本示例中，选择颜色、位置和仓库维度。</span><span class="sxs-lookup"><span data-stu-id="d984f-122">For this example, select the Color, Site and Warehouse dimensions.</span></span> <span data-ttu-id="d984f-123">您选择的维度将显示在订单网格中。</span><span class="sxs-lookup"><span data-stu-id="d984f-123">The dimensions you select here will appear in the sales order grid.</span></span> <span data-ttu-id="d984f-124">如果想要保存您的选择，则将“保存设置”选项设为“是”。</span><span class="sxs-lookup"><span data-stu-id="d984f-124">If you want your selections to persist, set the Save setup option to Yes.</span></span>   
3. <span data-ttu-id="d984f-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d984f-125">Click OK.</span></span>
4. <span data-ttu-id="d984f-126">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d984f-126">In the Item number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d984f-127">在本示例中，单击“物料编号 T0004”。</span><span class="sxs-lookup"><span data-stu-id="d984f-127">For this example, select item number T0004.</span></span>
6. <span data-ttu-id="d984f-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d984f-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d984f-129">如果物料是销售类别的一部分，物料名称将在“销售类别”字段自动显示。</span><span class="sxs-lookup"><span data-stu-id="d984f-129">If the item is part of a sales category, the item name will automatically appear in the Sales category field.</span></span>  
    * <span data-ttu-id="d984f-130">如果产品维度字段已包含一个值，则该值是从定义为默认产品维度的产品记录中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="d984f-130">If product dimension fields already contain a value, this is because the value was copied from the product record where it is defined as a default product dimension.</span></span> <span data-ttu-id="d984f-131">您可以随时更改默认值。</span><span class="sxs-lookup"><span data-stu-id="d984f-131">You can change the default value at any time.</span></span>   
7. <span data-ttu-id="d984f-132">在“颜色”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d984f-132">In the Color field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d984f-133">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d984f-133">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d984f-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d984f-134">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d984f-135">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="d984f-135">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d984f-136">如果物料销售单位与采购、生产和存储单位不同，且测量销售单位在产品记录中有设置，则该值将在“单位”字段显示。</span><span class="sxs-lookup"><span data-stu-id="d984f-136">If the item is sold in different units than when it’s purchased, produced, and stored, and a sales unit of measure is set on the product record, this value will be shown in the Unit field.</span></span> <span data-ttu-id="d984f-137">您可以随时更改该值。</span><span class="sxs-lookup"><span data-stu-id="d984f-137">You can change the value at any time.</span></span>   
    * <span data-ttu-id="d984f-138">如果“站点”字段已包含一个值，则该值是从订单抬头或产品相关的订单设置中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="d984f-138">If the Site field already contains a value, the value was copied from the order header or from the order settings that are associated with the product.</span></span> <span data-ttu-id="d984f-139">您可以随时更改该值。</span><span class="sxs-lookup"><span data-stu-id="d984f-139">You can change the value at any time.</span></span> <span data-ttu-id="d984f-140">如果此字段为空，则选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d984f-140">If the field is empty, select a value.</span></span>   
    * <span data-ttu-id="d984f-141">如果“单价”字段已包含一个值，则该值是从有效贸易协议或产品记录中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="d984f-141">If the Unit price field already contains a value, the value was copied from a valid trade agreement, or from the product record.</span></span> <span data-ttu-id="d984f-142">（单价还可来自销售协议，但是销售协议的销售订单创建流程与此处显示的不同。）如果此字段为空，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d984f-142">(The unit price can also originate from a sales agreement, but the process for creating sales orders from sales agreements is different to the one shown here.) If the field is empty, enter a value.</span></span>   
    * <span data-ttu-id="d984f-143">“折扣”字段包含一个产品单位的折扣金额。</span><span class="sxs-lookup"><span data-stu-id="d984f-143">The Discount field contains a discount amount per product unit.</span></span> <span data-ttu-id="d984f-144">若要计算总折扣金额，应用单行折扣值乘以行数。</span><span class="sxs-lookup"><span data-stu-id="d984f-144">To calculate the total line discount amount, the discount value is multiplied by line quantity.</span></span>    <span data-ttu-id="d984f-145">如果“折扣”字段已包含一个值，则该值是从有效贸易协议中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="d984f-145">If the Discount field already contains a value, the value was copied from a valid trade agreement.</span></span> <span data-ttu-id="d984f-146">如果此字段为空，且您想给该客户行折扣，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d984f-146">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="d984f-147">“折扣百分比”字段包含计算全部行总额时减去的百分比值。</span><span class="sxs-lookup"><span data-stu-id="d984f-147">The Discount percent field contains a percentage value by which the total line gross amount is to be reduced.</span></span>  <span data-ttu-id="d984f-148">如果“折扣百分比”字段已包含一个值，则该值是从有效贸易协议中复制过来的。</span><span class="sxs-lookup"><span data-stu-id="d984f-148">If the Discount percent field already contains a value, it was copied from a valid trade agreement.</span></span> <span data-ttu-id="d984f-149">如果此字段为空，且您想给该客户行折扣，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d984f-149">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="d984f-150">“净额”字段包含根据行数和折扣调整后单价计算的值。</span><span class="sxs-lookup"><span data-stu-id="d984f-150">The Net amount field contains a value that is calculated based on the line's quantity and unit price adjusted by discounts.</span></span>  <span data-ttu-id="d984f-151">您可以用另外的值覆盖该计算值。</span><span class="sxs-lookup"><span data-stu-id="d984f-151">You can override the calculated value to a different one.</span></span>  

## <a name="review-the-order-totals"></a><span data-ttu-id="d984f-152">查看订单总计</span><span class="sxs-lookup"><span data-stu-id="d984f-152">Review the order totals</span></span>
1. <span data-ttu-id="d984f-153">在操作窗格上，单击“销售订单”。</span><span class="sxs-lookup"><span data-stu-id="d984f-153">On the Action Pane, click Sales order.</span></span>
2. <span data-ttu-id="d984f-154">单击“总计”。</span><span class="sxs-lookup"><span data-stu-id="d984f-154">Click Totals.</span></span>
    * <span data-ttu-id="d984f-155">总计页面显示整个订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d984f-155">The Totals page displays details about the entire order.</span></span> <span data-ttu-id="d984f-156">这包括小计金额（最后单行折扣调整后所有行净额的总和）、总发票金额（最后订单折扣调整后的小计金额）、费用、销售税、客户信用额度情况和其他信息。</span><span class="sxs-lookup"><span data-stu-id="d984f-156">This includes the subtotal amount, which is a sum of all line net amounts adjusted for eventual line discounts, the total invoice amount, which is a subtotal amount adjusted for eventual order-level discount, charges, and sales tax, the customer credit limit situation, and more.</span></span>  <span data-ttu-id="d984f-157">发票金额是显示在客户的发票单据上的金额。</span><span class="sxs-lookup"><span data-stu-id="d984f-157">The invoice amount is the amount that will appear on the customer's invoice document.</span></span>  
3. <span data-ttu-id="d984f-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d984f-158">Click OK.</span></span>


