---
title: 将项目实际值直接从 Project Service Automation 同步到 Finance and Operations 中的项目集成日记帐进行过帐
description: 此主题介绍用于将项目实际值直接从 Microsoft Dynamics 365 Project Service Automation 同步到 Finance and Operations 的模板和基础任务。
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250522"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>将项目实际值直接从 Project Service Automation 同步到 Finance and Operations 中的项目集成日记帐进行过帐

[!include[banner](../includes/banner.md)]

此主题介绍用于直接同步 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 的项目实际值的模板和基础任务。

此模板将交易记录从 Project Service Automation 同步到 Finance 中的暂存表内。 同步完成后，**必须**将数据从暂存表导入集成日记帐。

> [!NOTE]
> - 版本 8.0.1 开始支持项目实际值集成。
> - 如果您正在使用 Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。 如果必须重置会计分配，建议也安装 KB 4131710。
> - 如果在使用版本 7.3.0，并从 Project Service Automation 导入免费交易记录，则必须安装 KB 4345320，以便将这些费用添加到该项目发票中。
> - 如果要在 Project Service Automation 中输入时间或支出交易记录的销售税金额，则必须安装 Project Service Automation 更新 7。 否则，将不会把税金实际值链接到关联的时间或支出实际值，因此不会同步到 Finance。 有关详细信息，请联系支持人员。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 到 Finance 的数据传输

Project Service Automation 到 Finance 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance 的实例之间同步数据。 可通过数据集成功能提供的集成模板将有关项目实际值的数据从 Project Service Automation 传输到 Finance。

下图显示 Project Service Automation 与 Finance 之间中如何同步数据。

[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>来自 Project Service Automation 的项目实际值

### <a name="template-and-tasks"></a>模板和任务

若要访问可用模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。

以下模板和基础任务用于将项目实际值从 Project Service Automation 同步到 Finance：

- **数据集成中的模板名称：** 项目实际值（PSA 到 Fin and Ops）
- **项目中的任务名称：**

    - 实际值
    - TransactionConnections

### <a name="entity-set"></a>实体集

| Project Service Automation | 财务                                   |
|----------------------------|----------------------------------------------------------|
| 实际值                    | 项目实际值的集成实体                   |
| 交易记录连接    | 项目交易记录关系的集成实体 |

### <a name="entity-flow"></a>实体流

项目实际值在 Project Service Automation 中管理，并同步到 Finance 中的项目集成日记帐。 将根据默认财务维度和过帐设置应用核算。

### <a name="prerequisites"></a>必备项

必须先配置 Project Service Automation 集成参数并同步项目、项目任务和项目支出类别，才能同步实际值。

### <a name="power-query"></a>Power Query

在项目实际值模板中，必须使用 Microsoft Power Query for Excel 才能完成以下任务：

- 将 Project Service Automation 中的交易记录类型转换为 Finance 中的正确交易记录类型。 已经在项目实际值（PSA 到 Fin and Ops）模板中定义了此项转换。
- 将 Project Service Automation 中的计费类型转换为 Finance 中的正确计费类型。 已经在项目实际值（PSA 到 Fin and Ops）模板中定义了此项转换。 然后将根据 **Project Service Automation 集成参数**页面中的配置把计费类型映射到行属性。
- 筛选出必须使用此模板同步的特定资源组织单位。
- 如果公司间时间或公司间支出实际值将同步到 Finance，您必须在 Finance 中将合同组织单位转换为正确的法人。 在项目实际值（PSA 到 Fin and Ops）模板中已基于演示数据定义了一个条件列。 必须将最后插入的条件列更新为正确的法人。 否则可能出现错误或将不正确的交易记录导入 Finance 中。
- 如果不将公司间时间或公司间支出实际值同步到 Finance，则必须从模板中删除最后插入的条件列。 否则可能出现错误或将不正确的交易记录导入 Finance 中。

#### <a name="contract-organizational-unit"></a>合同组织单位
若要更新模板中插入的条件列，请单击**映射**箭头打开映射。 选择**高级查询和筛选**链接以打开 Power Query。

- 如果在使用默认的项目实际值（PSA 到 Fin and Ops）模板，请在 Power Query, 中从**应用的步骤**部分选择最后一个**插入的条件**。 在**函数**条目中，将 **USSI** 替换为集成应使用的法人 的名称。 根据需要向**函数**条目添加更多条件，然后将 **else** 条件从 **USMF** 更新为正确的法人。
- 如果要新建模板，必须添加此列来为公司间数据和支出提供支持。 选择**添加条件列**，然后为列输入名称，如 **LegalEntity**。 为该列输入条件，其中，如果 **msdyn\_contractorganizationalunitid.msdyn\_name** 为 \<组织单位\>，则 \<输入法人\>，否则为空。

### <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的一个示例。 此映射显示将从 Project Service Automation 同步到 Finance 的字段信息。

[![模板映射](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![模板映射](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>从 Project Service Automation 集成后从暂存表导入

将实际值从 Project Service Automation 同步到 Finance 之后，必须运行“从暂存表导入”定期流程。 此流程将把项目交易记录从暂存表导入 Project Service Automation 集成日记帐中，可在其中应用核算和过帐导入的交易记录。 建议以批处理模式运行此流程；可以选择将其设置为以重复执行的批处理运行。

## <a name="update-actuals-from-finance"></a>从 Finance 更新实际值

### <a name="template-and-tasks"></a>模板和任务

以下模板和基础任务用于将所过帐项目交易记录的凭证号和销售税从 Finance 同步到 Project Service Automation：

- **数据集成中的模板名称：** 项目实际值更新（Fin Ops 到 PSA）
- **项目中的任务名称：**

    - 实际值 
    - TransactionConnections

### <a name="entity-set"></a>实体集

| 财务                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| 项目实际值的集成实体                   | 实际值                    |
| 项目交易记录关系的集成实体 | 交易记录连接    |

### <a name="entity-flow"></a>实体流

项目实际值在 Project Service Automation 中管理，并同步到 Finance 中的项目集成日记帐。 实际值在 Finance 中过帐之后，将在 Project Service Automation 中使用来自 Finance 的凭证号更新。 如果在 Finance 中添加了销售税，将在 Project Service Automation 中创建新的税金实际值。

### <a name="power-query"></a>Power Query

在项目实际值更新模板中，必须使用 Power Query 才能完成以下任务：

- 将 Finance 中的交易记录类型转换为 Project Service Automation 中的正确交易记录类型。 已经在项目实际值更新（Fin Ops 到 PSA）模板中定义了此项转换。
- 将 Finance 中的计费类型转换为 Project Service Automation 中的正确计费类型。 已经在项目实际值更新（Fin Ops 到 PSA）模板中定义了此项转换。

### <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板任务映射的示例。 此映射显示将从 Finance 同步到 Project Service Automation 的字段信息。

[![模板映射](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![模板映射](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
