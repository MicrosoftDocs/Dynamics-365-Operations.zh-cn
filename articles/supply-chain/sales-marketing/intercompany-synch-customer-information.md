---
title: 同步内部公司客户信息
description: 本文介绍了内部公司订单的客户信息同步
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
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897507"
---
# <a name="synchronize-intercompany-customer-information"></a>同步内部公司客户信息

[!include [banner](../../includes/banner.md)]

如果在创建销售订单时或在对客户、供应商参考或客户申请编号进行更改时启用了 **客户信息** 字段，则会同步客户信息。

您始终可以更改这些同步字段中的值。 但是，只能通过选择此参数确定该值是否复制到其他内部公司订单。 如果您已经在内部公司销售订单上启用了 **客户信息** 字段，则对内部公司销售订单的更改将同步到内部公司采购订单。 如果您在内部公司采购订单上也启用了 **客户信息** 字段，则它也同步回原始销售订单。

> [!NOTE]
> 如果您在内部公司采购订单和内部公司销售订单上都启用了 **客户信息** 字段，则在一个公司中某个人进行的更新将由其他公司中其他人对同一订单进行的更新所控制。

最佳实践是在内部公司采购订单上启用 **客户信息** 字段。 这将实现在原始销售订单与内部公司采购订单之间同步，以及从内部公司采购订单向内部公司销售订单同步。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
