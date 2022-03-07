---
title: 使用负现有数量进行计划
description: 此主题介绍在使用计划优化时如何处理负现有量。
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 97688e09aae9706dd85e7965aa08c7ea873a44d81391c39406e2e6367660e0d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758536"
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

如果您在存在实际预留时调整库存，则可能会出现针对负库存对订单进行实际预留的情况。 在这种情况下，由于存在实际预留，因此计划优化假设它受现有库存量支持，即使系统中尚未登记现有库存量的收据也不例外。 因此，它认为不需要补货，并且不会创建计划订单来对订单数量进行补货。

以下示例对此情况进行了说明。

### <a name="example"></a>示例

系统按以下方式进行了配置：

- 产品 *FG* 存在并且有 *10* 件 现有库存量。
- 产品配置允许出现实际负库存。
- 存在数量为 *10* 件的 产品 *FG* 的销售订单。
- 按现有库存量实际预留了销售订单数量。

然后，您调整产品 *FG* 的数量，以便现有库存量变为 0（零）。 由于现有产品库存为零，因此现在按负库存预留了销售订单数量。 但是，如果现在运行主计划，将不会创建计划订单来供应销售订单，因为计划优化将认为存在所需的现有库存量，可以供应实际预留。

## <a name="related-resources"></a>相关资源

- [计划优化概览](planning-optimization-overview.md)
- [开始使用计划优化](get-started.md)
- [计划优化拟合分析](planning-optimization-fit-analysis.md)
- [查看计划历史记录和计划日志](plan-history-logs.md)
- [取消计划作业](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
