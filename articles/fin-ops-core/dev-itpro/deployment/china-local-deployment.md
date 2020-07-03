---
title: 世纪互联在中国运营的 Dynamics 365 Finance 和世纪互联在中国运营的 Dynamics 365 Supply Chain Management
description: 本主题提供有关 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management（由世纪互联在中国运营）的信息。
author: kfend
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4088c8e82c1087e240e35d73b2e567e091af2a2e
ms.sourcegitcommit: 3fa1e8583003a90ba486f757c3826b139e1b3f73
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421520"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management---operated-by-21vianet-in-china"></a>Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management - 由世纪互联在中国运营

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 联机服务由世纪互联运营，可符合中国的监管要求。 这些服务是目前由本地运营商上海蓝云网络科技有限公司（以下简称**世纪互联**）运营和处理的云服务的物理分离实例。 该公司是位于中国大陆的北京世纪互联宽带数据中心有限公司的全资子公司。

Microsoft 将尽力保持商用服务与由世纪互联在中国运营的 Finance and Operations 应用之间的功能一致性。 但是，受依赖服务或合作伙伴解决方案可用性、市场优先级或法规合规性的影响，二者在功能一致性方面将存在明显的例外。

## <a name="provisioning"></a>预配

在选择如何访问 Finance 和 Supply Chain Management 应用时，中国客户有两个选项。

- 由世纪互联在中国运营的服务 - 世纪互联在中国运营并提供 Finance 和 Supply Chain Management 服务。 此选项提供与全球服务同样的一致应用程序体验。 此选项同时可满足希望使用由在中国境内存储数据的本地公司提供的联机服务的客户的要求。 为了遵守中国法律，这些服务有可能会有所更改。

- 由 Microsoft 运营的服务 – 此选项适用于希望使用 Microsoft 管理和提供的服务的 Finance 和 Supply Chain Management 客户。 无论是新客户还是现有客户，只要客户通过企业协议购买了 Microsoft Azure、Dynamics 365 和 Office，Office 365 和/或 Dynamics 365 就可以在租户中共存。

预配服务期间需要考虑到若干技术限制，以避免潜在的问题。 

|场景  |建议  |
|---------|---------|
|**通过 OSPA 购买 Azure、Office 365 和 Dynamics 365。**    |建议的预配顺序：必须先预配 Office 365 或 Dynamics 365，再预配 Azure。|
|**先通过 OSPA 购买 Azure，然后通过 OSPA 购买 Office 365。最后再通过 OSPA 购买 Dynamics 365。**   | 客户已经有两个租户，一个用于 Azure，另一个用于 Office 365。 Dynamics 365 可以添加到包含 Office 365 OSPA 的租户。        |
|**通过 OSPA 购买 Office 365，然后通过 OSPA 购买 Azure。最后再通过 OSPA 购买 Dynamics 365。**     | 客户先购买了 Office 365，然后添加了 Azure。 Dynamics 365 可以预配在同一租户上。        |
|**通过 OSPA 购买 Office 365，并计划添加 Dynamics 365。**   |如果已预配 Office 365，则客户可以在同一租户上预配 Dynamics 365。         |
|**通过 OSSA 或 CSP 购买 Office 365，然后购买 Dynamics 365。**    |Dynamics 365 需要在单独的租户上预配。          |

- OSPA = 联机服务高级版协议 
- OSSA = 联机服务标准版协议
- CSP = 云解决方案提供商

