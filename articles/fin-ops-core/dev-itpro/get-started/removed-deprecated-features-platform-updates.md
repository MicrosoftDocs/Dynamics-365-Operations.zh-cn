---
title: 已删除或已弃用的平台功能
description: 本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。
author: sericks007
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7bd5a64553afa04517633ed03d8bbd6077208c0b511d8fa131dc9a2849998708
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774401"
---
# <a name="removed-or-deprecated-platform-features"></a>已删除或已弃用的平台功能

[!include [banner](../includes/banner.md)]

本主题介绍已经或计划从 Finance and Operations 应用的平台更新中移除的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

[技术参考报告](/dynamics/s-e/global/axtechrefrep_61)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="feature-deprecation-notice-effective-may-2021"></a>功能弃用通知于 2021 年 5 月生效

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
| **影响的产品区域**         | Finance and Operations 应用|
| **部署选项**              | 云部署 - 影响 Microsoft 管理的生产环境以及第 2 层到第 5 层沙盒环境。 |
| **状态**                         | 此功能已删除。 |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.17 的平台更新


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
| **弃用/移除的原因** | 与 Dynamics AX 2012 Enterprise Portal (EP) 关联的元数据项目已弃用，因为 Finance and Operations 应用从未支持过 EP。 |
| **被另一个功能取代？**   | 不 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：计划在 2021 年 10 月的发行版本中删除所有 EP 代码。 |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.15 的平台更新

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 的 Internet Explorer 11 支持已弃用

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 所有|
| **状态**                         | 已弃用：2021 年 8 月之后将不再支持 Internet Explorer 11。|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio 加载项以应用元数据修补程序

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 在 2018 年 7 月版本 8.1 中引入的[一个版本](../../fin-ops/get-started/one-version.md)服务更新不再支持元数据修补程序。 |
| **被另一个功能取代？**   | 单独的元数据修补程序不适用于受支持的版本。 相反，将应用累积质量更新。 |
| **影响的产品区域**         | Visual Studio 加载项 |
| **部署选项**              | 开发虚拟机 |
| **状态**                         | 在版本 10.0.15 中，该加载项不再包含在 Visual Studio 工具中。 |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.14 的平台更新

### <a name="online-users-page"></a>联机用户页面 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 这是为以前的客户端/服务器体系结构构建的旧页面。 此页面上的信息并不总是准确的，这可能会造成混淆和误导。 |
| **被另一个功能取代？**   | 我们将在以后的更新中提供新页面。|
| **影响的产品区域**         | 系统管理 |
| **部署选项**              | 所有 |
| **状态**                         | 此窗体将在 2021 年 10 月前删除。   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.13 的平台更新


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS 报表属性中定义的自定义代码 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 通常，自定义代码优点有限，同时需要大量资源和计算来提供支持。 自定义代码主要由报表作者用来从自定义代码程序集调用公共方法。 但是，云托管服务不支持对 SSRS 报表的自定义程序集的引用。 |
| **被另一个功能取代？**   | 报表作者可以选择继续从任何文本框表达式引用公共 .NET API 来进行数学、转换和格式操作。 有关详细信息，请参阅[向报表添加代码 (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15)。  |
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
| **状态**                         | 在版本 10.0.13 中，新网格控件已正式推出，客户可以选择打开此功能。 新网格控件将在 2021 年 10 月版本中强制使用。 强制使用新网格控件后，将不再支持 **forceLegacyGrid()** API。 |

### <a name="personalization-without-saved-views"></a>无已保存视图的个性化 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 个性化子系统已全面改革，加入了已保存视图功能，因而具有更好的性能并提供更多功能。 |
| **被另一个功能取代？**   | 已保存的视图 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 在版本 10.0.13/平台更新 37 中，已保存视图功能已正式推出，客户可以选择打开此功能。 已保存视图功能将在 2021 年 10 月版本中强制使用。 |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.12 的平台更新

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>包含无效字段引用的网格或组控件窗体扩展

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 网格或组控件上的数据组属性用于自动显示字段组的所有字段。 通过扩展添加的网格或组控件可能包含不再在字段组中定义的字段，或者可能缺少在字段组中定义的字段。 这可能会导致运行时行为不一致。 Finance and Operations 应用版本 10.0.12 的平台更新现在将此问题归类为编译器 *警告*。 要解决此问题，请打开窗体扩展，然后保存它。
| **被另一个功能取代？**   | 在以后的更新中，此编译器警告将替换为编译器错误。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 在 Finance and Operations 应用版本 10.0.12 的平台更新中引入了编译器警告。 |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations 应用版本 10.0.11 的平台更新

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
| **弃用/移除的原因** | 表元数据定义中的字段组中可能包含无效的字段引用。 如果部署这些字段组，可能导致 Financial Reporting 和 Microsoft SQL Server Reporting Services (SSRS) 中发生运行时失败。 平台更新 23 引入了编译器 *警告*，从而解决了这个元数据问题。 Finance and Operations 应用版本 10.0.11 的平台更新将此问题归类为编译器 *错误*。<p>若要解决此问题，请按照以下步骤操作。</p><ol><li>删除表字段组定义中的无效字段引用。</li><li>重新编译。</li><li>确保解决了所有错误。</li></ol> |
| **被另一个功能取代？**   | 此编译器错误将永久替代编译器警告。  |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：在 Finance and Operations 应用版本 10.0.11 的平台更新中，此编译器警告已成为编译器错误。 |

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
| **被另一个功能取代？**   | 无 |
| **影响的产品区域**         | 申报 |
| **部署选项**              | 所有 |
| **状态**                         | 正在从服务中努力移除此功能。<br><br>现代客户端提供大量选项，用于生成其中包含自动生成的链接的视图，以便帮助您在应用程序中导航。 将为收件人推荐通过电子邮件发送，归档和打印的外部通信使用服务呈现的分页文档。 我们改进了直接在浏览器中预览文档的体验，可以直接访问本地打印机。 有关详细信息，请参阅[使用嵌入式查看器预览 PDF 文档](../analytics/preview-pdf-documents.md)。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../migration-upgrade/deprecated-features.md)。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
