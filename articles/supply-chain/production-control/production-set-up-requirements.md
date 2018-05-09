---
title: "生产设置需求"
description: "本文提供您需要先满足才可以使用生产控制的设置要求的相关信息。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ade7e55e0568acd7eff3ceead29c3c6d0ca2da1e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="production-setup-requirements"></a><span data-ttu-id="7f39f-103">生产设置需求</span><span class="sxs-lookup"><span data-stu-id="7f39f-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f39f-104">本文提供您需要先满足才可以使用生产控制的设置要求的相关信息。</span><span class="sxs-lookup"><span data-stu-id="7f39f-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="7f39f-105">生产控制与其他模块中的功能集成。</span><span class="sxs-lookup"><span data-stu-id="7f39f-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="7f39f-106">通过这一相互关联，您可以更改生产订单并确保它们在系统中的所有其他相关流程和计算中自动更新。</span><span class="sxs-lookup"><span data-stu-id="7f39f-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="7f39f-107">以下设置过程按照应完成的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="7f39f-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="7f39f-108">其他模块中要求的基准设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="7f39f-109">在使用生产控制前，必须设置其他模块中的信息。</span><span class="sxs-lookup"><span data-stu-id="7f39f-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="7f39f-110">本安装包含以下任务：</span><span class="sxs-lookup"><span data-stu-id="7f39f-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="7f39f-111">设置一般公司信息。</span><span class="sxs-lookup"><span data-stu-id="7f39f-111">Set up general company information.</span></span>
-   <span data-ttu-id="7f39f-112">设置总帐。</span><span class="sxs-lookup"><span data-stu-id="7f39f-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="7f39f-113">定义物料组。</span><span class="sxs-lookup"><span data-stu-id="7f39f-113">Define item groups.</span></span>
-   <span data-ttu-id="7f39f-114">为物料组设置会计科目。</span><span class="sxs-lookup"><span data-stu-id="7f39f-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="7f39f-115">在库存管理中设置库存物料表。</span><span class="sxs-lookup"><span data-stu-id="7f39f-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="7f39f-116">在库存管理中创建物料清单 (BOM) 和物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="7f39f-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="7f39f-117">要求的日历和资源设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-117">Required calendar and resource setup</span></span>
<span data-ttu-id="7f39f-118">在您使用生产控制前，请打开组织管理，并按以下顺序创建和定义日历和运营资源：</span><span class="sxs-lookup"><span data-stu-id="7f39f-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="7f39f-119">**工作时间模板** – 设置工作时间模板，以便定义可用于生产排产的时间。</span><span class="sxs-lookup"><span data-stu-id="7f39f-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="7f39f-120">**日历** – 设置工作时间日历，以便定义该年度的哪些天可供生产排产。</span><span class="sxs-lookup"><span data-stu-id="7f39f-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="7f39f-121">**资源组** – 在运行计划编制时，设置资源组以分组工序资源，从而让您能够概览所有可用产能。</span><span class="sxs-lookup"><span data-stu-id="7f39f-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="7f39f-122">在设置运营资源前，不必设置资源组。</span><span class="sxs-lookup"><span data-stu-id="7f39f-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="7f39f-123">但是，在您设置生产控制时，我们建议您确定如何对资源分组。</span><span class="sxs-lookup"><span data-stu-id="7f39f-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="7f39f-124">**资源** – 设置运营资源，以便定义用于完成生产流程和计划产能的不同资源。</span><span class="sxs-lookup"><span data-stu-id="7f39f-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="7f39f-125">要求的生产参数设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-125">Required production parameters setup</span></span>
<span data-ttu-id="7f39f-126">**生产控制参数** – 设置基本生产参数，以便定义该系统如何处理生产订单。</span><span class="sxs-lookup"><span data-stu-id="7f39f-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="7f39f-127">定义如何创建、评估、计划和使用生产订单。</span><span class="sxs-lookup"><span data-stu-id="7f39f-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="7f39f-128">您还可以选择所需反馈类型以及执行成本核算的方式。</span><span class="sxs-lookup"><span data-stu-id="7f39f-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="7f39f-129">所需的日志名称标识</span><span class="sxs-lookup"><span data-stu-id="7f39f-129">Required journal name identification</span></span>
<span data-ttu-id="7f39f-130">**生产日记帐名称** – 指定用于记录和过帐交易记录的生产日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="7f39f-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="7f39f-131">使用工序情况下的设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-131">Setup if you use operations</span></span>
<span data-ttu-id="7f39f-132">工序表示为生产成品而完成的特定活动。</span><span class="sxs-lookup"><span data-stu-id="7f39f-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="7f39f-133">**注意：**您必须知道为生产物料而需要的活动的类型，以及这些活动的顺序和优先级。</span><span class="sxs-lookup"><span data-stu-id="7f39f-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="7f39f-134">您还必须知道涉及哪些资源，以及涉及多少资源。</span><span class="sxs-lookup"><span data-stu-id="7f39f-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="7f39f-135">**工序** – 设置工序以表示生产成品而必须完成的任务。</span><span class="sxs-lookup"><span data-stu-id="7f39f-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="7f39f-136">**关系** – 设置用于确立详细属性的工序关系。</span><span class="sxs-lookup"><span data-stu-id="7f39f-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="7f39f-137">若要定义工序关系，请单击**“操作”**页上的**“关系”**。</span><span class="sxs-lookup"><span data-stu-id="7f39f-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="7f39f-138">使用工艺路线情况下的设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-138">Setup if you use routes</span></span>
<span data-ttu-id="7f39f-139">如果您在使用工艺路线，则必须为您设置的每个生产工艺路线定义工序。</span><span class="sxs-lookup"><span data-stu-id="7f39f-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="7f39f-140">工艺路线表示物料在各工序间流动的路线，从生产流程开始直到结束。</span><span class="sxs-lookup"><span data-stu-id="7f39f-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="7f39f-141">**成本类别** – 设置成本类别，以便定义指定流程和设置时间的每工时成本。</span><span class="sxs-lookup"><span data-stu-id="7f39f-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="7f39f-142">**成本组** – 设置用于创建和维护不同类型的成本计算的成本组。</span><span class="sxs-lookup"><span data-stu-id="7f39f-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="7f39f-143">**工艺路线组** – 设置工艺路线组，以便定义与工艺路线组有关的参数。</span><span class="sxs-lookup"><span data-stu-id="7f39f-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="7f39f-144">您必须首先设置工艺路线组，然后才能创建生产工艺路线。</span><span class="sxs-lookup"><span data-stu-id="7f39f-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="7f39f-145">**工艺路线** – 设置生产工艺路线，并定义默认设置，用于控制排产、成本计算和工艺路线工序价格以及控制进度报告。</span><span class="sxs-lookup"><span data-stu-id="7f39f-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="7f39f-146">**工艺路线** – 设置工艺路线版本，以便实现生产中的物料变化。</span><span class="sxs-lookup"><span data-stu-id="7f39f-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="7f39f-147">可选的高级设置</span><span class="sxs-lookup"><span data-stu-id="7f39f-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="7f39f-148">**生产组** – 设置生产组，以便在生产订单和会计科目之间建立关系。</span><span class="sxs-lookup"><span data-stu-id="7f39f-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="7f39f-149">会计科目用于对订单进行过帐或分组，以便报告。</span><span class="sxs-lookup"><span data-stu-id="7f39f-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="7f39f-150">**生产池** – 创建生产池，以便对生产订单进行分组，使您能够处理紧急的生产订单，或者删除和过帐订单组。</span><span class="sxs-lookup"><span data-stu-id="7f39f-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="7f39f-151">**属性** – 定义属性可以创建可分配到您的资源控制生产订单的特殊特性。</span><span class="sxs-lookup"><span data-stu-id="7f39f-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="7f39f-152">这些属性将与工作时间模板相关联。</span><span class="sxs-lookup"><span data-stu-id="7f39f-152">These attributes are connected to the working time template.</span></span>





