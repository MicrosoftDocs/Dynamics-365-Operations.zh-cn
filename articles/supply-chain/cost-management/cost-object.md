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
ms.openlocfilehash: 4590a1c1761d72472ec681be0cc3fbd098957d42
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188504"
---
# <a name="cost-objects"></a><span data-ttu-id="07c37-105">成本对象</span><span class="sxs-lookup"><span data-stu-id="07c37-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07c37-106">本文提供有关成本对象的信息，并说明如何累计成本和数量。</span><span class="sxs-lookup"><span data-stu-id="07c37-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="07c37-107">成本对象是为其累计成本和数量的实体。</span><span class="sxs-lookup"><span data-stu-id="07c37-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="07c37-108">成本对象实体可以是产品或产品变型，例如样式和颜色的变型。</span><span class="sxs-lookup"><span data-stu-id="07c37-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="07c37-109">成本对象</span><span class="sxs-lookup"><span data-stu-id="07c37-109">Cost objects</span></span>

<span data-ttu-id="07c37-110">**成本对象** 页面列出在某个产品上登记的所有成本对象。</span><span class="sxs-lookup"><span data-stu-id="07c37-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="07c37-111">成本对象由来自以下源的数据定义：</span><span class="sxs-lookup"><span data-stu-id="07c37-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="07c37-112">产品</span><span class="sxs-lookup"><span data-stu-id="07c37-112">Product</span></span>
-   <span data-ttu-id="07c37-113">产品维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-113">Product dimension group</span></span>
-   <span data-ttu-id="07c37-114">存储维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-114">Storage dimension group</span></span>
-   <span data-ttu-id="07c37-115">跟踪维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-115">Tracking dimension group</span></span>

<span data-ttu-id="07c37-116">**注意：** 成本对象仅表示 **直接材料** 类型的成本元素。</span><span class="sxs-lookup"><span data-stu-id="07c37-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="07c37-117">成本对象和库存对象在为财务库存所选的库存维度定义成本对象的方式上存在差异。</span><span class="sxs-lookup"><span data-stu-id="07c37-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="07c37-118">例如，某个物料具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="07c37-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="07c37-119">**站点：** Physical inventory = Yes, Financial inventory = Yes</span><span class="sxs-lookup"><span data-stu-id="07c37-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="07c37-120">**仓库：** Physical inventory = Yes, Financial inventory = No</span><span class="sxs-lookup"><span data-stu-id="07c37-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="07c37-121">**批号：** Physical inventory = Yes, Financial inventory = No</span><span class="sxs-lookup"><span data-stu-id="07c37-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="07c37-122">下表显示了成本对象和库存对象的定义。</span><span class="sxs-lookup"><span data-stu-id="07c37-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="07c37-123">对象类型</span><span class="sxs-lookup"><span data-stu-id="07c37-123">Object type</span></span>      | <span data-ttu-id="07c37-124">物料编号</span><span class="sxs-lookup"><span data-stu-id="07c37-124">Item number</span></span> | <span data-ttu-id="07c37-125">站点</span><span class="sxs-lookup"><span data-stu-id="07c37-125">Site</span></span> | <span data-ttu-id="07c37-126">仓库</span><span class="sxs-lookup"><span data-stu-id="07c37-126">Warehouse</span></span> | <span data-ttu-id="07c37-127">批号</span><span class="sxs-lookup"><span data-stu-id="07c37-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="07c37-128">成本对象</span><span class="sxs-lookup"><span data-stu-id="07c37-128">Cost object</span></span>      | <span data-ttu-id="07c37-129"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-129">x</span></span>           | <span data-ttu-id="07c37-130"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-130">x</span></span>    |           |           |
| <span data-ttu-id="07c37-131">库存对象</span><span class="sxs-lookup"><span data-stu-id="07c37-131">Inventory object</span></span> | <span data-ttu-id="07c37-132"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-132">x</span></span>           | <span data-ttu-id="07c37-133"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-133">x</span></span>    |  <span data-ttu-id="07c37-134"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-134">x</span></span>        | <span data-ttu-id="07c37-135"> x</span><span class="sxs-lookup"><span data-stu-id="07c37-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="07c37-136">成本和数量的累计</span><span class="sxs-lookup"><span data-stu-id="07c37-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="07c37-137">**值** 字段中的值为以下值的和：</span><span class="sxs-lookup"><span data-stu-id="07c37-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="07c37-138">实际成本额</span><span class="sxs-lookup"><span data-stu-id="07c37-138">Physical cost amount</span></span>
    -   <span data-ttu-id="07c37-139">财务成本额</span><span class="sxs-lookup"><span data-stu-id="07c37-139">Financial cost amount</span></span>
    -   <span data-ttu-id="07c37-140">调整</span><span class="sxs-lookup"><span data-stu-id="07c37-140">Adjustments</span></span>
-   <span data-ttu-id="07c37-141">**数量** 字段中的值为以下值的和：</span><span class="sxs-lookup"><span data-stu-id="07c37-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="07c37-142">已接收</span><span class="sxs-lookup"><span data-stu-id="07c37-142">Received</span></span>
    -   <span data-ttu-id="07c37-143">已扣除</span><span class="sxs-lookup"><span data-stu-id="07c37-143">Deducted</span></span>
    -   <span data-ttu-id="07c37-144">已过帐的数量</span><span class="sxs-lookup"><span data-stu-id="07c37-144">Posted quantity</span></span>
-   <span data-ttu-id="07c37-145">**平均单位成本** 字段为计算字段。</span><span class="sxs-lookup"><span data-stu-id="07c37-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="07c37-146">该值通过用 **值** 值除以 **数量** 值得出。</span><span class="sxs-lookup"><span data-stu-id="07c37-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="07c37-147">**注意：** **包括实际成本** 参数不影响之前的计算。</span><span class="sxs-lookup"><span data-stu-id="07c37-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07c37-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="07c37-148">Additional resources</span></span>

[<span data-ttu-id="07c37-149">产品维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-149">Product dimension group</span></span>](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[<span data-ttu-id="07c37-150">存储维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-150">Storage dimension group</span></span>](/dynamicsax-2012//storage-dimension-groups-form)

[<span data-ttu-id="07c37-151">跟踪维度组</span><span class="sxs-lookup"><span data-stu-id="07c37-151">Tracking dimension group</span></span>](/dynamicsax-2012//tracking-dimension-groups-form)

[<span data-ttu-id="07c37-152">新增功能或更改的功能</span><span class="sxs-lookup"><span data-stu-id="07c37-152">What's new or changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="07c37-153">成本条目</span><span class="sxs-lookup"><span data-stu-id="07c37-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]