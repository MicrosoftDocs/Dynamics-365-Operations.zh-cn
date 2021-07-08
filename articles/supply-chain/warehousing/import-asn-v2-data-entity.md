---
title: 通过 V2 数据实体导入入站 ASN
description: 本主题说明如何管理通过入站 ASN V2 数据实体导入入站发货通知单 (ASN)。
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249063"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="d7b56-103">通过 V2 数据实体导入入站 ASN</span><span class="sxs-lookup"><span data-stu-id="d7b56-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7b56-104">发货通知单 (ASN) 通知您有关供应商交货的信息。</span><span class="sxs-lookup"><span data-stu-id="d7b56-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="d7b56-105">它们帮助发送方描述装运的内容以及相关的其他信息，例如物料和包装。</span><span class="sxs-lookup"><span data-stu-id="d7b56-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="d7b56-106">ASN 可以帮助仓库工作人员了解收货的时间和内容。</span><span class="sxs-lookup"><span data-stu-id="d7b56-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="d7b56-107">因此，他们可以做好准备。</span><span class="sxs-lookup"><span data-stu-id="d7b56-107">Therefore, they can prepare.</span></span> <span data-ttu-id="d7b56-108">此外，仓库工作人员可以使用 ASN 将装运的详细信息与之前创建的相关采购订单进行匹配。</span><span class="sxs-lookup"><span data-stu-id="d7b56-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="d7b56-109">本主题显示了一系列场景，通过示例演示如何使用 ASN 文件。</span><span class="sxs-lookup"><span data-stu-id="d7b56-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7b56-110">*入站 ASN* 导入仅适用于为高级仓库管理 (WMS) 启用的物料。</span><span class="sxs-lookup"><span data-stu-id="d7b56-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="d7b56-111">在您收到 ASN 之前，必须在系统中针对发送该 ASN 的供应商注册采购订单。</span><span class="sxs-lookup"><span data-stu-id="d7b56-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="d7b56-112">入站 ASN V2 实体</span><span class="sxs-lookup"><span data-stu-id="d7b56-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="d7b56-113">您可以使用 *入站 ASN V2* 复合数据实体导入入站 ASN。</span><span class="sxs-lookup"><span data-stu-id="d7b56-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="d7b56-114">*入站 ASN V2* 利用以下实体：</span><span class="sxs-lookup"><span data-stu-id="d7b56-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="d7b56-115">入站负荷标题</span><span class="sxs-lookup"><span data-stu-id="d7b56-115">Inbound load header</span></span>
- <span data-ttu-id="d7b56-116">入站装运标题</span><span class="sxs-lookup"><span data-stu-id="d7b56-116">Inbound shipment header</span></span>
- <span data-ttu-id="d7b56-117">入站负荷装箱结构</span><span class="sxs-lookup"><span data-stu-id="d7b56-117">Inbound load packing structures</span></span>
- <span data-ttu-id="d7b56-118">入站负荷装箱结构案例</span><span class="sxs-lookup"><span data-stu-id="d7b56-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="d7b56-119">入站负荷装箱结构案例行</span><span class="sxs-lookup"><span data-stu-id="d7b56-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="d7b56-120">入站负荷装箱结构行</span><span class="sxs-lookup"><span data-stu-id="d7b56-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="d7b56-121">*入站 ASN V2* 复合数据实体专门面向使用基于 XML 文件的导入的异步集成场景。</span><span class="sxs-lookup"><span data-stu-id="d7b56-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="d7b56-122">用于导入 ASN 的 XML 格式</span><span class="sxs-lookup"><span data-stu-id="d7b56-122">XML format for importing ASNs</span></span>

<span data-ttu-id="d7b56-123">Microsoft Dynamics 365 Supply Chain Management 支持以下用于导入 ASN 的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="d7b56-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="d7b56-124">XML 文件中的每个节点表示来自单独实体的一个属性。</span><span class="sxs-lookup"><span data-stu-id="d7b56-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="d7b56-125">示例</span><span class="sxs-lookup"><span data-stu-id="d7b56-125">Examples</span></span>

<span data-ttu-id="d7b56-126">以下子部分提供了供应商装运的 ASN XML 导入文件的示例。</span><span class="sxs-lookup"><span data-stu-id="d7b56-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="d7b56-127">示例 1</span><span class="sxs-lookup"><span data-stu-id="d7b56-127">Example 1</span></span>

<span data-ttu-id="d7b56-128">以下示例显示了一个 XML 文件，用于在不包含案例详细信息时为一个采购订单导入供应商装运。</span><span class="sxs-lookup"><span data-stu-id="d7b56-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="d7b56-129">示例 2</span><span class="sxs-lookup"><span data-stu-id="d7b56-129">Example 2</span></span>

<span data-ttu-id="d7b56-130">以下示例显示了一个 XML 文件，用于在包含案例详细信息时为一个采购订单导入供应商装运。</span><span class="sxs-lookup"><span data-stu-id="d7b56-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="d7b56-131">示例 3</span><span class="sxs-lookup"><span data-stu-id="d7b56-131">Example 3</span></span>

<span data-ttu-id="d7b56-132">以下示例显示了一个 XML 文件，用于在包含案例详细信息时为多个采购订单导入供应商装运。</span><span class="sxs-lookup"><span data-stu-id="d7b56-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="d7b56-133">检查导入 ASN 文件的结果</span><span class="sxs-lookup"><span data-stu-id="d7b56-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="d7b56-134">按照以下步骤检查导入 ASN 文件的结果。</span><span class="sxs-lookup"><span data-stu-id="d7b56-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="d7b56-135">转到 **仓库管理 \> 负荷 \> 所有负荷**。</span><span class="sxs-lookup"><span data-stu-id="d7b56-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d7b56-136">查找并打开作为 ASN 导入的一部分创建的负荷。</span><span class="sxs-lookup"><span data-stu-id="d7b56-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="d7b56-137">在 **负荷** 快速选项卡上，您应该看到基于 XML 文件的值。</span><span class="sxs-lookup"><span data-stu-id="d7b56-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="d7b56-138">在 **负荷行** 快速选项卡上，您应该看到基于 XML 文件的采购订单编号和物料详细信息。</span><span class="sxs-lookup"><span data-stu-id="d7b56-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="d7b56-139">在操作窗格上的 **装运和收货** 选项卡上，在 **收货** 组中，选择 **装箱结构** 以查看负荷的装箱结构。</span><span class="sxs-lookup"><span data-stu-id="d7b56-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="d7b56-140">在 **托盘** 快速选项卡上，您应该看到基于 XML 文件的牌照。</span><span class="sxs-lookup"><span data-stu-id="d7b56-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="d7b56-141">在 **案例** 快速选项卡上，您应该看到基于 XML 文件的案例。</span><span class="sxs-lookup"><span data-stu-id="d7b56-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="d7b56-142">在 **物料** 快速选项卡上，您应该看到基于 XML 文件的物料和数量。</span><span class="sxs-lookup"><span data-stu-id="d7b56-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
