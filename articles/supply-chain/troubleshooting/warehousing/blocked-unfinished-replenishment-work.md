---
title: 补货工作未完成导致领料工作锁定
description: 领料工作可能由于有依赖的补货工作被锁定。 请完成补货工作，然后再处理领料工作。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475734"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>领料工作由于依赖的补货工作未完成不能解锁

## <a name="symptoms"></a>故障特征

在使用波次需求补货时，可能因为依赖补货工作导致领料工作锁定。 如果必须为某个领料位置补货以满足源订单需求，系统将同时创建补货工作和领料工作。 但是，将把领料工作锁定到补货工作完成，并且您将收到以下错误消息：

> 工作 %1 不能解锁，因为它包含未完成的补货工作。

## <a name="resolution"></a>解决方法

此行为是有意的，因为除非补货工作完成，否则领料位置会没有足够的库存。 请完成补货工作，然后再处理领料工作。
