---
title: 安排维护计划
description: 本主题介绍资产管理中的安排维护作业。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b6e5bde83474fe8971e482af518f7cee23a2220
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875521"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="537b6-103">安排维护计划</span><span class="sxs-lookup"><span data-stu-id="537b6-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="537b6-104">安排预防性维护将按照为资产设置的维护计划为资产生成条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="537b6-105">可根据所选维护计划、资产类型和资产来安排日历条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="537b6-106">单击**资产管理** > **定期** > **预防性维护** > **安排维护计划**。</span><span class="sxs-lookup"><span data-stu-id="537b6-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="537b6-107">可在**期间**和**期间频率**字段中选择时间间隔。</span><span class="sxs-lookup"><span data-stu-id="537b6-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="537b6-108">**期间**和**期间频率**字段指示希望根据创建的维护计划（基于时间或计数器）提前多久创建维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="537b6-109">在下图中，将创建从当前日期开始三个月的维护安排行（= 工作订单安排）。</span><span class="sxs-lookup"><span data-stu-id="537b6-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="537b6-110">如果应该根据维护计划行自动创建工作订单，请在**如果在行中指定则自动创建**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="537b6-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="537b6-111">如果此切换按钮设置为“是”，*并且*还在**维护计划**中的维护计划行上选中了**自动创建**复选框，则基于维护计划行创建工作订单，并创建状态为“已创建工作订单”的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="537b6-112">如果仅选择了一个选项（此对话框中的**如果在行中指定则自动创建**切换按钮，或**维护安排**窗体中的**自动创建**复选框），则创建状态为“已创建”的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="537b6-113">在此情况下，将不创建任何工作订单。</span><span class="sxs-lookup"><span data-stu-id="537b6-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="537b6-114">可基于维护计划（时间或计数器）、资产、资产类型、功能位置和功能位置类型生成日历条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="537b6-115">如果需要，请单击**筛选**按钮并进行选择。</span><span class="sxs-lookup"><span data-stu-id="537b6-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="537b6-116">有关为功能位置安排维护计划的信息：如果在安排维护计划之后在**所有功能位置** > **维护计划**快速选项卡中更新维护计划的资产类型、制造商和型号的设置，则自动删除与功能位置有关的现有维护安排条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="537b6-117">若要创建新日历条目（与功能位置中已更新的维护计划设置对应），则必须为该功能位置运行新的维护计划安排。</span><span class="sxs-lookup"><span data-stu-id="537b6-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="537b6-118">有关为功能位置设置资产类型、制造商和型号的详细信息，请参阅[创建功能位置](../functional-locations/create-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="537b6-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="537b6-119">*示例：* 您希望为特定功能位置创建维护计划，这意味着安排维护计划时，将包括在任何给定时间为该功能位置设置的所有资产。</span><span class="sxs-lookup"><span data-stu-id="537b6-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="537b6-120">在此情况下，将创建一个维护计划并选择特定功能位置，但是“不”在维护计划中添加任何对象。</span><span class="sxs-lookup"><span data-stu-id="537b6-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any objects in the maintenance plan.</span></span> <span data-ttu-id="537b6-121">结果是，在安排该维护计划时，将为此时与功能位置关联的所有资产创建维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="537b6-122">如果在**资产类型**中对资产类型、制造商和型号进行更改，则这些更改仅影响使用所更新资产类型的新资产。</span><span class="sxs-lookup"><span data-stu-id="537b6-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="537b6-123">有关资产类型设置的详细信息，请参阅[资产类型](../setup-for-objects/object-types.md)。</span><span class="sxs-lookup"><span data-stu-id="537b6-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="537b6-124">单击**确定**开始为资产生成维护安排条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="537b6-125">将在**所有维护安排**列表页中显示生成的条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span>

![图 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="537b6-127">可在**安排维护计划**对话框的**在后台运行**快速选项卡上设置批处理作业，以便定期生成日历条目。</span><span class="sxs-lookup"><span data-stu-id="537b6-127">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="537b6-128">计划预防性维护时，将不创建预计开始日期和时间在系统日期和时间之前的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-128">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="537b6-129">下图提供一个基于时间的维护计划计算的图形表示。</span><span class="sxs-lookup"><span data-stu-id="537b6-129">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![图 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="537b6-131">有关基于计数器的维护计划：下图中显示了两个不同的计数器登记周期。</span><span class="sxs-lookup"><span data-stu-id="537b6-131">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="537b6-132">它们基于为资产“V0001”设置的维护计划，该资产（一辆汽车）应该每月行驶大约 2,000 公里。</span><span class="sxs-lookup"><span data-stu-id="537b6-132">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="537b6-133">在第一个示例中，每月不会达到预计的 2,000 公里。</span><span class="sxs-lookup"><span data-stu-id="537b6-133">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="537b6-134">按照基于计数器的维护计划，阈值为 2,000 公里，这表示当您运行维护计划安排时，只要达到 2,000 公里这一阈值，都应该创建一个维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-134">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="537b6-135">示例 1 中有 4 个登记行，但是 2,000 公里这一阈值仅达到了一次。</span><span class="sxs-lookup"><span data-stu-id="537b6-135">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="537b6-136">这表示在运行该资产的安排维护计划 3 个月期间之类时，将创建一个维护安排行。</span><span class="sxs-lookup"><span data-stu-id="537b6-136">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="537b6-137">在下一个图中，每月登记 2,000 公里或更多。</span><span class="sxs-lookup"><span data-stu-id="537b6-137">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="537b6-138">因此，如果为此资产安排 3 个月期间的维护计划，将创建三个维护行。</span><span class="sxs-lookup"><span data-stu-id="537b6-138">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="537b6-139">此处介绍的示例显示，为一个资产创建的所有计数器登记显示了用于描述该资产磨损情况的趋势。</span><span class="sxs-lookup"><span data-stu-id="537b6-139">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="537b6-140">该趋势在安排维护计划时用作计算基础。</span><span class="sxs-lookup"><span data-stu-id="537b6-140">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![图 3](media/11-preventive-maintenance.png)

![图 4](media/12-preventive-maintenance.png)
