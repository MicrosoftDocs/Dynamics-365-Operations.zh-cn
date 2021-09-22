---
title: 计划订单需要很长时间来更新
description: 更新计划订单上的需求数量和/或交货日期时，每个订单保存更新通常至少需要 30 秒
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475701"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>计划订单需要很长时间来更新

## <a name="symptoms"></a>故障特征

更新计划订单上的需求数量和/或交货日期时，每个订单保存更新通常至少需要 30 秒。

## <a name="resolution"></a>解决方法

这是内置的主计划引擎的一个已知问题。 它是由编辑期间物料清单结构的基础自动分解引起的。 此问题在计划优化中得到了解决，规划员可以在其中更新和审核相关订单，并可以在需要时触发计划运行来更新基础物料清单结构的计划订单。

使用内置的主计划引擎提高性能的一种方法是执行以下步骤：

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 选择一个计划。
1. 展开 **按天计算的时限** 快速选项卡。
1. 将 **分解** 设置为 *是*，将将此设置下方的字段设置为 0（零）。

> [!NOTE]
> 这会将为这个主计划执行的分解的期间限制为一天。
