---
title: 定义和管理福利计划
description: 人力资源提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。 本文章提供了有关如何设置管理福利的信息。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b976bccf7f5da4483ec8a015f464db764b82a2f1
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197881"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="8139c-104">定义和管理福利计划</span><span class="sxs-lookup"><span data-stu-id="8139c-104">Define and manage a benefits program</span></span>

<span data-ttu-id="8139c-105">Human Resources 提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="8139c-105">Human Resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="8139c-106">本文章提供了有关如何设置和管理福利的信息。</span><span class="sxs-lookup"><span data-stu-id="8139c-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="8139c-107">福利设置</span><span class="sxs-lookup"><span data-stu-id="8139c-107">Benefit setup</span></span>

<span data-ttu-id="8139c-108">您必须先创建每项福利的元素，然后工作人员才能在这些福利中登记。</span><span class="sxs-lookup"><span data-stu-id="8139c-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="8139c-109">这些元素结合类似的福利计划并定义默认设置，如扣缴比率和核算详细信息。</span><span class="sxs-lookup"><span data-stu-id="8139c-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="8139c-110">许多这些设置可在工作人员随后在福利中登记时进行调整。</span><span class="sxs-lookup"><span data-stu-id="8139c-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="8139c-111">对于每个福利计划，组织可提供多个登记选项，或者工作人员可放弃该福利计划中的登记。</span><span class="sxs-lookup"><span data-stu-id="8139c-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="8139c-112">[![福利处理流程](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="8139c-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="8139c-113">福利元素</span><span class="sxs-lookup"><span data-stu-id="8139c-113">Benefit elements</span></span>

<span data-ttu-id="8139c-114">在开始创建福利并在其中注册工作人员之前，您必须定义构成福利的元素：类型、计划和选项。</span><span class="sxs-lookup"><span data-stu-id="8139c-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="8139c-115">**类型** - 某项特定福利计划的集合，如医疗或停车。</span><span class="sxs-lookup"><span data-stu-id="8139c-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="8139c-116">**计划** - 从提供商商定的特定福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="8139c-117">**选项** - 覆盖范围级别，例如：仅员工或员工及其配偶。</span><span class="sxs-lookup"><span data-stu-id="8139c-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="8139c-118">对于每种类型的福利（例如视力或护齿），组织可向其工作人员提供一个或多个计划。</span><span class="sxs-lookup"><span data-stu-id="8139c-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="8139c-119">对于每个计划，该组织可提供不同的选项。</span><span class="sxs-lookup"><span data-stu-id="8139c-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="8139c-120">例如，工作人员可以其年薪的一倍、两倍或三倍购买附加期限的人寿保险。</span><span class="sxs-lookup"><span data-stu-id="8139c-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="8139c-121">计划和选项的每个组合将成为工作人员可登记的福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="8139c-122">[![福利图片](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="8139c-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="8139c-123">资格</span><span class="sxs-lookup"><span data-stu-id="8139c-123">Eligibility</span></span>
<span data-ttu-id="8139c-124">许多因素决定工作人员有资格享有雇主提供的各种类型福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="8139c-125">当您在 Dynamics 365 Human Resources 中创建福利时，可以设置应用于该福利的资格类型。</span><span class="sxs-lookup"><span data-stu-id="8139c-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="8139c-126">您可以向所有工作人员提供福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="8139c-127">例如，某些公司向所有员工提供停车证作为附加福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="8139c-128">当您创建此福利时，将资格设置为**所有工作人员均符合资格**。</span><span class="sxs-lookup"><span data-stu-id="8139c-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="8139c-129">对于其他福利（例如扣押和征收税款），资格不适用。</span><span class="sxs-lookup"><span data-stu-id="8139c-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="8139c-130">当您创建这些类型的福利时，将资格设置为**跳过资格处理**。</span><span class="sxs-lookup"><span data-stu-id="8139c-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="8139c-131">最后，福利资格可基于规则。</span><span class="sxs-lookup"><span data-stu-id="8139c-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="8139c-132">例如，公司向员工提供两种类型的人寿保险福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="8139c-133">行政职员有资格享有一项人寿保险计划，而所有其他的全职员工则有资格享有另一项人寿保险计划。</span><span class="sxs-lookup"><span data-stu-id="8139c-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="8139c-134">在 Human Resources 中，您可以创建一种福利资格规则以找到所有行政职员和另一种规则以找到所有其他全职员工，然后将这些规则应用于相应的福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="8139c-135">登记</span><span class="sxs-lookup"><span data-stu-id="8139c-135">Enrollment</span></span>
<span data-ttu-id="8139c-136">在创建了组织提供的福利并确定了资格后，您可以在福利中登记您的工作人员。</span><span class="sxs-lookup"><span data-stu-id="8139c-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="8139c-137">在一个流程中，您可以在福利中登记一个工作人员，也可以在一项或多项福利中登记多个工作人员。</span><span class="sxs-lookup"><span data-stu-id="8139c-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="8139c-138">有时，组织会停止提供某些福利。</span><span class="sxs-lookup"><span data-stu-id="8139c-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="8139c-139">在这种情况下，您必须更新福利和已登记的工作人员。</span><span class="sxs-lookup"><span data-stu-id="8139c-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="8139c-140">大批福利到期让您可以同时更改福利或已登记该福利的工作人员的到期日期。</span><span class="sxs-lookup"><span data-stu-id="8139c-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="8139c-141">您还可以选择在某项福利中登记的多个工作人员，并更改该其福利覆盖的结束日期。</span><span class="sxs-lookup"><span data-stu-id="8139c-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="8139c-142">同样，如果您决定提供的福利期限比原始计划期限更长，则大批福利到期也让您可以同时扩展福利和已登记该福利的工作人员的到期日期。</span><span class="sxs-lookup"><span data-stu-id="8139c-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>


