---
title: 计划优化可扩展性
description: 此主题介绍计划优化中支持的可扩展性方案。
author: ChristianRytt
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e18801a02ae9e904eb5bc597f9f61ed42c537ab9
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651935"
---
# <a name="planning-optimization-extensibility"></a>计划优化可扩展性

[!include [banner](../../includes/banner.md)]

此主题介绍计划优化中支持的与主计划相关的可扩展性方案。 这些功能从 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.13 开始提供。

## <a name="custom-processing-when-master-planning-is-completed"></a>主计划完成时的自定义处理

在计划优化中最常见的可扩展性方案中，自定义处理是在计划更新后完成。 例如，您可能会将列添加到计划订单表 (`ReqPO`)，或者您可能想要从生成的计划派生一些统计信息。 启用这些方案的主要可扩展性点是 `MpsMasterPlanningEvents` 类中的 `jobCompletedSuccessfully` 方法。

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

以下是在计划订单上设置自定义 `CstmOrderPriority` 字段的扩展的示例。

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

添加自定义逻辑时，请考虑以下约束和最佳实践：

- `jobCompletedSuccessfully` 方法在交易范围之外调用。 因此，当自定义逻辑开始运行时，计划已对用户可见。 如果您的自定义在计划订单上设置其他字段，让用户知道这些字段的值最终会保持一致（换句话说，它们可能会在计划作业完成后立即过期），这一点很重要。
- 调用 `jobCompletedSuccessfully` 方法时，可以开始另一个主计划作业。 新作业可能会影响整个计划或计划的一部分。 新作业可能会更新或删除作为在 `jobCompletedSuccessfully` 中处理的计划作业的一部分而创建或更新的相同计划订单或要求交易记录。 扩展此事件时，必须处理更新冲突异常。
- 扩展此方法时避免使用单个交易范围。 单个主计划运行可以生成数百万个要求交易记录和成千上万个计划订单。 如果在单个交易记录范围内处理所有交易记录和计划订单，将会发生很多 SQL 锁定，阻止其他计划流程。 此外，如果长期保留交易记录，将在 SQL 数据库中创建“幽灵记录”。 幽灵记录会对系统中的每个流程产生负面影响。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]