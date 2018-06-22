---
title: "将项目估计值从 Project Service Automation 直接同步到 Finance and Operations 中的项目预测"
description: "本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Dynamics 365 for Finance and Operations 的模板和基础任务。"
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>将项目估计值从 Project Service Automation 直接同步到 Finance and Operations 中的项目预测

本主题介绍用于将项目工时估计值和项目支出估计值直接从 Microsoft Dynamics 365 for Project Service Automation 到 Dynamics 365 for Finance and Operations 的模板和基础任务。

> [!NOTE]
> Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation 到 Finance and Operations 的数据传输

Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。 可通过数据集成功能提供的集成模板将有关项目工时估计值和项目支出估计值的数据从 Project Service Automation 传输到 Finance and Operations。

下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>模板和任务

若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目工时估计值从 Project Service Automation 同步到 Finance and Operations：

-  **数据集成中的模板名称：** 项目工时估计值（PSA 到 Fin and Ops）

-  **项目中的任务名称：** 
    - 交易记录关系 
    - 支出估计值

## <a name="entity-set"></a>实体集

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| 项目任务                   | 项目工时估计集成实体   |

## <a name="entity-flow"></a>实体流

项目工时估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目工时预测。

## <a name="preconditions"></a>前提条件

必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目工时估计值。

## <a name="power-query"></a>Power Query

必须在项目工时估计值模板中使用 Microsoft Power Query 才能：
- 设置将在集成新建工时预测时使用的**预测模型 ID**。
- 筛选掉任务中所有资源特定的且将导致与工时预测集成失败的记录。
- 筛选掉所有空交易记录类别行。 如果失败，可能导致工时预测不正确。

### <a name="forecast-model-id"></a>预测模型 ID
若要更新模板中的默认预测模型 ID，请单击**映射**箭头打开映射。 选择打开“高级查询和筛选”。
- 如果在使用默认的 Microsoft 项目工时估计值（PSA 到 Fin and Ops）模板，请在**应用的步骤**部分中选择**插入的条件**。 在**函数**条目中，将 **O_forecast** 替换为集成应使用的**预测模型 ID** 的名称。 默认模板中包含来自一个演示数据的预测模型 ID。
- 如果要创建新模板，必须添加此列。 选择**添加条件列**并为列命名，如 ModelID。 输入列的条件：if Project task is not null, then<enter the forecast model ID>; else null。

### <a name="filter-out-resource-specific-records"></a>筛选掉资源特定的记录
项目工时估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于去除资源特定的所有记录。 如果创建自己的模板，则必须添加这个筛选器。 在“高级查询和筛选”窗体中，选择将列 **msdyn_islinetask** 筛选为仅包含 **False** 记录。

### <a name="filter-out-empty-transaction-category-rows"></a>筛选掉空交易记录类别行
必须添加筛选器以移除交易记录类别为空的所有行。 无论使用默认模板还是创建自己的模板，都需要执行此操作。 此筛选器将移除来自 Project Service Automation 且可能导致 Finance and Operations 中的工时预测不正确的所有汇总行。 在“高级查询和筛选”窗体中，选择筛选掉列 **msdyn_transactioncategory_value** 中的空记录。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的一个示例。 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

以下模板和基础任务用于将项目支出估计值从 Project Service Automation 同步到 Finance and Operations：

-  **数据集成中的模板名称：** 项目支出估计值（PSA 到 Fin and Ops）
-  **项目中的任务名称：** 
     - 交易记录关系 
     - 支出估计值

## <a name="entity-set"></a>实体集

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| 交易记录连接         | 项目交易记录关系的集成实体。   |
| 估计值行                  | 项目费用估计值的集成实体。           |

## <a name="entity-flow"></a>实体流

项目支出估计值在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目支出预测。

## <a name="prerequisites"></a>必备项

必须先同步项目、项目任务和项目支出交易记录类别，才能同步项目支出估计值。

## <a name="power-query"></a>Power Query

必须在项目支出估计值模板中使用 Microsoft Power Query 才能：
- 筛选为仅包含支出估计值行记录
- 设置将在集成新建工时预测时使用的**预测模型 ID**。
- 转换计费类型。
- 转换交易记录类型。

### <a name="filter-to-include-only-expense-estimate-lines"></a>筛选为仅包含支出估计值行
项目支出估计值（PSA 到 Fin and Ops）模板有一个默认筛选器，用于筛选为集成中仅包含支出行。 如果创建自己的模板，则必须添加这个筛选器。 选择“交易记录关系”任务，然后单击**映射**箭头。 选择**高级查询和筛选**。 将 **msdyn_transactiontype1**列筛选为仅包含 **msdyn_estimateline**。

### <a name="forecast-model-id"></a>预测模型 ID
若要更新模板中的默认预测模型 ID，对于“支出估计值”任务，请单击**映射**箭头打开映射。 选择打开“高级查询和筛选”。
- 如果在使用默认的 Microsoft 项目支出估计值（PSA 到 Fin and Ops）模板，请在**应用的步骤**部分中选择第一个**插入的条件**。 在**函数**条目中，将 **O_forecast** 替换为集成应使用的**预测模型 ID** 的名称。 默认模板中包含来自一个演示数据的预测模型 ID。
- 如果要创建新模板，必须添加此列。 选择**添加条件列**并为列命名，如 ModelID。 输入列的条件：如果估计值行 ID 非空，则 < enter the forecast model ID >；否则为空。

### <a name="transform-the-billing-types"></a>转换计费类型
项目支出估计值（PSA 到 Fin and Ops）模板增加了一个条件列，用于转换集成期间从 Project Service Automation 收到的计费类型。
- 如果创建自己的模板，则必须添加这个条件列。 在"高级查询和筛选"窗体中，选择**添加条件列**。 为该列指定名称，如“BillingType”。 要输入的条件如下所示：

    If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**

### <a name="transform-the-transaction-types"></a>转换交易记录类型
项目支出估计值（PSA 到 Fin and Ops）模板增加了一个条件列，用于转换集成期间从 Project Service Automation 收到的交易记录类型。
- 如果创建自己的模板，则必须添加这个条件列。 在"高级查询和筛选"窗体中，选择**添加条件列**。 为该列指定名称，如“TransactionType”。 要输入的条件如下所示：**msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的示例。 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![模板映射](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




