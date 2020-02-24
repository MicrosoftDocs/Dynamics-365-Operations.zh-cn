---
title: 设置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中配置福利管理的参数。
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008231"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="3a41f-103">设置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="3a41f-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3a41f-104">您必须先配置福利管理参数，然后才能在 Microsoft Dynamics 365 Human Resources 中设置休假计划。</span><span class="sxs-lookup"><span data-stu-id="3a41f-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="3a41f-105">这些参数设置默认值、原因代码和其他选项。</span><span class="sxs-lookup"><span data-stu-id="3a41f-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="3a41f-106">配置常规参数</span><span class="sxs-lookup"><span data-stu-id="3a41f-106">Configure general parameters</span></span>

1. <span data-ttu-id="3a41f-107">在**福利管理**工作区中，在**设置**下，选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3a41f-108">在**常规**选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="3a41f-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3a41f-109">字段</span><span class="sxs-lookup"><span data-stu-id="3a41f-109">Field</span></span> | <span data-ttu-id="3a41f-110">说明</span><span class="sxs-lookup"><span data-stu-id="3a41f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3a41f-111">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="3a41f-111">**Country/region**</span></span> | <span data-ttu-id="3a41f-112">**国家/地区**字段确定邮政编码/省/市/自治区的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="3a41f-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="3a41f-113">所选国家/地区首先显示在下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="3a41f-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="3a41f-114">**登记原因代码**</span><span class="sxs-lookup"><span data-stu-id="3a41f-114">**Enrollment reason code**</span></span> | <span data-ttu-id="3a41f-115">选择在开放登记处理期间创建员工计划时要使用的默认原因代码。</span><span class="sxs-lookup"><span data-stu-id="3a41f-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="3a41f-116">**取消原因代码**</span><span class="sxs-lookup"><span data-stu-id="3a41f-116">**Cancellation reason code**</span></span> | <span data-ttu-id="3a41f-117">取消员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="3a41f-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="3a41f-118">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="3a41f-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3a41f-119">如有必要，用户可以更改**取消原因代码**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="3a41f-120">**重新打开原因代码**</span><span class="sxs-lookup"><span data-stu-id="3a41f-120">**Reopen reason code**</span></span> | <span data-ttu-id="3a41f-121">重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="3a41f-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="3a41f-122">将在取消过程中显示在对话框中。</span><span class="sxs-lookup"><span data-stu-id="3a41f-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3a41f-123">如有必要，用户可以更改**重新打开原因代码**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="3a41f-124">**生命事件原因代码**</span><span class="sxs-lookup"><span data-stu-id="3a41f-124">**Life event reason code**</span></span> | <span data-ttu-id="3a41f-125">生命事件发生时要使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="3a41f-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="3a41f-126">**比率更改原因代码**</span><span class="sxs-lookup"><span data-stu-id="3a41f-126">**Rate change reason code**</span></span> | <span data-ttu-id="3a41f-127">在比率更改更新流程中取消和重新打开员工福利计划时使用的原因代码。</span><span class="sxs-lookup"><span data-stu-id="3a41f-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="3a41f-128">指示比率更改更新流程更改了哪些记录。</span><span class="sxs-lookup"><span data-stu-id="3a41f-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="3a41f-129">**新雇员符合资格**</span><span class="sxs-lookup"><span data-stu-id="3a41f-129">**New hire eligible**</span></span> | <span data-ttu-id="3a41f-130">指定新雇员是否符合资格。</span><span class="sxs-lookup"><span data-stu-id="3a41f-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="3a41f-131">**新雇用登记期间**</span><span class="sxs-lookup"><span data-stu-id="3a41f-131">**New hire enrollment period**</span></span> | <span data-ttu-id="3a41f-132">允许新雇用登记的时间段。</span><span class="sxs-lookup"><span data-stu-id="3a41f-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="3a41f-133">**注意**：此设置将覆盖您在计划资格规则中设置的所有新雇用登记期间。</span><span class="sxs-lookup"><span data-stu-id="3a41f-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="3a41f-134">**年薪增强**</span><span class="sxs-lookup"><span data-stu-id="3a41f-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="3a41f-135">指定是否自动计算**雇用福利详细信息**中的**年度福利薪金**金额。</span><span class="sxs-lookup"><span data-stu-id="3a41f-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="3a41f-136">基于员工的**固定薪酬付薪比率**、**平均工时数**和**付款频率**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="3a41f-137">**平均工时数** x **固定付薪比率** x **付款频率** (付款期间数) = **年度福利薪金**</span><span class="sxs-lookup"><span data-stu-id="3a41f-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="3a41f-138">如果**平均工时数**、**固定薪酬付薪比率**或**付款频率**字段中的任何值更改，系统将基于更改后的值自动重新计算员工的**年度福利薪金**金额。</span><span class="sxs-lookup"><span data-stu-id="3a41f-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="3a41f-139">系统将创建**生效日期**记录来标识更改发生的确切日期和时间。</span><span class="sxs-lookup"><span data-stu-id="3a41f-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="3a41f-140">如有必要，您可以手动编辑**年度福利薪金**金额。</span><span class="sxs-lookup"><span data-stu-id="3a41f-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="3a41f-141">**生命事件已启用**</span><span class="sxs-lookup"><span data-stu-id="3a41f-141">**Life events enabled**</span></span> | <span data-ttu-id="3a41f-142">启用生命事件。</span><span class="sxs-lookup"><span data-stu-id="3a41f-142">Enables life events.</span></span> |
   | <span data-ttu-id="3a41f-143">**隐藏旧版福利窗体**</span><span class="sxs-lookup"><span data-stu-id="3a41f-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="3a41f-144">允许您隐藏旧版福利窗体。</span><span class="sxs-lookup"><span data-stu-id="3a41f-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="3a41f-145">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="3a41f-146">配置员工自助服务参数</span><span class="sxs-lookup"><span data-stu-id="3a41f-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="3a41f-147">在**福利管理**工作区中，在**设置**下，选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3a41f-148">在**员工自助服务**选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="3a41f-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3a41f-149">字段</span><span class="sxs-lookup"><span data-stu-id="3a41f-149">Field</span></span> | <span data-ttu-id="3a41f-150">说明</span><span class="sxs-lookup"><span data-stu-id="3a41f-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3a41f-151">**福利验证**</span><span class="sxs-lookup"><span data-stu-id="3a41f-151">**Benefit verification**</span></span> | <span data-ttu-id="3a41f-152">自助服务福利结账期间时要使用的验证文本。</span><span class="sxs-lookup"><span data-stu-id="3a41f-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="3a41f-153">**自动选择指定人员**</span><span class="sxs-lookup"><span data-stu-id="3a41f-153">**Auto select designees**</span></span> | <span data-ttu-id="3a41f-154">指定是否根据依赖方和受益人的计划选项的资格自动选择依赖方和受益人。</span><span class="sxs-lookup"><span data-stu-id="3a41f-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="3a41f-155">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="3a41f-155">Select **Save**.</span></span>
