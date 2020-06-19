---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 5e4d3b3e4b373631bed5e2d7e3c3a4e14f0c5c98
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428936"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="966aa-103">配置休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="966aa-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="966aa-104">在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：</span><span class="sxs-lookup"><span data-stu-id="966aa-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="966aa-105">休假请求的编号规则</span><span class="sxs-lookup"><span data-stu-id="966aa-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="966aa-106">家庭医疗休假法 (FMLA) 设置</span><span class="sxs-lookup"><span data-stu-id="966aa-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="966aa-107">休假和缺勤请求的员工自助服务设置</span><span class="sxs-lookup"><span data-stu-id="966aa-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="966aa-108">休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="966aa-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="966aa-109">查看和更改人力资源参数</span><span class="sxs-lookup"><span data-stu-id="966aa-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="966aa-110">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="966aa-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="966aa-111">在**设置**下，选择**人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="966aa-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="966aa-112">在**编号规则**选项卡上，验证**休假请求 ID** 的**编号规则代码**并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="966aa-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="966aa-113">此设置确定用于向休假请求自动分配 ID 的顺序。</span><span class="sxs-lookup"><span data-stu-id="966aa-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="966aa-114">在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="966aa-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="966aa-115">在**员工自助服务**选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="966aa-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="966aa-116">在**休假和缺勤**选项卡上，验证设置并根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="966aa-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="966aa-117">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="966aa-117">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="966aa-118">查看和更改休假和缺勤参数</span><span class="sxs-lookup"><span data-stu-id="966aa-118">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="966aa-119">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="966aa-119">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="966aa-120">在**设置**下，选择**休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="966aa-120">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="966aa-121">在**常规**选项卡上，设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="966aa-121">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="966aa-122">将**休假和缺勤单位**设置为小时或天。</span><span class="sxs-lookup"><span data-stu-id="966aa-122">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="966aa-123">如果为天，则可以选择**启用半天定义**，以便允许员工在休假请求中选择前半天或后半天。</span><span class="sxs-lookup"><span data-stu-id="966aa-123">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="966aa-124">选择**服务生效日期的月份**以设置使用服务月份的休假计划的假期额度费率生效时间。</span><span class="sxs-lookup"><span data-stu-id="966aa-124">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="966aa-125">选择**余额计算**以显示截至今日的余额或应计期间的余额。</span><span class="sxs-lookup"><span data-stu-id="966aa-125">Select **Balance calculation** to display balances display as of today or as of the accrual period.</span></span> <span data-ttu-id="966aa-126">如果选择**截至今日的余额**，则余额显示截止今日的所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="966aa-126">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="966aa-127">如果选择**截至应计期间的余额**，则余额显示截止休假计划中的频率定义的应计期间所有应计、调整和请求的总计。</span><span class="sxs-lookup"><span data-stu-id="966aa-127">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

## <a name="configure-calendar-parameters"></a><span data-ttu-id="966aa-128">配置日历参数</span><span class="sxs-lookup"><span data-stu-id="966aa-128">Configure calendar parameters</span></span>

1. <span data-ttu-id="966aa-129">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="966aa-129">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="966aa-130">在**设置**下，选择**休假和缺勤参数**。</span><span class="sxs-lookup"><span data-stu-id="966aa-130">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="966aa-131">在**日历**选项卡上，根据需要更改日历设置。</span><span class="sxs-lookup"><span data-stu-id="966aa-131">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="966aa-132">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="966aa-132">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="966aa-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="966aa-133">See also</span></span>

- [<span data-ttu-id="966aa-134">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="966aa-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
