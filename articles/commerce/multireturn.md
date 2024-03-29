---
title: 跨多个客户订单和发票的退回物料
description: 本文将介绍 Dynamics 365 Commerce 中支持跨多个客户订单和发票进行退货的功能。
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890312"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>跨多个客户订单和发票的退回物料

[!include [banner](includes/banner.md)]


可以跨多个订单和发票处理退货。 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>配置 Commerce 以支持跨多个客户订单和发票进行退货

1. 转到 **Commerce 参数 \> 客户订单**。
1. 启用 **支持针对多个订单的退货** 参数。 

## <a name="process-returns"></a>处理退货

启用该参数并将更改同步到商店后，商店的出纳可以选择多个销售订单，以处理客户的退货。

选中订单后，将显示所有订单发票上的所有可退产品的列表。 然后，出纳可以选择要退回的产品。 将为所有选定的产品创建单个退货单。
