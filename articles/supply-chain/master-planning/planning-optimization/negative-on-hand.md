---
title: 使用负现有数量进行计划
description: 此主题介绍在使用计划优化时如何处理负现有量。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422969"
---
# <a name="planning-with-negative-on-hand-quantities"></a>使用负现有数量进行计划

[!include [banner](../../includes/banner.md)]

如果系统显示负聚合现有数量，计划引擎将把该数量视为 0（零），以帮助避免超额供应。 下面是此功能的工作原理：

1. 计划优化功能聚合较低级别覆盖范围维度的现有数量。 （例如，如果 *库位* 不是覆盖范围维度，则计划优化聚合 *仓库* 级别的现有数量。）
1. 如果最低级别覆盖范围维度的聚合现有数量为负，系统将假设现有数量的确为 0（零）。

> [!IMPORTANT]
> 计划系统的精确程度只能达到输入数据的程度。 如果输入数据不准确，负现有记录将指示 Microsoft Dynamics 365 Supply Chain Management 中的库存信息与现实不同步。 因此，计划结果将有瑕疵。 若要获取精确的计划结果，应该尽量减少显示负现有数量的记录的数量。

## <a name="example-1"></a>示例 1

仓库 13 的配置方式如下：

- **覆盖范围代码：** 最小值/最大值
- **最小值：** 15 件
- **最大值：** 25 件

覆盖范围维度的最低级别为 *仓库*，而以下现有数量的记录级别为 *库位*：

- **站点 1，仓库 13，库位 1：** 20 件
- **站点 1，仓库 13，库位 2：**&minus;8 件

因此，仓库 13 的聚合现有数量为 12 件 （= 20 件 &minus; 8 件）。

在此情况下，计划引擎对仓库 13 使用聚合现有数量 12 件 。

结果是，计划的订单为 13 件 （= 25 件 &minus; 12 件）以将仓库 13 从 12 件装 到 25 件。

## <a name="example-2"></a>示例 2

仓库 13 的配置方式如下：

- **覆盖范围代码：** 最小值/最大值
- **最小值：** 15 件
- **最大值：** 25 件

覆盖范围维度的最低级别为 *仓库*，而以下现有数量的记录级别为 *库位*：

- **站点 1，仓库 13，库位 1：** 4 件
- **站点 1，仓库 13，库位 2：**&minus;8 件

因此，仓库 13 的聚合现有数量为 &minus;4 件 （= 4 件 &minus; 8 件）。 换句话说，小于 0（零）。

在此情况下，计划引擎假设仓库 13 的现有数量为 0 件， 而不是 &minus;4 件。

结果是，计划的订单为 25 件 （= 25 件 &minus; 0 件）以将仓库 13 从 0 件装 到 25 件。

## <a name="related-resources"></a>相关资源

[计划优化概览](planning-optimization-overview.md)

[开始使用计划优化](get-started.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[取消计划作业](cancel-planning-job.md)
