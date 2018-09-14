--- 
title: "输入销售协议"
description: "该过程向您显示如何创建销售协议，以向一位客户承诺在一段时间内购买的产品达到协商的金额时获得特别折扣。"
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 874fee6de6e5aa5a29c271cc2e3d4cfd96672f3e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="489c0-103">输入销售协议</span><span class="sxs-lookup"><span data-stu-id="489c0-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="489c0-104">该过程向您显示如何创建以下内容的销售协议：向一位客户承诺如果在一段时间内购买的产品达到</span><span class="sxs-lookup"><span data-stu-id="489c0-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="489c0-105">议定的金额，将提供特别折扣。</span><span class="sxs-lookup"><span data-stu-id="489c0-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="489c0-106">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="489c0-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="489c0-107">设置销售协议标题</span><span class="sxs-lookup"><span data-stu-id="489c0-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="489c0-108">转到“销售和市场”>“销售协议”>“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="489c0-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="489c0-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="489c0-109">Click New.</span></span>
3. <span data-ttu-id="489c0-110">在“客户帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="489c0-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="489c0-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="489c0-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="489c0-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="489c0-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="489c0-113">在“销售协议分类”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="489c0-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="489c0-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="489c0-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="489c0-115">展开“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="489c0-115">Expand the General section.</span></span>
9. <span data-ttu-id="489c0-116">在“默认承诺”字段中，选择“产品价值承诺”。</span><span class="sxs-lookup"><span data-stu-id="489c0-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="489c0-117">承诺类型是您必须在协议中分配的用于定义如何执行协议合同的一个强制性条件。</span><span class="sxs-lookup"><span data-stu-id="489c0-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="489c0-118">四种预定义类型可以设置客户的承诺目标，表示为数量或值。</span><span class="sxs-lookup"><span data-stu-id="489c0-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="489c0-119">数量承诺类型仅适用于特定的产品，但是基于值的类型适用于特定和非特定的产品销售。</span><span class="sxs-lookup"><span data-stu-id="489c0-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="489c0-120">在“到期日期”字段中，将日期设置为您想要协议终止的将来的日期。</span><span class="sxs-lookup"><span data-stu-id="489c0-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="489c0-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="489c0-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="489c0-122">设置产品值承诺行</span><span class="sxs-lookup"><span data-stu-id="489c0-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="489c0-123">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="489c0-123">Click Add line.</span></span>
2. <span data-ttu-id="489c0-124">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="489c0-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="489c0-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="489c0-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="489c0-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="489c0-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="489c0-127">为协议所选择的承诺类型会影响您可以为协议行输入信息的种类。</span><span class="sxs-lookup"><span data-stu-id="489c0-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="489c0-128">例如，对于基于值的协议，必须为客户承诺购买您的货物的金额指定总净额（使用协定币种）。</span><span class="sxs-lookup"><span data-stu-id="489c0-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="489c0-129">在此示例中，由于您在为某一客户创建的购买特定值的产品的协议，所以该行上的“数量和单位”字段不可用。</span><span class="sxs-lookup"><span data-stu-id="489c0-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="489c0-130">在“净额”字段中，输入客户承诺要购买产品的金额。</span><span class="sxs-lookup"><span data-stu-id="489c0-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="489c0-131">在“折扣百分比”字段，输入与该协议相关的应用于客户销售订单行的百分值。</span><span class="sxs-lookup"><span data-stu-id="489c0-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="489c0-132">展开“行明细”部分。</span><span class="sxs-lookup"><span data-stu-id="489c0-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="489c0-133">在“执行最大”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="489c0-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="489c0-134">强制选择“最大”意味着使用承诺的特价、折扣和/或付款期限的所有销售订单行的总金额不能超过该承诺所指定的金额。</span><span class="sxs-lookup"><span data-stu-id="489c0-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="489c0-135">最小和最大发放金额指定了使用所选协议的每个销售订单的销售值的范围。</span><span class="sxs-lookup"><span data-stu-id="489c0-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="489c0-136">展开“销售协议标题”部分。</span><span class="sxs-lookup"><span data-stu-id="489c0-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="489c0-137">除非协议的状态设置为“有效”，否则销售订单不能与协议关联，因而不能参与协议的履行。</span><span class="sxs-lookup"><span data-stu-id="489c0-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="489c0-138">在此阶段，您可以手动更改状态。</span><span class="sxs-lookup"><span data-stu-id="489c0-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="489c0-139">但是，当您确认客户的协议时，状态通常将更改。</span><span class="sxs-lookup"><span data-stu-id="489c0-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="489c0-140">在“操作窗格”上单击“销售协议”。</span><span class="sxs-lookup"><span data-stu-id="489c0-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="489c0-141">单击“确认”。</span><span class="sxs-lookup"><span data-stu-id="489c0-141">Click Confirmation.</span></span>
    * <span data-ttu-id="489c0-142">确保“标记协议”作为有效选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="489c0-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="489c0-143">在“打印报告”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="489c0-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="489c0-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="489c0-144">Click OK.</span></span>
14. <span data-ttu-id="489c0-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="489c0-145">Close the page.</span></span>
    * <span data-ttu-id="489c0-146">协议现在生效，您可以将客户订单链接到协议，来抵消承诺目标。</span><span class="sxs-lookup"><span data-stu-id="489c0-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


