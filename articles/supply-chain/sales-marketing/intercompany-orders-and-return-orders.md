---
title: 内部公司订单和退货单
description: 本文说明内部公司订单和退货单
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
ms.openlocfilehash: 65d0dc6049969ff7d8f84ca4eb3baf486ddad660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859018"
---
# <a name="intercompany-orders-and-return-orders"></a>内部公司订单和退货单

[!include [banner](../../includes/banner.md)]

本文描述如何创建和更新内部公司采购订单、销售订单、退货单、采购协议和销售协议。

## <a name="about-intercompany-orders"></a>关于内部公司订单

创建内部公司销售订单时，Microsoft Dynamics 365 Supply Chain Management 会自动创建相应的采购订单。 同样，创建内部公司采购订单时将提示自动创建相应的内部公司销售订单。

这适用于双边订单（两个关联公司之间的交易记录）和多数三边公司（内部公司交易记录源自外部客户的销售订单）的情况。

## <a name="intercompany-order-example"></a>内部公司订单示例

有两个关联公司。 公司 A 是销售子公司，公司 B 是经销单位。 在以下情况下自动创建内部公司销售订单和采购订单：

- 当公司 A 创建采购订单且供应商为公司 B 时，将在公司 B 中自动创建内部公司销售订单。双边订单链由公司 A 中的采购订单和公司 B 中的内部公司销售订单构成。
- 当公司 A 创建销售订单且客户为公司 B 时，将在公司 B 中自动创建内部公司采购订单。双边订单链由公司 B 中的销售订单和公司 A 中的内部公司采购订单构成。
- 当公司 A 为外部客户最初创建销售订单时，可以在公司 A 中自动创建采购订单，这会相应地提示在公司 B 中自动创建内部公司销售订单。三边订单链的销售订单、公司 A 中的采购订单以及公司 B 中的内部公司销售订单构成。

## <a name="about-intercompany-return-orders"></a>关于内部公司退货单

您可以退回内部公司物料，这非常类似于普通退货。 不过，对于内部公司物料，来自外部客户的退货单将创建内部公司采购订单。 这又导致自动创建内部公司销售退货单。 您还可以在不存在外部客户退货单的情况下退回内部公司物料。

内部公司退货单（类似于一般退货单），在 **创建退货单** 页面上启动。

在 Microsoft Dynamics 365 Supply Chain Management 中，内部公司销售和采购协议将自动更新以反映退返物料。 当退回物料时，自动更新该物料的销售或采购协议承诺反映数量或金额的变化。

## <a name="intercompany-return-order-example"></a>内部公司退货单示例

公司 A 创建采购订单链接到内部公司物料的采购协议。 内部公司采购订单将自动在公司 B 中创建链接到相应的销售协议。 采购协议和销售协议关联为内部公司协议。

公司 A 退回内部公司物料给公司 B。公司 B 创建物料的退货单，并且，采购退货单在公司 A 中自动创建。与原始订单关联的采购协议和销售协议将自动调整承诺反映数量或金额的变化。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
