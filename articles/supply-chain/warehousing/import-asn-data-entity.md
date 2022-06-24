---
title: 通过 V3 数据实体导入传入 ASN
description: 本文说明如何管理通过入站 ASN 数据实体导入入站发货通知单 (ASN)。
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ac45e070d0473547c48da1380377de3d4bf60bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907107"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>通过 V3 数据实体导入传入 ASN

[!include [banner](../../includes/banner.md)]

发货通知单 (ASN) 通知您有关供应商交货的信息。 它们帮助发送方描述装运的内容以及相关的其他信息，例如物料和包装。

ASN 可以帮助仓库工作人员了解收货的时间和内容。 因此，他们可以做好准备。 此外，仓库工作人员可以使用 ASN 将装运的详细信息与之前创建的相关采购订单进行匹配。

本文显示了一系列场景，通过示例演示如何使用 ASN 文件。

> [!IMPORTANT]
> *入站 ASN* 导入仅适用于为高级仓库管理 (WMS) 启用的物料。 在您收到 ASN 之前，必须在系统中针对发送该 ASN 的供应商注册采购订单。

## <a name="inbound-asn-v3-entity"></a>入站 ASN V3 实体

您可以使用 *入站 ASN V3* 复合数据实体导入入站 ASN。 *入站 ASN V3* 利用以下实体：

- 入站负荷标题
- 入站装运标题
- 入站负荷装箱结构
- 入站负荷装箱结构案例
- 入站负荷装箱结构案例行
- 入站负荷装箱结构行

*入站 ASN V3* 复合数据实体专门面向使用基于 XML 文件的导入的异步集成场景。

## <a name="xml-format-for-importing-asns"></a>用于导入 ASN 的 XML 格式

Microsoft Dynamics 365 Supply Chain Management 支持以下用于导入 ASN 的 XML 格式。 XML 文件中的每个节点表示来自单独实体的一个属性。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>示例

以下子部分提供了供应商装运的 ASN XML 导入文件的示例。

### <a name="example-1"></a>示例 1

以下示例显示了一个 XML 文件，用于在不包含案例详细信息时为一个采购订单导入供应商装运。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>示例 2

以下示例显示了一个 XML 文件，用于在包含案例详细信息时为一个采购订单导入供应商装运。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>示例 3

以下示例显示了一个 XML 文件，用于在包含案例详细信息时为多个采购订单导入供应商装运。

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>检查导入 ASN 文件的结果

按照以下步骤检查导入 ASN 文件的结果。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 查找并打开作为 ASN 导入的一部分创建的负荷。
1. 在 **负荷** 快速选项卡上，您应该看到基于 XML 文件的值。
1. 在 **负荷行** 快速选项卡上，您应该看到基于 XML 文件的采购订单编号和物料详细信息。
1. 在操作窗格上的 **装运和收货** 选项卡上，在 **收货** 组中，选择 **装箱结构** 以查看负荷的装箱结构。
1. 在 **托盘** 快速选项卡上，您应该看到基于 XML 文件的牌照。
1. 在 **案例** 快速选项卡上，您应该看到基于 XML 文件的案例。
1. 在 **物料** 快速选项卡上，您应该看到基于 XML 文件的物料和数量。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
