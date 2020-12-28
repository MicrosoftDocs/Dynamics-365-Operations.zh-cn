---
title: 客户付款见解(预览)
description: 此主题介绍有助于加深对各客户的典型付款实践的付款见解功能。 此功能可帮助您确定证明开始执行本应提前进行的收款流程的情况。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644625"
---
# <a name="customer-payment-insights-preview"></a>客户付款见解(预览)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

此主题介绍有助于加深对各客户的典型付款实践的付款见解功能。 此功能可帮助您确定证明开始执行本应提前进行的收款流程的情况。 

## <a name="overview"></a>概览

可能很难预测客户何时为自己的发票付款。 缺乏见解会导致现金流量预测不准确，收款流程开始得太迟，或者订单被下达到可能拖欠付款的客户。 客户付款见解（预览）可帮助组织预测客户何时为发票付款。 此信息可帮助组织创建有关提高及时付款概率的收款策略。 

## <a name="predictions"></a>预测

付款预测将使组织能够轻松地识别可能延迟付款的发票，并采取适当的措施来提高其按时付款的机会，从而改善他们的业务流程。

使用利用历史发票、付款和客户数据的机器学习模型，客户付款见解（预览）可以更准确地预测客户会何时支付未清发票。

对于每个未结发票，客户付款见解（预览）可预测三种付款概率：

-   准时付款概率 
-   延迟付款概率
-   长时间延迟付款概率

客户付款见解（预览）也提供预期付款的聚合视图，可帮助组织了解他们可以期望客户会在三个时段（按时、逾期和长时间逾期）的哪一个收到付款总金额。

[![付款预测的聚合视图](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

而且，每个发票都指定了按时付款的概率。 如果按时付款的概率小于 50%，发票上会标有红色圆圈，以表示这些发票可能需要注意收款问题。 

[![付款概率列表](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

客户付款见解（预览）还提供上下文信息以解释预测，例如影响预测的主要因素，客户的业务现状以及有关客户历史付款行为的详细信息。 在许多企业中，收款流程是一种被动活动；在发票到期之前，收款流程不会开始。 

借助客户付款见解（预览），组织可以更主动地进行收款。 他们不再需要等待交易到期才开始收款流程。 他们可以使用付款预测功能来确定主动收款是否会提高按时付款的概率。 付款预测还为企业提供了证明有必要提前开始收款流程所需的信息。

## <a name="methodology"></a>方法

开发和部署 AI 解决方案非常困难。 需要一支由数据科学家、主题专家和工程师组成的团队长时间工作，以制定、开发、部署和维护可用的 AI 解决方案。 我们使在 Finance 中轻松部署和使用 AI 解决方案变得容易。 我们正在预打包基于 Microsoft AI Builder 构建的 Finance 中的 AI 解决方案。 最终用户只需单击一下按钮，即可部署 AI 解决方案并开始利用智能预测的好处。 如果组织对预测的准确性不满意，那么高级用户可以再次单击以输入 AI Builder 扩展体验，然后选择或取消选择用于生成预测的字段。 一旦准备好，他们就可以培养和发布更改，新培养的模型将在 Finance 中被自动选择用于预测。

## <a name="how-to-get-customer-payment-insights-preview"></a>如何获取客户付款见解（预览）

如果您有兴趣试用客户付款见解（预览），请向[客户付款见解（预览）](mailto:fiap@microsoft.com)发送电子邮件。

## <a name="privacy-notice"></a>隐私声明

预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。


