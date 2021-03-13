---
title: 维护停机时间活动
description: 此主题介绍如何维护停机时间用于获取在特定期间对特定资产执行维护作业所需产能的概览。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 986b2ae4cf7f7819caaf35e009fd4735f35e6928
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017936"
---
# <a name="maintenance-downtime-activities"></a><span data-ttu-id="48c6c-103">维护停机时间活动</span><span class="sxs-lookup"><span data-stu-id="48c6c-103">Maintenance downtime activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48c6c-104">维护停机时间用于获取在特定期间对特定资产执行维护作业所需产能的概览。</span><span class="sxs-lookup"><span data-stu-id="48c6c-104">Maintenance downtime is used to get an overview of the capacity required to carry out maintenance jobs on specific assets during a specific period.</span></span> <span data-ttu-id="48c6c-105">例如，可为生产地点 02 的生产大厅 29-A 中的产品线 10 创建维护停机时间登记。</span><span class="sxs-lookup"><span data-stu-id="48c6c-105">For example, you can create a maintenance downtime registration for Production line 10 in Production Hall 29-A on production site 02.</span></span> <span data-ttu-id="48c6c-106">维护停机时间登记有开始时间和结束时间，用于指示与维护停止有关的资产不可用于生产。</span><span class="sxs-lookup"><span data-stu-id="48c6c-106">The maintenance downtime registration has a start and end time indicating the period in which the assets related to the maintenance stop are not available for production.</span></span>

<span data-ttu-id="48c6c-107">**维护停机时间活动** 是维护安排行和指定期间内对关联资产执行的工作订单维护作业的概览。</span><span class="sxs-lookup"><span data-stu-id="48c6c-107">**Maintenance downtime activities** is an overview of maintenance schedule lines and work order maintenance jobs on related assets during a specified period.</span></span> <span data-ttu-id="48c6c-108">与工作订单维护作业有关的所有行的预计开始日期均在维护停止期间内。</span><span class="sxs-lookup"><span data-stu-id="48c6c-108">The lines related to work order maintenance jobs all have an expected start date within the maintenance stop period.</span></span> <span data-ttu-id="48c6c-109">可提取有用信息，并对计划的维护作业进行调整：</span><span class="sxs-lookup"><span data-stu-id="48c6c-109">You can extract useful information and make adjustments to planned maintenance jobs:</span></span>

- <span data-ttu-id="48c6c-110">获取生产设备（资产）的所需关机期间的概览。</span><span class="sxs-lookup"><span data-stu-id="48c6c-110">Get an overview of required shut-down periods of production equipment (assets).</span></span>  
- <span data-ttu-id="48c6c-111">获取计划的维护（工时）的概览，这些维护按能力（负责的维护工人组或维护工人）分组，例如，电工、金属工匠或执行计划的维护作业所需其他维护工作组的产能负荷。</span><span class="sxs-lookup"><span data-stu-id="48c6c-111">Get an overview of planned maintenance (hours), grouped by competencies (responsible maintenance worker groups or maintenance workers), for example capacity load on electricians, smiths, or other maintenance work groups required to do the planned maintenance jobs.</span></span>  
- <span data-ttu-id="48c6c-112">对与资产关联的维护安排行或工作订单维护作业进行调整，例如，更改行中的预计开始时间和结束时间，或选择其他维护工人以优化维护工人和维护工人组的工作流。</span><span class="sxs-lookup"><span data-stu-id="48c6c-112">Make adjustments to maintenance schedule lines or work order maintenance jobs related to the assets, for example, change expected start and end times on a line, or select other maintenance workers to optimize the workflow for maintenance workers and maintenance worker groups.</span></span>

<span data-ttu-id="48c6c-113">对维护停机时间登记选择了资产之后，维护停机时间登记中将包含与有效工作订单有关的所有已打开维护安排行和工作订单维护作业。</span><span class="sxs-lookup"><span data-stu-id="48c6c-113">When assets have been selected on a maintenance downtime registration, all open maintenance schedule lines and work order maintenance jobs relating to active work orders are included in the maintenance downtime registration.</span></span>

## <a name="maintenance-downtime-activities"></a><span data-ttu-id="48c6c-114">维护停机时间活动</span><span class="sxs-lookup"><span data-stu-id="48c6c-114">Maintenance downtime activities</span></span>

