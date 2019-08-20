---
title: 调整仓库中的库存级别（基本仓库）
description: 该过程向您介绍创建和过帐库存调整日记帐以调整仓库中的产品库存水平。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 450e95d8a4d5a216b84a3c944c6c63b4a8ad10c5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838815"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="1e059-103">调整仓库中的库存级别（基本仓库）</span><span class="sxs-lookup"><span data-stu-id="1e059-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e059-104">该过程向您介绍创建和过帐库存调整日记帐以调整仓库中的产品库存水平。</span><span class="sxs-lookup"><span data-stu-id="1e059-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="1e059-105">在开始前，您需要为库存调整设置一个库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="1e059-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="1e059-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="1e059-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="1e059-107">这些任务通常由仓库员工完成。</span><span class="sxs-lookup"><span data-stu-id="1e059-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="1e059-108">创建一个库存调整日记帐</span><span class="sxs-lookup"><span data-stu-id="1e059-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="1e059-109">转到“库存管理”>“日记帐条目”>“物料”>“库存调整”。</span><span class="sxs-lookup"><span data-stu-id="1e059-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="1e059-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1e059-110">Click New.</span></span>
3. <span data-ttu-id="1e059-111">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1e059-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1e059-112">在列表中，单击您要使用的库存调整日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="1e059-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="1e059-113">其他一些字段将根据您所选择的库存调整日记帐名称的设置填充数据。</span><span class="sxs-lookup"><span data-stu-id="1e059-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="1e059-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1e059-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="1e059-115">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="1e059-115">Create journal lines</span></span>
1. <span data-ttu-id="1e059-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1e059-116">Click New.</span></span>
2. <span data-ttu-id="1e059-117">在列表中，标记该物料编号字段。</span><span class="sxs-lookup"><span data-stu-id="1e059-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="1e059-118">在“物料编号”字段中，选择一个物料。</span><span class="sxs-lookup"><span data-stu-id="1e059-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="1e059-119">如果您使用演示数据公司 USMF，键入 "D0001"。</span><span class="sxs-lookup"><span data-stu-id="1e059-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="1e059-120">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="1e059-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1e059-121">在列表中，选择一个站点。</span><span class="sxs-lookup"><span data-stu-id="1e059-121">In the list, select a site.</span></span>
6. <span data-ttu-id="1e059-122">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="1e059-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1e059-123">在列表中，选择一个仓库。</span><span class="sxs-lookup"><span data-stu-id="1e059-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="1e059-124">如果您选择了一个强制性库存维度物料，就必须在此指定该库位。</span><span class="sxs-lookup"><span data-stu-id="1e059-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="1e059-125">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="1e059-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1e059-126">成本价格字段详细说明了库存收入每个单元的成本。</span><span class="sxs-lookup"><span data-stu-id="1e059-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="1e059-127">如果该物料数目的成本没有指定，或者需要手动更改，请在此输入。</span><span class="sxs-lookup"><span data-stu-id="1e059-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="1e059-128">验证并过帐库存调整日记帐</span><span class="sxs-lookup"><span data-stu-id="1e059-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="1e059-129">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="1e059-129">Click Validate.</span></span>
2. <span data-ttu-id="1e059-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1e059-130">Click OK.</span></span>
3. <span data-ttu-id="1e059-131">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="1e059-131">Click Post.</span></span>
    * <span data-ttu-id="1e059-132">过帐此类日记帐时，将过帐库存收货或发货单，更改库存水平及其值，同时生成分类帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="1e059-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="1e059-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1e059-133">Click OK.</span></span>
5. <span data-ttu-id="1e059-134">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="1e059-134">Close the form.</span></span>
6. <span data-ttu-id="1e059-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1e059-135">Close the page.</span></span>

