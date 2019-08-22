---
title: 在 Finance and Operations 与 Project Service Automation 之间同步项目支出类别
description: 此主题介绍用于直接同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Project Service Automation 之间的项目费用类别的模板和基础任务。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838359"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>在 Finance and Operations 与 Project Service Automation 之间同步项目支出类别

[!include[banner](../includes/banner.md)]

此主题介绍用于直接同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Project Service Automation 之间的项目费用类别的模板和基础任务。

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
> - Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本中支持实际值集成。
> - 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。 如果必须重置会计分配，建议也安装 KB 4131710。

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Project Service Automation 和 Finance and Operations 之间的数据传输

Project Service Automation 与 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。 可通过数据集成功能提供的集成模板在 Finance and Operations 与 Project Service Automation 之间传输有关项目支出交易记录类别的数据。

如果项目支出类别掌握在 Finance and Operations 中，则集成流首先从 Finance and Operations 到 Project Service Automation.。 然后，通过从 Project Service Automation 到 Finance and Operations 的同步更新项目支出类别的集成 ID。

如果项目支出类别掌握在 Project Service Automation 中，则集成流首先从 Project Service Automation 到 Finance and Operations。 从 Project Service Automation 同步之前，必须已在 Finance and Operations 中配置了项目类别。 然后从 Finance and Operations 同步回 Project Service Automation，然后再次从 Project Service Automation 同步到 Finance and Operations。 这样就可以帮助确保链接类别，并且不创建重复项。

> [!NOTE]
> 项目支出类别通常掌握在 Finance and Operations 中。 但是，如果掌握在 Finance and Operations 中，或者如果已在 Project Service Automation 中创建了支出类别，则必须首先通过使用支出交易记录类别（PSA 到 Fin and Ops）模板进行同步。 然后通过使用项目支出交易记录类别（Fin and Ops 到 PSA）模板进行同步。 然后应再次运行从 Project Service Automation 到 Finance and Operations 的同步。
>
> 如果首先从 Project Service Automation 同步，则必须先在 Finance and Operations 中满足以下要求，才能运行同步。
>
> - 必须有与 Project Service Automation 中设置的项目类别匹配的共享类别，并且必须同时为**项目**和**支出**启用该共享类别。
> - 对于必须集成的每个 Finance and Operations 法人，必须有以下项目类别：
>
>     - 有**项目类别**。 
>     - 已启用**在支出使用**。
>     - 已启用**在日记帐中有效**。
>     - **交易记录类型**设置为**支出**。

下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>从 Finance and Operations 到 Project Service Automation 的项目支出类别同步

### <a name="template-and-task"></a>模板和任务

若要访问此模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目支出类别从 Finance and Operations 同步到 Project Service Automation：

- **数据集成中的模板名称：** 项目支出交易记录类别（Fin and Ops 到 PSA）
- **项目中任务的名称：** 将类别同步到 PSA

### <a name="entity-set"></a>实体集

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| 类别的集成实体 | 交易记录类别     |

### <a name="entity-flow"></a>实体流

项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。

### <a name="power-query"></a>Power Query

同步到 Project Service Automation 时，必须使用 Microsoft Power Query for Excel 为交易记录类别设置计费类型。 项目支出交易记录类别（Fin and Ops 到 PSA）提供默认列和映射。 如果创建自己的模板，则必须在 Power Query 中添加一个条件列。 执行以下步骤。

1. 单击箭头在项目支出交易记录类别（Fin and Ops 到 PSA）模板中打开项目支出类别任务的映射。
2. 单击**高级查询和筛选**链接以打开 Power Query。
2. 选择**添加条件列**。
3. 为新列输入名称，如 **BillingType**。
4. 输入以下条件：**if CATEGORYID not equal to null then 19235001, Otherwise null**。
5. 在列中单击**确定**。
6. 请务必在映射页上映射这个新列。

下图显示了数据集成中的模板任务映射的一个示例。 此映射显示将从 Finance and Operations 同步到 Project Service Automation 的字段信息。

[![模板映射](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>从 Project Service Automation 到 Finance and Operations 的项目支出类别同步

### <a name="template-and-task"></a>模板和任务

以下模板和基础任务用于将项目支出类别从 Project Service Automation 同步到 Finance and Operations：

- **数据集成中的模板名称：** 项目支出交易记录类别（PSA 到 Fin and Ops）
- **项目中任务的名称：** 将类别同步到 Fin Ops

### <a name="entity-set"></a>实体集

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| 交易记录类别     | 类别的集成实体 |

### <a name="entity-flow"></a>实体流

项目支出类别掌握在 Finance and Operations 中，并且作为交易记录类别同步到 Project Service Automation。 同步回 Finance and Operations 将更新 Finance and Operations 项目类别中来自 Project Service Automation 的项目类别。

### <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的一个示例。

> [!NOTE]
> 此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。

[![模板映射](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