<span data-ttu-id="48c6c-115">单击 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** 以打开所有维护停机时间活动的列表和查看与这些活动有关的部分信息。</span><span class="sxs-lookup"><span data-stu-id="48c6c-115">Click **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** to open a list of all maintenance downtime activities and see some of the information related to the activities.</span></span> <span data-ttu-id="48c6c-116">单击 **维护停机时间活动** 列中的一个链接以打开详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="48c6c-116">Click on a link in the **Maintenance downtime activities** column to open the details view.</span></span> <span data-ttu-id="48c6c-117">下图显示 **维护停机时间活动** 列表的示例。</span><span class="sxs-lookup"><span data-stu-id="48c6c-117">The illustration below shows an example of the **Maintenance downtime activities** list.</span></span>

![图 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a><span data-ttu-id="48c6c-119">创建维护停机时间活动</span><span class="sxs-lookup"><span data-stu-id="48c6c-119">Create a maintenance downtime activity</span></span>

1. <span data-ttu-id="48c6c-120">单击 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** 或 **有效的维护停机时间活动**。</span><span class="sxs-lookup"><span data-stu-id="48c6c-120">Click **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** or **Active maintenance downtime activities**.</span></span>

2. <span data-ttu-id="48c6c-121">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="48c6c-121">Click **New**.</span></span>

3. <span data-ttu-id="48c6c-122">在 **维护停机时间活动** 字段中插入 ID，在 **名称** 字段中插入名称。</span><span class="sxs-lookup"><span data-stu-id="48c6c-122">Insert an ID in the **Maintenance downtime activities** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="48c6c-123">在 **开始日期/时间** 和 **结束日期/时间** 字段中插入维护停止的期间。</span><span class="sxs-lookup"><span data-stu-id="48c6c-123">Insert the period for the maintenance stop in the **Start date/time** and **End date/time** fields.</span></span>

5. <span data-ttu-id="48c6c-124">在 **维护停机时间活动资产** 快速选项卡上，单击 **添加行** 以向维护停机时间活动添加资产，一次一个。</span><span class="sxs-lookup"><span data-stu-id="48c6c-124">On the **Maintenance downtime activities assets** FastTab> click **Add line** to add assets, one at a time, to the maintenance downtime activity.</span></span>

6. <span data-ttu-id="48c6c-125">创建所有资产之后，单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="48c6c-125">Click **Save** when all assets have been added.</span></span> <span data-ttu-id="48c6c-126">下图显示具有关联资产和维护作业的维护停机时间活动的示例。</span><span class="sxs-lookup"><span data-stu-id="48c6c-126">The illustration below shows an example of a maintenance downtime activity with related assets and maintenance jobs.</span></span>

7. <span data-ttu-id="48c6c-127">将在 **生成的工作订单维护作业** 和 **维护安排行** 快速选项卡上显示与所选资产关联的工作订单维护作业和打开的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-127">The work order maintenance jobs and open maintenance schedule lines related to the selected assets are shown on the **Resulting work order maintenance jobs** and **Maintenance schedule lines** FastTabs.</span></span> <span data-ttu-id="48c6c-128">在 **常规** 快速选项卡 > **工人** 组 > **维护预测工时数** 字段和 **常规** 快速选项卡 > **维护安排** 组 > **维护预测工时数** 字段中，可以查看为工作订单维护作业和维护安排行预测的总工时数。</span><span class="sxs-lookup"><span data-stu-id="48c6c-128">On the **General** FastTab > **Work orders** group > **Maintenance forecast hours** field and **General** FastTab > **Maintenance schedule** group > **Maintenance forecast hours** field , you see the total number of hours forecasted for work order maintenance jobs and maintenance schedule lines.</span></span>

<span data-ttu-id="48c6c-129">下图显示 **维护停机时间活动** 详细信息视图的示例。</span><span class="sxs-lookup"><span data-stu-id="48c6c-129">The illustration below shows an example of the **Maintenance downtime activities** details view.</span></span>

![图 2](media/20-preventive-maintenance.png)

>[!NOTE]
><span data-ttu-id="48c6c-131">如果在创建维护停机时间活动之后创建了新的工作订单或维护安排行，将自动更新与所选资产关联的工作订单维护作业和维护安排行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-131">The work order maintenance jobs and maintenance schedule lines related to the selected assets are automatically updated if new work orders or maintenance schedule lines are created after you created the maintenance downtime activity.</span></span> <span data-ttu-id="48c6c-132">例如，如果在创建维护停机时间活动的两天后为关联资产安排维护安排或维护阶段，将自动向维护停机时间活动添加新的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-132">For example, if you schedule maintenance plans or maintenance rounds on the related assets two days after the maintenance downtime activity was created, new maintenance schedule lines are automatically added to the maintenance downtime activity.</span></span>

8. <span data-ttu-id="48c6c-133">在 **所有维护停机时间活动** > **维护停机时间活动** 中 > 在列表中选择一个维护停机时间活动，然后单击 **产能负荷** 以打开 **计算产能负荷** 对话框。</span><span class="sxs-lookup"><span data-stu-id="48c6c-133">In **All maintenance downtime activities** > **Maintenance downtime activities** > select a maintenance downtime activity in the list and click **Capacity load** to open the **Calculate capacity load** dialog.</span></span> <span data-ttu-id="48c6c-134">此对话框用于获取日期、资产、资产类型和维护作业类型之类的产能负荷的概览。</span><span class="sxs-lookup"><span data-stu-id="48c6c-134">Use this dialog to get an overview of capacity load on, for example, dates, assets, asset types, and maintenance job types.</span></span> <span data-ttu-id="48c6c-135">请注意，此对话框中显示的日期是 **维护停机时间活动** 中选择的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="48c6c-135">Note that the dates shown in the dialog are the start and end dates selected in **Maintenance downtime activities**.</span></span> <span data-ttu-id="48c6c-136">此项计算中包含与维护停机时间活动关联的资产。</span><span class="sxs-lookup"><span data-stu-id="48c6c-136">This calculation includes the assets related to the maintenance downtime activity.</span></span>

9. <span data-ttu-id="48c6c-137">如果需要，在 **计算产能负荷** 对话框中编辑开始时间和结束时间，并且选择是否要在计算中包含工作订单和维护安排。</span><span class="sxs-lookup"><span data-stu-id="48c6c-137">In the **Calculate capacity load** dialog, edit start and end times if required, and select if you want to include work orders and maintenance schedules in the calculation.</span></span> <span data-ttu-id="48c6c-138">可使用 **级别** 字段指示要与功能位置有关的产能负荷计算的详细程度。</span><span class="sxs-lookup"><span data-stu-id="48c6c-138">You can use the **Level** field to indicate how detailed you want the capacity load calculation to be regarding functional locations.</span></span> <span data-ttu-id="48c6c-139">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产（这是对维护停机时间活动选择的），因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="48c6c-139">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location, which are selected on the maintenance downtime activity, will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="48c6c-140">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有产能负荷行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-140">If you insert the number "0" in the **Level** field, you will see a detailed result showing all capacity load lines on all the functional location levels to which they are related.</span></span>

10. <span data-ttu-id="48c6c-141">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="48c6c-141">Click **OK** to start the calculation.</span></span> <span data-ttu-id="48c6c-142">将在 **产能负荷** 概览中显示总工时数。</span><span class="sxs-lookup"><span data-stu-id="48c6c-142">The total number of hours is shown in the **Capacity load** overview.</span></span> <span data-ttu-id="48c6c-143">在 **产能负荷** 选项卡 > **分组依据** 操作窗格组中，单击相关按钮获取更详细的预测工时分配概览。</span><span class="sxs-lookup"><span data-stu-id="48c6c-143">On the **Capacity load** tab > the **Group by...** Action Pane groups, click the relevant buttons to get a more detailed overview of the allocation of forecasted hours.</span></span> <span data-ttu-id="48c6c-144">下图显示 **产能负荷** 计算的结果。</span><span class="sxs-lookup"><span data-stu-id="48c6c-144">The illustration below shows the results of a **Capacity load** calculation.</span></span>

![图 3](media/21-preventive-maintenance.png)

11. <span data-ttu-id="48c6c-146">获取产能负荷概览之后，如果要对工作订单维护作业或维护安排行进行调整，请回到 **维护停机时间活动** 详细信息视图，然后在 **生成的工作订单维护作业** 和 **维护安排行** 快速选项卡上选择要进行调整的行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-146">After you get an overview of the capacity load, if you want to make adjustments on work order maintenance jobs or maintenance schedule lines, return to the **Maintenance downtime activities** details view and select the lines you want to adjust on the **Resulting work order maintenance jobs** and **Maintenance schedule lines** FastTabs.</span></span>

12. <span data-ttu-id="48c6c-147">单击 **调整** 按钮，然后更新所选工作订单维护作业或维护安排行的预计开始/结束日期、服务级别或负责的维护工人。</span><span class="sxs-lookup"><span data-stu-id="48c6c-147">Click the **Adjust** button and update expected start/end dates, service level, or responsible maintenance workers for the selected work order maintenance jobs or maintenance schedule lines.</span></span>

13. <span data-ttu-id="48c6c-148">进行所需调整之后，单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="48c6c-148">Click **OK** when you have made the required adjustments.</span></span> 

>[!NOTE]
><span data-ttu-id="48c6c-149">将从 **维护停机时间活动** 自动删除在进行调整之后不在维护停机时间活动期间中的工作订单维护作业和维护安排行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-149">Work order maintenance jobs and maintenance schedule lines that are not included in the maintenance downtime period after you have made adjustments are automatically removed from **Maintenance downtime activities**.</span></span>

14. <span data-ttu-id="48c6c-150">在 **所有维护停机时间活动** > **维护停机时间活动** 中 > 在列表中选择一个维护停机时间活动，然后单击 **物料预测** 以打开 **计算物料预测** 对话框。</span><span class="sxs-lookup"><span data-stu-id="48c6c-150">In **All maintenance downtime activities** > **Maintenance downtime activities** > select a maintenance downtime activity in the list and click **Item forecast** to open the **Calculate item forecast** dialog.</span></span> <span data-ttu-id="48c6c-151">此对话框用于计算物料（备件和其他必需物料）的预测，并为其分组以获取概览，例如，按日期、资产、资产类型和维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="48c6c-151">Use this dialog to calculate forecasts for items (spare parts and other required items) and group them to get an overview, for example, by date, asset, asset type, and maintenance job type.</span></span> <span data-ttu-id="48c6c-152">请注意，此对话框中显示的日期是 **维护停机时间活动** 中选择的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="48c6c-152">Note that the dates shown in the dialog are the start and end dates selected in **Maintenance downtime activities**.</span></span> <span data-ttu-id="48c6c-153">此项计算中包含与对维护停机时间活动选择的资产关联的备件和物料。</span><span class="sxs-lookup"><span data-stu-id="48c6c-153">This calculation includes spare parts and items related to the assets that are selected on the maintenance downtime activity.</span></span>

15. <span data-ttu-id="48c6c-154">如果需要，在 **计算物料预测** 对话框中编辑开始时间和结束时间，并且选择是否要在计算中包含工作订单和维护安排。</span><span class="sxs-lookup"><span data-stu-id="48c6c-154">In the **Calculate item forecast** dialog, edit start and end times if required, and select if you want to include work orders and maintenance schedules in the calculation.</span></span> <span data-ttu-id="48c6c-155">可使用 **级别** 字段指示要与功能位置有关的产能负荷计算的详细程度。</span><span class="sxs-lookup"><span data-stu-id="48c6c-155">You can use the **Level** field to indicate how detailed you want the capacity load calculation to be regarding functional locations.</span></span> <span data-ttu-id="48c6c-156">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产（这是对维护停机时间活动选择的），因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="48c6c-156">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location, which are selected on the maintenance downtime activity, will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="48c6c-157">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有产能负荷行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-157">If you insert the number "0" in the **Level** field, you will see a detailed result showing all capacity load lines on all the functional location levels to which they are related.</span></span>

16. <span data-ttu-id="48c6c-158">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="48c6c-158">Click **OK** to start the calculation.</span></span> <span data-ttu-id="48c6c-159">将在 **物料预测** 概览中显示物料预测总数。</span><span class="sxs-lookup"><span data-stu-id="48c6c-159">The total number of item forecasts is shown in the  **Item forecast** overview.</span></span> <span data-ttu-id="48c6c-160">在 **物料预测** 选项卡 > **分组依据** 操作窗格组中，单击相关按钮获取更详细的预测物料分配概览。下图显示 **物料预测** 计算的结果。</span><span class="sxs-lookup"><span data-stu-id="48c6c-160">On the **Item forecast** tab > the **Group by...** Action Pane groups, click the relevant buttons to get a more detailed overview of the allocation of forecasted items.The illustration below shows the results of an **Item forecast** calculation.</span></span>

![图 4](media/22-preventive-maintenance.png)

- <span data-ttu-id="48c6c-162">可将资产从一个维护停机时间活动复制到另一个维护停机时间活动。</span><span class="sxs-lookup"><span data-stu-id="48c6c-162">You can copy assets from one maintenance downtime activity to another.</span></span> <span data-ttu-id="48c6c-163">在 **所有维护停机时间活动** 中，选择 **复制维护停机时间活动** 按钮，在 **源维护停机时间活动** 和 **目标维护停机时间活动** 字段中进行选择，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="48c6c-163">In **All maintenance downtime activities**, select the **Copy maintenance downtime activities** button, and make your selections in the **From maintenance downtime activities** and **To maintenance downtime activities** fields, and click **OK**.</span></span>
- <span data-ttu-id="48c6c-164">在 **所有维护停机时间活动** 中，单击 **维护安排行** 按钮或 **有效工作订单** 按钮打开相关列表和查看与所选维护停机时间活动关联的行。</span><span class="sxs-lookup"><span data-stu-id="48c6c-164">In **All maintenance downtime activities**, click the **Maintenance schedule lines** button or the **Active work orders** button to open the related lists and view the lines related to the selected maintenance downtime activity.</span></span>

