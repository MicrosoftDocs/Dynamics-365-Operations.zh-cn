---
title: 航行创建实体
description: 本主题提供有关航行创建数据实体的信息，这些数据实体对创建工作航行所需的数据实体进行分组。
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
ms.openlocfilehash: 17f63af3ce1f858ed3e2086fc81c5e17c5e76be0
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813046"
---
# <a name="voyage-creation-entities"></a>航行创建实体

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

航行创建数据实体将创建工作航行所需的数据实体组织在一个组中。 您或您的货运转运商可以使用这些数据实体创建引用现有采购订单或转移单行的航行、装运集装箱、帐页和航行行记录。

## <a name="voyages-itmtableentity"></a>航行 (ITMTableEntity)

航行表示入站货物的行程，并充当到岸成本中最高级别的成本区域。 它包含与船舶、原产地港口和目标港口相关的标题级别信息。 `ITMTableEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 交货模式 | ITMTable.DlvModeId | Nvarchar(10) | 否 | 否 |
| 已建议代理 | ITMTable.ITMBrokerAdvised | DateTime | 否 | 否 |
| 客户预约 | ITMTable.ITMCustomerAppointment | DateTime | 否 | 否 |
| 已在仓库交货 | ITMTable.ITMDelAtWarehouse | DateTime | 否 | 否 |
| 交货说明 | ITMTable.ITMDeliveryInstructions | DateTime | 否 | 否 |
| 出发日期 | ITMTable.ITMDepartureDate | DateTime | 否 | 否 |
| 已发放货物 | ITMTable.ITMGoodsReleased | DateTime | 否 | 否 |
| 本地运输日期 | ITMTable.ITMLocalTransportDate | DateTime | 否 | 否 |
| 本地运输时间 | ITMTable.ITMLocalTransportTime | Int | 否 | 否 |
| 已发送原始提单 | ITMTable.ITMOriginalBOLSebt | DateTime | 否 | 否 |
| 已收到原始单据 | ITMTable.ITMOriginalDocsReceived | DateTime | 否 | 否 |
| 采购订单状态 | ITMTable.ITMPurchStatus | Int | 否 | 否 |
| 验证日期 | ITMTable.ITMVerificationDate | DateTime | 否 | 否 |
| 进口报关标识符 | ITMTable.ShipCustomsEntryId | Nvarchar(20) | 否 | 否 |
| 装运日期 | ITMTable.ShipDate | DateTime | 否 | 否 |
| Description | ITMTable.ShipDescription | Nvarchar(60) | 否 | 否 |
| 已收到单据 | ITMTable.ShipDocReceived | Int | 否 | 否 |
| 预计交货日期 | ITMTable.ShipEstDlvDate | DateTime | 否 | 否 |
| 装运港口 ETA | ITMTable.ShipEstPortDate | DateTime | 否 | 否 |
| 发运港口 | ITMTable.ShipFromPort | Nvarchar(20) | 否 | 否 |
| 内部航空运单/提单 | ITMTable.ShipHAWB | Nvarchar(20) | 否 | 否 |
| 航行 | ITMTable.ShipId | Nvarchar(20) | **是** | **是** |
| 记帐引用 | ITMTable.ShipIdExternal | Nvarchar(20) | 否 | 否 |
| 行程模板 | ITMTable.ShipJourneyId | Nvarchar(20) | 否 | 否 |
| 本地转运商 | ITMTable.ShipLocalForwarder | Nvarchar(20) | 否 | 否 |
| 主航空运单/提单 | ITMTable.ShipMAWB | Nvarchar(20) | 否 | 否 |
| 量化指标 | ITMTable.ShipMeasurement | 数字(32, 6) | 否 | 否 |
| 度量单位 | ITMTable.ShipMeasurementUnit | Int | 否 | 否 |
| 托盘数 | ITMTable.ShipNoOfPallets | Int | 否 | 否 |
| 待定航行 | ITMTable.ShipPending | Int | 否 | 否 |
| 注解 | ITMTable.ShipRemarks | Nvarchar(MAX) | 否 | 否 |
| 租赁 | ITMTable.ShipRental | Int | 否 | 否 |
| 航行状态 | ITMTable.ShipStatusId | Nvarchar(20) | 否 | 否 |
| 以数字表示的理货 | ITMTable.ShipTallyInNumber | Nvarchar(20) | 否 | 否 |
| 目标港口 | ITMTable.ShipToPort | Nvarchar(20) | 否 | 否 |
| 估价日期 | ITMTable.ShipValuationDate | DateTime | 否 | 否 |
| 装运公司 | ITMTable.ShipVendAccount | Nvarchar(20) | 否 | 否 |
| 船舶 | ITMTable.ShipVesselId | Nvarchar(20) | 否 | **是** |
| 外部航行 ID | ITMTable.ShipVoyage | Nvarchar(20) | 否 | 否 |

### <a name="number-sequences-for-voyages"></a>航行的编号规则

航行的共享编号规则控制航行 ID 的分配。

作为 **航行 ID** (`ShipId`) 值传递到数据实体的值用于标识现有记录以进行更新。 如果该记录不存在，则此行为取决于分配的编号规则是否已配置为允许手动输入：

- 如果启用手动输入，则将创建使用传递值的新记录。
- 如果未启用手动输入，则将使用分配的编号规则中的下一个编号，而不是传递的值。

在导入会话期间，会保留导入为航行 ID 的占位符值。 此行为可确保引用占位符的装运集装箱和航行行包括在航行中，并更新它们以反映根据编号规则分配的值。

### <a name="automatic-cost-transactions"></a>自动成本交易

可以从 Microsoft Dynamics 365 Supply Chain Management 的 **自动成本** 页面（**到岸成本 \> 成本计算设置 \> 自动成本**）将自动成本添加到航行中。 也可以使用到岸成本支持的每个成本区域的成本交易数据实体来创建自动成本的记录。

在创建航行行时，在 Supply Chain Management 中配置的自动成本将应用于航行。 在标题记录与行信息关联之前，不会对记录显示任何成本。

## <a name="shipping-containers-itmcontainersentity"></a>装运集装箱 (ITMContainersEntity)

装运集装箱表示运输货物所装入的实际集装箱。 此实际集装箱可能是用于远洋货运的货运集装箱，也可能是用于空运的单个托盘。 装运集装箱包括与装运集装箱 ID、封条编号和装运集装箱类型相关的标题级别信息。 （装运集装箱类型提供维度信息。）`ITMContainersEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 出发日期 | ITMContainers.ITMDepartureDate | DateTime | 否 | 否 |
| 本地运输日期 | ITMContainers.ITMLocalTransportDate | DateTime | 否 | 否 |
| 本地运输时间 | ITMContainers.ITMLocalTransportTime | Int | 否 | 否 |
| 原始航行 | ITMContainers.OrigShipId | Nvarchar(20) | 否 | 否 |
| 实际重量 | ITMContainers.ShipActualWeight | 数字(32, 6) | 否 | 否 |
| 已建议代理 | ITMContainers.ShipBrokerAdvised | DateTime | 否 | 否 |
| 装运集装箱 | ITMContainers.ShipContainerId | Nvarchar(20) | **是** | **是** |
| 装运集装箱类型 | ITMContainers.ShipContainerTypeId | Nvarchar(20) | 否 | 否 |
| 单位类型 | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | 否 | 否 |
| 已转换为租赁 | ITMContainers.ShipConvertedToRental | Int | 否 | 否 |
| 客户预约 | ITMContainers.ShipCustomerAppointment | DateTime | 否 | 否 |
| 装运日期 | ITMContainers.ShipDate | DateTime | 否 | 否 |
| 已在仓库交货 | ITMContainers.ShipDelAtWarehouse | DateTime | 否 | 否 |
| 交货说明 | ITMContainers.ShipDeliveryInstructions | DateTime | 否 | 否 |
| 检验证书申请日期 | ITMContainers.ShipECAppliedDate | DateTime | 否 | 否 |
| 检验证书到期日期 | ITMContainers.ShipECExpiryDate | DateTime | 否 | 否 |
| 检验证书编号 | ITMContainers.ShipECNum | Nvarchar(20) | 否 | 否 |
| 检验证书接收日期 | ITMContainers.ShipECReceivedDate | DateTime | 否 | 否 |
| 预计交货日期 | ITMContainers.ShipEstDlvDate | DateTime | 否 | 否 |
| 装运港口 ETA | ITMContainers.ShipEstPortDate | DateTime | 否 | 否 |
| 预期装运日期 | ITMContainers.ShipExpectedLoadingDate | DateTime | 否 | 否 |
| 发运港口 | ITMContainers.ShipFromPort | Nvarchar(20) | 否 | 否 |
| 货物描述 | ITMContainers.ShipGoodsDesc | Nvarchar(60) | 否 | 否 |
| 已发放货物 | ITMContainers.ShipGoodsReleased | DateTime | 否 | 否 |
| GPS 跟踪器单元 | ITMContainers.ShipGPSUnit | Nvarchar(30) | 否 | 否 |
| 内部航空运单/提单 | ITMContainers.ShipHAWB | Nvarchar(20) | 否 | 否 |
| 航行 | ITMContainers.ShipId | Nvarchar(20) | **是** | **是** |
| 行程模板 | ITMContainers.ShipJourneyId | Nvarchar(20) | 否 | 否 |
| 本地转运商 | ITMContainers.ShipLocalForwarder | Nvarchar(20) | 否 | 否 |
| 量化指标 | ITMContainers.ShipMeasurement | 数字(32, 6) | 否 | 否 |
| 度量单位 | ITMContainers.ShipMeasurementUnit | Int | 否 | 否 |
| 纸箱数量 | ITMContainers.ShipNoOfCartons | 数字(32, 6) | 否 | 否 |
| 已发送原始提单 | ITMContainers.ShipOriginalBOLSebt | DateTime | 否 | 否 |
| 已收到原始单据 | ITMContainers.ShipOriginalDocsReceived | DateTime | 否 | 否 |
| 我们的封条编号 | ITMContainers.ShipOurSealNum | Nvarchar(20) | 否 | 否 |
| 已使用 | ITMContainers.ShipPendingUsed | Int | 否 | 否 |
| 采购订单状态 | ITMContainers.ShipPurchStatus | Int | 否 | 否 |
| 冷冻类型 | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | 否 | 否 |
| 注解 | ITMContainers.ShipRemarks | Nvarchar(MAX) | 否 | 否 |
| 租赁 | ITMContainers.ShipRental | Int | 否 | 否 |
| 可退 | ITMContainers.ShipReturnable | Int | 否 | 否 |
| 航行状态 | ITMContainers.ShipStatusId | Nvarchar(20) | 否 | 否 |
| 装运公司封条编号 | ITMContainers.ShipTheirSealNum | Nvarchar(20) | 否 | 否 |
| 目标港口 | ITMContainers.ShipToPort | Nvarchar(20) | 否 | 否 |
| 验证日期 | ITMContainers.ShipVerificationDate | DateTime | 否 | 否 |
| 船舶 | ITMContainers.ShipVesselId | Nvarchar(20) | 否 | **是** |

