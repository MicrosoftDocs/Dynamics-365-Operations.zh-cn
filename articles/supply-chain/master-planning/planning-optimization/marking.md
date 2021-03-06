---
title: 通过计划优化进行库存标记
description: 本主题提供有关可用于在使用计划优化时在确认订单中标记库存的选项的信息。
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809486"
---
# <a name="inventory-marking-with-planning-optimization"></a>通过计划优化进行库存标记

[!include [banner](../../includes/banner.md)]

本主题提供有关可用于在使用计划优化时在确认订单中标记库存的选项的信息。

*标记* 用于链接供应和需求。 它类似于 *限定标准*，指示主计划预计如何满足需求。 从计划的角度看，主要区别在于标记比限定标准更具永久性。

引入标记以支持先进先出 (FIFO) 和后进先出 (LIFO) 的特殊成本计算方案。 但是，它现在还用于某些非成本计算方案。 供应和需求之间的标记是可选的，并且几乎是永久的。 标记可以由用户手动删除，也可以通过运行在其中选择 **删除标记** 选项的销售订单行分解来删除。

限定标准在覆盖范围期间由主计划控制，以将需求与所需供应链接在一起。 可针对每个计划运行限定标准，以优化满足需求所需的供应。 当主计划更新限定标准信息时，它将遵守任何现有标记。

限定标准首先包括相关标记、现有数量预留和在单数量预留，顺序如下：

1. 需求和供应之间的标记
1. 现有数量预留
1. 在单数量预留

确认计划订单后，**确认** 对话框提供用于为在确认期间创建的订单设置标记选项的 **更新标记** 字段。 选择以下值之一：

- **无** – 不应用库存标记。
- **标准** – 根据限定标准更新库存标记。 针对履行订单（供应）标记需求订单（需求）。 如果履行订单上还有一些数量，不会对其进行标记，并且参考信息将保留为空白。 例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将仅分配给销售订单。
- **扩展** – 同时标记需求订单（需求）和履行订单（供应），不管履行订单上仍然存在的任何数量。 例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将分配给销售订单和采购订单。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]