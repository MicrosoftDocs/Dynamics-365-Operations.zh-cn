---
title: 财务和运营应用的服务描述
description: 本文提供财务和运营应用的服务描述。
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 756895ab0ccdbd2bc42f0a750ad9895ee7b284a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847151"
---
# <a name="service-description-for-finance-and-operations-apps"></a>财务和运营应用的服务描述

[!include[banner](../includes/banner.md)]

财务和运营应用是基于并为了 [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/) 构建的企业资源计划 (ERP) 软件即服务 (SaaS) 产品。 财务和运营服务为组织提供 ERP 功能，以便为其唯一需求提供支持，并帮助其针对不断变化的业务环境进行调整，同时无需管理基础结构。 财务和运营应用中可以包含下面的一个或多个解决方案领域：

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

这些应用与[商业智能](/power-bi/fundamentals/power-bi-service-overview)、[基础结构](https://azure.microsoft.com/global-infrastructure/)、[计算](/azure/service-fabric/service-fabric-overview)和[数据服务](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/)共同让组织可以运行业务特定的运营业务流程。 客户在其实现合作伙伴的支持下，可以确定最适合自己的唯一业务流程的业务应用程序配置。 可以通过下面的一种或多种解决方案增强或扩展功能和业务流程：

- [个性化体验](personalize-user-experience.md)中内置
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) 工具
- 基于 [Visual Studio](https://visualstudio.microsoft.com) 的[财务和运营软件开发工具包 (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) 和 [Azure DevOps 构建自动化](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- [AppSource](https://appsource.microsoft.com/partners) 中的独立软件供应商 (ISV) 解决方案

客户可以根据需求选择自己的解决方案方法。 客户可以与自己的实现合作伙伴合作，以便通过使用 [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md) 中提供的工具和最佳实践，定义、开发和测试自己的解决方案。 有四种常见方案：

- 标准财务和运营应用“现成”配置（无扩展名）
- 包含一个或多个 ISV 解决方案的财务和运营应用配置
- 包含一个或多个特定于客户的扩展的财务和运营应用配置
- 包含特定于客户的扩展和一个或多个 ISV 解决方案的组合的财务和运营应用配置

组织可以通过简单、透明的订阅模型轻松添加用户和业务流程来跟上其业务增长。 有关详细信息，请参阅 [Dynamics 365 许可指南](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)。

## <a name="operating-model"></a>运行模型

财务和运营应用的运行模型定义客户、实现合作伙伴和 Microsoft 在整个服务生命周期中的具体角色和职责。 有关详细信息，请参阅[云操作和服务](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md)。

### <a name="customer-activities"></a>客户活动

客户与其合作伙伴和 [Microsoft FastTrack](/dynamics365/fasttrack/) 合作，遵循 [Dynamics 365 实施指南](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide)和 [Success by Design](/dynamics365/fasttrack/success-by-design-overview) 框架，并使用 [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) 中提供的工具和最佳实践来实现自己的解决方案。 常见活动包括：

- 用户标识和安全管理
- 定义、开发和操作业务流程
- 定义，开发，测试和操作扩展
- 监控和管理非生产部署
- 管理应用程序更新和验证扩展
- 管理 ISV 解决方案和第三方集成

### <a name="microsoft-responsibilities"></a>Microsoft 的职责

Microsoft 通过在 Microsoft SaaS 订阅中部署，主动监控和服务客户的沙盒环境和生产环境来管理 财务和运营服务。 此管理包括分配所需系统基础结构以运行该服务，以及主动与客户沟通服务的运行状况。 职责包括：

**基础结构管理**
- 安全和隔离
- 操作系统和虚拟化
- 服务器、存储和网络
- 数据中心的电源、网络、散热

**应用程序平台管理**
- 全天候应用程序监控和通知
- 诊断、平台更新、修补程序、服务更新
- 应用程序路由、负载平衡、站点复制
- 环境预配和管理
- 数据库管理、高可用性 (HA)/灾难恢复 (DR)、缩放、操作
- 计算部署、扩大规模、缩小规模

## <a name="system-configuration"></a>系统配置

财务和运营应用根据事务量和用户负载进行缩放。 每个客户实现都会生成由以下元素构成的唯一解决方案：

- **数据构成** – 一组唯一参数，用于控制交易记录的行为、组织布局、主数据（如财务和库存维度）结构，以及跟踪粒度。
- **扩展和配置** – 扩展机制，其使用代码扩展、ISV 解决方案和其中包含工作流、集成和报告配置的唯一配置。
- **使用模式** – 在线使用和批量使用的唯一组合，其还可以与同一数据流的上游系统和下游系统集成，以及根据客户在其业务流程中使用的信息视图进行区分。

Microsoft 将配置其规模足以应对交易记录量和用户并发的客户生产环境。 Microsoft 负责以下任务：

- 根据 [LCS 订阅估算器](../../dev-itpro/lifecycle-services/subscription-estimator.md)中的客户分析信息正确分配生产环境的资源
- 持续监视和诊断生产环境的服务可用性
- 分析和解决财务和运营应用的系统性能问题

若要确保为高性能配置实现，客户必须完成以下任务：

- 在 [LCS 订阅估算器](../../dev-itpro/lifecycle-services/subscription-estimator.md)中提供有关财务和运营实现的精确使用信息。
- 生成扩展并测试其性能和缩放。
- 适当测试数据配置的性能。
- 通过在实施之前执行[性能测试](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018)确保可伸缩性。

## <a name="onboarding-and-implementation"></a>加入和实现

下表显示典型加入和实现活动。

| 请求 | 预期的 Microsoft 操作 | 预期的客户/实现合作伙伴操作 |
|---|---|---|
| 购买初始套餐 | 购买套餐之后，将根据客户触发的活动创建 LCS 项目。 | 完成企业协议 (EA) 或云解决方案提供商 (CSP) [商业流程](before-you-buy.md)。 如果可以，合作伙伴将为客户创建租户。 |
| 购买附加产品 | 为客户授予实现期间所选附加产品的访问权限。 | 不适用 |
| 规划和分析实现 | 在 LCS 中提供相关工具，如[业务流程建模器 (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) 和[与 Azure DevOps 的互操作性](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md)。 | 执行项目计划，设置 Azure DevOps，完成系统加入和设置管理员帐户。 |

有关详细信息，请参阅[加入和实现项目](../imp-lifecycle/onboard.md)。

## <a name="globalization"></a>全球化

财务和运营应用从全球多个 Azure 区域提供。 财务和运营应用提供功能来支持不同国家/地区和本地语言。 有关详细信息，请参阅[本地化和监管功能](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features)。

### <a name="countryregion-specific-considerations"></a>特定于国家/地区的注意事项

- 与需要在本地驻留数据的法国实体开展业务的受监管行业或商业组织的客户应该查看[法国的财务和运营](../../dev-itpro/deployment/france-local-deployment.md)。
- 在中国经营的客户应该查看 [Azure 中国 Playbook](/azure/china/) 和[由世纪互联在中国运营的财务和运营](../../dev-itpro/deployment/china-local-deployment.md)。
- 在俄罗斯运营的客户应该查看[俄罗斯个人数据本地化法](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia)。

### <a name="general-data-protection-regulation-gdpr"></a>一般数据保护条例 (GDPR)

对于财务和运营应用，Microsoft 充当处理器。 作为数据处理器，财务和运营提供进程和功能，以作为数据控制者来帮助客户履行 GDPR 义务。 有关详细信息，请参阅 [GDPR 概述](../../dev-itpro/gdpr/gdpr-guide.md)。

## <a name="environment-and-data-management"></a>环境和数据管理

此部分介绍服务中进行的一些典型环境和数据管理事件。

### <a name="environment-and-data-management-events-for-production-instances"></a>生产实例的环境和数据管理事件

LCS 提供[自助服务工具](../../dev-itpro/deployment/infrastructure-stack.md)和[数据库移动操作](../../dev-itpro/database/dbmovement-operations.md)，用于执行环境和数据管理任务。 下面举了一些示例加以说明：

**事件：**[请求生产实例](../imp-lifecycle/go-live-faq.md#when-can-i-configure-and-request-my-production-environment)

- 完成[实行准备情况查看](../imp-lifecycle/prepare-go-live.md)，然后将其提交给 [Microsoft FastTrack](/dynamics365/fasttrack/) 团队。
- 请求生产实例之前，请填写 [LCS 订阅估算器](../../dev-itpro/lifecycle-services/subscription-estimator.md)。
- 完成 [LCS 方法](../../dev-itpro/lifecycle-services/create-methodology.md)中指定的所有实现任务。

**事件：**[将沙盒数据库复制到生产实例](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- 为模拟实行或实际实行直接转换执行。

**事件：**[维护模式](../../dev-itpro/sysadmin/maintenance-mode.md)

1. 在 LCS 中开启维护模式。
2. 完成所需维护。
3. 在 LCS 中关闭维护模式。

### <a name="environment-and-data-management-events-for-non-production-instances"></a>非生产实例的环境和数据管理事件

LCS 提供[自助服务预配](../../dev-itpro/deployment/infrastructure-stack.md)和[数据库移动操作](../../dev-itpro/database/dbmovement-operations.md)，用于执行环境和数据管理任务。 下面举了一些示例加以说明：

**事件：**[部署新沙盒实例](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- 确保已[计划](../imp-lifecycle/environment-planning.md)所有必需实例，并且已购买适用的附加产品套餐。
- 在 LCS 中运行部署流程。
- 完成 LCS 清单中指定的所有任务。
    
>[!NOTE]
>开发沙盒环境是[部署到客户的 Azure 订阅](../../dev-itpro/dev-tools/access-instances.md)并由客户管理的虚拟机 (VM)。

**事件：**[将黄金配置数据库从沙盒环境复制到生产环境](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- 为模拟实行或实际实行直接转换执行。

**事件：**[将非生产实例还原到生产时间点备份](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- 在 LCS 中运行[刷新数据库](../../dev-itpro/database/database-refresh.md)选项。
- 复制后：通过脚本删除或混淆敏感数据，调整特定于环境的应用程序配置（如集成终结点），以及启用或添加用户。 请注意，这些更改是通过应用[数据包](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package)进行的。

**事件：**[非生产实例数据库时间点还原](../../dev-itpro/database/database-point-in-time-restore.md)

- 接受不能撤消进程。
- 在 LCS 中运行时间点还原操作。

**事件：** 将第 2 层沙盒数据库复制到开发沙盒，以进行疑难解答和[调试](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- 在第 2 层沙盒环境中 LCS 内运行数据库导出操作。
- 在开发环境中导入和更新数据库。

## <a name="data-backup-and-retention"></a>数据备份和保留

SaaS 订阅中适用于财务和运营环境的数据库受到自动备份的保护。 对于生产环境，除非 Microsoft 执行回滚操作，否则自动备份将保留 28 天。 对于沙盒（2 层以上）环境，将保留 7 天。 如果计划的任何维护更新期间失败，可以回滚生产环境。

有关自动备份的详细信息，请参阅[自动备份 - Azure SQL 数据库和 SQL 托管实例](/azure/azure-sql/database/automated-backups-overview?tabs=single-database)。

## <a name="service-activity-responsibilities"></a>服务活动职责

下表介绍了服务的一些典型方案和活动。 还指示由 Microsoft，客户还是 Microsoft 与客户共同负责这些活动。

| 活动 | Microsoft 的职责 | 客户的职责 |
|---|---|---|
| **预配初始租户** | | |
| 使用订阅估算器工具设置 LCS 中的预测负荷大小，并请求预配特定环境。 | | X |
| 预配所有生产实例和非生产实例。 | X | |
| 验证部署的生产实例和非生产实例。 | | X |
| **服务更新** | |
| 将服务更新应用于指定的非生产实例和生产实例。 | X | |
| 手动将服务更新从 LCS 应用于沙盒实例。 定义、开发、测试更新，并将代码更新包重新提供给 LCS。 | | X |
| 请求将计划扩展更新应用于生产实例。 | | X |
| 在应用任何更新之前，为生产实例创建代码和数据备份。 | X | |
| 如果失败，请将生产实例回滚到代码和数据备份。 | X | |
| **数据管理（备份、还原和更新）** | | |
| 备备数据库。 | X | |
| 确定高可用性和灾难恢复计划。 | X | |
| 监控生产实例数据库的性能。 | X | |
| 针对性能调整生产实例数据库。 | X | |
| 对非生产实例执行生产实例数据库时间点刷新。 | | X |
| **更新基础结构** | | |
| 计划基础结构常规更新。 | X | |
| **向上扩展和向下扩展（用户、存储和实例）** | | |
| 购买更多用户和非生产附加产品。 | | X |
| 在 LCS 订阅估算器工具中更新使用情况更改。 | | X |
| 报告影响使用服务的任何重大性能问题。 | | X |
| 主动管理适用服务所需的资源。 | X | |
| 调查和排除事件。 | X | |
| **安全性（用户访问权限）** | | |
| 为用户提供服务的访问权限。 | | X |
| 提供 LCS 项目访问权限以管理和操作通过 LCS 部署的实例。 | | X |
| **监视生产实例** | | |
| 全天候监视生产实例。 | X | |
| 主动向客户通知涉及生产实例的事件。 | X | |
| **管理和监视非生产实例** | | |
| 使用 LCS 管理非生产实例。 | | X |
| 监视非生产实例。 | | X |

## <a name="service-update-strategy"></a>服务更新策略

根据[软件生命周期策略](../../dev-itpro/migration-upgrade/versions-update-policy.md)，财务和运营应用遵守 Microsoft [现代生命周期策略](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy)，该策略涵盖持续服务和支持的产品。 

Microsoft 在每年的以下月份发布八个针对财务和运营应用的服务更新：

- 1 月
- 2 月
- 4 月
- 五月
- 七月
- 八月
- 十月
- 十一月

>[!NOTE]
>4 月和 10 月是主要功能发布波次。 可以可以暂停单个服务更新最多三个连续更新周期。

有关详细信息，请查看以下主题：

- [One Version 服务更新概览](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [通过 LCS 配置服务更新](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [通过 LCS 暂停服务更新](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [通过 LCS 获取有关服务更新的通知](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [用于验证服务更新的回归测试工具](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 路线图和发布波次](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>安全性和管理访问权限

财务和运营生产环境的管理访问权限受到严格控制并严格记录。 客户数据按照 [Microsoft 在线服务条款](https://www.microsoft.com/licensing/terms/productoffering)处理。 

### <a name="customer-administrative-access"></a>客户管理访问权限

客户的租户管理员可以访问生产实例或非生产实例，如下表中所述：

| 环境类型 | 目的 | 客户访问权限级别 |
|---|---|---|
| **非生产**<br>第 1 层沙盒 | 客户为开发、演示或培训目的部署的非生产环境。 | 第 1 层沙盒（也称为云托管环境）是从 LCS 部署到客户的 Azure 订阅的客户托管 VM。 由于它是客户 Azure 订阅中的 VM，因此客户拥有通过远程桌面的环境完全管理访问权限。 |
| **非生产**<br>第 2 层（或更高）沙盒 | 客户为用户接受度测试、集成测试、培训、暂存或任何其他生产前方案部署的非生产环境。 | 第 2 层及以上沙盒将部署到 财务和运营 SaaS 订阅。 将通过[即时访问](../../dev-itpro/database/database-just-in-time-jit-access.md)授予与非生产环境关联的 Azure SQL 数据库的访问权限。 不可访问远程桌面。 |
| **生产** | 当项目[准备好初始实现](../imp-lifecycle/environment-planning.md#production-system-readiness)时，将部署生产环境。. | 将把生产环境部署到 SaaS 订阅。 所有访问都通过浏览器、服务终结点或 LCS 进行。 |

### <a name="microsoft-administrative-access"></a>Microsoft 管理访问权限

下表显示不同 Microsoft 管理员的不同访问权限级别：

| 管理员 | 客户数据 |
|---|---|
| Operations 响应团队<br>（仅限关键人员） | 将通过支持票证授予访问权限。 访问权限将经过审核，并且仅限于支持活动的持续时间有效。 |
| Microsoft 客户支持服务 (CSS) | 无直接访问权限。 客户可以使用屏幕共享与支持人员合作来调试问题。 |
| 工程 | 无直接访问权限。 Operations 响应团队可以使用屏幕共享来处理工程调试问题。 |
| Microsoft 中的其他人 | 无访问权限。 |

## <a name="monitoring"></a>监视

Microsoft 已投资大量工具集来监视和诊断客户的生产实例。 Microsoft 全天候监视客户的生产环境。 有关详细信息，请参阅[生产支持和监视](../imp-lifecycle/production-support-monitoring.md)。

| Microsoft 的职责 | 客户的职责 |
|---|---|
| <ul><li>监视服务的可用性。</li><li>通过针对关键组件（如应用程序对象服务器 (AOS)、Batch、数据导入/导出框架 (DIXF)、Commerce 和 Management Reporter）的运行状况指标和监视程序，持续监视和预警。</li><li>监视基础结构服务（如 Azure Active Directory \[Azure AD\] 和 Azure SQL）导致的性能降级。</li><li>如果 Microsoft 确定单个流程或批处理作业导致反常，则会在与客户沟通之后终止该流程或作业。</li></ul> | <ul><li>监视对应用程序配置和扩展进行且可能导致功能问题和性能问题的更改。</li><li>必须使用监视工具诊断应用程序错误。 将使用这些工具诊断用户报告的性能偏差。</li><li>如果系统的预期负载超过预测的峰值使用量，请通知 Microsoft。</li><li>如果适用的服务在生产实例中不可用，客户可以使用 LCS 报告[生产中断](../../dev-itpro/lifecycle-services/report-production-outage.md)。</li></ul> |

客户可以通过 LCS 在线提交支持请求，让 Microsoft 以最有效、最高效的方式提供快速且深入的技术体验。 虽然支持手机选项，但是仅应在在线选项不可用时才使用这种选项。 有关详细信息，请参阅[手机支持选项](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support)。

## <a name="incident-management"></a>事件管理

Microsoft 根据严重性级别响应和解决事件。 可以在最初评估事件期间，随着有关影响和作用范围的信息越来越多，更改 Microsoft 的事件严重性级别。 如果事件已缓解，则事件严重性保持不变。

有关严重性级别的详细信息，请参见[此严重性表](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request)。

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>通过高可用性和灾难恢复来保持业务连续性 

在发生 Azure 区域范围的中断时，Microsoft 为财务和运营应用的生产实例提供业务连续性和灾难恢复。 有关详细信息，包括服务恢复时间目标 (RTO) 和恢复点目标 (RPO)，请参阅[业务连续性和灾难恢复](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md)。

- **高可用性** – HA 功能可用于阻止 Azure 数据中心中单一节点故障导致停机时间。 每个服务的云架构都对计算层使用 Azure 可用性集来避免单一故障点事件。 数据库的 HA 通过 [Azure SQL HA 功能](/azure/azure-sql/database/high-availability-sla)提供。
- **灾难恢复** – [Azure 灾难恢复功能](/azure/best-practices-availability-paired-regions)为各服务会抵御广泛影响整个 Azure 数据中心的中断。 下面是这些功能中的一部分：

    - 适用于主数据库（即业务数据库）的 Azure SQL 活动异地复制。
    - 其他 Azure 区域中的 Azure Blob 存储（其中包含文档附件）的异地冗余副本。
    - 用于复制 Azure SQL 和 Azure Blob 存储的次要区域。

如果使用灾难恢复恢复客户的生产实例，Microsoft 和客户需要履行自己的[事件管理](service-description.md#incident-management)职责。

将通过系统和组织控制 (SOC) 审核定期检查 Microsoft 的灾难恢复计划和过程。 这些合规性审审核证实 Microsoft DR（包括 Dynamics 365 财务和运营应用）的技术和程序性流程。 [Microsoft 信任中心合规产品](/compliance/regulatory/offering-home)中提供 [SOC 合规性](/compliance/regulatory/offering-soc-2)审核报告和其他所有报告。

## <a name="finance-and-operations-support-offerings"></a>财务和运营支持产品/服务

提供财务和运营服务的市场提供技术支持。 LCS 或财务和运营应用中提供了[支持体验](../../dev-itpro/lifecycle-services/lcs-support.md)。 下面举了一些示例加以说明：

- LCS 中的[问题随时](../../dev-itpro/lifecycle-services/issue-search-lcs.md)
- 财务和运营应用中的[集成技术支持](../../dev-itpro/lifecycle-services/support-experience.md)
- LCS 中的[云动力支持](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md)

Microsoft 为财务和运营客户提供三款支持计划：顶级、专业直接和订阅中包含的支持。 每个计划的支持级别不同。 下表显示这三款计划的比较。

| 支持功能 | 顶级 | 专业人员直接支持 | 预订 |
|---|---|---|---|
| 无限中断/修复事件提交 | 是 | 是 | 是 |
| 全天候通过 LCS 访问 | 是 | 是 | 是 |
| 事件响应时间 | 少于 1 小时 | 少于 1 小时 | 下一个工作日 |
| 咨询小时 | 按协议购置池。 | 否 | 否 |
| 专门的支持客户经理 | 是 | 否 | 否 |
| 专门的支持工程师 | 根据单独的协议联系 | 否 | 否 |

有关详细信息，请参阅[支持概述](/power-platform/admin/support-overview)。

### <a name="process-to-engage-support"></a>参与到联系上支持

如果发生了涉及财务和运营应用的事件，客户将通过 LCS 向 Microsoft 提交支持票证。 CSS 将根据客户的支持计划和 CSS 指定的事件严重性处理事件。

### <a name="service-level-agreement"></a>服务级别协议

Microsoft 承诺每个服务月的可用率为 99.9%。 如果 Microsoft 未能按照服务级别协议 (SLA) 中的说明达到和保持适用服务的服务级别，客户可以要求退还该服务的一部分月服务费。 有关如何启动服务退费的信息，请参阅 [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services) 的“索赔”部分 。

## <a name="important-resources"></a>重要资源

- **[信任中心](https://www.microsoft.com/trust-center)** – 获取有关财务和运营数据的存储位置的信息，以及有关隐私、合规性和安全过程的更多信息。
- **[许可条款和文档](https://www.microsoftvolumelicensing.com/)** – 快速访问与使用通过 Microsoft 批量许可计划许可的产品和服务有关的许可条款、条件和补充信息。
- **[许可条款](https://www.microsoft.com/licensing/product-licensing/)** – 本页中的资源定义您通过 Microsoft 商业许可计划购买的软件和在线服务的条款和条件。
- **[Microsoft 生命周期策略](/lifecycle/)** – 此页面提供产品整个生命周期中支持可用性的一致且可预测的指南。
- **[许可指南](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – 本指南用于详细了解如何许可 Dynamics 365。
- **[客户支持](https://dynamics.microsoft.com/support/)** – 获取针对 Dynamics 365 应用的行业领先支持。
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – 管理您的应用程序生命周期，以及向可预测、可重复的高质量实现努力。
- **[Dynamics 365 实施指南](https://aka.ms/D365ImplementationGuideFlip)** - Dynamics 365 实施指南记录了久经考验的 Success by Design 原则，为架构、构建、测试和部署 Dynamics 365 解决方案提供说明性指导。

## <a name="definitions"></a>定义

### <a name="azure-region"></a>[Azure 区域](/azure/availability-zones/az-overview#regions)

有一个或多个 Azure 数据中心的地理区域。 例如，美国和欧洲。

### <a name="business-process-modeler-bpm"></a>[业务流程建模器 (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

LCS 中的一款工具通过使用财务和运营应用内支持的美国生产力与质量中心 (APQC) 业务流程定义完成对给定实施的填补差距分析。

### <a name="cloud-solution-provider"></a>云解决方案提供商

Microsoft 云解决方案提供商 (CSP) 计划中的一个合作伙伴，该合作伙伴为客户提供增值云服务、支持、一张发票和大规模客户管理。

### <a name="customer"></a>客户

使用财务和运营应用并由 Office 365 中的租户表示的业务实体。

### <a name="development-environment"></a>开发环境

用于开发扩展的非生产沙盒环境。 客户从 LCS 将此环境部署到自己的 Azure 订阅。 此环境还可用于演示、培训或其他测试任务。 也称为[第 1 层沙盒](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher)。

### <a name="downtime"></a>停机时间

根据 Microsoft 通过自动化运行状况监视和系统日志，未到期平台或服务基础结构中发生故障导致用户无法登录或访问其有效租户的期间。 停机时间不包括计划的停机时间，服务附加产品功能不可用，您修改服务导致无法访问服务，或超过了缩放单元容量的期间。

### <a name="implementation-partner"></a>实现合作伙伴

客户为了自定义、配置、实现和管理其财务和运营解决方案选择的合作伙伴。

### <a name="incident"></a>事件

客户在使用财务和运营服务时遇到并通过 LCS 为其提交票证的问题。

### <a name="microsoft-customer-support-services-css"></a>Microsoft 客户支持服务 (CSS)

致力于提供针对财务和运营应用的优质服务的 Microsoft 全球支持团队。

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

管理门户，用于对财务和运营应用进行从试用到实现，再到生产后产品管理和支持的生命周期管理。 有关详细信息，请参阅 [Lifecycle Services 资源](../../dev-itpro/lifecycle-services/lcs.md)。

### <a name="non-production-instance"></a>非生产实例

客户用于验证扩展和执行其他开发任务的以下任何服务实例：

- **沙盒第 1 层** – 开发人员实例（客户托管）
- **沙盒第 2 层** – 标准接受度测试实例
- **沙盒第 3-5 层** - 加载项沙盒

有关第 2 至 5 层的详细信息，请参阅[选择正确的第 2 层或更高环境](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment)。

### <a name="production-instance"></a>生产实例

客户用于管理其“实际”日常交易记录和业务流程的财务和运营环境。

### <a name="sandbox-environment"></a>沙盒环境

客户用于演示、培训、用户接受度测试、扩展验证和其他测试任务的非生产环境。

### <a name="service"></a>服务

财务和运营应用中包含的任何核心服务。

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoft 在线服务的服务级别协议 (SLA)

此 SLA 适用于 Microsoft 在线服务。 有关详细信息，请参阅[服务级别协议](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services)。

### <a name="service-update"></a>服务更新

Microsoft 通过服务更新始终如一地服务财务和运营环境。 客户根据业务需求制订自己的服务更新日历。 有关预览版的详细信息，请参阅 [One Version 服务更新](../../dev-itpro/lifecycle-services/oneversion-overview.md)。

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

此框架通过关键阶段的一系列评估系统地指导实施，以确保 Dynamics 365 解决方案的最佳体系结构、安全性、性能和用户体验。

### <a name="user"></a>用户

使用财务和运营环境的个人和与客户的租户关联的个人。
