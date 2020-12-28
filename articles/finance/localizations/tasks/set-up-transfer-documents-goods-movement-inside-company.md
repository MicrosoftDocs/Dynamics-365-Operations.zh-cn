---
title: 为公司内货物转移设置转移文档
description: 此过程显示如何为公司内货物转移创建转移单据。
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85bd359ce1053629ad4217cf623e57b2976463a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440796"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="061fd-103">为公司内货物转移设置转移文档</span><span class="sxs-lookup"><span data-stu-id="061fd-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="061fd-104">此过程显示如何为公司内货物转移创建转移单据。</span><span class="sxs-lookup"><span data-stu-id="061fd-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="061fd-105">此过程仅适用于主地址在立陶宛的法人。</span><span class="sxs-lookup"><span data-stu-id="061fd-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="061fd-106">此过程所用的演示数据公司为“DEMF“，其主要地址在立陶宛。</span><span class="sxs-lookup"><span data-stu-id="061fd-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="061fd-107">必须先完成“为公司内的货物转移设置转移单据”过程，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="061fd-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="061fd-108">该过程是专为库存会计师设计的。</span><span class="sxs-lookup"><span data-stu-id="061fd-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="061fd-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="061fd-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="061fd-110">创建转移单</span><span class="sxs-lookup"><span data-stu-id="061fd-110">Create a transfer order</span></span>
1. <span data-ttu-id="061fd-111">转到“库存管理”>“入站订单”>“转移单”。</span><span class="sxs-lookup"><span data-stu-id="061fd-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="061fd-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="061fd-112">Click New.</span></span>
3. <span data-ttu-id="061fd-113">在“源仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="061fd-114">在“目标仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="061fd-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="061fd-115">Click Add.</span></span>
6. <span data-ttu-id="061fd-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="061fd-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="061fd-117">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="061fd-118">输入转移单的运输详细信息</span><span class="sxs-lookup"><span data-stu-id="061fd-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="061fd-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="061fd-119">Click Save.</span></span>
2. <span data-ttu-id="061fd-120">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="061fd-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="061fd-121">单击“运输详细信息”。</span><span class="sxs-lookup"><span data-stu-id="061fd-121">Click Transportation details.</span></span>
4. <span data-ttu-id="061fd-122">在“打印运输详细信息”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="061fd-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="061fd-123">在“货物签发者”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="061fd-124">在“包装”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="061fd-125">在“负荷风险级别”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="061fd-126">在“承运人”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="061fd-127">在“型号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="061fd-128">在“登记编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="061fd-129">在“装运人登记编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="061fd-130">在“驾驶员”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="061fd-131">在“驾驶员名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="061fd-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="061fd-132">Click Save.</span></span>
15. <span data-ttu-id="061fd-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="061fd-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="061fd-134">查看未过帐转移单的装箱单</span><span class="sxs-lookup"><span data-stu-id="061fd-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="061fd-135">单击“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="061fd-135">Click Packing slip.</span></span>
2. <span data-ttu-id="061fd-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="061fd-136">Click OK.</span></span>
3. <span data-ttu-id="061fd-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="061fd-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="061fd-138">查看已过帐转移单的装箱单</span><span class="sxs-lookup"><span data-stu-id="061fd-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="061fd-139">在操作窗格上单击“转移单”。</span><span class="sxs-lookup"><span data-stu-id="061fd-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="061fd-140">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="061fd-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="061fd-141">单击“装运转移单”。</span><span class="sxs-lookup"><span data-stu-id="061fd-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="061fd-142">单击“常规”选项卡。</span><span class="sxs-lookup"><span data-stu-id="061fd-142">Click the General tab.</span></span>
5. <span data-ttu-id="061fd-143">在“更新”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="061fd-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="061fd-144">单击“概览”选项卡。</span><span class="sxs-lookup"><span data-stu-id="061fd-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="061fd-145">在“装箱单”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="061fd-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="061fd-146">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="061fd-146">Click OK.</span></span>
9. <span data-ttu-id="061fd-147">在操作窗格上，单击“装运”。</span><span class="sxs-lookup"><span data-stu-id="061fd-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="061fd-148">单击“装箱单”。</span><span class="sxs-lookup"><span data-stu-id="061fd-148">Click Packing slip.</span></span>
11. <span data-ttu-id="061fd-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="061fd-149">Click OK.</span></span>

