--- 
title: "定义精益计划组"
description: "精益计划组被定义为组，可区分看板计划中的产品。"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3ce7185c68b6342c1eae9cc9568da4bf4cc72205
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="54d8f-103">定义精益计划组</span><span class="sxs-lookup"><span data-stu-id="54d8f-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54d8f-104">精益计划组被定义为组，可区分看板计划中的产品。</span><span class="sxs-lookup"><span data-stu-id="54d8f-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="54d8f-105">每个公司或特定工作单元均可以通过通用关联实现分组。</span><span class="sxs-lookup"><span data-stu-id="54d8f-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="54d8f-106">为了在看板计划列表页具有目视识别特征，每个组都被分配了一个颜色代码。</span><span class="sxs-lookup"><span data-stu-id="54d8f-106">Each group has a color code assigned for visual indication in the kanban scheduling list page.</span></span> <span data-ttu-id="54d8f-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="54d8f-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="54d8f-108">定义精益计划组</span><span class="sxs-lookup"><span data-stu-id="54d8f-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="54d8f-109">转到“产品信息管理”>“精益制造”>“精益计划组”。</span><span class="sxs-lookup"><span data-stu-id="54d8f-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="54d8f-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="54d8f-110">Click New.</span></span>
3. <span data-ttu-id="54d8f-111">在“计划组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="54d8f-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="54d8f-112">计划组可以定义为全局组或工作单元的特定组。</span><span class="sxs-lookup"><span data-stu-id="54d8f-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="54d8f-113">在这个简单的例子中，我们定义了一个全局组且工作单元为空。</span><span class="sxs-lookup"><span data-stu-id="54d8f-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="54d8f-114">该组的设置适用于所有无特定计划组的工作单元。</span><span class="sxs-lookup"><span data-stu-id="54d8f-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="54d8f-115">在颜色选项中选择一种颜色。</span><span class="sxs-lookup"><span data-stu-id="54d8f-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="54d8f-116">颜色用于凸显看板计划清单页或看板流程板上的作业。</span><span class="sxs-lookup"><span data-stu-id="54d8f-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="54d8f-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="54d8f-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="54d8f-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="54d8f-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="54d8f-119">关联产品</span><span class="sxs-lookup"><span data-stu-id="54d8f-119">Associate product</span></span>
1. <span data-ttu-id="54d8f-120">关联特定产品</span><span class="sxs-lookup"><span data-stu-id="54d8f-120">Associate a specific product</span></span>
    * <span data-ttu-id="54d8f-121">可以采用两种方法将产品与精益计划组相关联：特定产品（物料关系类型 = 物料)或者物料分配参数（物料关系类型 = 组）。</span><span class="sxs-lookup"><span data-stu-id="54d8f-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="54d8f-122">在“物料关系类型”字段中，选择“物料”。</span><span class="sxs-lookup"><span data-stu-id="54d8f-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="54d8f-123">在“项目编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="54d8f-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="54d8f-124">在“吞吐率”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="54d8f-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="54d8f-125">默认吞吐率为 1，这意味着相关产品的资源消耗等于生产流的流程活动中指定的产能。</span><span class="sxs-lookup"><span data-stu-id="54d8f-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activities of the production flows.</span></span> <span data-ttu-id="54d8f-126">吞吐率 > 1 的定义是资源消耗高于产能，吞吐率 < 1 的定义是资源消耗低于产能。</span><span class="sxs-lookup"><span data-stu-id="54d8f-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="54d8f-127">该比率用于成本计算以及看板作业消耗量的计算。</span><span class="sxs-lookup"><span data-stu-id="54d8f-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="54d8f-128">关联物料分配参数</span><span class="sxs-lookup"><span data-stu-id="54d8f-128">Associate item allocation key</span></span>
1. <span data-ttu-id="54d8f-129">关联物料分配参数</span><span class="sxs-lookup"><span data-stu-id="54d8f-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="54d8f-130">使用“物料关系类型组”为物料分配参数添加关联。</span><span class="sxs-lookup"><span data-stu-id="54d8f-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="54d8f-131"> 请注意，该流程需要在您的数据中定义的预测物料分配参数。</span><span class="sxs-lookup"><span data-stu-id="54d8f-131">Note that for this process, you need a forecast item allocation key defined in your data.</span></span>  
2. <span data-ttu-id="54d8f-132">在“物料关系类型”字段中，选择“组”。</span><span class="sxs-lookup"><span data-stu-id="54d8f-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="54d8f-133">在“物料分配参数”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="54d8f-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="54d8f-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="54d8f-134">In the list, click the link in the selected row.</span></span>


