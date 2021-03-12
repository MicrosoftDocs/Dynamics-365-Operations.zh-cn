---
title: 装运合并政策
description: 此主题概述灵活配置装运合并策略的功能。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 326e9a32cdab049d974b6d88742434fbc8d56817
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006433"
---
# <a name="shipment-consolidation-policies"></a>装运合并政策

在自动和手动发放到仓库期间，可通过使用装运合并策略的装运合并流程自动合并装运。 引入此功能前提供的自动化合并具有硬编码字段，并基于为仓库设置的 **发放到仓库时合并装运** 字段。

装运合并策略用于以下功能：

- 自动化的发放到仓库批处理作业
- 销售订单或转移单中的 **发放到仓库** 命令
- 专用的 **发放到仓库** 页面
- **装载计划工作台** 页面中的 **发放到仓库** 命令
- **合并装运** 和 **装运合并工作台** 页面中的手动合并装运

引入装运合并策略之前，以仓库级设置存在的合并功能。 单个仓库的所有客户的所有订单被视为具有相同的合并要求。 装运合并策略增加了对不同组织具有不同装运合并的方案的支持。

查询用于识别应用的装运合并策略，而一组可编辑字段则决定如何在装运级别为装载行分组。 （此模式类似波次模板采用的模式。）此外，还已经向每个策略添加了一个 **与现有装运合并** 选项。 开启此选项后，*发放到仓库* 过程将通过在根据相同的合并策略创建的现有装运中进行搜索来查找要合并的装运。 在这种情况下，系统将选择现有装运或装载，而不是新建一个。 但是，系统将仅与状态为 *未结* 的现有装运合并；将不把属于状态为 *已发放* 或更高状态的波次发放的装运视为合并目标。

当装运合并策略可用时，将隐藏 **仓库** 设置页上以前提供的 **发放到仓库时合并装运** 设置。 为了帮助您过渡到新装运合并功能，**装运合并策略** 页上的一项功能将创建一个默认策略，其中自动包含现有仓库的旧设置。 创建这个默认策略之后，将不再考虑 **仓库** 设置页中的 **发放到仓库时合并装运** 设置。

可使用 **发放到仓库** 页按照覆盖履行策略的相同方法手动覆盖适用的合并策略。

执行发放到仓库之前，可以使用 **装载计划工作台** 页中的 **发放 \> 发放到仓库** 命令创建基于销售订单和转移单行的出站装载。 这些装载使用的合并逻辑与合并装运策略时一起引入的相同。

可使用 **装运合并工作台** 页合并尚未配置，但已经发放到仓库的现有装运。 此功能支持以下方案：一天多次运行有自己的装运合并的自动化发放流程，但是配置过程中完成装运到承运人之前手动识别了潜在更多合并。 可以在将装运发放到仓库之后，确认装运之前，随时使用此功能合并基于销售订单或转移单行创建的出站装运。

**装运合并工作台** 页的功能类似装载生成工作台，可在此处同时访问多个装运，并为特定装运分配非合并订单。 可以应用装运合并模板以多次评估建议的合并和确认。 将实施某些规则以阻止未经授权的合并和警示您可能的错误。

## <a name="overview-of-new-functionality"></a>新功能概述

此部分介绍当您开启和使用 *装运合并策略* 功能时更改或添加的页面、命令和功能。

### <a name="shipment-consolidation-policies-page"></a>装运合并策略页

策略根据工作订单类型进行区分。 **销售订单** 类型代表 _销售订单_ 装运，而 **转移单** 类型则表示 _转移发放_ 装运。

每个装运合并策略都有一个用于定义何时应用该策略的查询和一个用于确定执行顺序的序号。 将为所选字段的每个唯一组合应用合并。 还提供了一个参数，用于与现有（未结）装运合并。 每次创建新装运时（在进行波次处理之前），将评估和应用策略。

如果策略缺少任何必需字段，或者包含任何禁止的字段，将在 **所选** 部分中把此策略标记为无效。 必填字段和禁止字段的列表硬编码，并且可以扩展。

以下列表显示必需字段。 因为始终基于这些字段拆分装运，所以不能将这些字段的值不同的多个装运组合。

