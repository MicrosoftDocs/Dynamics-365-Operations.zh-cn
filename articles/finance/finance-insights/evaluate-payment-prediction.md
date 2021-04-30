---
title: 评估初始客户付款预测模型（预览）
description: 本主题描述您可以用来理解客户付款预测模型并评估其有效性的步骤。
author: ShivamPandey-msft
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 266f94b6a32c88307258aa99f2ac0c6bf9c50a84
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897904"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a><span data-ttu-id="497f5-103">评估初始客户付款预测模型（预览）</span><span class="sxs-lookup"><span data-stu-id="497f5-103">Evaluate the initial customer payment prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="497f5-104">本主题介绍在启用 Finance Insights 并生成和训练第一个模型之后如何评估预测模型。</span><span class="sxs-lookup"><span data-stu-id="497f5-104">This topic explains how to evaluate a prediction model after you've turned on Finance Insights and then generated and trained your first model.</span></span> <span data-ttu-id="497f5-105">本主题介绍预测客户付款的模型。</span><span class="sxs-lookup"><span data-stu-id="497f5-105">This topic addresses models for predicting customer payments.</span></span> <span data-ttu-id="497f5-106">其描述您可以用来理解客户付款预测模型并评估其有效性的步骤。</span><span class="sxs-lookup"><span data-stu-id="497f5-106">It describes the steps that you can take to understand the customer payment prediction model and evaluate its effectiveness.</span></span>

## <a name="getting-details-about-the-model"></a><span data-ttu-id="497f5-107">获取有关模型的详细信息</span><span class="sxs-lookup"><span data-stu-id="497f5-107">Getting details about the model</span></span>

<span data-ttu-id="497f5-108">在 Microsoft Dynamics 365 Finance 中的 **Finance Insights 参数** 页面上，准确性分数旁边将显示 **提高模型准确性** 链接。</span><span class="sxs-lookup"><span data-stu-id="497f5-108">On the **Finance Insights parameters** page in Microsoft Dynamics 365 Finance, an **Improve model accuracy** link appears next to the accuracy score.</span></span>

