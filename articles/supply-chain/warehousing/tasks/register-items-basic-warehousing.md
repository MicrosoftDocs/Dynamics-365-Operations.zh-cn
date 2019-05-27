---
title: 使用物料到达日记帐登记启用的基础仓库物料
description: 此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3e8ffa6cee7742de1cd98c9c83d134b6d5e4a89
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1528790"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="2798f-103">使用物料到达日记帐登记启用的基础仓库物料</span><span class="sxs-lookup"><span data-stu-id="2798f-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2798f-104">此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。</span><span class="sxs-lookup"><span data-stu-id="2798f-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="2798f-105">这将通常由一个收料员完成。</span><span class="sxs-lookup"><span data-stu-id="2798f-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="2798f-106">您可以使用所示的示例值运行 USMF 公司演示数据的过程。</span><span class="sxs-lookup"><span data-stu-id="2798f-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="2798f-107">如果您没有使用 USMF，则在开始本指南前，您需要使用未结采购订单行以确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="2798f-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="2798f-108">必须贮存行中的物料。</span><span class="sxs-lookup"><span data-stu-id="2798f-108">The item on the line must be stocked.</span></span> <span data-ttu-id="2798f-109">而且物料需与存储维度组进行关联，其站点和仓库是有效的。</span><span class="sxs-lookup"><span data-stu-id="2798f-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="2798f-110">创建物料到达日记帐标题</span><span class="sxs-lookup"><span data-stu-id="2798f-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="2798f-111">转到“库存管理”>“日记帐条目”>“物料到达”>“物料到达”。</span><span class="sxs-lookup"><span data-stu-id="2798f-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="2798f-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2798f-112">Click New.</span></span>
3. <span data-ttu-id="2798f-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2798f-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2798f-114">如果您正在使用 USMF，可以键入 WHS。</span><span class="sxs-lookup"><span data-stu-id="2798f-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="2798f-115">如果您正在使用其他数据，您选择的日记帐名称必须具有以下属性：“检查领料库位”必须设置为“否”，以及“检验管理”必须设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="2798f-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="2798f-116">在“装箱单”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2798f-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="2798f-117">它是来自供应商签发的装箱单的 ID。</span><span class="sxs-lookup"><span data-stu-id="2798f-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="2798f-118">添加唯一编号。</span><span class="sxs-lookup"><span data-stu-id="2798f-118">Add a unique number.</span></span>  
5. <span data-ttu-id="2798f-119">在“数字”字段中，在“数字”字段中，选择采购订单..</span><span class="sxs-lookup"><span data-stu-id="2798f-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="2798f-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2798f-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="2798f-121">添加行至物料到达日记帐</span><span class="sxs-lookup"><span data-stu-id="2798f-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="2798f-122">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2798f-122">Click Functions.</span></span>
2. <span data-ttu-id="2798f-123">单击“创建行”。</span><span class="sxs-lookup"><span data-stu-id="2798f-123">Click Create lines.</span></span>
    * <span data-ttu-id="2798f-124">行可以手动输入到此日记帐中或自动创建。</span><span class="sxs-lookup"><span data-stu-id="2798f-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="2798f-125">它将显示您如何自动创建此字段。</span><span class="sxs-lookup"><span data-stu-id="2798f-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="2798f-126">选中或取消选中“初始化数量”复选框。</span><span class="sxs-lookup"><span data-stu-id="2798f-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="2798f-127">这将用采购订单行未登记的数量初始化日记帐行上的数量。</span><span class="sxs-lookup"><span data-stu-id="2798f-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="2798f-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2798f-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="2798f-129">过帐日记帐</span><span class="sxs-lookup"><span data-stu-id="2798f-129">Post the journal</span></span>
1. <span data-ttu-id="2798f-130">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="2798f-130">Click Post.</span></span>
2. <span data-ttu-id="2798f-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2798f-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="2798f-132">生成产品收据</span><span class="sxs-lookup"><span data-stu-id="2798f-132">Generate the product receipt</span></span>
1. <span data-ttu-id="2798f-133">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="2798f-133">Click Functions.</span></span>
2. <span data-ttu-id="2798f-134">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="2798f-134">Click Product receipt.</span></span>
3. <span data-ttu-id="2798f-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2798f-135">Click OK.</span></span>

