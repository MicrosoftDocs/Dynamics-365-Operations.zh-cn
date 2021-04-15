---
title: 输入销售协议
description: 此主题介绍如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的销售协议。
author: omulvad
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 675eeda04880601f0261c6ae5e5a49de38f75a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810838"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="dca51-103">输入销售协议</span><span class="sxs-lookup"><span data-stu-id="dca51-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dca51-104">此主题介绍如何向您的客户创建承诺：在超限时间采购议定数量的产品将获得特定的销售折扣的销售协议。</span><span class="sxs-lookup"><span data-stu-id="dca51-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="dca51-105">您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="dca51-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="dca51-106">设置销售协议标题</span><span class="sxs-lookup"><span data-stu-id="dca51-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="dca51-107">在导航窗格中，转到 **模块 > 销售和营销 > 销售协议 > 销售协议**。</span><span class="sxs-lookup"><span data-stu-id="dca51-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="dca51-108">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dca51-108">Select **New**.</span></span>
3. <span data-ttu-id="dca51-109">在 **客户帐户** 字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="dca51-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="dca51-110">在 **销售协议分类** 字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="dca51-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="dca51-111">展开 **常规** 部分。</span><span class="sxs-lookup"><span data-stu-id="dca51-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="dca51-112">在 **默认承诺** 字段中，选择 **产品价值承诺**。</span><span class="sxs-lookup"><span data-stu-id="dca51-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="dca51-113">承诺类型是您必须在协议中分配的用于定义如何执行协议合同的一个强制性条件。</span><span class="sxs-lookup"><span data-stu-id="dca51-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="dca51-114">四种预定义类型可以设置客户的承诺目标，表示为数量或值。</span><span class="sxs-lookup"><span data-stu-id="dca51-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="dca51-115">数量承诺类型仅适用于特定的产品，但是基于值的类型适用于特定和非特定的产品销售。</span><span class="sxs-lookup"><span data-stu-id="dca51-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="dca51-116">在 **到期日期** 字段中，将日期设置为您想要协议终止的将来的日期。</span><span class="sxs-lookup"><span data-stu-id="dca51-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="dca51-117">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dca51-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="dca51-118">设置产品值承诺行</span><span class="sxs-lookup"><span data-stu-id="dca51-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="dca51-119">选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="dca51-119">Select **Add line**.</span></span>
2. <span data-ttu-id="dca51-120">在 **物料编号** 字段中，从下拉菜单选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="dca51-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="dca51-121">为协议所选择的承诺类型会影响您可以为协议行输入信息的种类。</span><span class="sxs-lookup"><span data-stu-id="dca51-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="dca51-122">例如，对于基于值的协议，必须为客户承诺购买您的货物的金额指定总净额（使用协定币种）。</span><span class="sxs-lookup"><span data-stu-id="dca51-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="dca51-123">在此示例中，由于您在为某一客户创建购买特定值的产品的协议，所以该行上的 **数量** 和 **单位** 字段不可用。</span><span class="sxs-lookup"><span data-stu-id="dca51-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="dca51-124">在 **净额** 字段中，输入客户承诺要购买产品的金额。</span><span class="sxs-lookup"><span data-stu-id="dca51-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="dca51-125">在 **折扣百分比** 字段，输入与该协议相关的应用于客户销售订单行的百分值。</span><span class="sxs-lookup"><span data-stu-id="dca51-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="dca51-126">展开 **行详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="dca51-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="dca51-127">在 **执行最大** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="dca51-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="dca51-128">选择 **执行最大** 意味着使用承诺的特价、折扣和/或付款期限的所有销售订单行的总金额不能超过该承诺所指定的金额。</span><span class="sxs-lookup"><span data-stu-id="dca51-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="dca51-129">最小和最大发放金额指定了使用所选协议的每个销售订单的销售值的范围。</span><span class="sxs-lookup"><span data-stu-id="dca51-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="dca51-130">展开 **销售协议标题** 部分。</span><span class="sxs-lookup"><span data-stu-id="dca51-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="dca51-131">除非协议的状态设置为 **有效**，否则销售订单不能与协议关联，因而不能参与协议的履行。</span><span class="sxs-lookup"><span data-stu-id="dca51-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="dca51-132">在此阶段，您可以手动更改状态。</span><span class="sxs-lookup"><span data-stu-id="dca51-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="dca51-133">但是，当您确认客户的协议时，状态通常将更改。</span><span class="sxs-lookup"><span data-stu-id="dca51-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="dca51-134">在操作窗格上选择 **销售协议**。</span><span class="sxs-lookup"><span data-stu-id="dca51-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="dca51-135">选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="dca51-135">Select **Confirmation**.</span></span> <span data-ttu-id="dca51-136">请确保将 **标记协议为有效** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="dca51-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="dca51-137">在 **打印报表** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="dca51-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="dca51-138">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dca51-138">Select **OK**.</span></span>
12. <span data-ttu-id="dca51-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dca51-139">Close the page.</span></span> <span data-ttu-id="dca51-140">此协议现在已生效。</span><span class="sxs-lookup"><span data-stu-id="dca51-140">The agreement is now effective.</span></span> <span data-ttu-id="dca51-141">您可以将客户订单链接到协议，来抵消承诺目标。</span><span class="sxs-lookup"><span data-stu-id="dca51-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]