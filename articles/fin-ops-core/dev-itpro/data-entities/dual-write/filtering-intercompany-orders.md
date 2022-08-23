---
title: 筛选内部公司订单以避免同步订单和订单行
description: 本文说明如何筛选内部公司订单，以不同步 Orders 和 OrderLines 实体。
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f5b7831e103aaa219394099b79537bf0842d9be8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289271"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>筛选内部公司订单以避免同步订单和订单行

[!include [banner](../../includes/banner.md)]

您可以筛选内部公司订单以不同步 **Orders** 和 **OrderLines** 表。 在某些情况下，客户互动应用中不需要内部公司订单详细信息。

每个标准 Dataverse 表已通过对 **IntercompanyOrder** 列的引用扩展，双写入映射已经修改，可以引用筛选器中的更多列。 因此，内部公司订单不再同步。 此流程帮助阻止客户互动应用中不必要的数据。

1. 通过添加对 **IntercompanyOrder** 列的引用扩展 **CDS 销售订单标头** 表。 仅在内部公司订单中填充此列。 **SalesTable** 表中有 **IntercompanyOrder** 列。

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="将暂存映射到 CDS 销售订单标头的目标页面。":::

2. 扩展 **CDS 销售订单标头** 之后，映射中将可以使用 **IntercompanyOrder** 列。 应用将 `INTERCOMPANYORDER == ""` 作为查询字符串的筛选器。

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS 销售订单标头的编辑查询对话框。":::

3. 通过添加对 **IntercompanyInventTransId** 列的引用扩展 **CDS 销售订单行** 表。 仅在内部公司订单中填充此列。 **SalesLine** 表中有 **InterCompanyInventTransId** 列。

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="将暂存映射到 CDS 销售订单行的目标页面。":::

4. 扩展 **CDS 销售订单行** 之后，映射中将可以使用 **IntercompanyInventTransId** 列。 应用将 `INTERCOMPANYINVENTTRANSID == ""` 作为查询字符串的筛选器。

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS 销售订单行的编辑查询对话框。":::

5. 重复步骤 1 和 2 扩展 **销售发票标题 V2** 表并添加筛选器查询。 在这种情况下，使用 `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` 作为筛选器的查询字符串。

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="将暂存映射到销售发票标头 V2 的目标页面。":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="销售发票标头 V2 的编辑查询对话框。":::

6. 重复步骤 3 和 4 扩展 **销售发票行 V2** 表并添加筛选器查询。 在这种情况下，使用 `INTERCOMPANYINVENTTRANSID == ""` 作为筛选器的查询字符串。

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="销售发票行 V2 的编辑查询对话框。":::

7. **报价单** 表没有内部公司关系。 如果有人为您的内部公司客户之一创建报价单，您可以使用 **CustGroup** 列将所有这些客户归为一个客户组。 您可以通过添加 **CustGroup** 列来扩展标题和行，然后进行筛选，以使该组不包括在内。

    :::image type="content" source="media/filter-cust-group.png" alt-text="将暂存映射到 CDS 销售报价单标头的目标页面。":::

8. 扩展 **报价单** 后，应用将 `CUSTGROUP != "<company>"` 作为查询字符串的筛选器。

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS 销售报价单标头的编辑查询对话框。":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
