---
title: 创建采购订单的产品包装
description: 此程序会逐步演示如何创建产品包装，以及在采购订单上使用它。
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e1fd19c6a27739ce9f57a4ab33f61e6baaeb2e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021735"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="ed2ad-103">创建采购订单的产品包装</span><span class="sxs-lookup"><span data-stu-id="ed2ad-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ed2ad-104">此程序会逐步演示如何创建产品包装，以及在采购订单上使用它。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="ed2ad-105">采购订单将被用于创建预定义集合产品的订单。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="ed2ad-106">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="ed2ad-107">创建产品包装</span><span class="sxs-lookup"><span data-stu-id="ed2ad-107">Create a product package</span></span>
1. <span data-ttu-id="ed2ad-108">转至“Retail 和 Commerce”>“库存管理”>“补货”>“产品包装”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="ed2ad-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-109">Click New.</span></span>
3. <span data-ttu-id="ed2ad-110">在“包装编号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="ed2ad-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ed2ad-112">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ed2ad-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ed2ad-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-114">Click Add.</span></span>
8. <span data-ttu-id="ed2ad-115">在“物料编号”字段中，输入“0160”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="ed2ad-116">在“尺寸”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ed2ad-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ed2ad-118">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="ed2ad-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-119">Click Add.</span></span>
13. <span data-ttu-id="ed2ad-120">在“物料编号”字段中，输入“0160”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="ed2ad-121">在“变型编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ed2ad-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ed2ad-123">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="ed2ad-124">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-124">Click Add.</span></span>
18. <span data-ttu-id="ed2ad-125">在“物料编号”字段中，输入“0175”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="ed2ad-126">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="ed2ad-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-127">Click Save.</span></span>
21. <span data-ttu-id="ed2ad-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="ed2ad-129">将包装添加到采购订单</span><span class="sxs-lookup"><span data-stu-id="ed2ad-129">Add package to purchase order</span></span>
1. <span data-ttu-id="ed2ad-130">转到“应付账款”>“采购订单”>“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ed2ad-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-131">Click New.</span></span>
3. <span data-ttu-id="ed2ad-132">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ed2ad-133">如果已选定一个供应商，则在列表中，选择以前曾为其创建产品包装的同一供应商。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="ed2ad-134">切换“概况”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="ed2ad-135">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ed2ad-136">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ed2ad-137">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ed2ad-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ed2ad-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-139">Click OK.</span></span>
11. <span data-ttu-id="ed2ad-140">切换“行详细信息”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="ed2ad-141">单击“产品包装”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="ed2ad-142">单击“采购订单行”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="ed2ad-143">单击“从包装中创建行”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="ed2ad-144">在列表中，查找并选择在上一步中创建的产品包装。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="ed2ad-145">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="ed2ad-146">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-146">Click Create.</span></span>
18. <span data-ttu-id="ed2ad-147">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-147">Click Save.</span></span>
