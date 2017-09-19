--- 
title: "过帐期间日记帐"
description: "定期日记帐有时称作循环日记帐，因为这些数额、文本和其他信息每次均会在检索定期日记帐时重复出现。"
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
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
ms.openlocfilehash: 233d145a9d3441ffc2b816b8514e58988b517136
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="49857-103">过帐期间日记帐</span><span class="sxs-lookup"><span data-stu-id="49857-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49857-104">定期日记帐有时称作循环日记帐，因为这些数额、文本和其他信息每次均会在检索定期日记帐时重复出现。</span><span class="sxs-lookup"><span data-stu-id="49857-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="49857-105">当您创建定期日记帐时，您需要指定循环的间隔周期，如天或月。</span><span class="sxs-lookup"><span data-stu-id="49857-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="49857-106">此任务指南将创建一个以月为周期的定期日记帐。</span><span class="sxs-lookup"><span data-stu-id="49857-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="49857-107">转到总分类记账>周期性任务 >周期账簿。</span><span class="sxs-lookup"><span data-stu-id="49857-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="49857-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="49857-108">Click New.</span></span>
3. <span data-ttu-id="49857-109">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="49857-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="49857-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="49857-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="49857-112">日后检索时，该描述将为期间日记帐的名称，因此请确保指定一个相关名称。</span><span class="sxs-lookup"><span data-stu-id="49857-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="49857-113">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="49857-113">Click Lines.</span></span>
    * <span data-ttu-id="49857-114">期间日记帐一般包含多个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="49857-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="49857-115">但是此任务向导只能添加一行。</span><span class="sxs-lookup"><span data-stu-id="49857-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="49857-116">在“日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="49857-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="49857-117">“日期”字段包含下次转移到日常记帐中的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="49857-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="49857-118">对于每个月均将检索的日记帐，建议过帐时采用当月日期，一般是期间的开始或结束日期。</span><span class="sxs-lookup"><span data-stu-id="49857-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="49857-119">也可以将“日期”字段留空，并在检索日记帐时通过“空白日期”字段指定一个日期。</span><span class="sxs-lookup"><span data-stu-id="49857-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="49857-120">检索交易记录时，该字段会自动更新为下一轮日期。</span><span class="sxs-lookup"><span data-stu-id="49857-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="49857-121">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="49857-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="49857-122">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="49857-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="49857-123">Close the page.</span></span>
11. <span data-ttu-id="49857-124">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="49857-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="49857-125">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="49857-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="49857-126">在“单位”字段中，选择“月”。</span><span class="sxs-lookup"><span data-stu-id="49857-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="49857-127">在“单位标号”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="49857-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="49857-128">在“最后日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="49857-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="49857-129">在上一个期间输入结束日期会避免在错误的开始期间错误地创建循环日记帐。</span><span class="sxs-lookup"><span data-stu-id="49857-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="49857-130">最后日期将会在每次检索期间日记帐之后得到更新。</span><span class="sxs-lookup"><span data-stu-id="49857-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="49857-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="49857-131">Click Save.</span></span>
17. <span data-ttu-id="49857-132">转到“默认仪表板”。</span><span class="sxs-lookup"><span data-stu-id="49857-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="49857-133">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="49857-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="49857-134">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="49857-134">Click New.</span></span>
20. <span data-ttu-id="49857-135">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="49857-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="49857-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="49857-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="49857-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="49857-138">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="49857-139">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="49857-139">Click Lines.</span></span>
25. <span data-ttu-id="49857-140">单击“定期日记帐”。</span><span class="sxs-lookup"><span data-stu-id="49857-140">Click Period journal.</span></span>
26. <span data-ttu-id="49857-141">单击“检索日记帐”。</span><span class="sxs-lookup"><span data-stu-id="49857-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="49857-142">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="49857-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="49857-143">“结束日期”是指周期凭证行的截止日期。</span><span class="sxs-lookup"><span data-stu-id="49857-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="49857-144">基于周期设置，同一行的“最后日期”和“结束日期”可能会多次出现在结果日记帐中。</span><span class="sxs-lookup"><span data-stu-id="49857-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="49857-145">结束日期将会根据定期行转移到日记帐的最后会话日期进行自动更新。</span><span class="sxs-lookup"><span data-stu-id="49857-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="49857-146">在“定期日记帐编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="49857-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="49857-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="49857-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="49857-148">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="49857-148">Click OK.</span></span>
    * <span data-ttu-id="49857-149">定期日记帐可以根据需求和设置进行检查、审核或过帐。</span><span class="sxs-lookup"><span data-stu-id="49857-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  

