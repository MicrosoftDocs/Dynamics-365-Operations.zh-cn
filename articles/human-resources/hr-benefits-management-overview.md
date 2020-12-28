---
title: 福利管理概览
description: Dynamics 365 Human Resources 中的福利管理功能概述。 通过易于使用的在线体验，为您的员工提供更多的福利选项。
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417422"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="c07f5-104">福利管理概述</span><span class="sxs-lookup"><span data-stu-id="c07f5-104">Benefits management overview</span></span>

<span data-ttu-id="c07f5-105">为了保持竞争力，您必须提供丰富的福利，以吸引和留住最好的员工。</span><span class="sxs-lookup"><span data-stu-id="c07f5-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="c07f5-106">除了医疗和牙科保险等标准福利外，您可能还希望提供更多服务，例如收养帮助、娱乐计划和服装津贴。</span><span class="sxs-lookup"><span data-stu-id="c07f5-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="c07f5-107">Microsoft Dynamics 365 Human Resources 中的福利管理为您提供了一个灵活的解决方案，它支持多种福利选项。</span><span class="sxs-lookup"><span data-stu-id="c07f5-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="c07f5-108">Human Resources 还提供易于使用的员工体验，以展示您的服务。</span><span class="sxs-lookup"><span data-stu-id="c07f5-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="c07f5-109">增强的福利计划使您可以创建和管理独特的福利计划，并支持复杂的福利比率表和嵌套层。</span><span class="sxs-lookup"><span data-stu-id="c07f5-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="c07f5-110">您可以轻松创建福利计划、捆绑和自动登记规则，以提供更轻松的员工体验。</span><span class="sxs-lookup"><span data-stu-id="c07f5-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="c07f5-111">弹性信贷项目可让您按比例来支持退休和其他生命事件。</span><span class="sxs-lookup"><span data-stu-id="c07f5-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="c07f5-112">广泛的资格规则可确保您为合适的员工提供合适的福利。</span><span class="sxs-lookup"><span data-stu-id="c07f5-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="c07f5-113">在线福利登记为您的员工提供轻松的体验。</span><span class="sxs-lookup"><span data-stu-id="c07f5-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="c07f5-114">合格的生命事件处理支持未来的生命事件。</span><span class="sxs-lookup"><span data-stu-id="c07f5-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="c07f5-115">如果您想访问演示数据，您需要重新部署沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="c07f5-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="c07f5-116">雇用福利管理</span><span class="sxs-lookup"><span data-stu-id="c07f5-116">Enable Benefits management</span></span>

<span data-ttu-id="c07f5-117">本主题介绍如何在 Human Resources 中开启功能。</span><span class="sxs-lookup"><span data-stu-id="c07f5-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="c07f5-118">还介绍在打开“福利管理”后，“福利管理”将替换或禁用 Human Resources 中的哪些现有功能。</span><span class="sxs-lookup"><span data-stu-id="c07f5-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c07f5-119">不能在 **生产** 环境中禁用已启用的福利管理。</span><span class="sxs-lookup"><span data-stu-id="c07f5-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="c07f5-120">建议在 **生产** 环境中启用福利管理之前，在 **沙盒** 环境中启用和测试。</span><span class="sxs-lookup"><span data-stu-id="c07f5-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="c07f5-121">旧福利功能和新福利管理功能之间差别很大，需要在投入生产之前进行更多设置和应该进行测试。</span><span class="sxs-lookup"><span data-stu-id="c07f5-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="c07f5-122">管理功能</span><span class="sxs-lookup"><span data-stu-id="c07f5-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="c07f5-123">配置员工信息</span><span class="sxs-lookup"><span data-stu-id="c07f5-123">Configure employee information</span></span>

