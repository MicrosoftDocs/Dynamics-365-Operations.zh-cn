---
title: 库存对象值
description: 本文提供有关库存对象的值如何计算的信息。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "319124"
---
# <a name="inventory-object-values"></a><span data-ttu-id="bb711-103">库存对象值</span><span class="sxs-lookup"><span data-stu-id="bb711-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb711-104">本文提供有关库存对象的值如何计算的信息。</span><span class="sxs-lookup"><span data-stu-id="bb711-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="bb711-105">利用名为**实际数量**的新功能，可以查看特定库存对象的值。</span><span class="sxs-lookup"><span data-stu-id="bb711-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="bb711-106">成本对象表示执行库存盘点的实体级别。</span><span class="sxs-lookup"><span data-stu-id="bb711-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="bb711-107">有关成本对象的更多信息，请参阅[成本对象](cost-object.md)。</span><span class="sxs-lookup"><span data-stu-id="bb711-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="bb711-108">要查看特定库存对象的值，请在**成本对象**页面上单击**实际数量**。</span><span class="sxs-lookup"><span data-stu-id="bb711-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="bb711-109">以下是如何计算库存对象的值：</span><span class="sxs-lookup"><span data-stu-id="bb711-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="bb711-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="bb711-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="bb711-111">以下示例显示如何计算库存对象和成本对象的值。</span><span class="sxs-lookup"><span data-stu-id="bb711-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="bb711-112">在物料 A 上登记两个产品收据事件：</span><span class="sxs-lookup"><span data-stu-id="bb711-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="bb711-113">产品收据 1：数量 = 100 pcs.，金额 = $1,000.00，站点 = 1，仓库 =11，批号 =</span><span class="sxs-lookup"><span data-stu-id="bb711-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bb711-114">= B1</span><span class="sxs-lookup"><span data-stu-id="bb711-114">= B1</span></span>
-   <span data-ttu-id="bb711-115">产品收据 2：数量 = 50 pcs.，金额 = $800.00，站点 = 1，仓库 =11，批号</span><span class="sxs-lookup"><span data-stu-id="bb711-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bb711-116">= B2</span><span class="sxs-lookup"><span data-stu-id="bb711-116">= B2</span></span>

