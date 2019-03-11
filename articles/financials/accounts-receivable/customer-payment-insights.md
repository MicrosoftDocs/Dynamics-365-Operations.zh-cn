---
title: 客户付款见解（预览版）
description: 此主题介绍客户付款见解如何帮助预测何时为发票付款，以及帮助组织创建优化策略以提高按时付款概率。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "344654"
---
# <a name="customer-payment-insights-preview"></a>客户付款见解（预览版）

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> 此功能是目标版本的一部分，仅适用于已选择加入专用预览的用户。 此功能还将在即将推出的一个一般可用性版本中提供。

# <a name="overview"></a>概览

组织通常发现很难预测客户何时为自己的发票付款。 缺少此项见解可能导致现金流量预测不精确，催款过程效率低下，以及可能将订单下达给可能有信用风险的客户。 客户付款见解（预览版）使用机器学习预测何时为发票付款。 还提供可调整的优化策略以将客户按时付款概率发挥到极致。

## <a name="predictions"></a>预测

组织可通过付款预测改进其业务流程，方法是帮助：

-   轻松识别据预测可能晚付款的发票。
-   采取相应措施提高按时付款的几率。

客户付款见解（预览版）使用机器学习预测何时为发票付款。 使用历史发票、付款和客户数据创建用于预测何时为发票付款的机器学习模型。

对于每个未结发票，客户付款见解（预览版）预测三种付款概率：

-  可能按时付款（在发票的到期日期内）。
-  可能在发票的到期日期 30 天内付款。
-  可能在发票的到期日期前 30 天内付款。

可以在预测部分中查看付款概率。

[![付款预测](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

还将使用上面定义的三种预测的付款概率之一为每个发票分配获胜的付款概率。 付款概率最高的方案为获胜方案。


例如，假设一个发票的预测显示其按时付款概率为 71%，到期日期 30 天内付款概率为 13%，到期日期 30 天前付款概率为 16%。 最高概率显示发票为准时方案，所以将使用准时付款概率标记发票。

[![付款预测](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>优化策略

除了付款预测，客户付款见解（预览版）还可以使用优化策略提高准时付款的几率。 这样组织就可以通过让用户调整发票和客户参数执行“假设”分析，然后比较对发票准时收款概率的相应影响。

例如，组织可能希望估计更新发票中的现金折扣对准时收款概率的影响。 发票优化后使用新折扣时，用户可以查看应用折扣对发票准时收款概率的影响。 如果与准时催款的优点相比，应用折扣的成本最低，组织可能选择对将来的所有未结订单应用所选折扣。

> [!NOTE] 
> 现在，只有折扣才可以成为客户付款见解（预览版）的优化策略。

[![优化后的预测](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>如何获取客户付款见解（预览版）

如果您有兴趣试用客户付款见解（预览版），请向[财务见解预览团队](mailto:fiap@microsoft.com)发电子邮件。 

## <a name="privacy-statement"></a>隐私声明

预览版将客户数据存储在美国。 此外，预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 for Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。
