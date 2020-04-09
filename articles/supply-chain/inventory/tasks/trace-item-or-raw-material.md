---
title: 跟踪物料或原材料
description: 该过程演示如何使用物料跟踪确定使用或正在使用物料或原材料的位置。
author: pjacobse
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba64093dfe9ca28108456641ad17b5eda23d7f49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148196"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="8a6d5-103">跟踪物料或原材料</span><span class="sxs-lookup"><span data-stu-id="8a6d5-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a6d5-104">该过程演示如何使用物料跟踪确定使用或正在使用物料或原材料的位置。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="8a6d5-105">通过该过程，您可以确定物料，跟踪其来源，然后继续跟踪其生产和成品销售。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="8a6d5-106">该流程可用于调查受影响客户和订单以及其他信息。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="8a6d5-107">该过程使用演示数据公司 USP2。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="8a6d5-108">使用已知批次编号倒推跟踪物料</span><span class="sxs-lookup"><span data-stu-id="8a6d5-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="8a6d5-109">在**导航窗格**中，转到**模块 > 库存管理 > 查询和报表 > 跟踪维度 > 物料跟踪**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="8a6d5-110">在**物料编号**字段中，选择“P9100”。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="8a6d5-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8a6d5-112">在**正推或倒推**字段中，选择“倒推”。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="8a6d5-113">在**批处理号**字段中，选择“as-12-344-01”。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="8a6d5-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8a6d5-115">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="8a6d5-116">标识物料，正推跟踪，然后进行分析</span><span class="sxs-lookup"><span data-stu-id="8a6d5-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="8a6d5-117">树形图的顶部节点表示所选物料和批次的现有量。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="8a6d5-118">您需要展开树形图结点以查找应对其执行正向跟踪的物料。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="8a6d5-119">在树结构中，展开“下面介绍的节点，然后选择最后一个节点”。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="8a6d5-120">展开：“P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● 已领料 ● 销售订单 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● 站点=1，仓库=10，批处理号=as-12-344-01  \P9100 ● 生产 B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● 站点=1，仓库=10，批处理号=as-12-344-01 ● 联产品：P9101”，然后选择该节点。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="8a6d5-121">在树结构中，展开“下面介绍的节点，然后选择该节点”。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="8a6d5-122">从您刚才选择的节点开始，展开“M9103 ● 生产订单行 B-000050 ● 12/9/2015  ● -160.00 lb ● 尺寸=70，颜色=OK，站点=1，仓库=10，批处理号=App01”，然后选择该节点。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="8a6d5-123">单击**从节点跟踪**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="8a6d5-124">单击**正推**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-124">Click **Forward**.</span></span>
5. <span data-ttu-id="8a6d5-125">在**操作窗格**上单击**跟踪**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="8a6d5-126">具有若干跟踪选项，提供有关受您跟踪的物料影响的客户的信息，以及与已装运和尚未装运的物料相关的销售订单的信息。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="8a6d5-127">单击**客户**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-127">Click **Customers**.</span></span>
7. <span data-ttu-id="8a6d5-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-128">Close the page.</span></span>
8. <span data-ttu-id="8a6d5-129">在**操作窗格**上单击**跟踪**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="8a6d5-130">单击**装运的销售订单**。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="8a6d5-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8a6d5-131">Close the page.</span></span>

