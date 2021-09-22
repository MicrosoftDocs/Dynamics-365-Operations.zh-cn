---
title: 生产计划不考虑安全宽限期
description: 生产计划不会考虑在限定供应的物料覆盖范围上设置的安全宽限期
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
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475667"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>生产计划不考虑安全宽限期

## <a name="symptoms"></a>故障特征

主计划会考虑安全宽限期。 但是，安全宽限期会在计划生产订单时被忽略。

## <a name="resolution"></a>解决方法

仅在主计划期间考虑宽限期，手动计划期间不会考虑。 宽限期的目的是在计划阶段充当缓冲，为实际流程提供一定的“余地”。

要获得所需的结果，您可以删除宽限期。 然后必须更新工艺路线，使其包含所需的时间（例如，排队时间）。 然后，主计划和手动计划应该都会产生相同的结果。
