---
title: 库存对象值
description: 本文提供有关库存对象的值如何计算的信息。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 543253714b3cf318ad5f6092b190e777772f956f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910129"
---
# <a name="inventory-object-values"></a><span data-ttu-id="fa9ec-103">库存对象值</span><span class="sxs-lookup"><span data-stu-id="fa9ec-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa9ec-104">本文提供有关库存对象的值如何计算的信息。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="fa9ec-105">利用名为 **实际数量** 的新功能，可以查看特定库存对象的值。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="fa9ec-106">成本对象表示执行库存盘点的实体级别。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="fa9ec-107">有关成本对象的更多信息，请参阅[成本对象](cost-object.md)。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="fa9ec-108">要查看特定库存对象的值，请在 **成本对象** 页面上单击 **实际数量**。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="fa9ec-109">以下是如何计算库存对象的值：</span><span class="sxs-lookup"><span data-stu-id="fa9ec-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="fa9ec-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span><span class="sxs-lookup"><span data-stu-id="fa9ec-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="fa9ec-111">以下示例显示如何计算库存对象和成本对象的值。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="fa9ec-112">在物料 A 上登记两个产品收据事件：</span><span class="sxs-lookup"><span data-stu-id="fa9ec-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="fa9ec-113">产品收据 1：数量 = 100 pcs.，金额 = $1,000.00，站点 = 1，仓库 =11，批号 =</span><span class="sxs-lookup"><span data-stu-id="fa9ec-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="fa9ec-114">= B1</span><span class="sxs-lookup"><span data-stu-id="fa9ec-114">= B1</span></span>
-   <span data-ttu-id="fa9ec-115">产品收据 2：数量 = 50 pcs.，金额 = $800.00，站点 = 1，仓库 =11，批号</span><span class="sxs-lookup"><span data-stu-id="fa9ec-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="fa9ec-116">= B2</span><span class="sxs-lookup"><span data-stu-id="fa9ec-116">= B2</span></span>

