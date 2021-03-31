---
title: 创建采购策略
description: 本主题显示如何创建与您的采购业务流程一致的采购政策。
author: RichardLuan
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8d29f4bd5840ff70fd918a05d68aa043216e27f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211902"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="d59bf-103">创建采购策略</span><span class="sxs-lookup"><span data-stu-id="d59bf-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d59bf-104">本主题显示如何创建与您的采购业务流程一致的采购政策。</span><span class="sxs-lookup"><span data-stu-id="d59bf-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="d59bf-105">在您可以创建采购政策之前，必须设置采购政策参数。</span><span class="sxs-lookup"><span data-stu-id="d59bf-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="d59bf-106">可以创建、修改和废弃采购政策，但不能删除采购政策。</span><span class="sxs-lookup"><span data-stu-id="d59bf-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="d59bf-107">此过程通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="d59bf-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="d59bf-108">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="d59bf-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="d59bf-109">设置政策参数</span><span class="sxs-lookup"><span data-stu-id="d59bf-109">Set up policy parameters</span></span>
1. <span data-ttu-id="d59bf-110">在导航窗格中，转到 **模块 > 采购 > 设置 > 策略 > 采购策略**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="d59bf-111">在操作窗格中，选择 **参数**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-111">On the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="d59bf-112">政策优先级规则适用于组织中的不同级别。</span><span class="sxs-lookup"><span data-stu-id="d59bf-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="d59bf-113">显示的组织单元取决于组织的层次结构，以及已经为层次结构中的哪些级别分配了采购内部控制用途。</span><span class="sxs-lookup"><span data-stu-id="d59bf-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="d59bf-114">例如，您的组织可能有法人、成本中心、地区和部门，但是可能其中只有一部分有采购内部控制的层次结构用途。</span><span class="sxs-lookup"><span data-stu-id="d59bf-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="d59bf-115">默认情况下，类型为“公司”的组织可用。</span><span class="sxs-lookup"><span data-stu-id="d59bf-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="d59bf-116">单击 **政策规则类型参数** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d59bf-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="d59bf-117">在树中，转到 **采购政策 > 采购申请控制规则**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="d59bf-118">您以策略级别为策略解决方法定义优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="d59bf-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="d59bf-119">但是，对于某些策略类型，您可以为单独的策略规则的类型覆盖优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="d59bf-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="d59bf-120">例如，您可以将采购政策的优先级顺序定义为：成本中心、部门、公司。</span><span class="sxs-lookup"><span data-stu-id="d59bf-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="d59bf-121">对于目录策略规则，您可能希望优先级顺序为：部门、成本中心、公司。</span><span class="sxs-lookup"><span data-stu-id="d59bf-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="d59bf-122">可以为目录策略规则更改优先顺序。</span><span class="sxs-lookup"><span data-stu-id="d59bf-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="d59bf-123">工作人员创建申请时，显示的目录由与该工作人员的部门，随后是与其成本中心，再然后是与其公司关联的政策决定。</span><span class="sxs-lookup"><span data-stu-id="d59bf-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="d59bf-124">如果列出了多个组织级别，可使用上下箭头设置采购申请控制规则的优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="d59bf-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="d59bf-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d59bf-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="d59bf-126">创建新策略</span><span class="sxs-lookup"><span data-stu-id="d59bf-126">Create a new policy</span></span>
1. <span data-ttu-id="d59bf-127">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-127">Select **New**.</span></span>
2. <span data-ttu-id="d59bf-128">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d59bf-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="d59bf-129">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d59bf-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="d59bf-130">单个采购政策仅可应用于一个组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d59bf-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="d59bf-131">例如，您可以有一个层次结构称为“地理”，一个称为“部门”，这两个层次结构分别有不同的采购政策。</span><span class="sxs-lookup"><span data-stu-id="d59bf-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="d59bf-132">选择政策应适用于的组织。</span><span class="sxs-lookup"><span data-stu-id="d59bf-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="d59bf-133">选择箭头添加所选组织。</span><span class="sxs-lookup"><span data-stu-id="d59bf-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="d59bf-134">可以重复执行此过程添加更多组织。</span><span class="sxs-lookup"><span data-stu-id="d59bf-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="d59bf-135">添加政策规则</span><span class="sxs-lookup"><span data-stu-id="d59bf-135">Add a policy rule</span></span>
1. <span data-ttu-id="d59bf-136">在 **政策规则类型** 列表中，选择 **申请用途规则**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="d59bf-137">您将创建一个规则，该规则把默认申请用途设置为类型“消耗量”，但是允许改为选择“补货”类型。</span><span class="sxs-lookup"><span data-stu-id="d59bf-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="d59bf-138">选择 **创建策略规则**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="d59bf-139">选择 **允许手动覆盖** 字段中的 **是**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="d59bf-140">选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="d59bf-140">Select **Close**.</span></span>
- <span data-ttu-id="d59bf-141">现在可为采购政策设置其他政策规则。</span><span class="sxs-lookup"><span data-stu-id="d59bf-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="d59bf-142">请注意，政策规则类型不能有在一个采购政策内同时有效的重叠规则。</span><span class="sxs-lookup"><span data-stu-id="d59bf-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]