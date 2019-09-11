---
title: 维护清单
description: 本主题介绍资产管理中的维护清单。
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
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875531"
---
# <a name="maintenance-checklists"></a><span data-ttu-id="458f7-103">维护清单</span><span class="sxs-lookup"><span data-stu-id="458f7-103">Maintenance checklists</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="458f7-104">维护清单是对维护作业类型设置的，在处理工作订单时使用。</span><span class="sxs-lookup"><span data-stu-id="458f7-104">Maintenance checklists are set up on maintenance job types and used when you work on a work order.</span></span> <span data-ttu-id="458f7-105">填写维护清单是完成工作订单时执行的部分工作。</span><span class="sxs-lookup"><span data-stu-id="458f7-105">Filling out maintenance checklists is part of completing a work order.</span></span> <span data-ttu-id="458f7-106">有关如何在**维护作业类型默认**窗体中对维护作业类型设置维护清单的详细信息，请参阅[维护作业类型类别和维护工作类型、维护作业类型变型、维护作业工种和维护清单](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)部分。</span><span class="sxs-lookup"><span data-stu-id="458f7-106">See the [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) section for more information on how to set up maintenance checklists on maintenance job types in the **Maintenance job type defaults** form.</span></span>

<span data-ttu-id="458f7-107">处理工作订单的维护清单时，可以填写与维护作业类型关联的预定义维护清单。</span><span class="sxs-lookup"><span data-stu-id="458f7-107">When you work with maintenance checklists on a work order, you can fill out the predefined maintenance checklists that are related to maintenance job types.</span></span> <span data-ttu-id="458f7-108">还可以添加更多维护清单。</span><span class="sxs-lookup"><span data-stu-id="458f7-108">It is also possible to add additional maintenance checklists.</span></span>

## <a name="fill-out-a-maintenance-checklist"></a><span data-ttu-id="458f7-109">填写维护清单</span><span class="sxs-lookup"><span data-stu-id="458f7-109">Fill out a maintenance checklist</span></span>

1. <span data-ttu-id="458f7-110">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="458f7-110">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="458f7-111">选择工作订单，然后单击**维护清单**。</span><span class="sxs-lookup"><span data-stu-id="458f7-111">Select the work order and click **Maintenance checklist**.</span></span>

3. <span data-ttu-id="458f7-112">在**工作订单维护作业清单**中，可以查看所有工作订单作业的维护清单。</span><span class="sxs-lookup"><span data-stu-id="458f7-112">In **Work order maintenance job checklist**, you see maintenance checklists for all work order jobs.</span></span> <span data-ttu-id="458f7-113">如果工作订单作业有不同的维护作业类型，则每个工作订单作业的维护清单可能不同。</span><span class="sxs-lookup"><span data-stu-id="458f7-113">If the work order jobs have different maintenance job types, the maintenance checklists may be different on each work order job.</span></span> <span data-ttu-id="458f7-114">选择工作订单作业以处理关联的维护清单。</span><span class="sxs-lookup"><span data-stu-id="458f7-114">Select a work order job to work with the related maintenance checklist.</span></span> <span data-ttu-id="458f7-115">将在**行详细信息**快速选项卡上显示所选维护清单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="458f7-115">Details of a selected maintenance checklist line are shown on the **Line details** FastTab.</span></span>

4. <span data-ttu-id="458f7-116">按照显示顺序填写所有维护清单行，一次一行。</span><span class="sxs-lookup"><span data-stu-id="458f7-116">Complete all the maintenance checklist lines, one at a time, in the sequential order they are shown.</span></span> <span data-ttu-id="458f7-117">类型为“标题”的维护清单行用作标题来为其下的维护清单行分组。</span><span class="sxs-lookup"><span data-stu-id="458f7-117">A maintenance checklist line of type "Header" is used as a heading to group the maintenance checklist lines below.</span></span> <span data-ttu-id="458f7-118">无需填写标题，但是对于所有维护清单行类型，可以向标题添加**注释**。</span><span class="sxs-lookup"><span data-stu-id="458f7-118">You are not required to fill out a header, but as for all maintenance checklist line types, it is possible to add a **Note** to the header.</span></span>

