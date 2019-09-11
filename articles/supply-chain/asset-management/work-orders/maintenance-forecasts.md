---
title: 维护预测
description: 本主题介绍资产管理中的维护预测。
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
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875528"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="f3e52-103">维护预测</span><span class="sxs-lookup"><span data-stu-id="f3e52-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f3e52-104">创建工作订单时，将创建与资产和维护作业类型关联的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="f3e52-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="f3e52-105">如果选择其中包含维护预测的维护作业类型，将把这些预测自动复制到工作订单。</span><span class="sxs-lookup"><span data-stu-id="f3e52-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="f3e52-106">您可能可以在工作订单中添加或删除预测行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f3e52-107">对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑预测行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="f3e52-108">单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f3e52-109">在列表中选择工作订单，然后单击**预测**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="f3e52-110">在**工作订单维护预测**中，将显示来自为工作订单作业选择的维护作业类型的预测行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="f3e52-111">向工作订单添加工时预测</span><span class="sxs-lookup"><span data-stu-id="f3e52-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="f3e52-112">选择要向其添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="f3e52-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f3e52-113">在**工时**快速选项卡上，单击**添加**创建新行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="f3e52-114">在**类别**字段中选择一个类别。</span><span class="sxs-lookup"><span data-stu-id="f3e52-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="f3e52-115">在**工时**字段中插入预测工时的数量。</span><span class="sxs-lookup"><span data-stu-id="f3e52-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="f3e52-116">在**行属性**字段中选择要对行使用的费用类型。</span><span class="sxs-lookup"><span data-stu-id="f3e52-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="f3e52-117">向工作订单添加物料预测</span><span class="sxs-lookup"><span data-stu-id="f3e52-117">Add items forecast to a work order</span></span>

<span data-ttu-id="f3e52-118">可以通过三种方法向工作订单维护预测添加物料：可以为备件列表做资产 BOM 中不包含的物料（即备件）创建行，可以从已核准的部件列表选择备件，还可以从资产 BOM 选择物料。</span><span class="sxs-lookup"><span data-stu-id="f3e52-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="f3e52-119">选择要向其添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="f3e52-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f3e52-120">选择**物料**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f3e52-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="f3e52-121">选择**添加**为部件列表或资产 BOM 列表中不包含的备件创建新行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="f3e52-122">在**物料编号**字段中选择物料。</span><span class="sxs-lookup"><span data-stu-id="f3e52-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="f3e52-123">在**销售数量**字段中插入数量，然后在**单位**字段中选择数量单位。</span><span class="sxs-lookup"><span data-stu-id="f3e52-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="f3e52-124">在相关字段中插入成本价和币种，然后选择**行属性**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="f3e52-125">如果要更改物料行中显示的维度的列表，请单击**库存** > **显示维度**，选择维度，然后在**保存设置**切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f3e52-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="f3e52-126">如果要向维护预测添加已核准的备件，请单击**添加备件**，选择备件，需要时编辑相关信息，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="f3e52-127">如果要向预测添加资产 BOM 物料，请单击**添加 BOM 物料**，选择物料，需要时编辑相关信息，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="f3e52-128">如果要在资产管理中获取有关在与资产、维护作业类型默认、备件和工作订单关联时，所选行中的物料的使用位置的概览，请选择**物料使用位置**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="f3e52-129">向工作订单添加费用预测</span><span class="sxs-lookup"><span data-stu-id="f3e52-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="f3e52-130">本主题介绍如何向工作订单添加费用预测。</span><span class="sxs-lookup"><span data-stu-id="f3e52-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="f3e52-131">在窗体的左侧，选择要向其添加预测的工作订单作业。</span><span class="sxs-lookup"><span data-stu-id="f3e52-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="f3e52-132">选择**费用**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="f3e52-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="f3e52-133">单击**添加**创建新行。</span><span class="sxs-lookup"><span data-stu-id="f3e52-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="f3e52-134">在**类别**字段中选择一个类别。</span><span class="sxs-lookup"><span data-stu-id="f3e52-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="f3e52-135">在**数量**字段中插入数量。</span><span class="sxs-lookup"><span data-stu-id="f3e52-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="f3e52-136">在相关字段中插入成本价、销售币种和销售价。</span><span class="sxs-lookup"><span data-stu-id="f3e52-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="f3e52-137">在**行属性**字段中选择要对行使用的费用类型。</span><span class="sxs-lookup"><span data-stu-id="f3e52-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="f3e52-138">在**维护预测总计**快速选项卡上的每个选项卡中，可查看为所选工作订单作业和为工作订单创建的行的数量。</span><span class="sxs-lookup"><span data-stu-id="f3e52-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="f3e52-139">还可以查看工作订单作业的和工作订单的预测工时之和。</span><span class="sxs-lookup"><span data-stu-id="f3e52-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![图 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="f3e52-141">自动更新工作订单预测</span><span class="sxs-lookup"><span data-stu-id="f3e52-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="f3e52-142">在资产管理中，可自动更新对已在 Dynamics 365 for Finance and Operations 的其他模块中更新了的有关工时成本、物料成本和费用的工作订单预测的所有更改。</span><span class="sxs-lookup"><span data-stu-id="f3e52-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f3e52-143">这是为了确保工作订单预测中始终使用最新成本价。</span><span class="sxs-lookup"><span data-stu-id="f3e52-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="f3e52-144">还可以对[维护作业类型预测](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)进行类似更新。</span><span class="sxs-lookup"><span data-stu-id="f3e52-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="f3e52-145">单击**资产管理** > **定期** > **预测** > **更新工作订单预测**。</span><span class="sxs-lookup"><span data-stu-id="f3e52-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="f3e52-146">如果需要，可以在**更新工作订单预测**下拉对话框中添加有关特定工作订单或工作订单作业的选项。</span><span class="sxs-lookup"><span data-stu-id="f3e52-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="f3e52-147">单击**筛选**创建这些选项。</span><span class="sxs-lookup"><span data-stu-id="f3e52-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="f3e52-148">如果需要，可以在**在后台运行**快速选项卡上将自动更新设置为批处理作业。</span><span class="sxs-lookup"><span data-stu-id="f3e52-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="f3e52-149">单击**确定**开始进行预测更新。</span><span class="sxs-lookup"><span data-stu-id="f3e52-149">Click **OK** to start the forecast update.</span></span>


![图 2](media/07-work-orders.png)

