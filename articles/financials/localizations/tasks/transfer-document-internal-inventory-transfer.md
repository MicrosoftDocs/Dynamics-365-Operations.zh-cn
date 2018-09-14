--- 
title: "为内部库存转移生成转移文档"
description: "此过程显示如何为公司内货物转移创建转移单据。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4b9ef0026129d958b4214bb6e235c288de023d10
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="100d2-103">为内部库存转移生成转移文档</span><span class="sxs-lookup"><span data-stu-id="100d2-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="100d2-104">此过程显示如何为公司内货物转移创建转移单据。</span><span class="sxs-lookup"><span data-stu-id="100d2-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="100d2-105">此过程仅适用于主地址在立陶宛的法人。</span><span class="sxs-lookup"><span data-stu-id="100d2-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="100d2-106">此过程所用的演示数据公司为“DEMF“，其主要地址在立陶宛。</span><span class="sxs-lookup"><span data-stu-id="100d2-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="100d2-107">必须先完成“为公司内的货物转移设置转移单据”过程，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="100d2-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="100d2-108">该过程是专为库存会计师设计的。</span><span class="sxs-lookup"><span data-stu-id="100d2-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="100d2-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="100d2-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="100d2-110">创建转移单</span><span class="sxs-lookup"><span data-stu-id="100d2-110">Create a transfer order</span></span>
1. <span data-ttu-id="100d2-111">转到“库存管理”>“入站订单”>“转移单”。</span><span class="sxs-lookup"><span data-stu-id="100d2-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="100d2-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="100d2-112">Click New.</span></span>
3. <span data-ttu-id="100d2-113">在“源仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="100d2-114">在“目标仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="100d2-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="100d2-115">Click Add.</span></span>
6. <span data-ttu-id="100d2-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="100d2-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="100d2-117">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="100d2-118">输入转移单的运输详细信息</span><span class="sxs-lookup"><span data-stu-id="100d2-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="100d2-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="100d2-119">Click Save.</span></span>
2. <span data-ttu-id="100d2-120">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="100d2-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="100d2-121">单击“运输详细信息”。</span><span class="sxs-lookup"><span data-stu-id="100d2-121">Click Transportation details.</span></span>
4. <span data-ttu-id="100d2-122">在“打印运输详细信息”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="100d2-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="100d2-123">在“货物签发者”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="100d2-124">在“包装”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="100d2-125">在“负荷风险级别”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="100d2-126">在“承运人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="100d2-127">在“型号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="100d2-128">在“登记编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="100d2-129">在“装运人登记编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="100d2-130">在“驾驶员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="100d2-131">在“驾驶员名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="100d2-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="100d2-132">Click Save.</span></span>
15. <span data-ttu-id="100d2-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="100d2-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="100d2-134">查看未过帐转移单的装箱单</span><span class="sxs-lookup"><span data-stu-id="100d2-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="100d2-135">单击“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="100d2-135">Click Packing slip.</span></span>
2. <span data-ttu-id="100d2-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="100d2-136">Click OK.</span></span>
3. <span data-ttu-id="100d2-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="100d2-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="100d2-138">查看已过帐转移单的装箱单</span><span class="sxs-lookup"><span data-stu-id="100d2-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="100d2-139">在操作窗格上单击“转移单”。</span><span class="sxs-lookup"><span data-stu-id="100d2-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="100d2-140">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="100d2-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="100d2-141">单击“装运转移单”。</span><span class="sxs-lookup"><span data-stu-id="100d2-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="100d2-142">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="100d2-142">Click the General tab.</span></span>
5. <span data-ttu-id="100d2-143">在“更新”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="100d2-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="100d2-144">单击“概览”选项卡。</span><span class="sxs-lookup"><span data-stu-id="100d2-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="100d2-145">在“装箱单”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="100d2-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="100d2-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="100d2-146">Click OK.</span></span>
9. <span data-ttu-id="100d2-147">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="100d2-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="100d2-148">单击“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="100d2-148">Click Packing slip.</span></span>
11. <span data-ttu-id="100d2-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="100d2-149">Click OK.</span></span>


