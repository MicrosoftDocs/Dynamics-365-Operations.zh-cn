---
title: 机器学习模型的结果
description: 本文讨论机器学习 (ML) 模型中的混淆矩阵、分类问题和准确度。 目的是加深您对 ML 预测结果准确度的理解。
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23df5979231fbd6908b6f1e7c3aca5dd3e0e733d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910162"
---
# <a name="results-of-machine-learning-models"></a>机器学习模型的结果

[!include [banner](../includes/banner.md)]

本文讨论机器学习 (ML) 模型中的混淆矩阵、分类问题和准确度。 目的是加深您对 ML 预测结果准确度的理解。 目标受众包括希望建立数据科学知识和技能的工程师、分析师和管理人员。

## <a name="confusion-matrix"></a>混淆矩阵
对一组历史数据培训了监视的 ML 问题之后，将使用培训流程中预扣的数据进行测试。 这样，您可以将训练的模型的预测与实际值进行比较。 混淆矩阵提供了一种评估分类问题的成功程度以及错误的发生位置（即混淆之处）的方法。

例如，您的目标是根据一些身体和行为属性来预测宠物是狗还是猫。 如果您的测试数据集中包含 30 只狗和 20 只猫，那么混淆矩阵可能类似于下图。

![物种预测示例。](media/species-prediction-matrix.png)

绿色单元格中的数字表示正确的预测。 如您所见，该模型正确预测了实际猫的百分比更高。 该模型的整体准确度很好计算。 在此示例中，为 42 ÷ 50，即 0.84。

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>混淆矩阵中的多类分类符

如前例所示，大多数关于混淆矩阵的讨论都集中在二进制分类符上。 这种情况是特殊情况，可以考虑其他指标，例如敏感性和召回率。

接下来，我们将考虑具有三个状态的财务方案的分类问题。 该模型预测是按时，逾期还是严重逾期支付客户发票。 例如，在 100 张测试发票中，有 50 张按时付款，有 35 张是逾期付款，有 15 张是很晚付款。 在这种情况下，模型可能会产生类似于下图的混淆矩阵。

![模型 1.](media/payment-prediction-matrix.png)]

混淆矩阵提供的信息远远超过简单的准确度指标。 但是，它仍然相对容易理解。 混淆矩阵告诉您是否具有平衡的数据集，其中输出类的计数相似。 对于多类方案，它告诉您当输出类为序数时预测可能有多深，如前面有关客户付款的示例所示。

## <a name="model-accuracy"></a>模型准确度 
不同的准确度指标具有量化模型质量的优势。 

由于准确度是易于理解的指标，因此这是向其他人（特别是向不是数据科学家的模型用户）解释模型的良好起点。 无需了解统计信息即可了解模型的准确度。 当混淆矩阵可用时，它将提供对模型性能的进一步了解。

但是，为了更全面地理解，应注意与准确度相关的几个挑战。 指标的有用性取决于问题的背景。 与模型性能有关的一个经常出现的问题是：“模型有多好？” 但是，这个问题的答案不一定很简单。 考虑以下混淆矩阵（模型 2）。

![样本较大的付款预测示例。](media/payment-prediction-matrix-2.png)

快速计算表明该模型的准确度为 (70 + 10 + 3) ÷ 100，即 0.83。 从表面上看，此结果似乎比以前的多类模型（模型 1）的结果好，后者的准确度为 0.73。 但是更好吗？

要开始解决这个问题，请考虑一下本能猜测的准确度。 对于分类问题，简单的猜测总是可以预测出最常见的类。 对于模型 1，该猜测将是“按时”，它将产生 0.50 的准确度。 对于模型 2，该猜测也将是“按时”，它将产生 0.80 的准确度。 因为模型 1 的本能猜测提升了 0.73 – 0.50 = 0.23，而模型 2 的本能猜测提升了 0.83 – 0.80 = 0.03，因此模型 1 更好，即使其准确度更低。 计算表明，模型质量的有效评估需要比准确度值更多的上下文。

还需要注意一个方面。 考虑使用医学测试来检测患者疾病的情况。 该问题是二进制分类问题，其中阳性结果表明患者患有该疾病。 在这种情况下，您必须考虑以下错误的影响：

- 误报，即测试表明患者患有疾病，但该患者实际上并非如此。
- 漏报，即测试表明患者未患疾病，但实际上该患者患有。

