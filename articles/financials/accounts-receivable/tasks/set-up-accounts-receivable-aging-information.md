--- 
title: "设置并生成应收账款的帐龄信息"
description: "本指南将帮助您设置帐龄期间定义、帐龄客户余额以及查看“帐龄余额表”和“收款”页的余额。"
author: mikefalkner
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 47402c31ac24f4276288e8957911d30ae98b5643
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="31277-103">设置并生成应收账款的帐龄信息</span><span class="sxs-lookup"><span data-stu-id="31277-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31277-104">本指南将帮助您设置帐龄期间定义、帐龄客户余额以及查看“帐龄余额表”和“收款”页的余额。</span><span class="sxs-lookup"><span data-stu-id="31277-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="31277-105">此记录使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="31277-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="31277-106">创建帐龄期间定义</span><span class="sxs-lookup"><span data-stu-id="31277-106">Create an aging period definition</span></span>
1. <span data-ttu-id="31277-107">转到“贷记和收款”>“设置”>“帐龄期间定义”。</span><span class="sxs-lookup"><span data-stu-id="31277-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="31277-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="31277-108">Click New.</span></span>
3. <span data-ttu-id="31277-109">在“帐龄期间定义”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="31277-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="31277-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="31277-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31277-111">单击下列“添加”按钮插入新的帐龄期间。</span><span class="sxs-lookup"><span data-stu-id="31277-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="31277-112">在“期间”字段中，输入在帐龄分析表中显示的描述。</span><span class="sxs-lookup"><span data-stu-id="31277-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="31277-113">在“单位”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="31277-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="31277-114">在“间隔”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="31277-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="31277-115">分类帐期间与您的分类帐日历期间匹配。</span><span class="sxs-lookup"><span data-stu-id="31277-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="31277-116">日、周、月、季度和年份定义日期类型的间隔范围。</span><span class="sxs-lookup"><span data-stu-id="31277-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="31277-117">根据是否为首个或最后期间，不限量选择前一期间之前或之后的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="31277-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="31277-118">在“帐龄指示器”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="31277-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="31277-119">在网格顶部选择期间。</span><span class="sxs-lookup"><span data-stu-id="31277-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="31277-120">更新该描述以说明帐龄期间定义的最早期间。</span><span class="sxs-lookup"><span data-stu-id="31277-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="31277-121">在“期间”字段中，输入帐龄期间的新描述。</span><span class="sxs-lookup"><span data-stu-id="31277-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="31277-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="31277-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="31277-123">设置余额帐龄</span><span class="sxs-lookup"><span data-stu-id="31277-123">Age the balances</span></span>
1. <span data-ttu-id="31277-124">转到“贷记和收款”>“定期任务”>“帐龄客户余额”。</span><span class="sxs-lookup"><span data-stu-id="31277-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="31277-125">在“帐龄期间定义”字段中，选择您要创建的帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="31277-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="31277-126">您可以获取每个帐龄期间定义的有效快照。</span><span class="sxs-lookup"><span data-stu-id="31277-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="31277-127">所有客户均按默认处理。</span><span class="sxs-lookup"><span data-stu-id="31277-127">All customers are processed by default.</span></span> <span data-ttu-id="31277-128">您可以使用此选择计算单一客户池。</span><span class="sxs-lookup"><span data-stu-id="31277-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="31277-129">从交易记录中选择您将用于帐龄的日期。</span><span class="sxs-lookup"><span data-stu-id="31277-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="31277-130">为帐龄选择“截止”日期。</span><span class="sxs-lookup"><span data-stu-id="31277-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="31277-131">默认日期为今天，但是如果您将此字段更改为选定的日期，您将能够选取您想要的日期。</span><span class="sxs-lookup"><span data-stu-id="31277-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="31277-132">对于批处理，请使用今天的日期。</span><span class="sxs-lookup"><span data-stu-id="31277-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="31277-133">扩大公司范围。</span><span class="sxs-lookup"><span data-stu-id="31277-133">Expand the Company range.</span></span> <span data-ttu-id="31277-134">您可以选择加入到快照中的公司。</span><span class="sxs-lookup"><span data-stu-id="31277-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="31277-135">默认选择当前公司。</span><span class="sxs-lookup"><span data-stu-id="31277-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="31277-136">单击“确定”处理该快照。</span><span class="sxs-lookup"><span data-stu-id="31277-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="31277-137">处理需要一些时间，因此请等待滑块消失并检查消息中心的消息。</span><span class="sxs-lookup"><span data-stu-id="31277-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="31277-138">查看“帐龄余额表”和“收款”页上的余额。</span><span class="sxs-lookup"><span data-stu-id="31277-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="31277-139">转到“贷记和收款”>“收款”>“帐龄余额”。</span><span class="sxs-lookup"><span data-stu-id="31277-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="31277-140">列表页显示客户的余额。</span><span class="sxs-lookup"><span data-stu-id="31277-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="31277-141">帐龄图标显示最早交易记录的帐龄期间。</span><span class="sxs-lookup"><span data-stu-id="31277-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="31277-142">选择一位有余额的客户。</span><span class="sxs-lookup"><span data-stu-id="31277-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="31277-143">展开“帐龄速见表”区域，以查看帐龄余额。</span><span class="sxs-lookup"><span data-stu-id="31277-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="31277-144">速见表的帐龄期间定义取自参数中设定的默认帐龄期间。</span><span class="sxs-lookup"><span data-stu-id="31277-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="31277-145">您可以使用“收集”菜单进行更改。</span><span class="sxs-lookup"><span data-stu-id="31277-145">You can change it using the Collect menu.</span></span>  


