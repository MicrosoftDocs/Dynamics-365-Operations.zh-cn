---
title: 启用 Dynamics 365 Commerce 和 Microsoft Teams 集成
description: 本主题介绍如何启用 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成。
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695726"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>启用 Dynamics 365 Commerce 和 Microsoft Teams 集成

[!include [banner](includes/banner.md)]

本主题介绍如何启用 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成。

若要为 Teams 预配 Dynamics 365 Commerce 中的信息并在 Teams 和销售点 (POS) 应用程序之间同步任务管理功能，您必须在 Commerce Headquarters 中启用集成功能。

> [!NOTE]
> 启用 Teams 集成，即表示您同意与 Teams 共享数据。 与 Teams 共享的数据可能与您的 Commerce 数据位于不同的国家/地区，并且可能受不同的合规性标准约束。 有关详细信息，请参阅 [Microsoft 信任中心](https://www.microsoft.com/trust-center)。 有关 Microsoft 隐私策略的信息，请参阅 [Microsoft 隐私声明](https://aka.ms/privacy)。

## <a name="enable-teams-integration"></a>启用 Teams 集成

必须先在 Azure 门户中使用您的租户注册 Teams 应用程序，然后才能启用 Microsoft Teams 与 Commerce 的集成。

若要在 Azure 门户中使用您的租户注册 Teams 应用程序，请按照下列步骤操作。

1. 按照[快速入门：在 Microsoft 身份平台中注册应用](/azure/active-directory/develop/quickstart-register-app)中的步骤操作，以在 Azure 门户中使用您的租户注册 Teams 应用程序。
1. 在 **应用注册** 选项卡上，选择您在上一步中创建的应用。 然后，在 **身份验证** 选项卡上，选择 **添加平台**。
1. 在对话框中，选择 **Web**。 然后，在 **重定向 URL** 字段中，输入格式为 **\<HQUrl\>/oauth** 的 URL。 将 **\<HQUrl\>** 替换为您的 Commerce headquarters URL（例如，`https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`）。
1. 在已注册应用的 **概览** 页面上，复制 **应用程序（客户端）ID** 值。 在下一节中，您必须提供此值来在 Commerce headquarters 中启用 Teams 集成。
1. 按照[添加客户端密码](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)中的说明添加客户端密码。 然后复制客户端的 **密码值**。 在下一节中，您必须提供此值来在 Commerce headquarters 中启用 Teams 集成。
1. 选择 **API 权限**，然后选择 **添加权限**。
1. 在 **请求 API 权限** 对话框中，选择 **Microsoft Graph**，选择 **委托的权限**，展开 **组**，选择 **Group.ReadWrite.All**，然后选择 **添加权限**。
1. 在 **请求 API 权限** 对话框中，选择 **添加权限**，选择 **Microsoft Graph**，选择 **应用程序权限**，展开 **组**，选择 **Group.ReadWrite.All**，然后选择 **添加权限**。
1. 在 **请求 API 权限** 对话框中，选择 **添加权限**。 在 **我的组织使用的 API** 选项卡上，搜索 **Microsoft Teams 零售服务**，选择此服务。
1. 选择 **委托的权限**，展开 **TaskPublishing**，选择 **TaskPublising.ReadWrite.All**，然后选择 **添加权限**。 有关详细信息，请参阅[配置客户端应用程序以访问 Web API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)。

若要在 Commerce Headquarters 中启用 Teams 集成，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。
1. 在操作窗格上，选择 **编辑**。
1. 将 **启用 Microsoft Teams 集成** 选项设置为 **是**。
1. 在 **应用程序 ID** 字段中，输入您在 Azure 门户中注册 Teams 应用程序时获得的 **应用程序（客户端）ID** 值。
1. 在 **应用程序密钥** 字段中，输入您在 Azure 门户中添加客户端密码时获得的 **密码值**。
1. 在操作窗格上，选择 **保存**。

下图显示在 Commerce Headquarters 中配置 Teams 集成的示例。

![Commerce Headquarters 中的 Teams 集成配置。](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>禁用 Teams 集成

若要在 Commerce Headquarters 中禁用 Microsoft Teams 集成，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。
1. 在操作窗格上，选择 **编辑**。
3. 将 **启用 Microsoft Teams 集成** 选项设置为 **否**。
4. 清除 **应用程序 ID** 和 **应用程序密钥** 字段中的值。
1. 在操作窗格上，选择 **保存**。

> [!NOTE]
> 禁用 Teams 与 Commerce 的集成后，POS 终端将不再显示从 Teams 应用程序发布的任务。

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 和 Microsoft Teams 集成概览](commerce-teams-integration.md)

[从 Dynamics 365 Commerce 预配 Microsoft Teams](provision-teams-from-commerce.md)

[在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理](synchronize-tasks-teams-pos.md)

[在 Microsoft Teams 中管理用户角色](manage-user-roles-teams.md)

[如果 Microsoft Teams 中有预先存在的团队，映射商店和团队](map-stores-existing-teams.md)

[Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答](teams-integration-faq.md)
