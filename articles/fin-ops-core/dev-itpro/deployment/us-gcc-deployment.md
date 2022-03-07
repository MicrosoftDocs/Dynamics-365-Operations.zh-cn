---
title: 美国政府社区云 (GCC) 中的 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management
description: 本主题提供有关可供合格政府和私人实体使用的 Microsoft Dynamics 365 US Government 产品的信息。
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817437"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>美国政府社区云 (GCC) 中的 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

选择可供合格政府和私人实体使用的 Microsoft Dynamics 365 United States (US) Government 产品。 这些实体仅限于以下类型：

- 美国联邦、州、地方、部落和地区政府实体
- 使用 Dynamics 365 US Government 向政府实体或云社区合格成员提供解决方案的私人实体
- 具有受政府法规约束的客户数据且 Dynamics 365 US Government 是满足监管要求的相应服务的私人实体

有关信息，请参阅 [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)。

## <a name="onboarding"></a>入职培训

若要完成 Microsoft Dynamics Lifecycle Services (LCS) 中实施项目的初始培训，请按照[培训实施项目](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md)中的说明进行操作。 但是，不要使用指向这些说明中提供的公共 LCS 的链接。 请改用以下 URL 为美国政府社区云 (GCC) 打开 LCS：<https://gov.lcs.microsoftdynamics.us>。

初始培训完成后，按照[项目培训](../lifecycle-services/project-onboarding.md)中的说明进行操作。 再次使用[适用于 GCC 的 LCS](https://gov.lcs.microsoftdynamics.us)，而不是公共 LCS。

## <a name="environment-deployment"></a>环境部署

完成项目培训后，您可以查看[适用于 Finance and Operations 应用客户的 Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) 中描述的其他 LCS 功能。 然后，继续进行环境部署。

- 若要通过 LCS 部署 Microsoft 托管环境，请按照[适用于 Finance and Operations 应用客户的 Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) 中的说明进行操作。
- 对于云托管的环境，请参阅[部署和访问开发环境](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md)。 您还必须完成连接器的资源管理器培训流程，如[完成美国政府 Lifecycle Services 项目的 Azure 资源管理器入门培训流程](arm-onbarding-us-goverment.md)中所述。

> [!NOTE]
> 对于美国政府 LCS 项目，仅支持 Azure 政府特定的 Azure 订阅。

## <a name="features-that-arent-available"></a>不可用的功能

某些功能将不可在 GCC 中部署，或者它们将无法在 GCC 中与 Dynamics 365 配合使用。 例如，Azure DevOps 服务在 GCC 中不可用。 但是，可以使用本地 Azure DevOps 或公共 Azure DevOps 服务。 有关功能可用性的详细信息，请参阅 [Business Applications US Government 功能可用性](https://aka.ms/BAPFunctionalParity)。

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>GCC-High 中是否支持 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management？

否。 GCC 中仅支持 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management。

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>我可以在 GCC 中将公用 Azure DevOps 与 Finance 和 Supply Chain Management 配合使用吗？

是的，如果您没有联邦风险与授权管理计划 (FEDRAMP) 认证的解决方案 方面的要求，则可以使用公共 Azure DevOps 服务。 或者，您可以使用 Azure DevOps 服务器。

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>能否在 Azure Commercial 订阅上部署云托管环境 1 级开发环境？

否。 在[适用于 GCC 的 LCS](https://gov.lcs.microsoftdynamics.us) 中，您必须使用 Azure 政府订阅才能部署云托管的环境。

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>如果我需要共用资产库中的包，但该包在适用于 GCC 的 LCS 中不可用，我该做什么？

您可以在[公共 LCS](https://lcs.dynamics.com) 中从共用资产库下载此包。 或者，您的合作伙伴可以帮助您下载此包。

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>代码升级工具是否在 GCC 中可用？

不，代码升级工具当前在 GCC 中不可用。 但是，您可以在[公共 LCS](https://lcs.dynamics.com) 中创建目标客户项目并使用代码升级工具。 请注意，您将无法在目标客户项目中部署环境。

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>我的合作伙伴是否可以代表我打开支持票证？

是。 但是，如果您的合作伙伴使用非 GCC 标识，则支持票证将被定向到公共支持队列。 我们建议您使用 LCS 中的客户 GCC 权利打开支持票证。

## <a name="see-also"></a>请参阅

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Business Applications US Government 功能可用性](https://aka.ms/BAPFunctionalParity)。
- [Lifecycle Services (LCS)用户指南](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [云部署概览](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