- 用于销售订单：

    - **帐号：**_WHSShipmentTable.AccountNum_
    - **收货人：**_WHSShipmentTable.DeliveryName_
    - **邮寄地址 (RecId)：**_WHSShipmentTable.DeliveryPostalAddress_
    - **仓库：**_WHSShipmentTable.InventLocationId_

- 对于转移单：

    - **源仓库：**_InventTransferTable.InventLocationIdFrom_
    - **目标仓库：**_InventTransferTable.InventLocationIdTo_

以下字段对所有文档类型不可用。 这些字段在用户界面 (UI) 中不可见，不能用于合并。

- **装运 ID：**_WHSShipmentTable.ShipmentId_
- **状态：**_WHSShipmentTable.ShipmentStatus_
- **装运合并策略：**_WHSShipmentTable.ShipConsolidationPolicyName_
- **工作交易类型：**_WHSShipmentTable.WorkTransType_
- **波浪 ID：**_WHSShipmentTable.WaveId_
- **装载 ID：**_WHSShipmentTable.LoadId_
- **装运 ID：**_WHSLoadLine.ShipmentId_
- **装载 ID：**_WHSLoadLine.LoadId_

默认情况下，创建策略时，将把必需字段集用作合并字段。 但是，可以使用向左箭头和向右箭头按钮修改列表。 （此流程类似在波次模板中选择方法的流程。）

将把用户为这些字段选择的值用于所有新建装运，或者在与这些装运合并时将其添加到现有装运。 当为了合并两个装运而为其选择的某个字段的值相同时，将合并这两个装运。 将把同一个主体应用于选择的所有后续合并字段。 如果值不同，将丢弃第二个装运，并为新装运选择。 自动化合并流程中包含为装运合并字段的值创建所有唯一组合，然后为相关组合分配装运。

在合并过程中，将忽略未选择的字段。 如果两个装运的某个未选择字段的值不同，将清除该字段（即设置为空）。 如果两个装运的某个未选择字段的值相同，则填写该字段。

将为合并字段（即值不同时将清除的字段）列表硬编码。 此列表中包含在创建新装运时从销售订单或转移单行初始化的所有字段。 换句话说，如果某个字段不是从销售订单或转移单行初始化的，向现有装运添加新数据时，将忽略该字段。

### <a name="release-to-warehouse-page"></a>发放到仓库页

- 下方网格中的一个新字段显示应用的合并策略。
- 可通过一个新按钮手动选择和/或覆盖合并策略。

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>装载计划工作台页面中的发放到仓库命令

- 已调整了逻辑，使其使用应用的合并策略。
- 现在仅在一个装载中合并装运。

### <a name="consolidate-shipments-page"></a>合并装运页

- 更改了相似字段（即合并候选项）的搜索，使其使用在装运合并策略中选择的字段。
- 现在将在不同装运中的值不同的字段设置为空。 （以前使用所选“基础”装运的值。）

### <a name="shipment-consolidation-workbench-page"></a>装运合并工作台页

- 新功能以更大规模复制手动合并流程。
- 现在可从 **仓库管理** 模块中的 **发放到仓库** 菜单打开此页。
- 此算法分析尚未装运的现有装运。 然后根据合并策略中选择的字段建议合并。

## <a name="comparison-of-functionality"></a>功能比较

下表总结了不使用装运合并策略时和使用时，装运合并的工作方式。

