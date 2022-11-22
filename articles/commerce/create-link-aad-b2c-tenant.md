---
title: 在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户
description: 本文介绍如何在 Microsoft Azure 门户中创建或链接到现有的 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785228"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Azure 门户中创建或链接到 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户。 有关详细信息，请参阅[教程：创建 Azure Active Directory B2C 租户](/azure/active-directory-b2c/tutorial-create-tenant)。

要在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户，请执行以下步骤。

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

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请转到[创建 B2C 应用程序](create-b2c-app.md)。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
