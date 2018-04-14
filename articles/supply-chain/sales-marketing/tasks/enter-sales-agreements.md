--- 
title: "输入销售协议"
description: "该过程向您显示如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的的销售协议。"
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
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bdf7b21d216f41f97a5b766f2de27cce918290c7
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="f2285-103">输入销售协议</span><span class="sxs-lookup"><span data-stu-id="f2285-103">Enter sales agreements</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2285-104">该过程向您显示如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的的销售协议。</span><span class="sxs-lookup"><span data-stu-id="f2285-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="f2285-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="f2285-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="f2285-106">设置销售协议标题</span><span class="sxs-lookup"><span data-stu-id="f2285-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="f2285-107">转到“销售和市场”>“销售协议”>“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="f2285-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="f2285-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f2285-108">Click New.</span></span>
3. <span data-ttu-id="f2285-109">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f2285-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f2285-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f2285-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f2285-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f2285-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f2285-112">在“销售协议分类”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f2285-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f2285-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f2285-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f2285-114">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="f2285-114">Expand the General section.</span></span>
9. <span data-ttu-id="f2285-115">在“默认承诺”字段中，选择“产品价值承诺”。</span><span class="sxs-lookup"><span data-stu-id="f2285-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="f2285-116">承诺类型是您必须在协议中分配的用于定义如何执行协议合同的一个强制性条件。</span><span class="sxs-lookup"><span data-stu-id="f2285-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="f2285-117">四种预定义类型可以设置客户的承诺目标，表示为数量或值。</span><span class="sxs-lookup"><span data-stu-id="f2285-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="f2285-118">数量承诺类型仅适用于特定的产品，但是基于值的类型适用于特定和非特定的产品销售。</span><span class="sxs-lookup"><span data-stu-id="f2285-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="f2285-119">在“到期日期”字段中，将日期设置为您想要协议终止的将来的日期。</span><span class="sxs-lookup"><span data-stu-id="f2285-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="f2285-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2285-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="f2285-121">设置产品值承诺行</span><span class="sxs-lookup"><span data-stu-id="f2285-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="f2285-122">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="f2285-122">Click Add line.</span></span>
2. <span data-ttu-id="f2285-123">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f2285-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f2285-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f2285-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f2285-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f2285-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f2285-126">为协议所选择的承诺类型会影响您可以为协议行输入信息的种类。</span><span class="sxs-lookup"><span data-stu-id="f2285-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="f2285-127">例如，对于基于值的协议，必须为客户承诺购买您的货物的金额指定总净额（使用协定币种）。</span><span class="sxs-lookup"><span data-stu-id="f2285-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="f2285-128">在此示例中，由于您在为某一客户创建的购买特定值的产品的协议，所以该行上的“数量和单位”字段不可用。</span><span class="sxs-lookup"><span data-stu-id="f2285-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="f2285-129">在“净额”字段中，输入客户承诺要购买产品的金额。</span><span class="sxs-lookup"><span data-stu-id="f2285-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="f2285-130">在“折扣百分比”字段，输入与该协议相关的应用于客户销售订单行的百分值。</span><span class="sxs-lookup"><span data-stu-id="f2285-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="f2285-131">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="f2285-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="f2285-132">在“执行最大”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f2285-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="f2285-133">强制选择“最大”意味着使用承诺的特价、折扣和/或付款期限的所有销售订单行的总金额不能超过该承诺所指定的金额。</span><span class="sxs-lookup"><span data-stu-id="f2285-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="f2285-134">最小和最大发放金额指定了使用所选协议的每个销售订单的销售值的范围。</span><span class="sxs-lookup"><span data-stu-id="f2285-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="f2285-135">展开“销售协议标题”部分。</span><span class="sxs-lookup"><span data-stu-id="f2285-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="f2285-136">除非协议的状态设置为“有效”，否则销售订单不能与协议关联，因而不能参与协议的履行。</span><span class="sxs-lookup"><span data-stu-id="f2285-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="f2285-137">在此阶段，您可以手动更改状态。</span><span class="sxs-lookup"><span data-stu-id="f2285-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="f2285-138">但是，当您确认客户的协议时，状态通常将更改。</span><span class="sxs-lookup"><span data-stu-id="f2285-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="f2285-139">在“操作窗格”上单击“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="f2285-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="f2285-140">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="f2285-140">Click Confirmation.</span></span>
    * <span data-ttu-id="f2285-141">确保“标记协议”作为有效选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="f2285-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="f2285-142">在“打印报告”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f2285-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="f2285-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f2285-143">Click OK.</span></span>
14. <span data-ttu-id="f2285-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2285-144">Close the page.</span></span>
    * <span data-ttu-id="f2285-145">协议现在生效，您可以将客户订单链接到协议，来抵消承诺目标。</span><span class="sxs-lookup"><span data-stu-id="f2285-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