<span data-ttu-id="fa9ec-117">下表显示成本对象的计算结果。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="fa9ec-118">您可以在 **成本对象** 页面上查看结果。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="fa9ec-119">对象类型</span><span class="sxs-lookup"><span data-stu-id="fa9ec-119">Object type</span></span></th>
<th><span data-ttu-id="fa9ec-120">物料编号</span><span class="sxs-lookup"><span data-stu-id="fa9ec-120">Item number</span></span></th>
<th><span data-ttu-id="fa9ec-121">站点</span><span class="sxs-lookup"><span data-stu-id="fa9ec-121">Site</span></span></th>
<th><span data-ttu-id="fa9ec-122">数量</span><span class="sxs-lookup"><span data-stu-id="fa9ec-122">Quantity</span></span></th>
<th><span data-ttu-id="fa9ec-123">库存单位</span><span class="sxs-lookup"><span data-stu-id="fa9ec-123">Inventory unit</span></span></th>
<th><span data-ttu-id="fa9ec-124">值</span><span class="sxs-lookup"><span data-stu-id="fa9ec-124">Value</span></span></th>
<th><span data-ttu-id="fa9ec-125">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="fa9ec-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa9ec-126">成本对象</span><span class="sxs-lookup"><span data-stu-id="fa9ec-126">Cost object</span></span></td>
<td><span data-ttu-id="fa9ec-127">A</span><span class="sxs-lookup"><span data-stu-id="fa9ec-127">A</span></span></td>
<td><span data-ttu-id="fa9ec-128">1</span><span class="sxs-lookup"><span data-stu-id="fa9ec-128">1</span></span></td>
<td><span data-ttu-id="fa9ec-129">150</span><span class="sxs-lookup"><span data-stu-id="fa9ec-129">150</span></span></td>
<td><span data-ttu-id="fa9ec-130">时间单位</span><span class="sxs-lookup"><span data-stu-id="fa9ec-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="fa9ec-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="fa9ec-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fa9ec-133">下表显示库存对象的计算结果。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="fa9ec-134">您可以通过在 **成本对象** 页面上单击 **实际数量** 来查看结果。</span><span class="sxs-lookup"><span data-stu-id="fa9ec-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="fa9ec-135">对象类型</span><span class="sxs-lookup"><span data-stu-id="fa9ec-135">Object type</span></span></th>
<th><span data-ttu-id="fa9ec-136">物料编号</span><span class="sxs-lookup"><span data-stu-id="fa9ec-136">Item number</span></span></th>
<th><span data-ttu-id="fa9ec-137">站点</span><span class="sxs-lookup"><span data-stu-id="fa9ec-137">Site</span></span></th>
<th><span data-ttu-id="fa9ec-138">仓库</span><span class="sxs-lookup"><span data-stu-id="fa9ec-138">Warehouse</span></span></th>
<th><span data-ttu-id="fa9ec-139">批号</span><span class="sxs-lookup"><span data-stu-id="fa9ec-139">Batch No.</span></span></th>
<th><span data-ttu-id="fa9ec-140">数量</span><span class="sxs-lookup"><span data-stu-id="fa9ec-140">Quantity</span></span></th>
<th><span data-ttu-id="fa9ec-141">库存单位</span><span class="sxs-lookup"><span data-stu-id="fa9ec-141">Inventory unit</span></span></th>
<th><span data-ttu-id="fa9ec-142">值</span><span class="sxs-lookup"><span data-stu-id="fa9ec-142">Value</span></span></th>
<th><span data-ttu-id="fa9ec-143">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="fa9ec-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa9ec-144">库存对象</span><span class="sxs-lookup"><span data-stu-id="fa9ec-144">Inventory object</span></span></td>
<td><span data-ttu-id="fa9ec-145">A</span><span class="sxs-lookup"><span data-stu-id="fa9ec-145">A</span></span></td>
<td><span data-ttu-id="fa9ec-146">1</span><span class="sxs-lookup"><span data-stu-id="fa9ec-146">1</span></span></td>
<td><span data-ttu-id="fa9ec-147">11</span><span class="sxs-lookup"><span data-stu-id="fa9ec-147">11</span></span></td>
<td><span data-ttu-id="fa9ec-148">B1</span><span class="sxs-lookup"><span data-stu-id="fa9ec-148">B1</span></span></td>
<td><span data-ttu-id="fa9ec-149">100</span><span class="sxs-lookup"><span data-stu-id="fa9ec-149">100</span></span></td>
<td><span data-ttu-id="fa9ec-150">时间单位</span><span class="sxs-lookup"><span data-stu-id="fa9ec-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="fa9ec-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="fa9ec-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa9ec-153">库存对象</span><span class="sxs-lookup"><span data-stu-id="fa9ec-153">Inventory object</span></span></td>
<td><span data-ttu-id="fa9ec-154">A</span><span class="sxs-lookup"><span data-stu-id="fa9ec-154">A</span></span></td>
<td><span data-ttu-id="fa9ec-155">1</span><span class="sxs-lookup"><span data-stu-id="fa9ec-155">1</span></span></td>
<td><span data-ttu-id="fa9ec-156">11</span><span class="sxs-lookup"><span data-stu-id="fa9ec-156">11</span></span></td>
<td><span data-ttu-id="fa9ec-157">B2</span><span class="sxs-lookup"><span data-stu-id="fa9ec-157">B2</span></span></td>
<td><span data-ttu-id="fa9ec-158">50</span><span class="sxs-lookup"><span data-stu-id="fa9ec-158">50</span></span></td>
<td><span data-ttu-id="fa9ec-159">时间单位</span><span class="sxs-lookup"><span data-stu-id="fa9ec-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="fa9ec-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="fa9ec-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="fa9ec-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="fa9ec-162">其他资源</span><span class="sxs-lookup"><span data-stu-id="fa9ec-162">Additional resources</span></span>
--------

[<span data-ttu-id="fa9ec-163">成本对象</span><span class="sxs-lookup"><span data-stu-id="fa9ec-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="fa9ec-164">成本条目</span><span class="sxs-lookup"><span data-stu-id="fa9ec-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="fa9ec-165">新增功能和更改的功能</span><span class="sxs-lookup"><span data-stu-id="fa9ec-165">What's new and changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]