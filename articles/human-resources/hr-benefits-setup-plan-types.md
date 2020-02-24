---
title: 创建计划类型
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c12eecb38bd943a9c604f878644da289783d3f74
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008230"
---
# <a name="create-plan-types"></a><span data-ttu-id="31a6e-102">创建计划类型</span><span class="sxs-lookup"><span data-stu-id="31a6e-102">Create plan types</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="31a6e-103">Microsoft Dynamics 365 Human Resources 中的计划类型是特定福利类型的高级分组。</span><span class="sxs-lookup"><span data-stu-id="31a6e-103">A plan type in Microsoft Dynamics 365 Human Resources is a high-level grouping of specific types of benefits.</span></span> <span data-ttu-id="31a6e-104">每个计划类型都有一个计划类型代码，用于确定该计划类型的规则。</span><span class="sxs-lookup"><span data-stu-id="31a6e-104">Each plan type has a plan type code that determines rules for the plan type.</span></span> <span data-ttu-id="31a6e-105">例如，计划类型“基本人寿”将具有计划类型代码 Life，因为它是一种人寿保险计划，必须符合为 Life 计划类型代码建立的规则。</span><span class="sxs-lookup"><span data-stu-id="31a6e-105">For example, the plan type Basic life would have the plan type code Life because it’s a kind of life insurance plan and must conform to rules established for the Life plan type code.</span></span> <span data-ttu-id="31a6e-106">另一种计划类型可能是“补充人寿”，也具有计划类型代码 Life。</span><span class="sxs-lookup"><span data-stu-id="31a6e-106">Another plan type might be Supplemental life, also with plan type code Life.</span></span>

<span data-ttu-id="31a6e-107">各个计划类型指示员工是否可以登记加入一个或多个该类型的计划。</span><span class="sxs-lookup"><span data-stu-id="31a6e-107">Each plan type indicates whether an employee can enroll in one plan of its type or multiple.</span></span> <span data-ttu-id="31a6e-108">例如，员工可能能够同时加入计划类型 Life 的“基本人寿”和“补充人寿”政策。</span><span class="sxs-lookup"><span data-stu-id="31a6e-108">For example, an employee would likely be able to enroll in both the Basic life and the Supplemental life policies of plan type Life.</span></span> <span data-ttu-id="31a6e-109">有可能只允许员工加入一个 Medical 类型的政策。</span><span class="sxs-lookup"><span data-stu-id="31a6e-109">An employee would likely be allowed to enroll in only one policy of type Medical.</span></span>

<span data-ttu-id="31a6e-110">如果计划类型涉及联系人，该计划类型将指示联系人是受益人还是依赖方。</span><span class="sxs-lookup"><span data-stu-id="31a6e-110">If a plan type involves contacts, the plan type indicates whether contacts are beneficiaries or dependents.</span></span> <span data-ttu-id="31a6e-111">例如，“基本人寿”计划类型将有受益人，而“基本医疗”计划类型将有依赖方。</span><span class="sxs-lookup"><span data-stu-id="31a6e-111">For example, a Basic life plan type would have beneficiaries, while a Basic medical plan type would have dependents.</span></span> <span data-ttu-id="31a6e-112">在某些情况下，计划可能没有任何个人联系人。</span><span class="sxs-lookup"><span data-stu-id="31a6e-112">In some cases, a plan may not have any personal contacts.</span></span> <span data-ttu-id="31a6e-113">例如，“弹性支出帐户”或“停车津贴”。</span><span class="sxs-lookup"><span data-stu-id="31a6e-113">For example, a Flexible Spending Account or Parking allowance.</span></span>

