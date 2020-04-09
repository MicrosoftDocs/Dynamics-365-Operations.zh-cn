---
title: 将过帐日记帐条目记入日记帐
description: 该过程显示如何将过帐的日记帐条目记入日记帐。
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145044"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="c8bed-103">将过帐日记帐条目记入日记帐</span><span class="sxs-lookup"><span data-stu-id="c8bed-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8bed-104">该过程显示如何将过帐的日记帐条目记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="c8bed-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="c8bed-105">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="c8bed-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="c8bed-106">在**导航窗格**中，转到**模块 > 总帐 > 分类帐设置 > 总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="c8bed-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="c8bed-107">可将**扩展分类日记帐**字段设置为“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="c8bed-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="c8bed-108">如果设置为“是”，报表输出将不同。</span><span class="sxs-lookup"><span data-stu-id="c8bed-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="c8bed-109">选择如果尚未运行日记帐分录流程时是否可关闭期间。</span><span class="sxs-lookup"><span data-stu-id="c8bed-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="c8bed-110">如果此选项设置为“是”，则完成期间的日记帐分录流程之前，不能关闭该期间。</span><span class="sxs-lookup"><span data-stu-id="c8bed-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="c8bed-111">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c8bed-111">Close the page.</span></span>
5. <span data-ttu-id="c8bed-112">在**导航窗格**中，转到**模块 > 总帐 > 定期任务 > 日记帐分录**。</span><span class="sxs-lookup"><span data-stu-id="c8bed-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="c8bed-113">单击**筛选器**。</span><span class="sxs-lookup"><span data-stu-id="c8bed-113">Click **Filter**.</span></span>
7. <span data-ttu-id="c8bed-114">突出显示带有要定义的筛选条件的行。</span><span class="sxs-lookup"><span data-stu-id="c8bed-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="c8bed-115">在**条件**字段中，输入或选择筛选条件。</span><span class="sxs-lookup"><span data-stu-id="c8bed-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="c8bed-116">单击**确定**以关闭“筛选”页面。</span><span class="sxs-lookup"><span data-stu-id="c8bed-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="c8bed-117">单击**确定**开始日记帐分录过程。</span><span class="sxs-lookup"><span data-stu-id="c8bed-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="c8bed-118">此流程完成之后将生成一个报告。</span><span class="sxs-lookup"><span data-stu-id="c8bed-118">A report will be generated after the process is complete.</span></span>  