### <a name="voyage-id-validation"></a>航行 ID 验证

装运集装箱 ID 不受编号规则的控制。 它仅在使用航行所在的上下文中是唯一的。

如果独立于航行实体 (`ITMTableEntity`) 使用了装运集装箱实体 (`ITMContainersEntity`)，则 **航行 ID**(`ShipId`) 值必须与航行表中的现有记录匹配。 否则，导入将失败。

如果在同一导入会话中使用装运集装箱实体 (`ITMContainersEntity`) 和航行实体 (`ITMTableEntity`) ，则必须在创建装运集装箱之前创建航行实体。 否则，无法成功验证 **航行 ID** (`ShipId`) 值。 如果占位符值用于 **航行 ID** (`ShipId`) 值，则仅当同一占位符用作装运集装箱实体中的 **航行 ID** (`ShipId`) 值时，才能创建关联。

### <a name="other-field-validations"></a>其他字段验证

下表显示根据到岸成本设置表验证的装运集装箱表 (`ITMContainers`) 中的字段。 它还显示货运转运商可用于读取现有值并确保在您的环境中接收有效值的到岸成本数据实体。

| ITMContainers 表中的字段 | 到岸成本数据实体 |
|---|---|
| 装运集装箱类型 | ITMShippingContainerTypeEntity |
| 货物描述 | ITMGoodsDescriptionEntity |
| 冷冻类型 | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>帐页 (ITMFolioEntity)

