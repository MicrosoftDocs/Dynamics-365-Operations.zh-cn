---
title: 启用来宾结帐订单查找功能
description: 本文介绍如何启用 Microsoft Dynamics 365 Commerce 中的来宾结帐订单查找功能。
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4f381f1ec0ea08f18db3cac474e8990906364504
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286883"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>启用来宾结帐订单查找功能

[!include [banner](includes/banner.md)]

本文介绍如何启用 Microsoft Dynamics 365 Commerce 中的来宾结帐订单查找功能。

来宾结帐订单查找功能让以来宾用户身份进行购买的客户可以查找自己的订单。 当用户希望执行如下功能时，这项订单查找功能非常有用：检查订单中产品的履行状态，验证订单的收货地址，重新订购产品，或确认订单的提货商店。

以注册用户身份下达订单的客户登录后，可以看到自己的订单详细信息，但是使用来宾结帐功能的客户则看不到。 但是，如果启用了来宾结帐订单查找功能，则会提供一个窗体，供客户搜索其以来宾身份下达的订单。 在此窗体中，客户输入订单确认 ID 和其在结帐时指定的电子邮件地址（可选）。

此外，还可以在任何与订单有关的事务电子邮件中添加链接或按钮，用于将客户直接带到其订单的订单详细信息页。 此链接或按钮同时适用于已注册用户和来宾用户下达的订单。

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>在 Commerce Headquarters 中开启必需功能

若要启用来宾结帐订单查找功能，必须在 Commerce Headquarters 中的 **工作区 \> 功能管理** 中开启下列功能。

| 功能 | 目的 |
|---------|---------|
| Retail 匿名用户搜索订单详细信息选择功能 | 此功能显示 Commerce 参数中的用户界面，供您为未经身份验证的用户启用订单查找 API 和配置个人数据的显示方式。 |
| 启用生成更强的渠道引用 ID | 此功能生成一个更安全的 12 字符渠道引用 ID（订单确认 ID），当查找订单时，可通过查询字符串传递该 ID。 |
| 跨渠道生成一致的渠道引用 ID 格式 | 此功能为通过电子商务站点、零售销售点 (POS) 或呼叫中心下达的订单生成安全渠道引用 ID。 必须先开启 **启用生成更强的渠道引用 ID** 功能，才能开启此功能。 |

开启 **Retail 匿名用户搜索订单详细信息选择功能** 功能之后，必须在 Commerce Headquarters 中启用支持未经身份验证的订单查找功能的 API。 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 客户订单**。 在 **客户订单** 页面中的 **订单搜索** 快速选项卡上，将 **启用未经身份验证的订单查找** 选项设置为 **是**，如下图中所示。

## <a name="manage-the-display-of-personal-data"></a>管理个人数据的显示

Commerce Headquarters 中 **客户订单** 页上的 **订单搜索** 快速选项卡内有一个 **在来宾订单查找中包括个人数据** 字段，可帮助您控制对客户显示哪些个人信息。 此个人信息包括客户的装运地址和客户信用卡号的最后四位数字。 默认情况下，启用未经身份验证的订单查找后，不会向客户显示个人信息。 下表对可用选项进行了说明。

| 选项 | 结果 |
|--------|--------|
| 从不 | 默认值。 订单查找中不显示个人信息。 当已登录的注册用户查找自己在之前登录后创建的订单时，他们可以看到自己的个人信息。 |
| 仅限访客订单 | 将在客户以来宾身份创建的订单的订单查找中显示个人信息。 如果订单是注册用户创建的，则该用户必须登录，然后才能查看自己的个人信息。 |
| 所有订单 | 所有订单查找中都将显示个人信息。 |

> [!NOTE]
> 这些选项决定何时对匿名来宾用户显示客户地址和客户信用卡号最后四位数字之类个人数据。 为了帮助保护注册客户的隐私，我们建议您选择 **仅限来宾订单** 选项。 但是，最安全的选项是 **从不**。

更改 **在来宾订单查找中包括个人数据** 字段的值之后，必须通过转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 配送计划**，在 Commerce Headquarters 中运行作业 1070（**渠道配置**）。

## <a name="configure-the-order-lookup-module"></a>配置订单查找模块

Commerce 模块库中的订单查找模块用于呈现来宾用户用于查找订单的窗体。 任何不要求客户登录的页面的主体插槽中都可以包含订单查找模块。 有关如何配置此模块的信息，请参阅[订单查找模块](order-lookup-module.md)。

## <a name="configure-the-order-details-page"></a>配置订单详细信息页

您的电子商务站点上的订单详细信息页面必须配置为不需要登录，来宾用户才可以查看他们的订单详细信息。 要关闭订单详细信息页面的登录要求，在 Commerce 站点构建器中打开该页面，在树视图中选择 **默认页面(必需)** 槽，然后清除右侧属性窗格底部的 **需要登录?** 复选框。

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>在交易电子邮件中添加指向订单详细信息的链接

在与订单相关的电子邮件中，您可以提供一个链接或按钮，将客户带到他们订单的订单详细信息页面。 要添加此链接或按钮，创建一个指向您的电子商务站点上订单详细信息页面的 HTML 超链接，并将订单确认 ID 和客户的电子邮件地址作为 URL 参数传递，如下例所示。

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

## <a name="additional-resources"></a>其他资源

[订单查找模块](order-lookup-module.md)

[设置电子邮件通知配置文件](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
