---
title: 配置休假和缺勤类型
description: 在 Dynamics 365 Human Resources 中设置员工可以申请的休假类型。
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 098f614da80a1e7e3e31b30cea707ecfbd5b0a70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056604"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="ba534-103">配置休假和缺勤类型</span><span class="sxs-lookup"><span data-stu-id="ba534-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ba534-104">Dynamics 365 Human Resources 中的休假类型定义员工可报告的各种缺勤类型。</span><span class="sxs-lookup"><span data-stu-id="ba534-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="ba534-105">您可以根据组织的需求定制休假类型。</span><span class="sxs-lookup"><span data-stu-id="ba534-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="ba534-106">休假类型的示例包括：</span><span class="sxs-lookup"><span data-stu-id="ba534-106">Examples of leave types include:</span></span>

- <span data-ttu-id="ba534-107">带薪休息时间 (PTO)</span><span class="sxs-lookup"><span data-stu-id="ba534-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="ba534-108">无薪假</span><span class="sxs-lookup"><span data-stu-id="ba534-108">Unpaid leave</span></span>
- <span data-ttu-id="ba534-109">带薪假</span><span class="sxs-lookup"><span data-stu-id="ba534-109">Paid vacation</span></span>
- <span data-ttu-id="ba534-110">病假</span><span class="sxs-lookup"><span data-stu-id="ba534-110">Sick leave</span></span>
- <span data-ttu-id="ba534-111">医疗休假</span><span class="sxs-lookup"><span data-stu-id="ba534-111">Medical leave</span></span>
- <span data-ttu-id="ba534-112">探亲假</span><span class="sxs-lookup"><span data-stu-id="ba534-112">Family leave</span></span>
- <span data-ttu-id="ba534-113">短期残障</span><span class="sxs-lookup"><span data-stu-id="ba534-113">Short-term disability</span></span>
- <span data-ttu-id="ba534-114">丧亲假</span><span class="sxs-lookup"><span data-stu-id="ba534-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="ba534-115">添加休假类型</span><span class="sxs-lookup"><span data-stu-id="ba534-115">Add a leave type</span></span>

1. <span data-ttu-id="ba534-116">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="ba534-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ba534-117">在 **设置** 下，选择 **休假和缺勤类型**。</span><span class="sxs-lookup"><span data-stu-id="ba534-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="ba534-118">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="ba534-118">Select **New**.</span></span>

4. <span data-ttu-id="ba534-119">在 **类型** 下输入休假类型的名称，从 **工作流 ID** 中选择一个工作流，然后在 **说明** 下输入说明。</span><span class="sxs-lookup"><span data-stu-id="ba534-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="ba534-120">在 **一般** 中，从 **类别** 下拉列表中选择 **无**、**计划** 或 **计划外**。</span><span class="sxs-lookup"><span data-stu-id="ba534-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="ba534-121">从 **收入代码** 下拉列表中选择一个收入代码。</span><span class="sxs-lookup"><span data-stu-id="ba534-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="ba534-122">在 **需要原因代码** 下，选择您是否希望提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="ba534-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="ba534-123">如果您希望提供原因代码，可能需要添加原因代码。</span><span class="sxs-lookup"><span data-stu-id="ba534-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="ba534-124">在 **原因代码** 下，选择 **添加**，选择一个原因代码，然后选择它旁边的 **已启用** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ba534-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="ba534-125">在 **限制对选定角色的访问** 下，选择是否要限制访问。</span><span class="sxs-lookup"><span data-stu-id="ba534-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="ba534-126">然后在 **此休假类型的安全角色** 下选择安全角色。</span><span class="sxs-lookup"><span data-stu-id="ba534-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="ba534-127">安全角色在您在此过程前面在 **工作流 ID** 下选择的工作流程中定义。</span><span class="sxs-lookup"><span data-stu-id="ba534-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="ba534-128">在 **日历颜色** 下，选择该请假类型在请假和缺勤日历上显示的颜色。</span><span class="sxs-lookup"><span data-stu-id="ba534-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="ba534-129">在 **暂停关系** 下，选择是否要让此休假类型暂停其他休假类型或被其他休假类型暂停。</span><span class="sxs-lookup"><span data-stu-id="ba534-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="ba534-130">当提交休假请求以暂停休假类型时，将自动为暂停的休假类型创建休假暂停。</span><span class="sxs-lookup"><span data-stu-id="ba534-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="ba534-131">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ba534-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="ba534-132">配置请假类型规则</span><span class="sxs-lookup"><span data-stu-id="ba534-132">Configure leave type rules</span></span>

