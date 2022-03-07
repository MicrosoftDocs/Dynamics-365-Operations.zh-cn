---
title: 您无法按主计划物料的相关覆盖范围组值对主计划物料进行筛选
description: 您无法按主计划物料的相关覆盖范围组值对主计划物料进行筛选。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049455"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>您无法按主计划物料的相关覆盖范围组值对主计划物料进行筛选

知识库编号：4612572

## <a name="symptoms"></a>故障特征

您想要根据物料覆盖范围表中相关记录的值来筛选将包含在主计划批处理作业中的物料。 （例如，您想要按 **供应商** 和/或 **覆盖范围组** 值筛选物料）。 批处理作业的筛选器设置允许您创建从 **物料** 表到 **物料覆盖范围** 表的联接，然后在查询中指定物料覆盖范围表中的字段值。 但是，完成此设置后，系统仍将为整个物料覆盖范围创建计划订单，而不只是为与物料覆盖范围表中的指定字段值匹配的物料创建。

## <a name="resolution"></a>解决方法

批处理作业筛选器只能对物料进行筛选。 虽然您可以向 **物料覆盖范围** 表添加联接，但您对该表进行的筛选器设置不会影响查询输出。 运行时，系统将为所有覆盖范围组以及筛选后的物料具有的所有变体运行计划。 物料已包含在运行中后，物料筛选器中包含的任何覆盖范围组都不会影响计划输出。
