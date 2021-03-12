---
title: 成本元素维度
description: 作为成本核算中的其中一个核心支柱，成本元素维度用来对成本分类和跟踪成本流向。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d4812021e45155c811707d54204f4549131da76a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989069"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="e7f84-103">成本元素维度</span><span class="sxs-lookup"><span data-stu-id="e7f84-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7f84-104">作为成本核算中的其中一个核心支柱，成本元素维度用来对成本分类和跟踪成本流向。</span><span class="sxs-lookup"><span data-stu-id="e7f84-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="e7f84-105">一个成本元素对应于会计科目表的成本相关物料。</span><span class="sxs-lookup"><span data-stu-id="e7f84-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="e7f84-106">基本上它可以是成本流向的公司中的最低级别的任何元素类型。</span><span class="sxs-lookup"><span data-stu-id="e7f84-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="e7f84-107">成本元素的概念范围从会计科目到所有与成本相关的资源。</span><span class="sxs-lookup"><span data-stu-id="e7f84-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="e7f84-108">目前，成本核算支持会计科目。</span><span class="sxs-lookup"><span data-stu-id="e7f84-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="e7f84-109">成本元素的两种类型</span><span class="sxs-lookup"><span data-stu-id="e7f84-109">Two types of cost elements</span></span>
<span data-ttu-id="e7f84-110">成本元素有两种类型：主要成本元素和辅助成本元素。</span><span class="sxs-lookup"><span data-stu-id="e7f84-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="e7f84-111">下表描述了两种类型之间的区别：</span><span class="sxs-lookup"><span data-stu-id="e7f84-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7f84-112"><strong>主要成本元素</strong></span><span class="sxs-lookup"><span data-stu-id="e7f84-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="e7f84-113"><strong>辅助成本元素</strong></span><span class="sxs-lookup"><span data-stu-id="e7f84-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7f84-114">主要成本元素表示从财务会计到成本核算的成本流动。</span><span class="sxs-lookup"><span data-stu-id="e7f84-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="e7f84-115">成本元素结构对应于总帐中的损益科目结构，其中成本要素可能对应于主科目。</span><span class="sxs-lookup"><span data-stu-id="e7f84-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="e7f84-116">并非所有的主科目都必须表示为成本元素，具体取决于业务要求。</span><span class="sxs-lookup"><span data-stu-id="e7f84-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="e7f84-117">主要成本元素的一些示例包括：</span><span class="sxs-lookup"><span data-stu-id="e7f84-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="e7f84-118">所售货物成本 (COG)</span><span class="sxs-lookup"><span data-stu-id="e7f84-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="e7f84-119">间接物料成本</span><span class="sxs-lookup"><span data-stu-id="e7f84-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="e7f84-120">人员成本</span><span class="sxs-lookup"><span data-stu-id="e7f84-120">Personnel costs</span></span></li>
<li><span data-ttu-id="e7f84-121">能源成本</span><span class="sxs-lookup"><span data-stu-id="e7f84-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="e7f84-122">辅助成本元素表示内部成本流，因为这些成本仅在成本核算中创建和使用。</span><span class="sxs-lookup"><span data-stu-id="e7f84-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="e7f84-123">它们可用于确保成本来源可以跟踪。</span><span class="sxs-lookup"><span data-stu-id="e7f84-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="e7f84-124">这些成本元素在成本分摊和开销计算中使用。</span><span class="sxs-lookup"><span data-stu-id="e7f84-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="e7f84-125">辅助成本元素的一些示例包括：</span><span class="sxs-lookup"><span data-stu-id="e7f84-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="e7f84-126">生产成本</span><span class="sxs-lookup"><span data-stu-id="e7f84-126">Production costs</span></span></li>
<li><span data-ttu-id="e7f84-127">生产、物料和营销开销</span><span class="sxs-lookup"><span data-stu-id="e7f84-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="e7f84-128">成本元素维度和成本元素维度成员</span><span class="sxs-lookup"><span data-stu-id="e7f84-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="e7f84-129">成本元素被称为“*成本元素维度*”。</span><span class="sxs-lookup"><span data-stu-id="e7f84-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="e7f84-130">各个维度值被称为“*成本元素维度成员*”。</span><span class="sxs-lookup"><span data-stu-id="e7f84-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="e7f84-131">例如，你将美国会计科目表结构 (COA) 作为法定申报的基础。</span><span class="sxs-lookup"><span data-stu-id="e7f84-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="e7f84-132">此 COA 用作成本元素维度。</span><span class="sxs-lookup"><span data-stu-id="e7f84-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="e7f84-133">科目为主要成本元素，在成本核算中表示为成本元素维度成员。</span><span class="sxs-lookup"><span data-stu-id="e7f84-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="e7f84-134">以下屏幕截图举例说明了作为成本元素维度的主科目及其作为成本元素维度成员的实际主科目。</span><span class="sxs-lookup"><span data-stu-id="e7f84-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="e7f84-135">[![作为成本元素维度的主科目的屏幕截图](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="e7f84-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="e7f84-136">通过数据连接器导入成本元素维度成员</span><span class="sxs-lookup"><span data-stu-id="e7f84-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="e7f84-137">为了便于设置成本核算中的成本元素维度成员，您可以使用预构建或您自定义构建的数据连接器检索一个或多个源系统中的主要成本元素。</span><span class="sxs-lookup"><span data-stu-id="e7f84-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="e7f84-138">实施注意事项</span><span class="sxs-lookup"><span data-stu-id="e7f84-138">Implementation considerations</span></span>
<span data-ttu-id="e7f84-139">由于成本元素表示最低级别的成本详细信息，因此您应当确保在实施成本元素结构时包括管理报告所必需的所有成本元素。</span><span class="sxs-lookup"><span data-stu-id="e7f84-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="e7f84-140">为成本控制找出合适的成本元素数量是一项挑战。</span><span class="sxs-lookup"><span data-stu-id="e7f84-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="e7f84-141">如果有上千个成本元素，则难以控制每一个成本元素。</span><span class="sxs-lookup"><span data-stu-id="e7f84-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="e7f84-142">作为替代方案，您可以将成本元素分组，在聚合级别管理成本控制。</span><span class="sxs-lookup"><span data-stu-id="e7f84-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>



