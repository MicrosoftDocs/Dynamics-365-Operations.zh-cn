---
title: 工作订单池
description: 本主题介绍在资产管理中如何使用工作订单池。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626354"
---
# <a name="work-order-pools"></a><span data-ttu-id="7b252-103">工作订单池</span><span class="sxs-lookup"><span data-stu-id="7b252-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="7b252-104">可使用工作订单池为具有某些共同点的工作订单分组。</span><span class="sxs-lookup"><span data-stu-id="7b252-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="7b252-105">以下是您可以为其创建工作订单池的内容的一些示例：</span><span class="sxs-lookup"><span data-stu-id="7b252-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="7b252-106">工作班组，如“维护班组 A”或“维护班组 B”</span><span class="sxs-lookup"><span data-stu-id="7b252-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="7b252-107">专业技能，如电工或管道工</span><span class="sxs-lookup"><span data-stu-id="7b252-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="7b252-108">物理位置</span><span class="sxs-lookup"><span data-stu-id="7b252-108">Physical locations</span></span>  

- <span data-ttu-id="7b252-109">时间安排，如周或其他期间</span><span class="sxs-lookup"><span data-stu-id="7b252-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="7b252-110">根据需要，您可以将一个工作订单放入多个工作订单池中。</span><span class="sxs-lookup"><span data-stu-id="7b252-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="7b252-111">创建工作订单池</span><span class="sxs-lookup"><span data-stu-id="7b252-111">Create a work order pool</span></span>

<span data-ttu-id="7b252-112">在**所有工作订单池**或**有效工作订单池**列表页上，可获取您的工作订单池的概览，以及创建新池。</span><span class="sxs-lookup"><span data-stu-id="7b252-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="7b252-113">选择**资产管理** > **常用** > **工作订单池** > **所有工作订单池**或**有效工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="7b252-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="7b252-114">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="7b252-114">Select **New**.</span></span>

3. <span data-ttu-id="7b252-115">在**池**字段中，输入工作订单池的 ID。</span><span class="sxs-lookup"><span data-stu-id="7b252-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="7b252-116">在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="7b252-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="7b252-117">将**有效**选项设置为**是**以指示工作订单池有效。</span><span class="sxs-lookup"><span data-stu-id="7b252-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="7b252-118">如果应从工作订单池自动删除工作订单，请将**删除工作订单关联**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7b252-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="7b252-119">在**删除生命周期状态**字段中，选择工作订单生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="7b252-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="7b252-120">例如，可以设置用于完成工作订单的工作订单生命周期状态以自动删除与工作订单池的关联。</span><span class="sxs-lookup"><span data-stu-id="7b252-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="7b252-121">可立即开始向工作订单池添加工作订单。</span><span class="sxs-lookup"><span data-stu-id="7b252-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="7b252-122">在**工作订单**快速选项卡中，选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="7b252-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="7b252-123">在**工作订单**字段中选择一个工作订单。</span><span class="sxs-lookup"><span data-stu-id="7b252-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="7b252-124">然后将自动更新关联的字段。</span><span class="sxs-lookup"><span data-stu-id="7b252-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="7b252-125">重复执行第 8 步到第 9 步，以添加更多工作订单。</span><span class="sxs-lookup"><span data-stu-id="7b252-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="7b252-126">如果您添加的工作订单应按特定顺序完成，在**排序顺序**字段中，您可以输入数字 **1**、**2**、**3**，依此类推，来指定该顺序。</span><span class="sxs-lookup"><span data-stu-id="7b252-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="7b252-127">要查看工作订单池中包含的所有工作订单的列表，请在操作窗格上**工作订单池**选项卡上的**查看相关的工作订单池**组中，选择**工作订单**打开**所有工作订单**列表页。</span><span class="sxs-lookup"><span data-stu-id="7b252-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="7b252-128">要计算和查看维护安排、未计划的工作订单和计划的工作订单的产能负荷，请在操作窗格的**工作订单池**选项卡上的**查看相关的工作订单池**组中，选择**产能负荷**以打开**计算产能负荷**对话框。</span><span class="sxs-lookup"><span data-stu-id="7b252-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="7b252-129">要计算和查看与维护安排、未计划的工作订单和计划的工作订单有关的物料（备件和其他必需物料）的预测，请在操作窗格的**工作订单池**选项卡上的**查看相关的工作订单池**组中，选择**物料预测**以打开**计算物料预测**对话框。</span><span class="sxs-lookup"><span data-stu-id="7b252-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="7b252-130">要查看与工作订单池中的工作订单相关的采购申请的列表，请在操作窗格上**工作订单池**选项卡上的**采购**组中，选择**工作订单采购申请**打开**工作订单采购申请**列表页。</span><span class="sxs-lookup"><span data-stu-id="7b252-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="7b252-131">要查看与工作订单池中的工作订单相关的采购订单的列表，请在操作窗格上**工作订单池**选项卡上的**采购**组中，选择**工作订单采购**打开**工作订单采购**列表页。</span><span class="sxs-lookup"><span data-stu-id="7b252-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="7b252-132">如果工作订单池不再与您的工作规划有关，请在**工作订单池**页面的列表视图中将该池的**有效**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="7b252-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="7b252-133">要删除所有工作订单行，请将**删除工作订单关联**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7b252-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="7b252-134">例如，如果您要创建一个空池，以后可以将其用于其他工作订单，则此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="7b252-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="7b252-135">当您准备在以后使用工作订单池创建新的工作订单关联时，请记住将**删除工作订单关联**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="7b252-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="7b252-136">下图显示**工作订单池**列表页的示例。</span><span class="sxs-lookup"><span data-stu-id="7b252-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![图 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="7b252-138">向工作订单池添加工作订单</span><span class="sxs-lookup"><span data-stu-id="7b252-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="7b252-139">如前一节中所述，可在创建工作订单池时向其添加工作订单。</span><span class="sxs-lookup"><span data-stu-id="7b252-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="7b252-140">您还可以在**所有工作订单**或**有效工作订单**列表页上将工作订单添加到工作订单池中。</span><span class="sxs-lookup"><span data-stu-id="7b252-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="7b252-141">选择工作订单，然后在“操作窗格”上的**工作订单**选项卡上，在**维护**组中，选择**工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="7b252-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="7b252-142">在列表中选择工作订单，然后单击**工作订单池**。</span><span class="sxs-lookup"><span data-stu-id="7b252-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="7b252-143">在**维护工作订单池**对话框中的**添加/删除**字段中，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="7b252-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="7b252-144">在**池**字段中选择工作订单池。</span><span class="sxs-lookup"><span data-stu-id="7b252-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="7b252-145">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7b252-145">Select **OK**.</span></span>

6. <span data-ttu-id="7b252-146">要将添加的工作订单以特定顺序放入工作订单池中，请在**所有工作订单池**或**有效工作订单池**列表页上，选择池，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="7b252-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="7b252-147">然后，在**工作订单池**页面的**工作订单**快速选项卡上，使用**排序顺序**字段调整池中包含的工作订单的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="7b252-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="7b252-148">要从工作订单池中删除工作订单，重复这些步骤，但在步骤 3 中选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="7b252-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

