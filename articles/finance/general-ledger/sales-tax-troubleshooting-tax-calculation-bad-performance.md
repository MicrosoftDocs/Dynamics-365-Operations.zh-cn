---
title: 税款计算性能影响交易
description: 本主题提供与税款计算性能及其对交易的影响有关的故障排除信息。
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: da19a83945450c2d35f95be2241b84e407860fe7808ff83934686ca2e00859bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748946"
---
# <a name="tax-calculation-performance-affects-transactions"></a>税款计算性能影响交易

[!include [banner](../includes/banner.md)]

有时，交易会受到税款计算存在的性能问题的影响。 要解决此问题，请根据需要按照以下各节中的步骤操作。

## <a name="review-the-transaction-line-count"></a>查看交易行计数

确定交易是否有很多行（例如，多于几百行）。 如果没有，请转到下一节。 如果交易确实有几百行，应延迟税款计算。 有关详细信息，请参阅[为日记帐启用延迟税款计算](enable-delayed-tax-calculation.md)。 

接下来，您可以确定是否满足以下任何条件：

- 有来自大文件的导入交易。
- 多个会话同时处理同一个交易税款计算。
- 交易有多个行，视图会实时更新。 例如，更改行的字段时，会实时更新 **普通日记帐** 页上的 **计算销售税金额** 字段。

   [![日记帐凭证页面上的“计算销售税金额”字段。](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

如果满足这些条件的任何一个，请延迟税款计算。

## <a name="review-the-call-stack"></a>查看调用堆栈

查看调用堆栈，确定是否多次调用了税款计算。 如果不是，请转到下一节。 如果调用堆栈被多次调用，请按照下列步骤帮助减少税款计算次数。

1. 如果日记帐已考虑了交易，请延迟税款计算。 有关详细信息，请参阅[为日记帐启用延迟税款计算](enable-delayed-tax-calculation.md)。
2. 如果交易是采购订单，应用程序版本晚于 10.0.15，可以通过启用 **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** 的外部测试将税款计算延迟到最终计算。

## <a name="review-the-call-stack-timeline"></a>查看调用堆栈时间线

查看调用堆栈时间线，确定是否存在以下问题。 如果存在，启用 **TaxUncommittedDoIsolateScopeFlighting** 的外部测试来解决该问题。

- 交易将导致系统停止响应，直到会话结束。 因此，交易无法计算税收结果。 下图显示了您收到的“会话已结束”消息框。

    [![会话已结束消息。](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted** 方法会比其他方法花费更多时间。 例如，在下图中，**TaxUncommitted::updateTaxUncommitted()** 方法需要 43,347.42 秒，而其他方法则需要 0.09 秒。

    [![方法持续时间。](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>自定义和调用税款计算

自定义时，请勿在每一行的 **insert()** 或 **update()** 方法中调用税款计算。 应在交易级别调用税款计算。

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义

如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。 如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
