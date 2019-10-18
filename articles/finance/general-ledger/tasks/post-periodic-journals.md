---
title: 过帐期间日记帐
description: 定期日记帐有时称作循环日记帐，因为这些数额、文本和其他信息每次均会在检索定期日记帐时重复出现。
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fdf630e9d292d0e016b6624a82b047d32bab898
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175312"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="4de3a-103">过帐期间日记帐</span><span class="sxs-lookup"><span data-stu-id="4de3a-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4de3a-104">定期日记帐有时称作循环日记帐，因为这些数额、文本和其他信息每次均会在检索定期日记帐时重复出现。</span><span class="sxs-lookup"><span data-stu-id="4de3a-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="4de3a-105">当您创建定期日记帐时，您需要指定循环的间隔周期，如天或月。</span><span class="sxs-lookup"><span data-stu-id="4de3a-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="4de3a-106">此任务指南将创建一个以月为周期的定期日记帐。</span><span class="sxs-lookup"><span data-stu-id="4de3a-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="4de3a-107">转到**导航窗格 > 模块 > 总帐 > 定期任务 > 定期日记帐**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="4de3a-108">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-108">Click **New**.</span></span>
3. <span data-ttu-id="4de3a-109">在**名称**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="4de3a-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4de3a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4de3a-111">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="4de3a-112">日后检索时，该描述将为期间日记帐的名称，因此请确保指定一个相关名称。</span><span class="sxs-lookup"><span data-stu-id="4de3a-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="4de3a-113">在**操作窗格**上，单击**行**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="4de3a-114">期间日记帐一般包含多个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="4de3a-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="4de3a-115">但是此任务向导只能添加一行。</span><span class="sxs-lookup"><span data-stu-id="4de3a-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="4de3a-116">在**日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="4de3a-117">**日期**字段包含日志账簿里下次交易的过账日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="4de3a-118">对于每个月均将检索的日记帐，建议过帐时采用当月日期，一般是期间的开始或结束日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="4de3a-119">也可以将“日期”字段留空，并在检索日记帐时通过“空白日期”字段指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="4de3a-120">检索交易记录时，该字段会自动更新为下一轮日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="4de3a-121">在**帐户**字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="4de3a-122">在**描述**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="4de3a-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4de3a-123">Close the page.</span></span>
11. <span data-ttu-id="4de3a-124">在**借方**字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="4de3a-125">在**抵销帐户**字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="4de3a-126">在**单位**字段中，选择“月”。</span><span class="sxs-lookup"><span data-stu-id="4de3a-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="4de3a-127">在**单位数量**字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="4de3a-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="4de3a-128">在**最后日期**字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="4de3a-129">在上一个期间输入结束日期会避免在错误的开始期间错误地创建循环日记帐。</span><span class="sxs-lookup"><span data-stu-id="4de3a-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="4de3a-130">最后日期将会在每次检索期间日记帐之后得到更新。</span><span class="sxs-lookup"><span data-stu-id="4de3a-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="4de3a-131">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-131">Click **Save**.</span></span>
17. <span data-ttu-id="4de3a-132">转到**导航窗格 > 模块 > 总帐 > 日记帐条目 > 普通日记帐**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="4de3a-133">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-133">Click **New**.</span></span>
19. <span data-ttu-id="4de3a-134">在**名称**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="4de3a-135">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4de3a-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="4de3a-136">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4de3a-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="4de3a-137">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="4de3a-138">在**操作窗格**上，单击**行**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="4de3a-139">在**操作窗格**中，单击**期间日记帐**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="4de3a-140">单击**检索日记帐**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="4de3a-141">在**结束日期**字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="4de3a-142">**结束日期**是指周期凭证行的截止日期。</span><span class="sxs-lookup"><span data-stu-id="4de3a-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="4de3a-143">基于周期设置，同一行的“最后日期”和“结束日期”可能会多次出现在结果日记帐中。</span><span class="sxs-lookup"><span data-stu-id="4de3a-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="4de3a-144">结束日期将会根据定期行转移到日记帐的最后会话日期进行自动更新。</span><span class="sxs-lookup"><span data-stu-id="4de3a-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="4de3a-145">在**定期日记帐编号**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="4de3a-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="4de3a-146">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4de3a-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="4de3a-147">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4de3a-147">Click **OK**.</span></span> <span data-ttu-id="4de3a-148">定期日记帐可以根据需求和设置进行检查、审核或过帐。</span><span class="sxs-lookup"><span data-stu-id="4de3a-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
