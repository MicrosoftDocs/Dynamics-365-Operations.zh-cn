--- 
title: "查找适用的价格和折扣"
description: "该过程会显示如何查找当前对于特定客户有效的产品价格和折扣，无需创建销售订单。"
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
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 7ef63151f352b3664bccd7a59e7417dfddc7470b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/01/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="e7cd6-103">查找适用的价格和折扣</span><span class="sxs-lookup"><span data-stu-id="e7cd6-103">Look up applicable prices and discounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7cd6-104">该过程会显示如何查找当前对于特定客户有效的产品价格和折扣，无需创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="e7cd6-105">该过程用一个具体示例进行示范，您需要遵循该示例，使用 USMF 演示公司，以选择所需的值。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="e7cd6-106">查找适用的价格</span><span class="sxs-lookup"><span data-stu-id="e7cd6-106">Find the applicable price</span></span>
1. <span data-ttu-id="e7cd6-107">转至“销售和营销”>“价格和折扣”>“查找价格”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="e7cd6-108">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e7cd6-109">在列表中，找到并选择客户 US-001。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="e7cd6-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e7cd6-111">在“物料编号”字段中，键入“T0004”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="e7cd6-112">默认情况下，“数量”字段设置为 1。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="e7cd6-113">但是，如果您知道客户打算订购所讨论的物料的订货量，则输入该数值。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="e7cd6-114">如果与客户签订的贸易协议有数量分段，即该产品的价格取决于采购的最小数量，此信息是相关的。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="e7cd6-115">在“日期”字段中，输入客户预计下单的日期。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="e7cd6-116">日期可以是今天或未来的任何日期。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="e7cd6-117">当选定客户在选定日期购买规定数量的选定产品时，系统会立即返回对于该选定产品有效的价格。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="e7cd6-118">在此示例中，如果客户 US-001 今天购买 1 个单位的产品 T0004，每个单位被收取 350 加拿大元。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="e7cd6-119">此价格源自与该客户签订的现行有效的贸易协议。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="e7cd6-120">该页面的其他字段提供了关于产品价格和产品成本（如果在基础产品上设置）以及计算得出的利润率的更多详情。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="e7cd6-121">如果选中“显示相关产品变型”选项，这意味着产品变量还有额外的贸易协议。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="e7cd6-122">单击“显示相关产品变型”复选框。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="e7cd6-123">产品变型列表及其维度信息会显示。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="e7cd6-124">在列表中，标记行中的代表颜色“白色”</span><span class="sxs-lookup"><span data-stu-id="e7cd6-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="e7cd6-125">注意，未根据维度指定时，产品价格现在不同于以前显示的价格。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="e7cd6-126">单击“查看销售价格”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-126">Click View sales prices.</span></span>
    * <span data-ttu-id="e7cd6-127">价格（售价）页会显示适用于产品的所有贸易协议，包括其变型。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="e7cd6-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="e7cd6-129">查找适用的折扣</span><span class="sxs-lookup"><span data-stu-id="e7cd6-129">Find the applicable discount</span></span>
    * <span data-ttu-id="e7cd6-130">确保“客户帐户”字段包含客户编号 US-001</span><span class="sxs-lookup"><span data-stu-id="e7cd6-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="e7cd6-131">在“物料编号”字段中，键入“T0012”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="e7cd6-132">请确保“数量”字段被设置为 1。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="e7cd6-133">产品 T0012 所显示的以下定价详情源自一个或多个贸易协议：单价为 1,000 加拿大元，并且折扣百分比是 5。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="e7cd6-134">将“数量”设置为“20”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="e7cd6-135">增加的订单数量导致提供给客户的行折扣从 5 更改为 7。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="e7cd6-136">“净额”是基于单价、折扣和总数量计算得出的。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="e7cd6-137">单击“查看行折扣”。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-137">Click View line discount.</span></span>
    * <span data-ttu-id="e7cd6-138">产品 T0012 有 2 个单行折扣协议，规定订单行数量为 1-10 的折扣百分比是 5，订单行数量为 10 以上的折扣百分比是 7。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="e7cd6-139">请注意，该折扣适用于产品组，在本示例中，组代码为 01，产品 T0012 包括在其中。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="e7cd6-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e7cd6-140">Close the page.</span></span>


