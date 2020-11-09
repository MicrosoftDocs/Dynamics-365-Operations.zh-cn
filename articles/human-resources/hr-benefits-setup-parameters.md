---
title: 设置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中配置福利管理的参数。
author: andreabichsel
manager: tfehr
ms.date: 07/16/2020
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
ms.openlocfilehash: cb9dd6eb8ef840dab54eabab8526200a3a8e21f0
ms.sourcegitcommit: e100c1c7c8dcdacf066defc206dd2f44b8ce6100
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4057020"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="13d80-103">设置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="13d80-103">Set Benefits management parameters</span></span>

<span data-ttu-id="13d80-104">您必须先配置福利管理参数，然后才能在 Microsoft Dynamics 365 Human Resources 中设置休假计划。</span><span class="sxs-lookup"><span data-stu-id="13d80-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="13d80-105">这些参数设置默认值、原因代码和其他选项。</span><span class="sxs-lookup"><span data-stu-id="13d80-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="13d80-106">配置常规参数</span><span class="sxs-lookup"><span data-stu-id="13d80-106">Configure general parameters</span></span>

1. <span data-ttu-id="13d80-107">在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源共享参数** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-107">In the **Benefits management** workspace, under **Setup** , select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="13d80-108">在 **常规** 选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="13d80-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="13d80-109">字段</span><span class="sxs-lookup"><span data-stu-id="13d80-109">Field</span></span> | <span data-ttu-id="13d80-110">说明</span><span class="sxs-lookup"><span data-stu-id="13d80-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="13d80-111">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="13d80-111">**Country/region**</span></span> | <span data-ttu-id="13d80-112">**国家/地区** 字段确定邮政编码/省/市/自治区的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="13d80-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="13d80-113">所选国家/地区首先显示在下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="13d80-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="13d80-114">**登记原因代码**</span><span class="sxs-lookup"><span data-stu-id="13d80-114">**Enrollment reason code**</span></span> | <span data-ttu-id="13d80-115">选择在开放登记处理期间创建员工计划时要使用的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="13d80-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="13d80-116">**取消原因代码**</span><span class="sxs-lookup"><span data-stu-id="13d80-116">**Cancellation reason code**</span></span> | <span data-ttu-id="13d80-117">取消员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="13d80-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="13d80-118">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="13d80-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="13d80-119">如有必要，用户可以更改 **取消原因代码** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="13d80-120">**重新打开原因代码**</span><span class="sxs-lookup"><span data-stu-id="13d80-120">**Reopen reason code**</span></span> | <span data-ttu-id="13d80-121">重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="13d80-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="13d80-122">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="13d80-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="13d80-123">如有必要，用户可以更改 **重新打开原因代码** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="13d80-124">**生命事件原因代码**</span><span class="sxs-lookup"><span data-stu-id="13d80-124">**Life event reason code**</span></span> | <span data-ttu-id="13d80-125">生命事件发生时要使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="13d80-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="13d80-126">**比率更改原因代码**</span><span class="sxs-lookup"><span data-stu-id="13d80-126">**Rate change reason code**</span></span> | <span data-ttu-id="13d80-127">在比率更改更新流程中取消和重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="13d80-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="13d80-128">指示比率更改更新流程更改了哪些记录。</span><span class="sxs-lookup"><span data-stu-id="13d80-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="13d80-129">**年度福利薪金**</span><span class="sxs-lookup"><span data-stu-id="13d80-129">**Benefits annual salary**</span></span> | <span data-ttu-id="13d80-130">使您可以为员工设置 **福利年薪** 金额。</span><span class="sxs-lookup"><span data-stu-id="13d80-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="13d80-131">人力资源部门在确定覆盖范围金额时将使用 **福利年薪** 金额，而不是固定薪酬年度金额。</span><span class="sxs-lookup"><span data-stu-id="13d80-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="13d80-132">**新雇员符合资格**</span><span class="sxs-lookup"><span data-stu-id="13d80-132">**New hire eligible**</span></span> | <span data-ttu-id="13d80-133">指定新雇员是否符合资格。</span><span class="sxs-lookup"><span data-stu-id="13d80-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="13d80-134">**新雇用登记期间**</span><span class="sxs-lookup"><span data-stu-id="13d80-134">**New hire enrollment period**</span></span> | <span data-ttu-id="13d80-135">允许新雇用登记的时间段。</span><span class="sxs-lookup"><span data-stu-id="13d80-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="13d80-136">**注意** ：此设置将覆盖您在计划资格规则中设置的所有新雇用登记期间。</span><span class="sxs-lookup"><span data-stu-id="13d80-136">**Note** : This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="13d80-137">**默认付薪频率**</span><span class="sxs-lookup"><span data-stu-id="13d80-137">**Default pay frequency**</span></span> | <span data-ttu-id="13d80-138">添加新工作人员时使用的默认付薪频率。</span><span class="sxs-lookup"><span data-stu-id="13d80-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="13d80-139">**生命事件已启用**</span><span class="sxs-lookup"><span data-stu-id="13d80-139">**Life events enabled**</span></span> | <span data-ttu-id="13d80-140">启用生命事件。</span><span class="sxs-lookup"><span data-stu-id="13d80-140">Enables life events.</span></span> |
   | <span data-ttu-id="13d80-141">**隐藏旧版福利窗体**</span><span class="sxs-lookup"><span data-stu-id="13d80-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="13d80-142">允许您隐藏旧版福利窗体。</span><span class="sxs-lookup"><span data-stu-id="13d80-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="13d80-143">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="13d80-144">配置员工自助服务参数</span><span class="sxs-lookup"><span data-stu-id="13d80-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="13d80-145">在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源参数** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-145">In the **Benefits management** workspace, under **Setup** , select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="13d80-146">在 **福利管理** 选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="13d80-146">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="13d80-147">字段</span><span class="sxs-lookup"><span data-stu-id="13d80-147">Field</span></span> | <span data-ttu-id="13d80-148">说明</span><span class="sxs-lookup"><span data-stu-id="13d80-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="13d80-149">**福利验证**</span><span class="sxs-lookup"><span data-stu-id="13d80-149">**Benefit verification**</span></span> | <span data-ttu-id="13d80-150">自助服务福利结账期间时要使用的验证文本。</span><span class="sxs-lookup"><span data-stu-id="13d80-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="13d80-151">**自动选择指定人员**</span><span class="sxs-lookup"><span data-stu-id="13d80-151">**Auto select designees**</span></span> | <span data-ttu-id="13d80-152">指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="13d80-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="13d80-153">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="13d80-153">Select **Save**.</span></span>
