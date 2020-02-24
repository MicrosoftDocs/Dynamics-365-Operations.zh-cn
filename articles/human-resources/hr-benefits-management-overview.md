---
title: 福利管理概述
description: Dynamics 365 Human Resources 中的福利管理预览功能概述。 通过易于使用的在线体验，为您的员工提供更多的福利选项。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029455"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="86905-104">福利管理概述</span><span class="sxs-lookup"><span data-stu-id="86905-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="86905-105">为了保持竞争力，您必须提供丰富的福利，以吸引和留住最好的员工。</span><span class="sxs-lookup"><span data-stu-id="86905-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="86905-106">除了医疗和牙科保险等标准福利外，您可能还希望提供更多服务，例如收养帮助、娱乐计划和服装津贴。</span><span class="sxs-lookup"><span data-stu-id="86905-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="86905-107">Microsoft Dynamics 365 Human Resources 中的福利管理预览功能为您提供了一个灵活的解决方案，它支持多种福利选项。</span><span class="sxs-lookup"><span data-stu-id="86905-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="86905-108">Human Resources 还提供易于使用的员工体验，以展示您的服务。</span><span class="sxs-lookup"><span data-stu-id="86905-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="86905-109">增强的福利计划使您可以创建和管理独特的福利计划，并支持复杂的福利比率表和嵌套层。</span><span class="sxs-lookup"><span data-stu-id="86905-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="86905-110">您可以轻松创建福利计划、捆绑和自动登记规则，以提供更轻松的员工体验。</span><span class="sxs-lookup"><span data-stu-id="86905-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="86905-111">弹性信贷项目可让您按比例来支持退休和其他生命事件。</span><span class="sxs-lookup"><span data-stu-id="86905-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="86905-112">广泛的资格规则可确保您为合适的员工提供合适的福利。</span><span class="sxs-lookup"><span data-stu-id="86905-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="86905-113">在线福利登记为您的员工提供轻松的体验。</span><span class="sxs-lookup"><span data-stu-id="86905-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="86905-114">合格的生命事件处理与员工自助服务集成在一起，同时还支持未来的生命事件。</span><span class="sxs-lookup"><span data-stu-id="86905-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="86905-115">如果您想访问演示数据，您需要重新部署沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="86905-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="86905-116">您可以提供直接反馈或将问题报告给：D365BenefitsPreview@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="86905-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="86905-117">福利管理已知问题</span><span class="sxs-lookup"><span data-stu-id="86905-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="86905-118">资格处理</span><span class="sxs-lookup"><span data-stu-id="86905-118">Eligibility processing</span></span>

<span data-ttu-id="86905-119">当运行使用 1-5X 薪金、薪金百分比和固定金额覆盖范围金额的福利的资格时，必须将**福利详细信息**日期设置为**工作经历**中的**员工开始日期**。</span><span class="sxs-lookup"><span data-stu-id="86905-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="86905-120">您还必须包括**工时数**、**付款频率**和**年度福利薪水金额**。</span><span class="sxs-lookup"><span data-stu-id="86905-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="86905-121">如果工作人员有固定薪酬，则输入**工时数**和**付款频率**。</span><span class="sxs-lookup"><span data-stu-id="86905-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="86905-122">将计算年度薪水金额。</span><span class="sxs-lookup"><span data-stu-id="86905-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="86905-123">如果员工是雇员，则不需要输入**工时数**。</span><span class="sxs-lookup"><span data-stu-id="86905-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="86905-124">我们建议在创建新工作人员时，首先输入固定薪酬。</span><span class="sxs-lookup"><span data-stu-id="86905-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="86905-125">要更新福利详细信息记录，导航到**工作人员 > 工作人员历史记录 > 雇用详细信息**。</span><span class="sxs-lookup"><span data-stu-id="86905-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="86905-126">将日期调整为工作人员开始日期。</span><span class="sxs-lookup"><span data-stu-id="86905-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="86905-127">员工自助服务</span><span class="sxs-lookup"><span data-stu-id="86905-127">Employee self-service</span></span>

<span data-ttu-id="86905-128">更新人寿保险的覆盖范围金额时，不会计算员工金额。</span><span class="sxs-lookup"><span data-stu-id="86905-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="86905-129">例如，向员工提供人寿保险计划时，他们最多可以选择 50,000 美元的保额，每 1,000 美元保额费用为 0.36 美元。</span><span class="sxs-lookup"><span data-stu-id="86905-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="86905-130">当员工更新覆盖范围金额时，员工的关联成本保持为零。</span><span class="sxs-lookup"><span data-stu-id="86905-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="86905-131">对于仅允许单一选择该计划类型的福利计划，如果用户在选择计划后尝试放弃计划，将会收到错误。</span><span class="sxs-lookup"><span data-stu-id="86905-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="86905-132">例如，用户选择医疗计划并将其放在他们的购物车中。</span><span class="sxs-lookup"><span data-stu-id="86905-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="86905-133">然后，用户选择**放弃**另一个医疗计划。</span><span class="sxs-lookup"><span data-stu-id="86905-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="86905-134">用户将收到错误。</span><span class="sxs-lookup"><span data-stu-id="86905-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="86905-135">雇用福利管理</span><span class="sxs-lookup"><span data-stu-id="86905-135">Enable Benefits management</span></span>