帐页表示装运集装箱中出于关税申报目的的物料组。 帐页包括与海关代理相关的标题级别信息和货物描述。 `ITMFolioEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 已建议代理 | ITMFolioTable.ShipBrokerAdvised | DateTime | 否 | 否 |
| 货物控制编号 | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | 否 | 否 |
| 客户预约 | ITMFolioTable.ShipCustomerAppointment | DateTime | 否 | 否 |
| 关税代理 | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | 否 | 否 |
| 海关 ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | 否 | 否 |
| 公司 | ITMFolioTable.ShipDataArea | Nvarchar(4) | 否 | **是** |
| 已在仓库交货 | ITMFolioTable.ShipDelAtWarehouse | DateTime | 否 | 否 |
| 交货说明 | ITMFolioTable.ShipDeliveryInstructions | DateTime | 否 | 否 |
| 已收到单据 | ITMFolioTable.ShipDocReceived | Int | 否 | 否 |
| 预计交货日期 | ITMFolioTable.ShipEstDlvDate | DateTime | 否 | 否 |
| 装运港口 ETA | ITMFolioTable.ShipEstPortDate | DateTime | 否 | 否 |
| 出口商 | ITMFolioTable.ShipExporterId | Nvarchar(20) | 否 | 否 |
| Name | ITMFolioTable.ShipExporterName | Nvarchar(60) | 否 | 否 |
| 帐页日期 | ITMFolioTable.ShipFolioDate | DateTime | 否 | 否 |
| 帐页 | ITMFolioTable.ShipFolioId | Nvarchar(20) | **是** | **是** |
| 发运港口 | ITMFolioTable.ShipFromPort | Nvarchar(20) | 否 | 否 |
| 货物描述 | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | 否 | 否 |
| 已发放货物 | ITMFolioTable.ShipGoodsReleased | DateTime | 否 | 否 |
| 内部航空运单/提单 | ITMFolioTable.ShipHAWB | Nvarchar(20) | 否 | 否 |
| 航行 | ITMFolioTable.ShipId | Nvarchar(20) | 否 | **是** |
| 量化指标 | ITMFolioTable.ShipMeasurement | 数字(32, 6) | 否 | 否 |
| 度量单位 | ITMFolioTable.ShipMeasurementUnit | Int | 否 | 否 |
| 纸箱数量 | ITMFolioTable.ShipNoOfCartons | 数字(32, 6) | 否 | 否 |
| 已发送原始提单 | ITMFolioTable.ShipOriginalBOLSebt | DateTime | 否 | 否 |
| 已收到原始单据 | ITMFolioTable.ShipOriginalDocsReceived | DateTime | 否 | 否 |
| 采购订单状态 | ITMFolioTable.ShipPurchStatus | Int | 否 | 否 |
| 注解 | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | 否 | 否 |
| 航行状态 | ITMFolioTable.ShipStatusId | Nvarchar(20) | 否 | 否 |
| 关税代码 | ITMFolioTable.ShipTariffCode | Nvarchar(10) | 否 | 否 |
| 目标港口 | ITMFolioTable.ShipToPort | Nvarchar(20) | 否 | 否 |
| 估价日期 | ITMFolioTable.ShipValuationDate | DateTime | 否 | 否 |
| 验证日期 | ITMFolioTable.ShipVerificationDate | DateTime | 否 | 否 |
| 供应商帐户 | ITMFolioTable.VendAccount | Nvarchar(20) | 否 | 否 |

### <a name="number-sequences-for-folios"></a>帐页的编号规则

帐页的编号规则控制帐页 ID 的分配。

作为 **帐页 ID** (`FolioId`) 值传递到数据实体的值用于标识现有记录以进行更新。 如果该记录不存在，则此行为取决于分配的编号规则是否已配置为允许手动输入：

- 如果启用手动输入，则将创建使用传递值的新记录。
- 如果未启用手动输入，则将使用分配的编号规则中的下一个编号，而不是传递的值。

在导入会话期间，会保留导入为帐页 ID 的占位符值。 此行为可确保正确关联引用占位符的航行行，并更新它们以反映根据编号规则分配的值。

### <a name="field-validations"></a>字段验证

帐页表 (`ITMFolioTable`) 中的 **货物描述** 字段根据同名的到岸成本设置表进行验证。 货运转运商可以使用 `ITMGoodsDescriptionEntity` 到岸成本数据实体读取现有值，并确保在您的环境中接收有效值的到岸成本数据实体。

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>采购订单的航行行 (ITMPurchaseLineEntity)

航行行表示航行中包含的单个采购订单行。 此关系是通过 **采购订单编号** 和 **采购行编号** 字段建立的。 航行行引用了为航行、装运集装箱和帐页创建的每个先前记录。 `ITMPurchaseLineEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 货币 | ITMLine.CurrencyCode | Nvarchar(3) | 否 | 否 |
| 净额 | ITMLine.LineAmountMST | 数字(32, 6) | 否 | 否 |
| 采购行号 | ITMLine.RefRecId | 数字(32, 6) | **是** | 否 |
| 装运集装箱 | ITMLine.ShipContainerId | Int | 否 | 否 |
| 公司 | ITMLine.ShipDataArea | Nvarchar(20) | **是** | 否 |
| 已申报数量 | ITMLine.ShipDeclaredQty | Nvarchar(4) | 否 | 否 |
| 帐页 | ITMLine.ShipFolioId | 数字(32, 6) | 否 | 否 |
| 航行 | ITMLine.ShipId | Nvarchar(20) | **是** | 否 |
| 物料编号 | ITMLine.ShipItemId | Nvarchar(20) | 否 | 否 |
| 量化指标 | ITMLine.ShipMeasurement | Nvarchar(20) | 否 | 否 |
| 度量单位 | ITMLine.ShipMeasurementUnit | 数字(32, 6) | 否 | 否 |
| 纸箱数量 | ITMLine.ShipNoOfCartons | Int | 否 | 否 |
| 位置 | ITMLine.ShipPosition | 数字(32, 6) | 否 | 否 |
| Quantity | ITMLine.ShipQty | Int | 否 | 否 |
| 采购订单编号 | ITMLine.TransRefId | 数字(32, 6) | **是** | 否 |
| 单位 | ITMLine.UnitId | Int | 否 | 否 |
| 卷 | ITMLine.Volume | Nvarchar(10) | 否 | 否 |
| 权重 | ITMLine.Weight | 数字(32, 6) | 否 | 否 |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>转移单的航行行 (ITMTransferLineEntity)

