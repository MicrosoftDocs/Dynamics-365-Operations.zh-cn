---
title: 预测、工作订单和项目
description: 此主题介绍预测和工作订单与资产管理中的项目管理与核算模块的集成。
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888803"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="4cdcc-103">预测、工作订单和项目</span><span class="sxs-lookup"><span data-stu-id="4cdcc-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4cdcc-104">在资产管理中，与**项目管理与核算**模块集成有助于优化成本控制，因此用户可以跟踪维护作业类型预测和工作订单作业的成本。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="4cdcc-105">跟踪维护作业类型预测需要进行两项设置：</span><span class="sxs-lookup"><span data-stu-id="4cdcc-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="4cdcc-106">在**资产管理** > **设置** > **资产管理参数**中选择一个项目，然后在**资产**选项卡 > **项目**快速选项卡上的**维护预测项目**字段中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="4cdcc-107">创建维护作业类型默认行时，将在**维护作业类型默认**页（**资产管理** > **设置** > **作业** > **维护作业类型默认**）上自动为该行创建一个活动编号。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="4cdcc-108">维护作业类型预测有两个用途：</span><span class="sxs-lookup"><span data-stu-id="4cdcc-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="4cdcc-109">可在**项目管理与核算**模块中跟踪维护作业类型预测的成本。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="4cdcc-110">在为工作订单作业选择维护作业类型时，将把预测自动传输到工作订单作业项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="4cdcc-111">若要跟踪工作订单作业的成本，首先必须设置工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="4cdcc-112">有关详细信息，请参阅[工作订单项目设置](../setup-for-work-orders/work-order-project-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="4cdcc-113">工作订单作业项目</span><span class="sxs-lookup"><span data-stu-id="4cdcc-113">Work order job projects</span></span>

<span data-ttu-id="4cdcc-114">为工作订单创建工作订单作业时，将通过在**工作订单项目**页（**资产管理** > **设置** > **工作订单** > **项目设置**）中为工作订单设置父项目来确定工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="4cdcc-115">工作订单作业项目通过使用以下工作订单信息的组合来创建：</span><span class="sxs-lookup"><span data-stu-id="4cdcc-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="4cdcc-116">工作订单中选择的工作订单类型</span><span class="sxs-lookup"><span data-stu-id="4cdcc-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="4cdcc-117">与工作订单作业中的资产关联的功能位置</span><span class="sxs-lookup"><span data-stu-id="4cdcc-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="4cdcc-118">与工作订单作业中的资产关联的资产类型</span><span class="sxs-lookup"><span data-stu-id="4cdcc-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="4cdcc-119">为工作订单设置的预计开始时间和结束时间</span><span class="sxs-lookup"><span data-stu-id="4cdcc-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="4cdcc-120">工作订单中可能不包含这些信息中的一部分。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="4cdcc-121">因此，将通过使用数据的可用组合和选择与工作订单数据对应的项目 ID 来搜索工作订单父项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="4cdcc-122">例如，在下图中，**卡车引擎**资产类型的设置方式导致使用**卡车引擎**资产类型创建的每个工作订单作业成为项目 ID 000186 的子项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![图 1](media/01-integration-to-pma.png)

<span data-ttu-id="4cdcc-124">工作订单作业中的项目 ID 和关联的活动编号的用途是在**项目管理与核算**模块中跟踪与工作订单作业有关的成本和在其中选择的资产。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="4cdcc-125">（若要查看项目 ID 和活动编号，请选择**资产管理** > **常用** > **工作订单** > **所有工作订单**，然后选择工作订单。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="4cdcc-126">**行详细信息**快速选项卡上的**项目 ID** 字段显示项目 ID，**活动编号**字段显示活动编号。）有关资产管理中的成本控制的详细信息，请参阅[成本和日期控制](../controlling-and-reporting/cost-and-date-control.md)。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="4cdcc-127">下图显示工作订单项目和关联的项目活动的图形概览。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![图 2](media/02-integration-to-pma.png)