<span data-ttu-id="31a6e-114">计划类型可以定义覆盖范围选项。</span><span class="sxs-lookup"><span data-stu-id="31a6e-114">A plan type may define coverage options.</span></span> <span data-ttu-id="31a6e-115">覆盖范围选项在覆盖范围选项窗体中定义。</span><span class="sxs-lookup"><span data-stu-id="31a6e-115">The coverage options are defined in the Coverage option form.</span></span> <span data-ttu-id="31a6e-116">覆盖范围选项可以指定福利的金额或符合计划类型条件的联系人。</span><span class="sxs-lookup"><span data-stu-id="31a6e-116">A coverage option can specify the amount of the benefit or the contacts who are eligible for the plan type.</span></span> <span data-ttu-id="31a6e-117">例如，如果联系人类型为“受益人”，覆盖范围选项应定义受益人在使用福利时有资格享受哪些项目的条款。</span><span class="sxs-lookup"><span data-stu-id="31a6e-117">For example, if the contact type is Beneficiary, the coverage option should define the terms of what the beneficiary is eligible to receive when the benefit is utilized.</span></span> <span data-ttu-id="31a6e-118">如果联系人类型为“依赖方”，覆盖范围选项应定义依赖方与员工之间的关系。</span><span class="sxs-lookup"><span data-stu-id="31a6e-118">If the contact type is Dependent, the coverage option should define the relationship between the dependent and employee.</span></span> 

1. <span data-ttu-id="31a6e-119">在**福利管理**工作区中，在**设置**下，选择**计划类型**。</span><span class="sxs-lookup"><span data-stu-id="31a6e-119">In the **Benefits management** workspace, under **Setup**, select **Plan types**.</span></span>

2. <span data-ttu-id="31a6e-120">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="31a6e-120">Select **New**.</span></span>

3. <span data-ttu-id="31a6e-121">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="31a6e-121">Specify values for the following fields:</span></span>

   | <span data-ttu-id="31a6e-122">字段</span><span class="sxs-lookup"><span data-stu-id="31a6e-122">Field</span></span> | <span data-ttu-id="31a6e-123">说明</span><span class="sxs-lookup"><span data-stu-id="31a6e-123">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="31a6e-124">计划类型</span><span class="sxs-lookup"><span data-stu-id="31a6e-124">Plan type</span></span> | <span data-ttu-id="31a6e-125">标识计划类型的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="31a6e-125">A unique name that identifies the plan type.</span></span> |
   | <span data-ttu-id="31a6e-126">说明</span><span class="sxs-lookup"><span data-stu-id="31a6e-126">Description</span></span> | <span data-ttu-id="31a6e-127">计划类型的描述。</span><span class="sxs-lookup"><span data-stu-id="31a6e-127">A description of the plan type.</span></span> |
   | <span data-ttu-id="31a6e-128">计划类型代码</span><span class="sxs-lookup"><span data-stu-id="31a6e-128">Plant type code</span></span> | <span data-ttu-id="31a6e-129">从值的下拉列表中选择计划类型代码。</span><span class="sxs-lookup"><span data-stu-id="31a6e-129">Select a plan type code from the drop down list of values.</span></span> <span data-ttu-id="31a6e-130">计划类型代码列表显示当前版本支持的所有计划类型。</span><span class="sxs-lookup"><span data-stu-id="31a6e-130">The plan type code list displays all the plan types that are supported in the current version.</span></span> |
   | <span data-ttu-id="31a6e-131">并发登记</span><span class="sxs-lookup"><span data-stu-id="31a6e-131">Concurrent enrollment</span></span> | <span data-ttu-id="31a6e-132">指定员工是否可以登记加入相同计划类型的多个福利计划，还是每个计划类型仅可登记加入一个福利计划。</span><span class="sxs-lookup"><span data-stu-id="31a6e-132">Specifies whether an employee can enroll in multiple benefit plans of the same plan type or only one benefit plan per plan type.</span></span> |
   | <span data-ttu-id="31a6e-133">联系人类型</span><span class="sxs-lookup"><span data-stu-id="31a6e-133">Contact type</span></span> | <span data-ttu-id="31a6e-134">指定个人联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="31a6e-134">Specifies the role of the personal contact.</span></span> <span data-ttu-id="31a6e-135">值有空白、依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="31a6e-135">The values are blank, Dependent, and Beneficiary.</span></span> <span data-ttu-id="31a6e-136">如果联系人的计划类型根据覆盖范围选项不需要是依赖方或受益人，可以将“联系类型”留空。</span><span class="sxs-lookup"><span data-stu-id="31a6e-136">You can leave Contact type blank if their plan type does not require a dependent or beneficiary based on the coverage option.</span></span> |