显然，两种类型的错误都是不希望的，但是哪个更糟？ 同样，这取决于具体情况。 对于需要迅速治疗的威胁生命的疾病，应尽量减少漏报（希望随后进行其他检查）。 在其他不太重要的情况下，模型创建者可能会尽量减少误报。 无论如何，合理的结论是，要有效地确定模型的质量，您必须拥有比准确度指标所提供的信息更多的信息。

### <a name="recommendations"></a>推荐

准确度是与不熟悉统计信息的领域专家进行交流的重要工具。 但是，为了使信息有用，至关重要的是提供更多上下文以及准确度值。

对于付款预测方案，您可以为 ML 模型设置一个目标，其中包括不同付款行为中的因素。 目标是该模型应通过减少至少 50％ 的错误答案来改善本能猜测。 换句话说，您想要一个目标准确度，该准确度将本能猜测的准确度与 100％ 的准确度分开。

下表总结了本文中混淆矩阵的这一原理。

| 模型   | 本能猜测 | 目标 | 模型准确度 | 目标达成了吗？                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| 模型 1 | 0.50        | 0.75   | 0.73           | 几乎达成。 该模型极大地改善了猜测。 |
| 模型 2 | 0.80        | 0.90   | 0.83           | 编号 需要改进。                              |

## <a name="classification-f1-accuracy"></a>分类 F1 准确度

本文中的最后注意事项是对分类 ML 性能的更高级度量，称为 F1 准确度。

在定义 F1 准确度之前，还必须引入两个指标：即精度和召回率。 精度指示正确分配了指定为阳性的预测总数中的多少个。 该指标也称为阳性预测值。 召回率是正确预测的实际阳性病例总数。 此度量标准也称为灵敏度。

[![真实结果与错误结果。](./media/tn-fn.png)](./media/tn-fn.png)

在上图的混淆矩阵中，这些指标是通过以下方式计算的：

- 精度 = TP ÷ (TP + FP)
- 召回率 = TP ÷ (TP + FN)

F1 度量结合了精度和召回率。 结果是两个值的谐量平均值。 其计算方法如下：

- F1 = 2 × (精度 × 召回率) ÷ (精度 + 召回率)

让我们看一个具体的例子。 在本文的前面部分，有一个模型示例可以预测动物是狗还是猫。 下面重复此图。

[![物种预测示例（重复）。](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

如果将“狗”用作肯定答案，则结果如下。

- 精度 = 24 ÷ (24 + 2) = 0.9231
- 召回率 = 24 ÷ (24 + 6) = 0.8
- F1 = 2 × (0.9231 × 0.8) ÷ (0.9231 + 0.8) = 0.8572

如您所见，F1 值介于精度和召回率之间。

尽管 F1 的准确性不是那么容易理解，但是它会增加基本准确性数字的细微差别。 如下面的讨论所示，它还可以帮助解决不平衡的数据集。

本文的[模型准确性](#model-accuracy)一节比较了以下两个混淆矩阵。 即使第一个模型的准确性较低，它也被认为是更有用的模型，因为它比默认的按时付款显示出更多的改进。

![付款预测与实际示例。](media/payment-prediction-matrix.png)

![样本较大的付款预测示例（重复）。](media/payment-prediction-matrix-2.png)

让我们看看使用 F1 分数时这两个模型的比较。 F1 分数会影响每种状态的精度和召回率，而 F1 宏计算会将每种状态的 F1 分数取平均值，以确定总体 F1 分数。 还有其他 F1 变体，但是考虑到所有三种状态的平等考虑，考虑宏版本会引起更大的兴趣。

为了简化计算，构建了样本数组以匹配实际值和预测值。 这些数组在 Python 中使用了 sklearn 的指标库来计算值。 结果如下。

| 型号   | 本能猜测 | 准确度 | F1 宏 |
|---------|-------------|----------|----------|
| 模型 1 | 0.5         | 0.73     | 0.67     |
| 模型 2 | 0.80        | 0.83     | 0.66     |

有关此计算如何工作的更多详细信息，下面是模型 1 的 sklearn.metrics 分类报告。 标签分别为 1、2 和 3 的行表示了三种状态：“按时”、“逾期”和“严重逾期”。 宏平均值只是“f1-score”列的平均值。

| &nbsp;    | 精度 | 召回率   | f1-score |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

从这些结果可以看出，两个模型的 F1 宏精度得分几乎相同。 在这种情况下以及其他许多情况下，F1 精度可以更好地指示模型的功能。 至于准确性，对结果的解释要求您了解模型中最重要的考虑因素。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
