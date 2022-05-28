---
title: 评估初始客户付款预测模型
description: 本主题描述您可以用来理解客户付款预测模型并评估其有效性的步骤。
author: ShivamPandey-msft
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: c0951c8dcf6205ebbb15baf86b1272af4e95547f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677945"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model"></a>评估初始客户付款预测模型

[!include [banner](../includes/banner.md)]

本主题介绍在启用 Finance Insights 并生成和训练第一个模型之后如何评估预测模型。 本主题介绍预测客户付款的模型。 其描述您可以用来理解客户付款预测模型并评估其有效性的步骤。

## <a name="getting-details-about-the-model"></a>获取有关模型的详细信息

在 Microsoft Dynamics 365 Finance 中的 **Finance Insights 参数** 页面上，准确性分数旁边将显示 **提高模型准确性** 链接。

[![“提高模型准确性”链接。](./media/prediction-model.png)](./media/prediction-model.png)

该链接将带您到 AI Builder，在这里您可以了解有关当前模型的详细信息，并采取措施进行改进。 下图显示了已打开的页面。

[![AI Builder。](./media/what-to-predict.png)](./media/what-to-predict.png)

打开的页面显示以下信息：

- 在 **性能** 部分中，模型性能等级提供有关模型质量的观点。 有关该等级的详细信息，请参阅 AI Builder 文档中的[预测模型性能](/ai-builder/prediction-performance)。
- **最有影响力的数据** 部分显示数据的不同输入类型对模型的重要程度。 您可以评估此列表和相应的百分比，以确定信息是否与您对业务和市场的了解一致。

    [![预测模型的“性能”和“最有影响力的数据”部分。](./media/models.png)](./media/models.png)

- 在 **性能** 部分中，选择 **查看详细信息** 了解有关性能和其他注意事项的详细信息。 在下图中，详细信息显示该模型使用的信息少于建议的信息。 因此，系统已生成警告消息。

    [![有关模型性能的警告。](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>深层发掘

尽管准确性是评估模型的良好起点，并且性能等级提供了视角，但 AI Builder 提供了更详细的度量标准，可用于评估。 要下载详细信息，请在 **性能** 部分中选择 **使用模型** 按钮旁边的省略号按钮 (**...**)，然后选择 **下载详细指标**。

[![“下载详细指标”命令。](./media/performance.png)](./media/performance.png)

下图显示可下载的数据的格式。

[![下载的数据的格式。](./media/data-format.png)](./media/data-format.png)

要对结果进行更深入的分析，一个很好的起点是查看“混淆矩阵”指标。 例如，下面是上图中为该指标显示的数据。

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

您可以通过以下方式扩展此数据。

| &nbsp;                   | 预计按时 | 预计逾期 | 预计严重逾期 |
|--------------------------|-------------------|----------------|---------------------|
| 实际按时付款   | **71**            | 0              | 21                  |
| 实际逾期付款      | 5                 | **0**          | 27                  |
| 实际严重逾期付款 | 2                 | 0              | **45**              |

混淆矩阵显示从训练过程中随机选择的测试数据集的结果。 由于不使用这些已结发票来训练模型，因此它们是模型的良好测试用例。 此外，由于知道发票的实际状态，因此也可以看到模型的性能。

首先要寻找的是最常见的实际值。 尽管此值可能无法与整体数据集完美匹配，但这是合理的近似值。 在这种情况下，总共 171 张发票中有 92 张 **实际按时付款**，这是最常见的实际值。 因此，这是您模型的良好基准。 如果您只是猜测所有发票都将按时寄出，那么 171 次中 92 次正确（即 54％ 的时间）。

了解数据集的平衡度很重要。 在此示例中，171 张发票中 92 张按时付款，32 张逾期付款，47 张是严重逾期付款。 这些值表示一个合理平衡的数据集，因为每个分类中都有不平凡的结果。 对于机器学习模型而言，一个状态的结果很少这种情况很具挑战性。

模型的准确性表示测试数据集的正确预测数。 这些正确预测是在前面的示例中以粗体显示的值。 在此示例中，值产生的计算准确性为 67.8% (= \[71 + 0 + 45\] ÷ 171)。 该值比 54％ 这一基准猜测提高了 14％，并且是模型质量的指标之一。

如果仔细查看混淆矩阵，您会注意到该模型在预测按时和严重逾期的发票付款方面做得很好。 但是，对实际逾期付款（但非严重逾期）的所有 32 张发票不正确。 该结果表明需要对模型进行更多探索和改进。

代表比准确性更高的模型性能数字是 F1 宏分数。 该分数将考虑每个分类状态（按时、逾期和严重逾期）的结果。 例如，下面是上图中为“F1 宏”指标显示的数据。

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

在此示例中，F1宏分数为大约 49.3%，表示模型在各状态未提供有效预测，虽然总体准确性分数似乎合理地高。

## <a name="improving-the-model"></a>改善模型

在更好地了解第一个模型的结果之后，您可能需要通过添加或删除功能列或筛选数据集中不支持准确预测的任何部分来改进模型。 关闭 AI Builder，然后使用 Dynamics 365 Finance 中的 **改善模型** 链接重新开始 AI Builder 流程。 您可以试验不同的特性而不会影响已发布的模型。 仅当选择了 **发布**，发布的模型才会受影响。 请记住，您的 Dynamics 365 Finance 实例使用单个模型。 因此，在发布任何新模型之前，应仔细检查。

## <a name="for-more-information"></a>有关详细信息

要了解有关如何评估预测模型的详细信息，请参阅[机器学习模型的结果](confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
