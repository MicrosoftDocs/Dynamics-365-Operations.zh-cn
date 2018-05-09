--- 
title: "通过使用单级结构计算 BOM（仅限 2016 年 2 月）"
description: "此过程显示如何通过使用“成本计算单”中的单级分解计算成品的成本。"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a318b2308f8cd5c3650a392aed53185df6f81dc
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="d2813-103">通过使用单级结构计算 BOM（仅限 2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="d2813-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2813-104">此过程显示如何通过使用“成本计算单”中的单级分解计算成品的成本。</span><span class="sxs-lookup"><span data-stu-id="d2813-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="d2813-105">这是 BOM 计算系列中的第六个任务。</span><span class="sxs-lookup"><span data-stu-id="d2813-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="d2813-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="d2813-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="d2813-107">转至“产品发布”。</span><span class="sxs-lookup"><span data-stu-id="d2813-107">Go to Released products.</span></span>
2. <span data-ttu-id="d2813-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d2813-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2813-109">选择产品 BOM_1。</span><span class="sxs-lookup"><span data-stu-id="d2813-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="d2813-110">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="d2813-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="d2813-111">单击“物料价格”。</span><span class="sxs-lookup"><span data-stu-id="d2813-111">Click Item price.</span></span>
5. <span data-ttu-id="d2813-112">单击“计算物料成本”。</span><span class="sxs-lookup"><span data-stu-id="d2813-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="d2813-113">可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。</span><span class="sxs-lookup"><span data-stu-id="d2813-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="d2813-114">在“成本计算版本”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="d2813-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d2813-115">在这个演示中选择“10”。</span><span class="sxs-lookup"><span data-stu-id="d2813-115">For this demo, select 10.</span></span> <span data-ttu-id="d2813-116">这是用于向组件添加成本价的同一个成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="d2813-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="d2813-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d2813-117">Click OK.</span></span>
8. <span data-ttu-id="d2813-118">单击“查看计算明细”。</span><span class="sxs-lookup"><span data-stu-id="d2813-118">Click View calculation details.</span></span>
    * <span data-ttu-id="d2813-119">可能需要单击省略号 (...) 才能在顶部菜单中看到此选项。</span><span class="sxs-lookup"><span data-stu-id="d2813-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="d2813-120">下面是成本的构成：  •    10 源于 ITEM_A，10 源于 ITEM_B，10 源于 BOM_2。</span><span class="sxs-lookup"><span data-stu-id="d2813-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="d2813-121">在此示例中，BOM_2 无详细信息，因为它是作为标准成本 10 输入的，未经计算。</span><span class="sxs-lookup"><span data-stu-id="d2813-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="d2813-122">•  7 源自设置时间，这是固定成本，7 源自运行时操作（流程）。</span><span class="sxs-lookup"><span data-stu-id="d2813-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="d2813-123">•   还有其他一些与间接成本对应的金额。</span><span class="sxs-lookup"><span data-stu-id="d2813-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


