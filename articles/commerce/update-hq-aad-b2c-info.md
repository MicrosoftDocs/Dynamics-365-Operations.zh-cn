---
title: 使用新的 Azure AD B2C 信息更新 Commerce Headquarters
description: 本文介绍如何使用新的 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 信息更新 Microsoft Dynamics 365 Commerce headquarters。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785233"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>使用新的 Azure AD B2C 信息更新 Commerce Headquarters

[!include [banner](includes/banner.md)]

本文介绍如何使用新的 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 信息更新 Microsoft Dynamics 365 Commerce headquarters。

完成了上面的 Azure AD B2C 预配步骤之后，必须在 Dynamics 365 Commerce 环境中注册 Azure AD B2C 应用程序。

若要使用新的 Azure AD B2C 信息更新 Headquarters，请执行以下步骤。

1. 在 Commerce 中，转到 **Commerce 共享参数**，然后选择左菜单中的 **标识提供程序**。
1. 在 **标识提供程序** 下，执行以下操作：
    1. 在 **颁发者** 框中，输入标识提供程序颁发者字符串。 要查找您的颁发者字符串，请参阅下面的[获取总部设置的颁发者字符串](#obtain-issuer-string-for-headquarters-setup)。
    1. 在 **名称** 框中，输入颁发者记录的名称。
    1. 在 **类型** 框中，输入 **Azure AD B2C (id_token)**。
1. 选择上面的 B2C 标识提供程序项之后，在 **回复方** 下执行以下操作：
    1. 在 **客户端 ID** 框中，输入您的 B2C 应用程序 ID，您可以在 B2C 应用程序属性页的 **应用程序 ID** 框中找到此 ID。
    1. 在 **类型** 框中，输入 **公开**。
    1. 在 **用户类型** 框中，输入 **客户**。
1. 在操作窗格上，选择 **保存**。
1. 在 Commerce 搜索框中，搜索 **配送计划**
1. 在 **配送计划** 页的左导航菜单中，选择作业 **1110 全局配置**。
1. 在操作窗格上，选择 **立即运行**。

### <a name="obtain-issuer-string-for-headquarters-setup"></a>获取总部设置的颁发者字符串

若要获取标识提供程序颁发者字符串，请执行以下步骤。

1. 在 Azure 门户的 Azure AD B2C 页面上，导航到 **注册和登录** 用户流。
1. 在左侧导航菜单中选择 **页面布局**，在 **布局名称** 下，选择 **统一注册或登录页面**，然后选择 **运行用户流**。
1. 确保您的应用程序设置为上面创建的预期 Azure AD B2C 应用程序，然后选择显示在 **运行用户流** 标题下包括 ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` 的用户流链接。 （不要选择 **运行用户流**。）将打开一个新选项卡，显示用于收集颁发者字符串的策略的元数据。
1. 在浏览器选项卡中显示的元数据页面上，复制类似于以下示例的标识提供者颁发者字符串（**颁发者** 值以“https://”开头，以"/v2.0/"结尾）。
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。
 
**或者**：若要手动构造相同的元数据 URL，请按照下列步骤操作。

1. 使用您的 B2C 租户和策略创建以下格式的元数据地址 URL：``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - 示例：``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``。
1. 在浏览器地址栏中输入该元数据地址 URL。
1. 在元数据中，复制标识提供程序颁发者 URL（**颁发者** 的值）。
    - 示例：``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请继续[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
