---
title: 启用 Dynamics 365 Commerce 和 Microsoft Teams 集成
description: 本主题介绍如何启用 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9910ee48a0792c89a4e04ec8685fd02484e45575d70b06454dea56a89ee8c914
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775330"
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
1. 复制已注册应用的 **概述** 页面中的 **应用程序（客户端）ID** 值。 您将使用该值在 Commerce Headquarters 中启用 Teams 集成。
1. 复制您在步骤 1 中[添加证书](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)时输入的证书值。 该证书也称为公钥或应用程序密钥。 您将使用该值在 Commerce Headquarters 中启用 Teams 集成。

若要在 Commerce Headquarters 中启用 Teams 集成，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。
1. 在操作窗格上，选择 **编辑**。
1. 将 **启用 Microsoft Teams 集成** 选项设置为 **是**。
1. 在 **应用程序 ID** 和 **应用程序密钥** 字段中，输入您在 Azure 门户中注册 Teams 应用程序时获取的值。
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