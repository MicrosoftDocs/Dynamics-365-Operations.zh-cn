---
title: 已删除或弃用的平台功能
description: 本文介绍已经或计划从财务和运营应用的平台更新中删除的功能。
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6283e07b87dc169d3cbaa71a371839ab9b2d6150
ms.sourcegitcommit: ee13b854cbd52a3aa33e2449a296aed775862594
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2022
ms.locfileid: "9799028"
---
# <a name="removed-or-deprecated-platform-features"></a>已删除或弃用的平台功能

[!include [banner](../includes/banner.md)]

本文介绍已经或计划从财务和运营应用的平台更新中删除的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

[技术参考报告](/dynamics/s-e/global/axtechrefrep_61)中提供了有关财务和运营应用中的对象的详细信息。 可比较这些报告的不同版本，以了解财务和运营应用各版本中已更改或已删除的对象。

## <a name="feature-deprecation-effective-august-2022"></a>功能弃用从 2022 年 8 月开始生效

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>2022 年 8 月弃用了 Lifecycle Services (LCS) 功能

作为[统一 Dynamics，统一平台](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform)工作的一部分，以下 LCS 功能已被弃用。

| 功能名称 | 是否与 AX 2012 一起使用？ | 是否与财务和运营应用一起使用？ | 被另一个功能取代？ |
|--------------|--------------------|----------------------------------------|------------------------------|
| 通告 | 是 | 是 | 是：单个项目和环境页面上存在通知横幅。 |
| 配置管理器 | 是 | 否 | 否 |
| 崩溃和转储分析 | 是 | 否 | 否 |
| 反馈和 Bug | 是 | 是 | 否 |
| 我的预订 | 是 | 是 | 否 |
| Office 365 | 是 | 是 | 是：Azure Active Directory 或 Microsoft 管理员门户。 |
| 影响分析 | 否 | 是 | 否 |
| 总体经济影响估算器 | 否 | 是 | 否 |
| 服务请求 | 否 | 是 | 是：[自助服务部署](../deployment/infrastructure-stack.md) |
| SharePoint 集成 | 是 | 是 | 否 |
| 配置和数据管理器 | 否 | 是 | 否 |
| 流程数据包 | 否 | 是 | 是：[数据导入导出框架 (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| 环境升级 | 否 | 是 | 是：[One Version](../lifecycle-services/oneversion-overview.md) 服务更新可用。 |
| 基础架构估算器 | 是 | 否 | 否 |
| 许可证规模 | 是 | 否 | 否 |
| 使用情况分析器 | 是 | 否 | 否 |
| 定制分析 | 是 | 否 | 否 |
| 系统诊断 | 是 | 是 | 否 |
| 业务流程建模器 Visio 管理 | 是 | 是 | 否 |
| AX 2012 云环境管理 | 是 | 否 | 否 |
| RDFE Azure 连接器 | 是 | 是 | 否 |
| AX 2012 版本 | 是 | 否 | 否 |
| 存储在 LCS 存储中的工作项 | 是 | 是 | 否 |
| 修补程序请求 | 是 | 是 | 否 |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>传输层安全 (TLS) RSA 密码套件

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们将删除以下密码套件列表以符合我们当前的安全协议。<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **被另一个功能取代？**   | 从 2023 年 1 月开始，客户只能使用我们的 [标准密码套件](/power-platform/admin/server-cipher-tls-requirements)。 此更改将影响与我们的服务器通信的客户端和服务器，例如，这可能会影响不符合我们标准密码套件的第三方集成。 |
| **影响的产品区域**         | 财务和运营应用 |
| **部署选项**              | 云部署 |
| **Status**                         | 已弃用。 客户必须在 2023 年 1 月之前升级其服务器。 有关配置 TLS 密码套件顺序的详细信息，请参阅 [管理传输层安全性 (TLS)](/windows-server/security/tls/manage-tls)。  |


## <a name="feature-deprecation-effective-june-2022"></a>功能弃用从 2022 年 6 月开始生效

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>财务和运营 (Dynamics 365) 移动应用和移动平台 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们正在弃用财务和运营 (Dynamics 365) 移动应用和平台以合并到单个移动平台，即 Power Apps。 |
| **被另一个功能取代？**   | 是，可以通过 Power Platform 集成生成财务和运营应用数据的移动体验。 有关更多详细信息，请参阅[博客文章](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/)和[生成移动体验](../power-platform/build-mobile-experiences.md)。 |
| **影响的产品区域**         | 财务和运营应用 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用。 支持结束日期定为 2024 年 10 月。 |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.29 的平台更新

### <a name="panorama-tab-style"></a>全景选项卡样式

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 水平滚动页面与具有已知可用性和辅助功能问题的过期布局模式保持一致。  |
| **被另一个功能取代？**   | 否，但其他选项卡样式仍然可用。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用。 |


## <a name="feature-deprecation-effective-april-2022"></a>功能弃用从 2022 年 4 月开始生效

### <a name="xml-url-resolution-in-data-management"></a>数据管理中的 XML URL 解决方案 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们正在删除对 XML URL 解决方案的支持，因为此问题已被标识为潜在的安全漏洞。 这意味着将不再解析与 XML 文件关联的外部资源。  |
| **被另一个功能取代？**   | 否。 |
| **影响的产品区域**         | 财务和运营应用 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用。 |

## <a name="feature-deprecation-effective-march-14-2022"></a>功能弃用从 2022 年 3 月 14 日开始生效

### <a name="xslt-scripting-in-data-management"></a>数据管理中的 XSLT 脚本

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 数据管理中的 XSLT 脚本支持已被弃用，以改进财务和运营应用中的安全性和数据保护。  |
| **被另一个功能取代？**   | 否。 客户和 ISV 应考虑基于 X++ 语言重新实施其解决方案，以取代 XSLT 脚本。 |
| **影响的产品区域**         | 财务和运营应用 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用 <br><br>**异常：** 当前正在使用 XLST 脚本的客户。 在更新到版本 10.0.30 或更高版本之前可以继续使用它。 对于早期版本，异常将于 2023 年 1 月 31 日到期。 出现此异常的客户已在 Microsoft 365 管理中心内可用的消息中心收到了通知。 |

## <a name="feature-removal-effective-october-2021"></a>功能删除从 2021 年 10 月开始生效

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 中的 Microsoft Azure SQL 报表

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 所有活动和监视都将由平台通过自动化在内部执行。 不需要任何手动干预。|
| **被另一个功能取代？**   | 是的，现在有一个自动化系统，它使这些功能过时。 |
| **影响的产品区域**         | SQL 报表：当前 DTU、当前 DTU 详细信息、获取锁定详细信息、当前计划向导列表、获取查询 ID 列表、获取给定计划 ID 的 SQL 查询计划、获取查询计划和执行状态、获取限制配置、获取等待统计信息、列举最耗资源的查询 |
| **部署选项**              | 云部署：影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 已删除 |

### <a name="azure-sql-actions-in-lcs"></a>LCS 中的 Azure SQL 操作

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们将弃用 LCS 中的部分 SQL 操作。 所有活动和监视都将由平台通过自动化在内部执行。 不需要任何手动干预。 |
| **被另一个功能取代？**   | 是的，现在有一个自动化系统，它使这些功能过时。 |
| **影响的产品区域**         | SQL 操作：创建计划指南以强制使用计划 ID，创建计划指南以添加表提示，删除计划指南，禁用/启用页面锁和锁升级，更新表中的统计信息，重建索引，创建索引 |
| **部署选项**              | 云部署：影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 已删除 |


## <a name="feature-deprecation-effective-october-2021"></a>功能弃用从 2021 年 10 月开始生效

### <a name="show-related-document-attachments-feature"></a>“显示相关文档附件”功能

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 此功能返回意外结果。 |
| **被另一个功能取代？**   | 否。 与此功能相关的任何进一步计划都将通过我们的标准发布波次披露流程传达。 |
| **影响的产品区域**         | Web 客户端 - 文档附件体验 |
| **部署选项**              | 全部 |
| **Status**                         | 已弃用  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.23 的平台更新

### <a name="ondbsynchronize-event"></a>OnDBSynchronize 事件

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 没有用于执行此事件的控件。 |
| **被另一个功能取代？**   | 是的，将通过 **OnDBSynchronize** 事件订阅的现有方法移到 SysSetup 扩展类。 |
| **影响的产品区域**         | 数据库同步 |
| **部署选项**              | 全部 |
| **状态**                         | 已弃用。 计划删除日期为 2022 年 10 月。 |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 添加通知时，Microsoft 需要其他参数。 |
| **被另一个功能取代？**   | 是的，**SystemNotificationsManager.AddSystemNotification()** API。 此 API 需要您为生成的通知明确设置 ExpirationDateTime 和 RuleID。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 全部 |
| **状态**                         | 已弃用。 计划删除日期为 2023 年 4 月。 |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.21 的平台更新

### <a name="skype-for-business-online-support"></a>Skype for Business Online 支持

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | Skype for Business Online 已停用。 有关详细信息，请参阅 [Skype for Business Online 服务已停用](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601)。 |
| **被另一个功能取代？**   | 目前不会，但将来我们可能会考虑从 Teams 中添加状态。|
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 全部 |
| **状态**                         | 已弃用。 从版本 10.0.21 开始已关闭了 **已启用 Skype** 设置。 删除此设置的目标日期定于 2022 年 4 月；但是，在 Skype 团队关闭服务后，该功能将停止运行。 |
 
## <a name="feature-deprecation-effective-august-2021"></a>功能弃用从 2021 年 8 月开始生效

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 中的 Microsoft Azure SQL 报表

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 所有活动和监视都将由平台通过自动化在内部执行。 不需要任何手动干预。|
| **被另一个功能取代？**   | 是的，现在有一个自动化系统，它使这些功能过时。 |
| **影响的产品区域**         | SQL 报表：当前 DTU、当前 DTU 详细信息、获取锁定详细信息、当前计划向导列表、获取查询 ID 列表、获取给定计划 ID 的 SQL 查询计划、获取查询计划和执行状态、获取限制配置、获取等待统计信息、列举最耗资源的查询 |
| **部署选项**              | 云部署：影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 已弃用：计划删除日期为 2021 年 10 月。 |

### <a name="azure-sql-actions-in-lcs"></a>LCS 中的 Azure SQL 操作

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们将弃用 LCS 中的部分 SQL 操作。 所有活动和监视都将由平台通过自动化在内部执行。 不需要任何手动干预。 |
| **被另一个功能取代？**   | 是的，现在有一个自动化系统，它使这些功能过时。 |
| **影响的产品区域**         | SQL 操作：创建计划指南以强制使用计划 ID，创建计划指南以添加表提示，删除计划指南，禁用/启用页面锁和锁升级，更新表中的统计信息，重建索引，创建索引 |
| **部署选项**              | 云部署：影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 已弃用：计划删除日期为 2021 年 10 月。 |

## <a name="feature-deprecation-effective-may-2021"></a>功能弃用从 2021 年 5 月开始生效

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 中的全球化门户

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 我们正在弃用 LCS 中的全球化门户，因为此功能已被其他基于 LCS 的服务取代。 |
| **被另一个功能取代？**   | 是的，此功能已被 LCS [问题搜索](../lifecycle-services/issue-search-lcs.md)和[动态监管预警提交服务](../lcs-solutions/submit-localization-alerts.md)取代。 |
| **影响的产品区域**         | LCS 中的全球化门户|
| **部署选项**              | 云部署 |
| **状态**                         | 已弃用：计划删除日期为 2022 年 5 月。 |


## <a name="feature-removed-effective-january-28-2021"></a>功能已删除，自 2021 年 1 月 28 日起生效

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>用于处理 SQL 索引碎片整理的批处理作业

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 为了减少客户操作、监视和维护索引管理的开销，此功能已被删除。 |
| **被另一个功能取代？**   | 在以后，索引维护将由 Microsoft 服务执行。 这会连续进行，不会影响用户的工作负荷。 |
| **影响的产品区域**         | 财务和运营应用|
| **部署选项**              | 云部署 - 影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 此功能已删除。 |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.17 的平台更新


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 为了支持 Visual Studio 的最新版本，必须对 Visual Studio 的 X++ 扩展进行一些更改。 这些更改与 Visual Studio 2015 不兼容。 |
| **被另一个功能取代？**   | Visual Studio 2017 将取代 Visual Studio 2015 成为已部署的必需版本。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：更新后，以前的 X++ 工具将从 Visual Studio 2015 中删除，更新后的工具不会安装在 Visual Studio 2015 中。 对托管版本没有影响。 对于构建虚拟机，需要手动更新构建管道（构建定义），以将依赖性从 MSBuild 14.0 (Visual Studio 2015) 更改为 MSBuild 15.0 (Visual Studio 2017)，如[更新 Azure Pipelines 中的旧管道](../dev-tools/pipeline-msbuild-update.md)中所述。 |

### <a name="user-avatar"></a>用户头像 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 显示在导航栏右侧的用户头像使用 Dynamics 365 标头控件中的 API 检索，这已被弃用。 |
| **被另一个功能取代？**   | 用户会在导航栏中看到他们的首字母在一个圆圈内。 这与开发计算机上当前使用的视觉对象相同。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 从版本 10.0.17 开始已删除 |

### <a name="enterprise-portal-ep-deprecation"></a>Enterprise Portal (EP) 弃用  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 与 Dynamics AX 2012 Enterprise Portal (EP) 关联的元数据项目已弃用，因为财务和运营应用从未支持过 EP。 |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：计划在 2021 年 10 月的发行版本中删除所有 EP 代码。 |

## <a name="deprecation-effective-december-2020"></a>从 2020 年 12 月起弃用

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 的 Internet Explorer 11 支持已弃用

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品和 Dynamics Lifecycle Services (LCS) 的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响使用 Dynamics 365 产品和 LCS 设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品和 LCS 将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品和 LCS |
| **部署选项**              | 所有|
| **Status**                         | 已弃用：2021 年 8 月之后将不再支持 Internet Explorer 11。|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.15 的平台更新

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio 加载项以应用元数据修补程序

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 在 2018 年 7 月版本 8.1 中引入的[一个版本](../../fin-ops/get-started/one-version.md)服务更新不再支持元数据修补程序。 |
| **被另一个功能取代？**   | 单独的元数据修补程序不适用于受支持的版本。 相反，将应用累积质量更新。 |
| **影响的产品区域**         | Visual Studio 加载项 |
| **部署选项**              | 开发虚拟机 |
| **状态**                         | 在版本 10.0.15 中，该加载项不再包含在 Visual Studio 工具中。 |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.14 的平台更新

### <a name="online-users-page"></a>联机用户页面 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 这是为以前的客户端/服务器体系结构构建的旧页面。 此页面上的信息并不总是准确的，这可能会造成混淆和误导。 |
| **被另一个功能取代？**   | 我们将在以后的更新中提供新页面。|
| **影响的产品区域**         | 系统管理 |
| **部署选项**              | 所有 |
| **状态**                         | 此窗体将在 2021 年 10 月前删除。   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.13 的平台更新


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS 报表属性中定义的自定义代码 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 通常，自定义代码优点有限，同时需要大量资源和计算来提供支持。 自定义代码主要由报表作者用来从自定义代码程序集调用公共方法。 但是，云托管服务不支持对 SSRS 报表的自定义程序集的引用。 |
| **被另一个功能取代？**   | 报表作者可以选择继续从任何文本框表达式引用公共 .NET API 来进行数学、转换和格式操作。 有关详细信息，请参阅[向报表添加代码 (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs)。  |
| **影响的产品区域**         | RDL 中定义的包含自定义代码的应用程序报表设计的子集。 |
| **部署选项**              | 所有 |
| **状态**                         | 在版本 10.0.13 中，编译器将开始针对在 SSRS 报表定义中检测到自定义代码的实例发出警告。 要解决此问题，打开报表设计定义，删除所有自定义代码项目。 在以后的更新中，此警告将替换为编译器错误。   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>升级三个 jQuery 组件库 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 三个 jQuery 组件库正在更新，以进行安全修复和维护货币。   
| **被另一个功能取代？**   | 以下库会受到影响：jQuery（从版本 2.1.4 到版本 3.5.0），jQuery UI（从版本 1.11.4 到版本 1.12.1），jQuery qTip（从版本 2.2.1 到版本 3.0.3）。 迁移指南已由 jQuery 在线提供。  |
| **影响的产品区域**         | 可扩展控件，特别是使用已弃用或已删除 API 的自定义 JavaScript 代码 |
| **部署选项**              | 所有 |
| **状态**                         | 使用版本 10.0.13/平台更新 37，客户可以通过启用“升级三个 jQuery 组件库”功能来有选择地迁移到最新库。 2021 年 4 月版本将必须迁移到新库以为迁移到受影响的 API 留下时间。   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>现有网格控件/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 现有网格控件由新网格控件替换。 |
| **被另一个功能取代？**   | [新网格控件](../..//fin-ops/get-started/grid-capabilities.md) |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 在版本 10.0.13 中，新网格控件已正式推出，客户可以选择打开此功能。 新网格控件将在 2021 年 10 月版本中默认启用，目前计划在 2022 年 4 月强制使用。 强制使用新网格控件后，将不再支持 **forceLegacyGrid()** API。 |

### <a name="personalization-without-saved-views"></a>无已保存视图的个性化 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 个性化子系统已全面改革，加入了已保存视图功能，因而具有更好的性能并提供更多功能。 |
| **被另一个功能取代？**   | 已保存的视图 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 在版本 10.0.13/平台更新 37 中，已保存视图功能已正式推出，客户可以选择打开此功能。 已保存视图功能将在 2021 年 10 月版本中强制使用。 |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.12 的平台更新

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>包含无效字段引用的网格或组控件窗体扩展

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 网格或组控件上的数据组属性用于自动显示字段组的所有字段。 通过扩展添加的网格或组控件可能包含不再在字段组中定义的字段，或者可能缺少在字段组中定义的字段。 这可能会导致运行时行为不一致。 财务和运营应用版本 10.0.12 的平台更新现在将此问题归类为编译器 *警告*。 要解决此问题，请打开窗体扩展，然后保存它。
| **被另一个功能取代？**   | 在以后的更新中，此编译器警告将替换为编译器错误。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 在财务和运营应用版本 10.0.12 的平台更新中引入了编译器警告。 |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>财务和运营应用版本 10.0.11 的平台更新

### <a name="explicit-safe-lists-for-self-service-environments"></a>自助服务环境的显式安全列表

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 将 IP 移至安全列表的流程已更改。 自助服务不再支持 IP 安全列表。 |
| **被另一个功能取代？**   | 有关详细信息，请参阅[配置 Azure Active Directory 条件访问](/appcenter/general/configuring-aad-conditional-access)。|
| **影响的产品区域**         | 安全性 |
| **部署选项**              | 云 |
| **状态**                         | 已弃用：自助服务部署已完全弃用此功能。 |

### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 为了支持 Visual Studio 的最新版本，必须对 Visual Studio 的 X++ 扩展进行一些更改。 这些更改与 Visual Studio 2015 不兼容。 |
| **被另一个功能取代？**   | Visual Studio 2017 将取代 Visual Studio 2015 成为已部署的必需版本。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 版本 10.0.13（平台更新 37）或更高版本中部署的虚拟机中包含 Visual Studio 2017。 版本 10.0.16（平台更新 40）是最后一个支持 Visual Studio 2015 的发行版。 仅具有 Visual Studio 2015 的虚拟机不能更新到版本 10.0.17（平台更新 41）。 |

### <a name="field-groups-containing-invalid-field-references"></a>其中包含无效字段引用的字段组

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 表元数据定义中的字段组中可能包含无效的字段引用。 如果部署这些字段组，可能导致 Financial Reporting 和 Microsoft SQL Server Reporting Services (SSRS) 中发生运行时失败。 平台更新 23 引入了编译器 *警告*，从而解决了这个元数据问题。 财务和运营应用版本 10.0.11 的平台更新将此问题归类为编译器 *错误*。<p>若要解决此问题，请按照以下步骤操作。</p><ol><li>删除表字段组定义中的无效字段引用。</li><li>重新编译。</li><li>确保解决了所有错误。</li></ol> |
| **被另一个功能取代？**   | 此编译器错误将永久替代编译器警告。  |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：在财务和运营应用版本 10.0.11 的平台更新中，编译器警告是一个编译器错误。 |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>使用 SHA1 哈希算法创建的 ISV 许可证

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 已经改变了独立软件供应商 (ISV) 许可证的创建方法。 有关详细信息，请参阅[独立软件供应商 (ISV) 许可](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes)。 |
| **被另一个功能取代？**   | 是。 使用 Windows PowerShell 创建许可证。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：使用 SHA1 哈希算法创建的 ISV 许可证。 此算法依赖于使用 MakeCert 实用程序创建的证书，但现在已弃用了该实用程序。<br><br>已弃用：SHA1 用于安全或哈希用途。 SHA1 将于 2021 年年初停止工作。 因此不应再使用它。<br><br>已去除：对传输层安全 (TLS) 1.0 和 TLS 1.1 传入或传出请求的支持。 |

## <a name="platform-update-32"></a>平台 update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>“工作流请求更改”对话框中不再包含用户选择下拉列表

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 这是一个安全问题，因为可能会将更改请求发送给非预期用户。 这也是一个可用性问题，因为它会强制用户确定工作流发起者是谁和谁手动选择它们。  |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 工作流 |
| **部署选项**              | 所有 |
| **状态**                         | 已从平台更新 32 中的请求更改对话框内删除了用户选择下拉列表。 将把请求更改请求正常自动发送到发起者。 有关此功能的详细信息，请参阅[工作流审核流程中的操作](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change)。 |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>云托管服务呈现的分页文档中将不再支持嵌入式钻取链接 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 服务呈现的文档中嵌入的导航 URL 中可能包含敏感的业务数据。 我们将取消对文档中的嵌入式钻取链接的支持，这是我们为了进一步保护客户的数据采取的安全预防措施。 此项更改还将让用户在以交互方式生成文档时可以享受性能提升。  |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 申报 |
| **部署选项**              | 所有 |
| **状态**                         | 正在从服务中努力移除此功能。<br><br>现代客户端提供大量选项，用于生成其中包含自动生成的链接的视图，以便帮助您在应用程序中导航。 将为收件人推荐通过电子邮件发送，归档和打印的外部通信使用服务呈现的分页文档。 我们改进了直接在浏览器中预览文档的体验，可以直接访问本地打印机。 有关详细信息，请参阅[使用嵌入式查看器预览 PDF 文档](../analytics/preview-pdf-documents.md)。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

