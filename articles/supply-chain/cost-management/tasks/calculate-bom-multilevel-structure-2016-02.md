--- 
title: "通过使用多级结构计算 BOM（仅限 2016 年 2 月）"
description: "此过程显示如何通过使用“成本计算单”中的多级分解计算成品的成本。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a><span data-ttu-id="4bd22-103">通过使用多级结构计算 BOM（仅限 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="4bd22-103">Calculate a BOM by using a multilevel structure (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bd22-104">此过程显示如何通过使用“成本计算单”中的多级分解计算成品的成本。</span><span class="sxs-lookup"><span data-stu-id="4bd22-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="4bd22-105">这是 BOM 计算系列中的第七个任务。</span><span class="sxs-lookup"><span data-stu-id="4bd22-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="4bd22-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="4bd22-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4bd22-107">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4bd22-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4bd22-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4bd22-109">选择产品 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="4bd22-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="4bd22-110">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="4bd22-111">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-111">Click Item price.</span></span>
5. <span data-ttu-id="4bd22-112">单击“计算物料成本”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="4bd22-113">可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。</span><span class="sxs-lookup"><span data-stu-id="4bd22-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="4bd22-114">在“成本计算版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4bd22-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="4bd22-115">选择“成本计算版本 20”，因为其“计划成本类型和分解模式”为“多级”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="4bd22-116">多级分解模式用于计划成本和模拟。</span><span class="sxs-lookup"><span data-stu-id="4bd22-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="4bd22-117">它不用于标准成本。</span><span class="sxs-lookup"><span data-stu-id="4bd22-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="4bd22-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-118">Click OK.</span></span>
8. <span data-ttu-id="4bd22-119">单击“查看计算明细”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-119">Click View calculation details.</span></span>
    * <span data-ttu-id="4bd22-120">可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。</span><span class="sxs-lookup"><span data-stu-id="4bd22-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="4bd22-121">在这种情况下，请注意 BOM_2 的计算考虑了原材料、流程和开销，所以总计为 29,40，而不是此系列中初始任务指南内激活的标准成本 10。</span><span class="sxs-lookup"><span data-stu-id="4bd22-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="4bd22-122">单击“成本计算单”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4bd22-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="4bd22-123">我们转到“成本计算单”选项卡，这里的单位成本组总计与上一个任务指南中完成的计算相比有所不同。</span><span class="sxs-lookup"><span data-stu-id="4bd22-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="4bd22-124">在“级别”字段中选择“多”。</span><span class="sxs-lookup"><span data-stu-id="4bd22-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="4bd22-125">如果选择“多”，则成本根据 BOM_2 的构成,归类，其中的 10 源自 M1 成本组 (ITEM_C)，15,60 源自其制造（成本组为 L2 的情况下）。</span><span class="sxs-lookup"><span data-stu-id="4bd22-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="4bd22-126">间接成本也会不同。</span><span class="sxs-lookup"><span data-stu-id="4bd22-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="4bd22-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4bd22-127">Close the page.</span></span>
12. <span data-ttu-id="4bd22-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4bd22-128">Close the page.</span></span>

