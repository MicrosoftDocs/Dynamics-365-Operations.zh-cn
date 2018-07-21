---
title: "计划工作量产能"
description: "本主题介绍如何为一个仓库或全体仓库中的工作人员设置和计划工作量产能。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: ba2386ba51a018990cf879edcdbbaa716437a216
ms.contentlocale: zh-cn
ms.lasthandoff: 07/21/2018

---

# <a name="schedule-workload-capacity"></a><span data-ttu-id="ad535-103">计划工作量产能</span><span class="sxs-lookup"><span data-stu-id="ad535-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ad535-104">您可以计划仓库的工作量产能，也可以预测单个仓库的工作人员当前和未来的工作量。</span><span class="sxs-lookup"><span data-stu-id="ad535-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="ad535-105">您可以为整个仓库计划工作量，或者为传入和传出工作量单独计划工作量。</span><span class="sxs-lookup"><span data-stu-id="ad535-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="ad535-106">若要预测所选仓库的工作量输出，主计划编制数据必须可用于这些仓库。</span><span class="sxs-lookup"><span data-stu-id="ad535-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="ad535-107">有关主计划的详细信息，请参阅[主计划](../master-planning/master-plans.md)。</span><span class="sxs-lookup"><span data-stu-id="ad535-107">For more information, see [Master plans](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="ad535-108">计划和查看仓库的工作量</span><span class="sxs-lookup"><span data-stu-id="ad535-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="ad535-109">若要为仓库计划工作量产能，您为一个或多个仓库创建工作量设置，然后将这些工作量设置与主计划相关联。</span><span class="sxs-lookup"><span data-stu-id="ad535-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="ad535-110">在工作量产能设置中，您可以为入货交易记录或出货交易记录定义重量或体积的限额。</span><span class="sxs-lookup"><span data-stu-id="ad535-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="ad535-111">您还可以为每个仓库创建多个设置，然后将设置与单独的主计划相关联。</span><span class="sxs-lookup"><span data-stu-id="ad535-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="ad535-112">例如，您可以使用此方法应对劳动力的季节性变化。</span><span class="sxs-lookup"><span data-stu-id="ad535-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="ad535-113">如果仓库的工作人员处理入货和出货工作量的交易记录，您可以配置仓库产能设置，以便在合并视图中计划工作量。</span><span class="sxs-lookup"><span data-stu-id="ad535-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="ad535-114">若要计划和查看仓库的工作量，必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="ad535-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="ad535-115">创建工作量产能设置并定义一个或多个仓库的产能限制。</span><span class="sxs-lookup"><span data-stu-id="ad535-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="ad535-116">将工作量产能设置与主计划相关联，以便创建工作量预测并指定这些预测的适用时长。</span><span class="sxs-lookup"><span data-stu-id="ad535-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="ad535-117">创建仓库的工作量产能设置</span><span class="sxs-lookup"><span data-stu-id="ad535-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="ad535-118">选择**库存管理** \> **设置** \> **仓库监视** \> **工作量产能**。</span><span class="sxs-lookup"><span data-stu-id="ad535-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ad535-119">在“操作窗格”中，选择**新建**创建工作量产能设置。</span><span class="sxs-lookup"><span data-stu-id="ad535-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="ad535-120">在**仓库**快速选项卡中，选择**新建**，然后输入有关行的值与仓库关联的产能负荷设置。</span><span class="sxs-lookup"><span data-stu-id="ad535-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="ad535-121">如果**工作量产能**报表应在一个视图中显示入货交易记录和出货交易记录的总工作量，请选中**组合的入货和出货工作量**。</span><span class="sxs-lookup"><span data-stu-id="ad535-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="ad535-122">在**交易记录类型**快速选项卡上，选择工作量限额要应用的入货和出货交易记录的类型。</span><span class="sxs-lookup"><span data-stu-id="ad535-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad535-123">您必须为入货工作量和出货工作量选择至少一个交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="ad535-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="ad535-124">定义体积或重量的限额</span><span class="sxs-lookup"><span data-stu-id="ad535-124">Define limits for volume or weight</span></span>

<span data-ttu-id="ad535-125">您可以为体积或重量设置限额，具体取决于仓库劳动力的相关限额。</span><span class="sxs-lookup"><span data-stu-id="ad535-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="ad535-126">您指定的限额包括在您可以在**工作量产能**报表中查看的工作量产能预测中。</span><span class="sxs-lookup"><span data-stu-id="ad535-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="ad535-127">若要预测有关物料的体积和数量的信息，必须为所有产品指定一个库存物料的标准体积和一个库存物料的重量。</span><span class="sxs-lookup"><span data-stu-id="ad535-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="ad535-128">**已发布产品详细信息**页**管理库存**快速选项卡上的以下字段组中提供了所需字段：</span><span class="sxs-lookup"><span data-stu-id="ad535-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="ad535-129">正在处理</span><span class="sxs-lookup"><span data-stu-id="ad535-129">Handling</span></span>
- <span data-ttu-id="ad535-130">物理维度</span><span class="sxs-lookup"><span data-stu-id="ad535-130">Physical dimensions</span></span>
- <span data-ttu-id="ad535-131">权重量化指标</span><span class="sxs-lookup"><span data-stu-id="ad535-131">Weight measurements</span></span>

<span data-ttu-id="ad535-132">如果此信息指定不正确，在生成**工作量产能**报表时，您将收到消息。</span><span class="sxs-lookup"><span data-stu-id="ad535-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="ad535-133">然后可以从该报告向下钻取到标识要预测未来工作量所需的缺失信息。</span><span class="sxs-lookup"><span data-stu-id="ad535-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="ad535-134">与此主计划关联的工作量产能设置</span><span class="sxs-lookup"><span data-stu-id="ad535-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="ad535-135">选择**库存管理** \> **定期任务** \> **计划工作量**。</span><span class="sxs-lookup"><span data-stu-id="ad535-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="ad535-136">在**主计划**字段中，选择工作量预测使用的主计划。</span><span class="sxs-lookup"><span data-stu-id="ad535-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="ad535-137">在**天数**字段中，指定工作量预测包含的天数。</span><span class="sxs-lookup"><span data-stu-id="ad535-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="ad535-138">在**工作量**字段中，选择与工作量设置关联的主计划。</span><span class="sxs-lookup"><span data-stu-id="ad535-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="ad535-139">查看工作负载产能</span><span class="sxs-lookup"><span data-stu-id="ad535-139">View workload capacity</span></span>

1. <span data-ttu-id="ad535-140">选择**库存管理** \> **查询和报表** \> **实际库存报表** \> **工作量产能**。</span><span class="sxs-lookup"><span data-stu-id="ad535-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ad535-141">在**列数**字段中，指定显示在报表中列的数目。</span><span class="sxs-lookup"><span data-stu-id="ad535-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="ad535-142">在**订单类型**字段中，选择**已计划并确认**、**已计划**或**已确认**，以便指示要对报表预测的订单类型。</span><span class="sxs-lookup"><span data-stu-id="ad535-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="ad535-143">在**负载类型**字段中，选择一种负载类型以指定应预测体积还是重量的工作量产能。</span><span class="sxs-lookup"><span data-stu-id="ad535-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="ad535-144">在**工作量产能**字段中，选择一种工作量产能设置。</span><span class="sxs-lookup"><span data-stu-id="ad535-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>

