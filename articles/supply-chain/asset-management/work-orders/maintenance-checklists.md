---
title: 维护清单
description: 本主题介绍资产管理中的维护清单。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a9973840021bd49c0878ab9252bbba9161fd283
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208147"
---
# <a name="maintenance-checklists"></a><span data-ttu-id="41624-103">维护清单</span><span class="sxs-lookup"><span data-stu-id="41624-103">Maintenance checklists</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="41624-104">维护清单是对维护作业类型设置的。</span><span class="sxs-lookup"><span data-stu-id="41624-104">Maintenance checklists are set up on maintenance job types.</span></span> <span data-ttu-id="41624-105">您作为完成工作订单流程的一部分填写维护清单。</span><span class="sxs-lookup"><span data-stu-id="41624-105">You fill in maintenance checklists as part of the process of completing a work order.</span></span> <span data-ttu-id="41624-106">有关如何在**维护作业类型默认值**页面对维护作业类型设置维护清单的详细信息，请参阅[维护作业类型类别和维护工作类型、维护作业类型变型、维护作业工种和维护清单](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)。</span><span class="sxs-lookup"><span data-stu-id="41624-106">For more information about how to set up maintenance checklists on maintenance job types on the **Maintenance job type defaults** page, see [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

<span data-ttu-id="41624-107">处理工作订单的维护清单时，可以填写与维护作业类型关联的预定义维护清单。</span><span class="sxs-lookup"><span data-stu-id="41624-107">When you work with maintenance checklists on a work order, you can fill in the predefined maintenance checklists that are related to maintenance job types.</span></span> <span data-ttu-id="41624-108">您还可以添加更多维护清单。</span><span class="sxs-lookup"><span data-stu-id="41624-108">You can also add more maintenance checklists.</span></span>


## <a name="fill-in-a-maintenance-checklist"></a><span data-ttu-id="41624-109">填写维护清单</span><span class="sxs-lookup"><span data-stu-id="41624-109">Fill in a maintenance checklist</span></span>

1. <span data-ttu-id="41624-110">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="41624-110">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="41624-111">选择工作订单，然后在“操作窗格”上的**工作订单**选项卡上，在**行**组中，选择**维护清单**。</span><span class="sxs-lookup"><span data-stu-id="41624-111">Select the work order and then, on the Action Pane, on the **Work order** tab, in the **Lines** group, select **Maintenance checklist**.</span></span>

3. <span data-ttu-id="41624-112">**工作订单维护作业清单**显示所有工作订单作业的清单。</span><span class="sxs-lookup"><span data-stu-id="41624-112">The **Work order maintenance job checklist** shows the checklists for all work order jobs.</span></span> <span data-ttu-id="41624-113">如果工作订单作业有不同的维护作业类型，则每个工作订单作业的维护清单可能不同。</span><span class="sxs-lookup"><span data-stu-id="41624-113">If the work order jobs have different maintenance job types, the maintenance checklists might differ for each work order job.</span></span> <span data-ttu-id="41624-114">选择工作订单作业以处理关联的维护清单。</span><span class="sxs-lookup"><span data-stu-id="41624-114">Select a work order job to work with the related maintenance checklist.</span></span> <span data-ttu-id="41624-115">将在**行明细**快速选项卡上显示所选维护清单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="41624-115">Details of the selected maintenance checklist line are shown on the **Line details** FastTab.</span></span>

