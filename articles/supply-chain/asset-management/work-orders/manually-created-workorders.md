---
title: 手动创建的工作订单
description: 本主题介绍如何在资产管理中手动创建工作订单。
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875524"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="bdae6-103">手动创建的工作订单</span><span class="sxs-lookup"><span data-stu-id="bdae6-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="bdae6-104">可以通过两种途径手动创建工作订单：</span><span class="sxs-lookup"><span data-stu-id="bdae6-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="bdae6-105">在**所有工作订单**或**有效工作订单**中</span><span class="sxs-lookup"><span data-stu-id="bdae6-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="bdae6-106">在**所有维护请求**、**有效维护请求**或**我的功能位置维护请求**中</span><span class="sxs-lookup"><span data-stu-id="bdae6-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="bdae6-107">创建工作订单</span><span class="sxs-lookup"><span data-stu-id="bdae6-107">Create work order</span></span>

1. <span data-ttu-id="bdae6-108">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bdae6-109">单击**新建**按钮。</span><span class="sxs-lookup"><span data-stu-id="bdae6-109">Click the **New** button.</span></span>

3. <span data-ttu-id="bdae6-110">在**创建工作订单**下拉菜单中，选择一种工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="bdae6-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="bdae6-111">如果需要，选择一个描述。</span><span class="sxs-lookup"><span data-stu-id="bdae6-111">If required, select a description.</span></span>

5. <span data-ttu-id="bdae6-112">为工作订单和维护作业类型选择资产。</span><span class="sxs-lookup"><span data-stu-id="bdae6-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="bdae6-113">选择资产时，有三个选项卡可用：**我的资产**选项卡中包含与可能将分配给您（即已登录系统的工人）的功能位置（在[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)）关联的资产。</span><span class="sxs-lookup"><span data-stu-id="bdae6-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="bdae6-114">如果未在[维护工人和工人组](../setup-for-objects/workers-and-worker-groups.md)中为工人设置任何功能位置，则不显示**我的资产**选项卡。</span><span class="sxs-lookup"><span data-stu-id="bdae6-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="bdae6-115">**有效资产**选项卡中包含资产生命周期状态为“有效”的所有资产的列表。</span><span class="sxs-lookup"><span data-stu-id="bdae6-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="bdae6-116">**资产视图**选项卡显示功能位置及其中安装的资产的树视图。</span><span class="sxs-lookup"><span data-stu-id="bdae6-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="bdae6-117">如果需要，请选择**维护作业类型变型**和**工种**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="bdae6-118">如果需要，可以在**服务级别**字段中更改工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="bdae6-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="bdae6-119">在相关字段中选择预计开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="bdae6-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="bdae6-120">单击**确定**以创建新的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="bdae6-121">如果需要，在**所有工作订单**中编辑工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="bdae6-122">在**所有工作订单**中，可以在详细信息视图中向工作订单添加多个资产，方法是在**工作订单维护作业**快速选项卡上添加行。</span><span class="sxs-lookup"><span data-stu-id="bdae6-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="bdae6-123">对于资产，您只能选择对为该资产选择的资产类型定义的维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="bdae6-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="bdae6-124">如果资产服务级别或资产关键性在用于工作订单之后被更改（请参阅[资产服务级别](../setup-for-objects/object-priorities.md)和[资产关键性](../setup-for-objects/object-criticalities.md)），不会在工作订单中相应更新该服务级别或关键性。</span><span class="sxs-lookup"><span data-stu-id="bdae6-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="bdae6-125">只要在工作订单中添加或删除工作订单行，都将重新计算工作订单的关键性。</span><span class="sxs-lookup"><span data-stu-id="bdae6-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="bdae6-126">可在**所有工作订单**详细信息视图 > **标题**视图 > **计划**快速选项卡上的**负责组**或**负责人**字段中选择负责维护工人组或负责维护工人。</span><span class="sxs-lookup"><span data-stu-id="bdae6-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="bdae6-127">只要工作订单有效（例如，工作订单生命周期状态改变时），都可以更改这些设置。</span><span class="sxs-lookup"><span data-stu-id="bdae6-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="bdae6-128">创建工作订单期间进行的自动选择基于**负责的维护工人**中的设置。</span><span class="sxs-lookup"><span data-stu-id="bdae6-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="bdae6-129">如果在创建工作订单之后添加或删除工作订单作业，并且更新该工作订单时**负责组**字段和**负责人**字段为空，资产管理将在设置窗体中搜索负责维护工人组或负责维护工人的可能匹配项。</span><span class="sxs-lookup"><span data-stu-id="bdae6-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="bdae6-130">如果更新工作订单时已经填写了**负责组**字段或**负责人**字段，则不进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="bdae6-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="bdae6-131">在**维护状态**中，可创建计算以获取与传入的工作订单和已完成工作订单有关的工作负载的概览。</span><span class="sxs-lookup"><span data-stu-id="bdae6-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="bdae6-132">可使用**行详细信息**快速选项卡上的**维度**和**经度** 字段添加为工作订单作业选择的资产的地理坐标。</span><span class="sxs-lookup"><span data-stu-id="bdae6-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="bdae6-133">创建相关工作订单</span><span class="sxs-lookup"><span data-stu-id="bdae6-133">Create related work order</span></span>

