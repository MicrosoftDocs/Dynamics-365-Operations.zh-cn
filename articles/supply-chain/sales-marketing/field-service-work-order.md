---
title: 将 Field Service 中的工作订单同步到 Supply Chain Management 中的销售订单
description: 本主题讨论用于将 Field Service 中的工作订单同步到 Supply Chain Management 中的销售订单的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f9395d39a68cd11f57262c791dd7646975c5e516
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998495"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>将 Field Service 中的工作订单同步到 Supply Chain Management 中的销售订单

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本主题讨论用于将 Dynamics 365 Field Service 中的工作订单同步到 Dynamics 365 Supply Chain Management 中的销售订单的模板和基础任务。

[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>模板和任务

以下模板和基础任务用于运行 Field Service 中的工作订单到 Supply Chain Management 中的销售订单的同步。

### <a name="names-of-the-templates-in-data-integration"></a>数据集成中的模板名称

**工作订单到销售订单（Field Service 到 Supply Chain Management）** 模板用于运行同步。

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>数据集成项目中的任务名称

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

在发生销售订单标头和行同步前，需要执行以下同步任务：

- Field Service 产品（Supply Chain Management 到 Field Service）
- 科目（Sales 到 Supply Chain Management）- 直接

## <a name="entity-set"></a>实体集

| **Field Service** | **供应链管理** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse 销售订单标头 |
| msdyn_workorderservices | Dataverse 销售订单行   |
| msdyn_workorderproducts | Dataverse 销售订单行   |

## <a name="entity-flow"></a>实体流

工作订单在 Field Service 中创建。 如果工作订单中仅包含外部维护的产品，并且 **工作订单状态** 值与 **打开 - 未计划** 和 **已关闭 – 已取消** 不同，则可通过 Microsoft Dataverse 数据集成项目将工作订单同步到 Supply Chain Management。 对工作订单的更新将在 Supply Chain Management 中作为销售订单同步。 这些更新中包含有关原始类型和状态的信息。

## <a name="estimated-versus-used"></a>估计与已使用

在 Field Service 中，工作订单内的产品和服务的数量和金额都有 **估计** 值和 **已使用** 值。 但是在 Supply Chain Management 中，销售订单没有相同的 **估计** 和 **已使用** 值概念。 若要在 Supply Chain Management 中为对销售订单使用预期数量的产品分配提供支持，但保留应消耗和开票的已使用数量，则需要通过两组任务同步工作订单中的产品和服务。 一组任务针对 **估计** 值，另一组任务针对 **已使用** 值。

此行为支持以下场景：估计值在 Supply Chain Management 中用于分配或保留，而已使用值则用于消耗和开票。

### <a name="estimated"></a>估计

要同步产品行，则在 **行状态** 值为 **估计**，**已分配** 选项设置为 **是** 且 **系统状态** 值不是 **已关闭 – 已过帐** 时，使用 **估计** 值。

要同步服务行，则在 **行状态** 值为 **估计** 且 **系统状态** 值不是 **已关闭 – 已过帐** 时，使用 **估计** 值。

### <a name="used"></a>已使用

**已使用** 值用于消耗和开票。 在这些情况下，将同步 **已使用** 值。

下表概述各种产品行组合。

| 系统状态 <br>(Field Service) | 行状态 <br>(Field Service) | 已分配 <br>(Field Service) |同步的值 <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| 打开 - 已计划   | 估计   | 是       | 估计                       |
| 打开 - 已计划   | 估计   | 无        | 已使用                            |
| 打开 - 已计划   | 已使用        | 是       | 已使用                            |
| 打开 - 已计划   | 已使用        | 无        | 已使用                            |
| 打开 - 正在进行 | 估计   | 是       | 估计                       |
| 打开 - 正在进行 | 估计   | 无        | 已使用                            |
| 打开 - 正在进行 | 已使用        | 是       | 已使用                            |
| 打开 - 正在进行 | 已使用        | 无        | 已使用                            |
| 打开 - 已完成   | 估计   | 是       | 估计                       |
| 打开 - 已完成   | 估计   | 无        | 已使用                            |
| 打开 - 已完成   | 已使用        | 是       | 已使用                            |
| 打开 - 已完成   | 已使用        | 无        | 已使用                            |
| 已关闭 - 已过帐    | 估计   | 是       | 已使用                            |
| 已关闭 - 已过帐    | 估计   | 无        | 已使用                            |
| 已关闭 - 已过帐    | 已使用        | 是       | 已使用                            |
| 已关闭 - 已过帐    | 已使用        | 无        | 已使用                            |

下表概述各种服务行组合。

| 系统状态 <br>(Field Service) | 行状态 <br>(Field Service) | 同步的值 <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| 打开 - 已计划   | 估计   | 估计 |
| 打开 - 已计划   | 已使用        | 已使用      |
| 打开 - 正在进行 | 估计   | 估计 |
| 打开 - 正在进行 | 已使用        | 已使用      |
| 打开 - 已完成   | 估计   | 估计 |
| 打开 - 已完成   | 已使用        | 已使用      |
| 已关闭 - 已过帐    | 估计   | 已使用      |
| 已关闭 - 已过帐    | 已使用        | 已使用      |

可通过两组任务管理产品行和服务行的 **估计** 值与 **已使用** 值同步。 预定义的筛选器将触发正确的任务，而基础映射则帮助确保同步正确的 **预期** 值与 **已使用** 值。

### <a name="example"></a>示例

1. 在 Field Service 中创建并计划工作订单。

    **系统状态** 值为 **打开 – 已计划**。

    - **产品行：** 估计数量 = 5ea，已使用数量 = 0ea，行状态 = 估计，已分配 = 否
    - **服务行：** 估计数量 = 2h，已使用数量 = 0h，行状态 = 估计

    在此示例中，将把产品的 **已使用数量** 值 **0**（零）和服务的 **估计数量** 值 **2h** 同步到 Supply Chain Management。

2. 将在 Field Service 中分配产品。

    **系统状态** 值为 **打开 – 已计划**。

    - **产品行：** 估计数量 = 5ea，已使用数量 = 0ea，行状态 = 估计，已分配 = 是
    - **服务行：** 估计数量 = 2h，已使用数量 = 0h，行状态 = 估计

    在此示例中，将把产品的 **估计数量** 值 **5ea** 和服务的 **估计数量** 值 **2h** 同步到 Supply Chain Management。

3. 服务技术人员开始处理工作订单，并登记材料用量 6。

    **系统状态** 值为 **打开 – 正在进行**。

    - **产品行：** 估计数量 = 5ea，已使用数量 = 6ea，行状态 = 已使用，已分配 = 是
    - **服务行：** 估计数量 = 2h，已使用数量 = 0h，行状态 = 估计

    在此示例中，将把产品的 **已使用数量** 值 **6** 和服务的 **估计数量** 值 **2h** 同步到 Supply Chain Management。

4. 服务技术人员将完成工作订单，并登记1.5 小时的已使用时间 。

    **系统状态** 值为 **打开 – 已完成**。

    - **产品行：** 估计数量 = 5ea，已使用数量 = 6ea，行状态 = 已使用，已分配 = 是
    - **服务行：** 估计数量 = 2h，已使用数量 = 1.5h，行状态 = 已使用

    在此示例中，将把产品的 **已使用数量** 值 **6** 和服务的 **已使用数量** 值 **1.5h** 同步到 Supply Chain Management。

## <a name="sales-order-origin-and-status"></a>销售订单来源和状态

### <a name="sales-origin"></a>销售订单来源

要跟踪源自工作订单的销售订单，可创建销售订单来源，其中的 **来源类型分配** 选项设置为 **是**，**销售订单来源类型** 字段设置为 **工作订单集成**。

默认情况下，映射为通过工作订单创建的所有销售订单选择 **工作订单集成** 销售订单来源类型的销售订单来源。 在 Supply Chain Management 中处理销售订单时，此行为可能非常有用。 必须确保不将源自工作订单的销售订单作为工作订单同步回 Field Service。

有关如何在 Supply Chain Management 中创建正确的销售订单来源设置的详细信息，请参阅本主题中的“先决条件和映射设置”部分。

### <a name="status"></a>状态

如果销售订单源自工作订单，则销售订单头的 **设置** 选项卡上将显示 **外部工作订单状态**。 此字段显示 Field Service 中的工作订单的系统状态，帮助跟踪 Supply Chain Management 中销售订单的同步后工作订单状态。 此字段还帮助用户确定应何时为销售订单发货或开票。

**外部工作订单状态** 字段可具有以下值：

- 打开 - 已计划
- 打开 - 正在进行
- 打开 - 已完成
- 已关闭 - 已过帐

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案

若要为 Field Service 与 Supply Chain Management 之间的同步提供支持，需要 Field Service CRM 解决方案的更多功能。 此解决方案中包含以下更改。

### <a name="work-order-entity"></a>工作订单实体

**仅具有外部维护的产品** 字段已添加到 **工作订单** 实体并在页面中显示。 用于持续跟踪工作订单是否完全由外部维护的产品构成。 如果所有相关产品在 Supply Chain Management 中进行维护，则工作订单完全由外部维护的产品构成。 此字段有助于保障用户不同步具有未知产品的工作订单。

### <a name="work-order-product-entity"></a>工作订单产品实体

- **订单仅具有外部维护的产品** 字段已添加到 **工作订单产品** 实体并在页面中显示。 用于持续跟踪工作订单产品是否在 Supply Chain Management 中维护。 此字段有助于保障用户不同步 Supply Chain Management 不认识的工作订单产品。
- **标头系统状态** 字段已添加到 **工作订单产品** 实体并在页面中显示。 用于持续跟踪工作订单的系统状态，并在将工作订单产品同步到 Supply Chain Management 时帮助确保正确筛选。 如果为集成任务设置了筛选器，还将使用 **标头系统状态** 信息确定应该同步估计值还是已使用值。
- **开票单位金额** 字段显示按所用实际单位开票的金额。 该值的计算方法是 **总金额** 值除以 **实际数量** 值。 此字段用于与不支持已使用数量和开单数量使用不同值的系统集成。 用户界面 (UI) 中不显示此字段。 
- **开票折扣金额** 字段的计算方法是 **折扣金额** 值加上 **开票单位金额** 值计算的化整结果。 此字段用于集成，不在 UI 中显示。
- **小数数量** 字段将 **数量** 字段的值作为小数存储。 此字段用于集成，不在 UI 中显示。 
- 如果工作订单产品的 **行状态** 值从 **已使用** 更改为 **估计**，**已使用** 字段中的值将重置为 **0**（零）。 此项更改有助于防止出现下面的情况：**行状态** 值为 **估计** 且 **已分配** 选项设置为 **否** 时，使用误输入的已使用数量进行同步。

### <a name="work-order-service-entity"></a>工作订单服务实体

- **订单仅具有外部维护的产品** 字段已添加到 **工作订单服务** 实体并在页面中显示。 用于持续跟踪工作订单服务是否在 Supply Chain Management 中维护。 此字段有助于保障用户不同步 Supply Chain Management 不认识的工作订单服务。
- **标头系统状态** 字段已添加到 **工作订单服务** 实体并在页面中显示。 用于持续跟踪工作订单的系统状态，并在将工作订单服务同步到 Supply Chain Management 时帮助确保正确筛选。 如果为集成任务设置了筛选器，还将使用 **标头系统状态** 信息确定应该同步估计值还是已使用值。
- **持续时间(小时)** 字段中存储 **持续时间** 字段的值从分钟转换为小时后的值。 此字段用于集成，不在 UI 中显示。
- **估计的持续时间(小时)** 字段中存储 **估计的持续时间** 字段的值从分钟转换为小时后的值。 此字段用于集成，不在 UI 中显示。
- **开票单位金额** 字段中存储按所用实际单位开票的金额。 该值的计算方法是 **总金额** 值除以 **实际数量** 值。 此字段用于与不支持已使用数量和开单数量使用不同值的系统集成。 UI 中不显示此字段。
- **开票折扣金额** 字段的计算方法是 **折扣金额** 值加上 **开票单位金额** 值计算的化整结果。 此字段用于集成，不在 UI 中显示。
- **外部行订单** 字段是计算出的负行订单编号，可在组合使用工作订单产品和服务行的外部系统中使用。 此字段让插入的工作订单产品可以有正行号，让工作订单服务可以有负行号。 此字段的值的计算方法是 **行订单** 值乘以 -1。 UI 中不显示此字段。
- 如果因为某个原因导致工作订单服务的 **行状态** 值从 **已使用** 更改为 **估计**，**已使用** 字段中的值将重置为 **0**（零）。 此项更改有助于防止出现下面的情况：**行状态** 值为 **估计** 且 **标头系统状态** 值为 **已关闭 - 已过帐** 时，使用误输入的已使用数量进行同步。

## <a name="preconditions-and-mapping-setup"></a>先决条件和映射设置

在同步工作订单前，更新系统中的下列设置十分重要。

### <a name="setup-in-field-service"></a>Field Service 中的设置

- 确保 Field Service 中用于工作订单的编号系列不与 Supply Chain Management 中用于销售订单的编号规则重合。 否则，可能会在 Field Service 或 Supply Chain Management 中错误地更新现有销售订单。
- 必须将 **工作订单发票创建** 字段设置为 **从不**，因为将从 Supply Chain Management 执行开票。 转至 **Field Service** \> **设置** \> **管理** \> **Field Service 设置**，确保 **工作订单发票创建** 字段设置为 **从不**。

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management 中的设置

工作订单集成需要您设置销售订单来源。 销售订单来源用于分辨 Supply Chain Management 中创建自 Field Service 中的工作订单的销售订单。 如果销售订单的销售订单来源类型为 **工作订单集成**，则销售订单头中将显示 **外部工作订单状态** 字段。 此外，销售订单来源有助于确保将销售订单从 Supply Chain Management 同步到 Field Service 期间过滤掉创建自 Field Service 中的工作订单的销售订单。

1. 转到 **销售和市场营销** \> **设置** \> **销售订单** \> **销售订单来源**。
2. 选择 **新建** 创建新的销售订单来源。
3. 在 **销售订单来源** 字段中，输入销售订单来源的名称，如 **WorkOrder**。
4. 在 **描述** 字段中，输入描述，如 **Field Service 工作订单**。
5. 选中 **来源类型分配** 复选框。
6. 将 **销售订单来源类型** 字段设置为 **工作订单集成**。
7. 选择 **保存**。


### <a name="setup-in-data-integration"></a>数据集成中的设置

确保有 **msdyn_workorders** 的 **集成键**
1. 转至“数据集成”
2. 选择 **连接集** 选项卡
3. 选择用于工作订单同步的连接集
4. 选择 **集成键** 选项卡
5. 找到 msdyn_workorders 并检查是否添加了 **msdyn_name (Work Order Number)** 键。 如果不显示，请通过单击页面顶部的 **添加键**，然后单击 **保存** 添加。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>工作订单到销售订单（Field Service 到 Supply Chain Management）：WorkOrderHeader

筛选器：(msdyn_systemstatus ne 690970005) 和 (msdyn_systemstatus ne 690970000) 与 (msdynce_hasexternallymaintainedproductsonly eq true)

[![数据集成中的模板映射](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>工作订单到销售订单（Field Service 到 Supply Chain Management）：WorkOrderServiceLineEstimate

筛选器：(msdynce_headersystemstatus ne 690970005) 和 (msdynce_headersystemstatus ne 690970000) 及 (msdynce_orderhasexternalmaintainedproductsonly eq true) 与 (msdyn_linestatus eq 690970000) 和 (msdynce_headersystemstatus ne 690970004)

[![数据集成中的模板映射](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>工作订单到销售订单（Field Service 到 Supply Chain Management）：WorkOrderServiceLineUsed

筛选器：(msdynce_headersystemstatus ne 690970005) 和 (msdynce_headersystemstatus ne 690970000) 及 (msdynce_orderhasexternalmaintainedproductsonly eq true) 与((msdyn_linestatus eq 690970001) 或 (msdynce_headersystemstatus eq 690970004))

[![数据集成中的模板映射](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>工作订单到销售订单（Field Service 到 Supply Chain Management）：WorkOrderProductLineEstimate

筛选器：(msdynce_headersystemstatus ne 690970005) 和 (msdynce_headersystemstatus ne 690970000) 及 (msdynce_orderhasexternalmaintainedproductsonly eq true) 与 (msdyn_linestatus eq 690970000) 和 (msdynce_headersystemstatus ne 690970004) 及 (msdyn_allocated eq true)

[![数据集成中的模板映射](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>工作订单到销售订单（Field Service 到 Supply Chain Management）：WorkOrderProductLineUsed

筛选器：(msdynce_headersystemstatus ne 690970005) 和 (msdynce_headersystemstatus ne 690970000) 及 (msdynce_orderhasexternalmaintainedproductsonly eq true) 和((msdyn_linestatus eq 690970001) 或 (msdynce_headersystemstatus eq 690970004) 或 (msdyn_allocated ne true))

[![数据集成中的模板映射](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]