4. <span data-ttu-id="41624-116">按照显示顺序填写所有维护清单行，一次一行。</span><span class="sxs-lookup"><span data-stu-id="41624-116">Complete all the maintenance checklist lines, one at a time, in the order that they appear in.</span></span> <span data-ttu-id="41624-117">可通过填写**行明细**快速选项卡上的字段来填写维护清单行。</span><span class="sxs-lookup"><span data-stu-id="41624-117">You complete a maintenance checklist line by filling in the fields on the **Line details** FastTab.</span></span> <span data-ttu-id="41624-118">填写行所需的信息可能会有所不同，具体取决于行的类型。</span><span class="sxs-lookup"><span data-stu-id="41624-118">The information that is required to complete a line can vary, depending on the line type.</span></span> <span data-ttu-id="41624-119">例如，在**文本**类型的行中添加说明您的检查结果的注释。</span><span class="sxs-lookup"><span data-stu-id="41624-119">For example, on a line of the **Text** type, you add a note that explains the result of your check.</span></span> <span data-ttu-id="41624-120">在**度量**类型的行中，您可以输入在设备上读取的计数器值，也可以根据需要添加注释。</span><span class="sxs-lookup"><span data-stu-id="41624-120">On a line of the **Measurement** type, you enter the counter value that you read on the equipment, and you can also add a note as you require.</span></span> <span data-ttu-id="41624-121">类型为**标题**的维护清单行用作标题来为其下显示的维护清单行分组。</span><span class="sxs-lookup"><span data-stu-id="41624-121">A maintenance checklist line of the **Header** type is used as a heading to group the maintenance checklist lines that appear below it.</span></span> <span data-ttu-id="41624-122">您不必填写标题。</span><span class="sxs-lookup"><span data-stu-id="41624-122">You don't have to fill in a header.</span></span> <span data-ttu-id="41624-123">对于所有其他类型的维护清单行，您可以在**标题**类型的行中添加注释。</span><span class="sxs-lookup"><span data-stu-id="41624-123">As for all other types of maintenance checklist lines, you can add a note to a line of the **Header** type.</span></span>

5. <span data-ttu-id="41624-124">如果为维护清单行关联了说明，则已选中**说明**复选框。</span><span class="sxs-lookup"><span data-stu-id="41624-124">If instructions are related to a maintenance checklist line, the **Instructions** check box is selected.</span></span> <span data-ttu-id="41624-125">可在**行明细**快速选项卡的**说明**字段中查看所选维护清单行的说明。</span><span class="sxs-lookup"><span data-stu-id="41624-125">Read instructions for the selected maintenance checklist line in the **Instructions** field on the **Line details** FastTab.</span></span>

6. <span data-ttu-id="41624-126">填写维护清单行之后，选中该行的**已检查**复选框将其标记为已填写。</span><span class="sxs-lookup"><span data-stu-id="41624-126">When you've completed a maintenance checklist line, select the **Checked** check box on that line to mark it as completed.</span></span> <span data-ttu-id="41624-127">若要由于某个维护清单行与工作订单作业无关而将其放弃，请选中该行上的**不适用**复选框。</span><span class="sxs-lookup"><span data-stu-id="41624-127">To discard a maintenance checklist line because it isn't relevant to the work order job, select the **N/A** check box on the line.</span></span> <span data-ttu-id="41624-128">如果在维护清单行中选中了**必需**复选框，则必须选中**已检查**复选框或**不适用**复选框。</span><span class="sxs-lookup"><span data-stu-id="41624-128">If the **Mandatory** check box is selected on a maintenance checklist line, you must select either the **Checked** check box or the **N/A** check box.</span></span>

>[!NOTE]
><span data-ttu-id="41624-129">只有在工作订单的生命周期状态为[有效](../setup-for-work-orders/work-order-lifecycle-states.md)时，才能更新维护清单登记。</span><span class="sxs-lookup"><span data-stu-id="41624-129">You can only update maintenance checklist registrations if the work order is in an [Active](../setup-for-work-orders/work-order-lifecycle-states.md) lifecycle state.</span></span>  


## <a name="add-a-maintenance-checklist-line"></a><span data-ttu-id="41624-130">添加维护清单行</span><span class="sxs-lookup"><span data-stu-id="41624-130">Add a maintenance checklist line</span></span>

