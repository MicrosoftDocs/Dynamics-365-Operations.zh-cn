---
title: 使用负现有数量进行计划
description: 本文介绍在使用计划优化时如何处理负现有量。
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04006bb12142be69c84bc8085dd82fc99280e90b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856126"
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

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>计划何时按负现有库存量进行预留

如果您在存在实际预留时调整库存，则可能会出现针对负库存对订单进行实际预留的情况。 在这种情况下，由于存在实际预留，您需要有供应才能满足预留数量。 因此，需要补货，因此系统将创建计划订单来补充现有库存无法满足的数量，或者使用该物料的现有订单来满足此数量。

以下示例对此情况进行了说明。

### <a name="example"></a>示例

系统按以下方式进行了配置：

- 产品 *FG* 存在并且有 *10* 件 现有库存量。
- 产品配置允许出现实际负库存。
- 存在数量为 *10* 件的 产品 *FG* 的销售订单。
- 按现有库存量实际预留了销售订单数量。

然后，您调整产品 *FG* 的数量，以便现有库存量变为 5。 由于现有产品库存为 5，因此现在针对不可用的现有数量预留了销售订单数量（如果现有量为 0，则情况类似，在这种情况下，将针对负库存预留销售订单 ）。 如果现在运行主计划，将创建 *FG* 数量为 5 的计划订单来供应销售订单，因为计划优化将始终使用现有供应或创建新计划订单来供应实际预留。

## <a name="related-resources"></a>相关资源

- [计划优化概览](planning-optimization-overview.md)
- [开始使用计划优化](get-started.md)
- [计划优化拟合分析](planning-optimization-fit-analysis.md)
- [查看计划历史记录和计划日志](plan-history-logs.md)
- [取消计划作业](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
