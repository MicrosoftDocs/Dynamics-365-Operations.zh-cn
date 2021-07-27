---
title: 电子商务站点概述
description: 本主题概述了 Microsoft Dynamics 365 Commerce 中对电子商务站点的支持。
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b7050f954116213f700e4a2b3326547f4d070674
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353004"
---
# <a name="e-commerce-site-overview"></a>电子商务站点概览

[!include [banner](includes/banner.md)]

本主题概述了 Microsoft Dynamics 365 Commerce 中对电子商务站点的支持。 它包含有关如何在 Dynamics 365 Commerce 中初始化和管理电子商务在线商店的信息。 另外还提供了有关在线商店的详细信息以及有关如何设置和配置电子商务站点的详细信息的链接。 尽管本主题涵盖许多基础知识，但并未涵盖设置生产电子商务站点所需的所有内容。 可在 Dynamics 365 Commerce 文档中找到更多高级主题。

## <a name="online-store-channel"></a>在线商店渠道

您必须至少先设置一个在线商店渠道，才能在 Dynamics 365 Commerce 中构建站点。 有关详细信息，请参阅[设置在线渠道](channel-setup-online.md)。 

在 Dynamics 365 Commerce 中，使用在线商店渠道建立产品、定价、语言、付款方式、交货方式、履行中心，以及应为客户提供的在线体验的其他方面。

只需设置一个在线商店渠道，便可以开始使用 Dynamics 365 Commerce。 但是，一个电子商务站点可以为多个在线商店提供在线体验。 例如，如果设置多个在线商店来支持不同的地理区域，可以使用一组电子商务页面来提供每个商店定义的独特体验。 有关如何配置站点以支持多个在线商店的详细信息，请参阅[将在线站点与渠道关联](associate-site-online-store.md)。

设置在线商店后，可以将其与将用作您的在线店面的 Dynamics 365 Commerce 站点关联。 有关在线商店以及如何设置的详细信息，请参阅[设置在线商店](/dynamics365/unified-operations/retail/online-stores)。

## <a name="deploy-a-new-e-commerce-tenant"></a>部署新的电子商务租户

在电子商务站点初始化期间，系统会提示您输入域名。 有关 Commerce 中的域的详细信息，请参阅[配置域名](configure-your-domain-name.md)和 [Dynamics 365 Commerce 中的域](domains-commerce.md)。 若要使用 [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) 部署新的电子商务租户，请按照[部署新的电子商务租户](deploy-ecommerce-site.md)中的步骤操作。 在 LCS 中设置电子商务租户后，将提供指向 Commerce 站点构建器的链接。 然后，您可以使用 Commerce 站点构建器来初始化和配置您的电子商务站点。

## <a name="initialize-your-e-commerce-site"></a>初始化电子商务站点

从 LCS 启动 Commerce 站点构建器时，将显示 **站点** 页面。 该页面包括两个预配置的站点（**默认** 和 **Fabrikam**），如下图中的示例所示。

![Commerce 站点构建器中的站点页面。](media/e-commerce-site-01.png)

当您选择其中一个站点时，系统会提示您选择域名、默认的在线商店渠道、所选渠道的受支持语言以及路径。 如果仅使用一个渠道，可以将路径保留为空白。 稍后可以在 Commerce 站点构建器中配置更多在线商店渠道或语言。 每个附加的渠道或语言都需要唯一的路径。 例如，您有两个与单个站点相关联的在线渠道，并且该站点的域名为 `www.fabrikam.com`。 在这种情况下，一个渠道的路径可以是没有路径的默认值 (`https://www.fabrikam.com`)，第二个渠道可以设置为将具有 URL `https://www.fabrikam.com/site2` 的新路径，例如 **site2**。 下图显示 Commerce 站点构建器中的站点初始化对话框的示例。

![Commerce 站点构建器中的站点初始化对话框。](media/e-commerce-site-02.png)

**站点** 页面还包含 **新建站点** 按钮。 选择此按钮时显示的对话框类似于站点初始化对话框，但是它用于创建新站点。 新站点为空白。 它们不包含通过 **默认** 和 **Fabrikam** 站点提供的相同默认模板、片段、页面和图像。 但是，您可以根据需要打开支持票证，以请求将默认内容的副本添加到新的空白站点。 有关详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。

初始化新站点后，将显示 Commerce 站点构建器 **主页**。 该页面包含指向常见操作和指导内容的链接，如下图中的示例所示。

![Commerce 站点构建器中的主页上的链接。](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>修改在线商店渠道或将在线商店渠道添加到电子商务站点

创建电子商务站点后，您可以按照[将电子商务站点与在线渠道关联](associate-site-online-store.md)中的步骤更改与之关联的渠道。 下图中的示例显示如何在 **渠道** 页面（**站点设置 \> 渠道**）上更改渠道操作单位编号 (OUN)。 完成更改后，请务必选择 **保存并发布**。 这样，您可以确保发布更改。

![Commerce 站点构建器中的渠道页面。](media/e-commerce-site-04.png)

您可以通过选择 **添加渠道** 添加新渠道。 若要将新语言添加到渠道，请选择该渠道，然后在显示的渠道对话框中选择 **添加区域设置**。 在区域设置显示在对话框中之前，必须在 Commerce 总部中为在线商店渠道预先配置它们。

![Commerce 站点构建器中的渠道对话框。](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>设置 Azure B2C 租户

Dynamics 365 Commerce 使用 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 支持用户凭据和身份验证流。 有关如何设置 Azure B2C 租户的信息，请参阅[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)、[设置用户登录自定义页面](custom-pages-user-logins.md)和[在 Commerce 环境中配置多个 B2C 租户](configure-multi-b2c-tenants.md)。

## <a name="overview-of-the-default-site-pages"></a>默认站点页面概述

**默认** 和 **Fabrikam** 站点包括预配置的模板、片段和页面，以帮助您入门。 有关详细信息，请参阅以下主题：

- [主页概览](quick-tour-home-page.md)
- [产品详细信息页面概述](quick-tour-pdp.md)
- [购物车和结帐页面概览](quick-tour-cart-checkout.md)
- [帐户管理页面概览](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>管理站点设置

有关如何管理站点设置的信息，请参阅以下主题：

- [管理电子商务用户和角色](manage-ecommerce-users-roles.md)
- [站点的搜索引擎优化 (SEO) 注意事项](/search-engine-optimization-considerations.md)
- [管理内容安全策略 (CSP)](manage-csp.md)
- [选择站点主题](select-site-theme.md)

## <a name="manage-site-content"></a>管理站点内容

有关如何管理站点内容的信息，请参阅以下主题：

- [页面模型词汇表](page-elements-overview.md)
- [文档状态和生命周期](document-states-overview.md)
- [模板和布局](templates-layouts-overview.md)
- [使用片段](work-with-fragments.md)
- [使用模块](work-with-modules.md)
- [数字资产管理概览](dam-overview.md)
- [模块库概览](starter-kit-overview.md)

## <a name="additional-resources"></a>其他资源

[创建电子商务站点](create-ecommerce-site.md)

[部署新的电子商务站点](deploy-ecommerce-site.md)

[将在线站点与渠道关联](associate-site-online-store.md)

[配置域名](configure-your-domain-name.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]