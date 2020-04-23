---
title: 维护预测
description: 本主题介绍资产管理中的维护预测。
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
ms.openlocfilehash: 0b9fb9265e93f27035e3770c6edbc9bb84d7a4df
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214818"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="0220e-103">维护预测</span><span class="sxs-lookup"><span data-stu-id="0220e-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0220e-104">创建工作订单时，将创建具有相关的资产和维护作业类型的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="0220e-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="0220e-105">如果选择包含维护预测的维护作业类型，将把这些预测自动复制到工作订单。</span><span class="sxs-lookup"><span data-stu-id="0220e-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="0220e-106">您可能可以将预测行添加到工作订单中或从工作订单中删除它们。</span><span class="sxs-lookup"><span data-stu-id="0220e-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="0220e-107">对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑预测行。</span><span class="sxs-lookup"><span data-stu-id="0220e-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="0220e-108">有关工作订单生命周期状态和相关的项目阶段的详细信息，请参阅[预测、工作订单和项目](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)。</span><span class="sxs-lookup"><span data-stu-id="0220e-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="0220e-109">选择**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="0220e-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0220e-110">在列表中选择工作订单，然后在“操作窗格”> **工作订单**选项卡 > **项目**组中，选择**预测**。</span><span class="sxs-lookup"><span data-stu-id="0220e-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="0220e-111">**工作订单维护预测**页面将显示来自为工作订单作业选择的维护作业类型的预测行。</span><span class="sxs-lookup"><span data-stu-id="0220e-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="0220e-112">向工作订单添加工时预测</span><span class="sxs-lookup"><span data-stu-id="0220e-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="0220e-113">在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="0220e-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="0220e-114">在**工时**快速选项卡上，选择**添加**创建新行。</span><span class="sxs-lookup"><span data-stu-id="0220e-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="0220e-115">在**类别**字段中选择一个类别。</span><span class="sxs-lookup"><span data-stu-id="0220e-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="0220e-116">在**工时**字段中，输入预测工时的数量。</span><span class="sxs-lookup"><span data-stu-id="0220e-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="0220e-117">在**行属性**字段中选择应该对行使用的费用类型。</span><span class="sxs-lookup"><span data-stu-id="0220e-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="0220e-118">向工作订单添加物料预测</span><span class="sxs-lookup"><span data-stu-id="0220e-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="0220e-119">有三种向工作订单维护预测添加物料的方法。</span><span class="sxs-lookup"><span data-stu-id="0220e-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="0220e-120">可以为备件列表或资产物料清单 (BOM) 中不包含的物料（备件）创建行，可以从已核准的备件列表选择备件，或从资产物料清单选择物料。</span><span class="sxs-lookup"><span data-stu-id="0220e-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="0220e-121">在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="0220e-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="0220e-122">在**物料**快速选项卡上，使用适当的方法将物料添加到维护预测中。</span><span class="sxs-lookup"><span data-stu-id="0220e-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="0220e-123">要为备件列表或资产物料清单中不包含的备件创建行，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="0220e-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="0220e-124">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="0220e-124">Select **Add**.</span></span>
2. <span data-ttu-id="0220e-125">在**物料编号**字段中，选择物料。</span><span class="sxs-lookup"><span data-stu-id="0220e-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="0220e-126">在**销售数量**字段中输入数量。</span><span class="sxs-lookup"><span data-stu-id="0220e-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="0220e-127">在**单位**字段中，选择数量的度量单位。</span><span class="sxs-lookup"><span data-stu-id="0220e-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="0220e-128">在**成本价**和**货币**字段中，输入相应值。</span><span class="sxs-lookup"><span data-stu-id="0220e-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="0220e-129">在**行属性**字段中，选择一个行属性。</span><span class="sxs-lookup"><span data-stu-id="0220e-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="0220e-130">要更改物料行中显示的维度的列表，请选择**库存** > **显示维度**，选择维度，然后将**保存设置**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0220e-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="0220e-131">要从已审核的备件列表添加备件，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="0220e-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="0220e-132">选择**添加备件**。</span><span class="sxs-lookup"><span data-stu-id="0220e-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="0220e-133">选择备件，然后根据需要编辑相关信息。</span><span class="sxs-lookup"><span data-stu-id="0220e-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="0220e-134">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0220e-134">Select **OK**.</span></span>

