---
title: 根据前一个问题的回答设定问题依赖项
description: 有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e49ee4dd1f2d4a5af3112d27eaf8d697904d2487
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538483"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="f7b5a-103">根据前一个问题的回答设定问题依赖项</span><span class="sxs-lookup"><span data-stu-id="f7b5a-103">Make a question dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7b5a-104">有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="f7b5a-105">例如，如果您提问“您喜欢喝咖啡还是茶”，可以根据回答者选择的是咖啡还是茶来确定逻辑后续问题。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="f7b5a-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="f7b5a-107">找到现有的调查表</span><span class="sxs-lookup"><span data-stu-id="f7b5a-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="f7b5a-108">转到“调查表”>“设计”>“调查表”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="f7b5a-109">在列表中，选择 WorkFH 调查表。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="f7b5a-110">添加所有问题和子问题到调查表中</span><span class="sxs-lookup"><span data-stu-id="f7b5a-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="f7b5a-111">单击问题。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-111">Click Questions.</span></span>
2. <span data-ttu-id="f7b5a-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-112">Click New.</span></span>
3. <span data-ttu-id="f7b5a-113">在“问题”字段中，选择问题编号 00016。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="f7b5a-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f7b5a-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f7b5a-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-116">Click Save.</span></span>
7. <span data-ttu-id="f7b5a-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="f7b5a-118">设置有条件问题的调查表顺序，并使问题依赖于相应问题</span><span class="sxs-lookup"><span data-stu-id="f7b5a-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="f7b5a-119">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-119">Click Edit.</span></span>
2. <span data-ttu-id="f7b5a-120">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="f7b5a-121">在“问题顺序”字段中，选择“有条件”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="f7b5a-122">单击“有条件问题”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-122">Click Conditional question.</span></span>
5. <span data-ttu-id="f7b5a-123">在树结构中，选择“问题\说明为什么以这种方式回答前一问题”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="f7b5a-124">在“主要问题”字段中，选择问题编号 00009</span><span class="sxs-lookup"><span data-stu-id="f7b5a-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="f7b5a-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f7b5a-126">在“回答”字段中，输入您所希望的依赖项的回答选项的序列 ID。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="f7b5a-127">例如，在第一个回答选项中输入 1。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="f7b5a-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-128">Click Save.</span></span>
10. <span data-ttu-id="f7b5a-129">在树结构中，选择“问题\我获得公平的工作报酬”。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="f7b5a-130">请注意，问题树已更新以显示差异。</span><span class="sxs-lookup"><span data-stu-id="f7b5a-130">Note that the question tree updated to show the dependency.</span></span>  