5. <span data-ttu-id="458f7-119">如果为维护清单行关联了说明，则已选中**说明**复选框。</span><span class="sxs-lookup"><span data-stu-id="458f7-119">If instructions are related to a maintenance checklist line, the **Instructions** check box is selected.</span></span> <span data-ttu-id="458f7-120">可在**行详细信息**快速选项卡 > **说明**部分中查看所选维护清单行的说明。</span><span class="sxs-lookup"><span data-stu-id="458f7-120">Read instructions for the selected maintenance checklist line on the **Line details** FastTab > **Instructions** section.</span></span>

6. <span data-ttu-id="458f7-121">填写维护清单行所需信息取决于关联的维护清单类型。</span><span class="sxs-lookup"><span data-stu-id="458f7-121">The information required to complete a maintenance checklist line may vary, depending on the related maintenance checklist type.</span></span> <span data-ttu-id="458f7-122">可通过填写**行详细信息**快速选项卡上的字段来填写维护清单行。</span><span class="sxs-lookup"><span data-stu-id="458f7-122">You complete a maintenance checklist line by filling out the fields on the **Line details** FastTab.</span></span> <span data-ttu-id="458f7-123">例如，在类型为“文本”的行中添加**注释**，用于说明该清单行的结果。</span><span class="sxs-lookup"><span data-stu-id="458f7-123">For example, on a line of type "Text", you add a **Note** explaining what was the result of that checklist line.</span></span> <span data-ttu-id="458f7-124">在类型为“度量”的行中添加读取的设备**计数器值**，如果需要，还可以添加**注释**。</span><span class="sxs-lookup"><span data-stu-id="458f7-124">On a line of type "Measurement", you add the **Counter value** you read on the equipment, and you can also add a **Note**, if required.</span></span>

- <span data-ttu-id="458f7-125">填写维护清单行之后，选中该行的**已选中**复选框将其标记为已填写。</span><span class="sxs-lookup"><span data-stu-id="458f7-125">When you have completed a maintenance checklist line, select the **Checked** check box on the line to mark it as completed.</span></span> <span data-ttu-id="458f7-126">如果因为某个维护清单行与工作订单作业无关而希望将其放弃，请选中该行上的**不适用**复选框。</span><span class="sxs-lookup"><span data-stu-id="458f7-126">If you want to discard a maintenance checklist line because it's not relevant for the work order job, select the **N/A** check box on the line.</span></span> <span data-ttu-id="458f7-127">如果维护清单行标记为**必需**，则必须将其标记为“已选中”或“不适用”。</span><span class="sxs-lookup"><span data-stu-id="458f7-127">If a maintenance checklist line is marked **Mandatory**, you must mark it as either "Checked" or "N/A".</span></span>  
- <span data-ttu-id="458f7-128">只有在工作订单的生命周期状态为[有效](../setup-for-work-orders/work-order-lifecycle-states.md)时，才能更新维护清单登记。</span><span class="sxs-lookup"><span data-stu-id="458f7-128">You can only update maintenance checklist registrations if the work order is in an [Active](../setup-for-work-orders/work-order-lifecycle-states.md) lifecycle state.</span></span>  


## <a name="add-a-maintenance-checklist-line"></a><span data-ttu-id="458f7-129">添加维护清单行</span><span class="sxs-lookup"><span data-stu-id="458f7-129">Add a maintenance checklist line</span></span>

<span data-ttu-id="458f7-130">维护清单通过定义维护作业类型默认创建，并传输到工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="458f7-130">Maintenance checklists are created from the definition on the maintenance job type default and transferred to a work order job.</span></span> <span data-ttu-id="458f7-131">如果需要，可以向工作订单作业添加维护清单行。</span><span class="sxs-lookup"><span data-stu-id="458f7-131">If required, you can add maintenance checklist lines to a work order job.</span></span> <span data-ttu-id="458f7-132">手动添加的维护清单行为“手动”引用。</span><span class="sxs-lookup"><span data-stu-id="458f7-132">Manually added maintenance checklist lines get the reference "Manual".</span></span>

