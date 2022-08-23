---
title: 在 Commerce 中设置 B2C 租户
description: 本文介绍如何在 Dynamics 365 Commerce 中设置 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以执行用户站点身份验证。
author: BrianShook
ms.date: 05/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 0b41d61c388e3723e3c30fa4dc0ae0055ffb1842
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271842"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>在 Commerce 中设置 B2C 租户

[!include [banner](includes/banner.md)]

本文介绍如何在 Dynamics 365 Commerce 中设置 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以执行用户站点身份验证。

Dynamics 365 Commerce 使用 Azure AD B2C 为用户凭据和身份验证流提供支持。 用户可以通过这些流注册、登录和重置密码。 Azure AD B2C 中存储敏感的用户身份验证信息，如用户名和密码。 B2C 租户中的用户记录中将存储 B2C 本地帐户记录或 B2C 社交标识提供程序记录。 这些 B2C 记录将链接回 Commerce 环境中的客户记录。

> [!WARNING] 
> Azure AD B2C 将于 2021 年 8 月 1 日停用旧（旧版）用户流。 因此，您应该计划将用户流迁移到新的推荐版本。 新版本提供功能奇偶一致性和新功能。 Commerce 版本 10.0.15 或更高版本的模块库应与推荐的 B2C 用户流一起使用。 有关详细信息，请参阅 [Azure Active Directory B2C 中的用户流](/azure/active-directory-b2c/user-flow-overview)。
 
 > [!NOTE]
 > Commerce 评估环境随预先加载的 Azure AD B2C 租户一起提供，以用于演示目的。 评估环境不需要使用下面的步骤加载自己的 Azure AD B2C 租户。

> [!TIP]
> 您可以通过 Azure AD 标识保护和条件访问进一步保护站点用户并增强 Azure AD B2C 租户的安全性。 若要查看 Azure AD B2C Premium P1 和 Premium P2 租户可用的功能，请参阅 [Azure AD B2C 的标识保护和条件访问](/azure/active-directory-b2c/conditional-access-identity-protection-overview)。

## <a name="dynamics-environment-prerequisites"></a>Dynamics 环境先决条件

首先，通过满足以下先决条件确保已正确配置了您的 Dynamics 365 Commerce 环境和电子商务渠道。

- 在 Commerce Headquarters 中将 POS 操作 **AllowAnonymousAccess** 值设置为“1”：
    1. 转到 **POS 操作**。
    1. 在操作网格中，双击并选择 **个性化**。
    1. 选择 **添加字段**。
    1. 在可用列列表中，选择 **AllowAnonymousAccess** 列以添加该列。
    1. 选择 **更新**。
    1. 对于 **612** “客户添加”操作，将 **AllowAnonymousAccess** 更改为“1”。
    1. 运行 **1090 (收银机)** 作业。
- 在 Commerce Headquarters 中，将客户帐户编号规则 **手动** 设置为 **否**：
    1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 应收帐款参数**。
    1. 选择 **编号规则**。
    1. 在 **客户帐户** 行中，双击 **编号规则代码** 值。
    1. 在编号规则的 **常规** 快速选项卡上，将 **手动** 设置为 **否**。

还建议您在部署 Dynamics 365 Commerce 环境之后，在该环境中[初始化种子数据](enable-configure-retail-functionality.md)。

## <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户

本节介绍创建或链接 Azure AD B2C 租户以在您的 Commerce 站点中使用。 有关详细信息，请参阅[教程：创建 Azure Active Directory B2C 租户](/azure/active-directory-b2c/tutorial-create-tenant)。

