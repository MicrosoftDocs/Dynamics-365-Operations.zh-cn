---
title: Cookie 合规性
description: 本文介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。
author: BrianShook
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 20bdc6466c5d89709f8ba790eb567bd7d8bbb15c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273604"
---
# <a name="cookie-compliance"></a>Cookie 合规性

[!include [banner](includes/banner.md)]

本文介绍 Cookie 合规注意事项以及 Microsoft Dynamics 365 Commerce 中包含的默认政策。

当跟踪影响电子商务客户的技术时，隐私是一个重要因素。 由于诸如欧盟 (EU) 的一般数据保护条例 (GDPR) 等隐私合规标准，今天处于活动状态的任何站点都必须考虑电子隐私准则。 由于默认情况下许多电子商务站点在全球范围内都可以访问，因此审查电子商务站点的合规标准很重要。

要了解有关 Microsoft 针对 Cookie 合规使用的基本原则的详细信息，请访问 [Microsoft 信任中心](https://www.microsoft.com/trust-center)。 在该站点上，您还可以获得有关合规和隐私区域的更多信息。

下表显示了 Dynamics 365 Commerce 站点放置的 cookie 的当前参考列表。

| Cookie 名称                               | 使用                                                        | 生存期 |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | 存储用于单点登录的 (SSO) 的 Microsoft Azure Active Directory (Azure AD) 身份验证 cookie。 存储加密的用户主体信息（名字、姓氏、电子邮件）。 | 会话 |
| \_msdyn365___cart_                           | 存储用于获取已添加到购物车实例的产品列表的购物车 ID。 | 会话 |
| \_msdyn365___checkout_cart_                           | 存储用于获取已添加到结帐购物车实例的产品列表的结帐购物车 ID。 | 会话 |
| \_msdyn365___ucc_                            | Cookie 合规性同意跟踪。                          | 1 年 |
| ai_session                                  | 检测有多少用户活动会话已包含应用的某些页面和功能。 | 30 分钟 |
| ai_user                                     | 检测有多少人使用了应用及其功能。 使用匿名 ID 对用户进行计数。 | 1 年 |
| b2cru                                       | 动态存储重定向 URL。                              | 会话 |
| JSESSIONID                                  | 由付款连接器 Adyen 用来存储用户会话。       | 会话 |
| OpenIdConnect.nonce.&#42;                       | 身份验证                                               | 11 分钟 |
| x-ms-cpim-cache:.&#42;                          | 用于维护请求状态。                      | 会话 |
| x-ms-cpim-csrf                              | 用于防御 CRSF 的跨网站请求伪造 (CRSF) 令牌。     | 会话 |
| x-ms-cpim-dc                                | 用于将请求路由到适当的生产身份验证服务器实例。 | 会话 |
| x-ms-cpim-rc.&#42;                              | 用于将请求路由到适当的生产身份验证服务器实例。 | 会话 |
| x-ms-cpim-slice                             | 用于将请求路由到适当的生产身份验证服务器实例。 | 会话 |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | 用于维护 SSO 会话。                        | 会话 |
| x-ms-cpim-trans                             | 用于跟踪事务（对企业对消费者 (B2C) 站点进行身份验证的打开选项卡的数量），包括当前事务。 | 会话 |
| \_msdyn365___muid_                            | 用于针对环境激活试验的情况；用作用户 ID 以供试验。 | 1 年 |
| \_msdyn365___exp_                             | 用于针对环境激活试验的情况；用于度量性能负载均衡。         | 1 小时 |
| d365mkt                                       | 在 Commerce 站点构建器中在 **站点设置 \> 常规 \> 启用基于位置的商店检测** 启用了基于位置的检测来跟踪用户的 IP 地址以获取商店位置建议时使用。      | 1 小时 |
| \_msdyn365___tuid_                           | 仅在为环境激活试验时使用；生成 GUID 以充当用户标识符。 如果用户的登录状态发生变化，值将发生变化。      | 1 年 |
| \_msdyn365___aud_0                          | 存储目标所使用的客户细分值，并且仅当目标在站点用户请求的页面或片段上配置时才会被使用。 仅当客户细分值来自第三方细分提供程序时才放置 Cookie。      | 7 天 |
| \_msdyn365___aud_1                           | 存储目标所使用的客户细分值，并且仅当目标在站点用户请求的页面或片段上配置时才会被使用。 仅当客户细分值来自第三方细分提供程序时才放置 Cookie。      | 7 天 |
| \_msdyn365___aud_2                           | 存储目标所使用的客户细分值，并且仅当目标在站点用户请求的页面或片段上配置时才会被使用。 仅当客户细分值来自第三方细分提供程序时才放置 Cookie。      | 7 天 |
| d365gi                                       | 使用第三方地理位置服务时，此 Cookie 会存储地理位置数据。      | 1 天 |

如果站点用户选择站点内的任何社交媒体链接，还将在其浏览器中跟踪下表中的 cookie。


| 域                      | Cookie               | 说明                                                  | 源                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn Ads ID 同步                                      | LinkedIn Feed 和 Insight 标记                                |
| .linkedin.com               | li_sugr                  | 浏览器标识符                                           | 如果 IP 地址不在指定的国家/地区，则为 LinkedIn Insight Tag 标记 |
| .linkedin.com               | BizographicsOptOut       | 确定第三方跟踪的选择退出状态。              | LinkedIn 来宾控制和行业选择退出页面           |
| .linkedin.com               | \_guid                    | Google Ads 的浏览器标识符。                            | LinkedIn Feed                                                |
| .linkedin.com               | li_oatml                 | 用于转换跟踪、重新定位和分析的成员间接标识符。 | LinkedIn Ads 和 Insight 标记                                |
| 各种第一方域 | li_fat_id                | 用于转换跟踪、重新定位和分析的成员间接标识符。 | LinkedIn Ads 和 Insight 标记                                |
| .adsymptotic.com            | U                        | 浏览器标识符                                           | 如果 IP 地址不在指定的国家/地区，则为 LinkedIn Insight Tag 标记 |
| .linkedin.com                | bcookie                  | 浏览器 ID cookie                                            | 对 LinkedIn 的请求                                         |
| .linkedin.com                | bscookie                 | 安全浏览器 cookie                                        | 对 LinkedIn 的请求                                         |
| .linkedin.com               | lang                     | 设置默认区域设置和语言。                                 | 对 LinkedIn 的请求                                         |
| .linkedin.com                | lidc                     | 用于路线选择。                                             | 对 LinkedIn 的请求                                         |
| .linkedin.com               | aam_uuid                 | Adobe Audience Manager cookie                                                     | 针对 ID 同步设置                                              |
| .linkedin.com               | \_ga                      | Google Analytics cookie                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics cookie                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics cookie                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Cookie 包含当前登录用户的用户 ID。  |   Facebook                                                           |
| .facebook.com               | datr                     | 用于标识用于连接到与登录用户无关的 Facebook 的 Web 浏览器。 | Facebook                                                             |
| .facebook.com               | wd                       | 存储浏览器窗口维度，并由 Facebook 用于优化页面的呈现。 | Facebook                                                             |
| .facebook.com               | xs                       | 表示会话编号的两位数字。 该值的第二部分是会话密码。 |  Facebook                                                            |
| .facebook.com               | fr                       | 包含用于目标广告的唯一浏览器和用户 ID。 |  Facebook                                                            |
| .facebook.com               | sb                       | 用于改善 Facebook 好友建议。                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Cookie 包含当前登录用户的用户 ID。  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Cookie 包含当前登录用户的用户 ID。  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | 当用户选择“Pinterest”按钮时，Cookie 包含页面。      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | 当用户选择“Pinterest”按钮时，Cookie 包含页面。      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | 当创建 cookie 时，包含用户 ID 和时间戳。 |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | 当用户选择“Pinterest”按钮时，Cookie 包含页面。      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | 当用户选择“Pinterest”按钮时，Cookie 包含页面。      | Pinterest                                                             |
| .pinterest.com              | 本地存储            |                                                              |  Pinterest                                                            |
| .pinterest.com              | 服务工作人员          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>电子商务站点中的站点用户 cookie 同意 

如果模块中的电子商务站点功能使用非基本 cookie，则必须先获取站点用户的同意，然后才能跟踪 cookie。 若要允许站点用户在电子商务站点中提供 cookie 同意，站点作者必须在页面的页眉模块中添加和配置 cookie 同意模块，以确保提示提供和接收同意。 必须先提供站点用户同意，然后才能在站点页面中显示使用非基本 cookie 的功能或模块。

## <a name="additional-resources"></a>其他资源

[辅助功能和功能](accessibility.md)

[合规性概览](compliance-overview.md)

[添加隐私政策页面](add-privacy-page.md)

[替换与所跟踪内容更改相关联的用户 ID](replace-IDs-tracked-changes.md)

[Cookie 同意模块](cookie-consent-module.md) 
 
[标题模块](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
