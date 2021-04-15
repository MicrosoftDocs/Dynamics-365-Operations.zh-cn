---
title: 创建计划类型
description: Microsoft Dynamics 365 Human Resources 中的计划类型是特定福利类型的高级分组。 每个计划类型都有一个计划类型代码，用于确定该计划类型的规则。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 70eae24e48a0541c445deead2dba8bc2716b4be5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801063"
---
# <a name="create-plan-types"></a><span data-ttu-id="69385-104">创建计划类型</span><span class="sxs-lookup"><span data-stu-id="69385-104">Create plan types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="69385-105">Microsoft Dynamics 365 Human Resources 中的计划类型是特定福利类型的高级分组。</span><span class="sxs-lookup"><span data-stu-id="69385-105">A plan type in Microsoft Dynamics 365 Human Resources is a high-level grouping of specific types of benefits.</span></span> <span data-ttu-id="69385-106">每个计划类型都有一个计划类型代码，用于确定该计划类型的规则。</span><span class="sxs-lookup"><span data-stu-id="69385-106">Each plan type has a plan type code that determines rules for the plan type.</span></span> <span data-ttu-id="69385-107">例如，计划类型“基本人寿”将具有计划类型代码 Life，因为它是一种人寿保险计划，必须符合为 Life 计划类型代码建立的规则。</span><span class="sxs-lookup"><span data-stu-id="69385-107">For example, the plan type Basic life would have the plan type code Life because it’s a kind of life insurance plan and must conform to rules established for the Life plan type code.</span></span> <span data-ttu-id="69385-108">另一种计划类型可能是“补充人寿”，也具有计划类型代码 Life。</span><span class="sxs-lookup"><span data-stu-id="69385-108">Another plan type might be Supplemental life, also with plan type code Life.</span></span>

<span data-ttu-id="69385-109">各个计划类型指示员工是否可以登记加入一个或多个该类型的计划。</span><span class="sxs-lookup"><span data-stu-id="69385-109">Each plan type indicates whether an employee can enroll in one plan of its type or multiple.</span></span> <span data-ttu-id="69385-110">例如，员工可能能够同时加入计划类型 Life 的“基本人寿”和“补充人寿”政策。</span><span class="sxs-lookup"><span data-stu-id="69385-110">For example, an employee would likely be able to enroll in both the Basic life and the Supplemental life policies of plan type Life.</span></span> <span data-ttu-id="69385-111">有可能只允许员工加入一个 Medical 类型的政策。</span><span class="sxs-lookup"><span data-stu-id="69385-111">An employee would likely be allowed to enroll in only one policy of type Medical.</span></span>

<span data-ttu-id="69385-112">如果计划类型涉及联系人，该计划类型将指示联系人是受益人还是依赖方。</span><span class="sxs-lookup"><span data-stu-id="69385-112">If a plan type involves contacts, the plan type indicates whether contacts are beneficiaries or dependents.</span></span> <span data-ttu-id="69385-113">例如，“基本人寿”计划类型将有受益人，而“基本医疗”计划类型将有依赖方。</span><span class="sxs-lookup"><span data-stu-id="69385-113">For example, a Basic life plan type would have beneficiaries, while a Basic medical plan type would have dependents.</span></span> <span data-ttu-id="69385-114">在某些情况下，计划可能没有任何个人联系人。</span><span class="sxs-lookup"><span data-stu-id="69385-114">In some cases, a plan may not have any personal contacts.</span></span> <span data-ttu-id="69385-115">例如，“弹性支出帐户”或“停车津贴”。</span><span class="sxs-lookup"><span data-stu-id="69385-115">For example, a Flexible Spending Account or Parking allowance.</span></span>

