---
title: 创建用户流策略
description: 本文介绍如何在 Microsoft Azure 门户中创建用户流策略。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785229"
---
# <a name="create-user-flow-policies"></a>创建用户流策略

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Azure 门户中创建用户流策略。

用户流是 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 用于提供安全登录、安全注册、编辑配置文件和忘记密码用户体验的策略。 Dynamics 365 Commerce 使用这些流执行策略操作来与 Azure AD B2C 租户交互。 当用户与这些策略交互时，将被重定向到 Azure AD B2C 租户以执行操作。

Azure AD B2C 提供三种基本的用户流类型：
- 注册和登录
- 配置文件编辑
- 密码重置

可选择使用 Azure AD 提供的默认用户流，这将显示 Azure AD B2C 托管的页面。 也可以创建 HTML 页面以控制这些用户流体验的外观。 

若要自定义具有内置于 Dynamics 365 Commerce 的页面的用户策略页面，请参阅[设置用户登录的自定义页面](custom-pages-user-logins.md)。 有关更多信息，请参阅[定义 Azure Active Directory B2C 中的用户体验界面](/azure/active-directory-b2c/tutorial-customize-ui)。

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>创建注册和登录用户流策略

若要创建注册和登录用户流策略，请执行以下步骤。

1. 在 Azure 门户的左侧导航窗格中，选择 **用户流（策略）**。
1. 在 **Azure AD B2C – 用户流（策略）** 页面中，选择 **新建用户流**。
1. 选择 **注册和登录** 策略，然后选择 **建议** 版本。
1. 在 **名称** 下面，输入策略名称。 此名称在门户分配的前缀后显示（例如，“B2C_1_”）。
1. 在 **标识提供者** 下，在 **本地帐户** 部分选择 **电子邮件注册**。 电子邮件身份验证用于最常见的 Commerce 场景。 如果您还在使用社交标识提供程序身份验证，此时也可以选择这些选项。
1. 在 **多重身份验证** 下，选择适合贵公司的选项。 
1. 在 **用户特性和声明** 下，根据需要选择用于收集特性或返回声明的选项。 选择 **显示更多...** 获取属性和声明选项的完整列表。 Commerce 需要以下默认选项：

    | **收集特性** | **返回声明** |
    | ---------------------- | ----------------- |
    | 电子邮件地址          | 电子邮件地址   |
    | 给定名称             | 给定名称        |
    |                        | 标识提供方 |
    | 姓                | 姓           |
    |                        | 用户的对象 ID  |

1. 选择 **创建**。

下图是 Azure AD B2C 注册和登录用户流的一个示例。

![注册和登录策略设置。](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>创建配置文件编辑用户流策略

若要创建配置文件编辑用户流策略，请执行以下步骤。

1. 在 Azure 门户的左侧导航窗格中，选择 **用户流（策略）**。
1. 在 **Azure AD B2C – 用户流（策略）** 页面中，选择 **新建用户流**。
1. 选择 **配置文件编辑**，然后选择 **建议** 版本。
1. 在 **名称** 下，输入配置文件编辑用户流。 此名称在门户分配的前缀后显示（例如，“B2C_1_”）。
1. 在 **标识提供者** 下，在 **本地帐户** 部分选择 **电子邮件登录**。
1. 在 **用户属性** 下，选中以下复选框：
    
    | **收集特性** | **返回声明** |
    | ---------------------- | ----------------- |
    |                        | 电子邮件地址   |
    | 给定名称             | 给定名称        |
    |                        | 标识提供方 |
    | 姓                | 姓           |
    |                        | 用户的对象 ID  |
    
1. 选择 **创建**。

下图显示 Azure AD B2C 配置文件编辑用户流的一个示例。

![Azure AD B2C 配置文件编辑用户流示例](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>创建密码重置用户流策略

若要创建密码重置用户流策略，请执行以下步骤。

1. 在 Azure 门户的左侧导航窗格中，选择 **用户流（策略）**。
1. 在 **Azure AD B2C – 用户流（策略）** 页面中，选择 **新建用户流**。
1. 选择 **密码重置**，然后选择 **建议** 版本。
1. 在 **名称** 下，输入密码重置用户流的名称。
1. 在 **标识提供程序** 下，选择 **使用电子邮件地址重置密码**。
1. 选择 **创建**。
1. 在 **应用程序声明** 下，选中以下复选框：
    - **电子邮件地址**
    - **给定名称**
    - **姓**
    - **用户的对象 ID**
1. 选择 **创建**。

下图显示在 Azure AD B2C 密码重置用户流中何处设置 **使用邮件地址重置密码**。

![在密码重置策略中设置“使用邮件地址重置密码”](./media/B2CImage_13.png)

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请转到[添加社交标识提供程序](add-social-identity-providers.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