1. 登录 [Azure 门户](https://portal.azure.com/)。
1. 在 Azure 门户菜单中选择 **创建资源**。 请务必使用将与您的 Commerce 环境连接的订阅和目录。

    ![在 Azure 门户中创建资源。](./media/B2CImage_1.png)

1. 转到 **标识 \> Azure Active Directory B2C**。
1. 进入 **创建新的 B2C 租户或链接至现有租户** 页之后，使用下面一个最适合贵公司需要的选项：

    - **创建新的 Azure AD B2C 租户**：此选项用于创建新的 Azure AD B2C 租户。
        1. 选择 **创建新的 Azure AD B2C 租户**。
        1. 在 **组织名称** 下，输入组织名称。
        1. 在 **初始域名** 下，输入初始域名。
        1. 对于 **国家或地区**，选择国家或地区。
        1. 选择 **创建** 创建租户。

     ![创建新的 Azure AD 租户。](./media/B2CImage_2.png)

     - **将现有 Azure AD B2C 租户链接至我的 Azure 订阅**：如果您已经有需要链接至的 Azure AD B2C 租户，请使用此选项。
        1. 选择 **将现有 Azure AD B2C 租户链接至我的 Azure 订阅**。
        1. 对于 **Azure AD B2C 租户**，选择相应 B2C 租户。 如果选择框中显示消息“未发现符合要求的 B2C 租户”，说明您还没有符合要求的 B2C 租户，需要新建一个。
        1. 对于 **资源组**，选择 **新建**。 输入将包含该租户的资源组的 **名称**，选择 **资源组位置**，然后选择 **创建**。

    ![将现有 Azure AD B2C 租户链接到 Azure 订阅。](./media/B2CImage_3.png)

1. 创建新的 Azure AD B2C 目录（可能需要一些时间）之后，仪表板中将显示这个新目录的链接。 这个链接将把您带到“欢迎使用 Azure Active Directory B2C”页面。

    ![链接到新的 Azure AD 目录](./media/B2CImage_4.png)

> [!NOTE]
> 如果您在您的 Azure 帐户中有多个订阅，或者如果您已经设置了 B2C 租户但未链接到有效订阅，**疑难解答** 横幅将引导您把该租户链接到订阅。 选择疑难解答消息，然后按照指示解决订阅问题。

下图显示一个 Azure AD B2C **疑难解答** 横幅示例。

![显示目录无有效订阅的警告。](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>创建 B2C 应用程序

创建 B2C 租户之后，您将在新的 Azure AD B2C 租户中创建 B2C 应用程序以与 Commerce 交互。

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

## <a name="create-user-flow-policies"></a>创建用户流策略

用户流是 Azure AD B2C 用于提供安全登录，安全注册，编辑配置文件和忘记密码用户体验的策略。 Dynamics 365 Commerce 使用这些流执行策略操作来与 Azure AD B2C 租户交互。 当用户与这些策略交互时，将被重定向到 Azure AD B2C 租户以执行操作。

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
1. 在 **标识提供者** 下，在 **本地帐户** 部分选择 **电子邮件注册**。 电子邮件身份验证用于最常见的 Commerce 场景。 如果您还在使用社交标识提供者身份验证，此时也可以选择以下选项。
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

## <a name="add-social-identity-providers-optional"></a>添加社交标识提供程序（可选）

社交标识提供程序让用户可以使用自己的社交帐户进行身份验证。 添加社交标识提供程序身份验证在 Dynamics 365 Commerce 中为可选操作。 

如果不添加社交标识提供程序身份验证，默认 Azure AD B2C 配置文件将充当您的用户群的主配置文件。 用户将选择自己的用户名（其首选电子邮件地址）并设置密码。 Azure AD B2C 将直接对用户进行身份验证。 

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
1. 若要附加登录/注册用户流策略，请选择您已经为帐户设置的每个标识提供程序。 若要对其进行测试，请为每个标识提供程序选择 **运行用户流**。 一个新选项卡将显示登录页，其中显示新标识提供程序选择框。

下图显示 Azure AD B2C 中 **添加标识提供程序** 和 **设置社交标识提供程序** 屏幕的示例。

![向应用程序添加社交标识提供者。](./media/B2CImage_14.png)

下图显示如何在 Azure AD B2C **标识提供程序** 页中选择标识提供程序的示例。

![选择要为策略启用的每个社交标识提供者。](./media/B2CImage_16.png)

下图显示默认登录屏幕的示例，该屏幕中显示了一个社交标识提供程序登录按钮。

> [!NOTE]
> 如果为用户流选择内置于 Commerce 的自定义页面，将需要使用 Commerce 模块库的可扩展性功能添加社交标识提供者的按钮。 此外，在使用特定的社交标识提供者设置应用程序时，在某些情况下，URL 或配置字符串可能区分大小写。 有关详细信息，请参考您的社交标识提供者的连接说明。
 
![显示社交标识提供者登录按钮的示例默认登录屏幕。](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>使用新的 Azure AD B2C 信息更新 Commerce Headquarters

完成了上面的 Azure AD B2C 预配步骤之后，必须在 Dynamics 365 Commerce 环境中注册 Azure AD B2C 应用程序。

若要使用新的 Azure AD B2C 信息更新 Headquarters，请执行以下步骤。

1. 在 Commerce 中，转到 **Commerce 共享参数**，然后选择左菜单中的 **标识提供程序**。
1. 在 **标识提供程序** 下，执行以下操作：
    1. 在 **颁发者** 框中，输入标识提供程序颁发者字符串。 要查找您的颁发者字符串，请参阅下面的[获取总部设置的颁发者字符串](#obtain-issuer-string-for-headquarters-setup)。
    1. 在 **名称** 框中，输入颁发者记录的名称。
    1. 在 **类型** 框中，输入 **Azure AD B2C (id_token)**。
1. 选择上面的 B2C 标识提供程序项之后，在 **回复方** 下执行以下操作：
    1. 在 **客户端 ID** 框中，输入您的 B2C 应用程序 ID。 可在您的 B2C 应用程序的属性页 **应用程序 ID** 框中找到此信息。
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

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>在 Commerce 站点构建器中配置 B2C 租户

Azure AD B2C 租户设置完毕之后，必须在 Commerce 站点构建器中配置该 B2C 租户。 配置步骤包括从 Azure 门户收集 B2C 应用程序信息，在站点构建器中输入 B2C 应用程序信息，然后将该 B2C 应用程序与您的站点和渠道关联。

### <a name="collect-the-required-application-information"></a>收集所需的应用程序信息

若要收集所需的应用程序信息，请执行以下步骤。

1. 在 Azure 门户中，转到 **主页\> Azure AD B2C - 应用注册**。
1. 选择您的应用程序，然后在左侧导航窗格中选择 **概览** 获取应用程序详细信息。
1. 从 **应用程序（客户端）ID** 引用中，收集在您的 B2C 租户中创建的 B2C 应用程序的应用程序 ID。 稍后将在站点构建器中把此信息作为 **客户端 GUID** 输入。
1. 选择 **重定向 URI**，收集为您的站点显示的回复 URL（在设置时输入的回复 URL）。
1. 转到 **主页 \> Azure AD B2C – 用户流**，然后收集每个用户流策略的完整名称。

下图显示 **Azure AD B2C - 应用注册** 概览页的示例。

![突出显示应用程序（客户端）ID的 Azure AD B2C - 应用注册概览页](./media/ClientGUID_Application_AzurePortal.png)

下图显示 **Azure AD B2C – 用户流（策略）** 页中用户流策略的一个示例。

![收集每个 B2C 策略流的名称。](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>在 Commerce 中输入您的 Azure AD B2C 租户应用程序信息

必须在 Commerce 站点构建器中输入 Azure AD B2C 租户的详细信息，才能将 B2C 租户与站点关联。

要将您的 Azure AD B2C 租户应用程序信息添加到 Commerce 中，请执行以下步骤。

1. 以管理员身份登录您的环境的 Commerce 站点构建器。
1. 在左侧导航窗格中，选择 **租户设置** 将其展开。
1. 在 **租户设置** 下，选择 **站点身份验证设置**。 
1. 在 **站点身份验证配置文件** 旁边的主窗口中，选择 **管理**。 （如果站点身份验证配置文件列表中显示您的租户，说明已经有管理员添加了此租户。 请验证下面步骤 6 中的项是否与您的预期 B2C 设置中的项相匹配。 还可以使用类似的 Azure AD B2C 租户或应用程序创建新配置文件，以说明细微差异，例如不同的用户策略 ID）。
1. 选择 **添加站点身份验证配置文件**。
1. 使用您的 B2c 租户和应用程序中的值在显示的窗体中输入下面的必需项。 可以将非必填字段（不带星号的字段）保留为空。

    - **应用程序名称**：您的 B2C 应用程序的名称，例如，“Fabrikam B2C”。
    - **租户名称**：您的 B2C 租户的名称（例如，如果 B2C 租户的域显示为“fabrikam.onmicrosoft.com”，则使用“fabrikam”）。 
    - **忘记密码策略 ID**：忘记密码用户流策略 ID，例如“B2C_1_PasswordReset”。
    - **注册登录策略 ID**：注册和登录用户流策略 ID，例如“B2C_1_signup_signin”。
    - **客户端 GUID**：B2C 应用程序 ID，例如“22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”。
    - **编辑配置文件策略 ID**：概要文件编辑用户流策略 ID，例如“B2C_1A_ProfileEdit”。

1. 选择 **确定**。 现在应该可以在列表中看到显示您的 B2C 应用程序的名称。
1. 选择 **保存** 以保存您的更改。

仅当您为 Azure AD B2C 租户设置自定义域时，才应使用可选的 **登录自定义域** 字段。 有关使用 **登录自定义域** 字段的其他详细信息和注意事项，请参阅下面的[其他 B2C 信息](#additional-b2c-information)。

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>将 B2C 应用程序关联到站点和渠道

> [!WARNING]
> - 如果您的站点已经与一个 B2C 应用程序关联，则切换到其他 B2C 应用程序将去除为已经登录该环境的用户建立的当前引用。 如果更改，与当前分配的 B2C 应用程序关联的所有凭据对用户均不可用。 
> - 仅当首次设置渠道的 B2C 应用程序时，或计划让用户使用此渠道的新凭据重新注册新 B2C 应用程序时，才更新此 B2C 应用程序。 将渠道关联到 B2C 应用程序时请小心谨慎，并为应用程序指定明确的名称。 如果不在下面的步骤中将渠道关联到 B2C 应用程序，将把登录您的站点的该渠道的用户输入到 B2C 应用程序中，并显示为 B2C 应用程序的 **租户设置 \> B2C 设置** 列表中的 **默认值**。

若要将 B2C 应用程序关联到站点和渠道，请执行以下步骤。

1. 在 Commerce 网站构建器中导航到您的网站。
1. 在左侧导航窗格中，选择 **站点设置** 将其展开。
1. 在 **站点设置** 下，选择 **渠道**。
1. 在主窗口中的 **渠道** 下，选择您的渠道。
1. 在右侧渠道属性窗格中，从 **选择 B2C 应用程序** 下拉菜单中选择您的 B2C 应用程序名称。
1. 选择 **关闭**，然后选择 **保存并发布**。

## <a name="additional-b2c-information"></a>附加 B2C 信息

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

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
