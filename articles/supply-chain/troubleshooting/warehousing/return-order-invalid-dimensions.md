---
title: 库存维度无效导致无法创建负荷行
description: 尝试将退货销售订单发放到仓库时，您可能会收到有关库存维度无效的错误。 请从订单行中删除这些内容。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119204"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>库存维度无效导致无法为退货销售订单创建负荷行

## <a name="symptoms"></a>故障特征

尝试将退货销售订单下达到仓库时，您可能会收到以下错误消息：

> 您无法为此订单行创建负荷行，因为它包含无效的库存维度。 您无法引用位于预留层次结构中位置维度以下的库存维度。 请从订单行中删除无效维度。

## <a name="resolution"></a>解决方法

很遗憾，此产品不支持销售退货流程的负荷处理。 因此，您不能将退货销售订单下达到仓库。

在销售订单交易中，您无法引用位于预留层次结构中 **位置** 维度以下的库存维度。 解决方法是从订单行中删除无效维度。
