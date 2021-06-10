---
title: 定义福利资格规则和策略
description: 本文将向您展示创建福利资格规则和政策并将规则分配给福利的方法。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053145"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="d0988-103">定义福利资格规则和策略</span><span class="sxs-lookup"><span data-stu-id="d0988-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d0988-104">本主题将向您展示创建福利资格规则和政策并将规则分配给福利的方法。</span><span class="sxs-lookup"><span data-stu-id="d0988-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="d0988-105">创建福利资格政策规则类型</span><span class="sxs-lookup"><span data-stu-id="d0988-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="d0988-106">转到 **人力资源 > 福利 > 资格 > 福利资格政策规则类型**。</span><span class="sxs-lookup"><span data-stu-id="d0988-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="d0988-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d0988-107">Select **New**.</span></span>
3. <span data-ttu-id="d0988-108">在 **规则名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0988-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="d0988-109">在 **描述** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="d0988-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="d0988-110">在 **查询名称** 字段中，选择下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="d0988-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d0988-111">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d0988-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="d0988-112">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d0988-112">Select **Save**.</span></span>
8. <span data-ttu-id="d0988-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d0988-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="d0988-114">福利资格策略</span><span class="sxs-lookup"><span data-stu-id="d0988-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="d0988-115">转到 **人力资源 > 福利 > 资格 > 福利资格政策**。</span><span class="sxs-lookup"><span data-stu-id="d0988-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="d0988-116">选择一个现有的福利政策。</span><span class="sxs-lookup"><span data-stu-id="d0988-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="d0988-117">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d0988-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="d0988-118">切换 **政策组织** 部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="d0988-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="d0988-119">您可以添加或删除您想要加入政策内的所有组织。</span><span class="sxs-lookup"><span data-stu-id="d0988-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="d0988-120">展开或折叠 **策略规则** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0988-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="d0988-121">在列表中，查找并选择以前创建的政策规则。</span><span class="sxs-lookup"><span data-stu-id="d0988-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="d0988-122">选择 **创建策略规则**。</span><span class="sxs-lookup"><span data-stu-id="d0988-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="d0988-123">在 **生效日期** 字段中，输入您希望政策开始生效的日期。</span><span class="sxs-lookup"><span data-stu-id="d0988-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="d0988-124">如果您希望这些更改生效，则设置有效截止日期，以允许您以后对政策规则作出更改，而无需返回到政策。</span><span class="sxs-lookup"><span data-stu-id="d0988-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="d0988-125">如果需要，在 **添加条件** 字段中添加 where 子句。</span><span class="sxs-lookup"><span data-stu-id="d0988-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="d0988-126">例如，如果您希望规则仅适用于销售经理，您可以创建 where 子句进行规定：Where 职位描述等于销售经理。</span><span class="sxs-lookup"><span data-stu-id="d0988-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="d0988-127">您可以在规则中一起添加多个 where 语句。</span><span class="sxs-lookup"><span data-stu-id="d0988-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="d0988-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d0988-128">Select **OK**.</span></span>
11. <span data-ttu-id="d0988-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d0988-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="d0988-130">分配福利规则</span><span class="sxs-lookup"><span data-stu-id="d0988-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="d0988-131">转到 **人力资源 > 福利 > 福利**。</span><span class="sxs-lookup"><span data-stu-id="d0988-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="d0988-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d0988-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d0988-133">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d0988-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="d0988-134">展开或折叠 **资格规则** 部分。</span><span class="sxs-lookup"><span data-stu-id="d0988-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="d0988-135">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="d0988-135">Select **Edit**.</span></span>
6. <span data-ttu-id="d0988-136">在 **资格** 字段中，选择规则。</span><span class="sxs-lookup"><span data-stu-id="d0988-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="d0988-137">在 **规则类型** 中，查找并选择以前创建的规则。</span><span class="sxs-lookup"><span data-stu-id="d0988-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="d0988-138">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d0988-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="d0988-139">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d0988-139">Select **Save**.</span></span>
11. <span data-ttu-id="d0988-140">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="d0988-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]