1. <span data-ttu-id="458f7-133">在**工作订单维护作业清单**中，选择要为其添加维护清单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="458f7-133">In **Work order maintenance job checklist**, select the work order job for which you want to add a maintenance checklist.</span></span>

2. <span data-ttu-id="458f7-134">如果要在所选维护清单行后面插入新行，请在**维护清单行**快速选项卡上选择一个维护清单行，然后按键盘上的向下箭头按钮。</span><span class="sxs-lookup"><span data-stu-id="458f7-134">On the **Maintenance checklist lines** FastTab, select a maintenance checklist line and press the arrow-down button on your keyboard if you want to insert a new line after the selected maintenance checklist line.</span></span> <span data-ttu-id="458f7-135">将在**行号**字段中自动插入序列中的下一个编号。</span><span class="sxs-lookup"><span data-stu-id="458f7-135">The next number in the sequence is automatically inserted in the **Line number** field.</span></span> <span data-ttu-id="458f7-136">如果要在所选维护清单行上方插入新行，也可以选择一个维护清单行，然后单击**添加行**按钮。</span><span class="sxs-lookup"><span data-stu-id="458f7-136">You can also select a maintenance checklist line and click the **Add line** button if you want to insert a new line above the selected maintenance checklist line.</span></span>

3. <span data-ttu-id="458f7-137">在**名称**字段中插入该维护清单行的名称。</span><span class="sxs-lookup"><span data-stu-id="458f7-137">Insert a name for the maintenance checklist line in the **Name** field.</span></span>

