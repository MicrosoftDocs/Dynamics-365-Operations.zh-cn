---
title: "订单保留"
description: "本主题描述使用 Dynamics 365 for Retail 将订单置于暂停状态。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>订单保留

[!include [banner](includes/banner.md)]

本主题描述使用 Dynamics 365 for Retail 将订单置于暂停状态。

出于各种原因，可将订单置于暂停状态。 例如，在可以验证客户地址或付款方式之前，或在经理可以查看客户的信用额度之前，您可以将订单置于暂停状态。 在销售流程中，有时必须将销售订单置于暂停状态。 例如，由于客户付款出现问题、可疑欺诈或经理必须审核销售订单，可能将销售订单置于暂停状态。 在销售订单置于暂停状态时，一个订单保留代码被分配给销售订单来表明保留的原因。 在**销售和市场营销** &gt; **设置** &gt; **销售订单** &gt; **订单保留代码**中配置销售订单保留代码。 可在创建订单时或稍后手动将销售订单置于暂停状态。 此外，可以根据欺诈规则自动将订单置于暂停状态。 在将销售订单置于暂停状态时，可能需要使用更多信息更新该订单。 或者，在继续使用销售订单时，可能需要签出该订单。 您可使用订单保留工作台来签出销售订单，将其签回甚至覆盖另一个用户的签出（**零售** &gt; **客户** &gt; **订单保留**）。 在订单即将完成时，您需在完成订单流程之前删除保留。




