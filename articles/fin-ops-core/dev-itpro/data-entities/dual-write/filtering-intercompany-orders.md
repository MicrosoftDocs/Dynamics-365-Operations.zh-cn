---
title: 筛选内部公司订单以避免同步订单和订单行
description: 此主题介绍如何筛选内部公司订单以避免同步订单和订单行。
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701025"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="67753-103">筛选内部公司订单以避免同步订单和订单行</span><span class="sxs-lookup"><span data-stu-id="67753-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67753-104">可以筛选内部公司订单以避免同步 **订单** 和 **订单行** 实体。</span><span class="sxs-lookup"><span data-stu-id="67753-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="67753-105">在某些情况下，客户参与应用中不需要内部公司订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="67753-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="67753-106">每个标准 Common Data Service 实体均已经过扩展，带有对 **IntercompanyOrder** 字段的引用，而改双向写入映射已修改为引用筛选器中的更多字段。</span><span class="sxs-lookup"><span data-stu-id="67753-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="67753-107">结果是不再同步内部公司订单。</span><span class="sxs-lookup"><span data-stu-id="67753-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="67753-108">此过程避免了客户参与应用中不必要的数据。</span><span class="sxs-lookup"><span data-stu-id="67753-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="67753-109">向 **CDS 销售订单标头** 添加对 **IntercompanyOrder** 的引用。</span><span class="sxs-lookup"><span data-stu-id="67753-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="67753-110">仅在内部公司订单中填充。</span><span class="sxs-lookup"><span data-stu-id="67753-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="67753-111">**SalesTable** 中有 **IntercompanyOrder** 字段。</span><span class="sxs-lookup"><span data-stu-id="67753-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="将暂存映射到目标，销售订单标题":::
    
2. <span data-ttu-id="67753-113">扩展 **CDS 销售订单标头** 之后，映射中将可以使用 **IntercompanyOrder** 字段。</span><span class="sxs-lookup"><span data-stu-id="67753-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="67753-114">将 `INTERCOMPANYORDER == ""` 作为查询字符串应用筛选器。</span><span class="sxs-lookup"><span data-stu-id="67753-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="销售订单标题，编辑查询":::

3. <span data-ttu-id="67753-116">向 **CDS 销售订单行** 添加对 **IntercompanyInventTransId** 的引用。</span><span class="sxs-lookup"><span data-stu-id="67753-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="67753-117">仅在内部公司订单中填充。</span><span class="sxs-lookup"><span data-stu-id="67753-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="67753-118">**SalesLine** 中将有字段 **InterCompanyInventTransID**。</span><span class="sxs-lookup"><span data-stu-id="67753-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="将暂存映射到目标，SalesOrderLine":::

4. <span data-ttu-id="67753-120">扩展 **CDS 销售订单行** 之后，映射中将可以使用 **IntercompanyInventTransId** 字段。</span><span class="sxs-lookup"><span data-stu-id="67753-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="67753-121">将 `INTERCOMPANYINVENTTRANSID == ""` 作为查询字符串应用筛选器。</span><span class="sxs-lookup"><span data-stu-id="67753-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="销售订单行，编辑查询":::

5. <span data-ttu-id="67753-123">按照步骤 1 和 2 中扩展 Common Data Service 实体的相同方法扩展 **销售发票标题 V2** 和 **销售发票行 V2**。</span><span class="sxs-lookup"><span data-stu-id="67753-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="67753-124">然后添加筛选器查询。</span><span class="sxs-lookup"><span data-stu-id="67753-124">Then add the filter queries.</span></span> <span data-ttu-id="67753-125">**销售发票标题 V2** 的筛选器字符串为 `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`。</span><span class="sxs-lookup"><span data-stu-id="67753-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="67753-126">**销售发票行 V2** 的筛选器字符串为 `INTERCOMPANYINVENTTRANSID == ""`。</span><span class="sxs-lookup"><span data-stu-id="67753-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="将暂存映射到目标，销售发票标题":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="销售发票标题，编辑查询":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="销售发票行，编辑查询":::

6. <span data-ttu-id="67753-130">**报价单** 实体没有内部公司关系。</span><span class="sxs-lookup"><span data-stu-id="67753-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="67753-131">如果有人为您的内部公司客户之一创建报价但，则可以使用 **CustGroup** 字段将所有这些客户归为一个客户组。</span><span class="sxs-lookup"><span data-stu-id="67753-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="67753-132">标题和行可以扩展以添加 **CustGroup** 字段，然后筛选以不包括该组。</span><span class="sxs-lookup"><span data-stu-id="67753-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="将暂存映射到目标，销售报价单标题":::

7. <span data-ttu-id="67753-134">扩展 **报价单** 实体之后，以 `CUSTGROUP !=  "<company>"` 为查询字符串应用筛选器。</span><span class="sxs-lookup"><span data-stu-id="67753-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="销售报价单标题，编辑查询":::
