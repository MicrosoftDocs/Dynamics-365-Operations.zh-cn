--- 
title: "盘点仓库中的库存"
description: "该过程介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: cff65842f9eefb4365aaec86822173c6cfd35473
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="0eef4-103">盘点仓库中的库存</span><span class="sxs-lookup"><span data-stu-id="0eef4-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0eef4-104">该过程介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。</span><span class="sxs-lookup"><span data-stu-id="0eef4-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="0eef4-105">该过程适用于“基础仓储”功能，在库存管理模块可用，在仓库管理模块的仓储功能不可用。</span><span class="sxs-lookup"><span data-stu-id="0eef4-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="0eef4-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="0eef4-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0eef4-107">如果您使用自己的数据，确保您有产品和库位设置，并且您为盘点日记帐创建了库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="0eef4-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="0eef4-108">库存盘点通常由仓管人员执行。</span><span class="sxs-lookup"><span data-stu-id="0eef4-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="0eef4-109">创建库存盘点日记帐</span><span class="sxs-lookup"><span data-stu-id="0eef4-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="0eef4-110">转到“库存管理”>“日记帐条目”>“物料盘点”>“盘点”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="0eef4-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-111">Click New.</span></span>
3. <span data-ttu-id="0eef4-112">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0eef4-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0eef4-113">在列表中，单击您要使用的库存盘点日记帐名称</span><span class="sxs-lookup"><span data-stu-id="0eef4-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="0eef4-114">将根据您选择的库存盘点日记帐的设置填充一些其他字段。</span><span class="sxs-lookup"><span data-stu-id="0eef4-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="0eef4-115">在“工作人员”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0eef4-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0eef4-116">在列表中，选择您想要使用的工作人员。</span><span class="sxs-lookup"><span data-stu-id="0eef4-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="0eef4-117">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-117">Click Select.</span></span>
8. <span data-ttu-id="0eef4-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="0eef4-119">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="0eef4-119">Create journal lines</span></span>
1. <span data-ttu-id="0eef4-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-120">Click New.</span></span>
2. <span data-ttu-id="0eef4-121">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0eef4-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0eef4-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0eef4-123">如果您使用演示数据公司 USMF，选择“A0001”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="0eef4-124">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="0eef4-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0eef4-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0eef4-126">如果您使用演示数据公司 USMF，选择站点“2”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="0eef4-127">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0eef4-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0eef4-128">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0eef4-129">如果您使用演示数据公司 USMF，请选择仓库“24”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="0eef4-130">在“地点”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0eef4-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0eef4-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0eef4-132">如果您使用演示数据公司 USMF，选择“散装-001”</span><span class="sxs-lookup"><span data-stu-id="0eef4-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="0eef4-133">在“已盘点”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0eef4-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="0eef4-134">如果您输入的盘点数字与“现有量”字段显示的数字不同，“数量”字段会更新此差异。</span><span class="sxs-lookup"><span data-stu-id="0eef4-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="0eef4-135">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="0eef4-136">过帐库存盘点日记帐</span><span class="sxs-lookup"><span data-stu-id="0eef4-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="0eef4-137">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-137">Click Post.</span></span>
    * <span data-ttu-id="0eef4-138">在您过帐库存盘点日记帐时，如果盘点数与“现有量”字段报告的数额不同，会过帐库存收货或问题，更改库存水平和价值和生成分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="0eef4-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="0eef4-140">查看库存交易记录</span><span class="sxs-lookup"><span data-stu-id="0eef4-140">View inventory transactions</span></span>
1. <span data-ttu-id="0eef4-141">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-141">Click Inventory.</span></span>
2. <span data-ttu-id="0eef4-142">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="0eef4-142">Click Transactions.</span></span>
    * <span data-ttu-id="0eef4-143">在这里，您可以查看过帐库存盘点日记帐时创建的所有相关交易记录。</span><span class="sxs-lookup"><span data-stu-id="0eef4-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   