航行行表示航行中包含的单个转移单行。 此关系是通过 **转移单编号** 和 **转移行编号** 字段建立的。 航行行引用了为航行、装运集装箱和帐页创建的每个先前记录。 `ITMTransferLineEntity` 实体支持此功能。 下表列出了构成此实体的字段和映射。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 货币 | ITMLine.CurrencyCode | Nvarchar(3) | 否 | 否 |
| 净额 | ITMLine.LineAmountMST | 数字(32, 6) | 否 | 否 |
| 装运集装箱 | ITMLine.ShipContainerId | Int | 否 | 否 |
| 公司 | ITMLine.ShipDataArea | Nvarchar(20) | **是** | 否 |
| 已申报数量 | ITMLine.ShipDeclaredQty | Nvarchar(4) | 否 | 否 |
| 帐页 | ITMLine.ShipFolioId | 数字(32, 6) | 否 | 否 |
| 航行 | ITMLine.ShipId | Nvarchar(20) | **是** | 否 |
| 物料编号 | ITMLine.ShipItemId | Nvarchar(20) | 否 | 否 |
| 量化指标 | ITMLine.ShipMeasurement | Nvarchar(20) | 否 | 否 |
| 度量单位 | ITMLine.ShipMeasurementUnit | 数字(32, 6) | 否 | 否 |
| 纸箱数量 | ITMLine.ShipNoOfCartons | Int | 否 | 否 |
| 位置 | ITMLine.ShipPosition | 数字(32, 6) | 否 | 否 |
| Quantity | ITMLine.ShipQty | Int | 否 | 否 |
| 转移行号 | ITMLine.TransferLineNumber | 数字(32, 6) | **是** | 否 |
| 转移单编号 | ITMLine.TransRefId | 数字(32, 6) | **是** | 否 |
| 单位 | ITMLine.UnitId | Int | 否 | 否 |
| 卷 | ITMLine.Volume | Nvarchar(10) | 否 | 否 |
| 权重 | ITMLine.Weight | 数字(32, 6) | 否 | 否 |

