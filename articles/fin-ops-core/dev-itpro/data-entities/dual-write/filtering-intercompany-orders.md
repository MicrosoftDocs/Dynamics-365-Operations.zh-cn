---
title: 筛选内部公司订单以避免同步订单和订单行
description: 本主题说明如何筛选内部公司订单，以不同步 Orders 和 OrderLines 实体。
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568094"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="be83d-103">筛选内部公司订单以避免同步订单和订单行</span><span class="sxs-lookup"><span data-stu-id="be83d-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be83d-104">您可以筛选内部公司订单以不同步 **Orders** 和 **OrderLines** 表。</span><span class="sxs-lookup"><span data-stu-id="be83d-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="be83d-105">在某些情况下，客户互动应用中不需要内部公司订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="be83d-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="be83d-106">每个标准 Dataverse 表已通过对 **IntercompanyOrder** 列的引用扩展，双写入映射已经修改，可以引用筛选器中的更多列。</span><span class="sxs-lookup"><span data-stu-id="be83d-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="be83d-107">因此，内部公司订单不再同步。</span><span class="sxs-lookup"><span data-stu-id="be83d-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="be83d-108">此流程帮助阻止客户互动应用中不必要的数据。</span><span class="sxs-lookup"><span data-stu-id="be83d-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="be83d-109">通过添加对 **IntercompanyOrder** 列的引用扩展 **CDS 销售订单标头** 表。</span><span class="sxs-lookup"><span data-stu-id="be83d-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="be83d-110">仅在内部公司订单中填充此列。</span><span class="sxs-lookup"><span data-stu-id="be83d-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="be83d-111">**SalesTable** 表中有 **IntercompanyOrder** 列。</span><span class="sxs-lookup"><span data-stu-id="be83d-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="将暂存映射到 CDS 销售订单标头的目标页面":::

2. <span data-ttu-id="be83d-113">扩展 **CDS 销售订单标头** 之后，映射中将可以使用 **IntercompanyOrder** 列。</span><span class="sxs-lookup"><span data-stu-id="be83d-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="be83d-114">应用将 `INTERCOMPANYORDER == ""` 作为查询字符串的筛选器。</span><span class="sxs-lookup"><span data-stu-id="be83d-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS 销售订单标头的编辑查询对话框":::

3. <span data-ttu-id="be83d-116">通过添加对 **IntercompanyInventTransId** 列的引用扩展 **CDS 销售订单行** 表。</span><span class="sxs-lookup"><span data-stu-id="be83d-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="be83d-117">仅在内部公司订单中填充此列。</span><span class="sxs-lookup"><span data-stu-id="be83d-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="be83d-118">**SalesLine** 表中有 **InterCompanyInventTransId** 列。</span><span class="sxs-lookup"><span data-stu-id="be83d-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="将暂存映射到 CDS 销售订单行的目标页面":::

4. <span data-ttu-id="be83d-120">扩展 **CDS 销售订单行** 之后，映射中将可以使用 **IntercompanyInventTransId** 列。</span><span class="sxs-lookup"><span data-stu-id="be83d-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="be83d-121">应用将 `INTERCOMPANYINVENTTRANSID == ""` 作为查询字符串的筛选器。</span><span class="sxs-lookup"><span data-stu-id="be83d-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS 销售订单行的编辑查询对话框":::

5. <span data-ttu-id="be83d-123">重复步骤 1 和 2 扩展 **销售发票标题 V2** 表并添加筛选器查询。</span><span class="sxs-lookup"><span data-stu-id="be83d-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="be83d-124">在这种情况下，使用 `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` 作为筛选器的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="be83d-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="将暂存映射到销售发票标题 V2 的目标页面":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="销售发票标题 V2 的编辑查询对话框":::

6. <span data-ttu-id="be83d-127">重复步骤 3 和 4 扩展 **销售发票行 V2** 表并添加筛选器查询。</span><span class="sxs-lookup"><span data-stu-id="be83d-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="be83d-128">在这种情况下，使用 `INTERCOMPANYINVENTTRANSID == ""` 作为筛选器的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="be83d-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="销售发票行 V2 的编辑查询对话框":::

7. <span data-ttu-id="be83d-130">**报价单** 表没有内部公司关系。</span><span class="sxs-lookup"><span data-stu-id="be83d-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="be83d-131">如果有人为您的内部公司客户之一创建报价单，您可以使用 **CustGroup** 列将所有这些客户归为一个客户组。</span><span class="sxs-lookup"><span data-stu-id="be83d-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="be83d-132">您可以通过添加 **CustGroup** 列来扩展标题和行，然后进行筛选，以使该组不包括在内。</span><span class="sxs-lookup"><span data-stu-id="be83d-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="将暂存映射到 CDS 销售报价单标题的目标页面":::

8. <span data-ttu-id="be83d-134">扩展 **报价单** 后，应用将 `CUSTGROUP != "<company>"` 作为查询字符串的筛选器。</span><span class="sxs-lookup"><span data-stu-id="be83d-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS 销售报价单标题的编辑查询对话框":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]