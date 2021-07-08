---
title: 惯例
description: 本主题介绍了如何设置惯例以确定应如何在全球库存核算中核算成本。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273120"
---
# <a name="conventions"></a><span data-ttu-id="0e20d-103">惯例</span><span class="sxs-lookup"><span data-stu-id="0e20d-103">Conventions</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="0e20d-104">惯例是一组影响系统行为的策略的容器。</span><span class="sxs-lookup"><span data-stu-id="0e20d-104">A convention is a container for a set of policies that affect system behavior.</span></span> <span data-ttu-id="0e20d-105">基于您的业务需求，必须使用各种策略的组合来定义惯例，这些策略用于确定应如何在全球库存核算中核算成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-105">Based on your business requirements, you must define conventions by using a combination of the various policies that establish how costs should be accounted in Global Inventory Accounting.</span></span> <span data-ttu-id="0e20d-106">您可以将每个惯例与一个或多个分类帐相关联，以确保跨分类帐应用的核算策略的一致性。</span><span class="sxs-lookup"><span data-stu-id="0e20d-106">You can associate each convention with one or more ledgers to ensure consistency in accounting policies that are applied across ledgers.</span></span>

<span data-ttu-id="0e20d-107">若要设置您的惯例，请转到 **全球库存核算 \> 设置 \> 惯例**。</span><span class="sxs-lookup"><span data-stu-id="0e20d-107">To set up your conventions, go to **Global inventory accounting \> Setup \> Conventions**.</span></span> <span data-ttu-id="0e20d-108">对于每个惯例，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="0e20d-108">For each convention, set the following fields:</span></span>

- <span data-ttu-id="0e20d-109">**名称** – 输入惯例的名称。</span><span class="sxs-lookup"><span data-stu-id="0e20d-109">**Name** – Enter the name of the convention.</span></span>
- <span data-ttu-id="0e20d-110">**描述** – 输入惯例的描述。</span><span class="sxs-lookup"><span data-stu-id="0e20d-110">**Description** – Enter a description of the convention.</span></span>
- <span data-ttu-id="0e20d-111">**成本对象策略** – 选择成本对象策略。</span><span class="sxs-lookup"><span data-stu-id="0e20d-111">**Cost Object policy** – Select a cost object policy.</span></span> <span data-ttu-id="0e20d-112">这些策略确定系统应用于计算和维护库存值的粒度级别。</span><span class="sxs-lookup"><span data-stu-id="0e20d-112">These policies determine the level of granularity that the system applies to calculate and maintain the inventory value.</span></span> <span data-ttu-id="0e20d-113">以下预定义选项可用：</span><span class="sxs-lookup"><span data-stu-id="0e20d-113">The following predefined options are available:</span></span>

    - <span data-ttu-id="0e20d-114">产品</span><span class="sxs-lookup"><span data-stu-id="0e20d-114">Product</span></span>
    - <span data-ttu-id="0e20d-115">产品 – 站点</span><span class="sxs-lookup"><span data-stu-id="0e20d-115">Product – Site</span></span>
    - <span data-ttu-id="0e20d-116">产品 – 站点 – 仓库</span><span class="sxs-lookup"><span data-stu-id="0e20d-116">Product – Site – Warehouse</span></span>

    <span data-ttu-id="0e20d-117">例如，如果您选择 *产品 – 站点*，对于每个库存移动（流入或流出），系统都会在站点级别计算和维护每个产品的库存成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-117">For example, if you select *Product – Site*, for every inventory movement (inflow or outflow), the system calculates and maintains the inventory cost of each product at the site level.</span></span> <span data-ttu-id="0e20d-118">因此，较低级别（例如仓库级别）的库存移动不会影响库存价值。</span><span class="sxs-lookup"><span data-stu-id="0e20d-118">Therefore, inventory movements at lower levels, such as the warehouse level, don't affect the inventory value.</span></span> <span data-ttu-id="0e20d-119">（仓库级别转移的一个示例是一个站点中两个仓库之间的物料转移。）同样，您无法在较低级别（例如仓库级别）查看库存成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-119">(An example of a warehouse-level transfer is an item transfer between two warehouses in one site.) Likewise, you can't view the inventory cost at a lower level, such as the warehouse level.</span></span>

