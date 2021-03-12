---
title: 采用双写入的库存可用性
description: 本主题提供有关如何以双写入方式检查库存可用性的信息。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839541"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="3bb7d-103">采用双写入的库存可用性</span><span class="sxs-lookup"><span data-stu-id="3bb7d-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3bb7d-104">使用库存可用性，可以在 Microsoft Dynamics 365 Sales 中先检查库存，然后再将产品添加到 **报价单**、**订单** 或 **发票** 页面。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="3bb7d-105">例如，检查库存并将履行日期确定为[目标客户到现金](dual-write-prospect-to-cash.md)流程的一个关键任务。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="3bb7d-106">如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="3bb7d-107">您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="3bb7d-108">现有库存</span><span class="sxs-lookup"><span data-stu-id="3bb7d-108">On-hand inventory</span></span>

<span data-ttu-id="3bb7d-109">在 Dynamics 365 Sales 中，**报价单**、**订单** 和 **发票** 页面的标题中已经添加了一个新的 **现有库存量** 按钮。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3bb7d-110">选择此按钮时，将出现一个对话框，您可以在其中指定要检查其现有库存量的公司和产品。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="3bb7d-111">此对话框显示的信息与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="3bb7d-112">此对话框返回 Dynamics 365 Supply Chain Management 中的库存信息。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3bb7d-113">此信息包括以下数量：</span><span class="sxs-lookup"><span data-stu-id="3bb7d-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="3bb7d-114">现有数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-114">On-hand quantity</span></span>
- <span data-ttu-id="3bb7d-115">预留现有数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="3bb7d-116">可用现有数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-116">Available on-hand quantity</span></span>
- <span data-ttu-id="3bb7d-117">订购数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-117">Ordered quantity</span></span>
- <span data-ttu-id="3bb7d-118">在单数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-118">On-order quantity</span></span>
- <span data-ttu-id="3bb7d-119">预留的订购数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="3bb7d-120">可用总数</span><span class="sxs-lookup"><span data-stu-id="3bb7d-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="3bb7d-121">ATP 信息</span><span class="sxs-lookup"><span data-stu-id="3bb7d-121">ATP information</span></span>

<span data-ttu-id="3bb7d-122">在 Sales 中，**报价单**、**订单** 和 **发票** 页面的行项中已经添加了新的 **ATP 信息** 按钮。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3bb7d-123">选择此按钮时，将出现一个对话框，您可以在其中指定公司、产品、库存站点、库存仓库和订单数量。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="3bb7d-124">此对话框具有与[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置相同的设置。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="3bb7d-125">此对话框返回 Supply Chain Management 中的 ATP 信息。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="3bb7d-126">此信息包括以下数量：</span><span class="sxs-lookup"><span data-stu-id="3bb7d-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="3bb7d-127">ATP 数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-127">ATP quantity</span></span>
- <span data-ttu-id="3bb7d-128">收货数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-128">Receipt quantity</span></span>
- <span data-ttu-id="3bb7d-129">发货数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-129">Issue quantity</span></span>
- <span data-ttu-id="3bb7d-130">现有数量</span><span class="sxs-lookup"><span data-stu-id="3bb7d-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="3bb7d-131">工作原理</span><span class="sxs-lookup"><span data-stu-id="3bb7d-131">How it works</span></span>

<span data-ttu-id="3bb7d-132">当您在 **报价单**、**订单** 或 **发票** 页上选择 **现有库存量** 按钮时，会对 **现有库存量** API 进行实时双写入调用。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="3bb7d-133">API 计算给定产品的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="3bb7d-134">结果存储在 **InventCDSInventoryOnHandRequestEntity** 和 **InventCDSInventoryOnHandEntryEntity** 表中，然后通过双写入将其写入 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="3bb7d-135">要使用此功能，您需要运行以下双写入映射。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="3bb7d-136">运行映射时跳过初始同步。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="3bb7d-137">CDS 现有库存条目 (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="3bb7d-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="3bb7d-138">CDS 现有库存请求 (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="3bb7d-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="3bb7d-139">模板</span><span class="sxs-lookup"><span data-stu-id="3bb7d-139">Templates</span></span>
<span data-ttu-id="3bb7d-140">以下模板可用于公开现有库存量数据。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="3bb7d-141">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="3bb7d-141">Finance and Operations apps</span></span> | <span data-ttu-id="3bb7d-142">Customer engagement 应用</span><span class="sxs-lookup"><span data-stu-id="3bb7d-142">Customer engagement app</span></span> | <span data-ttu-id="3bb7d-143">说明</span><span class="sxs-lookup"><span data-stu-id="3bb7d-143">Description</span></span> 
---|---|---
[<span data-ttu-id="3bb7d-144">CDS 库存现有条目</span><span class="sxs-lookup"><span data-stu-id="3bb7d-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="3bb7d-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="3bb7d-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="3bb7d-146">CDS 库存现有请求</span><span class="sxs-lookup"><span data-stu-id="3bb7d-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="3bb7d-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="3bb7d-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="3bb7d-148">CDS 现有库存条目 (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="3bb7d-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="3bb7d-149">此模板在 Finance and Operations 应用与 Dataverse 之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="3bb7d-150">Finance and Operations 字段</span><span class="sxs-lookup"><span data-stu-id="3bb7d-150">Finance and Operations field</span></span> | <span data-ttu-id="3bb7d-151">映射类型</span><span class="sxs-lookup"><span data-stu-id="3bb7d-151">Map type</span></span> | <span data-ttu-id="3bb7d-152">Customer engagement 字段</span><span class="sxs-lookup"><span data-stu-id="3bb7d-152">Customer engagement field</span></span> | <span data-ttu-id="3bb7d-153">默认值</span><span class="sxs-lookup"><span data-stu-id="3bb7d-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="3bb7d-154">CDS 现有库存请求 (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="3bb7d-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="3bb7d-155">此模板在 Finance and Operations 应用与 Dataverse 之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="3bb7d-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="3bb7d-156">Finance and Operations 字段</span><span class="sxs-lookup"><span data-stu-id="3bb7d-156">Finance and Operations field</span></span> | <span data-ttu-id="3bb7d-157">映射类型</span><span class="sxs-lookup"><span data-stu-id="3bb7d-157">Map type</span></span> | <span data-ttu-id="3bb7d-158">Customer engagement 字段</span><span class="sxs-lookup"><span data-stu-id="3bb7d-158">Customer engagement field</span></span> | <span data-ttu-id="3bb7d-159">默认值</span><span class="sxs-lookup"><span data-stu-id="3bb7d-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




