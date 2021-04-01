---
title: 转移仓库内的实际库存
description: 该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b745308aca2503b31d7d24d7cac693bb803fc6ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244247"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="57f56-103">转移仓库内的实际库存</span><span class="sxs-lookup"><span data-stu-id="57f56-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57f56-104">该过程向您介绍创建和过帐库存转移日记帐，以登记物料在仓库内的库位转移。</span><span class="sxs-lookup"><span data-stu-id="57f56-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="57f56-105">在您开始该过程前，您需要为库存转移设置库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="57f56-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="57f56-106">您可以使用所示的示例值或者使用您自己的数据（如果有产品和库位设置）在该过程中用演示数据公司 USMF 运行。</span><span class="sxs-lookup"><span data-stu-id="57f56-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="57f56-107">这些任务通常由仓库员工完成。</span><span class="sxs-lookup"><span data-stu-id="57f56-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="57f56-108">创建库存转移日记帐</span><span class="sxs-lookup"><span data-stu-id="57f56-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="57f56-109">在 **导航窗格** 中，转到 **库存管理 > 日记帐条目 > 物料 > 转移**。</span><span class="sxs-lookup"><span data-stu-id="57f56-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="57f56-110">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="57f56-110">Click **New**.</span></span>
3. <span data-ttu-id="57f56-111">在 **名称** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="57f56-112">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="57f56-112">Click **OK**.</span></span> <span data-ttu-id="57f56-113">这是指定每一日记帐行的“开始”和“结束”维度的选项。</span><span class="sxs-lookup"><span data-stu-id="57f56-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="57f56-114">这些对于日记帐类型十分重要。</span><span class="sxs-lookup"><span data-stu-id="57f56-114">These are essential for this journal type.</span></span> <span data-ttu-id="57f56-115">您可以使用不同规则将物料转移到库位。</span><span class="sxs-lookup"><span data-stu-id="57f56-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="57f56-116">在此示例中，我们将相同仓库内的物料从受牌照控制的库位转移到不受牌照控制的库位。</span><span class="sxs-lookup"><span data-stu-id="57f56-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="57f56-117">创建日记帐行</span><span class="sxs-lookup"><span data-stu-id="57f56-117">Create journal lines</span></span>
1. <span data-ttu-id="57f56-118">在 **日记帐行** 快速选项卡上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="57f56-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="57f56-119">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="57f56-120">如果您正在使用 USMF，可以选择“A0001”。</span><span class="sxs-lookup"><span data-stu-id="57f56-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="57f56-121">在 **源站点** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="57f56-122">如果您正在使用 USMF，可以选择“2”。</span><span class="sxs-lookup"><span data-stu-id="57f56-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="57f56-123">在 **目标站点** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="57f56-124">如果您正在使用 USMF，可以选择“2”。</span><span class="sxs-lookup"><span data-stu-id="57f56-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="57f56-125">在 **源仓库** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="57f56-126">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="57f56-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="57f56-127">在 **目标仓库** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="57f56-128">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="57f56-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="57f56-129">在 **源库位** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="57f56-130">如果您正在使用 USMF，可以选择“FL-001”。</span><span class="sxs-lookup"><span data-stu-id="57f56-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="57f56-131">在 **目标库位** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="57f56-132">如果您正在使用 USMF，可以选择“散装-001”。</span><span class="sxs-lookup"><span data-stu-id="57f56-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="57f56-133">在 **数量** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="57f56-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="57f56-134">在 **行明细** 快速选项卡上，单击 **库存维度** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="57f56-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="57f56-135">在 **源库存维度** 的 **牌照** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="57f56-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="57f56-136">如果您正在使用 USMF，可以选择“24”。</span><span class="sxs-lookup"><span data-stu-id="57f56-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="57f56-137">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="57f56-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="57f56-138">过帐库存转移日记帐</span><span class="sxs-lookup"><span data-stu-id="57f56-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="57f56-139">在 **操作窗格** 上，单击 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="57f56-139">On the **Action Pane**, click **Post**.</span></span>
2. <span data-ttu-id="57f56-140">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="57f56-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="57f56-141">查看库存交易记录</span><span class="sxs-lookup"><span data-stu-id="57f56-141">View inventory transactions</span></span>
1. <span data-ttu-id="57f56-142">单击 **库存**。</span><span class="sxs-lookup"><span data-stu-id="57f56-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="57f56-143">单击 **交易记录**。</span><span class="sxs-lookup"><span data-stu-id="57f56-143">Click **Transactions**.</span></span> <span data-ttu-id="57f56-144">在这里，您可以查看过帐日记帐时创建的交易记录。</span><span class="sxs-lookup"><span data-stu-id="57f56-144">Here you can see the transactions that were created when you posted your journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]