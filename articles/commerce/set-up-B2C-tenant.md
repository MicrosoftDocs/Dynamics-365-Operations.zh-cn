---
title: 在 Commerce 中设置 B2C 租户
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中设置 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以执行用户站点身份验证。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785119"
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

## <a name="next-steps"></a>后续步骤

要继续在 Commerce 中设置 B2C 租户的过程，请继续[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)。

## <a name="additional-resources"></a>其他资源

[在 Azure 门户中创建或链接到现有的 Azure AD B2C 租户](create-link-aad-b2c-tenant.md)

[创建 B2C 应用程序](create-b2c-app.md)

[创建用户流策略](create-user-flow-policies.md)

[添加社交标识提供程序（可选）](add-social-identity-providers.md)

[使用新的 Azure AD B2C 信息更新 Commerce Headquarters](update-hq-aad-b2c-info.md)

[在 Commerce 站点构建器中配置 B2C 租户](config-b2c-tenant-site-builder.md)

[附加 B2C 信息](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
