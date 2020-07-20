---
title: 设置用户登录自定义页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9e78a4d6dc4189c927d9ef321f1eb5a6c120ee2
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533451"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>设置用户登录自定义页面


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中生成用于处理 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户用户的自定义登录的自定义页面。

## <a name="overview"></a>概览

若要使用在 Dynamics 365 Commerce 中创作的自定义页面来处理用户登录流，必须设置 Commerce 环境中将引用的Azure AD 策略。 可以使用 Azure AD B2C 应用程序配置“注册和登录”、“个人资料编辑”和“密码重置”Azure AD B2C 策略。 然后可以在使用 Microsoft Dynamics Lifecycle Services (LCS) 对 Commerce 环境进行预配流程期间引用 Azure AD B2C 租户和策略名称。

可以使用登录、注册、帐户个人资料编辑或密码重置模块生成自定义 Commerce 页面。 然后，应该在 Azure 门户中的 Azure AD B2C 策略配置内引用为这些自定义页面发布的页面 URL。

## <a name="set-up-b2c-policies"></a>设置 B2C 策略

设置 Azure AD B2C 租户并将其与 Commerce 环境关联之后，在 Azure 门户中转到 **Azure AD B2C** 页面，在菜单中**策略**下选择**用户流(策略)**。

![菜单中的“用户流(策略)”命令](./media/B2C_CustomPage_PoliciesMenu.png)

现在可使用“注册和登录”、“个人资料编辑”和“密码重置”用户登录流。

### <a name="configure-the-sign-up-and-sign-in-policy"></a>配置“注册和登录”策略

若要配置“注册和登录”策略，请执行以下步骤。

1. 选择**新建用户流**，然后在**建议**选项卡中选择**注册和登录**策略。
1. 输入策略的名称（如 **B2C\_1\_SignInSignUp**）。
1. 在**身份提供程序**部分中，选择要用于策略的身份提供程序。 至少必须选择**电子邮件注册**。
1. 在**收集属性**列中，选中**电子邮件地址**、**给定名称**和**姓**复选框。
1. 在**返回声明**列中，选中**电子邮件地址**、**给定名称**、**身份提供程序**、**姓**和**用户的对象 ID** 复选框。

    ![已选中属性和声明](./media/B2C_SignInSignUp_Attributes.png)

