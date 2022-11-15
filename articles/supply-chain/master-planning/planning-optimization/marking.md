---
title: 库存标记
description: 本文提供有关可用于在确认订单中标记库存的选项的信息。
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740568"
---
# <a name="inventory-marking"></a>库存标记

[!include [banner](../../includes/banner.md)]

本文提供有关可用于在确认订单中标记库存的选项的信息。

*标记* 用于链接供应和需求。 它类似于 *限定标准*，指示主计划预计如何满足需求。 从计划的角度看，主要区别在于标记比限定标准更具永久性。

引入标记以支持先进先出 (FIFO) 和后进先出 (LIFO) 的特殊成本计算方案。 但是，它现在还用于某些非成本计算方案。 供应和需求之间的标记是可选的，并且几乎是永久的。 标记可以由用户手动删除，也可以通过运行在其中选择 **删除标记** 选项的销售订单行分解来删除。

限定标准在覆盖范围期间由主计划控制，以将需求与所需供应链接在一起。 可针对每个计划运行限定标准，以优化满足需求所需的供应。 当主计划更新限定标准信息时，它将遵守任何现有标记。

限定标准首先包括相关标记、现有数量预留和在单数量预留，顺序如下：

1. 需求和供应之间的标记
1. 现有数量预留
1. 在单数量预留

确认计划订单后，**确认** 对话框提供用于为在确认期间创建的订单设置标记选项的 **更新标记** 字段。 选择以下值之一：

- *无* – 不应用库存标记。
- *标准* – 根据限定标准更新库存标记。 针对履行订单（供应）标记需求订单（需求）。 如果履行订单上还有一些数量，不会对其进行标记，并且参考信息将保留为空白。 例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将仅分配给销售订单。
- *扩展* – 同时标记需求订单（需求）和履行订单（供应），不管履行订单上仍然存在的任何数量。 例如，如果针对 150 ea 的采购订单限定 100 ea 的销售订单，参考信息将分配给销售订单和采购订单。
- *单级别标准* - 使用单级别标记。 单级别标记仅标记主物料，而不是其物料清单（物料清单）组件。 因此，您可以在确认后保持生产订单组件分配灵活。 单级别标记使系统能够针对紧急需求变化进行优化。 在 *标准* 单级别标记中，要求订单将根据其履行订单进行标记，但如果履行订单具有剩余数量，则不会标记它们。
- *单级别已扩展* - 使用单级别标记。 在 *已扩展* 单级别标记中，要求订单将根据其履行订单进行标记，并且无论是否剩余任何数量，都始终标记履行订单。

要为您的系统设置默认标记选项，请转到 **主计划 \> 设置 \> 主计划参数**。 然后，在 **标准更新** 选项卡上，将 **更新标记** 字段设置为首选选项。

> [!NOTE]
> 仅当系统上启用了 *按订单生产供应自动化* 功能时，才可使用 *单级别标准* 和 *单级别已扩展* 选项。 有关此功能以及如何启用此功能的详细信息，请参阅[按订单生产供应自动化](../make-to-order-supply-automation.md)。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