<span data-ttu-id="bdae6-134">可在要使用主工作订单和次级工作订单之类情况下创建与现有工作订单关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="bdae6-135">新工作订单基于现有工作订单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="bdae6-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="bdae6-136">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bdae6-137">选择要为其创建关联的工作订单的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="bdae6-138">单击**关联的工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="bdae6-139">在**创建关联的工作订单**下拉对话框的**工作订单作业**字段中，选择要为其创建关联的工作订单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="bdae6-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="bdae6-140">在**维护作业类型**字段中选择维护作业类型，并且如果需要，在**维护作业类型变型**和**工种**字段中选择关联的维护作业类型变型和工种。</span><span class="sxs-lookup"><span data-stu-id="bdae6-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="bdae6-141">如果这是您创建的第一个关联的工作订单，请单击**新工作订单**单选按钮。</span><span class="sxs-lookup"><span data-stu-id="bdae6-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="bdae6-142">在相关字段中选择**工作订单类型**和**描述**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="bdae6-143">如果需要，在**服务级别**字段中更改工作订单服务级别。</span><span class="sxs-lookup"><span data-stu-id="bdae6-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="bdae6-144">在相关字段中插入预计开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="bdae6-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="bdae6-145">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-145">Click **OK**.</span></span> <span data-ttu-id="bdae6-146">将在**所有工作订单**列表中显示新的关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="bdae6-147">如果为已经有关联的工作订单的工作订单创建关联的工作订单，可以向现有关联的工作订单添加工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="bdae6-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="bdae6-148">方法是单击步骤 6 中的**添加到关联的工作订单**单选按钮。</span><span class="sxs-lookup"><span data-stu-id="bdae6-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="bdae6-149">然后选择要向其添加新工作订单作业的关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="bdae6-150">根据需要编辑**服务级别**、**预计开始日期**和**预计结束日期**字段，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="bdae6-151">将把工作订单作业添加到现有关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-151">The work order job is added to the existing related work order.</span></span>


![图 1](media/03-work-orders.png)

<span data-ttu-id="bdae6-153">**注意：** 如果已经在**资产管理参数** > **工作订单**链接 > **关联的工作订单掩码**字段中设置了关联的工作订单掩码，将按照掩码设置创建工作订单 ID。</span><span class="sxs-lookup"><span data-stu-id="bdae6-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="bdae6-154">如果未设置关联的工作订单掩码，将把下一个可用工作订单 ID 用于关联的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="bdae6-155">复制工作订单</span><span class="sxs-lookup"><span data-stu-id="bdae6-155">Copy work order</span></span>

<span data-ttu-id="bdae6-156">可以基于现有工作订单快速创建新的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="bdae6-157">这种工作订单处理方法与基于维护计划创建工作订单不同。</span><span class="sxs-lookup"><span data-stu-id="bdae6-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="bdae6-158">这在有一个工作订单中包含大量工作订单作业，这些工作订单作业具有不同资产的应该定期完成的各种作业之类情况下非常有用。</span><span class="sxs-lookup"><span data-stu-id="bdae6-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="bdae6-159">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bdae6-160">选择要复制其内容的工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="bdae6-161">单击**复制工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-161">Click **Copy work order**.</span></span> <span data-ttu-id="bdae6-162">将显示所选工作订单的工作订单设置。</span><span class="sxs-lookup"><span data-stu-id="bdae6-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="bdae6-163">如果需要，可以编辑某些字段。</span><span class="sxs-lookup"><span data-stu-id="bdae6-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="bdae6-164">单击**确定**以创建新工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="bdae6-165">如果需要，在**所有工作订单**中编辑工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="bdae6-166">创建新工作订单时，将直接从现有工作订单复制一些信息。</span><span class="sxs-lookup"><span data-stu-id="bdae6-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="bdae6-167">不复制与预测、工具、维护清单、功能位置、地址和计划有关的信息，而是从资产管理中的当前设置初始化。</span><span class="sxs-lookup"><span data-stu-id="bdae6-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="bdae6-168">这意味着，如果在创建第一个工作订单之后到创建第一个工作订单的副本之前对这些数据进行了更改，则创建的新工作订单中将包含这些更改。</span><span class="sxs-lookup"><span data-stu-id="bdae6-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="bdae6-169">例如，对预测或更新后的维护清单的更改。</span><span class="sxs-lookup"><span data-stu-id="bdae6-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![图 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="bdae6-171">基于维护请求创建工作订单</span><span class="sxs-lookup"><span data-stu-id="bdae6-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="bdae6-172">单击**资产管理** > **常用** > **维护请求** > **所有维护请求**或**有效维护请求**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="bdae6-173">选择要为其创建工作订单的维护请求，然后单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="bdae6-174">在**所有请求**中，单击**工作订单**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="bdae6-175">填写**工作订单**下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="bdae6-176">如果已经在维护请求中选择了维护作业类型，如果需要，可在创建工作订单时选择其他维护作业类型。</span><span class="sxs-lookup"><span data-stu-id="bdae6-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="bdae6-177">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdae6-177">Click **OK**.</span></span> <span data-ttu-id="bdae6-178">将显示一条消息来通知您，说明已创建了工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="bdae6-179">如果要查看哪些工作订单与维护请求相连，请在**所有维护请求**或**有效维护请求**列表中选择维护请求，然后单击**工作订单**按钮。</span><span class="sxs-lookup"><span data-stu-id="bdae6-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![图 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="bdae6-181">也可以通过计划维护计划作业，或通过为资产设置“自动创建”维护计划或维护阶段，自动创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="bdae6-182">将使用在维护请求中选择的维护作业类型，基于**维护安排**中的维护请求创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="bdae6-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

