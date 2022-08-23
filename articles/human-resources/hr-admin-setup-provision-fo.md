---
title: 在财务和运营基础结构中预配 Human Resources
description: 本文介绍在财务和运营基础结构中为 Microsoft Dynamics 365 Human Resources 预配新生产环境的流程。
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221583"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>在财务和运营基础结构中预配 Human Resources

_**适用于：** 财务和运营应用基础结构中的 Human Resources_ 

> [!NOTE]
> 从 2022 年 7 月开始，无法在独立的 Human Resources 基础结构中预配新的 Human Resources 环境，因此无法在其中创建新的 Microsoft Dynamics Lifecycle Services (LCS) 项目。 客户可以在财务和运营基础结构上部署 Human Resources 环境。

本文介绍在财务和运营基础结构中为 Microsoft Dynamics 365 Human Resources 预配新生产环境的流程。

## <a name="prerequisites"></a>先决条件

在开始预配新环境之前，必须满足以下先决条件：

- 您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。 如果您有已包括 Human Resources 服务计划的现有 Dynamics 365 许可证，但无法完成本文中的步骤，请联系支持人员。
- 全局管理员已登录到 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) 并创建了新的财务和运营项目。

## <a name="provision-a-human-resources-trial-environment"></a>预配 Human Resources 试用环境

> [!NOTE]
> 从 2022 年 4 月开始，Human Resources 试用环境将无法在独立应用程序中使用。 有兴趣评估财务和运营应用中的 Human Resources 功能的潜在客户可以使用免费的 30 天试用以及演示数据。 Dynamics 365 Finance 将包括通过合并独立应用程序为 Finance 基础结构引入的 Human Resources 功能。 有关详细信息，请参阅[合并 HR 产品/服务为客户汇聚能力](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers)。 有关 Dynamics 365 Finance 试用版的详细信息，请参阅[分步指南](../fin-ops-core/fin-ops/get-started/before-you-buy.md)。

## <a name="plan-human-resources-environments"></a>计划 Human Resources 环境

在创建第一个 Human Resources 环境之前，您应该仔细计划项目的环境需求。 Human Resources 的基本订阅包括两个环境：生产环境和默认的标准验收测试（沙盒）环境。 根据项目的复杂性，您可以选择购买其他环境来支持项目活动。

以下是其他可选环境的一些注意事项：

- **数据迁移**：数据迁移活动使沙盒环境能够用于整个项目的测试。 如果具有一个附加环境，那么当测试和配置活动在不同环境中同时进行时，数据迁移活动可以继续进行。
- **集成** – 配置和测试集成，这可能包括本地集成或自定义集成，如工资单、申请人跟踪系统或福利系统和提供商的集成。
- **培训** - 您可能需要一个单独的环境，并在环境中配置一组培训数据，以便培训员工如何使用新系统。 
- **多阶段项目** - 您可能需要一个额外的环境来支持项目初始投入使用后计划的项目阶段内的配置、数据迁移、测试或其他活动。
- **开发** - 在财务和运营基础结构中，您现在可以扩展解决方案并开发您自己的自定义项。 每个开发人员都必须使用自己的开发环境。 有关详细信息，请参阅[部署和访问开发环境](../fin-ops-core/dev-itpro/dev-tools/access-instances.md)。
- **GOLD** - 对于新部署，一种常见的做法是使用单独的 GOLD 环境，该环境保持原始状态以便进行配置和数据迁移。 此环境可在整个实施过程中使用以刷新其他环境。 它将用于创建具有基本配置和数据迁移功能的新生产环境。 直到完成启用准备流程，您才能在财务和运营基础结构上部署生产环境。 有关详细信息，请参阅[准备实施](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)。

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> 在您考虑您的环境时，我们建议您使用以下方法：
>
> - 使用默认标准验收测试（以前的沙盒）环境或其他环境，在您实施之前进行模拟转换。
> - 保留一份详细的直接转换清单，其中包括在执行转换期间将最终数据迁移到生产环境所需的每个数据包。 如果您没有单独的 GOLD 环境来存储您的配置，则此建议尤其重要。
> - 在整个项目中使用默认标准验收测试（以前称为沙盒）环境或另一个 2 层或更高层环境作为测试环境。 如果您需要其他环境，您的组织可以购买，但需要支付额外的费用。

