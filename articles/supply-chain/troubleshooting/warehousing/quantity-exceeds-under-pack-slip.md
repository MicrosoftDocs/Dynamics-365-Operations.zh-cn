---
title: 在装箱单生成期间数量超过欠交百分比
description: 生成装箱单时，出站负荷包含的数量超过欠交百分比。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ae02846c0ec937ebaff440dc5272a135e16c8aa7355ecc303929e760a54b6627
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760290"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>在装箱单生成期间数量超过欠交百分比

错误代码：SYS24921

## <a name="symptoms"></a>故障特征

生成装箱单时，出站负荷包含的数量超过欠交百分比。

当您尝试生成装箱单时，系统显示以下错误消息：

> 行欠交百分比是 %1，但允许的欠交百分比只有 %2。

因此，您无法为负荷生成装箱单。

## <a name="cause"></a>原因

负荷或装运的领料数量小于订购数量且不在欠交百分比的范围内。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装箱单生成失败的状态。 要解决此问题，请完成以下任务之一：

- 调整欠交百分比。
- 冲销并进行调整。

### <a name="adjust-the-under-delivery-percentage"></a>调整欠交百分比

使用以下过程调整欠交百分比。

1. 转到 **应收帐款 \> 订单 \> 所有订单**。
1. 选择无法为其过帐负荷的装箱单的销售订单。
1. 在 **销售订单行** 选项卡上，为超过欠交百分比的物料选择销售订单行。
1. 在  **行详细信息** 选项卡上，选择 **交货**。
1. 将 **欠交** 字段设置为可接受根据负荷数量领料的数量的更大百分比，以便可以继续生成装箱单。

### <a name="reverse-and-make-adjustments"></a>冲销并进行调整

冲销已为负荷过帐的所有内容（例如，装箱单、装运确认和工作），进行销售订单调整，将订单重新发放到仓库，并完成装运过程。

使用以下过程取消装箱单。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **取消装箱单**。

使用以下过程冲销装运确认。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **冲销** 组中，选择 **冲销装运确认**。

使用以下过程来冲销工作。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 在操作窗格上的 **负荷** 选项卡上，在 **工作** 组中，选择 **冲销工作**。
