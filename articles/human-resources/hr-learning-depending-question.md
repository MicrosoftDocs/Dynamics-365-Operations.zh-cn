---
title: 根据前一个问题的回答设定问题依赖项
description: 有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67dac872d6dc3a5046f5d554b1f185aa6607d193
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5114996"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="08758-103">根据前一个问题的回答设定问题依赖项</span><span class="sxs-lookup"><span data-stu-id="08758-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="08758-104">有条件问题允许您根据前一问题的回答，指定向回答者显示哪些后续问题。</span><span class="sxs-lookup"><span data-stu-id="08758-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="08758-105">例如，如果您提问“您喜欢喝咖啡还是茶”，可以根据回答者选择的是咖啡还是茶来确定逻辑后续问题。</span><span class="sxs-lookup"><span data-stu-id="08758-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="08758-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="08758-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="08758-107">找到现有的调查表</span><span class="sxs-lookup"><span data-stu-id="08758-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="08758-108">转到“调查表”>“设计”>“调查表”。</span><span class="sxs-lookup"><span data-stu-id="08758-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="08758-109">在列表中，选择 WorkFH 调查表。</span><span class="sxs-lookup"><span data-stu-id="08758-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="08758-110">添加所有问题和子问题到调查表中</span><span class="sxs-lookup"><span data-stu-id="08758-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="08758-111">单击问题。</span><span class="sxs-lookup"><span data-stu-id="08758-111">Click Questions.</span></span>
2. <span data-ttu-id="08758-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="08758-112">Click New.</span></span>
3. <span data-ttu-id="08758-113">在“问题”字段中，选择问题编号 00016。</span><span class="sxs-lookup"><span data-stu-id="08758-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="08758-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="08758-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="08758-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="08758-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="08758-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="08758-116">Click Save.</span></span>
7. <span data-ttu-id="08758-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="08758-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="08758-118">设置有条件问题的调查表顺序，并使问题依赖于相应问题</span><span class="sxs-lookup"><span data-stu-id="08758-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="08758-119">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="08758-119">Click Edit.</span></span>
2. <span data-ttu-id="08758-120">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="08758-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="08758-121">在“问题顺序”字段中，选择“有条件”。</span><span class="sxs-lookup"><span data-stu-id="08758-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="08758-122">单击“有条件问题”。</span><span class="sxs-lookup"><span data-stu-id="08758-122">Click Conditional question.</span></span>
5. <span data-ttu-id="08758-123">在树结构中，选择“问题\说明为什么以这种方式回答前一问题”。</span><span class="sxs-lookup"><span data-stu-id="08758-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="08758-124">在“主要问题”字段中，选择问题编号 00009</span><span class="sxs-lookup"><span data-stu-id="08758-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="08758-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="08758-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="08758-126">在“回答”字段中，输入您所希望的依赖项的回答选项的序列 ID。</span><span class="sxs-lookup"><span data-stu-id="08758-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="08758-127">例如，在第一个回答选项中输入 1。</span><span class="sxs-lookup"><span data-stu-id="08758-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="08758-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="08758-128">Click Save.</span></span>
10. <span data-ttu-id="08758-129">在树结构中，选择“问题\我获得公平的工作报酬”。</span><span class="sxs-lookup"><span data-stu-id="08758-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="08758-130">请注意，问题树已更新以显示差异。</span><span class="sxs-lookup"><span data-stu-id="08758-130">Note that the question tree updated to show the dependency.</span></span>  

