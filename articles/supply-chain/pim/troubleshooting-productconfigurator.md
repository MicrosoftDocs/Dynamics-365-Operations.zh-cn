---
title: 产品配置器疑难解答
description: 此主题介绍如何解决使用产品配置器时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516735"
---
# <a name="troubleshoot-the-product-configurator"></a>产品配置器疑难解答

此主题介绍如何解决使用产品配置器时可能遇到的问题。

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>当我在销售订单行上配置产品时，物料文本会被覆盖。

### <a name="issue-description"></a>问题描述

当您为可配置物料创建销售订单行，然后修改物料文本时，会发生此问题。 当您配置物料，然后选择 **确定** 时，文本会被标准文本覆盖。

### <a name="issue-resolution"></a>解决问题

此行为是预期的。 文本字段包含变型名称，仅在您配置行后填充。 因此，您必须在配置行之后而不是在之前更改文本。

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>计算产品配置模型时，整数属性舍入不正确。

### <a name="issue-description"></a>问题描述

当您执行以下一系列操作时，可能会发生此问题：

1. 在生产配置模型上设置以下属性：

    - Input（整数）
    - Percent（十进制）
    - Result（整数）

2. 创建具有以下表达式的计算：

    *Result* = *Input* × *Percent* ÷ 100

在这种情况下，整数结果并不总是会正确舍入。 例如，输入为 1,000，百分比为 2.40。 因此，整数结果应为 24，因为 1,000 的 2.40% 为 24（或十进制形式的 24.00）。 而结果显示为 23。 但是，当百分比为 2.39 时，计算将舍入到 24 而不是 23。 当百分比为 2.50 时，计算将按预期舍入到 25。

### <a name="issue-resolution"></a>解决问题

发生此问题的原因是 Microsoft Solver Foundation 内部使用分数表示数字。 对于前面的示例，百分比为 2.40 的计算结果表示为 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375。 当 .NET 将此值计算为整数时，将返回 23。

此行为将不会更改，因为其他场景要依赖于此行为。 对于前面的示例，您可以通过引入其他十进制属性和计算来解决此问题。

例如，您可以在生产配置模型上设置以下属性：

- Input（整数）
- Percent（十进制）
- ResultDecimal（十进制）
- ResultInteger（整数）

然后，您可以添加以下计算：

- *ResultDecimal* = *Input* × *Percent* ÷ 100
- *ResultInteger* = *ResultDecimal*
