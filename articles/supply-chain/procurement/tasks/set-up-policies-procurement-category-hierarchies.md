---
title: 设置采购类别层次结构的策略
description: 使用此过程设置类别中订购产品的规则。
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc01793ee83444e5c7097021c19aeda80a132e6
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017080"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="0e7fe-103">设置采购类别层次结构的策略</span><span class="sxs-lookup"><span data-stu-id="0e7fe-103">Set up policies for procurement category hierarchies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e7fe-104">使用此过程设置类别中订购产品的规则。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="0e7fe-105">规则是为具体采购政策定义的。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="0e7fe-106">类别访问策略规则控制员工在创建申请时有权访问的采购类别。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="0e7fe-107">在创建申请时，应采用的采购政策和类别访问规则由员工所属法人和运营单位确定。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="0e7fe-108">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="0e7fe-109">此任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="0e7fe-110">查找采购政策</span><span class="sxs-lookup"><span data-stu-id="0e7fe-110">Find the procurement policy</span></span>
1. <span data-ttu-id="0e7fe-111">在导航窗格中，转到 **模块 > 采购 > 设置 > 策略 > 采购策略**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-111">In the Navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="0e7fe-112">单击“采购政策 USMF”政策中的链接。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-112">Click the link on the 'Procurement Policy USMF' policy.</span></span> <span data-ttu-id="0e7fe-113">这是您将为其添加规则的政策。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-113">This is the policy that you'll add a rule to.</span></span> <span data-ttu-id="0e7fe-114">该政策必须是有效政策。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="0e7fe-115">创建类别访问规则</span><span class="sxs-lookup"><span data-stu-id="0e7fe-115">Create a category access rule</span></span>
1. <span data-ttu-id="0e7fe-116">展开 **政策规则** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-116">Expand the **Policy rules** fastTab.</span></span>
2. <span data-ttu-id="0e7fe-117">在 **政策规则类型** 列表中，选择 **类别访问政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-117">In the **Policy rule type** list, select the **Category access policy rule**.</span></span> <span data-ttu-id="0e7fe-118">如果 **创建政策规则** 按钮灰显，这是因为“类别访问”已经有一个有效政策规则。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-118">If the **Create policy rule** button is dimmed, it's because there's already an active policy rule for Category access.</span></span> <span data-ttu-id="0e7fe-119">检查 **生效日期** 和 **到期日期** 字段以确定到底是哪个，将其选中，然后单击 **废弃政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-119">Check the **Effective** and **Expiration** fields to determine which it is, then select it, and click **Retire policy rule**.</span></span> <span data-ttu-id="0e7fe-120">如果 **创建政策规则** 按钮可用，则不需要执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-120">If the **Create policy rule** button is available, you don't need to do anything.</span></span>  
3. <span data-ttu-id="0e7fe-121">单击 **创建政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-121">Click **Create policy rule**.</span></span>
4. <span data-ttu-id="0e7fe-122">在 **生效日期** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-122">In the **Effective date** field, enter a date and time.</span></span> <span data-ttu-id="0e7fe-123">时间不得与已处于有效状态的其他规则重合。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-123">The time must not overlap with another rule that's already active.</span></span>  
5. <span data-ttu-id="0e7fe-124">选择将应用此规则的类别。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-124">Select a category that the rule will apply to.</span></span> <span data-ttu-id="0e7fe-125">记下此规则的类别，以后会用到。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-125">Make a note of which category this is – you'll need it later.</span></span> <span data-ttu-id="0e7fe-126">当您选择类别时，其父类别也会添加到选定的类别列表中。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-126">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span> <span data-ttu-id="0e7fe-127">如果要将规则应用于所选类别的所有子类别，请选中 **包括子类别** 复选框。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-127">If you want the rule to apply to all subcategories of the selected category, select the **Include subcategories** check box.</span></span>
6. <span data-ttu-id="0e7fe-128">单击向右箭头添加到 **所选类别** 列表。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-128">Click the right arrow to add to the **Selected categories** list.</span></span>  
4. <span data-ttu-id="0e7fe-129">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-129">Click **OK**.</span></span> <span data-ttu-id="0e7fe-130">如果将 **包括父规则** 选项设置为“是”，并且尚未为子类别定义任何政策规则，还将把为父类别定义的政策规则分配给其子类别。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-130">If you set the **Include parent rule** option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="0e7fe-131">创建类别策略规则</span><span class="sxs-lookup"><span data-stu-id="0e7fe-131">Create a category policy rule</span></span>
1. <span data-ttu-id="0e7fe-132">在 **政策规则类型** 列表中，选择 **类别政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-132">In the **Policy rule type** list, select the **Category policy rule**.</span></span> <span data-ttu-id="0e7fe-133">如果 **创建政策规则** 按钮灰显，请选择有效政策规则，然后单击 **废弃政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-133">If the **Create policy rule** button is dimmed, select the active policy rule, and then click **Retire policy rule**.</span></span>  
2. <span data-ttu-id="0e7fe-134">单击 **创建政策规则**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-134">Click **Create policy rule**.</span></span>
3. <span data-ttu-id="0e7fe-135">在 **生效日期** 字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-135">In the **Effective date** field, enter a date and time.</span></span>
4. <span data-ttu-id="0e7fe-136">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-136">Click **Add**.</span></span>
5. <span data-ttu-id="0e7fe-137">在 **类别** 字段中，选择用于 **类别访问规则** 的同一个类别。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-137">In the **Category** field, select the same category that you used for the **Category access rule**.</span></span>
6. <span data-ttu-id="0e7fe-138">在 **供应商选择** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-138">In the **Vendor selection** field, select an option.</span></span> <span data-ttu-id="0e7fe-139">选择一个规则来控制创建申请时可以为类别选择哪种供应商。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-139">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="0e7fe-140">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-140">Click **Close**.</span></span> <span data-ttu-id="0e7fe-141">您已定义的政策规则针对类型为“消耗量”的申请。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-141">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="0e7fe-142">如果要为类型为“补货”的申请定义政策，请为该政策规则类型创建名称为“补货类别访问政策规则”的规则。</span><span class="sxs-lookup"><span data-stu-id="0e7fe-142">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called "Replenishment category access policy rule".</span></span>  

