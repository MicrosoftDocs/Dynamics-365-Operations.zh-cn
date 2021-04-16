---
title: 为所有公司设置福利管理和员工自助服务参数
description: 在 Microsoft Dynamics 365 Human Resources 中配置福利管理和员工自助服务的参数。
author: andreabichsel
ms.date: 12/07/2020
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
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791477"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="1164f-103">为所有公司设置福利管理和员工自助服务参数</span><span class="sxs-lookup"><span data-stu-id="1164f-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1164f-104">您必须先配置福利管理参数，然后才能在 Microsoft Dynamics 365 Human Resources 中设置福利计划。</span><span class="sxs-lookup"><span data-stu-id="1164f-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="1164f-105">这些参数设置默认值、原因代码和其他选项。</span><span class="sxs-lookup"><span data-stu-id="1164f-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="1164f-106">配置常规参数</span><span class="sxs-lookup"><span data-stu-id="1164f-106">Configure general parameters</span></span>

1. <span data-ttu-id="1164f-107">在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源共享参数**。</span><span class="sxs-lookup"><span data-stu-id="1164f-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="1164f-108">在 **福利管理** 选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="1164f-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="1164f-109">字段</span><span class="sxs-lookup"><span data-stu-id="1164f-109">Field</span></span> | <span data-ttu-id="1164f-110">说明</span><span class="sxs-lookup"><span data-stu-id="1164f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1164f-111">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="1164f-111">**Country/region**</span></span> | <span data-ttu-id="1164f-112">**国家/地区** 字段确定邮政编码/省/市/自治区的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="1164f-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="1164f-113">所选国家/地区首先显示在下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="1164f-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="1164f-114">**登记原因代码**</span><span class="sxs-lookup"><span data-stu-id="1164f-114">**Enrollment reason code**</span></span> | <span data-ttu-id="1164f-115">选择在开放登记处理期间创建员工计划时要使用的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="1164f-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="1164f-116">**取消原因代码**</span><span class="sxs-lookup"><span data-stu-id="1164f-116">**Cancellation reason code**</span></span> | <span data-ttu-id="1164f-117">取消员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="1164f-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="1164f-118">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="1164f-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="1164f-119">如有必要，用户可以更改 **取消原因代码**。</span><span class="sxs-lookup"><span data-stu-id="1164f-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="1164f-120">**重新打开原因代码**</span><span class="sxs-lookup"><span data-stu-id="1164f-120">**Reopen reason code**</span></span> | <span data-ttu-id="1164f-121">重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="1164f-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="1164f-122">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="1164f-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="1164f-123">如有必要，用户可以更改 **重新打开原因代码**。</span><span class="sxs-lookup"><span data-stu-id="1164f-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="1164f-124">**生命事件原因代码**</span><span class="sxs-lookup"><span data-stu-id="1164f-124">**Life event reason code**</span></span> | <span data-ttu-id="1164f-125">生命事件发生时要使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="1164f-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="1164f-126">**比率更改原因代码**</span><span class="sxs-lookup"><span data-stu-id="1164f-126">**Rate change reason code**</span></span> | <span data-ttu-id="1164f-127">在比率更改更新流程中取消和重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="1164f-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="1164f-128">指示比率更改更新流程更改了哪些记录。</span><span class="sxs-lookup"><span data-stu-id="1164f-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="1164f-129">**年度福利薪金**</span><span class="sxs-lookup"><span data-stu-id="1164f-129">**Benefits annual salary**</span></span> | <span data-ttu-id="1164f-130">使您可以为员工设置 **福利年薪** 金额。</span><span class="sxs-lookup"><span data-stu-id="1164f-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="1164f-131">人力资源部门在确定覆盖范围金额时将使用 **福利年薪** 金额，而不是固定薪酬年度金额。</span><span class="sxs-lookup"><span data-stu-id="1164f-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="1164f-132">**新雇员符合资格**</span><span class="sxs-lookup"><span data-stu-id="1164f-132">**New hire eligible**</span></span> | <span data-ttu-id="1164f-133">指定新雇员是否符合资格。</span><span class="sxs-lookup"><span data-stu-id="1164f-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="1164f-134">**新雇用登记期间**</span><span class="sxs-lookup"><span data-stu-id="1164f-134">**New hire enrollment period**</span></span> | <span data-ttu-id="1164f-135">允许新雇用登记的时间段。</span><span class="sxs-lookup"><span data-stu-id="1164f-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="1164f-136">**注意**：此设置将覆盖您在计划资格规则中设置的所有新雇用登记期间。</span><span class="sxs-lookup"><span data-stu-id="1164f-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="1164f-137">**默认付薪频率**</span><span class="sxs-lookup"><span data-stu-id="1164f-137">**Default pay frequency**</span></span> | <span data-ttu-id="1164f-138">添加新工作人员时使用的默认付薪频率。</span><span class="sxs-lookup"><span data-stu-id="1164f-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="1164f-139">**生命事件已启用**</span><span class="sxs-lookup"><span data-stu-id="1164f-139">**Life events enabled**</span></span> | <span data-ttu-id="1164f-140">启用生命事件。</span><span class="sxs-lookup"><span data-stu-id="1164f-140">Enables life events.</span></span> |
   | <span data-ttu-id="1164f-141">**隐藏旧版福利窗体**</span><span class="sxs-lookup"><span data-stu-id="1164f-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="1164f-142">允许您隐藏旧版福利窗体。</span><span class="sxs-lookup"><span data-stu-id="1164f-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="1164f-143">**福利验证**</span><span class="sxs-lookup"><span data-stu-id="1164f-143">**Benefit verification**</span></span> | <span data-ttu-id="1164f-144">自助服务福利结账期间时要使用的验证文本。</span><span class="sxs-lookup"><span data-stu-id="1164f-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="1164f-145">**自动选择指定人员**</span><span class="sxs-lookup"><span data-stu-id="1164f-145">**Auto select designees**</span></span> | <span data-ttu-id="1164f-146">指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="1164f-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="1164f-147">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1164f-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="1164f-148">配置员工自助服务参数</span><span class="sxs-lookup"><span data-stu-id="1164f-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="1164f-149">在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="1164f-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="1164f-150">在 **福利管理** 选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="1164f-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="1164f-151">字段</span><span class="sxs-lookup"><span data-stu-id="1164f-151">Field</span></span> | <span data-ttu-id="1164f-152">说明</span><span class="sxs-lookup"><span data-stu-id="1164f-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1164f-153">**福利验证**</span><span class="sxs-lookup"><span data-stu-id="1164f-153">**Benefit verification**</span></span> | <span data-ttu-id="1164f-154">自助服务福利结账期间时要使用的验证文本。</span><span class="sxs-lookup"><span data-stu-id="1164f-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="1164f-155">**自动选择指定人员**</span><span class="sxs-lookup"><span data-stu-id="1164f-155">**Auto select designees**</span></span> | <span data-ttu-id="1164f-156">指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="1164f-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="1164f-157">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1164f-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]