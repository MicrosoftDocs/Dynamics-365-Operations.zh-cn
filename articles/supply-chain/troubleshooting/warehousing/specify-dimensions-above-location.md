---
title: 无法为采用 batch-above 层次结构的部分数量发放负荷
description: 如果使用的物料采用 batch-above 预留层次结构，则负荷行必须指定位置以上的维度，才能分配库存。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475663"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>无法为采用 batch-above 预留层次结构的部分数量发放负荷

## <a name="symptoms"></a>故障特征

当您使用具有 *batch-above* 预留层次结构的物料时，如果尝试发放部分数量的装载，**装载计划工作台** 页面的 **发放到仓库** 命令将不起作用。 您会收到以下错误消息：

> 要分配到波次，负荷行必须指定位置以上的维度。 要分配这些维度，请预留并重新创建负荷行。

但是，当您使用具有 *batch-below* 预留层次结构的物料时，您可以从 **装载计划工作台** 页面发放部分数量的装载。

## <a name="cause"></a>原因

当某个维度在预留层次结构中位于 **库位** 维度上方时，必须在发放到仓库之前指定该维度。 仅在库位上方的维度中没有间隙时才能成功分配库存。

## <a name="resolution"></a>解决方法

通过预留和重新创建负荷行，确保已指定 **位置** 之上的所有维度。
