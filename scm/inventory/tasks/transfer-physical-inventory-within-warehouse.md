---
title: "转移仓库内的实际库存"
description: "该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="809a9-103">转移仓库内的实际库存</span><span class="sxs-lookup"><span data-stu-id="809a9-103">Transfer physical inventory within the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="809a9-104">该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。</span><span class="sxs-lookup"><span data-stu-id="809a9-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="809a9-105">在您开始该过程前，您需要为库存转移设置库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="809a9-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="809a9-106">您可以使用所示的示例值或者使用您自己的数据（如果有产品和库位设置）在该过程中用演示数据公司 USMF 运行。</span><span class="sxs-lookup"><span data-stu-id="809a9-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="809a9-107">这些任务通常由仓库员工完成。</span><span class="sxs-lookup"><span data-stu-id="809a9-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="809a9-108">创建库存转移日记帐</span><span class="sxs-lookup"><span data-stu-id="809a9-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="809a9-109">转到“转移”。</span><span class="sxs-lookup"><span data-stu-id="809a9-109">Go to Transfer.</span></span>
2. <span data-ttu-id="809a9-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="809a9-110">Click New.</span></span>
3. <span data-ttu-id="809a9-111">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="809a9-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="809a9-112">Click OK.</span></span>
    * <span data-ttu-id="809a9-113">这是指定每一日记帐行的“开始”和“结束”维度的选项。</span><span class="sxs-lookup"><span data-stu-id="809a9-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="809a9-114">这些对于日记帐类型十分重要。</span><span class="sxs-lookup"><span data-stu-id="809a9-114">These are essential for this journal type.</span></span> <span data-ttu-id="809a9-115">您可以使用不同规则将物料转移到库位。</span><span class="sxs-lookup"><span data-stu-id="809a9-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="809a9-116">在此示例中，我们将相同仓库内的物料从受牌照控制的库位转移到不受牌照控制的库位。</span><span class="sxs-lookup"><span data-stu-id="809a9-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="809a9-117">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="809a9-117">Create journal lines</span></span>
1. <span data-ttu-id="809a9-118">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="809a9-118">Click New.</span></span>
2. <span data-ttu-id="809a9-119">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-120">如果您正在使用 USMF，可以选择“A0001”。</span><span class="sxs-lookup"><span data-stu-id="809a9-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="809a9-121">在“源站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-122">如果您正在使用 USMF，可以选择“2”。</span><span class="sxs-lookup"><span data-stu-id="809a9-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="809a9-123">在“目标站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-124">如果您正在使用 USMF，可以选择“2”。</span><span class="sxs-lookup"><span data-stu-id="809a9-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="809a9-125">在“源仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-126">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="809a9-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="809a9-127">在“目标仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-128">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="809a9-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="809a9-129">在“源库位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-130">如果您正在使用 USMF，可以选择“FL-001”。</span><span class="sxs-lookup"><span data-stu-id="809a9-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="809a9-131">在“目标库位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-132">如果您正在使用 USMF，可以选择“散装-001”。</span><span class="sxs-lookup"><span data-stu-id="809a9-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="809a9-133">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="809a9-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="809a9-134">单击“库存维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="809a9-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="809a9-135">在“牌照”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="809a9-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="809a9-136">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="809a9-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="809a9-137">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="809a9-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="809a9-138">过帐库存转移日记帐</span><span class="sxs-lookup"><span data-stu-id="809a9-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="809a9-139">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="809a9-139">Click Post.</span></span>
2. <span data-ttu-id="809a9-140">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="809a9-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="809a9-141">查看库存交易记录</span><span class="sxs-lookup"><span data-stu-id="809a9-141">View inventory transactions</span></span>
1. <span data-ttu-id="809a9-142">单击“库存”。</span><span class="sxs-lookup"><span data-stu-id="809a9-142">Click Inventory.</span></span>
2. <span data-ttu-id="809a9-143">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="809a9-143">Click Transactions.</span></span>
    * <span data-ttu-id="809a9-144">在这里，您可以查看过帐日记帐时创建的交易记录。</span><span class="sxs-lookup"><span data-stu-id="809a9-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