<span data-ttu-id="4cdcc-129">为工作订单创建新的工作订单作业时，将为该作业自动创建一个工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="4cdcc-130">将把与该工作订单作业关联的资产的财务维度自动传输到该工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="4cdcc-131">为工作订单作业创建的项目活动附加有相关信息。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="4cdcc-132">此信息与维护作业类型、维护作业类型变型和交易有关。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="4cdcc-133">其在如下情况下非常有用：基于工作订单创建采购订单(请参阅[采购](../work-orders/procurement.md))，或将**项目管理与核算**模块用于时间登记。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="4cdcc-134">如果资产已安装到某个功能位置，但是之后又安装到其他功能位置，则为该资产自动更新与新功能位置关联的财务维度。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="4cdcc-135">然后，当您为该资产创建工作订单作业时，该工作订单作业的工作订单项目将自动获取现在与这个资产关联的财务维度。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="4cdcc-136">因此，如果使用功能位置，则始终可以跟踪在任何给定时间安装了资产的功能位置的成本。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="4cdcc-137">自动更新财务维度有助确保可以完全跟踪成本来进行项目控制和报告。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="4cdcc-138">工作订单项目、工作订单生命周期状态、项目阶段和项目类型</span><span class="sxs-lookup"><span data-stu-id="4cdcc-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="4cdcc-139">若要帮助确保对工作订单正确使用工作订单生命周期状态和关联的项目阶段，请注意与**项目管理与核算**模块有关的依赖关系：</span><span class="sxs-lookup"><span data-stu-id="4cdcc-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="4cdcc-140">在**项目管理与核算**模块中，项目类型的项目阶段是在**项目管理与核算参数**页中设置的。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="4cdcc-141">在**项目管理与核算参数**页中，使用复选框选择将使用的所有项目类型的相关项目阶段。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="4cdcc-142">下图中为**时间和材料**个**内部**项目类型已选择了五个阶段（**已创建**、**已估计**、**已计划**、**进行中**和**已完成**）。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="4cdcc-143">这五个阶段与内部维护作业和服务维护作业都有关。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="4cdcc-144">在**资产管理**模块中，项目类型由您在**工作订单项目设置**页 > **项目设置**选项卡（**资产管理** > **设置** > **工作订单** > **项目设置**）中设置的项目组定义。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="4cdcc-145">创建工作订单时，将使用在**工作订单项目设置**页中设置的项目组。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="4cdcc-146">创建工作订单时，将为该工作订单自动创建一个工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="4cdcc-147">每个工作订单生命周期状态都必须有一个关联的项目阶段。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="4cdcc-148">必须将与工作订单生命周期状态关联的项目阶段定义为在工作订单项目定义的项目组的有效阶段。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="4cdcc-149">将为工作订单自动创建工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="4cdcc-150">创建新的工作订单时，将根据在**工作订单项目设置**页中的设置自动分配工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="4cdcc-151">下图显示工作订单项目组、关联的项目类型、项目阶段和工作订单生命周期状态之间的关联。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![图 3](media/03-integration-to-pma.png)

![图 4](media/04-integration-to-pma.png)

![图 5](media/05-integration-to-pma.png)

<span data-ttu-id="4cdcc-155">有关如何设置工作订单项目的信息，请参阅[工作订单项目设置](../setup-for-work-orders/work-order-project-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="4cdcc-156">有关如何创建工作订单生命周期状态的信息，请参阅[工作订单生命周期状态](../setup-for-work-orders/work-order-lifecycle-states.md)。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="4cdcc-157">下图显示为了实现与**项目管理与核算**模块集成而在**资产管理**模块中创建的各项目的图形概览。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="4cdcc-158">还显示这些项目关联的工作流程。</span><span class="sxs-lookup"><span data-stu-id="4cdcc-158">It also shows the work processes that the projects are related to.</span></span>

![图 6](media/06-integration-to-pma.png)

