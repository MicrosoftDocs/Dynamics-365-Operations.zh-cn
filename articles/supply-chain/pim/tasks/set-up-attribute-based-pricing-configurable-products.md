---
title: 为可配置产品设置基于属性的定价
description: 本主题介绍如何设置基于属性的定价。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921233"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="494ac-103">为可配置产品设置基于属性的定价</span><span class="sxs-lookup"><span data-stu-id="494ac-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="494ac-104">本主题介绍如何设置基于属性的定价。</span><span class="sxs-lookup"><span data-stu-id="494ac-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="494ac-105">首先必须有一个拥有一个或多个组件和属性的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="494ac-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="494ac-106">此示例使用 USMF 演示数据公司中的高端扬声器产品模型。</span><span class="sxs-lookup"><span data-stu-id="494ac-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="494ac-107">通常，产品经理使用此过程。</span><span class="sxs-lookup"><span data-stu-id="494ac-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="494ac-108">创建新的价格模型</span><span class="sxs-lookup"><span data-stu-id="494ac-108">Create a new price model</span></span>

1. <span data-ttu-id="494ac-109">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="494ac-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="494ac-110">在列表中，选择 **高端扬声器** 行，但是不选择名称的链接。</span><span class="sxs-lookup"><span data-stu-id="494ac-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="494ac-111">在操作窗格上，选择 **模型**。</span><span class="sxs-lookup"><span data-stu-id="494ac-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="494ac-112">选择 **价格模型**。</span><span class="sxs-lookup"><span data-stu-id="494ac-112">Select **Price models**.</span></span>
1. <span data-ttu-id="494ac-113">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="494ac-113">Select **New**.</span></span>
1. <span data-ttu-id="494ac-114">在 **价格模型名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="494ac-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="494ac-115">使用易于识别模型的名称。</span><span class="sxs-lookup"><span data-stu-id="494ac-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="494ac-116">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="494ac-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="494ac-117">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="494ac-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="494ac-118">添加价格元素</span><span class="sxs-lookup"><span data-stu-id="494ac-118">Add price elements</span></span>

1. <span data-ttu-id="494ac-119">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="494ac-119">Select **Edit**.</span></span> <span data-ttu-id="494ac-120">产品模型中的每个组件可以有一个基价元素和任意数量的价格表达式规则。</span><span class="sxs-lookup"><span data-stu-id="494ac-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="494ac-121">还可以添加不同币种的价格。</span><span class="sxs-lookup"><span data-stu-id="494ac-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="494ac-122">在 **基价表达式** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="494ac-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="494ac-123">例如，键入“100”。</span><span class="sxs-lookup"><span data-stu-id="494ac-123">For example, type 100.</span></span> <span data-ttu-id="494ac-124">基价表达式可以是数值，也可以包含涉及一个或多个属性的算术计算。</span><span class="sxs-lookup"><span data-stu-id="494ac-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="494ac-125">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="494ac-125">Select **Add**.</span></span>
4. <span data-ttu-id="494ac-126">在 **名称** 字段中，键入 `Rosewood`。</span><span class="sxs-lookup"><span data-stu-id="494ac-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="494ac-127">价格表达式名称帮助识别价格元素的含义。</span><span class="sxs-lookup"><span data-stu-id="494ac-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="494ac-128">在此示例中，我们为红木扬声器机箱装饰选件创建一个价格元素。</span><span class="sxs-lookup"><span data-stu-id="494ac-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="494ac-129">选择 **编辑条件**。</span><span class="sxs-lookup"><span data-stu-id="494ac-129">Select **Edit condition**.</span></span> <span data-ttu-id="494ac-130">价格条件帮助确保仅当存在特定属性组合时，销售价中才包含价格表达式元素。</span><span class="sxs-lookup"><span data-stu-id="494ac-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="494ac-131">在 **ConstraintBody** 字段中，输入 `CabinetFinish=="Rosewood"`。</span><span class="sxs-lookup"><span data-stu-id="494ac-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="494ac-132">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="494ac-132">Select **OK**.</span></span>
8. <span data-ttu-id="494ac-133">在 **表达式** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="494ac-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="494ac-134">例如，键入 `50`。</span><span class="sxs-lookup"><span data-stu-id="494ac-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="494ac-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="494ac-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]