### <a name="reference-table"></a>引用表

航行行是通过与未结入站订单行关联创建的。 此行可以位于采购订单上，也可以是转移单上的收货交易。 航行行表 (`ITMLine`) 中的 `RefTableId` 字段通过引用表编号指定该行与哪个订单类型相关。 如果在创建数据的表中引用了特定的表编号，则将根据这些值拆分实体。

在选择到岸成本采购行实体或到岸成本转移行实体时，引用表 (`RefTableId`) 和交易类型 (`TransType`) 的值是隐式值。

### <a name="validation"></a>验证

航行行直接引用航行记录、装运集装箱记录和帐页记录。 如果独立于用于创建这些引用记录的实体来使用采购行实体 (`ITMPurchaseLinesEntity`) 或转移行实体 (`ITMPurchaseLinesEntity`)，则 **航行 ID** (`ShipId`)、**装运集装箱** (`ShipContainerId`) 和 **帐页** (`ShipFolioId`) 值必须与对应表中的现有记录匹配。 否则，导入将失败。

如果行实体用作同一导入会话的一部分，则必须在创建航行行之前创建那些其他实体。 否则，无法成功验证值。 如果占位符值用于航行或帐页编号，则仅当相同占位符用于航行行实体中的航行或帐页编号时，才能创建关联。

