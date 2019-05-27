---
title: 更正库存跟踪信息
description: 该过程让您了解创建和过帐库存转移日志的流程，以纠正库存跟踪信息。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549909"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="e38d5-103">更正库存跟踪信息</span><span class="sxs-lookup"><span data-stu-id="e38d5-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e38d5-104">该过程让您了解创建和过帐库存转移日志的流程，以纠正库存跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="e38d5-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="e38d5-105">在此示例中，我们通过将不正确登记的批更新为其他批，来更新批控制物料的信息。</span><span class="sxs-lookup"><span data-stu-id="e38d5-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="e38d5-106">您可以使用演示数据公司 USPI 或您自己的数据了解该过程。</span><span class="sxs-lookup"><span data-stu-id="e38d5-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="e38d5-107">如果您使用您自己的数据，需启用可以批处理的物料；并且它不能是位置控制。</span><span class="sxs-lookup"><span data-stu-id="e38d5-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="e38d5-108">您还需要有一个为库存转移而设置的库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="e38d5-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="e38d5-109">这些任务通常由仓库员工完成。</span><span class="sxs-lookup"><span data-stu-id="e38d5-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e38d5-110">创建库存转移日记帐</span><span class="sxs-lookup"><span data-stu-id="e38d5-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e38d5-111">转到“转移”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-111">Go to Transfer.</span></span>
2. <span data-ttu-id="e38d5-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-112">Click New.</span></span>
3. <span data-ttu-id="e38d5-113">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e38d5-114">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="e38d5-115">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="e38d5-115">Create journal lines</span></span>
1. <span data-ttu-id="e38d5-116">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-116">Click New.</span></span>
2. <span data-ttu-id="e38d5-117">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e38d5-118">如果您正在使用 USPI，请选择物料 M5003。</span><span class="sxs-lookup"><span data-stu-id="e38d5-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="e38d5-119">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e38d5-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="e38d5-120">单击“库存维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="e38d5-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="e38d5-121">在“批号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="e38d5-122">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="e38d5-123">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="e38d5-124">在“批号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e38d5-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="e38d5-125">过帐日记帐</span><span class="sxs-lookup"><span data-stu-id="e38d5-125">Post the journal</span></span>
1. <span data-ttu-id="e38d5-126">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-126">Click Post.</span></span>
2. <span data-ttu-id="e38d5-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="e38d5-128">检查跟踪信息</span><span class="sxs-lookup"><span data-stu-id="e38d5-128">Check tracing information</span></span>
1. <span data-ttu-id="e38d5-129">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-129">Click Inventory.</span></span>
2. <span data-ttu-id="e38d5-130">单击“跟踪“。</span><span class="sxs-lookup"><span data-stu-id="e38d5-130">Click Trace.</span></span>
3. <span data-ttu-id="e38d5-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-131">Click OK.</span></span>
    * <span data-ttu-id="e38d5-132">使用此跟踪信息，您可以返回跟踪您从哪个批中更正库存。</span><span class="sxs-lookup"><span data-stu-id="e38d5-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="e38d5-133">您还可以使用“物料跟踪页”以查看此信息。</span><span class="sxs-lookup"><span data-stu-id="e38d5-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="e38d5-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e38d5-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="e38d5-135">检查库存交易记录</span><span class="sxs-lookup"><span data-stu-id="e38d5-135">Check inventory transactions</span></span>
1. <span data-ttu-id="e38d5-136">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-136">Click Inventory.</span></span>
2. <span data-ttu-id="e38d5-137">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="e38d5-137">Click Transactions.</span></span>
    * <span data-ttu-id="e38d5-138">在这里，您可以查看过帐日记帐时创建的交易记录。</span><span class="sxs-lookup"><span data-stu-id="e38d5-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

