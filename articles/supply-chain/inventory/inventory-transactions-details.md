---
title: 库存交易详细信息
description: 本文概述了显示所选库存交易详细信息的“交易详细信息”页面。
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859378"
---
# <a name="inventory-transaction-details"></a>库存交易详细信息

使用 **交易详细信息** 页面查看任何所选库存交易的详细信息。

## <a name="open-the-transaction-details-page"></a>打开“交易详细信息”页面

要打开 **交易详细信息** 页，请执行以下步骤。

1. 转到 **库存管理 \> 查询和报表 \> 交易**。
1. 选择要检查的交易。
1. 在操作窗格上，选择 **交易详细信息**。

## <a name="fasttabs-overview"></a>快速选项卡概览

**交易详细信息** 页面被拆分为多个快速选项卡。 下表描述了每个快速选项卡的用途。

| 快速选项卡 | Description |
|---|---|
| 常规 | 此快速选项卡显示有关所选库存交易的基本信息。 除了显示在 **库存交易** 页面上的字段外，还包括本文后面描述的其他字段。 |
| 更新 | 此快速选项卡显示与所选库存交易的实物、财务和结算方面相关的信息。 根据交易的当前状态，某些字段可能为空白。 但是，在过帐交易时将自动设置这些字段。 除了显示在 **库存交易** 页面上的字段外，此快速选项卡还包括本文后面描述的其他字段。 |
| 分类帐过帐 | 此快速选项卡显示用于与所选库存交易相关的实际更新、财务更新、实际收入、实际费用、财务收入和财务费用的过帐类型和会计科目。 |
| 引用 | 此快速选项卡显示有关创建所选库存交易的源交易的附加信息。 例如，此信息可能包括采购订单或销售订单的详细信息。 |
| 相关信息 | 此快速选项卡显示有关所选库存交易的附加信息。 如果您不使用某些功能（例如采购类别或项目），则可能不会设置这些字段。 |
| 财务维度 - 实际 | 此快速选项卡显示过帐实际更新时使用的财务维度值。 如果尚未过帐实际更新，则该字段将为空白。 |
| 财务维度 - 财务 | 此快速选项卡显示过帐财务更新时使用的财务维度值。 如果尚未过帐财务更新，则该字段将为空白。 |
| 库存维度 | 此快速选项卡显示分配给所选库存交易的库存维度值。 这些值包括站点、仓库、大小、颜色、配置、位置、批号、序列号、库存状态、牌照和所有者。 |

## <a name="fields-on-the-general-fasttab"></a>常规快速选项卡上的字段

下表描述了 **常规** 快速选项卡上的字段，这些字段也不会显示在 **库存交易** 页上。

| 字段 | Description |
|---|---|
| 当事方 | 所选库存交易的相关方的名称。 例如，采购订单交易显示采购订单上的供应商名称，销售订单交易显示客户的名称。 此字段不适用于所有类型的库存交易。 |
| 库存引用 | 如果另一个库存交易与所选库存交易相关，则是该其他交易的类型。 例如，如果针对销售订单标记了采购订单，则采购订单交易的 **库存参考** 字段将设置为 *销售订单*。 系统将自动标记直接交货订单和内部公司订单。 当您使用 *标准成本* 和 *移动平均* 以外的成本计算方法进行标记时，系统将对标记的精确交易创建结算和调整。 这样，您可以实现替代先进先出 (FIFO)、后进先出 (LIFO) 或加权平均的逻辑的“实际”成本计算。 |
| 库存编号 | 与所选库存交易相关的特定交易。 例如，如果针对销售订单标记了采购订单，则采购订单交易的 **库存编号** 字段将设置为销售订单编号。 |
| 项目 ID | 如果所选库存交易与项目相关，则此字段将设置为项目编号。 |
| 批次 ID | 系统已分配给所选库存交易的唯一批次 ID。 |
| 引用批次 | 如果另一个库存交易与所选库存交易相关，则是该其他交易的批次 ID。 例如，如果针对销售订单标记了采购订单，则采购订单交易的 **引用批次** 字段将是销售订单行的库存交易的 **批次 ID**。 |
| 维度编号 | 一个唯一 ID，表示分配给所选库存交易的所有库存维度值的组合。 |
| 财务未记帐 | 一个指示所选库存交易是否已由库存结转流程结算的值。 如果此字段设置为 *是*，则交易尚未结算。 |
| 预期日期 | 对于收货交易，这是库存收货的预计发生日期。 例如，此字段可能会显示库存冻结订单上的预期收货日期或采购订单行上的交货日期。 |
| 库存日期 | 在过帐实际收据之前对收据订单进行登记交易时，会设置此字段。 |
| 非财务转移 | 一个指示所选库存交易是否为非财务转移的值。 当 **物料模型组** 页面上未对库存维度更改进行财务跟踪时，就会发生非财务转移。 |
| 转移批次 ID | 如果选定的库存交易是非财务转移，则此字段设置为结算所选交易所针对的其他库存交易的 **批次 ID**。 |

## <a name="fields-on-the-updates-fasttab"></a>“更新”快速选项卡上的字段

下表描述了 **更新** 快速选项卡上的字段，这些字段也不会显示在 **库存交易** 页上。

| 字段 | Description |
|---|---|
| 实际凭证 | 为所选库存交易生成实际过帐的总帐中的凭证号。 |
| 工艺路线 | 与所选库存交易相关的工艺路线。 系统仅针对物料清单 (BOM) 或配方行与特定物料相关的生产领料单交易设置此字段。 |
| 装箱单 | 为采购订单产品收货交易输入的装箱单编号。 |
| 实际成本额 | 为实际更新而过帐到总帐的金额。 对于标准成本产品，此金额代表标准成本。 对于其他成本计算方法，它代表过帐时产品的加权平均值。 |
| 实际收入 | 为实际更新而过帐到总帐的延期收入金额。 |
| 装载 ID | 如果当前事务与运输管理中的负荷相关，则此字段显示包含该项目的负荷的唯一编号。 |
| 实物已过帐 | 一个指示所选库存交易是否已实际过帐的值。 如果将当前交易记录过帐到总帐，则还将有实际凭证。 |
| 财务已过帐 | 一个指示所选库存交易是否已财务过帐的值。 如果将当前交易记录过帐到总帐，则还将有财务凭证。 |
| 实际费用已过帐 | 一个指示与所选库存交易相关的实际费用是否已过帐的值。 |
| 财务费用已过帐 | 一个指示与所选库存交易相关的财务费用是否已过帐的值。 |
| 财务凭证 | 生成财务过帐的总帐中的凭证号。 |
| 发票 | 为采购订单或销售订单生成的发票编号。 |
| 调整 | 从库存结转和调整流程中对所选库存交易进行调整的金额。 |
| 损益，已过帐金额 | 已过帐到损益表的选定库存交易的金额。 |
| 未过帐的发票 | 显示在 **待定供应商发票** 页面上的相关采购订单的发票编号。 |
| 财务上已结算 | 完全结算交易的日期。 |
| 涵盖的 CW 数量 | 结算涵盖的实际称重数量。 |
| 已结算数量 | 已为所选库存交易结算的数量。 |
| 已结算的金额 | 已为所选库存交易结算的值。 |