<span data-ttu-id="c07f5-124">必须先提供必需信息，才能为员工登记福利。</span><span class="sxs-lookup"><span data-stu-id="c07f5-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="c07f5-125">您必须在员工的开始日期在 **固定薪酬计划** 中登记员工，并且必须在 **工作人员** 窗体的 **雇用详细信息** 中选择 **福利支付频率**。</span><span class="sxs-lookup"><span data-stu-id="c07f5-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="c07f5-126">如果您有一名员工将收到诸如佣金之类的附加报酬，您可以从员工记录添加 **福利年薪** 金额。</span><span class="sxs-lookup"><span data-stu-id="c07f5-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="c07f5-127">人力资源部门在确定覆盖范围金额时将使用 **福利年薪** 金额，而不是固定薪酬年度金额。</span><span class="sxs-lookup"><span data-stu-id="c07f5-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="c07f5-128">**福利年薪** 必须自员工的开始日期或福利期开始之日（以较早者为准）起生效。</span><span class="sxs-lookup"><span data-stu-id="c07f5-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="c07f5-129">如果同时记录了员工的固定薪酬和福利年薪金额，福利年薪将用于确定覆盖范围金额。</span><span class="sxs-lookup"><span data-stu-id="c07f5-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="c07f5-130">创建用户基于性别或年龄评定的福利计划时，必须输入员工的生日和性别以计算福利成本。</span><span class="sxs-lookup"><span data-stu-id="c07f5-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="c07f5-131">配置福利管理</span><span class="sxs-lookup"><span data-stu-id="c07f5-131">Configure Benefits management</span></span>

<span data-ttu-id="c07f5-132">在为员工创建福利计划之前，需要配置计划的选项。</span><span class="sxs-lookup"><span data-stu-id="c07f5-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="c07f5-133">设置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="c07f5-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="c07f5-134">配置资格规则和选项</span><span class="sxs-lookup"><span data-stu-id="c07f5-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="c07f5-135">配置个人联系人资格选项</span><span class="sxs-lookup"><span data-stu-id="c07f5-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="c07f5-136">创建覆盖范围选项</span><span class="sxs-lookup"><span data-stu-id="c07f5-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="c07f5-137">设置付款频率</span><span class="sxs-lookup"><span data-stu-id="c07f5-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="c07f5-138">配置生活事件类型</span><span class="sxs-lookup"><span data-stu-id="c07f5-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="c07f5-139">创建计划类型</span><span class="sxs-lookup"><span data-stu-id="c07f5-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="c07f5-140">设置原因代码</span><span class="sxs-lookup"><span data-stu-id="c07f5-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="c07f5-141">设置层代码</span><span class="sxs-lookup"><span data-stu-id="c07f5-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="c07f5-142">配置费率</span><span class="sxs-lookup"><span data-stu-id="c07f5-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="c07f5-143">配置扣缴</span><span class="sxs-lookup"><span data-stu-id="c07f5-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="c07f5-144">配置等待天数</span><span class="sxs-lookup"><span data-stu-id="c07f5-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="c07f5-145">配置等待时段</span><span class="sxs-lookup"><span data-stu-id="c07f5-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="c07f5-146">设置舍入规则</span><span class="sxs-lookup"><span data-stu-id="c07f5-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="c07f5-147">创建雇用类别</span><span class="sxs-lookup"><span data-stu-id="c07f5-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="c07f5-148">设置雇用类型</span><span class="sxs-lookup"><span data-stu-id="c07f5-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="c07f5-149">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="c07f5-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="c07f5-150">创建福利计划</span><span class="sxs-lookup"><span data-stu-id="c07f5-150">Create benefit plans</span></span>

<span data-ttu-id="c07f5-151">这些文章说明如何创建福利计划，包括捆绑和弹性信贷项目。</span><span class="sxs-lookup"><span data-stu-id="c07f5-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="c07f5-152">设置福利计划</span><span class="sxs-lookup"><span data-stu-id="c07f5-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="c07f5-153">设置弹性信贷计划</span><span class="sxs-lookup"><span data-stu-id="c07f5-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="c07f5-154">处理福利计划</span><span class="sxs-lookup"><span data-stu-id="c07f5-154">Process benefit plans</span></span>

<span data-ttu-id="c07f5-155">您需要处理一些更改以使它们生效。</span><span class="sxs-lookup"><span data-stu-id="c07f5-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="c07f5-156">处理登记资格</span><span class="sxs-lookup"><span data-stu-id="c07f5-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="c07f5-157">处理生命事件</span><span class="sxs-lookup"><span data-stu-id="c07f5-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="c07f5-158">处理生命事件更改</span><span class="sxs-lookup"><span data-stu-id="c07f5-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="c07f5-159">处理生命事件资格</span><span class="sxs-lookup"><span data-stu-id="c07f5-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="c07f5-160">处理比率更改</span><span class="sxs-lookup"><span data-stu-id="c07f5-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

