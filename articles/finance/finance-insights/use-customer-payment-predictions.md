---
title: 使用客户付款预测(预览)
description: 本主题介绍了使用 Finance insights 试用版的先决条件和各种步骤。
author: ShivamPandey-msft
ms.date: 07/17/2021
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
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 144de66678beea64b9f96239b519a19926d87ab5
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638310"
---
# <a name="use-customer-payment-predictions-preview"></a>使用客户付款预测(预览)

[!include [banner](../includes/banner.md)]

本主题说明如何使用客户付款预测。 使用此功能之前，请确保已完成该功能的设置步骤。 有关详细信息，请参阅[启用客户付款预测](enable-cust-paymnt-prediction.md)。

您可以在 **管理客户信用和收款** 工作区和 **每笔交易的付款预测** 与 **每个客户的付款预测** 这两个新列表页上查看客户付款预测。

### <a name="manage-customer-credit-and-collections-workspace"></a>管理“客户信用和收款”工作区

**管理客户信用和收款** 工作区中有两个磁贴：**每笔交易的付款预测** 和 **预计逾期余额较高的客户**。

- **每笔交易的付款预测** 磁贴显示在 **按时** 时段中付款概率低于 50% 的未结客户交易记录的数量。 您可以选择此磁贴打开 **每笔交易的付款预测** 列表页。
- **预计逾期余额较高的客户** 磁贴显示预计总余额中超过一半 (50％) 付款逾期和/或严重逾期的客户的数量。 您可以选择此磁贴打开 **每个客户的付款预测** 列表页。

[![管理“客户信用和收款”工作区。](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>“每笔交易的付款预测”列表页

在 **每笔交易的付款预测** 列表页，您可以在 **按时**、**逾期** 和 **严重逾期** 时段中查看未结交易记录的付款概率。 对于网格中的每个交易，**按时概率** 列显示在到期日或之前付款的概率。 如果按时付款的概率小于 50％，则在 **按时概率** 列旁边显示一个红圈以指示逾期付款的风险。

[![“每笔交易的付款预测”页面。](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

页面右侧的 **相关信息** 窗格显示有关预测的更多详细信息：

- 对于网格中选中的交易，**付款预测** 快速选项卡会在 **按时**、**逾期** 和 **严重逾期** 时段显示付款预测的详细信息。 **主要因素** 部分显示影响预测的主要因素。 主要因素是所选交易和/或该交易的客户的属性。
- **Customer Insights** 快速选项卡显示所选交易的客户的当前发票、付款和收款统计信息。
- **客户历史记录** 快速选项卡在 **按时**、**逾期** 和 **严重逾期** 时段中显示客户的付款历史记录。

**主要因素** 部分、**Customer Insights** 和 **客户历史记录** 快速选项卡中的数据有助于说明付款预测。 它可以帮助您增加对预测效果的信心。

[![“相关信息”窗格中付款预测的图形指示符。](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>“每个客户的付款预测”列表页

**每个客户的付款预测** 列表页显示 **按时**、**逾期** 和 **严重逾期** 时段中预计付款的总未结余额和金额。

[![“每个客户的付款预测”页面。](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

每个时段中的付款金额的计算方法是交易余额的加权平均值之和。 此金额根据每个时段中的付款概率计算。

例如，一个客户有三笔未结交易在每个时段中具有以下付款概率。

| 交易 | 时长 | 按时付款概率 | 逾期付款概率 | 严重逾期付款概率 |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10%                  | 50%               | 40%                    |
| T2          | 1,000  | 50%                  | 30%               | 20%                    |
| T3          | 10,000 | 1%                   | 4%                | 95%                    |

在这种情况下，将按以下方式预测每个时段的付款。

| 时段   | 交易 T1      | 交易 T2         | 交易 T3            | 合计 |
|-----------|---------------------|------------------------|---------------------------|-------|
| 按时   | 100 × 10 ÷ 100 = 10 | 1,000 × 50 ÷ 100 = 500 | 10,000 × 1 ÷ 100 = 100    | 610   |
| 延迟      | 100 × 50 ÷ 100 = 50 | 1,000 × 30 ÷ 100 = 300 | 10,000 × 4 ÷ 100 = 400    | 750   |
| 过度延迟 | 100 × 40 ÷ 100 = 40 | 1,000 × 20 ÷ 100 = 200 | 10,000 × 95 ÷ 100 = 9,500 | 9,740 |

页面右侧的 **相关信息** 部分显示有关预测的更多详细信息：

- 对于网格中选中的交易，**付款预测** 快速选项卡会在 **按时**、**逾期** 和 **严重逾期** 时段显示付款预测的详细信息。 **主要因素** 部分显示影响付款的主要因素。 主要因素是所选交易和/或该交易的客户的属性。
- **Customer Insights** 快速选项卡显示所选交易的客户的当前发票、付款和收款统计信息。
- **客户历史记录** 快速选项卡在 **按时**、**逾期** 和 **严重逾期** 时段中显示客户的付款历史记录。

**主要因素** 部分、**Customer Insights** 和 **客户历史记录** 快速选项卡中的数据有助于说明付款预测。 它可以帮助您增加对预测效果的信心。

## <a name="improving-the-accuracy-of-payment-predictions"></a>提高付款预测的准确性

可以转到 **信用和收款 \> 设置 \> Finance insights \> Finance insights 参数** 查看付款预测的准确性。 **客户付款见解** 选项卡上的 **预测模型** 部分以百分比形式显示预测模型的准确性。

[![付款预测的准确性。](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

如果您对准确性不满意，请选择 **提高模型准确性** 链接打开 AI Builder 扩展体验。 在 AI Builder 扩展体验中，您可以选择或取消选择字段，直到选择了您认为对准确预测付款概率最重要的字段。 完成后，您可以轻松地重新训练预测模型并发布更改。 将在 Dynamics 365 Finance 中自动选取新训练的预测模型以进行预测。

[![AI Builder 扩展经验。](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>发布详细信息

Finance insights 公开预览版可用于美国、欧洲和英国的试用部署。 Microsoft 将逐渐增加对更多地区的支持。

可以并且应该仅在第 2 层沙盒环境中启用公开预览版功能。 在沙盒环境中创建的设置和 AI 模型不能迁移到生产环境。 有关详细信息，请参阅 [Microsoft Dynamics 365 Previews 补充使用条款](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
