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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>筛选内部公司订单以避免同步订单和订单行

[!include [banner](../../includes/banner.md)]

可以筛选内部公司订单以避免同步 **订单** 和 **订单行** 实体。 在某些情况下，客户参与应用中不需要内部公司订单详细信息。

每个标准 Common Data Service 实体均已经过扩展，带有对 **IntercompanyOrder** 字段的引用，而改双向写入映射已修改为引用筛选器中的更多字段。 结果是不再同步内部公司订单。 此过程避免了客户参与应用中不必要的数据。

1. 向 **CDS 销售订单标头** 添加对 **IntercompanyOrder** 的引用。 仅在内部公司订单中填充。 **SalesTable** 中有 **IntercompanyOrder** 字段。

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="将暂存映射到目标，销售订单标题":::
    
2. 扩展 **CDS 销售订单标头** 之后，映射中将可以使用 **IntercompanyOrder** 字段。 将 `INTERCOMPANYORDER == ""` 作为查询字符串应用筛选器。

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="销售订单标题，编辑查询":::

3. 向 **CDS 销售订单行** 添加对 **IntercompanyInventTransId** 的引用。  仅在内部公司订单中填充。 **SalesLine** 中将有字段 **InterCompanyInventTransID**。

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="将暂存映射到目标，SalesOrderLine":::

4. 扩展 **CDS 销售订单行** 之后，映射中将可以使用 **IntercompanyInventTransId** 字段。 将 `INTERCOMPANYINVENTTRANSID == ""` 作为查询字符串应用筛选器。

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="销售订单行，编辑查询":::

5. 按照步骤 1 和 2 中扩展 Common Data Service 实体的相同方法扩展 **销售发票标题 V2** 和 **销售发票行 V2**。 然后添加筛选器查询。 **销售发票标题 V2** 的筛选器字符串为 `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`。 **销售发票行 V2** 的筛选器字符串为 `INTERCOMPANYINVENTTRANSID == ""`。

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="将暂存映射到目标，销售发票标题":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="销售发票标题，编辑查询":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="销售发票行，编辑查询":::

6. **报价单** 实体没有内部公司关系。 如果有人为您的内部公司客户之一创建报价但，则可以使用 **CustGroup** 字段将所有这些客户归为一个客户组。  标题和行可以扩展以添加 **CustGroup** 字段，然后筛选以不包括该组。

    :::image type="content" source="media/filter-cust-group.png" alt-text="将暂存映射到目标，销售报价单标题":::

7. 扩展 **报价单** 实体之后，以 `CUSTGROUP !=  "<company>"` 为查询字符串应用筛选器。

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="销售报价单标题，编辑查询":::