- <span data-ttu-id="0e20d-120">**输入度量依据策略** – 选择输入度量依据策略。</span><span class="sxs-lookup"><span data-stu-id="0e20d-120">**Input measurement basis policy** – Select an input measurement basis policy.</span></span> <span data-ttu-id="0e20d-121">这些策略确定应流入库存科目的成本和应收取的成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-121">These policies determine the costs that should flow into the inventory account and the costs that should be charged.</span></span> <span data-ttu-id="0e20d-122">以下选项与贸易公司相关：</span><span class="sxs-lookup"><span data-stu-id="0e20d-122">The following options are relevant for trading companies:</span></span>

    - <span data-ttu-id="0e20d-123">**普通历史** – 所有成本构成都流入库存科目。</span><span class="sxs-lookup"><span data-stu-id="0e20d-123">**Normal historical** – All the cost components flow into the inventory account.</span></span>
    - <span data-ttu-id="0e20d-124">**标准** – 标准成本流入库存科目，向差异科目收取应用成本与实际成本之间的差额。</span><span class="sxs-lookup"><span data-stu-id="0e20d-124">**Standard** – Standard cost flows into the inventory accounts, and the difference between the applied cost and the actual costs is charged to variance accounts.</span></span> <span data-ttu-id="0e20d-125">如果您想要创建 *标准* 输入度量依据策略，必须首先创建一个价目表，策略可以在其中查找物料的标准成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-125">If you want to create a *Standard* input measurement basis policy, you must first create a price list where the policy can look up the item's standard cost.</span></span>
    - <span data-ttu-id="0e20d-126">**价目表** – 全球库存核算支持从多个法人获取物料价格。</span><span class="sxs-lookup"><span data-stu-id="0e20d-126">**Price lists** – Global Inventory Accounting supports fetching item prices from multiple legal entities.</span></span> <span data-ttu-id="0e20d-127">您可以定义输入度量依据策略将使用的价目表。</span><span class="sxs-lookup"><span data-stu-id="0e20d-127">You can define a price list that the input measurement basis policy will use.</span></span> <span data-ttu-id="0e20d-128">这样，系统就会知道在哪里查找物料价格。</span><span class="sxs-lookup"><span data-stu-id="0e20d-128">In this way, the system will know where to look up the item price.</span></span> <span data-ttu-id="0e20d-129">按照以下步骤设置价目表：</span><span class="sxs-lookup"><span data-stu-id="0e20d-129">Follow these steps to set up price lists:</span></span>

        1. <span data-ttu-id="0e20d-130">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="0e20d-130">In the **Name** field, enter a name.</span></span>
        1. <span data-ttu-id="0e20d-131">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="0e20d-131">In the **Description** field, enter a description.</span></span>
        1. <span data-ttu-id="0e20d-132">在 **成本计算类型** 字段中，选择成本计算类型（*标准成本* 或 *计划成本*）。</span><span class="sxs-lookup"><span data-stu-id="0e20d-132">In the **Costing type** field, select a costing type (*Standard cost* or *Planned cost*).</span></span>
        1. <span data-ttu-id="0e20d-133">在 **价格类型** 字段中，选择价格类型（*成本*、*购买* 或 *销售价*）。</span><span class="sxs-lookup"><span data-stu-id="0e20d-133">In the **Price type** field, select a price type (*Cost*, *Purchase*, or *Sales price*).</span></span>
        1. <span data-ttu-id="0e20d-134">添加成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-134">Add a costing version.</span></span>
        1. <span data-ttu-id="0e20d-135">在操作窗格上，选择 **价格** 以验证价目表上的物料价格。</span><span class="sxs-lookup"><span data-stu-id="0e20d-135">On the Action Pane, select **Price** to validate the item prices on the price list.</span></span>

