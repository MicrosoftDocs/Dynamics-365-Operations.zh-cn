---
title: 维护阶段
description: 本主题介绍资产管理中的维护阶段。
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
ms.openlocfilehash: a0ac4820d2efa37387382c2890e3ddc7dbc0878b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875522"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="c6991-103">维护阶段</span><span class="sxs-lookup"><span data-stu-id="c6991-103">Maintenance rounds</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c6991-104">在**资产管理**中，可以为各资产创建维护阶段，在这些阶段，需要定期执行相似任务。</span><span class="sxs-lookup"><span data-stu-id="c6991-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="c6991-105">例如，需要在相同间隔内对一些机器执行的润滑作业或安全检查作业。</span><span class="sxs-lookup"><span data-stu-id="c6991-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="c6991-106">第一步是创建维护阶段，其中包括需要对其执行相同形式的维护作业的资产。</span><span class="sxs-lookup"><span data-stu-id="c6991-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="c6991-107">接下来，安排维护阶段。</span><span class="sxs-lookup"><span data-stu-id="c6991-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="c6991-108">完成了维护阶段安排之后，可在**所有维护安排**和**打开维护安排行**中查看与该阶段关联的所有作业记录。</span><span class="sxs-lookup"><span data-stu-id="c6991-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="c6991-109">也可以在创建基于阶段的工作订单时，为在功能位置安装的资产的功能位置设置要完成的维护阶段。</span><span class="sxs-lookup"><span data-stu-id="c6991-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="c6991-110">有关为功能位置设置维护阶段的详细信息，请参阅[创建功能位置](../functional-locations/create-functional-locations.md)。</span><span class="sxs-lookup"><span data-stu-id="c6991-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="c6991-111">设置维护阶段</span><span class="sxs-lookup"><span data-stu-id="c6991-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="c6991-112">单击**资产管理** > **设置** > **预防性维护** > **维护阶段**。</span><span class="sxs-lookup"><span data-stu-id="c6991-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="c6991-113">单击 **新建** 以创建新的维护阶段。</span><span class="sxs-lookup"><span data-stu-id="c6991-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="c6991-114">在**维护阶段**字段中插入 ID，在**名称**字段中插入维护阶段的名称。</span><span class="sxs-lookup"><span data-stu-id="c6991-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="c6991-115">在**开始日期**字段中选择阶段的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="c6991-116">在**完成期限(天)** 和**完成期限(小时)** 字段中，可输入以天或小时为单位的预计结束日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="c6991-117">将计算相对开始日期（这是创建维护安排行时计算出的）的预计结束日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="c6991-118">例如，可以在**完成期限(天)** 字段中插入“7”，指示关联作业将在开始日期之后一周内完成。</span><span class="sxs-lookup"><span data-stu-id="c6991-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="c6991-119">如果应该基于从该维护阶段创建的维护安排行自动创建工作订单，请在**自动创建**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c6991-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="c6991-120">在**工作订单类型**字段中，选择要为基于该维护阶段创建的工作订单使用的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="c6991-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="c6991-121">在**服务级别**字段中，选择要为基于该维护阶段创建的工作订单使用的工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="c6991-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="c6991-122">在**资产行**快速选项卡上，单击**添加**向维护阶段添加资产。</span><span class="sxs-lookup"><span data-stu-id="c6991-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="c6991-123">将在**行号**字段中自动插入行号，以指示维护阶段中的资产序列。</span><span class="sxs-lookup"><span data-stu-id="c6991-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="c6991-124">在**资产**字段中选择资产。</span><span class="sxs-lookup"><span data-stu-id="c6991-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="c6991-125">在**维护作业类型**字段中，选择资产的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="c6991-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="c6991-126">如果需要，选择与维护作业类型关联的**维护作业类型变型**和**工种**。</span><span class="sxs-lookup"><span data-stu-id="c6991-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="c6991-127">在**期间类型**字段中选择重复发生频率（天、周等）。</span><span class="sxs-lookup"><span data-stu-id="c6991-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="c6991-128">在**期间频率**字段中插入维护阶段的发生次数。</span><span class="sxs-lookup"><span data-stu-id="c6991-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="c6991-129">示例：如果已在**期间类型**字段中选择“天”，并且在此字段中插入数字“7”，将在预防性维护安排期间每周创建一次新的维护阶段行。</span><span class="sxs-lookup"><span data-stu-id="c6991-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="c6991-130">在**开始日期**字段中选择维护阶段中要包括的资产的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="c6991-131">此日期可以不是为维护阶段设置的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="c6991-132">重复步骤 9-16 向维护阶段添加更多资产。</span><span class="sxs-lookup"><span data-stu-id="c6991-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="c6991-133">在**功能位置行**快速选项卡上，单击**添加**向维护阶段添加功能位置。</span><span class="sxs-lookup"><span data-stu-id="c6991-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="c6991-134">请参阅上面的关联字段描述。</span><span class="sxs-lookup"><span data-stu-id="c6991-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="c6991-135">同样的字段可用于创建资产行，不过如果需要，也可以为功能位置选择**制造商**和**型号**。</span><span class="sxs-lookup"><span data-stu-id="c6991-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="c6991-136">如果仅为行选择功能位置，不在**资产类型**、**制造商**、**型号**、**维护作业类型**、**维护作业类型变型**和**工种**中进行选择，则维护阶段中将包括在进行维护安排时与该功能位置关联的所有资产。</span><span class="sxs-lookup"><span data-stu-id="c6991-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="c6991-137">在**池**快速选项卡上，单击**添加**以选择维护阶段中要包括的工作订单池。</span><span class="sxs-lookup"><span data-stu-id="c6991-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="c6991-138">可将多个工作订单池与一个维护阶段关联。</span><span class="sxs-lookup"><span data-stu-id="c6991-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="c6991-139">保存设置。</span><span class="sxs-lookup"><span data-stu-id="c6991-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="c6991-140">**标题**快速选项卡上**详细信息**组中的**资产**和**行**字段显示与所选维护阶段关联的资产和行的总数。</span><span class="sxs-lookup"><span data-stu-id="c6991-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