<span data-ttu-id="bb711-117">下表显示成本对象的计算结果。</span><span class="sxs-lookup"><span data-stu-id="bb711-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="bb711-118">您可以在**成本对象**页面上查看结果。</span><span class="sxs-lookup"><span data-stu-id="bb711-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb711-119">对象类型</span><span class="sxs-lookup"><span data-stu-id="bb711-119">Object type</span></span></th>
<th><span data-ttu-id="bb711-120">物料编号</span><span class="sxs-lookup"><span data-stu-id="bb711-120">Item number</span></span></th>
<th><span data-ttu-id="bb711-121">站点</span><span class="sxs-lookup"><span data-stu-id="bb711-121">Site</span></span></th>
<th><span data-ttu-id="bb711-122">数量</span><span class="sxs-lookup"><span data-stu-id="bb711-122">Quantity</span></span></th>
<th><span data-ttu-id="bb711-123">库存单位</span><span class="sxs-lookup"><span data-stu-id="bb711-123">Inventory unit</span></span></th>
<th><span data-ttu-id="bb711-124">值</span><span class="sxs-lookup"><span data-stu-id="bb711-124">Value</span></span></th>
<th><span data-ttu-id="bb711-125">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="bb711-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb711-126">成本对象</span><span class="sxs-lookup"><span data-stu-id="bb711-126">Cost object</span></span></td>
<td><span data-ttu-id="bb711-127">A</span><span class="sxs-lookup"><span data-stu-id="bb711-127">A</span></span></td>
<td><span data-ttu-id="bb711-128">1</span><span class="sxs-lookup"><span data-stu-id="bb711-128">1</span></span></td>
<td><span data-ttu-id="bb711-129">150</span><span class="sxs-lookup"><span data-stu-id="bb711-129">150</span></span></td>
<td><span data-ttu-id="bb711-130">时间单位</span><span class="sxs-lookup"><span data-stu-id="bb711-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="bb711-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="bb711-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="bb711-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="bb711-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bb711-133">下表显示库存对象的计算结果。</span><span class="sxs-lookup"><span data-stu-id="bb711-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="bb711-134">您可以通过在**成本对象**页面上单击**实际数量**来查看结果。</span><span class="sxs-lookup"><span data-stu-id="bb711-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb711-135">对象类型</span><span class="sxs-lookup"><span data-stu-id="bb711-135">Object type</span></span></th>
<th><span data-ttu-id="bb711-136">物料编号</span><span class="sxs-lookup"><span data-stu-id="bb711-136">Item number</span></span></th>
<th><span data-ttu-id="bb711-137">站点</span><span class="sxs-lookup"><span data-stu-id="bb711-137">Site</span></span></th>
<th><span data-ttu-id="bb711-138">仓库</span><span class="sxs-lookup"><span data-stu-id="bb711-138">Warehouse</span></span></th>
<th><span data-ttu-id="bb711-139">批号</span><span class="sxs-lookup"><span data-stu-id="bb711-139">Batch No.</span></span></th>
<th><span data-ttu-id="bb711-140">数量</span><span class="sxs-lookup"><span data-stu-id="bb711-140">Quantity</span></span></th>
<th><span data-ttu-id="bb711-141">库存单位</span><span class="sxs-lookup"><span data-stu-id="bb711-141">Inventory unit</span></span></th>
<th><span data-ttu-id="bb711-142">值</span><span class="sxs-lookup"><span data-stu-id="bb711-142">Value</span></span></th>
<th><span data-ttu-id="bb711-143">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="bb711-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb711-144">库存对象</span><span class="sxs-lookup"><span data-stu-id="bb711-144">Inventory object</span></span></td>
<td><span data-ttu-id="bb711-145">A</span><span class="sxs-lookup"><span data-stu-id="bb711-145">A</span></span></td>
<td><span data-ttu-id="bb711-146">1</span><span class="sxs-lookup"><span data-stu-id="bb711-146">1</span></span></td>
<td><span data-ttu-id="bb711-147">11</span><span class="sxs-lookup"><span data-stu-id="bb711-147">11</span></span></td>
<td><span data-ttu-id="bb711-148">B1</span><span class="sxs-lookup"><span data-stu-id="bb711-148">B1</span></span></td>
<td><span data-ttu-id="bb711-149">100</span><span class="sxs-lookup"><span data-stu-id="bb711-149">100</span></span></td>
<td><span data-ttu-id="bb711-150">时间单位</span><span class="sxs-lookup"><span data-stu-id="bb711-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="bb711-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="bb711-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="bb711-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="bb711-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb711-153">库存对象</span><span class="sxs-lookup"><span data-stu-id="bb711-153">Inventory object</span></span></td>
<td><span data-ttu-id="bb711-154">A</span><span class="sxs-lookup"><span data-stu-id="bb711-154">A</span></span></td>
<td><span data-ttu-id="bb711-155">1</span><span class="sxs-lookup"><span data-stu-id="bb711-155">1</span></span></td>
<td><span data-ttu-id="bb711-156">11</span><span class="sxs-lookup"><span data-stu-id="bb711-156">11</span></span></td>
<td><span data-ttu-id="bb711-157">B2</span><span class="sxs-lookup"><span data-stu-id="bb711-157">B2</span></span></td>
<td><span data-ttu-id="bb711-158">50</span><span class="sxs-lookup"><span data-stu-id="bb711-158">50</span></span></td>
<td><span data-ttu-id="bb711-159">时间单位</span><span class="sxs-lookup"><span data-stu-id="bb711-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="bb711-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="bb711-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="bb711-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="bb711-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="bb711-162">其他资源</span><span class="sxs-lookup"><span data-stu-id="bb711-162">Additional resources</span></span>
--------

[<span data-ttu-id="bb711-163">成本对象</span><span class="sxs-lookup"><span data-stu-id="bb711-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="bb711-164">成本条目</span><span class="sxs-lookup"><span data-stu-id="bb711-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="bb711-165">新增功能和更改的功能</span><span class="sxs-lookup"><span data-stu-id="bb711-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



