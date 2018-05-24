---
title: "查看和评估调查表的结果"
description: "本主题介绍如何查看和评估回应者完成的调查表的结果。"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f87238b3b2f6e7cc68bf2f1a7cd3a21254f3599a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a><span data-ttu-id="e1744-103">查看和评估调查表的结果</span><span class="sxs-lookup"><span data-stu-id="e1744-103">View and evaluate the results of a questionnaire</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1744-104">本主题介绍如何查看和评估回应者完成的调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="e1744-105">调查对象完成调查表后，您可以以下列方式查看和评估调查表结果：</span><span class="sxs-lookup"><span data-stu-id="e1744-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="e1744-106">**完成的回答会话** - 查看有关回应者已完成的调查表的详细信息，并生成用于总结回答和所得所有分数的报表。</span><span class="sxs-lookup"><span data-stu-id="e1744-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="e1744-107">**结果组** - 查看调查表的结果组详细信息和统计信息。</span><span class="sxs-lookup"><span data-stu-id="e1744-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="e1744-108">结果组统计信息可针对调查表的一个回答会话生成，也可以针对所有回答会话生成。</span><span class="sxs-lookup"><span data-stu-id="e1744-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="e1744-109">**调查表统计信息** - 指定用于计算特定回应者组的统计信息的条件。</span><span class="sxs-lookup"><span data-stu-id="e1744-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="e1744-110">您也可以生成各种报表，以便按人员、回答会话或结果组顺序查看结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="e1744-111">可使用以下与完成的调查表相关的报表：</span><span class="sxs-lookup"><span data-stu-id="e1744-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="e1744-112">结果</span><span class="sxs-lookup"><span data-stu-id="e1744-112">Answers</span></span>
-   <span data-ttu-id="e1744-113">调查表答卷</span><span class="sxs-lookup"><span data-stu-id="e1744-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="e1744-114">个人答卷</span><span class="sxs-lookup"><span data-stu-id="e1744-114">Answers per person</span></span>
-   <span data-ttu-id="e1744-115">反馈分析</span><span class="sxs-lookup"><span data-stu-id="e1744-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="e1744-116">回答会话结果</span><span class="sxs-lookup"><span data-stu-id="e1744-116">Answer session results</span></span>
<span data-ttu-id="e1744-117">调查对象完成调查表后，您可以查看完成的回答会话结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="e1744-118">回答会话是一个用户对调查表的响应。</span><span class="sxs-lookup"><span data-stu-id="e1744-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="e1744-119">您可以在**答卷**页面上查看有关完成的回答会话的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e1744-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="e1744-120">**答卷**页面上包含的回答会话将以各种方式进行筛选，具体取决于您打开此页面的方式：</span><span class="sxs-lookup"><span data-stu-id="e1744-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="e1744-121">全部调查表</span><span class="sxs-lookup"><span data-stu-id="e1744-121">All questionnaires</span></span>
-   <span data-ttu-id="e1744-122">特定调查表</span><span class="sxs-lookup"><span data-stu-id="e1744-122">A specific questionnaire</span></span>
-   <span data-ttu-id="e1744-123">特定人员</span><span class="sxs-lookup"><span data-stu-id="e1744-123">A specific person</span></span>

<span data-ttu-id="e1744-124">在**答卷**页面中，您可以查看有关回答、所得分数、回应者在每个结果组中的响应以及用于选定调查表的问题层次结构（如果已使用）的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e1744-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="e1744-125">您也可以生成和打印以下报告：</span><span class="sxs-lookup"><span data-stu-id="e1744-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="e1744-126">**结果报表** - 此报表显示针对所选回答会话的每个结果组中所得分数的图形表示形式。</span><span class="sxs-lookup"><span data-stu-id="e1744-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="e1744-127">**答卷报表** - 此报表显示针对调查表上每个问题选择的回应者的回答。</span><span class="sxs-lookup"><span data-stu-id="e1744-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="e1744-128">**不正确回答** - 此报表显示与回应者所选的不正确回答相关的信息。</span><span class="sxs-lookup"><span data-stu-id="e1744-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="e1744-129">**注意：** **结果**报表仅在您在调查表上使用结果组并已在**调查表**页面上选择**结果页面**时可用。</span><span class="sxs-lookup"><span data-stu-id="e1744-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="e1744-130">**答卷**报表和**不正确回答**报表仅在您已在**调查表**页面上选择**答卷报表**时可用。</span><span class="sxs-lookup"><span data-stu-id="e1744-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="e1744-131">调查表统计</span><span class="sxs-lookup"><span data-stu-id="e1744-131">Questionnaire statistics</span></span>
<span data-ttu-id="e1744-132">您可以使用调查表统计分析基于您定义的计算的已完成的调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="e1744-133">要定义计算，必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="e1744-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="e1744-134">选择条件计算并显示该统计。</span><span class="sxs-lookup"><span data-stu-id="e1744-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="e1744-135">您可以按调查表、问题、问题行或结果组显示统计。</span><span class="sxs-lookup"><span data-stu-id="e1744-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="e1744-136">选择在查看结果时将使用的图表类型。</span><span class="sxs-lookup"><span data-stu-id="e1744-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="e1744-137">选择网络中要包括其回答的人员的类型，如员工、联系人或申请人。</span><span class="sxs-lookup"><span data-stu-id="e1744-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="e1744-138">还可以包括从完成后匿名的调查表的回答。</span><span class="sxs-lookup"><span data-stu-id="e1744-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="e1744-139">设置基于年限或资历分析结果的间隔。</span><span class="sxs-lookup"><span data-stu-id="e1744-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="e1744-140">选择或验证细化统计主题的设置。</span><span class="sxs-lookup"><span data-stu-id="e1744-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="e1744-141">例如，通过选择邮政编码，您可以分析某个特定地理区域内所有回应者的结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="e1744-142">选择或验证标准以按回应者或调查表特征分析结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="e1744-143">例如，通过选择**邮政编码**，您可以分析回应者的位置和正确回答之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="e1744-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="e1744-144">您定义的设置将被保存下来并且可用于定期重新计算结果。</span><span class="sxs-lookup"><span data-stu-id="e1744-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e1744-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="e1744-145">Additional resources</span></span>
--------

[<span data-ttu-id="e1744-146">设计调查表</span><span class="sxs-lookup"><span data-stu-id="e1744-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="e1744-147">使用调查表</span><span class="sxs-lookup"><span data-stu-id="e1744-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="e1744-148">分发和完成调查表</span><span class="sxs-lookup"><span data-stu-id="e1744-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)


