---
title: "从 Project Service Automation 同步项目支出类别"
description: "本主题介绍用于在 Microsoft Dynamics 365 for Finance and Operations 与 Dynamics 365 for Project Service Automation 之间同步项目支出类别的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>在 Finance and Operations 与 Project Service Automation 之间同步项目支出类别

本主题介绍用于在 Microsoft Dynamics 365 for Finance and Operations 与 Dynamics 365 for Project Service Automation 之间同步项目支出类别的模板和基础任务。

> [!NOTE]
> Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation 和 Finance and Operations 之间的数据传输

Project Service Automation 与 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。 可通过数据集成功能提供的集成模板在 Finance and Operations 与 Project Service Automation 之间传输有关项目支出交易记录类别的数据。

如果项目支出类别掌握在 Finance and Operations 中，则集成流首先从 Finance and Operations 到 Project Service Automation，然后通过从 Project Service Automation 同步到 Finance and Operations 更新项目支出类别集成 ID。

如果项目支出类别掌握在 Project Service Automation 中，则集成流首先从 Project Service Automation 到 Finance and Operations。 从 Project Service Automation 同步之前，必须已在 Finance and Operations 中配置了项目类别。 然后从 Finance and Operations 同步回 Project Service Automation，然后再次从 Project Service Automation 同步到 Finance and Operations。 这样就确保了链接类别，并且不创建重复项。

> [!NOTE]
> 项目支出类别通常掌握在 Finance and Operations 中。 如果您的情况不是这样，或者您已经在 Project Service Automation 中创建了支出类别，则必须首先使用项目支出交易记录类别（PSA 到 Fin and Ops）同步，然后使用项目支出交易记录类别（Fin and Ops 到 PSA）同步。 然后应该再次运行从 PSA 到 Fin and Ops 的同步。

> 如果首先从 Project Service Automation 同步，则必须已在 Finance and Operations 中设置了项目类别，并且必须将需要使用 Project Service Automation 交易记录类别同步的任何项目类别设置为**在日记帐中有效**。

下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目支出类别从 Finance and Operations 同步到 Project Service Automation：

-  **数据集成中的模板名称：** 项目支出交易记录类别（Fin and Ops 到 PSA）
-  **项目中任务的名称：** 将类别同步到 PSA

## <a name="entity-set"></a>实体集

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| 类别的集成实体    | 交易记录类别        |

## <a name="entity-flow"></a>实体流

项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。

## <a name="power-query"></a>Power Query

同步到 Project Service Automation 时，必须使用 Microsoft Power Query 为交易记录类别设置计费类型。 项目支出交易记录类别（Fin and Ops 到 PSA）模板具有一个默认列，并且已提供了映射。 如果创建自己的模板，则必须在 Power Query 中添加一个条件列。
- 从项目支出类别映射任务内打开 “高级查询和筛选”窗体。
- 选择**添加条件列**。
- 为新列指定名称，如 BillingType。
- 输入以下条件：if **CATEGORYID not equal to null then 19235001, Otherwise null**。
- 在列中单击**确定**。
- 请务必在映射页中映射这个新列。

下图显示了数据集成中的模板任务映射的一个示例。 此映射显示将从 Finance and Operations 同步到 Project Service Automation 的字段信息。

[![模板映射](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

以下模板和基础任务用于将项目支出类别从 Project Service Automation 同步到 Finance and Operations：

-**项目中的模板名称：** 项目支出交易记录类别（PSA 到 Fin and Ops）-**项目中的任务名称：** 将类别同步到 Fin Ops

## <a name="entity-set"></a>实体集

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| 交易记录类别          | 类别的集成实体  | 

## <a name="entity-flow"></a>实体流

项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。 同步回 Finance and Operations 将更新 Finance and Operations 项目类别中来自 Project Service Automation 的集成 ID。

下图显示了数据集成中的模板任务映射的一个示例。

> [!NOTE]
> 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

