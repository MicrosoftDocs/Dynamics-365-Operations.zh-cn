---
title: 配置休假和缺勤类型
description: 在 Dynamics 365 Human Resources 中设置员工可以申请的休假类型。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198042"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="68437-103">配置休假和缺勤类型</span><span class="sxs-lookup"><span data-stu-id="68437-103">Configure leave and absence types</span></span>

<span data-ttu-id="68437-104">Dynamics 365 Human Resources 中的休假类型定义员工可报告的各种缺勤类型。</span><span class="sxs-lookup"><span data-stu-id="68437-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="68437-105">您可以根据组织的需求定制休假类型。</span><span class="sxs-lookup"><span data-stu-id="68437-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="68437-106">休假类型的示例包括：</span><span class="sxs-lookup"><span data-stu-id="68437-106">Examples of leave types include:</span></span>

- <span data-ttu-id="68437-107">带薪休息时间 (PTO)</span><span class="sxs-lookup"><span data-stu-id="68437-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="68437-108">无薪假</span><span class="sxs-lookup"><span data-stu-id="68437-108">Unpaid leave</span></span>
- <span data-ttu-id="68437-109">带薪假</span><span class="sxs-lookup"><span data-stu-id="68437-109">Paid vacation</span></span>
- <span data-ttu-id="68437-110">病假</span><span class="sxs-lookup"><span data-stu-id="68437-110">Sick leave</span></span>
- <span data-ttu-id="68437-111">医疗休假</span><span class="sxs-lookup"><span data-stu-id="68437-111">Medical leave</span></span>
- <span data-ttu-id="68437-112">探亲假</span><span class="sxs-lookup"><span data-stu-id="68437-112">Family leave</span></span>
- <span data-ttu-id="68437-113">短期残障</span><span class="sxs-lookup"><span data-stu-id="68437-113">Short-term disability</span></span>
- <span data-ttu-id="68437-114">丧亲假</span><span class="sxs-lookup"><span data-stu-id="68437-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="68437-115">添加休假类型</span><span class="sxs-lookup"><span data-stu-id="68437-115">Add a leave type</span></span>

1. <span data-ttu-id="68437-116">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="68437-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="68437-117">在**设置**下，选择**休假和缺勤类型**。</span><span class="sxs-lookup"><span data-stu-id="68437-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="68437-118">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="68437-118">Select **New**.</span></span>

4. <span data-ttu-id="68437-119">在**类型**下输入休假类型的名称，从**工作流 ID** 中选择一个工作流，然后在**说明**下输入说明。</span><span class="sxs-lookup"><span data-stu-id="68437-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="68437-120">在**一般**中，从**类别**下拉列表中选择**无**、**计划**或**计划外**。</span><span class="sxs-lookup"><span data-stu-id="68437-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="68437-121">从**收入代码**下拉列表中选择一个收入代码。</span><span class="sxs-lookup"><span data-stu-id="68437-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="68437-122">在**需要原因代码**下，选择您是否希望提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="68437-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="68437-123">如果您希望提供原因代码，可能需要添加原因代码。</span><span class="sxs-lookup"><span data-stu-id="68437-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="68437-124">在**原因代码**下，选择**添加**，选择一个原因代码，然后选择它旁边的**已启用**复选框。</span><span class="sxs-lookup"><span data-stu-id="68437-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="68437-125">在**限制对选定角色的访问**下，选择是否要限制访问。</span><span class="sxs-lookup"><span data-stu-id="68437-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="68437-126">然后在**此休假类型的安全角色**下选择安全角色。</span><span class="sxs-lookup"><span data-stu-id="68437-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="68437-127">安全角色在您在此过程前面在**工作流 ID** 下选择的工作流程中定义。</span><span class="sxs-lookup"><span data-stu-id="68437-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="68437-128">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="68437-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="68437-129">配置请假类型规则</span><span class="sxs-lookup"><span data-stu-id="68437-129">Configure leave type rules</span></span>

1. <span data-ttu-id="68437-130">设置休假类型的舍入选项。</span><span class="sxs-lookup"><span data-stu-id="68437-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="68437-131">选项包括**无**、**向上**、**向下**和**最近**。</span><span class="sxs-lookup"><span data-stu-id="68437-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="68437-132">您还可以为休假类型设置舍入精度。</span><span class="sxs-lookup"><span data-stu-id="68437-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="68437-133">为休假类型设置**假日更正**。</span><span class="sxs-lookup"><span data-stu-id="68437-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="68437-134">选择此选项时，Human Resources 将使用工作日的假日数来确定如何累积休假类型的休息时间。</span><span class="sxs-lookup"><span data-stu-id="68437-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="68437-135">例如，如果圣诞节在星期一，Human Resources 在处理累积时将从休假类型中减去一天。</span><span class="sxs-lookup"><span data-stu-id="68437-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="68437-136">在工作时间日历中设置假日。</span><span class="sxs-lookup"><span data-stu-id="68437-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="68437-137">有关详细信息，请参阅[创建工作时间日历](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="68437-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="68437-138">配置预览功能</span><span class="sxs-lookup"><span data-stu-id="68437-138">Configure preview features</span></span>

<span data-ttu-id="68437-139">如果您已启用休假和缺勤的预览功能，您还需要为其配置设置。</span><span class="sxs-lookup"><span data-stu-id="68437-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="68437-140">选择结转余额要转移到的休假类型。</span><span class="sxs-lookup"><span data-stu-id="68437-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="68437-141">也可以为结转创建新的休假类型。</span><span class="sxs-lookup"><span data-stu-id="68437-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="68437-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="68437-142">See also</span></span>

- [<span data-ttu-id="68437-143">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="68437-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="68437-144">创建休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="68437-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="68437-145">创建工作时间日历</span><span class="sxs-lookup"><span data-stu-id="68437-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