4. <span data-ttu-id="458f7-138">在**类型**字段中，为维护清单行选择类型。</span><span class="sxs-lookup"><span data-stu-id="458f7-138">In the **Type** field, select a type for the maintenance checklist line.</span></span> <span data-ttu-id="458f7-139">对于每个维护清单类型，**行详细信息**快速选项卡上将显示相关字段。</span><span class="sxs-lookup"><span data-stu-id="458f7-139">For each maintenance checklist type, the related fields are shown on the **Line details** FastTab.</span></span>  
  <span data-ttu-id="458f7-140">a.</span><span class="sxs-lookup"><span data-stu-id="458f7-140">a.</span></span> <span data-ttu-id="458f7-141">“文本”用于添加包含有关要执行的操作文本说明的维护清单行。</span><span class="sxs-lookup"><span data-stu-id="458f7-141">"Text" is used to add a maintenance checklist line with a text description of what to do.</span></span> <span data-ttu-id="458f7-142">如果要让工人进行检查或检验，但是不需要获得具体（可度量的）结果，可使用此维护清单类型。</span><span class="sxs-lookup"><span data-stu-id="458f7-142">This maintenance checklist type can be used if you want a worker to check or inspect something, without expecting a specific (measurable) result.</span></span> <span data-ttu-id="458f7-143">请在**行详细信息**快速选项卡上的**说明**部分中插入要执行的操作的说明。</span><span class="sxs-lookup"><span data-stu-id="458f7-143">Insert a description of what to do in the **Instructions** section on the **Line details** FastTab.</span></span> <span data-ttu-id="458f7-144">b.</span><span class="sxs-lookup"><span data-stu-id="458f7-144">b.</span></span> <span data-ttu-id="458f7-145">“标题”用作标题来为标题下显示的维护清单行分组。</span><span class="sxs-lookup"><span data-stu-id="458f7-145">"Header" is used as a heading to group the maintenance checklist lines shown below the header.</span></span> <span data-ttu-id="458f7-146">如果有多个可拆分为特定区域的维护清单行，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="458f7-146">This is useful if you have several maintenance checklist lines that can be divided into specific areas.</span></span> <span data-ttu-id="458f7-147">请在**名称**字段中插入描述性名称。</span><span class="sxs-lookup"><span data-stu-id="458f7-147">Insert a descriptive name in the **Name** field.</span></span>  
  <span data-ttu-id="458f7-148">c.</span><span class="sxs-lookup"><span data-stu-id="458f7-148">c.</span></span> <span data-ttu-id="458f7-149">在工作订单作业中手动添加维护清单行时，“模板”不适用。</span><span class="sxs-lookup"><span data-stu-id="458f7-149">"Template" is not applicable when you add a maintenance checklist line manually on a work order job.</span></span>  
  <span data-ttu-id="458f7-150">d.</span><span class="sxs-lookup"><span data-stu-id="458f7-150">d.</span></span> <span data-ttu-id="458f7-151">“变量”用于定义维护清单行的一定范围可能结果。</span><span class="sxs-lookup"><span data-stu-id="458f7-151">"Variable" is used to define a possible result in a range on a maintenance checklist line.</span></span> <span data-ttu-id="458f7-152">[维护作业类型类别和维护工作类型、维护作业类型变型、维护作业贸易和维护清单](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)中介绍了维护清单变量的设置。</span><span class="sxs-lookup"><span data-stu-id="458f7-152">The setup of maintenance checklist variables is described in [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span> <span data-ttu-id="458f7-153">在**名称**字段中插入用于描述变量的名称。</span><span class="sxs-lookup"><span data-stu-id="458f7-153">Insert a name to describe the variable in the **Name** field.</span></span> <span data-ttu-id="458f7-154">在**变量**字段中选择变量。</span><span class="sxs-lookup"><span data-stu-id="458f7-154">Select the variable in the **Variable** field.</span></span> <span data-ttu-id="458f7-155">请在**行详细信息**快速选项卡上的**说明**部分中插入要执行的操作的说明。</span><span class="sxs-lookup"><span data-stu-id="458f7-155">Insert a description of what to do in the **Instructions** section on the **Line details** FastTab.</span></span>  
  <span data-ttu-id="458f7-156">e.</span><span class="sxs-lookup"><span data-stu-id="458f7-156">e.</span></span> <span data-ttu-id="458f7-157">“度量”用于记录特定度量。</span><span class="sxs-lookup"><span data-stu-id="458f7-157">"Measurement" is used to record a specific measurement.</span></span> <span data-ttu-id="458f7-158">在**名称**字段中插入度量的名称。</span><span class="sxs-lookup"><span data-stu-id="458f7-158">Insert a name for the measurement in the **Name** field.</span></span> <span data-ttu-id="458f7-159">在**行详细信息**快速选项卡上，选择**计数器**和**单位**。</span><span class="sxs-lookup"><span data-stu-id="458f7-159">On the **Line details** FastTab, select **Counter** and **Unit**.</span></span> <span data-ttu-id="458f7-160">在**说明**部分中插入要执行的操作的说明。</span><span class="sxs-lookup"><span data-stu-id="458f7-160">Insert a description of what to do in the **Instructions** section.</span></span>  

5. <span data-ttu-id="458f7-161">手动添加维护清单行之后，按照上面部分中的说明填写行。</span><span class="sxs-lookup"><span data-stu-id="458f7-161">When you are done adding maintenance checklist lines manually, fill out the lines as described in the section above.</span></span>

>[!NOTE]
><span data-ttu-id="458f7-162">不能删除**工作订单维护作业清单**中引用为“作业类型”的维护清单行。</span><span class="sxs-lookup"><span data-stu-id="458f7-162">In **Work order maintenance job checklist**, you can't delete maintenance checklist lines with the reference "Job type".</span></span> <span data-ttu-id="458f7-163">只能删除引用为“手动”的维护清单行，此类行是您或其他维护工人手动创建的。</span><span class="sxs-lookup"><span data-stu-id="458f7-163">You can only delete maintenance checklist lines with the reference "Manual", which you or other maintenance workers have created manually.</span></span>


![图 1](media/14-work-orders.png)

