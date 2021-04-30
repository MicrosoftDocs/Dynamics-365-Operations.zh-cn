---
title: 成本对象
description: 本文提供有关成本对象的信息，并说明如何累计成本和数量。 成本对象是为其累计成本和数量的实体。 成本对象实体可以是产品或产品变型，例如样式和颜色的变型。
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6829f24b8efa29b39f5ed742d8ca99e09bcef01
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910345"
---
# <a name="cost-objects"></a><span data-ttu-id="1782e-105">成本对象</span><span class="sxs-lookup"><span data-stu-id="1782e-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1782e-106">本文提供有关成本对象的信息，并说明如何累计成本和数量。</span><span class="sxs-lookup"><span data-stu-id="1782e-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="1782e-107">成本对象是为其累计成本和数量的实体。</span><span class="sxs-lookup"><span data-stu-id="1782e-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="1782e-108">成本对象实体可以是产品或产品变型，例如样式和颜色的变型。</span><span class="sxs-lookup"><span data-stu-id="1782e-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="1782e-109">成本对象</span><span class="sxs-lookup"><span data-stu-id="1782e-109">Cost objects</span></span>

<span data-ttu-id="1782e-110">**成本对象** 页面列出在某个产品上登记的所有成本对象。</span><span class="sxs-lookup"><span data-stu-id="1782e-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="1782e-111">成本对象由来自以下源的数据定义：</span><span class="sxs-lookup"><span data-stu-id="1782e-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="1782e-112">产品</span><span class="sxs-lookup"><span data-stu-id="1782e-112">Product</span></span>
-   <span data-ttu-id="1782e-113">产品维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-113">Product dimension group</span></span>
-   <span data-ttu-id="1782e-114">存储维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-114">Storage dimension group</span></span>
-   <span data-ttu-id="1782e-115">跟踪维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-115">Tracking dimension group</span></span>

<span data-ttu-id="1782e-116">**注意：** 成本对象仅表示 **直接材料** 类型的成本元素。</span><span class="sxs-lookup"><span data-stu-id="1782e-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="1782e-117">成本对象和库存对象在为财务库存所选的库存维度定义成本对象的方式上存在差异。</span><span class="sxs-lookup"><span data-stu-id="1782e-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="1782e-118">例如，某个物料具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="1782e-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="1782e-119">**站点：** Physical inventory = Yes, Financial inventory = Yes</span><span class="sxs-lookup"><span data-stu-id="1782e-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="1782e-120">**仓库：** Physical inventory = Yes, Financial inventory = No</span><span class="sxs-lookup"><span data-stu-id="1782e-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="1782e-121">**批号：** Physical inventory = Yes, Financial inventory = No</span><span class="sxs-lookup"><span data-stu-id="1782e-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="1782e-122">下表显示了成本对象和库存对象的定义。</span><span class="sxs-lookup"><span data-stu-id="1782e-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="1782e-123">对象类型</span><span class="sxs-lookup"><span data-stu-id="1782e-123">Object type</span></span>      | <span data-ttu-id="1782e-124">物料编号</span><span class="sxs-lookup"><span data-stu-id="1782e-124">Item number</span></span> | <span data-ttu-id="1782e-125">站点</span><span class="sxs-lookup"><span data-stu-id="1782e-125">Site</span></span> | <span data-ttu-id="1782e-126">仓库</span><span class="sxs-lookup"><span data-stu-id="1782e-126">Warehouse</span></span> | <span data-ttu-id="1782e-127">批号</span><span class="sxs-lookup"><span data-stu-id="1782e-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="1782e-128">成本对象</span><span class="sxs-lookup"><span data-stu-id="1782e-128">Cost object</span></span>      | <span data-ttu-id="1782e-129"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-129">x</span></span>           | <span data-ttu-id="1782e-130"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-130">x</span></span>    |           |           |
| <span data-ttu-id="1782e-131">库存对象</span><span class="sxs-lookup"><span data-stu-id="1782e-131">Inventory object</span></span> | <span data-ttu-id="1782e-132"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-132">x</span></span>           | <span data-ttu-id="1782e-133"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-133">x</span></span>    |  <span data-ttu-id="1782e-134"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-134">x</span></span>        | <span data-ttu-id="1782e-135"> x</span><span class="sxs-lookup"><span data-stu-id="1782e-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="1782e-136">成本和数量的累计</span><span class="sxs-lookup"><span data-stu-id="1782e-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="1782e-137">**值** 字段中的值为以下值的和：</span><span class="sxs-lookup"><span data-stu-id="1782e-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="1782e-138">实际成本额</span><span class="sxs-lookup"><span data-stu-id="1782e-138">Physical cost amount</span></span>
    -   <span data-ttu-id="1782e-139">财务成本额</span><span class="sxs-lookup"><span data-stu-id="1782e-139">Financial cost amount</span></span>
    -   <span data-ttu-id="1782e-140">调整</span><span class="sxs-lookup"><span data-stu-id="1782e-140">Adjustments</span></span>
-   <span data-ttu-id="1782e-141">**数量** 字段中的值为以下值的和：</span><span class="sxs-lookup"><span data-stu-id="1782e-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="1782e-142">已接收</span><span class="sxs-lookup"><span data-stu-id="1782e-142">Received</span></span>
    -   <span data-ttu-id="1782e-143">已扣除</span><span class="sxs-lookup"><span data-stu-id="1782e-143">Deducted</span></span>
    -   <span data-ttu-id="1782e-144">已过帐的数量</span><span class="sxs-lookup"><span data-stu-id="1782e-144">Posted quantity</span></span>
-   <span data-ttu-id="1782e-145">**平均单位成本** 字段为计算字段。</span><span class="sxs-lookup"><span data-stu-id="1782e-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="1782e-146">该值通过用 **值** 值除以 **数量** 值得出。</span><span class="sxs-lookup"><span data-stu-id="1782e-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="1782e-147">**注意：** **包括实际成本** 参数不影响之前的计算。</span><span class="sxs-lookup"><span data-stu-id="1782e-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1782e-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="1782e-148">Additional resources</span></span>
--------

[<span data-ttu-id="1782e-149">产品维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-149">Product dimension group</span></span>](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[<span data-ttu-id="1782e-150">存储维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-150">Storage dimension group</span></span>](/dynamicsax-2012//storage-dimension-groups-form)

[<span data-ttu-id="1782e-151">跟踪维度组</span><span class="sxs-lookup"><span data-stu-id="1782e-151">Tracking dimension group</span></span>](/dynamicsax-2012//tracking-dimension-groups-form)

[<span data-ttu-id="1782e-152">新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="1782e-152">What's new or changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="1782e-153">成本条目</span><span class="sxs-lookup"><span data-stu-id="1782e-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]