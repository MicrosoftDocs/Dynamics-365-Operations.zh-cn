---
title: 设置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中配置福利管理的参数。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429975"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="ec1cb-103">设置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="ec1cb-103">Set Benefits management parameters</span></span>

<span data-ttu-id="ec1cb-104">您必须先配置福利管理参数，然后才能在 Microsoft Dynamics 365 Human Resources 中设置休假计划。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="ec1cb-105">这些参数设置默认值、原因代码和其他选项。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="ec1cb-106">配置常规参数</span><span class="sxs-lookup"><span data-stu-id="ec1cb-106">Configure general parameters</span></span>

1. <span data-ttu-id="ec1cb-107">在**福利管理**工作区中，在**设置**下，选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="ec1cb-108">在**常规**选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ec1cb-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ec1cb-109">字段</span><span class="sxs-lookup"><span data-stu-id="ec1cb-109">Field</span></span> | <span data-ttu-id="ec1cb-110">说明</span><span class="sxs-lookup"><span data-stu-id="ec1cb-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ec1cb-111">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-111">**Country/region**</span></span> | <span data-ttu-id="ec1cb-112">**国家/地区**字段确定邮政编码/省/市/自治区的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="ec1cb-113">所选国家/地区首先显示在下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="ec1cb-114">**登记原因代码**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-114">**Enrollment reason code**</span></span> | <span data-ttu-id="ec1cb-115">选择在开放登记处理期间创建员工计划时要使用的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="ec1cb-116">**取消原因代码**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-116">**Cancellation reason code**</span></span> | <span data-ttu-id="ec1cb-117">取消员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="ec1cb-118">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ec1cb-119">如有必要，用户可以更改**取消原因代码**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="ec1cb-120">**重新打开原因代码**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-120">**Reopen reason code**</span></span> | <span data-ttu-id="ec1cb-121">重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="ec1cb-122">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ec1cb-123">如有必要，用户可以更改**重新打开原因代码**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="ec1cb-124">**生命事件原因代码**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-124">**Life event reason code**</span></span> | <span data-ttu-id="ec1cb-125">生命事件发生时要使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="ec1cb-126">**比率更改原因代码**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-126">**Rate change reason code**</span></span> | <span data-ttu-id="ec1cb-127">在比率更改更新流程中取消和重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="ec1cb-128">指示比率更改更新流程更改了哪些记录。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="ec1cb-129">**新雇员符合资格**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-129">**New hire eligible**</span></span> | <span data-ttu-id="ec1cb-130">指定新雇员是否符合资格。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="ec1cb-131">**新雇用登记期间**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-131">**New hire enrollment period**</span></span> | <span data-ttu-id="ec1cb-132">允许新雇用登记的时间段。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="ec1cb-133">**注意**：此设置将覆盖您在计划资格规则中设置的所有新雇用登记期间。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="ec1cb-134">**生命事件已启用**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-134">**Life events enabled**</span></span> | <span data-ttu-id="ec1cb-135">启用生命事件。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-135">Enables life events.</span></span> |
   | <span data-ttu-id="ec1cb-136">**隐藏旧版福利窗体**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="ec1cb-137">允许您隐藏旧版福利窗体。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="ec1cb-138">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="ec1cb-139">配置员工自助服务参数</span><span class="sxs-lookup"><span data-stu-id="ec1cb-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="ec1cb-140">在**福利管理**工作区中，在**设置**下，选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="ec1cb-141">在**员工自助服务**选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ec1cb-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ec1cb-142">字段</span><span class="sxs-lookup"><span data-stu-id="ec1cb-142">Field</span></span> | <span data-ttu-id="ec1cb-143">说明</span><span class="sxs-lookup"><span data-stu-id="ec1cb-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ec1cb-144">**福利验证**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-144">**Benefit verification**</span></span> | <span data-ttu-id="ec1cb-145">自助服务福利结账期间时要使用的验证文本。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="ec1cb-146">**自动选择指定人员**</span><span class="sxs-lookup"><span data-stu-id="ec1cb-146">**Auto select designees**</span></span> | <span data-ttu-id="ec1cb-147">指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="ec1cb-148">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="ec1cb-148">Select **Save**.</span></span>
