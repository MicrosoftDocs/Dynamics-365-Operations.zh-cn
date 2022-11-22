---
title: 附加 B2C 信息
description: 本文提供有关如何在 Microsoft Dynamics 365 Commerce 中设置企业对消费者 (B2C) 租户的更多信息。
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785219"
---
# <a name="additional-b2c-information"></a>附加 B2C 信息

[!include [banner](includes/banner.md)]

本文提供有关如何在 Microsoft Dynamics 365 Commerce 中设置企业对消费者 (B2C) 租户的更多信息。

### <a name="customer-migration"></a>客户迁移

如果考虑迁移早期标识提供程序平台中的客户记录，请与 Dynamics 365 Commerce 团队合作检查您的客户迁移需求。

有关客户迁移的更多 Azure AD B2C 文档，请参阅[将用户迁移到 Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration)。

### <a name="custom-policies"></a>自定义策略

有关自定义非 B2C 标准策略提供的 Azure AD B2C 交互和策略流的更多信息，请参阅[在 Azure Active Directory B2C 中自定义策略](/azure/active-directory-b2c/active-directory-b2c-overview-custom)。 

### <a name="secondary-admin"></a>第二管理员

可以在 B2C 租户的 **用户** 部分中添加可选的第二管理员帐户。 这可以是直接帐户或一般帐户。 如果需要在团队资源之间共享某个帐户，也可以创建公共帐户。 由于 Azure AD B2C 中存储的数据为敏感数据，所以应该按照贵公司的安全实践密切监控公共帐户。

### <a name="set-up-a-custom-sign-in-domain"></a>设置自定义登录域

Azure AD B2C 允许您为 Azure AD B2C 租户设置自定义登录域。 有关说明，请参阅[为 Azure Active Directory B2C 启用自定义域](/azure/active-directory-b2c/custom-domain)。 

如果您使用自定义登录域，则必须将域输入到 Commerce 站点生成器中。

要在站点生成器中输入自定义登录域，请执行以下步骤。

1. 在站点生成器的右上角，选择站点切换器，然后选择 **管理站点**。
1. 在左侧导航窗格中，选择 **租户设置 \> 站点身份验证设置**。
1. 在 **站点身份验证配置文件** 部分中，选择 **管理**。
1. 在右侧的弹出菜单中，选择要为其输入自定义域的站点身份验证配置文件旁边的 **编辑** 按钮（铅笔符号）。
1. 在 **编辑站点身份验证配置文件** 对话框中，在 **登录自定义域** 下，输入自定义登录域（例如“login.fabrikam.com”）。

> [!WARNING]
> 当您更新Azure AD B2C 租户的自定义域时，该更改将影响所生成令牌的租户的颁发者详细信息。 然后，颁发者详细信息将包括自定义域，而不是 Azure AD B2C 提供的默认域。 Commerce Headquarters 中的其他 **颁发者** 配置（**Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数 \> 标识提供者**）将更改系统与站点用户的交互，如果用户正在对新颁发者进行身份验证，则可能会创建新的客户记录。 在实时 Azure AD B2C 环境中切换到自定义域之前，应先彻底测试任何自定义域更改。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
