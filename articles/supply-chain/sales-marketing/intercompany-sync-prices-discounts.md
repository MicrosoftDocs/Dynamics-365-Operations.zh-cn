---
title: 同步内部公司价格和折扣
description: 本主题介绍了内部公司销售订单和采购订单的价格和折扣的同步
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 90fa2244b5947c37b8498d1c70cddf894979f931
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673625"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>同步内部公司价格和折扣

[!include [banner](../../includes/banner.md)]

折扣和价格在内部公司销售订单和内部公司采购订单之间总是同步的。 您也可以使原始销售订单同步到价格和折扣，并使价格和折扣同步到原始销售订单，以便所有的订单都具有相同的价格和折扣。 您从 **所有客户** 列表页上的 **常规** 选项卡中访问的 **内部公司** 页面中执行此操作 - 从 **销售和市场营销** 或 **采购** 中。

**价格和折扣** 字段同步到内部公司销售订单行。 这表示通过选择 **允许编辑价格** 字段和 **允许编辑折扣** 字段，您已允许在内部公司销售订单与内部公司采购订单之间进行更改。 对内部公司销售订单中单位价格、计价单位或销售计费所做的更改决定了内部公司采购订单行中的价格。

如果在内部公司销售订单或内部公司采购订单上启用 **允许编辑价格** 和 **允许编辑折扣**，那么您可以手动在两个订单上更改价格或折扣。 否则不能。

如果在内部公司销售订单上未启用 **允许编辑价格** 和 **允许编辑折扣**，那么您无法在内部公司销售订单上对价格（或费用）或折扣进行手动更改。

如果在内部公司采购订单上未启用 **允许编辑价格** 和 **允许编辑折扣**，那么您无法在内部公司采购订单上对价格（或费用）或折扣进行手动更改。

如果在内部公司采购订单和内部公司销售订单上都启用了 **允许编辑价格** 和 **允许编辑折扣**，那么您可以对这两个订单进行手动更改。 但是，这可能会导致一种情况，在该情况中，由某个人做出的更新会被同一订单上的另一个公司的另一个人进行的更新否决。

> [!NOTE]
> 如果您已经对内部公司采购订单和内部公司销售订单同时启用 **价格和折扣** 字段，您将无法对定价进行控制。

若要避免这些类型的冲突，最好只允许更改内部公司销售订单或内部公司采购订单中的价格和折扣。 这是通过在任何这些订单上启用 **允许编辑价格** 和 **允许编辑折扣** 字段来完成的。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
