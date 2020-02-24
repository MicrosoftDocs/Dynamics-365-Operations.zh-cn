---
title: 创建工作时间日历
description: 在 Dynamics 365 Human Resources 中定义工作时间日历、假日和非工作时间。
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
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008261"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="0ec91-103">创建工作时间日历</span><span class="sxs-lookup"><span data-stu-id="0ec91-103">Create a working time calendar</span></span>

<span data-ttu-id="0ec91-104">Dynamics 365 Human Resources 中的工作时间日历显示员工在您的组织中工作的天数和时数。</span><span class="sxs-lookup"><span data-stu-id="0ec91-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="0ec91-105">当员工提交休息时间请求时，他们不必担心假日和歇业的影响。</span><span class="sxs-lookup"><span data-stu-id="0ec91-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="0ec91-106">要简化休息时间请求，请为您的组织配置以下项目：</span><span class="sxs-lookup"><span data-stu-id="0ec91-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="0ec91-107">工作时间日历</span><span class="sxs-lookup"><span data-stu-id="0ec91-107">Working time calendar</span></span>
- <span data-ttu-id="0ec91-108">假日和歇业</span><span class="sxs-lookup"><span data-stu-id="0ec91-108">Holidays and closures</span></span>
- <span data-ttu-id="0ec91-109">非工作时间</span><span class="sxs-lookup"><span data-stu-id="0ec91-109">Non-work time</span></span>

<span data-ttu-id="0ec91-110">您可以在设置工作时间日历时添加最后两个项目。</span><span class="sxs-lookup"><span data-stu-id="0ec91-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="0ec91-111">您还可以单独配置或更新它们。</span><span class="sxs-lookup"><span data-stu-id="0ec91-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="0ec91-112">设置工作日历</span><span class="sxs-lookup"><span data-stu-id="0ec91-112">Set up a working time calendar</span></span>

<span data-ttu-id="0ec91-113">设置至少一个工作时间日历，以显示您的工作天数和时数。</span><span class="sxs-lookup"><span data-stu-id="0ec91-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="0ec91-114">如果您在多个国家和地区设有分点，您可能需要为每个区域设置工作时间日历。</span><span class="sxs-lookup"><span data-stu-id="0ec91-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="0ec91-115">在**组织管理**页面上，选择**日历**。</span><span class="sxs-lookup"><span data-stu-id="0ec91-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="0ec91-116">选择**新建**，然后为日历输入名称和说明。</span><span class="sxs-lookup"><span data-stu-id="0ec91-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="0ec91-117">在**生成选项**下，为您的组织选择工作日，然后输入工作时间。</span><span class="sxs-lookup"><span data-stu-id="0ec91-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="0ec91-118">要添加假日和歇业，请选择**假日和歇业**旁边的**添加**按钮。</span><span class="sxs-lookup"><span data-stu-id="0ec91-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="0ec91-119">要添加非工作时间（例如午餐或工间休息），请选择**非工作时间**下的**添加**并输入名称和时间范围。</span><span class="sxs-lookup"><span data-stu-id="0ec91-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="0ec91-120">在**天数**下，选择**生成**以生成日历中包含的天数。</span><span class="sxs-lookup"><span data-stu-id="0ec91-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="0ec91-121">为日历输入日期范围，然后选择**生成日**。</span><span class="sxs-lookup"><span data-stu-id="0ec91-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="0ec91-122">要添加工作计划，在**工作计划**下，选择**添加**，然后输入每个工作计划的时间。</span><span class="sxs-lookup"><span data-stu-id="0ec91-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="0ec91-123">配置假日和歇业</span><span class="sxs-lookup"><span data-stu-id="0ec91-123">Configure holidays and closures</span></span>

<span data-ttu-id="0ec91-124">您可以从工作时间日历单独添加或更改假日和歇业。</span><span class="sxs-lookup"><span data-stu-id="0ec91-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="0ec91-125">在**组织管理**页面上，选择**假日和歇业**。</span><span class="sxs-lookup"><span data-stu-id="0ec91-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="0ec91-126">选择**新建**，然后为假日和歇业输入名称和日期。</span><span class="sxs-lookup"><span data-stu-id="0ec91-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="0ec91-127">配置非工作时间</span><span class="sxs-lookup"><span data-stu-id="0ec91-127">Configure non-work time</span></span>

<span data-ttu-id="0ec91-128">您可以从工作时间日历单独添加或更改非工作时间。</span><span class="sxs-lookup"><span data-stu-id="0ec91-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="0ec91-129">在**组织管理**页面上，选择**非工作时间**。</span><span class="sxs-lookup"><span data-stu-id="0ec91-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="0ec91-130">选择**新建**，然后为非工作时间输入名称和时间范围。</span><span class="sxs-lookup"><span data-stu-id="0ec91-130">Select **New** and enter a name and time range for the non-work time.</span></span>

## <a name="leave-and-absence-preview-feature"></a><span data-ttu-id="0ec91-131">休假和缺勤预览功能</span><span class="sxs-lookup"><span data-stu-id="0ec91-131">Leave and absence preview feature</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="0ec91-132">如果已启用“休假和缺勤银行假日更正”预览功能，Human Resources 将使用假日和歇业日期来确定要为日历中登记的员工调整的天数。</span><span class="sxs-lookup"><span data-stu-id="0ec91-132">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ec91-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ec91-133">See also</span></span>

- [<span data-ttu-id="0ec91-134">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="0ec91-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="0ec91-135">配置休假和缺勤类型</span><span class="sxs-lookup"><span data-stu-id="0ec91-135">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
