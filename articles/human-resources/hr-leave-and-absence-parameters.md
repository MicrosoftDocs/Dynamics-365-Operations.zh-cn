---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
author: andreabichsel
ms.date: 11/02/2020
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
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056844"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="8a44a-103">配置休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8a44a-104">在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：</span><span class="sxs-lookup"><span data-stu-id="8a44a-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="8a44a-105">休假请求的编号规则</span><span class="sxs-lookup"><span data-stu-id="8a44a-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="8a44a-106">家庭医疗休假法 (FMLA) 设置</span><span class="sxs-lookup"><span data-stu-id="8a44a-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="8a44a-107">休假和缺勤请求的员工自助服务设置</span><span class="sxs-lookup"><span data-stu-id="8a44a-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="8a44a-108">休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="8a44a-109">查看和更改人力资源参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="8a44a-110">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8a44a-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8a44a-111">在 **设置** 下，选择 **人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="8a44a-112">在 **编号规则** 选项卡上，验证 **休假请求 ID** 的 **编号规则代码** 并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="8a44a-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="8a44a-113">此设置确定用于向休假请求自动分配 ID 的顺序。</span><span class="sxs-lookup"><span data-stu-id="8a44a-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="8a44a-114">在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="8a44a-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="8a44a-115">在 **员工自助服务** 选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="8a44a-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="8a44a-116">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8a44a-117">跨公司查看休假和缺勤当前处于预览状态。</span><span class="sxs-lookup"><span data-stu-id="8a44a-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="8a44a-118">您需要在 **沙盒** 环境中启用它以显示休假和缺勤的选项。</span><span class="sxs-lookup"><span data-stu-id="8a44a-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="8a44a-119">有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="8a44a-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="8a44a-120">查看和更改 Human Resources 共享参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="8a44a-121">在 **人事管理** 页面上，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8a44a-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8a44a-122">在 **设置** 下，选择 **Human Resources 共享参数**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="8a44a-123">在 **高级访问** 选项卡上，针对 **启用跨公司休假查看** 选择 **是** 以允许跨公司查看休假。</span><span class="sxs-lookup"><span data-stu-id="8a44a-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="8a44a-124">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="8a44a-125">查看和更改休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="8a44a-126">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8a44a-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8a44a-127">在 **设置** 下，选择 **休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="8a44a-128">在 **常规** 选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="8a44a-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="8a44a-129">将 **休假和缺勤单位** 设置为小时或天。</span><span class="sxs-lookup"><span data-stu-id="8a44a-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="8a44a-130">如果为天，则可以选择 **启用半天定义**，以便允许员工在休假请求中选择前半天或后半天。</span><span class="sxs-lookup"><span data-stu-id="8a44a-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="8a44a-131">选择 **服务生效日期的月份** 以设置使用服务月份的休假计划的假期额度费率生效时间。</span><span class="sxs-lookup"><span data-stu-id="8a44a-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="8a44a-132">选择 **余额计算** 以显示截至今日的余额或应计期间的余额。</span><span class="sxs-lookup"><span data-stu-id="8a44a-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="8a44a-133">如果选择 **截至今日的余额**，则余额显示截止今日的所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="8a44a-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="8a44a-134">如果选择 **截至应计期间的余额**，则余额显示截止休假计划中的频率定义的应计期间所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="8a44a-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="8a44a-135">设置结转到期批处理作业的开始时间。</span><span class="sxs-lookup"><span data-stu-id="8a44a-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="8a44a-136">为 **允许员工购买休假** 和 **允许员工出售休假** 选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="8a44a-137">如果为这些选项选择 **是**，可以创建购买和出售休假策略，让员工能够提交购买和出售休假请求。</span><span class="sxs-lookup"><span data-stu-id="8a44a-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="8a44a-138">配置日历参数</span><span class="sxs-lookup"><span data-stu-id="8a44a-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="8a44a-139">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="8a44a-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8a44a-140">在 **设置** 下，选择 **休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="8a44a-141">在 **日历** 选项卡上，根据需要更改日历设置。</span><span class="sxs-lookup"><span data-stu-id="8a44a-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="8a44a-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8a44a-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a44a-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a44a-143">See also</span></span>

- [<span data-ttu-id="8a44a-144">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="8a44a-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]