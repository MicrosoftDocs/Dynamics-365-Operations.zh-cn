---
title: 预测、工作订单和项目
description: 此主题介绍预测和工作订单与资产管理中的项目管理与核算模块的集成。
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886808"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="6e5fc-103">预测、工作订单和项目</span><span class="sxs-lookup"><span data-stu-id="6e5fc-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6e5fc-104">在资产管理中，与**项目管理与核算**模块集成是为了优化成本控制，从而让用户可以跟踪维护作业类型预测和工作订单作业的成本。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="6e5fc-105">若要跟踪维护作业类型预测，必须进行两项设置：</span><span class="sxs-lookup"><span data-stu-id="6e5fc-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="6e5fc-106">在**资产管理** > **设置** > **资产管理参数** > **资产**链接 > **项目**快速选项卡 > **维护预测项目**字段中选择项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="6e5fc-107">在**维护作业类型默认**中，在创建维护作业类型默认行时，将为此行自动创建一个活动编号（**资产管理** > **设置** > **作业** > **维护作业类型默认**）。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="6e5fc-108">维护作业类型预测起到两个作用：在**项目管理与核算**模块中跟踪维护作业类型预测的成本。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="6e5fc-109">此外，在为工作订单作业选择维护作业类型时，将把预测自动传输到工作订单作业项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="6e5fc-110">若要跟踪工作订单作业的成本，首先必须设置工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="6e5fc-111">有关此过程的描述，请参阅[工作订单项目设置](../setup-for-work-orders/work-order-project-setup.md)部分。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="6e5fc-112">工作订单作业项目</span><span class="sxs-lookup"><span data-stu-id="6e5fc-112">Work order job projects</span></span>

<span data-ttu-id="6e5fc-113">为工作订单创建工作订单作业时，将通过在**资产管理** > **设置** > **工作订单** > **项目设置**中为工作订单设置父项目来确定工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="6e5fc-114">工作订单作业项目通过使用以下工作订单信息的组合来创建：</span><span class="sxs-lookup"><span data-stu-id="6e5fc-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="6e5fc-115">工作订单中选择的工作订单类型</span><span class="sxs-lookup"><span data-stu-id="6e5fc-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="6e5fc-116">与工作订单作业中的资产关联的功能位置</span><span class="sxs-lookup"><span data-stu-id="6e5fc-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="6e5fc-117">与工作订单作业中的资产关联的资产类型</span><span class="sxs-lookup"><span data-stu-id="6e5fc-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="6e5fc-118">为工作订单设置的预计开始时间和结束时间</span><span class="sxs-lookup"><span data-stu-id="6e5fc-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="6e5fc-119">工作订单中可能并未包含上面介绍的所有信息。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="6e5fc-120">因此，将通过使用数据的可用组合和选择与工作订单数据对应的项目 ID 来搜索工作订单父项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="6e5fc-121">示例：在下图中，设置资产类型“卡车引擎”意味着使用该资产类型创建的每个工作订单作业都将是项目 ID“000186”的子项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![图 1](media/01-integration-to-pma.png)

<span data-ttu-id="6e5fc-123">工作订单作业的项目 ID 和关联的活动编号（**资产管理** > **常用** > **工作订单** > **所有工作订单** > 在列表中选择工作订单 > **行详细信息**快速选项卡 > **项目 ID** 字段和**活动编号**字段）的用途是，在**项目管理与核算**模块中跟踪与工作订单作业及为其选择的资产的成本。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="6e5fc-124">在下图中，将显示工作订单项目和关联的项目活动的图形概览。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![图 2](media/02-integration-to-pma.png)

<span data-ttu-id="6e5fc-126">为工作订单创建新的工作订单作业时，将为该作业自动创建一个工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="6e5fc-127">将把与该工作订单作业关联的资产的财务维度自动传输到该工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="6e5fc-128">将把与维护作业类型、维护作业类型变型和工种有关的相关信息附加到为工作订单作业创建的项目活动。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="6e5fc-129">这些数据在如下情况下非常有用：基于工作订单创建采购订单（请参阅[采购](../work-orders/procurement.md)），或将**项目管理与核算**模块用于时间登记。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="6e5fc-130">如果资产已安装到某个功能位置，并且之后又安装到另一个功能位置，则为该资产自动更新与新功能位置关联的财务维度。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="6e5fc-131">然后，当您为该资产创建工作订单作业时，该工作订单作业的工作订单项目将自动获取现在与这个资产关联的财务维度。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="6e5fc-132">这意味着，如果使用功能位置，则始终可以跟踪在任何给定时间安装了资产的功能位置的成本。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="6e5fc-133">自动更新财务维度确保了可以完全跟踪成本来进行项目控制和报告。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="6e5fc-134">工作订单项目、工作订单生命周期状态、项目阶段和项目类型</span><span class="sxs-lookup"><span data-stu-id="6e5fc-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="6e5fc-135">若要确保对工作订单正确使用工作订单生命周期状态和关联的项目阶段，请注意与**项目管理与核算**模块有关的依赖关系：</span><span class="sxs-lookup"><span data-stu-id="6e5fc-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="6e5fc-136">在**项目管理与核算**模块中，项目类型的项目阶段是在**项目管理与核算参数**中设置的。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="6e5fc-137">在**项目管理与核算参数**中，务必选中要使用的所有项目类型的相关项目阶段复选框。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="6e5fc-138">下图中为项目类型“时间和材料”与“内部”选择了五个阶段：**已创建** - **已估计** - **已计划** - **进行中** - **已完成**。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="6e5fc-139">这五个阶段与内部维护和服务维护作业都有关。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="6e5fc-140">在**资产管理**中，项目类型通过**工作订单项目设置**窗体 > **项目组**链接中设置的项目组定义。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="6e5fc-141">创建工作订单时，将使用**工作订单项目设置**中设置的项目组。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="6e5fc-142">创建工作订单时，将为该工作订单自动创建一个工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="6e5fc-143">每个工作订单生命周期状态都必须有一个关联的项目阶段。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="6e5fc-144">必须将与工作订单生命周期状态关联的项目阶段定义为在工作订单项目定义的项目组的有效阶段。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="6e5fc-145">将为工作订单自动创建工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="6e5fc-146">创建新的工作订单时，将根据**工作订单项目设置**（**资产管理** > **设置** > **工作订单** > **项目设置**）中的设置自动分配工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="6e5fc-147">下图显示了工作订单项目组、关联的项目类型、项目阶段和工作订单生命周期状态之间的关联。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![图 3](media/03-integration-to-pma.png)

![图 4](media/04-integration-to-pma.png)

![图 5](media/05-integration-to-pma.png)

<span data-ttu-id="6e5fc-151">有关如何设置工作订单项目的信息，请参阅[工作订单项目设置](../setup-for-work-orders/work-order-project-setup.md)，有关如何创建工作订单生命周期状态的信息，请参阅[工作订单生命周期状态](../setup-for-work-orders/work-order-lifecycle-states.md)。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="6e5fc-152">下图显示为了与**项目管理与核算**模块集成，在**资产管理**模块中创建的各种项目以及这些项目关联的工作流程的图形概览。</span><span class="sxs-lookup"><span data-stu-id="6e5fc-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![图 6](media/06-integration-to-pma.png)

