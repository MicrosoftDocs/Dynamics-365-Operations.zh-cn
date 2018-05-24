---
title: "设计调查表"
description: "本主题描述创建调查表的过程。 第一步是设计调查表。 在您设计调查表时，您不仅编写问题和回答，还要创建结构，以便对回答进行记录和制表。"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cc25f4fde93df03145baedafb9c6b093659594d0
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="design-a-questionnaire"></a><span data-ttu-id="ac8c5-105">设计调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-105">Design a questionnaire</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac8c5-106">本主题描述创建调查表的过程。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="ac8c5-107">第一步是设计调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="ac8c5-108">在您设计调查表时，您不仅编写问题和回答，还要创建结构，以便对回答进行记录和制表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="ac8c5-109">仔细设计调查表可以有助于提高您收集的数据的质量。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="ac8c5-110">通过仔细设计，您可以在调查表的相应的时间处更好低寻找相应的选项。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="ac8c5-111">以下各点可以帮助您规划有效的调查表：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="ac8c5-112">清晰地定义调查表的用途以帮助确保问题支持用途。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="ac8c5-113">确定应完成调查表的个人或群体。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="ac8c5-114">编写将显示在调查表上的问题，并提供回答选择（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="ac8c5-115">确保调查表的安排符合逻辑，以便调查对象能够保持参与。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="ac8c5-116">按应显示给调查对象的顺序规划问题和回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="ac8c5-117">如果适用，确定应如何评估该结果。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="ac8c5-118">确定您是否需要其他功能。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="ac8c5-119">例如，确定是否以及如何分类结果、是否需要时间限制，或者是否强制回答所有问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="ac8c5-120">设计阶段包括您必须按此顺序完成的四类任务：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="ac8c5-121">根据需要，设置先决条件。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="ac8c5-122">如果适用，则设置回答组并回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="ac8c5-123">设置问题及其与回答组的关联。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="ac8c5-124">设置调查表并将问题附加到调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac8c5-125">必备项</span><span class="sxs-lookup"><span data-stu-id="ac8c5-125">Prerequisites</span></span>
<span data-ttu-id="ac8c5-126">在您可以创建调查表、回答和问题之前，必须具备某些必备项。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="ac8c5-127">但是，并非所有必备项都是完整功能必需的。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="ac8c5-128">必需</span><span class="sxs-lookup"><span data-stu-id="ac8c5-128">Required</span></span>

| <span data-ttu-id="ac8c5-129">先决条件</span><span class="sxs-lookup"><span data-stu-id="ac8c5-129">Prerequisite</span></span>        | <span data-ttu-id="ac8c5-130">描述</span><span class="sxs-lookup"><span data-stu-id="ac8c5-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="ac8c5-131">调查表类型</span><span class="sxs-lookup"><span data-stu-id="ac8c5-131">Questionnaire types</span></span> | <span data-ttu-id="ac8c5-132">对调查表进行分类。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="ac8c5-133">问题类型</span><span class="sxs-lookup"><span data-stu-id="ac8c5-133">Question types</span></span>      | <span data-ttu-id="ac8c5-134">对问题进行分类。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="ac8c5-135">可选</span><span class="sxs-lookup"><span data-stu-id="ac8c5-135">Optional</span></span>

| <span data-ttu-id="ac8c5-136">先决条件</span><span class="sxs-lookup"><span data-stu-id="ac8c5-136">Prerequisite</span></span>             | <span data-ttu-id="ac8c5-137">描述</span><span class="sxs-lookup"><span data-stu-id="ac8c5-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ac8c5-138">调查表参数</span><span class="sxs-lookup"><span data-stu-id="ac8c5-138">Questionnaire parameters</span></span> | <span data-ttu-id="ac8c5-139">修改调查表的基本控件和默认设置。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="ac8c5-140">调查表类型</span><span class="sxs-lookup"><span data-stu-id="ac8c5-140">Questionnaire types</span></span>

