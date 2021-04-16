---
title: 在 Commerce 环境中配置多个 B2C 租户
description: 本主题介绍何时和如何在专用的 Dynamics 365 Commerce 环境中设置多个按渠道 Microsoft Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以进行用户身份验证。
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4e50855368a3fa86c38c756492fc7e6cd518f497
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796091"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>在 Commerce 环境中配置多个 B2C 租户

[!include [banner](includes/banner.md)]

本主题介绍何时和如何在专用的 Dynamics 365 Commerce 环境中按渠道设置多个 Microsoft Azure Active Directory (Azure AD) 企业对消费者 (B2C) 租户以进行用户身份验证。

Dynamics 365 Commerce 使用 Azure AD B2C 云标识服务为用户凭据和身份验证流提供支持。 用户可以使用身份验证流注册，登录和重置密码。 Azure AD B2C 中存储用户的敏感身份验证信息，如用户名和密码。 用户记录对每个 B2C 租户都是唯一的，其使用用户名（电子邮件地址）凭据或社交标识提供程序凭据。

大多数情况下，一个 Commerce 环境中仅使用一个 Azure AD B2C 租户。 然后，Commerce 客户可以在同一个 Commerce 环境中创建和发布多个站点，而这些站点中将使用相同的客户凭据。 但是，如果应该将环境中的站点视为不同品牌，并作为不同企业向用户显示，则可以为渠道配置 B2C 租户来区分站点/品牌。

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>按渠道设置多个 B2C 租户时的注意事项

将每个渠道或站点视为一个单独的企业时，Commerce 中与用户身份验证流有关的最佳选项通常是使用单独的法人。 但是，如果要让每个渠道/站点保留在同一个环境和法人中，但是不希望为每个站点使用单独的用户身份验证，请务必在继续操作之前注意以下事项：

- 用户自己有每个渠道/站点的不同凭据。

    同一人可以有每个渠道/站点的两个不同帐户，因为每个帐户在一个单独的 B2C 租户中是一个唯一条目。

- 在 Microsoft Dynamics 环境中，将为全局记录搜索返回单独的客户记录。

    如果用户在多个渠道/站点中使用同一个电子邮件地址，全局客户搜索将返回每个渠道/站点的结果。 （将显示渠道指示器。）

- 可使用通讯簿帮助为用户分组，以便按渠道跟踪这些用户。
- 每个渠道的客户记录数可能会增加，并且这种增加可能会影响全局客户搜索的性能。
- 必须将 B2C 租户仔细地映射到渠道，以便帮助避免客户注册错误的租户。 否则，可能会发生混淆或跟踪问题。

下图显示一个 Commerce 环境中的多个 B2C 租户。

![一个 Commerce 环境中的多个 B2C 租户](media/MultiB2C_In_Environment.png)

如果认定您的企业在同一个 Commerce 环境中每个渠道需要不同 B2C 租户，请完成以下部分中的过程请求此功能。

## <a name="configure-b2c-tenants-in-your-environment"></a>在环境中配置 B2C 租户

若要在环境中配置 B2C 租户，请完成此部分中的相关过程。

### <a name="add-an-azure-ad-b2c-tenant"></a>添加 Azure AD B2C 租户

若要向环境添加 Azure AD B2C 租户，请完成以下步骤。

1. 以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。
1. 在左侧导航窗格中，选择 **租户设置** 将其展开。
1. 选择 **B2C 设置**，然后选择 **管理**。
1. 选择 **添加 B2C 应用程序**，然后输入以下信息：

    - **应用程序名称**：输入应该在 Commerce 中的应用程序管理上下文内用于应用程序的名称。 建议使用您在 Azure 门户中设置 Azure AD B2C 应用程序时选择的应用程序名称。 这样就可以在 Commerce 中管理 B2C 租户时帮助降低混淆程度。
    - **租户名称**：输入要在 Azure 门户中显示的 B2C 租户名称。
    - **忘记密码策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。
    - **注册登录策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。
    - **客户端 GUID**：输入在 Azure 门户中显示的 Azure AD B2C 租户 ID（而不是 B2C 租户的应用程序 ID）。
    - **编辑配置文件策略 ID**：输入策略 ID（策略在 Azure 门户中的名称）。

1. 输入完此信息之后，选择 **确定** 保存更改。 现在 **管理 B2C 应用程序** 下的列表中应该会显示您的新 Azure AD B2C 租户。

> [!NOTE]
> 除非 Dynamics 365 Commerce 团队指示您设置 **范围**、**非交互式策略 ID**、**非交互式客户端 ID**、**登录自定义域** 和 **注册策略 ID** 等字段，否则请将这些字段保留为空。


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>管理或删除 Azure AD B2C 租户

1. 以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。
1. 在左侧导航窗格中，选择 **租户设置** 将其展开。
1. 选择 **B2C 设置**，然后选择 **管理**。
1. 若要编辑 B2C 租户，请选择其旁边的铅笔符号。 若要删除 B2C 租户，请选择其旁边的废纸篓符号。
1. 选择 **保存**，然后选择 **发布** 激活您的更改。

> [!WARNING]
> 为有效/已发布站点配置了 B2C 租户之后，用户可能已通过使用租户中的帐户进行了注册。 如果在 **租户设置 \> B2C 租户** 菜单中删除配置的租户，将解除该 B2C 租户和与该租户的任何渠道关联的站点之间的关联。 在此情况下，您的用户可能再也不能登录自己的帐户。 因此，删除配置的租户时，请务必小心谨慎。
>
> 如果删除配置的租户，将继续保留 B2C 租户和记录，但是将更改或删除该租户的 Commerce 系统配置。 尝试注册或登录站点的用户将在为该站点的渠道配置的默认的或新关联的 B2C 租户中创建一个新的帐户记录。

## <a name="configure-your-channel-with-a-b2c-tenant"></a>为渠道配置 B2C 租户

1. 以系统管理员身份登录环境的 Commerce 站点构建器。只有 Commerce 环境的系统管理员才能配置 Azure AD B2C 租户。
1. 在左侧导航窗格中，选择 **站点设置** 将其展开。
1. 选择 **渠道**，然后选择要配置的渠道。
1. 在右侧的属性窗格中 **选择 B2C 应用程序** 字段内，选择为用于此渠道而配置的 Azure AD B2C 租户。
1. 在命令栏中，选择 **保存并发布** 提交新的或更新后的配置。

> [!WARNING]
> 如果更改分配给渠道的 B2C 应用程序，将删除已经为在环境中已注册的任何用户建立的当前首选项。 在此情况下，与当前分配的 B2C 应用程序关联的所有凭据对用户均不可用。 因此，仅当您首次设置渠道，并且任何用户均不可注册时，才更改渠道的 Azure AD B2C 配置。 否则，用户可能必须再次注册，才能在新的 Azure AD B2C 租户中建立记录。
## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[部署新的电子商务租户](deploy-ecommerce-site.md)

[创建电子商务站点](create-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
