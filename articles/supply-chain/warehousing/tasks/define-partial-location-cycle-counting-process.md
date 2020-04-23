---
title: 定义部分库位周期盘点流程
description: 使用周期盘点计划创建盘点工作时，可以通过请求仅盘点特定产品和产品变型，而不是盘点库位中的所有现成库存，指导实际盘点操作。
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3d80171ec524e3401d7971cb743d73abdda87ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217026"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="7eb01-103">定义部分库位周期盘点流程</span><span class="sxs-lookup"><span data-stu-id="7eb01-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7eb01-104">使用周期盘点计划创建盘点工作时，可以通过请求仅盘点特定产品和产品变型，而不是盘点库位中的所有现成库存，指导实际盘点操作。</span><span class="sxs-lookup"><span data-stu-id="7eb01-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="7eb01-105">通过筛选特定产品，仓库经理可以降低审核开销，帮助避免合并错误和节省时间。</span><span class="sxs-lookup"><span data-stu-id="7eb01-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="7eb01-106">通常，仓库管理员执行设置任务。</span><span class="sxs-lookup"><span data-stu-id="7eb01-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="7eb01-107">您可以在 USMF 演示数据公司或您自己的数据中了解该过程。</span><span class="sxs-lookup"><span data-stu-id="7eb01-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="7eb01-108">创建周期盘点工作模板</span><span class="sxs-lookup"><span data-stu-id="7eb01-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="7eb01-109">转到“仓库管理”>“设置”>“工作”>“工作模板”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="7eb01-110">在“工作订单类型”字段中，选择“周期盘点”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="7eb01-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-111">Click New.</span></span>
4. <span data-ttu-id="7eb01-112">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="7eb01-113">排序顺序是从最小数字到最大数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="7eb01-114">值必须大于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="7eb01-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="7eb01-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7eb01-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="7eb01-116">在“工作模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="7eb01-117">在“工作模板描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="7eb01-118">在“工作池 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="7eb01-119">在“工作优先级”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="7eb01-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-120">Click Save.</span></span>
11. <span data-ttu-id="7eb01-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-121">Click New.</span></span>
12. <span data-ttu-id="7eb01-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7eb01-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7eb01-123">在“工作类型”字段中，选择“盘点”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="7eb01-124">在“工作类 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="7eb01-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-125">Click Save.</span></span>
16. <span data-ttu-id="7eb01-126">单击“工作行中断”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="7eb01-127">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-127">Click New.</span></span>
18. <span data-ttu-id="7eb01-128">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="7eb01-129">排序顺序是从最小数字到最大数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="7eb01-130">值必须大于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="7eb01-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="7eb01-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-131">Click Save.</span></span>
20. <span data-ttu-id="7eb01-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7eb01-132">Close the page.</span></span>
21. <span data-ttu-id="7eb01-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7eb01-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="7eb01-134">创建周期盘点计划</span><span class="sxs-lookup"><span data-stu-id="7eb01-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="7eb01-135">转到“仓库管理”>“设置”>“周期盘点”>“周期盘点计划”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="7eb01-136">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-136">Click New.</span></span>
3. <span data-ttu-id="7eb01-137">在“周期盘点计划 ID ”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="7eb01-138">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7eb01-139">在“周期盘点最大数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="7eb01-140">在“工作模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="7eb01-141">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-141">Click New.</span></span>
8. <span data-ttu-id="7eb01-142">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="7eb01-143">排序顺序是从最小数字到最大数字。</span><span class="sxs-lookup"><span data-stu-id="7eb01-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="7eb01-144">值必须大于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="7eb01-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="7eb01-145">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="7eb01-146">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-146">Click Save.</span></span>
11. <span data-ttu-id="7eb01-147">单击“定义产品查询”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-147">Click Define product query.</span></span>
12. <span data-ttu-id="7eb01-148">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7eb01-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7eb01-149">在“标准”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7eb01-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="7eb01-150">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7eb01-150">Click OK.</span></span>
15. <span data-ttu-id="7eb01-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7eb01-151">Close the page.</span></span>