<span data-ttu-id="ac8c5-141">创建调查表时，需要调查表类型，并且必须分配调查表类型。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="ac8c5-142">调查表类型可帮助您更轻松地对调查表进行管理和分类。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="ac8c5-143">使用调查表类型可对调查表进行分类，并将其区分开来。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="ac8c5-144">例如，如果要选择多个调查表，则可以按类型进行筛选，这样有助于更轻松地找到特定调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="ac8c5-145">以下是几个调查表类型示例：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="ac8c5-146">人力资源开发</span><span class="sxs-lookup"><span data-stu-id="ac8c5-146">Human resource development</span></span>
-   <span data-ttu-id="ac8c5-147">客户调查</span><span class="sxs-lookup"><span data-stu-id="ac8c5-147">Customer surveys</span></span>
-   <span data-ttu-id="ac8c5-148">审查流程</span><span class="sxs-lookup"><span data-stu-id="ac8c5-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="ac8c5-149">问题类型</span><span class="sxs-lookup"><span data-stu-id="ac8c5-149">Question types</span></span>

<span data-ttu-id="ac8c5-150">创建问题时，需要问题类型，并且必须分配问题类型。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="ac8c5-151">使用问题类型对用于报告的问题进行分类。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="ac8c5-152">问题类型还便于您查找问题，因为您可以使用类型作为**问题**页上的筛选器。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="ac8c5-153">以下是几个问题类型示例：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="ac8c5-154">人力资源</span><span class="sxs-lookup"><span data-stu-id="ac8c5-154">Human resource</span></span>
-   <span data-ttu-id="ac8c5-155">业务管理</span><span class="sxs-lookup"><span data-stu-id="ac8c5-155">Managing business</span></span>
-   <span data-ttu-id="ac8c5-156">课程评估</span><span class="sxs-lookup"><span data-stu-id="ac8c5-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="ac8c5-157">调查表参数</span><span class="sxs-lookup"><span data-stu-id="ac8c5-157">Questionnaire parameters</span></span>

<span data-ttu-id="ac8c5-158">调查表参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="ac8c5-159">根据您的公司的要求，您可以不使用它们。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="ac8c5-160">调查表参数定义调查表的匿名性、编号序列代码和引用类型。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="ac8c5-161">组织分发调查表时，是否允许调查对象保持匿名可能会成为问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="ac8c5-162">编号序列代码用于组织问题和回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="ac8c5-163">根据这些编号序列代码，值将自动分配给项。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="ac8c5-164">在开始创建数据之前，应先定义所有参数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="ac8c5-165">可以随时修改调查表参数设置。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="ac8c5-166">调查表组成部分</span><span class="sxs-lookup"><span data-stu-id="ac8c5-166">Questionnaire components</span></span>
<span data-ttu-id="ac8c5-167">调查表包含三个主要元素：包含多选问题回答的回答组、问题和调查表本身。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span> <span data-ttu-id="ac8c5-168">您可以（可选）将调查表上的问题分成结果组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-168">You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="ac8c5-169">结果组能让您对问题进行分类，并提供对调查表的进一步分析。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="ac8c5-170">[![调查表组成部分](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="ac8c5-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="ac8c5-171">回答组和回答</span><span class="sxs-lookup"><span data-stu-id="ac8c5-171">Answer groups and answers</span></span>

<span data-ttu-id="ac8c5-172">调查对象可通过两种方式回答某一问题，具体采用何种方式取决于问题的主题：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="ac8c5-173">开放式问题不需要特定格式的响应。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="ac8c5-174">调查对象可以将响应以文本、数字或者日期或时间的形式键入。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="ac8c5-175">这些问题通常要求调查对象在其回答中提供主观信息，例如意见、描述、评价或估计。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="ac8c5-176">封闭式问题要求调查对象在可能正确的回答列表中选择回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="ac8c5-177">若要为封闭式问题提供可能回答的列表，您可以在**回答组**页上创建回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="ac8c5-178">回答组和回答是组成从其中创建问题的信息正文的组成部分。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="ac8c5-179">创建回答组之后，可以将回答组与**问题**页上的**回答组**字段中的问题相关联。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="ac8c5-180">回答组可用于同一调查表上的多个问题，并且可用于多个调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

