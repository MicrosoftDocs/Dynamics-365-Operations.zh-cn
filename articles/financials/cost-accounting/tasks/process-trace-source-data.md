--- 
title: "处理和跟踪源数据"
description: "所有数据处理通过作业运行。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d7470c53c3fe48e4adb584847dbb3b7dc931e578
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="ea87e-103">处理和跟踪源数据</span><span class="sxs-lookup"><span data-stu-id="ea87e-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea87e-104">所有数据处理通过作业运行。</span><span class="sxs-lookup"><span data-stu-id="ea87e-104">All data processing is run by jobs.</span></span> <span data-ttu-id="ea87e-105">将为每个作业和数据提供方创建一个日记帐，用于记录已运行流程，以及条目是在当前作业中处理的。</span><span class="sxs-lookup"><span data-stu-id="ea87e-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="ea87e-106">此过程用于设置数据源，然后跟踪特定成本条目的来源。</span><span class="sxs-lookup"><span data-stu-id="ea87e-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="ea87e-107">此录制使用 USP2 演示数据公司 USP2。</span><span class="sxs-lookup"><span data-stu-id="ea87e-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="ea87e-108">完成此任务之前，确保播放以下任务指南：“创建成本核算分类帐”、“定义成本控制单元”和“管理成本核算分类帐的数据源”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="ea87e-109">转到“成本核算”>“分类帐设置”>“成本核算分类帐”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="ea87e-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ea87e-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ea87e-111">选择前面创建的成本核算分类帐。</span><span class="sxs-lookup"><span data-stu-id="ea87e-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="ea87e-112">单击“实际版本”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-112">Click Actual versions.</span></span>
4. <span data-ttu-id="ea87e-113">在操作窗格上，单击“源数据处理”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="ea87e-114">单击“总帐条目转移日记帐”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="ea87e-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ea87e-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ea87e-116">单击“日记帐条目”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-116">Click Journal entries.</span></span>
8. <span data-ttu-id="ea87e-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="ea87e-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ea87e-118">单击“成本条目”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-118">Click Cost entries.</span></span>
10. <span data-ttu-id="ea87e-119">单击“源条目”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-119">Click Source entry.</span></span>
11. <span data-ttu-id="ea87e-120">在操作窗格上，单击“源数据处理”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="ea87e-121">单击“总帐”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-121">Click General ledger.</span></span>
13. <span data-ttu-id="ea87e-122">在“会计日历期间”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea87e-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="ea87e-123">在此示例中，选择“2017 年会计期间 9”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="ea87e-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ea87e-124">Click OK.</span></span>


