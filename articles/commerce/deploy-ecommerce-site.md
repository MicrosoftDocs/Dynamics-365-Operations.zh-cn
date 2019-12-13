---
title: 部署新的电子商务租户
description: 此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务租户。
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697443"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>部署新的电子商务租户

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的电子商务站点。

## <a name="overview"></a>概览
    
Microsoft Dynamics Lifecycle Services (LCS) 是基于云的协作工作空间，合作伙伴和客户可将其用于管理自己的项目和环境，查看有关 Microsoft Dynamics 产品和功能的最新信息，以及创建，跟踪和浏览支持事件。 电子商务管理功能集成到 LCS 中。

若要详细了解 LCS，请参阅 [Lifecycle Services 用户指南](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)。
    
## <a name="get-started"></a>入门

必须先初始化项目、环境和 Retail Cloud Scale Unit (RCSU)，才能初始化电子商务。 若要在 LCS 中执行初始化，必须具有项目负责人或环境管理员角色的权限。 支持生产环境和沙盒环境拓扑。

有关环境的详细信息，请参阅[环境计划](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)。 有关 RCSU 的详细信息，请参阅[初始化 Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)。

## <a name="initialize-e-commerce"></a>初始化电子商务

此过程用于初始化现有环境中的电子商务功能。

首先，确保具有以下必需信息：

- 将使用的 RCSU。
- 将用于电子商务系统管理员的 Microsoft Azure Active Directory 安全组。
- 将用于评分和评价审查者的 Microsoft Azure Active Directory 安全组。
- 将与环境关联的域。

此外，还可以收集以下可选信息：

- Azure AD 企业对消费者 (B2C) 信息：

    - 租户名称。
    - 客户端 ID。
    - 登录自定义域。
    - 回复 URL。
    - 注册登录策略 ID。
    - 重置密码策略 ID。
    - 编辑个人资料策略 ID。

[!NOTE]
以后可通过服务请求添加此信息。

收集所需信息之后，请执行以下步骤初始化电子商务。

1. 登录 [LCS](https://lcs.dynamics.com)。
1. 打开包含要在其中初始化电子商务的环境的项目。
1. 在**环境**部分中，选择环境。
1. 在**环境功能**下，选择**零售管理**链接。
1. 在**电子商务**选项卡中，选择**设置**。 将显示对话框，必须在其中输入预配所需信息。
1. 填写必需信息，然后转到下一页。
1. 在下一页，填写必需信息，然后提交表单。 将回到**电子商务**选项卡，在这里应该会看到已经开始初始化。
1. 若要查看初始化状态，请**刷新**或以后回到**电子商务**选项卡。
    
从 LCS 初始化电子商务之后，系统将预配电子商务所需若干组件，并将其与环境关联。 预配完成后，将更新**零售管理**页中的**电子商务**选项卡以体现预配。 页面将显示最新自定义部署和其他任何进行中部署的状态。 还包含电子商务站点和电子商务站点管理工具（创作工具）的链接。

## <a name="access-the-authoring-environment"></a>访问创作环境

若要访问创作环境，请转到**零售管理**页中的**电子商务**选项卡。 可在这里找到电子商务站点和站点管理工具的链接。

## <a name="additional-resources"></a>其他资源

[在线商店概览](online-store-overview.md)

[创建电子商务站点](create-ecommerce-site.md)

[将在线站点与渠道关联](associate-site-online-store.md)

[配置域名](configure-your-domain-name.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)