| 不使用装运合并策略时 | 使用装运合并策略时 |
|---|----|
| 不适用 | 为合并选择的销售装运或转移装运必须与正在创建的装运的合并策略相同，或者必须将其分配给未结装运（当开启了 **与现有装运合并** 选项时）。 |
| *发放到仓库* 过程不在现有装运中搜索以查找要合并的装运。 将仅把 *发放到仓库* 过程的当前实例创建的装运用于查找要合并的装运。 | 如果为当前正在使用的合并策略开启了 **与现有装运合并** 选项，*发放到仓库* 过程将在基于同一个合并策略创建的现有装运中搜索以查找要合并的装运。 因此，如果您有两个策略，切勿将正在基于策略 2 创建的装运与基于策略 1 创建的装运合并。 |
| 不适用 | 如果合并策略字段列表为空，或者找不到策略，将为每个销售订单或转移单行创建新装运。 |
| 以下合并字段定义用于合并 *转移行* 的装运的值的唯一组合。 （将忽略所有其他字段。）<ul><li>订单号 (OrderNum)</li></ul> | 以下合并字段定义用于合并 *转移行* 的装运的值的唯一组合。 （将忽略所有其他字段。）<ul><li>订单号 (OrderNum)</li><li>收货人 (DeliveryName)</li><li>邮寄地址 (DeliveryPostalAddress)</li><li>ISO 国家/地区代码 (CountryRegionISOCode)</li><li>地址 (Address)</li><li>站点 (InventSiteId)</li><li>仓库 (InventLocationId)</li><li>装运承运人 (CarrierCode)</li><li>承运人服务 (CarrierServiceCode)</li><li>交货方式 (ModeCode)</li><li>承运人组 (CarrierGroupCode)</li><li>交货期 (DlvTermId)</li></ul>创建新装运时，只有这些字段可用和初始化这些字段。 |
| 以下合并字段定义用于合并 *销售行* 的装运的值的唯一组合。 （将忽略所有其他字段。）<ul><li>订单号 (OrderNum)</li><li>客户参考 (CustomerRef)</li><li>客户申请 (CustomerReq)</li><li>交货期 (DlvTermId)</li></ul> | 以下合并字段定义用于合并 *销售行* 的装运的值的唯一组合。 （将忽略所有其他字段。）<ul><li>订单号 (OrderNum)</li><li>帐号 (AccountNum)</li><li>收货人 (DeliveryName)</li><li>邮寄地址 (DeliveryPostalAddress)</li><li>ISO 国家/地区代码 (CountryRegionISOCode)</li><li>地址 (Address)</li><li>站点 (InventSiteId)</li><li>仓库 (InventLocationId)</li><li>装运承运人 (CarrierCode)</li><li>承运人服务 (CarrierServiceCode)</li><li>交货方式 (ModeCode)</li><li>承运人组 (CarrierGroupCode)</li><li>代理人 ID (BrokerCode)</li><li>方向 (LoadDirection)</li><li>交货期 (DlvTermId)</li><li>客户参考 (CustomerRef)</li><li>客户申请 (CustomerReq)</li></ul>创建新装运时，只有这些字段可用和初始化这些字段。 |
| 不适用 | 以下合并字段是 *销售行* 的必需字段，不能删除：<ul><li>帐号 (AccountNum)</li><li>收货人 (DeliveryName)</li><li>邮寄地址 (DeliveryPostalAddress)</li><li>仓库 (InventLocationId)</li></ul>默认情况下，在创建新策略时分配这些字段。 不能删除它们。 |
| **装载计划工作台** 页面中的 *将装载发放到仓库* 过程使用自己的单独代码创建装运和波次。 | 将应用装运合并策略以确定应该为合并评估哪些字段。 仅在一个装载中合并装运。 |
| 请在 **所有装运** 页中手动选择 **合并装运**，然后选择目标“基础”装运。 筛选器将推荐具有多个关键字段的匹配值的任何现有装运。 | 请在 **所有装运** 页中手动选择 **合并装运**，然后选择目标“基础”装运。 系统将通过匹配为相关装运合并策略配置的多个关键字段的值，建议其他现有装运。 |
| **所有装运** 页中的 **合并装运** 命令只能用于一个装运。 | **装运合并工作台** 页可帮助您查找还不是已装运状态的一组装运。 将根据在装运合并策略中配置的多个关键字段分析这些装运。 将建议合并这些字段的值匹配的任何装运。<p>可以通过从建议合并删除装运和/或通过向其添加装运，手动维护合并。 可能发生多种错误，但是可以覆盖其中的一部分。</p> |
| **设计说明**：*将销售订单自动发放到仓库* 过程将销售行拆分为组。 每个组有自己的唯一 **ReleaseToWarehouseId** 值，并通过 *发放到仓库* 过程单独处理。 无论如何设置工作分解，此过程都会产生新工作。 | **设计说明**：*将销售订单自动发放到仓库* 过程为正在处理的所有销售行分配同一个 **ReleaseToWarehouseId** 值。 所有销售行由 *发放到仓库* 过程同时处理。 为了确保前面的行为，必须按装运 ID 配置工作分解。 |

## <a name="additional-resources"></a>其他资源

- [配置装运合并策略](configure-shipment-consolidation-policies.md)
