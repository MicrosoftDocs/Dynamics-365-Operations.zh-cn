---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712368"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="c4b3f-103">配置休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="c4b3f-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="c4b3f-104">在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：</span><span class="sxs-lookup"><span data-stu-id="c4b3f-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="c4b3f-105">休假请求的编号规则</span><span class="sxs-lookup"><span data-stu-id="c4b3f-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="c4b3f-106">家庭医疗休假法 (FMLA) 设置</span><span class="sxs-lookup"><span data-stu-id="c4b3f-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="c4b3f-107">休假和缺勤请求的员工自助服务设置</span><span class="sxs-lookup"><span data-stu-id="c4b3f-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="c4b3f-108">休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="c4b3f-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="c4b3f-109">查看和更改人力资源参数</span><span class="sxs-lookup"><span data-stu-id="c4b3f-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="c4b3f-110">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c4b3f-111">在**设置**下，选择**人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c4b3f-112">在**编号规则**选项卡上，验证**休假请求 ID** 的**编号规则代码**并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="c4b3f-113">此设置确定用于向休假请求自动分配 ID 的顺序。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="c4b3f-114">在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="c4b3f-115">在**员工自助服务**选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="c4b3f-116">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="c4b3f-117">查看和更改休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="c4b3f-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="c4b3f-118">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c4b3f-119">在**设置**下，选择**休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="c4b3f-120">在**常规**选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="c4b3f-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="c4b3f-121">将**休假和缺勤单位**设置为小时或天。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="c4b3f-122">如果为天，则可以选择**启用半天定义**，以便允许员工在休假请求中选择前半天或后半天。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="c4b3f-123">选择**服务生效日期的月份**以设置使用服务月份的休假计划的假期额度费率生效时间。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="c4b3f-124">选择**余额计算**以显示截至今日的余额或应计期间的余额。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="c4b3f-125">如果选择**截至今日的余额**，则余额显示截止今日的所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="c4b3f-126">如果选择**截至应计期间的余额**，则余额显示截止休假计划中的频率定义的应计期间所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="c4b3f-127">设置结转到期批处理作业的开始时间。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="c4b3f-128">为**允许员工购买休假**和**允许员工出售休假**选择**是**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="c4b3f-129">如果为这些选项选择**是**，可以创建购买和出售休假策略，让员工能够提交购买和出售休假请求。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="c4b3f-130">配置日历参数</span><span class="sxs-lookup"><span data-stu-id="c4b3f-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="c4b3f-131">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c4b3f-132">在**设置**下，选择**休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="c4b3f-133">在**日历**选项卡上，根据需要更改日历设置。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="c4b3f-134">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="c4b3f-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4b3f-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="c4b3f-135">See also</span></span>

- [<span data-ttu-id="c4b3f-136">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="c4b3f-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
