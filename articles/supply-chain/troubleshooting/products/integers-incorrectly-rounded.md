---
title: 计算产品配置模型时整数舍入错误
description: 计算产品配置模型时，整数结果始终舍入错误。 请通过增加小数属性和计算修复此问题。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475707"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>计算产品配置模型时整数舍入错误

## <a name="symptoms"></a>故障特征

当您执行以下一系列操作时，可能会发生此问题：

1. 在生产配置模型上设置以下属性：

    - Input（整数）
    - Percent（十进制）
    - Result（整数）

2. 创建具有以下表达式的计算：

    *Result* = *Input* × *Percent* ÷ 100

在这种情况下，整数结果并不总是会正确舍入。 例如，如果输入为 1,000 且百分比为 2.40，则整数结果应该为 24，因为 1,000 的 2.4% 为 24（或小数格式为 24.00）。 而结果显示为 23。 但是，当百分比为 2.39 时，计算将舍入到 24 而不是 23。 当百分比为 2.50 时，计算将按预期舍入到 25。

## <a name="cause"></a>原因

发生此问题的原因是 Microsoft Solver Foundation 内部使用分数表示数字。 对于前面的示例，百分比为 2.40 的计算结果表示为 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375。 当 .NET 将此值计算为整数时，将返回 23。

## <a name="resolution"></a>解决方法

此行为将不会更改，因为其他场景要依赖于此行为。 对于前面的示例，您可以通过引入其他十进制属性和计算来解决此问题。

例如，在生产配置模型上设置以下属性：

- Input（整数）
- Percent（十进制）
- ResultDecimal（十进制）
- ResultInteger（整数）

然后，您可以添加以下计算：

- *ResultDecimal* = *Input* × *Percent* ÷ 100
- *ResultInteger* = *ResultDecimal*