如果采购订单或转移单行已分配给现有航行行，则将不会创建新的航行行。 在将订单行分配给新航行之前，必须将其从当前航行中删除。

### <a name="order-line-identification"></a>订单行标识

航行行直接引用引用 **记录 ID** (`RefRecId`)、**库存维度 ID** (`InventDimId`) 和 **库存交易 ID** (`InventTransId`) 值。 使用数据实体时，不再需要包含这些值。 相反，现在必须包括订单行号。 订单行号和订单编号一起使这些参考值中的每一个都能够被识别。

### <a name="voyage-line-quantity"></a>航行行数量

由于航行行直接与订单行关联，因此使用实体输入的 **数量** (`ShipQty`) 值要求值匹配。 验证根据采购订单行或转移行上的数量运行。 如果验证失败，将不会处理该记录。

### <a name="calculated-fields"></a>计算字段

**重量** 和 **体积** 计算字段接受通过数据实体接收的值。 如果未提供值，则系统值将用于更新这些字段（如果系统值可用）。 对于到岸成本，会按以下方式计算值：

- *重量* = *数量* × *物料毛重*
- *体积* = *数量*×（*物料总深度* × *物料总高度* × *物料总宽度*）

## <a name="sequencing"></a>先后顺序

由于表之间存在依赖关系，必须首先创建航行记录。 只有在创建航行、装运集装箱和帐页之后才能创建航行行。

要创建没有验证警告的航行，系统必须按照以下顺序处理实体：

1. 航行 (`ITMTableEntity`)
1. 装运集装箱 (`ITMContainersEntity`)
1. 帐页 (`ITMFolioTableEntity`)
1. 航行行（`ITMPurchaseLinesEntity` 或 `ITMTransferLinesEntity`）
