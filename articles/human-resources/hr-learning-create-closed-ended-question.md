---
title: 创建封闭式问题
description: 封闭式问题允许您为回答者提供供选择的选项。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09bf57b26111be0e3de358a6c955b3df7bf50668
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467883"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="e1656-103">创建封闭式问题</span><span class="sxs-lookup"><span data-stu-id="e1656-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="e1656-104">封闭式问题允许您为回答者提供供选择的选项。</span><span class="sxs-lookup"><span data-stu-id="e1656-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="e1656-105">首先，您需要创建有回答的回答组，然后创建使用该回答组的问题。</span><span class="sxs-lookup"><span data-stu-id="e1656-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="e1656-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="e1656-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="e1656-107">创建回答组</span><span class="sxs-lookup"><span data-stu-id="e1656-107">Create an answer group</span></span>
1. <span data-ttu-id="e1656-108">转到“调查表”>“设计”>“回答组”。</span><span class="sxs-lookup"><span data-stu-id="e1656-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="e1656-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-109">Click New.</span></span>
3. <span data-ttu-id="e1656-110">在“回答组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="e1656-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e1656-112">每次将回答组用于问题时，使用随机功能以随机在不同订单中设置回答。</span><span class="sxs-lookup"><span data-stu-id="e1656-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="e1656-113">单击“回答”。</span><span class="sxs-lookup"><span data-stu-id="e1656-113">Click Answer.</span></span>
6. <span data-ttu-id="e1656-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-114">Click New.</span></span>
    * <span data-ttu-id="e1656-115">序列号控制回答显示的顺序，除非回答组已选择“随机”。</span><span class="sxs-lookup"><span data-stu-id="e1656-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="e1656-116">可规定回答项分数，以对调查表进行评分。</span><span class="sxs-lookup"><span data-stu-id="e1656-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="e1656-117">在“分数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e1656-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="e1656-118">可以标记正确答案，以指示所选答案正确。</span><span class="sxs-lookup"><span data-stu-id="e1656-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="e1656-119">这可用于对调查表进行评分。</span><span class="sxs-lookup"><span data-stu-id="e1656-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="e1656-120">在“回答”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="e1656-121">继续为回答组创建回答选项。</span><span class="sxs-lookup"><span data-stu-id="e1656-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="e1656-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-122">Click New.</span></span>
10. <span data-ttu-id="e1656-123">在“分数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e1656-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="e1656-124">在“回答”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="e1656-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-125">Click New.</span></span>
13. <span data-ttu-id="e1656-126">在“分数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e1656-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="e1656-127">在“回答”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="e1656-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-128">Click New.</span></span>
16. <span data-ttu-id="e1656-129">在“分数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e1656-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="e1656-130">在“回答”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="e1656-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-131">Click New.</span></span>
19. <span data-ttu-id="e1656-132">在“分数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e1656-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="e1656-133">在“回答”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="e1656-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e1656-134">Close the page.</span></span>
22. <span data-ttu-id="e1656-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e1656-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="e1656-136">创建问题</span><span class="sxs-lookup"><span data-stu-id="e1656-136">Create the question</span></span>
1. <span data-ttu-id="e1656-137">转到“调查表”>“设计”>“问题”。</span><span class="sxs-lookup"><span data-stu-id="e1656-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="e1656-138">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e1656-138">Click New.</span></span>
3. <span data-ttu-id="e1656-139">使用“类型”字段，以将相关问题分组。</span><span class="sxs-lookup"><span data-stu-id="e1656-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="e1656-140">您可以选择输入类型：复选框、备选按钮或封闭式问题的组合框。</span><span class="sxs-lookup"><span data-stu-id="e1656-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="e1656-141">在“输入类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="e1656-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="e1656-142">在“回答组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="e1656-143">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e1656-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]