<span data-ttu-id="0220e-135">要从资产物料清单添加物料，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="0220e-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="0220e-136">选择**添加 BOM 物料**。</span><span class="sxs-lookup"><span data-stu-id="0220e-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="0220e-137">选择物料，然后根据需要编辑相关信息。</span><span class="sxs-lookup"><span data-stu-id="0220e-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="0220e-138">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0220e-138">Select **OK**.</span></span>

<span data-ttu-id="0220e-139">若要获取显示所选行上的物料在资产管理中在何处用于资产、维护作业类型默认值、备件和工作订单的概览，请选择**物料使用位置**。</span><span class="sxs-lookup"><span data-stu-id="0220e-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="0220e-140">有关此概览的详细信息，请参阅[物料的使用位置](../controlling-and-reporting/item-where-used.md)。</span><span class="sxs-lookup"><span data-stu-id="0220e-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="0220e-141">向工作订单添加费用预测</span><span class="sxs-lookup"><span data-stu-id="0220e-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="0220e-142">在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="0220e-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="0220e-143">在**费用**快速选项卡上，选择**添加**创建行。</span><span class="sxs-lookup"><span data-stu-id="0220e-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="0220e-144">在**类别**字段中选择一个类别。</span><span class="sxs-lookup"><span data-stu-id="0220e-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="0220e-145">在**数量**字段中输入数量。</span><span class="sxs-lookup"><span data-stu-id="0220e-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="0220e-146">在**成本价**、**销售币种**和**销售价**字段中，输入相应的值。</span><span class="sxs-lookup"><span data-stu-id="0220e-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="0220e-147">在**行属性**字段中选择应该对行使用的费用类型。</span><span class="sxs-lookup"><span data-stu-id="0220e-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="0220e-148">**维护预测总计**快速选项卡在每个快速选项卡上显示为所选工作订单作业和为工作订单创建的行的数量的概览。</span><span class="sxs-lookup"><span data-stu-id="0220e-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="0220e-149">另外还显示工作订单作业的和工作订单的预测工时总计。</span><span class="sxs-lookup"><span data-stu-id="0220e-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="0220e-150">下图显示**工作订单维护预测**页面的示例。</span><span class="sxs-lookup"><span data-stu-id="0220e-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![图 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="0220e-152">自动更新工作订单预测</span><span class="sxs-lookup"><span data-stu-id="0220e-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="0220e-153">如果在 Microsoft Dynamics 365 for Finance and Operations 的其他模块中更新了工时成本、物料成本和费用，资产管理中的工作订单预测可以自动更新以反映这些更改。</span><span class="sxs-lookup"><span data-stu-id="0220e-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="0220e-154">此功能帮助确保工作订单预测中始终使用最新成本价。</span><span class="sxs-lookup"><span data-stu-id="0220e-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="0220e-155">您还可以对[维护作业类型预测](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)进行类似更新。</span><span class="sxs-lookup"><span data-stu-id="0220e-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="0220e-156">选择**资产管理** > **定期** > **预测** > **更新工作订单预测**。</span><span class="sxs-lookup"><span data-stu-id="0220e-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="0220e-157">根据需要，可以在**更新工作订单预测**对话框中，在**要包括的记录**快速选项卡上，添加有关特定工作订单或工作订单作业的选项。</span><span class="sxs-lookup"><span data-stu-id="0220e-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="0220e-158">单击**筛选器**进行相关选择。</span><span class="sxs-lookup"><span data-stu-id="0220e-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="0220e-159">在**在后台运行**快速选项卡上，可根据需要将自动更新设置为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="0220e-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="0220e-160">选择**确定**开始进行预测更新。</span><span class="sxs-lookup"><span data-stu-id="0220e-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="0220e-161">下图显示**更新工作订单预测**对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="0220e-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![图 2](media/07-work-orders.png)
