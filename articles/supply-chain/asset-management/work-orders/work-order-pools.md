---
title: 工作订单池
description: 本主题介绍在资产管理中如何使用工作订单池。
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875526"
---
# <a name="work-order-pools"></a><span data-ttu-id="c81bc-103">工作订单池</span><span class="sxs-lookup"><span data-stu-id="c81bc-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c81bc-104">可使用工作订单池为具有某些共同点的工作订单分组。</span><span class="sxs-lookup"><span data-stu-id="c81bc-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="c81bc-105">例如，可以为以下对象创建工作订单池：</span><span class="sxs-lookup"><span data-stu-id="c81bc-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="c81bc-106">工作班组，如“维护班组 A”、“维护班组 B”</span><span class="sxs-lookup"><span data-stu-id="c81bc-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="c81bc-107">专业技能，如电工或管道工</span><span class="sxs-lookup"><span data-stu-id="c81bc-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="c81bc-108">物理位置</span><span class="sxs-lookup"><span data-stu-id="c81bc-108">physical locations</span></span>  

- <span data-ttu-id="c81bc-109">时间安排，如周或其他期间</span><span class="sxs-lookup"><span data-stu-id="c81bc-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="c81bc-110">如果需要，可将一个工作订单放入多个工作订单池中。</span><span class="sxs-lookup"><span data-stu-id="c81bc-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="c81bc-111">创建工作订单池</span><span class="sxs-lookup"><span data-stu-id="c81bc-111">Create work order pool</span></span>

<span data-ttu-id="c81bc-112">在**所有工作订单池**或**有效工作订单池**中，可获取您的工作订单池的概览，以及创建新池。</span><span class="sxs-lookup"><span data-stu-id="c81bc-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="c81bc-113">单击**资产管理** > **常用** > **工作订单池** > **所有工作订单池**或**有效工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="c81bc-114">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-114">Click **New**.</span></span>

3. <span data-ttu-id="c81bc-115">在**池**字段中插入工作订单池 ID，在**名称**字段中插入名称。</span><span class="sxs-lookup"><span data-stu-id="c81bc-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="c81bc-116">在**有效**切换按钮上选择“是”以指示工作订单池有效。</span><span class="sxs-lookup"><span data-stu-id="c81bc-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="c81bc-117">如果要从工作订单池自动删除工作订单，请在**删除工作订单关联**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="c81bc-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="c81bc-118">在**删除生命周期状态**字段中，选择工作订单生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="c81bc-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="c81bc-119">例如，可以设置用于完成工作订单的工作订单生命周期状态以自动删除与工作订单池的关联。</span><span class="sxs-lookup"><span data-stu-id="c81bc-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="c81bc-120">可立即开始向工作订单池添加工作订单。</span><span class="sxs-lookup"><span data-stu-id="c81bc-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="c81bc-121">在**工作订单**快速选项卡中，单击**添加行**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="c81bc-122">在**工作订单**字段中选择一个工作订单。</span><span class="sxs-lookup"><span data-stu-id="c81bc-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="c81bc-123">然后将自动更新关联的字段。</span><span class="sxs-lookup"><span data-stu-id="c81bc-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="c81bc-124">如果要添加更多工作订单，请重复步骤 7-8。</span><span class="sxs-lookup"><span data-stu-id="c81bc-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="c81bc-125">在**排序顺序**字段中，可指示是否应按照特定顺序执行工作订单。</span><span class="sxs-lookup"><span data-stu-id="c81bc-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="c81bc-126">插入数字 1、2、3，以此类推，为所选工作订单指定特定序列。</span><span class="sxs-lookup"><span data-stu-id="c81bc-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="c81bc-127">单击**工作订单**按钮可查看工作订单池中包含的所有工作订单的列表。</span><span class="sxs-lookup"><span data-stu-id="c81bc-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="c81bc-128">单击**产能负荷**按钮可打开**产能负荷**以计算和查看维护安排、未安排的工作订单和已安排的工作订单的产能负荷。</span><span class="sxs-lookup"><span data-stu-id="c81bc-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="c81bc-129">单击**物料预测**按钮可打开**物料预测**以计算和查看与维护安排、未安排的工作订单和已安排的工作订单关联的物料（备件和其他必需物料）的预测。</span><span class="sxs-lookup"><span data-stu-id="c81bc-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="c81bc-130">单击**工作订单采购申请**按钮可打开**工作订单采购申请**列表以查看与工作订单池中的工作订单关联的采购申请的列表。</span><span class="sxs-lookup"><span data-stu-id="c81bc-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="c81bc-131">单击**工作订单采购**按钮可打开**工作订单采购**列表以查看与工作订单池中的工作订单关联的采购订单的列表。</span><span class="sxs-lookup"><span data-stu-id="c81bc-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="c81bc-132">如果工作订单池不再与您的工作规划有关，请在**工作订单池**列表视图中将该池的**有效**复选框设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="c81bc-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="c81bc-133">如果要删除所有工作订单行（例如，为了创建空池，以便以后将其用于其他工作订单），请选中**删除工作订单关联**复选框。</span><span class="sxs-lookup"><span data-stu-id="c81bc-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="c81bc-134">如果要在以后使用工作订单池新建工作订单关联，请务必清除**删除工作订单关联**复选框。</span><span class="sxs-lookup"><span data-stu-id="c81bc-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![图 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="c81bc-136">向工作订单池添加工作订单</span><span class="sxs-lookup"><span data-stu-id="c81bc-136">Add work order to a work order pool</span></span>

<span data-ttu-id="c81bc-137">如上面的部分中所述，可在创建工作订单池时向其添加工作订单。</span><span class="sxs-lookup"><span data-stu-id="c81bc-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="c81bc-138">也可以从其中一个**所有工作订单**列表向工作订单池添加工作订单。</span><span class="sxs-lookup"><span data-stu-id="c81bc-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="c81bc-139">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c81bc-140">在列表中选择工作订单，然后单击**工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="c81bc-141">在**添加/删除**字段中选择“添加”。</span><span class="sxs-lookup"><span data-stu-id="c81bc-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="c81bc-142">在**池**字段中选择工作订单池。</span><span class="sxs-lookup"><span data-stu-id="c81bc-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="c81bc-143">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c81bc-143">Click **OK**.</span></span>

6. <span data-ttu-id="c81bc-144">向工作订单池添加工作订单之后，如果要按照特定序列将工作订单放到池中：打开一个工作订单池列表页，选择池，单击**编辑**，然后在**工作订单池**窗体 > **工作订单**快速选项卡 > **排序顺序**字段中调整池中包含的工作订单的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="c81bc-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="c81bc-145">如果要从工作订单池删除所选工作订单，请在步骤 3 中选择“删除”。</span><span class="sxs-lookup"><span data-stu-id="c81bc-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

