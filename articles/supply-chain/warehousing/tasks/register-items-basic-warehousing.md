---
title: 使用物料到达日记帐登记启用的基础仓库物料
description: 此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec8c1912435cf822db6eaecc5fff3dbcac793f77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977054"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="65b19-103">使用物料到达日记帐登记启用的基础仓库物料</span><span class="sxs-lookup"><span data-stu-id="65b19-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65b19-104">此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。</span><span class="sxs-lookup"><span data-stu-id="65b19-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="65b19-105">这将通常由一个收料员完成。</span><span class="sxs-lookup"><span data-stu-id="65b19-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="65b19-106">您可以使用所示的示例值运行 USMF 公司演示数据的过程。</span><span class="sxs-lookup"><span data-stu-id="65b19-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="65b19-107">如果您没有使用 USMF，则在开始本指南前，您需要使用未结采购订单行以确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="65b19-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="65b19-108">必须贮存行中的物料。</span><span class="sxs-lookup"><span data-stu-id="65b19-108">The item on the line must be stocked.</span></span> <span data-ttu-id="65b19-109">而且物料需与存储维度组进行关联，其站点和仓库是有效的。</span><span class="sxs-lookup"><span data-stu-id="65b19-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="65b19-110">创建物料到达日记帐标题</span><span class="sxs-lookup"><span data-stu-id="65b19-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="65b19-111">转到“库存管理”>“日记帐条目”>“物料到达”>“物料到达”。</span><span class="sxs-lookup"><span data-stu-id="65b19-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="65b19-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="65b19-112">Click New.</span></span>
3. <span data-ttu-id="65b19-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="65b19-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="65b19-114">如果您正在使用 USMF，可以键入 WHS。</span><span class="sxs-lookup"><span data-stu-id="65b19-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="65b19-115">如果您正在使用其他数据，您选择的日记帐名称必须具有以下属性：“检查领料库位”必须设置为“否”，以及“检验管理”必须设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="65b19-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="65b19-116">在“装箱单”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="65b19-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="65b19-117">它是来自供应商签发的装箱单的 ID。</span><span class="sxs-lookup"><span data-stu-id="65b19-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="65b19-118">添加唯一编号。</span><span class="sxs-lookup"><span data-stu-id="65b19-118">Add a unique number.</span></span>  
5. <span data-ttu-id="65b19-119">在“数字”字段中，在“数字”字段中，选择采购订单..</span><span class="sxs-lookup"><span data-stu-id="65b19-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="65b19-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="65b19-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="65b19-121">添加行至物料到达日记帐</span><span class="sxs-lookup"><span data-stu-id="65b19-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="65b19-122">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="65b19-122">Click Functions.</span></span>
2. <span data-ttu-id="65b19-123">单击“创建行”。</span><span class="sxs-lookup"><span data-stu-id="65b19-123">Click Create lines.</span></span>
    * <span data-ttu-id="65b19-124">行可以手动输入到此日记帐中或自动创建。</span><span class="sxs-lookup"><span data-stu-id="65b19-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="65b19-125">它将显示您如何自动创建此字段。</span><span class="sxs-lookup"><span data-stu-id="65b19-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="65b19-126">选中或取消选中“初始化数量”复选框。</span><span class="sxs-lookup"><span data-stu-id="65b19-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="65b19-127">这将用采购订单行未登记的数量初始化日记帐行上的数量。</span><span class="sxs-lookup"><span data-stu-id="65b19-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="65b19-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="65b19-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="65b19-129">过帐日记帐</span><span class="sxs-lookup"><span data-stu-id="65b19-129">Post the journal</span></span>
1. <span data-ttu-id="65b19-130">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="65b19-130">Click Post.</span></span>
2. <span data-ttu-id="65b19-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="65b19-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="65b19-132">生成产品收据</span><span class="sxs-lookup"><span data-stu-id="65b19-132">Generate the product receipt</span></span>
1. <span data-ttu-id="65b19-133">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="65b19-133">Click Functions.</span></span>
2. <span data-ttu-id="65b19-134">单击“产品收据”。</span><span class="sxs-lookup"><span data-stu-id="65b19-134">Click Product receipt.</span></span>
3. <span data-ttu-id="65b19-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="65b19-135">Click OK.</span></span>