<span data-ttu-id="ac8c5-181">**注释：** 如果在已完成调查表上已经使用的回答组中修改回答文本，则数据会变得难以评估，调查表结果可能不再有效。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-181">**Note:** If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="ac8c5-182">如果您必须更改回答组，请考虑创建新的回答组，而不是更改现有回答组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="ac8c5-183">您不能删除附加到问题或回答的回答组，也不能删除已回答的回答组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="ac8c5-184">问题</span><span class="sxs-lookup"><span data-stu-id="ac8c5-184">Questions</span></span>

<span data-ttu-id="ac8c5-185">调查表必须包含问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="ac8c5-186">问题可以是开放式问题或封闭式问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="ac8c5-187">开放式问题的回答不受控制，并且调查对象可以键入其回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="ac8c5-188">封闭式问题则要求事先提供一组预定义的回应选项，问题可以结构化，以便调查对象能够选择多个回应。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="ac8c5-189">问题应设计为可诱导调查对象提供明确信息，并且必须链接到为每个封闭式问题提供回应选项的回答组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 
     -  <span data-ttu-id="ac8c5-190">**注释：** 您必须先创建回答组和回答，才可以设置封闭式问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-190">**Note:** Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="ac8c5-191">问题可以按条件问题层次结构排列，因此，辅助问题取决于调查对象为前一个问题选择的回答。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="ac8c5-192">您可以首先编写问题，然后将其排列到层次结构中。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="ac8c5-193">设置调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-193">Setting up questionnaires</span></span>
<span data-ttu-id="ac8c5-194">**注释：** 在可以设置调查表之前，必须先设置回答、问题和必备条件。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-194">**Note:** Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="ac8c5-195">对于每个调查表，您可指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="ac8c5-196">回答必答题的总时间或时间限制。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="ac8c5-197">所有问题是否均为必答题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="ac8c5-198">是否计算调查表中的点数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="ac8c5-199">如何对结果分类。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-199">How to categorize results.</span></span>
-   <span data-ttu-id="ac8c5-200">调查表是否可供一组受限的调查对象使用。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="ac8c5-201">表格模板是否应作为背景显示在每个调查表页的后面。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="ac8c5-202">是否需要附加注释，才能向调查对象阐明调查表目的。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="ac8c5-203">是要按固定的顺序显示问题，还是随机从池中选择问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="ac8c5-204">是否只有对前面的回答给出特定响应后才会问到问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="ac8c5-205">设置调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-205">Set up a questionnaire</span></span>

<span data-ttu-id="ac8c5-206">您用来设置调查表的主要页面是**调查表**页。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="ac8c5-207">若要设置调查表，请按顺序完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="ac8c5-208">创建调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="ac8c5-209">按以下步骤之一将问题附加到调查表：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="ac8c5-210">如果您使用结果组，则可以使用结果组将问题附加到调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="ac8c5-211">首先为调查表设置结果组，然后将问题添加到结果组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="ac8c5-212">如果您不使用结果组，可以将问题直接附加到调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="ac8c5-213">如果需要，设置条件问题层次结构。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="ac8c5-214">测试调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-214">Test the questionnaire.</span></span>

<span data-ttu-id="ac8c5-215">在**调查表**页上，单击**验证**以测试调查表是否可以正确使用。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="ac8c5-216">但是，还可以在分发之前先完成调查表并进行自我测试。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="ac8c5-217">修改调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-217">Modify a questionnaire</span></span>

<span data-ttu-id="ac8c5-218">您可以在**调查表**页面上完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="ac8c5-219">修改调查表中的信息，例如结果组和问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="ac8c5-220">删除和添加问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-220">Delete and add questions.</span></span>
-   <span data-ttu-id="ac8c5-221">对结果组和序列号进行更改。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-221">Make changes in the result groups and sequence number.</span></span> 