![图 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="c6991-142">安排维护阶段</span><span class="sxs-lookup"><span data-stu-id="c6991-142">Schedule maintenance rounds</span></span>

<span data-ttu-id="c6991-143">设置维护阶段之后，可运行安排作业来安排与该维护阶段关联的所有作业。</span><span class="sxs-lookup"><span data-stu-id="c6991-143">When you have set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="c6991-144">单击**资产管理** > **定期** > **预防性维护** > **安排维护阶段**，或**资产管理** > **常用** > **维护安排** > **所有维护安排**或**打开维护安排行**或**打开维护安排池** > 选择列表中的维护安排行 > **维护阶段**按钮。</span><span class="sxs-lookup"><span data-stu-id="c6991-144">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="c6991-145">在**期间**字段中，选择要用于安排作业的期间类型。</span><span class="sxs-lookup"><span data-stu-id="c6991-145">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="c6991-146">在**期间频率**字段中插入安排作业中要包括的期间的数量。</span><span class="sxs-lookup"><span data-stu-id="c6991-146">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="c6991-147">该安排的开始日期为当前日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-147">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="c6991-148">如果应该基于维护阶段自动创建工作订单，请在**自动创建**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c6991-148">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="c6991-149">如果此切换按钮设置为“是”，并且**维护阶段**窗体中维护阶段的**自动创建**切换按钮也设置为“是”，则基于维护阶段行创建工作订单，并创建状态为“已创建工作订单”的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="c6991-149">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="c6991-150">如果此下拉菜单中或**维护阶段**中只有一个**自动创建**切换按钮设置为“是”，则仅创建状态为“已创建”的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="c6991-150">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="c6991-151">在此情况下，将不创建任何工作订单。</span><span class="sxs-lookup"><span data-stu-id="c6991-151">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="c6991-152">如果需要，可以为安排作业选择特定阶段或其他开始日期。</span><span class="sxs-lookup"><span data-stu-id="c6991-152">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="c6991-153">单击**筛选**，然后添加要包括的阶段。</span><span class="sxs-lookup"><span data-stu-id="c6991-153">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="c6991-154">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c6991-154">Click **OK**.</span></span>

7. <span data-ttu-id="c6991-155">现在可以在**资产管理** > **常用** > **维护安排** > **所有维护安排**或**打开维护安排行**中查看维护阶段作业。</span><span class="sxs-lookup"><span data-stu-id="c6991-155">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="c6991-156">如果已将安排的阶段与工作订单池关联，还可以在**打开维护安排池**中查看维护安排行。</span><span class="sxs-lookup"><span data-stu-id="c6991-156">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c6991-157">将基于阶段创建引用类型为“维护阶段”的维护安排行。</span><span class="sxs-lookup"><span data-stu-id="c6991-157">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

![图 2](media/14-preventive-maintenance.png)

![图 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="c6991-160">为供应商保修涵盖的资产手动创建工作订单时，将显示一个对话框，用于提醒用户注意保修。</span><span class="sxs-lookup"><span data-stu-id="c6991-160">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="c6991-161">然后可以取消创建此工作订单。</span><span class="sxs-lookup"><span data-stu-id="c6991-161">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="c6991-162">将对自动创建的工作订单忽略检查保修关联。</span><span class="sxs-lookup"><span data-stu-id="c6991-162">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="c6991-163">可以在**在后台运行**快速选项卡上设置批处理作业，以便安排定期执行的阶段。</span><span class="sxs-lookup"><span data-stu-id="c6991-163">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="c6991-164">如果一个阶段包含在多个工作订单池中（请参阅[工作订单池](../work-orders/work-order-pools.md)），将为**打开维护安排池**中的每个池显示一条记录。</span><span class="sxs-lookup"><span data-stu-id="c6991-164">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c6991-165">这是为了优化工作订单池的筛选选项。</span><span class="sxs-lookup"><span data-stu-id="c6991-165">This is done to optimize the filtering options for work order pools.</span></span>

