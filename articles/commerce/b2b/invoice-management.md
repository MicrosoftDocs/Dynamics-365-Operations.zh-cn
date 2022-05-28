---
title: B2B 电子商务网站的发票管理
description: 本主题介绍 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站的发票管理功能。
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 60cb0c8aaede4a0eaeed80cf5ebe41068da57836
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686292"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>B2B 电子商务网站的发票管理

[!include [banner](../../includes/banner.md)]

本主题介绍 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站的发票管理功能。

对于处理 B2B 交易的公司来说，接受客户信用订单，然后在客户完成订单后向客户发送发票，这是常见做法。 付款条款针对客户定义，可能会有一些折扣来激励客户按时或提前付款。 为帮助提高按时收到付款的可能性，B2B 电子商务网站允许客户查看他们的所有发票。 客户可以轻松筛选发票来查看已付、未付和部分支付的发票以及截止日期。

![B2B 网站上的发票页面。](../media/ViewInvoices.png)

> [!NOTE]
> 登录用户只能查看和支付自己的发票。 如果在 Commerce headquarters 中客户记录的 **发票和交货** 快速选项卡上的 **发票帐户** 下拉菜单中配置了组织帐户，用户将能够查看和支付组织帐户的发票。

在 B2B 网站的 **发票** 页面上，用户可以选择未支付或部分支付的发票，然后选择 **支付发票**。 所选发票将添加到购物车中，用户可以继续付款。 然后，用户可以决定是支付发票的全部金额还是部分金额。 用户不能使用分期付款付款方式支付发票。

> [!NOTE]
> 只有当前没有商品时，才能将发票添加到购物车中。 反之，只有当前没有发票时，才能将商品添加到购物车中。 Microsoft 计划在未来的 Commerce 版本中取消此限制。

![B2B 网站上的购物车页面。](../media/PayInvoice.png)

在 **发票** 页面上，用户还可以选择发票旁边的 **请求发票**。 通过这种方式，用户可以请求将发票的详细信息发送到他们注册的电子邮件地址。

![请求发票对话框。](../media/RequestInvoice2.png)

用户请求发票后，请求将进入 **我的帐户** 页面的 **B2B 请求** 部分。 然后，在 Commerce headquarters 中运行 **P-0001** 和 **同步订单和渠道请求** 作业后，将触发发票电子邮件，B2B 请求的状态将被标记为已完成。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