<span data-ttu-id="ac8c5-222">**警告：** 对已回答的调查表进行更改时要小心谨慎。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-222">**Caution:** Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="ac8c5-223">更改可能会降低统计的准确性，使它们成为不良评估基础。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="ac8c5-224">考虑创建新的问题来代替更改已回答的问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="ac8c5-225">在调查表中，您不能删除以下类型的问题：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="ac8c5-226">附加到调查表中的问题</span><span class="sxs-lookup"><span data-stu-id="ac8c5-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="ac8c5-227">已回答并且因此显示在**回答**对话框中的问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="ac8c5-228">结果组</span><span class="sxs-lookup"><span data-stu-id="ac8c5-228">Result groups</span></span>

<span data-ttu-id="ac8c5-229">在您将问题附加到调查表时，结果组是可选的。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="ac8c5-230">结果组用于计算分数和分类调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="ac8c5-231">如果您使用结果组，可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="ac8c5-232">基于得分统计评估调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="ac8c5-233">为您设置的每个结果组评估回应者的分数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="ac8c5-234">为每个结果组生成统计可以帮助您分析结果。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="ac8c5-235">打印显示每个结果组的结果和基于每个结果组中所得分数的可选分数/文本的报告。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

<span data-ttu-id="ac8c5-236">**注释：** 您必须先完成以下任务，然后才能设置结果组：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-236">**Note:** Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="ac8c5-237">设置封闭式问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-237">Set up closed-ended questions.</span></span> <span data-ttu-id="ac8c5-238">对于封闭式问题，**问题**页上的输入类型必须是**复选框**、**选择按钮**或**组合框**。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="ac8c5-239">为回答组中分配给每个问题的回答定义分数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="ac8c5-240">设置调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-240">Set up a questionnaire.</span></span>

<span data-ttu-id="ac8c5-241">若要使用结果组将问题附加到调查表，首先设置调查表的结果组，然后将问题添加到结果组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="ac8c5-242">如果没有使用结果组，可以将问题直接附加到调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="ac8c5-243">您可以设置多个结果组，以评估每个类别中调查对象得到的分数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="ac8c5-244">完成调查表后，您可以查看每个结果组所得的分数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

<span data-ttu-id="ac8c5-245">**提示：** 若要使用分数评估调查表但不划分类别，可以将所有问题添加到某一个结果组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-245">**Tip:** To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="ac8c5-246">对于每个结果组，您还可以设置一个或多个基于分数的消息，这些是调查对象在完成调查表后收到的消息。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="ac8c5-247">显示的文本会有所不同，具体取决于调查对象在结果组中的得分。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="ac8c5-248">若要使用基于分数的消息，必须定义分数间隔和对每个间隔的描述。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="ac8c5-249">在调查对象在特定间隔中得分时，该间隔的文本将包括在结果报告中。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="ac8c5-250">由于结果组与分数有关，而分数与调查表上的特定问题组关联，因此您只能为一份调查表使用一个特定结果组。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="ac8c5-251">示例：针对结果组 3 的分数/文本</span><span class="sxs-lookup"><span data-stu-id="ac8c5-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="ac8c5-252">您使用一个用于领导才能测试的调查表，它有三个类别的 15 个问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="ac8c5-253">您创建三个结果组，向每个结果组添加五个问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="ac8c5-254">然后分数在三个组中合计。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="ac8c5-255">三个结果组如下：</span><span class="sxs-lookup"><span data-stu-id="ac8c5-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="ac8c5-256">创造能力</span><span class="sxs-lookup"><span data-stu-id="ac8c5-256">Creative abilities</span></span>
-   <span data-ttu-id="ac8c5-257">领导能力</span><span class="sxs-lookup"><span data-stu-id="ac8c5-257">Leadership abilities</span></span>
-   <span data-ttu-id="ac8c5-258">技术能力</span><span class="sxs-lookup"><span data-stu-id="ac8c5-258">Technical abilities</span></span>

