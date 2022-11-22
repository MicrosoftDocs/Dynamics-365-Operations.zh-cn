---
title: 在 Commerce 站点构建器中配置 B2C 租户
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中配置企业对消费者 (B2C) 租户。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785232"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>在 Commerce 站点构建器中配置 B2C 租户

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中配置企业对消费者 (B2C) 租户。

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

仅当您为 Azure AD B2C 租户设置自定义域时，才应使用可选的 **登录自定义域** 字段。 有关使用 **登录自定义域** 字段的其他详细信息和注意事项，请参阅[其他 B2C 信息](additional-b2c-info.md)。

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

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请转到[其他 B2C 信息](additional-b2c-info.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