<span data-ttu-id="86905-136">福利管理是一项预览功能，仅在**沙盒**中可用。</span><span class="sxs-lookup"><span data-stu-id="86905-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="86905-137">这些文章介绍如何在 Human Resources 中打开预览功能。</span><span class="sxs-lookup"><span data-stu-id="86905-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="86905-138">另外还介绍在打开“福利管理”后，“福利管理”将替换或禁用 Human Resources 中的哪些现有功能。</span><span class="sxs-lookup"><span data-stu-id="86905-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="86905-139">管理功能</span><span class="sxs-lookup"><span data-stu-id="86905-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="86905-140">预览功能：福利管理</span><span class="sxs-lookup"><span data-stu-id="86905-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="86905-141">配置福利管理</span><span class="sxs-lookup"><span data-stu-id="86905-141">Configure Benefits management</span></span>

<span data-ttu-id="86905-142">在为员工创建福利计划之前，需要配置计划的选项。</span><span class="sxs-lookup"><span data-stu-id="86905-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="86905-143">设置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="86905-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="86905-144">配置资格规则和选项</span><span class="sxs-lookup"><span data-stu-id="86905-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="86905-145">配置个人联系人资格选项</span><span class="sxs-lookup"><span data-stu-id="86905-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="86905-146">创建覆盖范围选项</span><span class="sxs-lookup"><span data-stu-id="86905-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="86905-147">设置付款频率</span><span class="sxs-lookup"><span data-stu-id="86905-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="86905-148">配置生命事件类型</span><span class="sxs-lookup"><span data-stu-id="86905-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="86905-149">创建计划类型</span><span class="sxs-lookup"><span data-stu-id="86905-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="86905-150">设置原因代码</span><span class="sxs-lookup"><span data-stu-id="86905-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="86905-151">设置层代码</span><span class="sxs-lookup"><span data-stu-id="86905-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="86905-152">配置比率</span><span class="sxs-lookup"><span data-stu-id="86905-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="86905-153">配置扣缴</span><span class="sxs-lookup"><span data-stu-id="86905-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="86905-154">配置等待天数</span><span class="sxs-lookup"><span data-stu-id="86905-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="86905-155">配置等待期间</span><span class="sxs-lookup"><span data-stu-id="86905-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="86905-156">设置舍入规则</span><span class="sxs-lookup"><span data-stu-id="86905-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="86905-157">创建雇用类别</span><span class="sxs-lookup"><span data-stu-id="86905-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="86905-158">设置雇用类型</span><span class="sxs-lookup"><span data-stu-id="86905-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="86905-159">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="86905-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="86905-160">创建福利计划</span><span class="sxs-lookup"><span data-stu-id="86905-160">Create benefit plans</span></span>

<span data-ttu-id="86905-161">这些文章说明如何创建福利计划，包括捆绑和弹性信贷项目。</span><span class="sxs-lookup"><span data-stu-id="86905-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="86905-162">设置福利计划</span><span class="sxs-lookup"><span data-stu-id="86905-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="86905-163">创建工作人员福利计划</span><span class="sxs-lookup"><span data-stu-id="86905-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="86905-164">设置弹性信贷项目</span><span class="sxs-lookup"><span data-stu-id="86905-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="86905-165">配置未来的生命事件</span><span class="sxs-lookup"><span data-stu-id="86905-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="86905-166">处理福利计划</span><span class="sxs-lookup"><span data-stu-id="86905-166">Process benefit plans</span></span>

<span data-ttu-id="86905-167">您需要处理一些更改以使它们生效。</span><span class="sxs-lookup"><span data-stu-id="86905-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="86905-168">处理登记资格</span><span class="sxs-lookup"><span data-stu-id="86905-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="86905-169">处理生命事件</span><span class="sxs-lookup"><span data-stu-id="86905-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="86905-170">处理生命事件更改</span><span class="sxs-lookup"><span data-stu-id="86905-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="86905-171">处理生命事件资格</span><span class="sxs-lookup"><span data-stu-id="86905-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="86905-172">处理比率更改</span><span class="sxs-lookup"><span data-stu-id="86905-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