1. 选择**确定**创建策略。
1. 双击新策略名称，然后在导航窗格中选择**属性**。
1. 将**启用 JavaScript 执行页面布局(预览)** 选项设置为**开**。

    ![新策略的属性页](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> 将在 Commerce 环境中完全引用策略名称。 （引用中将包括前缀 **B2C\_1\_**。）策略在创建后不能重命名。 如果要更换 Commerce 环境的现有策略，可删除原始策略，然后生成一个同名新策略。 此外，如果已预配了环境，可以通过服务请求提交新策略名称。

生成自定义页面之后，您将回到此策略以完成设置。 现在，关闭策略以回到 Azure 门户中的**用户流(策略)** 页面。

### <a name="configure-the-profile-editing-policy"></a>配置“个人资料编辑”策略

若要配置“个人资料编辑”策略，请执行以下步骤。

1. 选择**新建用户流**，然后在**建议**选项卡中选择**个人资料编辑**策略。
1. 输入策略的名称（如 **B2C\_1\_EditProfile**）。
1. 在**身份提供程序**部分中，选择要用于策略的身份提供程序。 至少必须选择**本地帐户登录**。
1. 在**收集属性**列中，选中**电子邮件地址**和**姓**复选框。
1. 在**返回声明**列中，选中**电子邮件地址**、**给定名称**、**身份提供程序**、**姓**和**用户的对象 ID** 复选框。
1. 选择**确定**创建策略。
1. 双击新策略名称，然后在导航窗格中选择**属性**。
1. 将**启用 JavaScript 执行页面布局(预览)** 选项设置为**开**。

生成自定义页面之后，您将回到此策略以完成设置。 现在，关闭策略以回到 Azure 门户中的**用户流(策略)** 页面。

### <a name="configure-the-password-reset-policy"></a>配置“密码重置”策略

若要配置“密码重置”策略，请执行以下步骤。

1. 选择**新建用户流**，然后在**预览**选项卡中选择**密码重置 v1.1** 策略。

    ![“预览”选项卡中已选择“密码重置 v1.1”策略](./media/B2C_ForgetPassword_Menu.png)

1. 输入策略的名称（如 **B2C\_1\_ForgetPassword**）。
1. 在**身份提供程序**部分中，选择**使用电子邮件地址重置密码**。
1. 在**返回声明**列中，选中**电子邮件地址**、**给定名称**、**姓**和**用户的对象 ID** 复选框。

    ![已选择声明](./media/B2C_ForgetPassword_Attributes.png)

1. 选择**确定**创建策略。
1. 双击新策略名称，然后在导航窗格中选择**属性**。
1. 将**启用 JavaScript 执行页面布局(预览)** 选项设置为**开**。

生成自定义页面之后，您将回到此策略以完成设置。 现在，关闭策略以回到 Azure 门户中的**用户流(策略)** 页面。

## <a name="build-the-custom-pages"></a>生成自定义页面

若要声明自定义页面以处理用户登录，请执行以下步骤。

1. 在 Commerce 创作工具中，转到您的站点。
1. 生成下面的五个模板和五个页面：

    - 使用登录模块的**登录** 模板和页面。
    - 使用注册模块的**注册** 模板和页面。
    - 使用密码重置模块的**密码重置**模板和页面。
    - 使用密码重置验证模块的**密码重置验证**模板和页面。
    - 使用帐户个人资料编辑模块的**个人资料编辑**模板和页面

生成页面时，请遵守以下说明：

- 对每个页面或模块使用最适合您的业务要求的布局和样式。
- 发布 Azure AD B2C 设置中必须使用的所有页面和 URL。
- 发布页面和 URL 之后，收集必须用于 Azure AD B2C 策略配置的 URL。 将在使用每个 URL 时向其添加 **?preloadscripts=true** 后缀。

> [!IMPORTANT]
> 请勿使用具有相对链接的通用页眉和页脚。 因为这些页面在使用时托管在 Azure AD B2C 域中，所以仅应对所有链接使用绝对 URL。

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>为 Azure AD B2C 策略配置自定义页面信息 

在 Azure 门户中，回到 **Azure AD B2C** 页面，然后在菜单中**策略**下，选择**用户流(策略)**。

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>使用自定义页面信息更新“注册和登录”策略

若要使用自定义页面信息更新“注册和登录”策略，请执行以下步骤。

1. 在前面配置的**登录和注册**策略中导航窗格内，选择**页面布局**。
1. 选择**统一注册或登录页面**布局。
1. 将**使用自定义页面内容**选项设置为**是**。
1. 在**自定义页面 URI** 字段中，输入完整的登录 URL。 包括后缀 **?preloadscripts=true**。 例如，输入 ``www.<my domain>.com/sign-in?preloadscripts=true``。
1. 在**页面布局版本(预览)** 字段中，选择 **1.2.0**。
1. 选择**本地帐户注册页面**布局。
1. 将**使用自定义页面内容**选项设置为**是**。
1. 在**自定义页面 URI** 字段中，输入完整的注册 URL。 包括后缀 **?preloadscripts=true**。 例如，输入 ``www.<my domain>.com/sign-up?preloadscripts=true``。
1. 在**页面布局版本(预览)** 字段中，选择 **1.2.0**。
1. 在**用户属性**部分中，执行以下步骤：

    1. 在**需要验证**字段中对**电子邮件地址**、**给定名称**和**姓**属性选择**否**。
    1. 在**可选**字段中对**给定名称**和**姓**属性选择**否**。

    ![“本地帐户注册页面”策略的配置](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>使用自定义页面信息更新“个人资料编辑”策略

若要使用自定义页面信息更新“个人资料编辑”策略，请执行以下步骤。

1. 在前面配置的**个人资料编辑**策略中导航窗格内，选择**页面布局**。
1. 选择**个人资料编辑页面**布局。
1. 将**使用自定义页面内容**选项设置为**是**。
1. 在**自定义页面 URI** 字段中，输入完整的个人资料编辑 URL。 包括后缀 **?preloadscripts=true**。 例如，输入 ``www.<my domain>.com/profile-edit?preloadscripts=true``。
1. 在**页面布局版本(预览)** 字段中，选择 **1.2.0**。
1. 在**用户属性**部分中，执行以下步骤：

    1. 在**需要验证**字段中对**电子邮件地址**和**给定名称**属性选择**否**。
    1. 在**可选**字段中对**给定名称**和**姓**属性选择**否**。

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>使用自定义页面信息更新“密码重置”策略

若要使用自定义页面信息更新“密码重置”策略，请执行以下步骤。

1. 在前面配置的**密码重置**策略中导航窗格内，选择**页面布局**。
1. 选择**新建密码页面**布局。
1. 将**使用自定义页面内容**选项设置为**是**。
1. 在**自定义页面 URI** 字段中，输入完整的密码重置 URL。 包括后缀 **?preloadscripts=true**。 例如，输入 ``www.<my domain>.com/passwordreset?preloadscripts=true``。
1. 在**页面布局版本(预览)** 字段中，选择 **1.2.0**。
1. 选择**帐户验证页面**布局。
1. 将**使用自定义页面内容**选项设置为**是**。
1. 在**自定义页面 URI** 字段中，输入完整的密码重置验证 URL。 包括后缀 **?preloadscripts=true**。 例如，输入 ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``。
1. 在**页面布局版本(预览)** 字段中，选择 **1.2.0**。



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>自定义标签和描述的默认文本字符串

在入门套件中，已经为登录模块预填充了标签和描述的默认文本字符串。 可通过更新登录模块的 global.json 文件来自定义软件开发工具包 (SDK) 中的这些字符串。

例如，遗忘密码链接的默认文本为**忘记密码了?**。 下面显示登录页面中的默认文本。

![登录页面中忘记密码了链接的默认文本](./media/B2C_SignUp_ModuleFace.png)

但是，在入门套件登录模块的 global.json 文件中，可将文本编辑为**忘记了密码?**，如下图中所示。

![登录模块的 global.json 文件中更新后的链接文本](./media/B2C_CustomizingStringsForModule.png)

更新 global.json 文件并发布更改之后，将在 Commerce 中和活动的登录页面内登录模块中显示新链接文本。

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务站点](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将在线站点与渠道关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)
