---
title: 跨多个客户订单和账单的退回物料
description: 本主题介绍了 Dynamics 365 Commerce 中支持跨多个客户订单和账单进行退货的功能。
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976655"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>跨多个客户订单和账单的退回物料

[!include [banner](includes/banner.md)]


本文介绍了两项功能，这些功能可对多个账单的客户订单退货进行优化。 

## <a name="enable-refunds-over-multiple-captures"></a>启用针对多个捕获的退款

此功能可针对同一客户订单进行多次关联退款。 

1. 转到 **功能管理** 工作区并搜索 **启用针对多个捕获的退款**。
2. 选择 **启用针对多个订单的退款**，然后单击 **启用**。 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>对具有部分数量的退货启用正确的税金计算

此功能可确保在使用多个账单进行订单退货时，最终的税金等于最初收取的税额。 

1. 转到 **功能管理** 工作区并搜索 **对具有部分数量的退货启用正确的税金计算**。
2. 选择 **对具有部分数量的退货启用正确的税金计算**，然后单击 **启用**。 


## <a name="process-returns"></a>处理退货

启用这些功能并将更改同步到商店后，商店的出纳可以选择多个销售订单，以处理客户的退货。

选中订单后，将显示所有订单发票上的所有可退产品的列表。 然后，出纳可以选择要退回的产品。 将为所有选定的产品创建单个退货单。

如果订单已全部退货，那么退还给客户的税额等于最初收取的税额。

