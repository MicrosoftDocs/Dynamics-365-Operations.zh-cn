---
title: 帐户管理页和模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785368"
---
# <a name="account-management-pages-and-modules"></a>帐户管理页和模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。

## <a name="overview"></a>概览

帐户管理指的是 Dynamics 365 Commerce 中一组用于管理与用户帐户有关的信息的页面。 帐户管理页包括帐户管理登陆页、用户个人资料页、用户地址页、订单历史记录页、订单详细信息页、会员页和愿望列表页。

### <a name="account-management-landing-page"></a>帐户管理登陆页

帐户管理登陆页使用以下模块：

- **内容放置** – 此模块是容器模块，其中包含帐户管理登陆页中的所有模块。
- **帐户欢迎项** – 此模块用于提供帐户管理页中的欢迎消息。 其中包括标题和磁贴大小属性。 **磁贴大小**属性定义模块在内容放置模块中的宽度。 值范围为 **1** 到 **12**，其中的 **12** 表示内容放置容器的完整宽度。
- **帐户订单下达项** – 此模块用于提供用户帐户下达的订单数量的摘要。 其中包括标题、磁贴大小和“视图详细信息”链接的属性。 应该将此“视图详细信息”链接配置为重定向到订单历史记录页。
- **帐户个人资料放置项** – 此模块用于提供用户个人资料的摘要。 其中包括标题、磁贴大小和“视图详细信息”链接的属性。 应该将此“视图详细信息”链接配置为重定向到用户个人资料页。
- **帐户愿望列表项** – 此模块用于提供有关客户愿望列表的项的摘要。 例如，可能显示“您的愿望列表中有 10 项”。 其中包括标题、磁贴大小和“视图详细信息”链接的属性。 应该将此“视图详细信息”链接配置为重定向到愿望列表页。
- **帐户地址项** – 此模块用于提供用户地址的摘要。 例如，可能显示“您已向您的帐户添加了 2 个地址”。 其中包括标题、磁贴大小和“视图详细信息”链接的属性。 应该将此“视图详细信息”链接配置为重定向到用户地址页。
- **帐户会员项** – 此模块用于显示和链接到会员计划信息。 其中包括标题、磁贴大小和“成为会员”链接的属性。 应该将此“视图详细信息”链接配置为重定向到会员页。 应该将“成为会员”链接配置为重定向到一个页面，用户可在其中加入会员计划。

### <a name="order-history-page"></a>订单历史记录页

订单历史记录页使用订单历史记录模块显示用户最近下达的所有订单。

### <a name="order-details-page"></a>订单详细信息

订单详细信息页提供每个订单的详细信息，可从订单历史记录页访问。 它使用订单详细信息模块，后者需要销售 ID 或交易 ID 才能检索订单详细信息。

### <a name="user-profile-page"></a>用户个人资料页

用户个人资料页显示用户帐户详细信息，如用户的姓名和电子邮件地址。 它使用用户个人资料模块。 虽然不能删除电子邮件地址，但可以对其进行编辑。

### <a name="user-address-page"></a>用户地址页

用户地址页显示与用户帐户关联的地址的列表。 用户在结帐期间提供这些地址，或直接将其添加到此页面中。 用户地址模块用于添加和编辑地址，设置主地址和在页面中显示现有地址。

### <a name="wish-list-page"></a>愿望列表页

愿望列表页显示已添加到客户的愿望列表的项。 它使用愿望列表模块显示愿望列表项。

### <a name="loyalty-page"></a>会员页面

会员页供客户加入会员计划；如果客户已经是会员计划成员，则用于查看其计划详细信息。 也可以查看在最近交易中获得的积分和兑换的积分。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
