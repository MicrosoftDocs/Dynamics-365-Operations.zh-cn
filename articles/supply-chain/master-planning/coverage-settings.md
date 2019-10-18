---
title: 覆盖范围设置
description: 本主题提供有关主计划编制用于计算物料要求的覆盖范围设置的信息。
author: roxanadiaconu
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a63184852751bb65fb7e80d721f8c48fd847609
ms.sourcegitcommit: edfd805356894710488ce07cb1c89313f448b222
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2019
ms.locfileid: "1998963"
---
# <a name="coverage-settings"></a><span data-ttu-id="964a6-103">覆盖范围设置</span><span class="sxs-lookup"><span data-stu-id="964a6-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="964a6-104">主计划编制使用覆盖范围设置计算物料需求。</span><span class="sxs-lookup"><span data-stu-id="964a6-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="964a6-105">您可以通过以下几种方式指定覆盖范围设置：</span><span class="sxs-lookup"><span data-stu-id="964a6-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="964a6-106">为覆盖范围组指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="964a6-107">您可以创建一个覆盖范围组，它包含与该组关联的所有产品的设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="964a6-108">若要创建覆盖范围组，请转到**主计划 &gt; 设置 &gt; 覆盖范围 &gt; 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="964a6-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="964a6-109">您可以将覆盖范围组与某个产品链接。</span><span class="sxs-lookup"><span data-stu-id="964a6-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="964a6-110">如果链接特定于站点、仓库或产品维度，请使用**物料覆盖范围**页的**覆盖范围组**字段。</span><span class="sxs-lookup"><span data-stu-id="964a6-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="964a6-111">如果链接是通用的，无论产品维度如何，请使用**产品详细信息**页的**计划**快速选项卡上的**覆盖范围组**字段。</span><span class="sxs-lookup"><span data-stu-id="964a6-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="964a6-112">默认情况下，如果您没有将某一覆盖范围组与某一产品关联，则主计划将使用在**主计划参数**页中指定的一般覆盖范围组作为默认覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="964a6-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="964a6-113">为产品指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="964a6-114">您可为特定产品创建覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="964a6-115">转到**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="964a6-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="964a6-116">选择产品，然后在操作窗格上的**计划**选项卡中**覆盖范围组**中，选择**物料覆盖范围**打开**物料覆盖范围**页。</span><span class="sxs-lookup"><span data-stu-id="964a6-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="964a6-117">如果该产品已链接到某一覆盖范围组，则您可以使用**覆盖**字段覆盖该覆盖范围组设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="964a6-118">**物料覆盖范围**页上的覆盖范围设置优先于**覆盖范围组**页上的设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="964a6-119">使用向导为产品指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="964a6-120">此向导将引导您逐步执行主物料覆盖范围参数设置流程。</span><span class="sxs-lookup"><span data-stu-id="964a6-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="964a6-121">在**物料覆盖范围**页上的操作窗格中，选择**向导**打开**物料覆盖范围向导**。</span><span class="sxs-lookup"><span data-stu-id="964a6-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="964a6-122">为维度组指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="964a6-123">转到**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="964a6-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="964a6-124">在**已发布产品详细信息**页上，在**常规**快速选项卡上，在**管理**部分中，选择**存储维度组**字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="964a6-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="964a6-125">在**存储维度组**页，选择**按维度的覆盖范围计划**复选框为存储维度组中的维度创建覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="964a6-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="964a6-126">必须为所有产品维度（如配置、颜色、尺寸和样式）选择**按维度的覆盖范围计划**字段。</span><span class="sxs-lookup"><span data-stu-id="964a6-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="964a6-127">覆盖范围代码</span><span class="sxs-lookup"><span data-stu-id="964a6-127">Coverage codes</span></span>

<span data-ttu-id="964a6-128">主计划可以配置为使用不同的补货方法。</span><span class="sxs-lookup"><span data-stu-id="964a6-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="964a6-129">补货方法或批次规模方法是系统用于确定已购买或已生产物料的批次大小的技术。</span><span class="sxs-lookup"><span data-stu-id="964a6-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="964a6-130">每个补货方法都分配了以下覆盖范围代码之一：</span><span class="sxs-lookup"><span data-stu-id="964a6-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="964a6-131">**手动** - 系统不为物料建议采购订单、转移单或生产订单的批次规模方法。</span><span class="sxs-lookup"><span data-stu-id="964a6-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="964a6-132">物料规划员将负责为物料补货创建所需订单。</span><span class="sxs-lookup"><span data-stu-id="964a6-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="964a6-133">**根据需求** - 系统根据需求为物料创建计划采购订单、转移单或生产订单的批次规模方法。</span><span class="sxs-lookup"><span data-stu-id="964a6-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="964a6-134">通常用于具有间断需求的昂贵物料。</span><span class="sxs-lookup"><span data-stu-id="964a6-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="964a6-135">**根据期间** - 将一个期间的所有需求合并为物料的一个订单的批次规模方法。</span><span class="sxs-lookup"><span data-stu-id="964a6-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="964a6-136">订单将期间的第一天进行计划，其数量将在确定的期间内满足净需求。</span><span class="sxs-lookup"><span data-stu-id="964a6-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="964a6-137">期间从物料的第一个需求开始，覆盖定义的时间长度。</span><span class="sxs-lookup"><span data-stu-id="964a6-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="964a6-138">下一个期间将从物料的下一个需求开始。</span><span class="sxs-lookup"><span data-stu-id="964a6-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="964a6-139">**最小/最大** - 当预计的现有量低于阈值时，将库存补货提高到某个级别的批次规模方法。</span><span class="sxs-lookup"><span data-stu-id="964a6-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="964a6-140">补货数量将是最大级别与预计现有量级别之间的差值。</span><span class="sxs-lookup"><span data-stu-id="964a6-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="964a6-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="964a6-141">Additional resources</span></span>

[<span data-ttu-id="964a6-142">主计划</span><span class="sxs-lookup"><span data-stu-id="964a6-142">Master plans</span></span>](master-plans.md)
