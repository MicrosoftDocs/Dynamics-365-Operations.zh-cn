--- 
title: "为可配置产品设置基于属性的定价"
description: "此过程显示如何设置基于属性的定价。"
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b113fb639b5d7c50e519a0225b1e5d8315b7f3a9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="10246-103">为可配置产品设置基于属性的定价</span><span class="sxs-lookup"><span data-stu-id="10246-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10246-104">此过程显示如何设置基于属性的定价。</span><span class="sxs-lookup"><span data-stu-id="10246-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="10246-105">首先必须有一个拥有一个或多个组件和属性的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="10246-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="10246-106">此示例使用 USMF 演示数据公司中的高端扬声器产品模型。</span><span class="sxs-lookup"><span data-stu-id="10246-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="10246-107">通常，产品经理使用此过程。</span><span class="sxs-lookup"><span data-stu-id="10246-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="10246-108">创建新的价格模型</span><span class="sxs-lookup"><span data-stu-id="10246-108">Create a new price model</span></span>
1. <span data-ttu-id="10246-109">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="10246-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="10246-110">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="10246-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="10246-111">在列表中，选择“高端扬声器”行，但是不单击名称的链接。</span><span class="sxs-lookup"><span data-stu-id="10246-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="10246-112">在“操作窗格”上单击“模型”。</span><span class="sxs-lookup"><span data-stu-id="10246-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="10246-113">单击“价格模型”。</span><span class="sxs-lookup"><span data-stu-id="10246-113">Click Price models.</span></span>
6. <span data-ttu-id="10246-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="10246-114">Click New.</span></span>
7. <span data-ttu-id="10246-115">在“价格模型名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="10246-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="10246-116">使用易于识别模型的名称。</span><span class="sxs-lookup"><span data-stu-id="10246-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="10246-117">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="10246-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="10246-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="10246-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="10246-119">添加价格元素</span><span class="sxs-lookup"><span data-stu-id="10246-119">Add price elements</span></span>
1. <span data-ttu-id="10246-120">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="10246-120">Click Edit.</span></span>
    * <span data-ttu-id="10246-121">产品模型中的每个组件可以有一个基价元素和任意数量的价格表达式规则。</span><span class="sxs-lookup"><span data-stu-id="10246-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="10246-122">还可以添加不同币种的价格。</span><span class="sxs-lookup"><span data-stu-id="10246-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="10246-123">在“基价表达式”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="10246-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="10246-124">例如，键入“100”。</span><span class="sxs-lookup"><span data-stu-id="10246-124">For example, type 100.</span></span>   <span data-ttu-id="10246-125">基价表达式可以是数值，也可以包含涉及一个或多个属性的算术计算。</span><span class="sxs-lookup"><span data-stu-id="10246-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="10246-126">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="10246-126">Click Add.</span></span>
4. <span data-ttu-id="10246-127">在“名称”字段中，键入“红木”。</span><span class="sxs-lookup"><span data-stu-id="10246-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="10246-128">价格表达式名称帮助识别价格元素的含义。</span><span class="sxs-lookup"><span data-stu-id="10246-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="10246-129">在此示例中，我们为红木扬声器机箱装饰选件创建一个价格元素。</span><span class="sxs-lookup"><span data-stu-id="10246-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="10246-130">单击“编辑条件”。</span><span class="sxs-lookup"><span data-stu-id="10246-130">Click Edit condition.</span></span>
    * <span data-ttu-id="10246-131">价格条件帮助确保仅当存在特定属性组合时，销售价中才包含价格表达式元素。</span><span class="sxs-lookup"><span data-stu-id="10246-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="10246-132">在“约束体”字段中，输入“机箱装饰 =="红木"”。</span><span class="sxs-lookup"><span data-stu-id="10246-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="10246-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="10246-133">Click OK.</span></span>
8. <span data-ttu-id="10246-134">在“表达式”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="10246-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="10246-135">例如，键入“50”。</span><span class="sxs-lookup"><span data-stu-id="10246-135">For example, type 50.</span></span>  
9. <span data-ttu-id="10246-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="10246-136">Close the page.</span></span>
10. <span data-ttu-id="10246-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="10246-137">Close the page.</span></span>