4. <span data-ttu-id="31a6e-137">要配置生命事件选项，选择**操作**，然后选择**生命事件选项**。</span><span class="sxs-lookup"><span data-stu-id="31a6e-137">To configure life event options, select **Actions**, and then select **Life event options**.</span></span> <span data-ttu-id="31a6e-138">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="31a6e-138">Specify values for the following fields:</span></span>

   | <span data-ttu-id="31a6e-139">字段</span><span class="sxs-lookup"><span data-stu-id="31a6e-139">Field</span></span> | <span data-ttu-id="31a6e-140">说明</span><span class="sxs-lookup"><span data-stu-id="31a6e-140">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="31a6e-141">计划类型</span><span class="sxs-lookup"><span data-stu-id="31a6e-141">Plan type</span></span> | <span data-ttu-id="31a6e-142">要为其配置生命事件选项的计划类型。</span><span class="sxs-lookup"><span data-stu-id="31a6e-142">The plan type to configure life event options for.</span></span> |
   | <span data-ttu-id="31a6e-143">生命事件类型 ID</span><span class="sxs-lookup"><span data-stu-id="31a6e-143">Life event type id</span></span> | <span data-ttu-id="31a6e-144">生命事件类型的 ID。</span><span class="sxs-lookup"><span data-stu-id="31a6e-144">The ID of the life event type.</span></span> |
   | <span data-ttu-id="31a6e-145">允许取消</span><span class="sxs-lookup"><span data-stu-id="31a6e-145">Allow cancellation</span></span> | <span data-ttu-id="31a6e-146">指定员工在生命事件期间是否可取消福利计划。</span><span class="sxs-lookup"><span data-stu-id="31a6e-146">Specifies whether an employee can cancel a benefits plan during the life event.</span></span> |
   |<span data-ttu-id="31a6e-147">更改覆盖范围选项</span><span class="sxs-lookup"><span data-stu-id="31a6e-147">Change coverage option</span></span> | <span data-ttu-id="31a6e-148">指定员工在生命事件期间是否可更改覆盖范围选项。</span><span class="sxs-lookup"><span data-stu-id="31a6e-148">Specifies whether an employee can change coverage options during the life event.</span></span> |
   | <span data-ttu-id="31a6e-149">更改为新计划</span><span class="sxs-lookup"><span data-stu-id="31a6e-149">Change to a new plan</span></span> | <span data-ttu-id="31a6e-150">指定员工在生命事件期间是否可更改计划。</span><span class="sxs-lookup"><span data-stu-id="31a6e-150">Specifies whether an employee can change plans during the life event.</span></span> |
   | <span data-ttu-id="31a6e-151">自动取消计划</span><span class="sxs-lookup"><span data-stu-id="31a6e-151">Auto cancel plan</span></span> |<span data-ttu-id="31a6e-152">指定是否在生命事件期间自动取消计划。</span><span class="sxs-lookup"><span data-stu-id="31a6e-152">Specifies whether to automatically cancel the plan during the life event.</span></span> |
   | <span data-ttu-id="31a6e-153">自动重新打开资格检查</span><span class="sxs-lookup"><span data-stu-id="31a6e-153">Auto reopen eligibility check</span></span> | <span data-ttu-id="31a6e-154">指定是否在生命事件期间自动重新开放福利登记资格检查。</span><span class="sxs-lookup"><span data-stu-id="31a6e-154">Specifies whether to automatically reopen the benefits enrollment eligibility check during the life event.</span></span> |
   | <span data-ttu-id="31a6e-155">报告时间范围</span><span class="sxs-lookup"><span data-stu-id="31a6e-155">Reporting window</span></span> | <span data-ttu-id="31a6e-156">指定生命事件的报告时间范围(以天为单位)。</span><span class="sxs-lookup"><span data-stu-id="31a6e-156">Specifies the reporting window, in days, of the life event.</span></span> <span data-ttu-id="31a6e-157">**注意**：如果您不输入金额，系统将假定报告时间范围为零，不会处理生命事件。</span><span class="sxs-lookup"><span data-stu-id="31a6e-157">**Note**: If you don't enter an amount, the system assumes the reporting window to be zero and won't process the life event.</span></span> |

5. <span data-ttu-id="31a6e-158">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="31a6e-158">Select **Save**.</span></span> 