<span data-ttu-id="41624-131">维护清单通过定义维护作业类型默认创建，并传输到工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="41624-131">Maintenance checklists are created from the definition on the maintenance job type default and are transferred to a work order job.</span></span> <span data-ttu-id="41624-132">如果需要，可以向工作订单作业添加维护清单行。</span><span class="sxs-lookup"><span data-stu-id="41624-132">As you require, you can add maintenance checklist lines to a work order job.</span></span> <span data-ttu-id="41624-133">您手动添加的维护清单行为**手动**引用。</span><span class="sxs-lookup"><span data-stu-id="41624-133">Maintenance checklist lines that you manually add get the **Manual** reference.</span></span>

1. <span data-ttu-id="41624-134">在**工作订单维护作业清单**页上，选择要为其添加维护清单的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="41624-134">On the **Work order maintenance job checklist** page, select the work order job to add a maintenance checklist for.</span></span>

2. <span data-ttu-id="41624-135">在**维护清单行**快速选项卡上，选择维护清单行。</span><span class="sxs-lookup"><span data-stu-id="41624-135">On the **Maintenance checklist lines** FastTab, select a maintenance checklist line.</span></span> <span data-ttu-id="41624-136">然后，要在所选行之后插入新行，请按**向下箭头**键。</span><span class="sxs-lookup"><span data-stu-id="41624-136">Then, to insert a new line after the selected line, press the **Down arrow** key.</span></span> <span data-ttu-id="41624-137">将在**行号**字段中自动输入序列中的下一个编号。</span><span class="sxs-lookup"><span data-stu-id="41624-137">The next number in the sequence is automatically entered in the **Line number** field.</span></span> <span data-ttu-id="41624-138">要在所选行之前插入新行，请选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="41624-138">To insert a new line before the selected line, select **Add line**.</span></span> 

3. <span data-ttu-id="41624-139">在**名称**字段中，输入该维护清单行的名称。</span><span class="sxs-lookup"><span data-stu-id="41624-139">On the **Name** field, enter a name for the maintenance checklist line.</span></span>

