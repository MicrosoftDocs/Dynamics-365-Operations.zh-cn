---
title: 盘点仓库中的库存
description: 本主题介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e9457074b696efaf5958b3a3b4616f06f5a6ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145747"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="e40f2-103">盘点仓库中的库存</span><span class="sxs-lookup"><span data-stu-id="e40f2-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e40f2-104">本主题介绍创建和过帐库存盘点日记帐，以盘点仓库一个库位的特定物料的步骤。</span><span class="sxs-lookup"><span data-stu-id="e40f2-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="e40f2-105">该过程适用于“基础仓储”功能，在库存管理模块可用，在仓库管理模块的仓储功能不可用。</span><span class="sxs-lookup"><span data-stu-id="e40f2-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="e40f2-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="e40f2-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="e40f2-107">如果您使用自己的数据，确保您有产品和库位设置，并且您为盘点日记帐创建了库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="e40f2-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="e40f2-108">库存盘点通常由仓管人员执行。</span><span class="sxs-lookup"><span data-stu-id="e40f2-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="e40f2-109">创建库存盘点日记帐</span><span class="sxs-lookup"><span data-stu-id="e40f2-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="e40f2-110">转到**导航窗格 > 模块 > 库存管理 > 日记帐条目 > 物料盘点 > 盘点**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="e40f2-111">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-111">Select **New**.</span></span>
3. <span data-ttu-id="e40f2-112">在**名称**字段中，从下拉列表选择要使用的库存盘点日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="e40f2-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="e40f2-113">将根据您选择的库存盘点日记帐的设置填充一些其他字段。</span><span class="sxs-lookup"><span data-stu-id="e40f2-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="e40f2-114">在**工人**字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e40f2-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e40f2-115">在列表中，**选择**您想要使用的工人。</span><span class="sxs-lookup"><span data-stu-id="e40f2-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="e40f2-116">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="e40f2-117">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="e40f2-117">Create journal lines</span></span>
1. <span data-ttu-id="e40f2-118">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-118">Select **New**.</span></span>
2. <span data-ttu-id="e40f2-119">在**物料编号**字段中，从下拉列表选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="e40f2-120">如果您使用演示数据公司 USMF，选择 **A0001**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="e40f2-121">在**站点**字段中，从下拉列表选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="e40f2-122">如果您使用演示数据公司 USMF，选择站点 **2**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="e40f2-123">在**仓库**字段中，从下拉列表选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="e40f2-124">如果您使用演示数据公司 USMF，请选择仓库 **24**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="e40f2-125">在**位置**字段中，从下拉列表选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="e40f2-126">如果您使用演示数据公司 USMF，选择 **散装-001**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="e40f2-127">在“已盘点”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e40f2-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="e40f2-128">如果您输入的盘点数字与**现有量**字段显示的数字不同，**数量**字段会更新此差异。</span><span class="sxs-lookup"><span data-stu-id="e40f2-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="e40f2-129">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="e40f2-130">过帐库存盘点日记帐</span><span class="sxs-lookup"><span data-stu-id="e40f2-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="e40f2-131">选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-131">Select **Post**.</span></span> <span data-ttu-id="e40f2-132">在您过帐库存盘点日记帐时，如果盘点数与**现有量**字段报告的数额不同，会过帐库存收货或问题，更改库存水平和价值和生成分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="e40f2-133">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e40f2-134">查看库存交易记录</span><span class="sxs-lookup"><span data-stu-id="e40f2-134">View inventory transactions</span></span>
1. <span data-ttu-id="e40f2-135">选择**库存**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="e40f2-136">选择**交易记录**。</span><span class="sxs-lookup"><span data-stu-id="e40f2-136">Select **Transactions**.</span></span> <span data-ttu-id="e40f2-137">在这里，您可以查看过帐库存盘点日记帐时创建的所有相关交易记录。</span><span class="sxs-lookup"><span data-stu-id="e40f2-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