1. <span data-ttu-id="ba534-133">设置休假类型的舍入选项。</span><span class="sxs-lookup"><span data-stu-id="ba534-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="ba534-134">选项包括 **无**、**向上**、**向下** 和 **最近**。</span><span class="sxs-lookup"><span data-stu-id="ba534-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="ba534-135">您还可以为休假类型设置舍入精度。</span><span class="sxs-lookup"><span data-stu-id="ba534-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="ba534-136">为休假类型设置 **假日更正**。</span><span class="sxs-lookup"><span data-stu-id="ba534-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="ba534-137">选择此选项时，Human Resources 将使用工作日的假日数来确定如何累积休假类型的休息时间。</span><span class="sxs-lookup"><span data-stu-id="ba534-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="ba534-138">例如，如果圣诞节在星期一，Human Resources 在处理累积时将从休假类型中减去一天。</span><span class="sxs-lookup"><span data-stu-id="ba534-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="ba534-139">在工作时间日历中设置假日。</span><span class="sxs-lookup"><span data-stu-id="ba534-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="ba534-140">有关详细信息，请参阅[创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="ba534-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="ba534-141">为休假类型设置 **结转休假类型**。</span><span class="sxs-lookup"><span data-stu-id="ba534-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="ba534-142">选择此选项时，任何结转余额都将转移到指定的休假类型。</span><span class="sxs-lookup"><span data-stu-id="ba534-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="ba534-143">结转休假类型也需要包括在休假和缺勤计划中。</span><span class="sxs-lookup"><span data-stu-id="ba534-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="ba534-144">为休假类型定义 **到期规则**。</span><span class="sxs-lookup"><span data-stu-id="ba534-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="ba534-145">配置此选项时，可以选择天或月单位并设置有效期限。</span><span class="sxs-lookup"><span data-stu-id="ba534-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="ba534-146">您还可以设置到期规则的生效日期。</span><span class="sxs-lookup"><span data-stu-id="ba534-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="ba534-147">生效日期用于确定何时开始运行处理休假到期或规则生效日期的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="ba534-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="ba534-148">将批处理作业设置为处理后，到期本身将始终在休假计划开始日期发生。</span><span class="sxs-lookup"><span data-stu-id="ba534-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="ba534-149">例如，计划开始日期可能是 2020 年 1 月 1 日，但是直到 2020 年 6 月 1 日规则才创建。</span><span class="sxs-lookup"><span data-stu-id="ba534-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="ba534-150">通过将生效日期设置为 2020 年 6 月 1 日，规则将在下一年度边界（即 2021 年 1 月 1 日）处理。</span><span class="sxs-lookup"><span data-stu-id="ba534-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="ba534-151">到期时存在的任何休假余额将从休假类型中减去，并反映在休假余额中。</span><span class="sxs-lookup"><span data-stu-id="ba534-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="ba534-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba534-152">See also</span></span>

- [<span data-ttu-id="ba534-153">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="ba534-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="ba534-154">创建休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="ba534-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="ba534-155">创建工作时间日历</span><span class="sxs-lookup"><span data-stu-id="ba534-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="ba534-156">暂停休假</span><span class="sxs-lookup"><span data-stu-id="ba534-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
