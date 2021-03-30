---
title: 在物料对于工作单元不可用时准备处理看板作业
description: 此过程的重点是在某些物料不可用于工作单元时准备流程看板作业，因此对于从仓库领料很有必要。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 742ac97c4b730d3552f532c53409ef54320b263a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204560"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="b5696-103">在物料对于工作单元不可用时准备处理看板作业</span><span class="sxs-lookup"><span data-stu-id="b5696-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5696-104">此过程的重点是在某些物料不可用于工作单元时准备流程看板作业，因此对于从仓库领料很有必要。</span><span class="sxs-lookup"><span data-stu-id="b5696-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="b5696-105">“在物料可用时准备流程看板作业”这一过程是创建此过程的先决条件。</span><span class="sxs-lookup"><span data-stu-id="b5696-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="b5696-106">此过程是专为机器操作员设计的。</span><span class="sxs-lookup"><span data-stu-id="b5696-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="b5696-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="b5696-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b5696-108">转到“生产控制”>“看板”>“处理作业的看板面板”。</span><span class="sxs-lookup"><span data-stu-id="b5696-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="b5696-109">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="b5696-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b5696-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b5696-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b5696-111">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="b5696-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="b5696-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5696-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b5696-113">选择看板 000356。</span><span class="sxs-lookup"><span data-stu-id="b5696-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="b5696-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5696-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b5696-115">在列表中，取消选择行 4。</span><span class="sxs-lookup"><span data-stu-id="b5696-115">In the list, deselect row 4.</span></span> <span data-ttu-id="b5696-116">或者如果您未完成“在物料可用时准备流程看板作业”这一任务，请选择行 4。</span><span class="sxs-lookup"><span data-stu-id="b5696-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="b5696-117">切换“领料单”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="b5696-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="b5696-118">供应状态中的“无条目”图标指示工作单元缺少物料 P0002 的 48 ea。</span><span class="sxs-lookup"><span data-stu-id="b5696-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="b5696-119">转移物料到工作单元</span><span class="sxs-lookup"><span data-stu-id="b5696-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="b5696-120">切换“转移作业”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="b5696-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="b5696-121">使用“快速筛选”来筛选带有值“P0002”的“物料编号”字段。</span><span class="sxs-lookup"><span data-stu-id="b5696-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="b5696-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b5696-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b5696-123">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="b5696-123">Click Start.</span></span>
    * <span data-ttu-id="b5696-124">正在转换中。</span><span class="sxs-lookup"><span data-stu-id="b5696-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="b5696-125">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="b5696-125">Click Complete.</span></span>
    * <span data-ttu-id="b5696-126">物料 P0002 现在可用于看板作业的领料单。</span><span class="sxs-lookup"><span data-stu-id="b5696-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="b5696-127">这意味着我们可以为看板准备所有所需的物料。</span><span class="sxs-lookup"><span data-stu-id="b5696-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="b5696-128">单击“准备”。</span><span class="sxs-lookup"><span data-stu-id="b5696-128">Click Prepare.</span></span>
    * <span data-ttu-id="b5696-129">请注意，作业状态的图标指示作业现在可供处理。</span><span class="sxs-lookup"><span data-stu-id="b5696-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]