## <a name="create-an-lcs-project"></a>创建 LCS 项目

若要使用 LCS 来管理您的 Human Resources 环境，您必须先创建 LCS 项目。 如果要将 Human Resources 环境迁移到财务和运营基础结构，则必须为财务和运营应用创建新的 LCS 项目。 如果您已拥有其他财务和运营应用的 LCS 项目，则可以在 **功能管理** 工作区中启用 Human Resources 功能。 有关更多信息，请参见[功能管理概述](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

当新客户注册 Human Resources 时，订阅包括一个实施项目工作区。 客户激活服务后，租户管理员必须使用租户帐户在 <https://lcs.dynamics.com> 登录。 系统会自动为组织创建项目工作区。 有关详细信息，请参阅[面向财务和运营应用客户的 Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md)。

> [!NOTE]
> 要确保成功预配，必须将用于预配 Human Resources 环境的帐户分配给与 Human Resources 环境关联的 Power Apps 环境中的 **系统管理员** 角色或 **系统定制员** 角色。 有关如何在 Microsoft Power Platform 中为用户分配安全角色的详细信息，请参阅[为资源配置用户安全性](/power-platform/admin/database-security)。

您必须先完成 LCS 项目入门流程，然后才能开始部署环境。 有关详细信息，请参阅[项目入门](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md)。 有关如何使用 LCS 的详细信息，请参阅 [Lifecycle Services (LCS) 用户指南](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)。

## <a name="deploy-human-resources-environments"></a>部署 Human Resources 环境

若要在云中部署财务和运营应用（包括 Human Resources），您需要了解要部署到的环境和订阅、谁可以执行哪些任务以及您必须管理哪些数据和自定义项。 我们建议您在部署新环境时使用服务帐户而不是指定用户。 有关如何在财务和运营基础结构中部署环境的详细信息，请参阅[云部署概览](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview)。

要在财务和运营基础结构上部署 Human Resources 生产环境，您必须完成启用准备流程。 有关详细信息，请参阅[准备实施](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)。 此流程包括 LCS 中的订阅估算器。 有关详细信息，请参阅[订阅估算器](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md)。

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>将 Microsoft Power Platform 与 Human Resources 集成

Microsoft Power Platform 通过 Power Platform 管理中心提供一套 Dynamics 365 应用程序功能。 您可以使用 Microsoft Power Platform 集成和扩展 Human Resources 数据的使用。 有关如何将 Microsoft Power Platform 与 Human Resources 集成的信息，请参阅 [Microsoft Power Platform 与财务和运营应用的集成](../fin-ops-core/dev-itpro/power-platform/overview.md)。

## <a name="supported-geographies"></a>支持的地理区域

有关 Human Resources 支持的语言和地区的信息，请参阅[设计初衷面向全球：了解受支持的国家/地区和语言](https://dynamics.microsoft.com/availability-reports/)。

## <a name="grant-access-to-the-environment"></a>授予对环境的访问

默认情况下，创建环境的全局管理员可以访问环境。 您必须为更多应用程序用户明确授予访问权限。 您必须在 Human Resources 环境中添加用户并为其分配相应角色。 有关详细信息，请参阅[创建新用户](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users)和[向安全角色分配用户](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles)。

## <a name="additional-resources"></a>其他资源
您可以使用以下资源详细了解如何在财务和运营应用基础结构上使用和管理 LCS 中的项目：

- [Lifecycle Services 资源](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS)用户指南](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [自助服务部署概览](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [数据库移动操作主页](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