<span data-ttu-id="69385-116">计划类型可以定义覆盖范围选项。</span><span class="sxs-lookup"><span data-stu-id="69385-116">A plan type may define coverage options.</span></span> <span data-ttu-id="69385-117">覆盖范围选项在覆盖范围选项窗体中定义。</span><span class="sxs-lookup"><span data-stu-id="69385-117">The coverage options are defined in the Coverage option form.</span></span> <span data-ttu-id="69385-118">覆盖范围选项可以指定福利的金额或符合计划类型条件的联系人。</span><span class="sxs-lookup"><span data-stu-id="69385-118">A coverage option can specify the amount of the benefit or the contacts who are eligible for the plan type.</span></span> <span data-ttu-id="69385-119">例如，如果联系人类型为“受益人”，覆盖范围选项应定义受益人在使用福利时有资格享受哪些项目的条款。</span><span class="sxs-lookup"><span data-stu-id="69385-119">For example, if the contact type is Beneficiary, the coverage option should define the terms of what the beneficiary is eligible to receive when the benefit is utilized.</span></span> <span data-ttu-id="69385-120">如果联系人类型为“依赖方”，覆盖范围选项应定义依赖方与员工之间的关系。</span><span class="sxs-lookup"><span data-stu-id="69385-120">If the contact type is Dependent, the coverage option should define the relationship between the dependent and employee.</span></span> 

1. <span data-ttu-id="69385-121">在 **福利管理** 工作区中，在 **设置** 下，选择 **计划类型**。</span><span class="sxs-lookup"><span data-stu-id="69385-121">In the **Benefits management** workspace, under **Setup**, select **Plan types**.</span></span>

2. <span data-ttu-id="69385-122">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="69385-122">Select **New**.</span></span>

3. <span data-ttu-id="69385-123">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="69385-123">Specify values for the following fields:</span></span>

   | <span data-ttu-id="69385-124">字段</span><span class="sxs-lookup"><span data-stu-id="69385-124">Field</span></span> | <span data-ttu-id="69385-125">说明</span><span class="sxs-lookup"><span data-stu-id="69385-125">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="69385-126">**计划类型**</span><span class="sxs-lookup"><span data-stu-id="69385-126">**Plan type**</span></span> | <span data-ttu-id="69385-127">标识计划类型的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="69385-127">A unique name that identifies the plan type.</span></span> |
   | <span data-ttu-id="69385-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="69385-128">**Description**</span></span> | <span data-ttu-id="69385-129">计划类型的描述。</span><span class="sxs-lookup"><span data-stu-id="69385-129">A description of the plan type.</span></span> |
   | <span data-ttu-id="69385-130">**计划类型代码**</span><span class="sxs-lookup"><span data-stu-id="69385-130">**Plan type code**</span></span> | <span data-ttu-id="69385-131">从值的下拉列表中选择计划类型代码。</span><span class="sxs-lookup"><span data-stu-id="69385-131">Select a plan type code from the drop-down list of values.</span></span> <span data-ttu-id="69385-132">计划类型代码列表显示当前版本支持的所有计划类型。</span><span class="sxs-lookup"><span data-stu-id="69385-132">The plan type code list displays all the plan types that are supported in the current version.</span></span> |
   | <span data-ttu-id="69385-133">**并发登记**</span><span class="sxs-lookup"><span data-stu-id="69385-133">**Concurrent enrollment**</span></span> | <span data-ttu-id="69385-134">指定员工是否可以登记加入相同计划类型的多个福利计划，还是每个计划类型仅可登记加入一个福利计划。</span><span class="sxs-lookup"><span data-stu-id="69385-134">Specifies whether an employee can enroll in multiple benefit plans of the same plan type or only one benefit plan per plan type.</span></span> |
   | <span data-ttu-id="69385-135">**联系人类型**</span><span class="sxs-lookup"><span data-stu-id="69385-135">**Contact type**</span></span> | <span data-ttu-id="69385-136">指定个人联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="69385-136">Specifies the role of the personal contact.</span></span> <span data-ttu-id="69385-137">值有空白、依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="69385-137">The values are blank, Dependent, and Beneficiary.</span></span> <span data-ttu-id="69385-138">如果联系人的计划类型根据覆盖范围选项不需要是依赖方或受益人，可以将 **联系类型** 留空。</span><span class="sxs-lookup"><span data-stu-id="69385-138">You can leave **Contact type** blank if their plan type does not require a dependent or beneficiary based on the coverage option.</span></span> |

