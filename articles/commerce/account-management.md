---
title: 帐户管理页面和模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206623"
---
# <a name="account-management-pages-and-modules"></a>帐户管理页面和模块

[!include [banner](includes/banner.md)]

此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。

帐户管理指的是 Dynamics 365 Commerce 中一组用于管理与用户帐户有关的信息的页面。 帐户管理页包括帐户管理登陆页、用户个人资料页、用户地址页、订单历史记录页、订单详细信息页、会员页和愿望列表页。

### <a name="account-management-landing-page"></a>帐户管理登陆页

帐户管理登陆页使用以下模块：

- **容器** - 所有帐户管理登录页面模块均应放置在容器中。 
- **帐户欢迎磁贴** – 此模块用于提供帐户管理页中的欢迎消息。 它包括标题的属性。
- **帐户通用磁贴** - 此模块可用于提供标题和指向帐户管理页面（例如“订单历史记录”或“我的个人资料”页面）的链接。 通用磁贴模块可用于为任何页面配置磁贴。 在 Fabrikam 中，此模块用于帐户管理登录页面上的“订单历史记录”和“我的个人资料”页面链接。
- **帐户愿望列表磁贴** – 此模块用于提供客户愿望列表项的摘要。 例如，可能显示“您的愿望列表中有 10 项”。 其中包括标题和“查看详细信息”链接的属性。 应该将此“查看详细信息”链接配置为重定向到愿望列表页。 
- **帐户地址磁贴** – 此模块用于提供用户地址的摘要。 例如，可能显示“您已向您的帐户添加了 2 个地址”。 其中包括标题和“查看详细信息”链接的属性。 应该将此“查看详细信息”链接配置为重定向到用户地址页。
- **帐户会员磁贴** – 此模块用于显示和链接到会员计划信息。 此磁贴有两种状态：一种状态显示用于加入会员计划的链接（如果用户还不是会员）。 当用户已经是会员时，另一状态显示用于查看会员详细信息页面的链接。 属性包括标题、“注册”链接和“查看会员”链接。 应该将此“查看会员”链接配置为重定向到会员页。 应该将“注册”链接配置为重定向到一个页面，用户可在其中加入会员计划。 

### <a name="order-history-page"></a>订单历史记录页

订单历史记录页使用订单历史记录模块显示用户最近下达的所有订单。

### <a name="order-details-page"></a>订单详细信息

订单详细信息页提供每个订单的详细信息，可从订单历史记录页访问。 它使用订单详细信息模块，后者需要销售 ID 或交易 ID 才能检索订单详细信息。

### <a name="user-profile-page"></a>用户个人资料页

用户个人资料页显示用户帐户详细信息，如用户的姓名和电子邮件地址。 它使用用户个人资料详细信息和用户个人资料编辑模块。 虽然不能删除电子邮件地址，但可以对其进行编辑。 用户个人资料页面还显示用户首选项，使用户可以选择加入或退出某些功能，例如建议列表的个性化。 

### <a name="user-address-page"></a>用户地址页

用户地址页显示与用户帐户关联的地址的列表。 用户在结帐期间提供这些地址，或直接将其添加到此页面中。 用户地址模块用于添加和编辑地址，设置主地址和在页面中显示现有地址。

### <a name="wish-list-page"></a>愿望列表页

愿望列表页显示已添加到客户的愿望列表的项。 它使用愿望列表模块显示愿望列表项。

### <a name="loyalty-page"></a>会员页面

如果客户已经是会员计划成员，则会员页可供客户查看会员详细信息。 也可以查看在最近交易中获得的积分和兑换的积分。 该页面使用会员详细信息模块来展示会员详细信息。 

要加入会员计划，可以用会员注册和会员条款模块创建一个市场营销页面。 如果用户不是会员计划的成员，则这些模块将使用户能够注册。

## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]