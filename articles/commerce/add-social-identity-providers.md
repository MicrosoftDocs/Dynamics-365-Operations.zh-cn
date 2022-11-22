---
title: 添加社交标识提供程序
description: 本文介绍如何在 Microsoft Azure 门户中添加社交标识提供程序。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785224"
---
# <a name="add-social-identity-providers"></a>添加社交标识提供程序

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Azure 门户中添加社交标识提供程序。

社交标识提供程序让用户可以使用自己的社交帐户进行身份验证。 添加社交标识提供程序身份验证在 Dynamics 365 Commerce 中为可选操作。 

如果不添加社交标识提供程序身份验证，默认 Azure Active Directory (Azure AD) B2C 配置文件将充当您的用户群的主配置文件。 用户将选择自己的用户名（其首选电子邮件地址）并设置密码。 Azure AD B2C 将直接对用户进行身份验证。 

如果已添加了社交标识提供程序身份验证，并且用户选择了提供的一个社交标识提供程序，将在 Azure AD B2C 租户中创建一个条目。 然后，Azure AD B2C 将使用该社交标识提供程序对用户的凭据进行身份验证。

> [!NOTE]
> 标识提供程序登录将在 B2C 租户中创建一个记录，但是其格式与本地帐户的格式不同，因为其将调用外部社交标识提供程序引用来进行身份验证。 用户可以在多个社交标识提供程序中使用同一个电子邮件地址，这意味着用于身份验证的电子邮件用户名可能对租户不是唯一的。 Azure AD B2C 将仅强制在本地 B2C 帐户中具有唯一电子邮件地址的用户进行身份验证。

必须先转到标识提供程序的门户并按照 Azure AD B2C 文档中的指示设置标识提供程序应用程序，才能添加用于身份验证的社交标识提供程序。 下面提供了文档的链接列表。

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD（单个租户）](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft 帐户](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID 连接](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>添加和设置社交标识提供程序

> [!NOTE]
> 在 Microsoft Dynamics 365 Commerce 中设置企业对消费者 (B2C) 租户时，添加社交标识提供程序是可选步骤。

若要添加和设置社交标识提供程序，请执行以下步骤。  

1. 在 Azure 门户中，导航到 **标识提供程序**。
1. 选择 **添加**。 将显示 **添加标识提供程序** 屏幕。
1. 在 **名称** 下，输入要在登录屏幕中对用户显示的名称。
1. 在 **标识提供程序类型** 下，从列表中选择标识提供程序。
1. 选择 **确定**。
1. 选择 **设置此标识提供程序** 以访问 **设置社交标识提供程序** 屏幕。
1. 在 **客户端 ID** 下，输入从标识提供程序应用程序设置中获取的客户端 ID。
1. 在 **客户端密钥** 下，输入从标识提供程序应用程序设置中获取的客户端密钥。
1. 附加登录/注册策略的用户流：
1. 转到 **Azure AD B2C – 用户流（策略）\> {您的登录注册策略} \> 标识提供程序**。
1. 若要附加登录/注册用户流策略，请选择您已经为帐户设置的每个标识提供程序。 要对这些流进行测试，为每个标识提供程序选择 **运行用户流**。 一个新选项卡将显示登录页，其中显示新标识提供程序选择框。

下图显示 Azure AD B2C 中 **添加标识提供程序** 和 **设置社交标识提供程序** 屏幕的示例。

![向应用程序添加社交标识提供者。](./media/B2CImage_14.png)

下图显示如何在 Azure AD B2C **标识提供程序** 页中选择标识提供程序的示例。

![选择要为策略启用的每个社交标识提供者。](./media/B2CImage_16.png)

下图显示默认登录屏幕的示例，该屏幕中显示了一个社交标识提供程序登录按钮。

> [!NOTE]
> 如果为用户流选择内置于 Commerce 的自定义页面，将需要使用 Commerce 模块库的可扩展性功能添加社交标识提供者的按钮。 此外，在使用特定的社交标识提供者设置应用程序时，在某些情况下，URL 或配置字符串可能区分大小写。 有关详细信息，请参考您的社交标识提供者的连接说明。
 
![显示社交标识提供者登录按钮的示例默认登录屏幕。](./media/B2CImage_17.png)

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请继续[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
