---
title: 创建 B2C 应用程序
description: 本文介绍如何在 Microsoft Azure 门户中创建企业对消费者 (B2C) 应用程序。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785225"
---
# <a name="create-a-b2c-application"></a>创建 B2C 应用程序

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Azure 门户中创建企业对消费者 (B2C) 应用程序。

创建 B2C 租户之后，您将在新的 Azure Active Directory (Azure AD) 租户中创建 B2C 应用程序以与 Commerce 交互。

若要创建 B2C 应用程序，请执行以下步骤。

1. 在 Azure 门户中，选择 **应用注册**，然后选择 **新注册**。
1. 在 **名称** 下方，输入此 Azure AD B2C 应用程序的名称。
1. 在 **受支持的帐户类型** 下方，选择 **任何标识提供者或组织目录中的帐户(用于使用用户流对用户进行身份验证)**。
1. 对于 **重定向 URI**，输入您的专用回复 URL 作为类型 **Web**。 有关回复 URL 的信息以及如何进行格式化，请参阅下面的[回复 URL](#reply-urls)。 当用户进行身份验证时，必须输入重定向 URI/回复 URL 以启用从 Azure AD B2C 重定向回您的站点。 回复 URL 可以在注册过程中添加，也可以以后通过从 B2C 应用程序的 **概览** 部分的 **概览** 菜单中选择 **添加重定向 URI** 链接来添加。
1. 对于 **权限**，选择 **授予对 OpenID 和脱机访问权限的管理员同意**。
1. 选择 **注册**。
1. 选择新创建的应用程序，然后导航到 **身份验证** 菜单。 
1. 如果输入回复 URL，在 **隐式授权和混合流** 下同时选择 **访问令牌** 和 **ID 令牌** 选项，以为应用程序启用它们，然后选择 **保存**。 如果注册时没有输入回复 URL，也可以在此页面添加，方法是选择 **添加平台**，选择 **Web**，然后输入应用程序的重定向 URI。 然后，**隐式授权和混合流** 部分将可用于选择 **访问令牌** 和 **ID 令牌** 选项。
1. 转到 Azure 门户的 **概述** 菜单，然后复制 **应用程序(客户端) ID**。 记下此 ID 以用于以后的设置步骤（以后称为 **客户端 GUID**）。

有关 Azure AD B2C 中应用注册的其他参考，请参阅 [Azure Active Directory B2C 的新应用注册体验](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>回复 URL

回复 URL 非常重要，因为当您的站点调用 Azure AD B2C 以对用户进行身份验证时，它们会提供返回域的允许列表。 这将允许把已通过身份验证的用户返回到其用于登录的域（您的站点域）。 

在 **Azure AD B2c - 应用程序 \> 新应用程序** 屏幕的 **回复 URL** 框中，需要为您的站点域（预配环境之后）和 Commerce 生成的 URL 分别添加单独的行。 这些 URL 必须始终使用有效的 URL 格式，并且只能是基 URL（结尾没有斜杠或路径）。 然后，需要将字符串 ``/_msdyn365/authresp`` 附加到基 URL，如下面的示例中所示。

- ``https://www.fabrikam.com/_msdyn365/authresp``（该域应该与电子商务域完全匹配。 如果有多个域，则需要为每个域添加此 URL。）
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请转到[创建用户流策略](create-user-flow-policies.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
