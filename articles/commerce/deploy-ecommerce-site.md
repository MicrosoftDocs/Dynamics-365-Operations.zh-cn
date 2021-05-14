---
title: 部署新的电子商务租户
description: 本主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的 Dynamics 365 Commerce 电子商务站点。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936698"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>部署新的电子商务租户

[!include [banner](includes/banner.md)]

本主题介绍如何使用 Microsoft Dynamics Lifecycle Services (LCS) 部署新的 Dynamics 365 Commerce 电子商务站点。

Microsoft Dynamics Lifecycle Services (LCS) 是基于云的协作工作空间，合作伙伴和客户可将其用于管理自己的项目和环境，查看有关 Microsoft Dynamics 产品和功能的最新信息，以及创建，跟踪和浏览支持事件。 电子商务管理功能将集成到 LCS 中。

若要详细了解 LCS，请参阅 [Lifecycle Services 用户指南](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)。
    
## <a name="get-started"></a>开始

必须先初始化项目、环境和 Retail Cloud Scale Unit (RCSU)，才能初始化电子商务。 若要在 LCS 中执行初始化，必须具有项目负责人或环境管理员角色的权限。 支持生产环境和沙盒环境拓扑。

有关环境的详细信息，请参阅[环境计划](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)。 有关 RCSU 的详细信息，请参阅[初始化 Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)。

## <a name="initialize-e-commerce"></a>初始化电子商务

使用此过程在现有环境中初始化电子商务功能。

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

> [!NOTE]
> 以后可通过服务请求添加此信息。

收集所需信息之后，请执行以下步骤初始化电子商务。

1. 登录 [LCS](https://lcs.dynamics.com)。
1. 打开包含要在其中初始化电子商务的环境的项目。
1. 在 **环境** 部分中，选择环境。
1. 在 **环境功能** 下，选择 **零售管理** 链接。
1. 在 **电子商务** 选项卡中，选择 **设置**。 将显示对话框，必须在其中输入预配所需信息。
1. 填写必需信息，然后转到下一页。
1. 在下一页，填写必需信息，然后提交表单。 将回到 **电子商务** 选项卡，在这里应该会看到已经开始初始化。
1. 若要查看初始化状态，请 **刷新** 或以后回到 **电子商务** 选项卡。
    
从 LCS 初始化电子商务时，系统将预配电子商务所需的若干组件，并将其与环境关联。 预配完成后，将更新 **零售管理** 页中的 **电子商务** 选项卡以体现预配。 页面将显示最新自定义部署和其他任何进行中部署的状态。 还包含指向电子商务站点以及在其中创作站点的 Commerce 站点构建器的链接。

## <a name="access-commerce-site-builder"></a>访问 Commerce 站点构建器

若要访问 Commerce 站点构建器，请转到 LCS 中 **零售管理** 页面上的 **电子商务** 选项卡，然后选择 **电子商务站点管理工具** 链接。 站点构建器登录页面显示租户级别的视图。 从此页中，您可以：

- 修改租户级别设置。
- 导航到您创建并有权查看的任何站点。 
- 访问审核功能，例如审查和报告。
- 创建新站点。 有关如何创建新站点的详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。 

## <a name="additional-resources"></a>其他资源

[配置域名](configure-your-domain-name.md)

[创建电子商务站点](create-ecommerce-site.md)

[将 Dynamics 365 Commerce 站点与在线渠道相关联](associate-site-online-store.md)

[管理 robots.txt 文件](manage-robots-txt-files.md)

[批量上传 URL 重定向](upload-bulk-redirects.md)

[在 Commerce 中设置 B2C 租户](set-up-B2C-tenant.md)

[设置用户登录自定义页面](custom-pages-user-logins.md)

[在 Commerce 环境中配置多个 B2C 租户](configure-multi-B2C-tenants.md)

[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)

[启用基于位置的商店检测](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]