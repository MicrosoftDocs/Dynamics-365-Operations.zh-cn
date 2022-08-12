---
title: 供应商发票实体
description: 本文提供有关供应商发票实体的信息，这些信实体允许为内部成本或外部派生成本配置成本类型代码。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f0371cf9862afaf3bc43a44def725c420e9aaf56
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166734"
---
# <a name="vendor-invoice-entities"></a>供应商发票实体

[!include [banner](../includes/banner.md)]

**到岸成本** 模块允许为内部成本或外部派生成本配置成本类型代码。 如果成本是业务外部成本，则服务提供商应该开具发票。 此发票作为可以与航行关联的发票日记帐进行处理，并且可在航行的一个或多个成本中分配发票的值。

供应商发票实体允许在共享相同成本类型代码的航行的一个或多个成本中分配日记帐行的值。

仅当发票日记帐标题和发票日记帐行存在时，才能分配成本。

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>供应商航行成本分摊 (ITMLedgerJournalCostLinesVoyagesEntity)

供应商航行成本分配数据实体允许在应用于航行成本区域的一个或多个成本中分配供应商发票行。 `ITMLedgerJournalCostLinesVoyagesEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |
| 航行 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>供应商装运集装箱成本分配 (ITMLedgerJournalCostLinesContainersEntity)

供应商装运集装箱成本分配数据实体允许在应用于装运集装箱成本区域的一个或多个成本中分配供应商发票行。 `ITMLedgerJournalCostLinesContainersEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 装运集装箱 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |
| 航行 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>供应商帐页成本分摊 (ITMLedgerJournalCostLinesFoliosEntity)

供应商帐页成本分配数据实体允许在应用于帐页成本区域的一个或多个成本中分配供应商发票行。 `ITMLedgerJournalCostLinesFoliosEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 帐页 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>供应商采购订单成本分配 (ITMLedgerJournalCostLinesPurchTableEntity)

供应商采购订单成本分配数据实体允许在应用于采购订单成本区域的一个或多个成本中分配供应商发票行。 `ITMLedgerJournalCostLinesPurchTableEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |
| 采购订单 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>供应商物料成本分摊 (ITMLedgerJournalCostLinesPurchLineEntity)

供应商物料成本分配数据实体允许在应用于物料成本区域的一个或多个成本中分配供应商发票行。 物料成本区域涵盖采购订单行上的成本。 `ITMLedgerJournalCostLinesPurchLineEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |
| 采购订单 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |
| 采购订单行编号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>供应商转移单行成本分配 (ITMLedgerJournalCostLinesTransferLineEntity)

供应商转移单成本分配数据实体允许在应用于转移单成本区域的一个或多个成本中分配供应商发票行。 `ITMLedgerJournalCostLinesTransferLineEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 分配的金额 | ITMLedgerJournalCostLines.Amount | 数字(32, 6) | 否 | 否 |
| 成本交易记录行号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐行号 | ITMLedgerJournalCostLines.RefRecId | 数字(32, 16) | **是** | 否 |
| 日记帐编号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **是** | 否 |
| 转移单 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **是** | 否 |
| 转移单行编号 | ITMLedgerJournalCostLines.CostTransRefRecId | 数字(32, 16) | **是** | 否 |

### <a name="reference-table"></a>引用表

航行成本行与成本交易记录直接关联。 此记录包括 **引用表 ID** 值。 此值对于每个成本区域（航行、装运集装箱等）都是唯一的。 为使用数据实体创建的数据引用特定表编号时，将基于 **引用表 ID** 值拆分实体。

在选择到岸成本采购行或到岸成本转移行实体时，引用表 (`RefTableId`) 和交易类型 (`TransType`) 的值是隐式值。

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>供应商发票日记帐行 (VendorInvoiceJournalLineEntity)

在可以将日记帐行值分配到 **到岸成本** 模块中的一个或多个成本之前，此日记帐行必须与成本区域关联。 为了支持此功能，**到岸成本** 模块会将一些新字段添加到日记帐行表 (`LedgerJournalTrans`)。

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>添加到供应商发票日记帐行实体的字段

下表列出了 **到岸成本** 模块添加到供应商发票日记帐行实体 (`VendorInvoiceJournalLineEntity`) 的字段。 这些字段使系统能够创建日记帐行并根据它们分配成本。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 成本区域 | LedgerJournalTrans.ITMCostArea | Int | 否 | 否 |
| 成本类型代码 | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | 否 | 否 |

### <a name="mainoffset-account"></a>主/对方科目

与到岸成本航行关联的发票日记帐行的主/对方科目由成本类型代码确定。 如果在发票日记帐行中包含了成本类型代码，则该代码的结算帐户将用作主科目或对方科目，具体取决于方案：

- **单行日记帐** - 如果定义了主科目（换句话说，定义了供应商帐户），并且提供了成本类型代码，则将在对方科目中输入该成本类型代码的结算帐户值。
- **多行日记帐** - 如果未定义主科目，但提供了成本类型代码，则将在主科目中输入该成本类型代码的结算帐户值。 贷记供应商的日记帐行不会引用成本类型代码。

## <a name="sequencing"></a>先后顺序

由于日记帐和日记帐行表之间存在依赖关系，必须首先创建航行记录。 只有在创建航行、装运集装箱和帐页之后才能创建航行行。

若要分配航行发票，系统必须按照以下顺序处理实体：

1. 发票日记帐标题 (`VendInvoiceJournalHeaderEntity`)
1. 发票日记帐行 (`VendInvoiceJournalLineEntity`)
1. 到岸成本分摊 (`ITMLedgerJournalEntities`)