4. <span data-ttu-id="69385-139">要配置生命事件选项，选择 **操作**，然后选择 **生命事件选项**。</span><span class="sxs-lookup"><span data-stu-id="69385-139">To configure life event options, select **Actions**, and then select **Life event options**.</span></span> <span data-ttu-id="69385-140">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="69385-140">Specify values for the following fields:</span></span>

   | <span data-ttu-id="69385-141">字段</span><span class="sxs-lookup"><span data-stu-id="69385-141">Field</span></span> | <span data-ttu-id="69385-142">说明</span><span class="sxs-lookup"><span data-stu-id="69385-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="69385-143">**计划类型**</span><span class="sxs-lookup"><span data-stu-id="69385-143">**Plan type**</span></span> | <span data-ttu-id="69385-144">要为其配置生命事件选项的计划类型。</span><span class="sxs-lookup"><span data-stu-id="69385-144">The plan type to configure life event options for.</span></span> |
   | <span data-ttu-id="69385-145">**生命事件类型 ID**</span><span class="sxs-lookup"><span data-stu-id="69385-145">**Life event type ID**</span></span> | <span data-ttu-id="69385-146">生命事件类型的 ID。</span><span class="sxs-lookup"><span data-stu-id="69385-146">The ID of the life event type.</span></span> |
   | <span data-ttu-id="69385-147">**允许取消**</span><span class="sxs-lookup"><span data-stu-id="69385-147">**Allow cancellation**</span></span> | <span data-ttu-id="69385-148">指定员工在生命事件期间是否可取消福利计划。</span><span class="sxs-lookup"><span data-stu-id="69385-148">Specifies whether an employee can cancel a benefits plan during the life event.</span></span> |
   | <span data-ttu-id="69385-149">**更改覆盖范围选项**</span><span class="sxs-lookup"><span data-stu-id="69385-149">**Change coverage option**</span></span> | <span data-ttu-id="69385-150">指定员工在生命事件期间是否可更改覆盖范围选项。</span><span class="sxs-lookup"><span data-stu-id="69385-150">Specifies whether an employee can change coverage options during the life event.</span></span> |
   | <span data-ttu-id="69385-151">**更改为新计划**</span><span class="sxs-lookup"><span data-stu-id="69385-151">**Change to a new plan**</span></span> | <span data-ttu-id="69385-152">指定员工在生命事件期间是否可更改计划。</span><span class="sxs-lookup"><span data-stu-id="69385-152">Specifies whether an employee can change plans during the life event.</span></span> |
   | <span data-ttu-id="69385-153">**自动取消计划**</span><span class="sxs-lookup"><span data-stu-id="69385-153">**Auto cancel plan**</span></span> | <span data-ttu-id="69385-154">指定是否在生命事件期间自动取消计划。</span><span class="sxs-lookup"><span data-stu-id="69385-154">Specifies whether to automatically cancel the plan during the life event.</span></span> |
   | <span data-ttu-id="69385-155">**自动重新打开资格检查**</span><span class="sxs-lookup"><span data-stu-id="69385-155">**Auto reopen eligibility check**</span></span> | <span data-ttu-id="69385-156">指定是否在生命事件期间自动重新开放福利登记资格检查。</span><span class="sxs-lookup"><span data-stu-id="69385-156">Specifies whether to automatically reopen the benefits enrollment eligibility check during the life event.</span></span> |
   | <span data-ttu-id="69385-157">**报告时间范围**</span><span class="sxs-lookup"><span data-stu-id="69385-157">**Reporting window**</span></span> | <span data-ttu-id="69385-158">指定生命事件的报告时间范围(以天为单位)。</span><span class="sxs-lookup"><span data-stu-id="69385-158">Specifies the reporting window, in days, of the life event.</span></span> <span data-ttu-id="69385-159">**注意**：如果您不输入金额，系统将假定报告时间范围为零，不会处理生命事件。</span><span class="sxs-lookup"><span data-stu-id="69385-159">**Note**: If you don't enter an amount, the system assumes the reporting window to be zero and won't process the life event.</span></span> |

5. <span data-ttu-id="69385-160">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="69385-160">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]