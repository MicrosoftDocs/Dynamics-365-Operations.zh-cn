---
title: 按需与 Supply Chain Management 定价引擎同步
description: 本主题介绍如何通过 Microsoft Dynamics 365 Sales 使用 Microsoft Dynamics 365 Supply Chain Management 中的定价引擎。
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6b0cc8f403be866ff00b89a33f6c59089c987bb0
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402822"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>按需与 Supply Chain Management 定价引擎同步

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 包括处理贸易协议、价目表、客户会员计划、促销和折扣的定价引擎。 定价引擎使用复杂的规则来确定给定报价单或订单的最佳价格。 使用双向写入时，您可以在 Microsoft Dynamics 365 Sales 中的 **报价单** 和 **订单** 页面上使用 Supply Chain Management 中的静态定价或定价引擎。

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>使用 Sales 中的 Supply Chain Management 中的定价引擎

1. 在 Sales 中，转到 **销售 \> 订单**。
1. 选择 **新建** 创建新订单，或在 **我的订单** 列表中选择现有订单。
1. 添加新订单行。
1. 如果您要创建新订单，请在操作窗格上选择 **价格订单**。 如果您要更新现有订单，请选择在操作窗格上 **重新计算**。
1. 以下列将自动填充：

    - 详细信息金额
    - 折扣百分比
    - 折扣
    - 不计运费金额
    - 运费金额
    - 总税款
    - 总金额

> [!NOTE]
> 创建报价单时会应用类似流程。

## <a name="how-it-works"></a>工作原理

当您在 Sales 中创建订单时，该订单将使用您在 Sales 中输入的值立即同步到 Supply Chain Management。 当您在 Sales 中选择 **价格订单** 或 **价格报价单** 时，Supply Chain Management 将根据 Supply Chain Management 中定义的贸易协议规则计算每个订单行和总订单的价格。 然后，新的计算值将重新同步到 Sales。

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>在 Supply Chain Management 中设置贸易协议评估选项

当 Supply Chain Management 计算在 Sales 中创建的订单的价格时，您可以将 Supply Chain Management 配置为遵循或忽略贸易协议。 请按照以下步骤设置此选项。

1. 登录到您的 Supply Chain Management 环境。
1. 转至 **应收帐款 \> 设置 \> 应收帐款参数**。
1. 在 **价格** 选项卡上的 **贸易协议评估** 快速选项卡上，根据需要添加或删除 **手动输入** 策略的行。 此策略的存在或缺失控制 Supply Chain Management 定价引擎是否将自动覆盖在 Sales 中输入的销售价。

    - 如果 **贸易协议评估** 设置中 *不存在* 此 **手动输入** 策略，则 Supply Chain Management 会提供价格主数据。 当用户在 Sales 内操作窗格中选择 **价格订单** 或 **价格报价单** 时，将调用 Supply Chain Management 定价引擎，并覆盖在 Sales 中输入的销售价，除非它等于在 Supply Chain Management 中计算的销售价。
    - 如果 **贸易协议评估** 设置中 *存在* 此 **手动输入** 策略，则 Sales 会提供价格主数据。 当用户在 Sales 内操作窗格中选择 **价格订单** 或 **价格报价单** 时，会阻止自动覆盖在 Sales 中输入的销售价。
    - Sale 中 **单位价格** 和/或 **折扣** 值为 *0（零）* 的订单行和报价单行被视为特殊情况。 如果相关贸易协议价格可用，则 Supply Chain Management 会 *始终* 将其应用于这些字段，而与 **贸易协议评估** 设置无关。

    对于每个案例的示例，请参阅接下来的方案。

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>示例方案 1：无手动输入选项的贸易协议评估

在此方案中，Supply Chain Management 中的 **贸易协议评估** 并 *不* 包括 **手动输入** 策略。 Sales 用户输入 Sales 中具有非零销售价的订单行，并且没有为 Supply Chain Management 中的物料定义销售价。

1. 在 Sales 中，用户创建 **单价** 为 1 美元（USD）的订单行。
1. 订单行已与 Supply Chain Management 同步，销售价为 1 美元。
1. 在 Sales 中，用户在操作窗格上选择 **价格订单**。
1. Supply Chain Management 搜索相关价格和折扣，然后计算总计。 由于物料在 Supply Chain Management 中没有销售价，因此该计算将更新行，以便其销售价为 0 美元。
1. 行的新销售价将重新同步到 Sales。
1. 结果是 Sales 中销售价为 0 美元的订单行。

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>示例方案 2：具有手动输入选项的贸易协议评估

在此方案中，Supply Chain Management 中的 **贸易协议评估** 并 *确实* 包括 **手动输入** 策略。 Sales 用户输入 Sales 中具有非零销售价的订单行。 Supply Chain Management 包括一个贸易协议，该贸易协议为订购物料设置的销售价为 2 美元。

1. 在 Sales 中，用户为物料创建 **单价** 为 1 美元（USD）的订单行。
1. 订单行已与 Supply Chain Management 同步，销售价为 1 美元。
1. 在 Sales 中，用户在操作窗格上选择 **价格订单**。
1. 由于 Supply Chain Management 中的 **贸易协议评估** 设置包括 **手动输入** 策略，因此销售价不会更改，即使适用的贸易协议指定了其他销售价也不例外。
1. Sales 和 Supply Chain Management 中的销售价格保持不变。

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>示例方案 3：Sales 中销售价格为零的物料的贸易协议评估

在此方案中，Supply Chain Management 中的 **贸易协议评估** 并 *确实* 包括 **手动输入** 策略。 Sales 用户输入 Sales 中销售价为 0（零）的订单行。 Supply Chain Management 包括一个贸易协议，该贸易协议为订购物料设置的销售价为 2 美元。

1. 在 Sales 中，用户创建 **单价** 值为 0 美元且 **行折扣** 值为 0 美元的订单行。
1. 订单行已与 Supply Chain Management 同步，销售价为 0 美元。
1. 由于它收到了销售价为 0（零）的订单行，因此 Supply Chain Management 会调用其定价引擎，即使启用了 **手动输入** 选项也不例外。 定价引擎返回由贸易协议确定的 2 美元的销售价，并更新 Supply Chain Management 中的订单行。
1. 更新的销售价尚未同步到 Sales 中的订单行。
1. 在 Sales 中，用户在操作窗格上选择 **价格订单**。
1. Supply Chain Management 中的订单行保持其销售价 2 美元，此值现在已重新同步到 Sales。 因此，Sales 中订单行的 **单价** 值从 0 美元更新为 2 美元。
1. 在 Sales 中，用户输入 0.50 美元的新 **行折扣** 值。 Sales 现在计算出该行的 **扩展金额** 值为 1.50 美元。
1. 订单行已与 Supply Chain Management 同步，**行折扣** 值为 0.50 美元。
1. 在 Sales 中，用户在操作窗格上选择 **价格订单**。
1. Sales 中的订单行没有更改价格或折扣。

## <a name="limitations"></a>限制

填写 Sales 中的列后，将应用以下限制：

- Supply Chain Management 中的费用设置和费用分配不会在 Sales 中复制。
- 定价不考虑在 Supply Chain Management 中销售订单行页面上的 **零售渠道** 列中指定的特殊零售定价。
- 不考虑 Supply Chain Management 的 **贸易折让管理** 部分定义的折扣。
- 定价不考虑销售协议。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