有关预配环境的信息，请参阅 [Power Platform 管理中心的“创建和管理环境”部分](https://docs.microsoft.com/power-platform/admin/create-environment)。

## <a name="features-not-available"></a>不可用的功能

由于某些技术依赖性，由世纪互联运营的 Dynamics 365 服务中通常不提供下列功能： 有关功能未来可用性的信息，请参阅[业务应用程序和平台发布计划](https://go.microsoft.com/fwlink/?linkid=2010158)。

-   **开发、构建和测试自定义**功能在**中国大陆境内的 Azure DevOps** 中将不可用。 但是，从 2019 年 4 月起，中国将支持在本地使用 Azure DevOps。 此外，可以在其他区域使用 Azure DevOps。 有关详细信息，请参阅[面向中国区 Azure 世纪互联的开发人员指南](https://docs.microsoft.com/azure/china/china-get-started-developer-guide)。

-   由于 Azure Active Directory 限制，[设置和维护供应商协作](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md)将不可用。

-   由于 Google Play 商店在中国不可用，某些**移动应用**（如[安装和配置仓库应用概述](../../../supply-chain/warehousing/install-configure-warehousing-app.md)和[项目时间条目移动工作区](../../../finance/project-management/project-time-entry-mobile-workspace.md)）将不可用；但正在考虑推出替代方案。

-   由于某些应用商店的依赖项在中国不可用，**[移动平台](../mobile-apps/platform/mobile-platform-home-page.md)** 将不可用。

-   由于依赖项不可用，以下 **Microsoft Dynamics Lifecycle Services (LCS)** 功能的用户体验将有所不同或者将不可用：

    -   **APQC 业务流程建模器 (BPM) 库**将不可用。 但是，从 2019 年 4 月起，将可针对自定义模型使用基本业务流程建模器 (BPM) 功能。 BPM 中的搜索功能在中国将不可用。

    -   **[电子报告 (ER) 概述](../analytics/general-electronic-reporting.md?toc=/fin-and-ops/toc.json)资产**不会自动提供，但可以从 LCS 全球资产库中手动上传。

    -   从 Dynamics AX 2012 升级时，不能使用**代码升级**。

    -   **服务和支持请求**可以通过 LCS 访问，但世纪互联是服务运营商。 有关详细信息，请参阅[对世纪互联在中国运营的 Dynamics 365 Finance and Operations 应用的支持](../lifecycle-services/21vianet-support.md)。
    
    -   [可扩展性请求](../extensibility/extensibility-requests.md)将不可用。
    
    -   修补程序请求将不可用。

    -   [Dynamics 365 Translation Service 概览](../lifecycle-services/translation-service-overview.md)将不可用。

    -   [嵌入式 Power Apps](../../fin-ops/get-started/embed-power-apps.md) 和与 Microsoft Power Apps 和 Microsoft Power Automate 的连接将不可用。

    -   [使用 Common Data Service 的数据集成概述](../data-entities/data-integration-cds.md?toc=/fin-and-ops/toc.json)将不可用。

-   由于中国目前存在某些 **Azure Active Directory 限制**，以下功能将不可用：

    -   由于中国的 Azure Active Directory 中不能使用企业到企业 (B2B)，**系统管理 \> 设置 \> B2B 邀请配置**页面将不可用。 有关详细信息，请参阅[在 Azure Active Directory B2B 中，来宾用户访问是什么？](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)。

-   [条件访问](https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference)是为 Azure Active Directory Premium 2 SKU 提供的 Azure Active Directory 功能。 此功能在中国不可用。 

## <a name="additional-resources"></a>其他资源

- [由世纪互联运营的 Dynamics 365 支持网站（中文）](https://www.21vbluecloud.com/Dynamics365/)
- [对世纪互联在中国运营的 Dynamics 365 Finance and Operations 应用的支持](../lifecycle-services/21vianet-support.md)
- [Dynamics 365 中的模型驱动应用 - 由世纪互联在中国运营](https://docs.microsoft.com/dynamics365/customer-engagement/admin/datacenter/about-microsoft-cloud-china)
- [Dynamics 365 隐私声明 (Dynamics 365 隐私声明)](https://www.21vbluecloud.com/Dynamics365/d365-privacy/)
- [Dynamics 365 Service Level agreement (世纪互联在线服务的服务级别协议)](https://www.21vbluecloud.com/Dynamics365/d365-sla/)
- [Dynamics 365 法律信息（Dynamics 365 法律信息）](https://www.21vbluecloud.com/Dynamics365/dynamics365-legal/)
- [Dynamics 365 Lifecycle Services 的服务条款](https://www.21vbluecloud.com/dynamics365/d365-lcs/)
- [OSPT of Dynamics 365 (世纪互联在线服务的服务级别协议)](https://www.21vbluecloud.com/ostpt/)
- [Azure 文档（中文）](https://docs.azure.cn/zh-cn/)
- [中国区 Azure 世纪互联](https://docs.microsoft.com/azure/china/china-welcome)
- [业务应用程序在中国的可用性 – 由世纪互联在中国运营](https://docs.microsoft.com/power-platform/admin/business-applications-availability-china)
