--- 
title: "将过帐日记帐条目记入日记帐"
description: "该过程显示如何将过帐的日记帐条目记入日记帐。"
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 490e9a4beda43f6e32b87792b11153c3e8e322d6
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="a0e62-103">将过帐日记帐条目记入日记帐</span><span class="sxs-lookup"><span data-stu-id="a0e62-103">Journalize posted journal entries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0e62-104">该过程显示如何将过帐的日记帐条目记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="a0e62-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="a0e62-105">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="a0e62-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="a0e62-106">在“总帐”>“分类帐设置”>“总帐参数”下验证日记帐分录的设置。</span><span class="sxs-lookup"><span data-stu-id="a0e62-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="a0e62-107">可将“扩展分类日记帐”字段设置为“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="a0e62-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="a0e62-108">如果设置为“是”，报表输出将不同。</span><span class="sxs-lookup"><span data-stu-id="a0e62-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="a0e62-109">选择如果尚未运行日记帐分录流程时是否可关闭期间。</span><span class="sxs-lookup"><span data-stu-id="a0e62-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="a0e62-110">如果此选项设置为“是”，则完成期间的日记帐分录流程之前，不能关闭该期间。</span><span class="sxs-lookup"><span data-stu-id="a0e62-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="a0e62-111">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0e62-111">Close the page.</span></span>
5. <span data-ttu-id="a0e62-112">转到总分类记账>周期性任务 >记日记账。</span><span class="sxs-lookup"><span data-stu-id="a0e62-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="a0e62-113">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="a0e62-113">Click Filter.</span></span>
7. <span data-ttu-id="a0e62-114">突出显示带有要定义的筛选条件的行。</span><span class="sxs-lookup"><span data-stu-id="a0e62-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="a0e62-115">在“条件”字段中，输入或选择筛选条件。</span><span class="sxs-lookup"><span data-stu-id="a0e62-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="a0e62-116">单击“确定”以关闭“筛选”页面。</span><span class="sxs-lookup"><span data-stu-id="a0e62-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="a0e62-117">单击“确定”开始日记帐分录过程。</span><span class="sxs-lookup"><span data-stu-id="a0e62-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="a0e62-118">此流程完成之后将生成一个报告。</span><span class="sxs-lookup"><span data-stu-id="a0e62-118">A report will be generated after the process is complete.</span></span>  


