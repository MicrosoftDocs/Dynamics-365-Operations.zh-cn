---
title: Cookie 合规
description: 本主题介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215689"
---
# <a name="cookie-compliance"></a>Cookie 合规性

[!include [banner](includes/banner.md)]

本主题介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。

## <a name="overview"></a>概览

当跟踪影响电子商务客户的技术时，隐私是一个重要因素。 由于诸如欧盟 (EU) 的一般数据保护条例 (GDPR) 等隐私合规标准，今天处于活动状态的任何站点都必须考虑电子隐私准则。 由于默认情况下许多电子商务站点在全球范围内都可以访问，因此审查电子商务站点的合规标准很重要。

要了解有关 Microsoft 针对 Cookie 合规使用的基本原则的详细信息，请访问 [Microsoft 信任中心](https://www.microsoft.com/trust-center)。 在该站点上，您还可以获得有关合规和隐私区域的更多信息。

下表显示了 Dynamics 365 Commerce 站点放置的 cookie 的当前参考列表。

| Cookie 名称                               | 用法                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | 存储用于单点登录的 (SSO) 的 Microsoft Azure Active Directory (Azure AD) 身份验证 cookie。 存储加密的用户主体信息（名字、姓氏、电子邮件）。 |
| &#95;msdyn365___cart&#95;                           | 存储用于获取已添加到购物车实例的产品列表的购物车 ID。 |
| &#95;msdyn365___ucc&#95;                            | Cookie 合规性同意跟踪。                          |
| ai_session                                  | 检测有多少用户活动会话已包含应用的某些页面和功能。 |
| ai_user                                     | 检测有多少人使用了应用及其功能。 使用匿名 ID 对用户进行计数。 |
| b2cru                                       | 动态存储重定向 URL。                              |
| JSESSIONID                                  | 由付款连接器 Adyen 用来存储用户会话。       |
| OpenIdConnect.nonce.&#42;                       | 身份验证                                               |
| x-ms-cpim-cache:.&#42;                          | 用于维护请求状态。                      |
| x-ms-cpim-csrf                              | 用于防御 CRSF 的跨网站请求伪造 (CRSF) 令牌。     |
| x-ms-cpim-dc                                | 用于将请求路由到适当的生产身份验证服务器实例。 |
| x-ms-cpim-rc.&#42;                              | 用于将请求路由到适当的生产身份验证服务器实例。 |
| x-ms-cpim-slice                             | 用于将请求路由到适当的生产身份验证服务器实例。 |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | 用于维护 SSO 会话。                        |
| x-ms-cpim-trans                             | 用于跟踪事务（对企业对消费者 (B2C) 站点进行身份验证的打开选项卡的数量），包括当前事务。 |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>电子商务站点中的站点用户 cookie 同意 

如果模块中的电子商务站点功能使用非基本 cookie，则必须先获取站点用户的同意，然后才能跟踪 cookie。 若要允许站点用户在电子商务站点中提供 cookie 同意，站点作者必须在页面的页眉中添加和配置 cookie 同意模块，以确保提示提供和接收同意。 必须先提供站点用户同意，然后才能在站点页面中显示使用非基本 cookie 的功能或模块。

## <a name="additional-resources"></a>其他资源

[辅助功能和功能](accessibility.md)

[合规性概览](compliance-overview.md)

[添加隐私政策页面](add-privacy-page.md)

[替换与所跟踪内容更改相关联的用户 ID](replace-IDs-tracked-changes.md)

[Cookie 同意模块](cookie-consent-module.md) 
 
[标题模块](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]