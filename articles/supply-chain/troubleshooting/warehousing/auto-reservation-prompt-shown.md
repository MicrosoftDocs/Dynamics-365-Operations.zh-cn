---
title: 库存可用时显示自动预留提示
description: 当您在尚未启用仓库流程的仓库中使用物料时，将显示自动预留提示。 请指定库位上方的所有维度。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475725"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>即使库存可用也不显示批处理号的自动预留提示

## <a name="symptoms"></a>故障特征

当您在未启用仓库流程但启用了自动预留的仓库中使用具有 *batch-above* 预留层次结构的物料时，即使只有一个批次可供领料，也会显示批号的自动预留提示。

但是，当您在启用了仓库流程的仓库中使用同一物料时，不会显示自动预留提示。

## <a name="resolution"></a>解决方法

如果预留层次结构定义为 *batch-above* 或 *serial-above* ，必须始终在需求订单上指定引用的维度（**批号** 或 **序列号**）。 如果单个批号或序列号可用，则仓库流程可能能够完成信息。 但是，由于没有为仓库流程启用仓库，因此用户必须始终指定 **库位** 上方的所有维度。
