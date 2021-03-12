---
title: 在物料对于工作单元可用时准备处理看板作业
description: 此任务的重点是在所有物料可用于工作单元时准备处理看板作业。
author: johanhoffmann
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
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12773cc6d94a34197084c8fe12c90167d4dca62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977755"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="7c3aa-103">在物料对于工作单元可用时准备处理看板作业</span><span class="sxs-lookup"><span data-stu-id="7c3aa-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c3aa-104">此任务的重点是在所有物料可用于工作单元时准备处理看板作业。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="7c3aa-105">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7c3aa-106">此过程是专为机器操作员设计的。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="7c3aa-107">转到“处理作业的看板面板”。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="7c3aa-108">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7c3aa-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7c3aa-110">选择工作单元 1250，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="7c3aa-111">在列表中，选择第 4 行 。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="7c3aa-112">在演示公司中，第 4 行的看板 000329 是第一个作业，且未完成。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="7c3aa-113">切换“领料单”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="7c3aa-114">验证领料单上的所有物料均可有供应状态。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="7c3aa-115">如果选中多个作业，领料单将显示所选作业所需的所有物料的总和。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="7c3aa-116">单击“准备”。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-116">Click Prepare.</span></span>
    * <span data-ttu-id="7c3aa-117">准备流程现在已完成。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-117">The preparation process is now completed.</span></span> <span data-ttu-id="7c3aa-118">物料单中选中所有行的复选框指示供应状态为已领料。</span><span class="sxs-lookup"><span data-stu-id="7c3aa-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

