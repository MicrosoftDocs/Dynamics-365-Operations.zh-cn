---
title: 主计划疑难解答
description: 本主题介绍如何解决在使用主计划时可能遇到的问题。
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4dc3c5c8a1597fce4cc61461d16cd11ad80426eb8841871278772fcd7b8c86b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766623"
---
# <a name="troubleshoot-master-planning"></a>主计划疑难解答

本主题介绍如何解决在使用主计划时可能遇到的问题。

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>物料清单分解行为对于确定的生产订单和人工创建工作的估计生产订单是不同的。

### <a name="issue-description"></a>问题描述

生产订单确定后，物料在您分解物料清单 (BOM) 时不会分解。 但是，当您手动创建工作订单然后估计生产订单时，物料将被分解。

### <a name="issue-resolution"></a>解决问题

系统按预期运行。 确定生产订单时发生的分解将指向计划订单，但似乎计划订单在这种情况下目前不会确定。 但是，如果已经估计了生产订单，分解将从不存在计划订单的已下达生产订单触发。

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>当我重新计划计划订单时，延迟值不更新。

要更新计划订单的延迟，请打开计划订单的 **重新计划** 对话框。 在 **分解** 快速选项卡上，确保将 **重新计划后执行分解** 选项设置为 *是*。

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>生产计划不会考虑在限定供应的物料覆盖范围上设置的安全宽限期。

### <a name="issue-description"></a>问题描述

主计划会考虑安全宽限期。 但是，安全宽限期会在计划生产订单时被忽略。

### <a name="issue-resolution"></a>解决问题

仅在主计划期间考虑宽限期，手动计划期间不会考虑。 宽限期的目的是在计划阶段充当缓冲，为实际流程提供一定的“余地”。

要获得所需的结果，您可以删除宽限期。 然后必须更新工艺路线，使其包含所需的时间（例如，排队时间）。 然后，主计划和手动计划应该都会产生相同的结果。

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>计划订单将生成，即使我们在库存中有物料，并且它们已经存在生产订单。

您可以通过在 **覆盖范围组** 页上为相关组增加 **正天数** 值来解决此问题。 此更改会让系统确定现有库存量是否可用于需求。 之后就不会为库存中的物料生成新的计划订单。

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>主计划似乎不遵守产能限制，计划的产能超过可用产能。

### <a name="issue-description"></a>问题描述

当您使用存在有限产能且工艺路线指定资源组和单个资源的混合需要的工序计划编制时，由于算法验证产能冲突的方式，超额预订的可能性较小。 当您使用帮助程序运行主计划时，可能会发生这种超额预订情况。 如果有很多作业的运行时间相对较短，最有可能发生这种情况。

### <a name="issue-resolution"></a>解决问题

如果必须确保工序计划编制不会发生超额预订，可以打开 **主计划参数** 页上的 **工序计划编制的准确有限产能** 选项，让主计划的计划编制部分变为单线程。 此选项默认不可用。 您必须使用个性化功能将其手动添加到页面。 使用此选项时，由于缺少并行处理，计划编制会运行得更慢。

## <a name="planned-orders-take-a-long-time-to-update"></a>计划订单需要很长时间来更新。

### <a name="issue-description"></a>问题描述

更新计划订单上的需求数量和/或交货日期时，每个订单保存更新通常至少需要 30 秒。

### <a name="issue-resolution"></a>解决问题

这是内置的主计划引擎的一个已知问题。 它是由编辑期间物料清单结构的基础自动分解引起的。 此问题在计划优化中得到了解决，规划员可以在其中更新和审核相关订单，并可以在需要时触发计划运行来更新基础物料清单结构的计划订单。

使用内置的主计划引擎提高性能的一种方法是执行以下操作：

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**。
1. 选择一个计划。
1. 展开 **按天计算的时限** 快速选项卡。
1. 将 **分解** 设置为 *是*，将将此设置下方的字段设置为 0（零）。

> [!NOTE]
> 这会将为这个主计划执行的分解的期间限制为一天。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]