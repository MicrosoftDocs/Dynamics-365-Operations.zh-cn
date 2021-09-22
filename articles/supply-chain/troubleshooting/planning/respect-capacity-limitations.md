---
title: 主计划编制的产能超过了可用产能
description: 主计划似乎不遵守产能限制，计划的产能超过可用产能
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
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475702"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>主计划编制的产能超过了可用产能

## <a name="symptoms"></a>故障特征

主计划似乎不遵守产能限制，计划的产能超过可用产能。

当您使用存在有限产能且工艺路线指定资源组和单个资源的混合需要的工序计划编制时，由于算法验证产能冲突的方式，超额预订的可能性较小。 当您使用帮助程序运行主计划时，可能会发生这种超额预订情况。 如果有很多作业的运行时间相对较短，最有可能发生这种情况。

## <a name="resolution"></a>解决方法

如果必须确保工序计划编制不会发生超额预订，可以打开 **主计划参数** 页上的 **工序计划编制的准确有限产能** 选项，让主计划的计划编制部分变为单线程。 此选项默认不可用。 您必须使用个性化功能将其手动添加到页面。 使用此选项时，由于缺少并行处理，计划编制会运行得更慢。