<span data-ttu-id="497f5-109">[![“提高模型准确性”链接](./media/prediction-model.png)](./media/prediction-model.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-109">[![Improve model accuracy link](./media/prediction-model.png)](./media/prediction-model.png)</span></span>

<span data-ttu-id="497f5-110">该链接将带您到 AI Builder，在这里您可以了解有关当前模型的详细信息，并采取措施进行改进。</span><span class="sxs-lookup"><span data-stu-id="497f5-110">This link takes you to AI Builder, where you can learn more about the current model and also take steps to improve it.</span></span> <span data-ttu-id="497f5-111">下图显示了已打开的页面。</span><span class="sxs-lookup"><span data-stu-id="497f5-111">The following illustration shows the page that is opened.</span></span>

<span data-ttu-id="497f5-112">[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-112">[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)</span></span>

<span data-ttu-id="497f5-113">打开的页面显示以下信息：</span><span class="sxs-lookup"><span data-stu-id="497f5-113">The page that is opened shows the following information:</span></span>

- <span data-ttu-id="497f5-114">在 **性能** 部分中，模型性能等级提供有关模型质量的观点。</span><span class="sxs-lookup"><span data-stu-id="497f5-114">In the **Performance** section, the model performance grade provides perspective on the quality of the model.</span></span> <span data-ttu-id="497f5-115">有关该等级的详细信息，请参阅 AI Builder 文档中的[预测模型性能](/ai-builder/prediction-performance)。</span><span class="sxs-lookup"><span data-stu-id="497f5-115">For more information about this grade, see [Prediction model performance](/ai-builder/prediction-performance) in the AI Builder documentation.</span></span>
- <span data-ttu-id="497f5-116">**最有影响力的数据** 部分显示数据的不同输入类型对模型的重要程度。</span><span class="sxs-lookup"><span data-stu-id="497f5-116">The **Most influential data** section shows how important different input types of data were for your model.</span></span> <span data-ttu-id="497f5-117">您可以评估此列表和相应的百分比，以确定信息是否与您对业务和市场的了解一致。</span><span class="sxs-lookup"><span data-stu-id="497f5-117">You can evaluate this list and the corresponding percentages to determine whether the information is consistent with what you know about your business and market.</span></span>

    <span data-ttu-id="497f5-118">[![预测模型的“性能”和“最有影响力的数据”部分](./media/models.png)](./media/models.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-118">[![Performance and Most influential data sections for the prediction model](./media/models.png)](./media/models.png)</span></span>

- <span data-ttu-id="497f5-119">在 **性能** 部分中，选择 **查看详细信息** 了解有关性能和其他注意事项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="497f5-119">In the **Performance** section, select **See details** to learn more about the grade and other considerations.</span></span> <span data-ttu-id="497f5-120">在下图中，详细信息显示该模型使用的信息少于建议的信息。</span><span class="sxs-lookup"><span data-stu-id="497f5-120">In the following illustration, the details show that the model uses less information than is recommended.</span></span> <span data-ttu-id="497f5-121">因此，系统已生成警告消息。</span><span class="sxs-lookup"><span data-stu-id="497f5-121">Therefore, the system has generated a warning message.</span></span>

    <span data-ttu-id="497f5-122">[![有关模型性能的警告](./media/details.png)](./media/details.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-122">[![Warnings about the model's performance](./media/details.png)](./media/details.png)</span></span>

## <a name="digging-deeper"></a><span data-ttu-id="497f5-123">深层发掘</span><span class="sxs-lookup"><span data-stu-id="497f5-123">Digging deeper</span></span>

<span data-ttu-id="497f5-124">尽管准确性是评估模型的良好起点，并且性能等级提供了视角，但 AI Builder 提供了更详细的度量标准，可用于评估。</span><span class="sxs-lookup"><span data-stu-id="497f5-124">Although accuracy is a good starting point for evaluating a model, and the performance grade provides perspective, AI Builder provides more detailed metrics that you can use for your evaluation.</span></span> <span data-ttu-id="497f5-125">要下载详细信息，请在 **性能** 部分中选择 **使用模型** 按钮旁边的省略号按钮 (**...**)，然后选择 **下载详细指标**。</span><span class="sxs-lookup"><span data-stu-id="497f5-125">To download the details, in the **Performance** section, select the ellipsis button (**...**) next to the **Use model** button, and then select **Download detailed metrics**.</span></span>

<span data-ttu-id="497f5-126">[![“下载详细指标”命令](./media/performance.png)](./media/performance.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-126">[![Download detailed metrics command](./media/performance.png)](./media/performance.png)</span></span>

<span data-ttu-id="497f5-127">下图显示可下载的数据的格式。</span><span class="sxs-lookup"><span data-stu-id="497f5-127">The following illustration shows the format that you can download the data in.</span></span>

<span data-ttu-id="497f5-128">[![下载的数据的格式](./media/data-format.png)](./media/data-format.png)</span><span class="sxs-lookup"><span data-stu-id="497f5-128">[![Format of downloaded data](./media/data-format.png)](./media/data-format.png)</span></span>

<span data-ttu-id="497f5-129">要对结果进行更深入的分析，一个很好的起点是查看“混淆矩阵”指标。</span><span class="sxs-lookup"><span data-stu-id="497f5-129">For a deeper analysis of the results, a good starting point is to review the "Confusion Matrix" metric.</span></span> <span data-ttu-id="497f5-130">例如，下面是上图中为该指标显示的数据。</span><span class="sxs-lookup"><span data-stu-id="497f5-130">For example, here is the data that is shown for this metric in the previous illustration.</span></span>

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

<span data-ttu-id="497f5-131">您可以通过以下方式扩展此数据。</span><span class="sxs-lookup"><span data-stu-id="497f5-131">You can expand this data in the following way.</span></span>

| &nbsp;                   | <span data-ttu-id="497f5-132">预计按时</span><span class="sxs-lookup"><span data-stu-id="497f5-132">Predicted On time</span></span> | <span data-ttu-id="497f5-133">预计逾期</span><span class="sxs-lookup"><span data-stu-id="497f5-133">Predicted Late</span></span> | <span data-ttu-id="497f5-134">预计严重逾期</span><span class="sxs-lookup"><span data-stu-id="497f5-134">Predicted Very late</span></span> |
|--------------------------|-------------------|----------------|---------------------|
| <span data-ttu-id="497f5-135">实际按时付款</span><span class="sxs-lookup"><span data-stu-id="497f5-135">Actual on time payment</span></span>   | <span data-ttu-id="497f5-136">**71**</span><span class="sxs-lookup"><span data-stu-id="497f5-136">**71**</span></span>            | <span data-ttu-id="497f5-137">0</span><span class="sxs-lookup"><span data-stu-id="497f5-137">0</span></span>              | <span data-ttu-id="497f5-138">21</span><span class="sxs-lookup"><span data-stu-id="497f5-138">21</span></span>                  |
| <span data-ttu-id="497f5-139">实际逾期付款</span><span class="sxs-lookup"><span data-stu-id="497f5-139">Actual late payment</span></span>      | <span data-ttu-id="497f5-140">5</span><span class="sxs-lookup"><span data-stu-id="497f5-140">5</span></span>                 | <span data-ttu-id="497f5-141">**0**</span><span class="sxs-lookup"><span data-stu-id="497f5-141">**0**</span></span>          | <span data-ttu-id="497f5-142">27</span><span class="sxs-lookup"><span data-stu-id="497f5-142">27</span></span>                  |
| <span data-ttu-id="497f5-143">实际严重逾期付款</span><span class="sxs-lookup"><span data-stu-id="497f5-143">Actual very late payment</span></span> | <span data-ttu-id="497f5-144">2</span><span class="sxs-lookup"><span data-stu-id="497f5-144">2</span></span>                 | <span data-ttu-id="497f5-145">0</span><span class="sxs-lookup"><span data-stu-id="497f5-145">0</span></span>              | <span data-ttu-id="497f5-146">**45**</span><span class="sxs-lookup"><span data-stu-id="497f5-146">**45**</span></span>              |

<span data-ttu-id="497f5-147">混淆矩阵显示从训练过程中随机选择的测试数据集的结果。</span><span class="sxs-lookup"><span data-stu-id="497f5-147">The confusion matrix shows the results of a randomly selected test dataset from the training process.</span></span> <span data-ttu-id="497f5-148">由于不使用这些已结发票来训练模型，因此它们是模型的良好测试用例。</span><span class="sxs-lookup"><span data-stu-id="497f5-148">Because these closed invoices weren't used to train the model, they are good test cases for the model.</span></span> <span data-ttu-id="497f5-149">此外，由于知道发票的实际状态，因此也可以看到模型的性能。</span><span class="sxs-lookup"><span data-stu-id="497f5-149">Additionally, because the actual state of the invoice is known, the model's performance can also be seen.</span></span>

<span data-ttu-id="497f5-150">首先要寻找的是最常见的实际值。</span><span class="sxs-lookup"><span data-stu-id="497f5-150">The first thing to look for is the most common actual value.</span></span> <span data-ttu-id="497f5-151">尽管此值可能无法与整体数据集完美匹配，但这是合理的近似值。</span><span class="sxs-lookup"><span data-stu-id="497f5-151">Although this value might not be perfectly aligned with the overall dataset, it's a reasonable approximation.</span></span> <span data-ttu-id="497f5-152">在这种情况下，总共 171 张发票中有 92 张 **实际按时付款**，这是最常见的实际值。</span><span class="sxs-lookup"><span data-stu-id="497f5-152">In this case, **Actual on time payment** occurs for 92 of the 171 total invoices and is the most common actual value.</span></span> <span data-ttu-id="497f5-153">因此，这是您模型的良好基准。</span><span class="sxs-lookup"><span data-stu-id="497f5-153">Therefore, it's a good baseline for your model.</span></span> <span data-ttu-id="497f5-154">如果您只是猜测所有发票都将按时寄出，那么 171 次中 92 次正确（即 54％ 的时间）。</span><span class="sxs-lookup"><span data-stu-id="497f5-154">If you just guessed that all invoices would be on time, you would be correct 92 out of 171 times (that is, 54 percent of the time).</span></span>

<span data-ttu-id="497f5-155">了解数据集的平衡度很重要。</span><span class="sxs-lookup"><span data-stu-id="497f5-155">It's important that you understand how balanced your dataset is.</span></span> <span data-ttu-id="497f5-156">在此示例中，171 张发票中 92 张按时付款，32 张逾期付款，47 张是严重逾期付款。</span><span class="sxs-lookup"><span data-stu-id="497f5-156">In this case, 92 out of 171 invoices were paid on time, 32 were paid late, and 47 were paid very late.</span></span> <span data-ttu-id="497f5-157">这些值表示一个合理平衡的数据集，因为每个分类中都有不平凡的结果。</span><span class="sxs-lookup"><span data-stu-id="497f5-157">These values indicate a reasonably balanced dataset, because there are non-trivial results in each classification.</span></span> <span data-ttu-id="497f5-158">对于机器学习模型而言，一个状态的结果很少这种情况很具挑战性。</span><span class="sxs-lookup"><span data-stu-id="497f5-158">A situation where one of the states has very few results can be challenging for a machine learning model.</span></span>

<span data-ttu-id="497f5-159">模型的准确性表示测试数据集的正确预测数。</span><span class="sxs-lookup"><span data-stu-id="497f5-159">The accuracy of the model indicates the number of correct predictions for the test dataset.</span></span> <span data-ttu-id="497f5-160">这些正确预测是在前面的示例中以粗体显示的值。</span><span class="sxs-lookup"><span data-stu-id="497f5-160">These correct predictions are the values that are shown in bold in the preceding example.</span></span> <span data-ttu-id="497f5-161">在此示例中，值产生的计算准确性为 67.8% (= \[71 + 0 + 45\] ÷ 171)。</span><span class="sxs-lookup"><span data-stu-id="497f5-161">In this case, the values produce a calculated accuracy of 67.8 percent (= \[71 + 0 + 45\] ÷ 171).</span></span> <span data-ttu-id="497f5-162">该值比 54％ 这一基准猜测提高了 14％，并且是模型质量的指标之一。</span><span class="sxs-lookup"><span data-stu-id="497f5-162">This value represents an improvement of 14 percent over the baseline guess of 54 percent and is one indicator of the model's quality.</span></span>

<span data-ttu-id="497f5-163">如果仔细查看混淆矩阵，您会注意到该模型在预测按时和严重逾期的发票付款方面做得很好。</span><span class="sxs-lookup"><span data-stu-id="497f5-163">If you look more closely at the confusion matrix, you will notice that the model does a good job of predicting on-time and very late invoice payments.</span></span> <span data-ttu-id="497f5-164">但是，对实际逾期付款（但非严重逾期）的所有 32 张发票不正确。</span><span class="sxs-lookup"><span data-stu-id="497f5-164">However, it's wrong about all 32 invoices that were actually paid late (but not very late).</span></span> <span data-ttu-id="497f5-165">该结果表明需要对模型进行更多探索和改进。</span><span class="sxs-lookup"><span data-stu-id="497f5-165">This result suggests that additional exploration and improvement of the model are required.</span></span>

<span data-ttu-id="497f5-166">代表比准确性更高的模型性能数字是 F1 宏分数。</span><span class="sxs-lookup"><span data-stu-id="497f5-166">A number that represents the performance of the model better than accuracy is the F1 Macro score.</span></span> <span data-ttu-id="497f5-167">该分数将考虑每个分类状态（按时、逾期和严重逾期）的结果。</span><span class="sxs-lookup"><span data-stu-id="497f5-167">This score considers the results of each classification state (on-time, late, and very late).</span></span> <span data-ttu-id="497f5-168">例如，下面是上图中为“F1 宏”指标显示的数据。</span><span class="sxs-lookup"><span data-stu-id="497f5-168">For example, here is the data that is shown for the "F1 Macro" metric in the previous illustration.</span></span>

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

<span data-ttu-id="497f5-169">在此示例中，F1宏分数为大约 49.3%，表示模型在各状态未提供有效预测，虽然总体准确性分数似乎合理地高。</span><span class="sxs-lookup"><span data-stu-id="497f5-169">In this case, the F1 Macro score of approximately 49.3 percent indicates that the model doesn't provide effective predictions across each state, despite an overall accuracy score that seems reasonably high.</span></span>

## <a name="improving-the-model"></a><span data-ttu-id="497f5-170">改善模型</span><span class="sxs-lookup"><span data-stu-id="497f5-170">Improving the model</span></span>

<span data-ttu-id="497f5-171">在更好地了解第一个模型的结果之后，您可能需要通过添加或删除功能列或筛选数据集中不支持准确预测的任何部分来改进模型。</span><span class="sxs-lookup"><span data-stu-id="497f5-171">After you understand the results of your first model better, you might want to improve the model by adding or removing feature columns, or by filtering any parts of the dataset that don't support accurate predictions.</span></span> <span data-ttu-id="497f5-172">关闭 AI Builder，然后使用 Dynamics 365 Finance 中的 **改善模型** 链接重新开始 AI Builder 流程。</span><span class="sxs-lookup"><span data-stu-id="497f5-172">Close AI Builder, and then use the **Improve model** link in Dynamics 365 Finance to restart the AI Builder process.</span></span> <span data-ttu-id="497f5-173">您可以试验不同的特性而不会影响已发布的模型。</span><span class="sxs-lookup"><span data-stu-id="497f5-173">You can experiment with different characteristics without affecting the published model.</span></span> <span data-ttu-id="497f5-174">仅当选择了 **发布**，发布的模型才会受影响。</span><span class="sxs-lookup"><span data-stu-id="497f5-174">The published model is affected only when you select **Publish**.</span></span> <span data-ttu-id="497f5-175">请记住，您的 Dynamics 365 Finance 实例使用单个模型。</span><span class="sxs-lookup"><span data-stu-id="497f5-175">Remember that a single model is used for your instance of Dynamics 365 Finance.</span></span> <span data-ttu-id="497f5-176">因此，在发布任何新模型之前，应仔细检查。</span><span class="sxs-lookup"><span data-stu-id="497f5-176">Therefore, you should carefully review any new model before you publish it.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="497f5-177">有关详细信息</span><span class="sxs-lookup"><span data-stu-id="497f5-177">For more information</span></span>

<span data-ttu-id="497f5-178">要了解有关如何评估预测模型的详细信息，请参阅[机器学习模型的结果](/confusion-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="497f5-178">For more information about how to evaluate prediction models, [Results of machine learning models](/confusion-matrix.md)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="497f5-179">隐私声明</span><span class="sxs-lookup"><span data-stu-id="497f5-179">Privacy notice</span></span>
<span data-ttu-id="497f5-180">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="497f5-180">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]