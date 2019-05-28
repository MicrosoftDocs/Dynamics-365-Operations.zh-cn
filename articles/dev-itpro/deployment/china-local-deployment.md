---
title: 世纪互联在中国运营的 Dynamics 365 for Finance and Operations
description: 本主题提供有关世纪互联在中国运营的 Dynamics 365 for Finance and Operations 的信息。
author: ShylaThompson
manager: AnnBe
ms.date: 04/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: afc6402250fb8457020d3807f754549cd042f0e7
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538404"
---
# <a name="dynamics-365-for-finance-and-operations---operated-by-21vianet-in-china"></a>世纪互联在中国运营的 Dynamics 365 for Finance and Operations

[!include [banner](../includes/banner.md)]

世纪互联运营的 Microsoft Dynamics 365 Online 服务旨在满足中国的法规要求。 这些服务是由本地运营商上海蓝云网络科技有限公司（即**世纪互联**）运营和处理的，物理分隔的云服务实例。 这家公司是中国大陆的北京世纪互联宽带数据中心有限公司北京的全资子公司。

Microsoft 致力于维护我们的商业服务与世纪互联在中国运营的 Dynamics 365 for Finance and Operations 之间的功能平等。 但是，这有些重要例外，这些例外会受到依赖服务或合作伙伴解决方案可用性、市场优先级或合规性法规的影响。

## <a name="features-not-available"></a>功能不可用

由于某些技术依赖项的原因，下面列出的功能不是世纪互联运营的 Dynamics 365 Services 常规提供的功能。 有关将来提供的功能的信息，请参阅[业务应用程序和平台版本说明](https://go.microsoft.com/fwlink/?linkid=2010158)。

-   **中国大陆的 Azure DevOps** 中不支持**开发、构建和测试定制功能**。 但是，2019 年 4 月开始支持使用 Azure DevOps 本地部署。 此外，其他地区也可以使用 Azure DevOps。 有关详细信息，请参阅 [Azure 中国世纪互联开发人员指南](https://docs.microsoft.com/azure/china/china-get-started-developer-guide)。

-   **Retail cloud scale unit** 功能将不可用。 但是，从 2019 年 4 月开始，[Retail store scale unit](../../retail/dev-itpro/retail-store-system-begin.md) 和 Retail Modern Store 应用将可用。

-   由于 Azure Active Directory 限制，[供应商管理和协作](../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md)将不可用。

-   由于 Google Play Store 在中国不可用，所以某些**移动应用**（如[仓库](../../supply-chain/warehousing/install-configure-warehousing-app.md)和[项目时间录入移动工作区](../../financials/project-management/mobile-timesheets.md)）将不可用；但是，正在考虑备用项。

-   由于某些 App store 依赖项在中国不可用，所以**[移动平台](../mobile-apps/platform/mobile-platform-home-page.md)** 将不可用。

-   以下 **Microsoft Dynamics Lifecycle Services (LCS)** 功能提供不同的体验或因为依赖项不可用而不可用：

    -   **APQC 业务流程建模器 (BPM) 库**将不可用。 但是，从 2019 年 4 月开始，基本业务流程建模器 (BPM) 功能将可用于自定义模型。 BPM 中的搜索功能将在中国不可用。

    -   **[电子申报 (ER)](../analytics/general-electronic-reporting.md?toc=/fin-and-ops/toc.json) 资产**将自动不可用，但是可以从 LCS 全球资产库手动上传。

    -   不可对来自 Dynamics AX 2012 的升级执行**代码升级**。

    -   可通过 LCS 创建**服务和支持请求**，但是世纪互联为服务运营商。 有关详细信息，请参阅[世纪互联支持运营的 Dynamics 365 Finance and Operations](../lifecycle-services/21vianet-support.md)。
    
    -   [可扩展性支持请求](../extensibility/extensibility-requests.md)将不可用。
    
    -   修补程序请求将不可用。

    -   [Translation service](../lifecycle-services/translation-service-overview.md) 将不可用。

-   [嵌入式 PowerApps](../../fin-and-ops/get-started/embed-power-apps.md) 和连接 Microsoft PowerApps 与 Microsoft Flow 将不可用。

-   [使用 Common Data Service 的数据集成](../data-entities/data-integration-cds.md?toc=/fin-and-ops/toc.json)将不可用。

-   由于中国的某些**现有 Azure Active Directory 限制**，下列功能将不可用：

    -   由于在中国，Azure Active Directory 中企业到企业 (B2B) 不可用，**系统管理 \> 设置 \> B2B 邀请配置**页面将不可用。 有关详细信息，请参阅 [Azure Active Directory B2B 中的来宾用户访问是什么](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)。

-   [条件式访问](https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference)是一项可用于 Azure Active Directory Premium 2 SKU 的 Azure Active Directory 功能。 此项功能在中国不可用。 

## <a name="additional-resources"></a>其他资源

- [世纪互联的 Dynamics 365 支持站点（中文）](https://www.21vbluecloud.com/Dynamics365/)
- [对世纪互联运营的 Dynamics 365 for Finance and Operations 的支持](../lifecycle-services/21vianet-support.md)
- [世纪互联运营的 Dynamics 365 for Customer Engagement](https://docs.microsoft.com/dynamics365/customer-engagement/admin/datacenter/about-microsoft-cloud-china)
- [Dynamics 365 Privacy statement (Dynamics 365 隐私声明)](https://www.21vbluecloud.com/Dynamics365/d365-privacy/)
- [Dynamics 365 Service Level agreement (世纪互联在线服务的服务级别协议)](https://www.21vbluecloud.com/Dynamics365/d365-sla/)
- [Dynamics 365 Legal information (Dynamics 365 法律信息)](https://www.21vbluecloud.com/Dynamics365/dynamics365-legal/)
- [Dynamics 365 Lifecycle Services 的服务条款](https://www.21vbluecloud.com/Dynamics365/d365-lcs/)
- [OSPT of Dynamics 365 (世纪互联在线服务的服务级别协议)](https://www.21vbluecloud.com/ostpt/)
- [Azure 文档（中文）](https://docs.azure.cn/zh-cn/)
- [Azure 中国世纪互联](https://docs.microsoft.com/azure/china/china-welcome)
