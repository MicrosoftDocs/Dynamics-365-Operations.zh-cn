---
title: 客户付款预测
description: 此主题介绍可帮助您更好理解客户的典型付款实践的付款预测功能。 此功能还可以帮助您确定应导致您开始执行本应提前进行的收款流程的情况。
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f3d6f328ff3fd4da6ad3e7d4f3f751d3be692736
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713181"
---
# <a name="customer-payment-predictions"></a>客户付款预测

[!include [banner](../includes/banner.md)]

此主题介绍可帮助您更好理解客户的典型付款实践的付款预测功能。 此功能还可以帮助您确定应导致您开始执行本应提前进行的收款流程的情况。

## <a name="overview"></a>概览

组织通常发现很难预测客户何时为自己的发票付款。 缺乏此见识可能会导致以下问题：

- 现金流量预测不准确
- 开始得太晚的收款流程
- 下达给可能拖欠付款的客户的订单

客户付款预测可帮助组织预测客户何时为发票付款。 因此，他们可以创建收款策略，以帮助增加按时付款的可能性。

## <a name="predictions"></a>预测

付款预测使组织可以通过帮助组织识别可能逾期付款的发票来改善其业务流程。 组织可以使用该信息来采取行动，以提高按时付款的机会。

客户付款预测功能使用机器学习模型来更准确地预测客户何时支付未清发票。 该机器学习模型包括历史发票、付款和客户数据。

对于每张未结发票，此功能分配三项付款概率：

- 按时付款的概率
- 逾期付款的概率
- 严重逾期付款的概率

该功能还提供了预期付款的汇总视图。

[![付款预测的聚合视图。](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

每个发票都指定了按时付款的概率。 按时付款概率小于 50% 的发票上会标有红色圆圈，以表示收款代理可能需要注意这些发票。

[![付款概率的列表。](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

客户付款预测功能还提供上下文信息以解释预测。 此信息包括影响预测的主要因素、与客户之间的业务的当前状态，以及有关客户的历史付款行为的详细信息。

在许多业务中，收款流程是一种被动活动。 换句话说，直到发票到期，才开始收款流程。 借助客户付款预测，组织可以更主动地进行收款。 他们不再需要等待交易到期才开始收款流程。 他们可以使用付款预测功能来确定主动收款是否会提高按时付款的概率。

## <a name="methodology"></a>方法

过去，通常很难开发和部署人工智能 (AI) 解决方案。 此流程需要一支由数据科学家、主题专家 (SME) 和工程师组成的团队长时间工作，以制定、开发、部署和维护可用的 AI 解决方案。 客户付款预测有助于在 Microsoft Dynamics 365 Finance 中部署和使用 AI 解决方案。 Microsoft 正在预打包基于 Microsoft AI Builder 构建的 AI 解决方案。 因此，用户只需单击一下鼠标即可部署 AI 解决方案，以利用智能预测的优势。 如果您对预测的准确性不满意，那么高级用户可以（再次强调，只需单击一次鼠标）获得 AI Builder 扩展体验，然后选择或清除用于生成预测的字段。 准备就绪后，您可以“训练”模型并发布更改。 将在 Dynamics 365 Finance 中自动选取新训练的模型以生成预测。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
