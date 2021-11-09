---
title: 为收款流程自动化配置参数
description: 本主题介绍影响自动收款流程的参数，并提供设置这些参数以使自动流程反映您的意图和期望的指导。
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3055e10375f1b0be936e3ed0344cdf33dc7bc7e9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487066"
---
# <a name="configure-parameters-for-collection-process-automation"></a>为收款流程自动化配置参数

[!include [banner](../includes/banner.md)]

本主题介绍影响自动收款流程的参数，并提供设置这些参数以使自动流程反映您的意图和期望的指导。 有关如何自动执行收款流程的信息，请参阅[收款流程自动化](collections-process-automate.md)。

## <a name="general"></a>常规
在 **每个批处理任务的客户百分比** 中输入一个数字，确定每个自动化流程的批处理任务数。 将 **自动过帐催款单** 设置为 **是**，让催款单操作类型在自动化过程中过帐催款单。 将 **为自动化创建活动** 设置为 **是** 创建和关闭非活动操作类型的活动，来查看对帐户执行的所有自动化步骤。 在 **保留收款流程自动化历史记录的天数** 中定义收款历史记录存储的天数。 当发票到达收款流程的最后一步时，如果 **激活最后一个流程步骤后排除发票** 设置为 **是**，它将不会用于创建未来的流程自动化操作类型。 下一个最旧发票将确定下一个流程自动化步骤，以确保继续执行收款流程自动化操作。 

## <a name="payment-predictions"></a>付款预测
从版本 10.0.21 开始，Finance Insights 中的客户付款预测将预测发票是会按时、逾期还是严重逾期支付。 您可以在 Finance insights 中配置每个类别。 如果预测发票会逾期支付，请务必在发票到期之前开始收款流程。 这些预测可用于在收款流程自动化运行时创建收款活动。 将 **启用付款预测** 设置为 **是** 可以使用客户付款预测根据发票逾期支付的可能性创建收款活动。 

有关客户付款预测和 Finance Insights 的详细信息，请参阅[客户付款预测](payment-insights-overview.md)。

当客户付款预测模型运行时，它会为发票按时支付、逾期支付或严重逾期支付的预测分配一个百分比。 在预计延迟付款的情况下，您可以使用该信息使用收款流程自动化自动开始收款活动。 您可以在 **信用和收款 > 收款** 下的 **每个客户的付款预测** 或 **每笔交易的付款预测** 页面上查看这些百分比。 

如果客户发票的平均付款预测低于基准百分比，则不会创建活动。 如果发票预测大于或等于基准百分比，将为每个客户创建一个活动。 对于 **预测: 逾期**，输入达到多少 **基准百分比** 时收款流程自动化应创建收款活动。 这是逾期和严重逾期的一个聚合值。 选择一个 **业务文档模板** 用于创建的活动或创建新活动。 这将确定 **类型**、**用途** 和 **活动结束前的天数**。 输入任何 **注释**，它们将在创建活动时默认作为描述。 对于 **预测: 严重逾期**，输入达到多少 **基准百分比** 时收款流程自动化应为预测会严重逾期支付发票的客户创建收款活动。 选择一个 **业务文档模板** 用于创建的活动。 这将确定 **类型**、**用途** 和 **活动结束前的天数**。 输入任何 **注释**，它们将在创建活动时默认作为描述。 

### <a name="example"></a>示例
如果逾期基准百分比设置为 60%。 当对每个发票运行客户付款预测时，系统会分配按时、逾期或严重逾期支付的百分比预测。 如果发票逾期支付的付款预测为 59% 或更少，自动收款流程不会为发票创建收款活动。 如果发票的客户付款预测大于或等于 60%，将在收款流程自动化期间创建收款活动。 

> [!NOTE]
> 严重逾期预测在逾期预测之前进行评估，因为严重逾期包括预测会逾期支付的发票。 如果发票同时属于逾期和严重逾期基准，收款流程将仅生成一个活动。 在这种情况下，系统会使用严重逾期活动和业务文档，因为严重逾期的优先级更高。 已生成的任何其他操作不会再次生成。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]