<span data-ttu-id="ac8c5-259">若要使用基于分数的消息，可以为每个结果组设置文本间隔。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="ac8c5-260">每个问题被分配两个分数。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-260">Each question is assigned two points.</span></span> <span data-ttu-id="ac8c5-261">因此，每个结果组中的最大总分数为 10。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="ac8c5-262">下表显示您为“领导才能”结果组定义的基于分数的消息。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="ac8c5-263">分数间隔</span><span class="sxs-lookup"><span data-stu-id="ac8c5-263">Point interval</span></span> | <span data-ttu-id="ac8c5-264">文本</span><span class="sxs-lookup"><span data-stu-id="ac8c5-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="ac8c5-265">1 到 3</span><span class="sxs-lookup"><span data-stu-id="ac8c5-265">1 to 3</span></span>         | <span data-ttu-id="ac8c5-266">您具有平均领导能力。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="ac8c5-267">4 到 7</span><span class="sxs-lookup"><span data-stu-id="ac8c5-267">4 to 7</span></span>         | <span data-ttu-id="ac8c5-268">您具有良好的领导能力。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="ac8c5-269">8 到 10</span><span class="sxs-lookup"><span data-stu-id="ac8c5-269">8 to 10</span></span>        | <span data-ttu-id="ac8c5-270">您具有优秀的领导能力。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="ac8c5-271">您可以为调查表上的每个结果组设置分数间隔和文本。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="ac8c5-272">将显示每个结果组对应于每个回应者的分数的文本。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

<span data-ttu-id="ac8c5-273">**注释：** 您可以更改间隔和文本。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-273">**Note:** You can change intervals and texts.</span></span> <span data-ttu-id="ac8c5-274">但是，如果此时调查表已填完，则这些更改将导致新的结果报告和以前的结果报告有出入。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="ac8c5-275">有条件问题的层次结构</span><span class="sxs-lookup"><span data-stu-id="ac8c5-275">Conditional question hierarchies</span></span>

<span data-ttu-id="ac8c5-276">在您设置调查表时，有条件问题层次结构是可选的。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

<span data-ttu-id="ac8c5-277">**注释：** 在您可以设置有条件问题层次结构前，您必须将分配了回答组的问题附加到调查表。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-277">**Note:** Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="ac8c5-278">有条件问题使您可以，使用由条件问题在调查表中创建问题层次结构，您可以按基于对每个问题的调查对象选择的回答显示问题建立序列。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="ac8c5-279">通过在调查对象的回答的基础上建立问题序列，您可以在调查对象完成后对调查表进行修改。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="ac8c5-280">示例</span><span class="sxs-lookup"><span data-stu-id="ac8c5-280">Examples</span></span>

<span data-ttu-id="ac8c5-281">法人向其客户提供物料和服务。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="ac8c5-282">和通常在这种情况下发生的事情一样，某些客户通常只购买物料或只购买服务，而其他一些客户则同时购买这两者。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="ac8c5-283">因此，在该法人想要分发客户满意度调查时，它将某一条件结构应用于该调查表，因此仅购买服务的客户不必回答与物料有关的问题。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="ac8c5-284">另外，您可以设置一个调查表，以便如果调查对象为问题 1 选择了答案 A，则接下来显示问题 2。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="ac8c5-285">但是，如果调查对象为问题 1 选择了答案 B，则接下来显示问题 5。</span><span class="sxs-lookup"><span data-stu-id="ac8c5-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ac8c5-286">其他资源</span><span class="sxs-lookup"><span data-stu-id="ac8c5-286">Additional resources</span></span>
--------

[<span data-ttu-id="ac8c5-287">使用调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-287">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="ac8c5-288">分发和完成调查表</span><span class="sxs-lookup"><span data-stu-id="ac8c5-288">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="ac8c5-289">查看和评估调查表的结果</span><span class="sxs-lookup"><span data-stu-id="ac8c5-289">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