- <span data-ttu-id="0e20d-136">**成本流假设政策** – 选择成本流假设策略。</span><span class="sxs-lookup"><span data-stu-id="0e20d-136">**Cost flow assumption policy** – Select a cost flow assumption policy.</span></span> <span data-ttu-id="0e20d-137">这些策略确定如何从库存中删除成本并将其报告为所售货物成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-137">These policies determine how costs are removed from inventory and reported as the cost of goods sold.</span></span> <span data-ttu-id="0e20d-138">以下预定义选项可用：</span><span class="sxs-lookup"><span data-stu-id="0e20d-138">The following predefined options are available:</span></span>

    - <span data-ttu-id="0e20d-139">平均</span><span class="sxs-lookup"><span data-stu-id="0e20d-139">Average</span></span>
    - <span data-ttu-id="0e20d-140">特定 – 批次</span><span class="sxs-lookup"><span data-stu-id="0e20d-140">Specific – Batch</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e20d-141">全球库存核算是一个永久库存系统。</span><span class="sxs-lookup"><span data-stu-id="0e20d-141">Global Inventory Accounting is a perpetual inventory system.</span></span> <span data-ttu-id="0e20d-142">因此，系统基于每笔交易跟踪库存价值。</span><span class="sxs-lookup"><span data-stu-id="0e20d-142">Therefore, the system tracks the inventory value on a transaction-by-transaction basis.</span></span>

- <span data-ttu-id="0e20d-143">**成本元素策略** – 您可以定义成本元素策略并将它们链接到此字段。</span><span class="sxs-lookup"><span data-stu-id="0e20d-143">**Cost element policy** – You can define cost element policies and link them to this field.</span></span> <span data-ttu-id="0e20d-144">*成本元素* 是事件所消耗的资源的成本。</span><span class="sxs-lookup"><span data-stu-id="0e20d-144">A *cost element* is the cost of a resource that is consumed by an event.</span></span> <span data-ttu-id="0e20d-145">您可以使用成本元素跟踪成本并对其进行分类。</span><span class="sxs-lookup"><span data-stu-id="0e20d-145">You can use cost elements to track and categorize costs.</span></span> <span data-ttu-id="0e20d-146">若要创建成本元素策略，请在以下位置输入信息：</span><span class="sxs-lookup"><span data-stu-id="0e20d-146">To create cost element policies, enter information in the following places:</span></span>

    - <span data-ttu-id="0e20d-147">**名称** 字段</span><span class="sxs-lookup"><span data-stu-id="0e20d-147">**Name** field</span></span>
    - <span data-ttu-id="0e20d-148">**描述** 字段</span><span class="sxs-lookup"><span data-stu-id="0e20d-148">**Description** field</span></span>
    - <span data-ttu-id="0e20d-149">**成本元素** 列表</span><span class="sxs-lookup"><span data-stu-id="0e20d-149">**Cost element** list</span></span>
    - <span data-ttu-id="0e20d-150">**规则** 网格</span><span class="sxs-lookup"><span data-stu-id="0e20d-150">**Rules** grid</span></span>

    <span data-ttu-id="0e20d-151">如果您不想要对库存价值进行进一步细分，必须仍然创建具有单个成本元素的成本元素列表。</span><span class="sxs-lookup"><span data-stu-id="0e20d-151">If you don't want to break down the inventory value further, you must still create a cost element list that has a single cost element.</span></span> <span data-ttu-id="0e20d-152">然后，必须创建成本元素策略，以将所有相关的度量类型（成本构成）映射到该成本元素。</span><span class="sxs-lookup"><span data-stu-id="0e20d-152">You must then create a cost element policy to map all the relevant measurement types (cost components) to that cost element.</span></span>
