---
title: Hybrid customer orders
description: "较一客户订单是一个将领取或之后装运包含的订单，产品可执行商店按客户，以及产品。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid customer orders

较一客户订单是一个将领取或之后装运包含的订单，产品可执行商店按客户，以及产品。

在零售的工序的 Microsoft Dynamics 365 -中，可以选择执行所有产品或执行客户订单的所选产品。 标记自动执行开票的产品系列，在创建订单后，与这同样将领取的订单，订单的在创建后。 由于在较订单添加在领料和装运产品线的存款金额百分比取决于与执行行的所有金额。 对于较订单，在客户订单和模式提供现款货商店模式的系统之间切换如下：

-   如果在购物车的所有产品设置**请执行交货**，则将事务作为一自运付现的交易记录。
-   如果在购物车的任意或所有的行设置到或** ** **或领取装运交货**，则将事务作为客户订单交易记录。

如果行的选择和**选择的装运，领取** ** ** **或选择所选 Carry out **，选择，则特定的行设置具有该交货方法。 在这种情况下，工序的顺流流量照常继续。 **，但是，如果领取选择** **，装运** **或选择所选 Carry out **选择，但无所选的行，则列出所有行的新购物篮的页面将打开。 在该屏幕上，您可以一次选择多行的交货方法设置。 如果您针对为该行选择使用该付款方式，分配给行的所有以往的交货方法将替代。

<a name="see-also"></a>请参阅
--------

[] 客户订单概览 (overview.md 客户订单)