4. <span data-ttu-id="41624-140">在**类型**字段中，为维护清单行选择类型。</span><span class="sxs-lookup"><span data-stu-id="41624-140">In the **Type** field, select a type for the maintenance checklist line.</span></span> <span data-ttu-id="41624-141">**行明细**快速选项卡包含每个维护清单类型的相关字段。</span><span class="sxs-lookup"><span data-stu-id="41624-141">The **Line details** FastTab contains related fields for each maintenance checklist type.</span></span>
    - <span data-ttu-id="41624-142">**文本** - 使用此类型来添加维护清单行，其中包含说明必须执行的操作的文本。</span><span class="sxs-lookup"><span data-stu-id="41624-142">**Text** - Use this type to add a maintenance checklist line that has text that describes what must be done.</span></span> <span data-ttu-id="41624-143">例如，如果要让工作人员进行检查或检验，但是不希望获得具体（可度量的）结果，可以使用此类型。</span><span class="sxs-lookup"><span data-stu-id="41624-143">For example, you can use this type if you want a worker to check or inspect something, but you aren't expecting a specific (measurable) result.</span></span> <span data-ttu-id="41624-144">选择此类型后，在**行明细**上的**说明**字段中，输入说明必须执行的操作的文本。</span><span class="sxs-lookup"><span data-stu-id="41624-144">After you select this type, on the **Lines details** FastTab, in the **Instructions** field, enter text that describes what must be done.</span></span>
    - <span data-ttu-id="41624-145">**标题** - 此类型的维护清单行用作标题来为其下显示的维护清单行分组。</span><span class="sxs-lookup"><span data-stu-id="41624-145">**Header** - A maintenance checklist line of this type is used as a heading to group the maintenance checklist lines that appear below it.</span></span> <span data-ttu-id="41624-146">如果有多个可拆分为特定区域的维护清单行，此类型非常有用。</span><span class="sxs-lookup"><span data-stu-id="41624-146">This type is useful if you have several maintenance checklist lines that can be divided into specific areas.</span></span> <span data-ttu-id="41624-147">选择此类型之后，在**名称**字段中输入描述性名称。</span><span class="sxs-lookup"><span data-stu-id="41624-147">After you select this type, in the **Name** field, enter a descriptive name.</span></span>
    - <span data-ttu-id="41624-148">**模板** - 此类型在工作订单作业中手动添加维护清单行时不适用。</span><span class="sxs-lookup"><span data-stu-id="41624-148">**Template** - This type isn't applicable when you manually add a maintenance checklist line on a work order job.</span></span>  
    - <span data-ttu-id="41624-149">**变量** - 使用此类型来定义维护清单行的一定范围内的可能结果。</span><span class="sxs-lookup"><span data-stu-id="41624-149">**Variable** - Use this type to define a possible result in a range on the maintenance checklist line.</span></span> <span data-ttu-id="41624-150">有关如何设置维护清单变量的信息，请参阅[维护作业类型类别和维护工作类型、维护作业类型变型、维护作业工种和维护清单](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)。</span><span class="sxs-lookup"><span data-stu-id="41624-150">For information about how to set up maintenance checklist variables, see [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span> <span data-ttu-id="41624-151">选择此类型之后，在**名称**字段中输入描述变量的名称。</span><span class="sxs-lookup"><span data-stu-id="41624-151">After you select this type, in the **Name** field, enter a name to describe the variable.</span></span> <span data-ttu-id="41624-152">在**行明细**快速选项卡上的**变量**字段中，选择变量。</span><span class="sxs-lookup"><span data-stu-id="41624-152">On the **Line details** FastTab, in the **Variable** field, select the variable.</span></span> <span data-ttu-id="41624-153">在**说明**字段中，输入说明必须执行的操作的文本。</span><span class="sxs-lookup"><span data-stu-id="41624-153">In the **Instructions** field, enter text that describes what must be done.</span></span>
    - <span data-ttu-id="41624-154">**度量** - 使用此类型可以在维护清单表行上记录特定度量。</span><span class="sxs-lookup"><span data-stu-id="41624-154">**Measurement** - Use this type to record a specific measurement on the maintenance checklist line.</span></span> <span data-ttu-id="41624-155">选择此类型之后，在**名称**字段中输入度量的名称。</span><span class="sxs-lookup"><span data-stu-id="41624-155">After you select this type, in the **Name** field, enter a name for the measurement.</span></span> <span data-ttu-id="41624-156">在**行明细**快速选项卡上的**计数器**和**单位**字段中，选择适当的值。</span><span class="sxs-lookup"><span data-stu-id="41624-156">On the **Line details** FastTab, in the **Counter** and **Unit** fields, select appropriate values.</span></span> <span data-ttu-id="41624-157">在**说明**字段中，输入说明必须执行的操作的文本。</span><span class="sxs-lookup"><span data-stu-id="41624-157">In the **Instructions** field, enter text that describes what must be done.</span></span>

5. <span data-ttu-id="41624-158">手动添加维护清单行之后，请按照上面的**填写维护清单**部分的说明填写行。</span><span class="sxs-lookup"><span data-stu-id="41624-158">When you've finished manually adding maintenance checklist lines, fill in the lines as described in the **Fill in a maintenance checklist** section above.</span></span>

>[!NOTE]
><span data-ttu-id="41624-159">在**工作订单维护作业清单**页面，不能删除具有**作业类型**引用的维护清单行。</span><span class="sxs-lookup"><span data-stu-id="41624-159">On the **Work order maintenance job checklist** page, you can't delete maintenance checklist lines that have the **Job type** reference.</span></span> <span data-ttu-id="41624-160">只能删除您或其他维护工人手动创建的且具有**手动**引用的维护清单行。</span><span class="sxs-lookup"><span data-stu-id="41624-160">You can delete only maintenance checklist lines that you or other maintenance workers have manually created, and that have the **Manual** reference.</span></span>

<span data-ttu-id="41624-161">下图显示了维护清单的示例。</span><span class="sxs-lookup"><span data-stu-id="41624-161">The illustration below shows an example of a maintenance checklist.</span></span>

![图 1](media/14-work-orders.png)

