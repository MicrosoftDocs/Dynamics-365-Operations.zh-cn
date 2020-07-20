---
title: 先前版本中已删除或弃用的功能
description: 此主题介绍从 Dynamics 365 for Finance and Operations 和该产品的早期版本已经删除或曾经计划删除的功能。
author: sericks007
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a73231a8286a412e9ec8a4eef6c58d7afd73ec0
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500404"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>先前版本中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 此主题不再更新。 若要查看已经从 Finance and Operations 应用删除或弃用的功能的当前列表，请搜索与您在使用的应用有关的**已删除或弃用的功能**内容。

此主题介绍从 Dynamics 365 for Finance and Operations 和该产品的早期版本已经删除或弃用的功能。

- *已移除*的功能在产品中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

[技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="finance-1007-with-platform-update-31"></a>带平台更新 31 的 Finance 10.0.7

### <a name="chinese-voucher-types-without-account-groups-selection"></a>不带帐户组选择的中国凭证类型
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 更改为带帐户组选择的功能。 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。 在“10.0.7 的新增功能”中查找有关新功能设计的更多详细信息 |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>带平台更新 30 的 Finance and Operations 10.0.6


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Windows 即将弃用 SHA1，如 [SHA1 证书的 Windows 执行](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)中所述。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 4 月 1 日，开发人员必须使用新 API。 |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(string message)

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Windows 即将弃用 SHA1，如 [SHA1 证书的 Windows 执行](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)中所述。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 平台 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 4 月 1 日，开发人员必须使用新 API。 |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 我们正在停用 **setUtcString()** 方法，因为可以使用更好的替换方法。 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 平台 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 10 月 1 日，我们计划不再支持 **setUtcString()** 方法。 开发人员应改用 **setUtcDateTime()** 方法。 |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>黑名单报告 (IT) – 功能引用 IT-00001

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 非法律要求。 |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 意大利本地化 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 10 月 1 日，我们计划不再支持 **黑名单报告 (IT) – 功能引用 IT-00001**。 |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>国内税报表 – 功能引用 IT-00003

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 非法律要求。 |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 意大利本地化 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 10 月 1 日，我们计划不再支持 **国内税报表 (IT) – 功能引用 IT-00003**。 |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>带平台更新 29 的 Finance and Operations 10.0.5

### <a name="us-payroll-tax-updates"></a>美国工资单税更新

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 我们停止了美国工资单税更新功能，原因是使用率低，并且现在通过战略集成提供增强功能。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 工资单 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：我们计划从 2021 年 10 月 1 日开始不再向美国工资单客户提供税更新。 此功能将留在产品中，但是不再通过增强让此功能保持最新，并且将根据具体案例评估所有产品瑕疵。 有关详细信息，请参阅 [Microsoft Dynamics 365 for Finance and Operations 中的美国工资单功能将停止税更新](https://aka.ms/financepayrollfaq)。 |


### <a name="data-management-staging-clean-up"></a>清除数据管理暂存
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 不满足安排定期清理所需核心要求。 |
| **被另一个功能取代？**   | 是，将增加作业历史记录清理功能以全面满足方案的要求。 |
| **影响的产品区域**         | 数据管理 |
| **部署选项**              | 所有  |
| **状态**                         | 已弃用：移除功能的目标时间范围为 2020 年 12 月。 |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>带平台更新 28 的 Finance and Operations 10.0.4

### <a name="france-fec-accounting-data-export-in-xml"></a>法国：以 XML 格式导出 FEC 会计数据

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | **法国 FEC 审计文件**已替换为 TXT 格式，可以从**总帐** \> **定期任务** \> **数据导出**访问。
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 总帐 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用。 移除功能的目标时间范围为 2020 年 7 月。 |


### <a name="legacy-navigation-bar"></a>旧导航栏

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 标题与其他 Dynamics and Office 产品对齐 有关更多详细信息，请参阅[更新后的导航栏与 Office 标题对齐](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar)。
| **被另一个功能取代？**   | 从平台更新 24 开始，引入了具有搜索功能且样式已改变的导航栏。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 2020 年 4 月开始，将不再提供原来的导航栏。 在此之前，客户可以通过**客户端性能选项**页恢复为旧导航栏。 |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>带平台更新 26 的 Finance and Operations 10.0.2


### <a name="legacy-default-action-behavior"></a>旧版默认操作行为

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 通过个性化为网格列重新排序之后，网格中的默认操作的旧版行为生成具有默认操作链接的意外列。 新的粘滞默认操作功能对此进行了更正。 有关更多详细信息，请参阅[网格中的粘滞默认操作](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action)。 |
| **被另一个功能取代？**   | 从平台更新 21 开始，为“粘滞默认操作”引入了一项功能。 可在**客户端性能选项**页面中启用此功能。 |
| **影响的产品区域**         | Web 客户端中的网格 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 2020 年 4 月开始，粘滞默认操作将成为默认行为，但没有恢复为旧版行为的机制。 |

### <a name="legacy-is-one-of-filtering-experience"></a>旧版“之一”筛选体验

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 在平台更新 22 中，“之一”筛选体验已经过重新设计，并计划此体验最终成为唯一的“之一”筛选体验。 |
| **被另一个功能取代？**   | 从平台更新 22 开始，**客户端性能选项**页面中提供经过改进的“之一”筛选体验。 有关详细信息，请参阅[优化的“之一”筛选体验](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering)。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 2020 年 4 月开始，经过改进的“之一”体验将成为默认行为，但没有恢复为旧版行为的机制。 |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>用于启用包含多个项目合同融资来源的销售订单的参数
将使用**项目管理参数**设置**允许项目的销售订单具有多个融资来源**启用对创建其中的项目合同具有多个融资来源的且基于项目的销售订单的支持。 默认情况下，不启用此参数。 

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 删除此参数之后，将始终启用此功能。 |
| **被另一个功能取代？**   | 编号 将始终启用用于支持具有多个融资来源且基于项目的销售订单的功能。   |
| **影响的产品区域**         |将删除**允许项目的销售订单具有多个融资来源**参数。 如果删除此选项，将修改以下方法：**ProjStatusType** 类中的 **ctrlSalesOrderTable** 方法、**ProjId** 字段的 **validate** 方法，以及 **SalescreateOrder** 窗体中的 **run** 方法。 如果删除了此参数，将废弃以下方法：**ProjTable** 表文件中的 **IsSalesOrderAllowedForMultipleFundingSources**、**ProjTable** 表文件中的 **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** 方法、**ProjParameters** 窗体和 **ProjParameterEntity** 文件中的 **AllowSalesOrdersForMultipleFundingSources** 数据字段，以及 **ProjTable** 表文件中的 **IsAssociatedToMultipleFundingSourcesContract** 专用方法。 |
| **部署选项**              | 所有  |
| **状态**                         | 计划 2020 年 4 月的发布波次将弃用。 |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>跟踪和实例状态的旧版工作流报告

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 将弃用跟踪和实例状态的旧版工作流报告，因为导航时不再参考这些报告。 报告名为 WorkflowWorkflowInstanceByStatusReport 和 WorkflowWorkflowTrackingReport。 |
| **被另一个功能取代？**   | 可改用工作流历史记录窗体。 |
| **影响的产品区域**         | Web 客户端 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：移除功能的目标时间范围为 2020 年 4 月。 |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>带平台更新 25 的 Finance and Operations 10.0.1

### <a name="deprecated-apis-and-potential-breaking-changes"></a>已弃用的 API 和可能的突破性更改


#### <a name="deriving-from-internal-classes-is-deprecated"></a>已弃用从内部类派生

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 在平台更新 25 之前，可创建派生自另一个包/模块内定义的内部类/表的类或表。 这种编码行为不安全。 从平台更新 25 开始，编译器将显示警告。 |
| **被另一个功能取代？**   | 在平台更新 26 中，此编译器警告将替换为错误。 此更改是为了在运行时向后兼容，这意味着平台更新 25 或更高版本可以在任何沙盒或生产环境中部署，不需要修改自定义代码。 此更改仅影响开发和编译时间。|
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：在平台更新 26 中，此警告将成为编译错误。 |

#### <a name="overriding-internal-methods-is-deprecated"></a>已弃用替代内部方法。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 在平台更新 25 之前，可替代另一个包/模块内定义的派生类中的内部方法。 这种编码行为不安全。 从平台更新 25 开始，编译器将显示警告。 |
| **被另一个功能取代？**   | 在平台更新 26 中，此警告将替换为编译器错误。 此更改是为了在运行时向后兼容，这意味着平台更新 25 或更高版本可以在任何沙盒或生产环境中部署，不需要修改自定义代码。 此更改仅影响开发和编译时间。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：在平台更新 26 中，此警告将成为编译错误。 |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>带平台更新 24 的 Finance and Operations 10.0.0

### <a name="renaming-released-products"></a>重命名已发布产品 
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 使用**对主键进行重命名**功能更改已发布产品的 ItemId 时，将仅更新外键直接引用。 对已发布产品的其他所有引用都将保留旧 ItemId。 因此，将导致数据不一致，最终阻止业务流程。 |
| **被另一个功能取代？**   | 编号 |
| **影响的产品区域**         | 产品信息管理 |
| **部署选项**              | 所有  |
| **状态**                         | 已从带平台更新 24 的 Finance and Operations 10.0.0 开始移除。|


## <a name="finance-and-operations-813-with-platform-update-23"></a>带平台更新 23 的 Finance and Operations 8.1.3

### <a name="sql-server-reporting-services-reportviewer-control"></a>SQL Server Reporting Services ReportViewer 控件
客户可使用嵌入的 SQL Server Reporting Services (SSRS) ReportViewer 控件提供的**导出**操作下载 Finance and Operations 应用程序生成的单据。 这种基于 HTML 的报表表示为用户提供不分页的单据预览。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 基于 HTML 的预览体验的不分页特征**不能**提供 Finance and Operations 最终生成的单据实体的逼真感。 用户可通过完全接纳 PDF 充当业务文档的标准格式，在生成应用程序报告时通过改进的性能利用现代查看体验。 |
| **被另一个功能取代？**   | 在以后，PDF 单据将成为 Finance and Operations 呈现的报表的默认格式。   |
| **影响的产品区域**         | 此更改**不**影响以电子方式分发报表或将报表直接发送到打印机的客户场景。    |
| **部署选项**              | 所有  |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 按照计划，2019 年 5 月的平台更新将使用嵌入的 PDF 查看器自动预览应用程序报告。 |

### <a name="client-kpi-controls"></a>客户端 KPI 控件
开发人员可以在 Visual Studio 中为嵌入式关键绩效指标 (KPI) 建模，并由最终用户进一步自定义。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 很少客户采用用于定义 KPI 的本机客户端控件，此类控件依赖开发人员增加可跟踪的度量。 |
| **被另一个功能取代？**   | PowerBI.com 服务提供世界级的工具，用于基于外部源的数据定义和管理 KPI。  在即将推出的版本中，计划让您可以将 PowerBI.com 中托管的解决方案嵌入到应用程序工作空间中。   |
| **影响的产品区域**         | 此更改将阻止开发人员在 Visual Studio 设计器中引入新的 KPI 控件。    |
| **部署选项**              | 所有  |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="deprecated-apis-and-future-breaking-changes"></a>已弃用的 API 和将来的突破性更改

#### <a name="field-groups-containing-invalid-field-references"></a>其中包含无效字段引用的字段组

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 表元数据定义中可以有包含无效字段引用的字段组。 如果部署，可能导致 Financial Reporting 和 SQL Server Reporting Services (SSRS) 中发生运行时失败。 此问题目前归类为*编译器警告*，而不是*错误*，这意味着可以在不解决此问题的情况下继续创建和部署可部署包。 要解决此问题，请执行以下操作：<br><br>1. 删除表字段组定义中的无效字段引用。<br><br>2. 重新编译。<br><br>3. 确保解决所有警告或错误。 |
| **被另一个功能取代？**   | 以后此警告将替换为编译器错误。 |
| **影响的产品区域**         | Visual Studio 开发工具 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：在 Finance and Operations 应用版本 10.0.11 的平台更新中，此警告已成为编译时错误。 |

#### <a name="complete-list"></a>完整列表
若要访问将弃用的 API 的完整列表，请参阅[弃用方法和元数据元素](deprecation-deletion-apis.md)。

## <a name="finance-and-operations-81-with-platform-update-20"></a>带平台更新 20 的 Finance and Operations 8.1

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>子分类日记帐科目分录的批处理转移规则
总帐参数中已弃用了同步转移模式。  此模式刚被异步和计划批处理，后者表示为转移选项。 有关更多信息，请参阅[总帐参数 – 批量转移规则](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules)博客。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 因为对系统存在影响，我们将移除同步选项。 |
| **被另一个功能取代？**   | 异步和计划批处理选项取代了同步。   |
| **影响的产品区域**         | 总帐、应付帐款、应收帐款、采购、支出    |
| **部署选项**              | 所有  |
| **状态**                         | 已弃用：移除功能的目标时间范围为 10.0 版本。|

### <a name="electronic-reporting-for-russia"></a>俄罗斯的电子报告格式
用于配置申报的 .txt 和 .xml 文件格式的功能。 

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 已被电子申报取代。 |
| **被另一个功能取代？**   | 是。 |
| **影响的产品区域**         | 总帐 |
| **部署选项**              | 所有 |
| **状态**                         | 已从带平台更新 20 的 Finance and Operations 8.1 开始移除。 |

### <a name="financial-reports-generator-for-russia"></a>俄罗斯的财务报表生成器
用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。 功能部件：已移除了将数据导出到 XLS 和 DOC 报表模板、查询和固定必备项这一功能。 

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 移除的部件已被电子申报取代。 |
| **被另一个功能取代？**   | 是。 应使用财务报表设置用户界面按总帐科目和税务登记簿设置数据收集规则。 应在电子申报中配置将数据导出到各种文件类型、固定必备项和类似查询的数据收集规则。 |
| **影响的产品区域**         | 总帐。 |
| **部署选项**              | 所有 |
| **状态**                         | 已从带平台更新 20 的 Finance and Operations 8.1 开始移除。 |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>俄罗斯的与外部提供商集成以通过通信通道发送电子报告
用于将生成的电子版申报文件导出到文件夹以进一步发送给正式的电子申报提供商和导入回状态的功能。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 已被电子消息可配置功能取代。 |
| **被另一个功能取代？**   | 是。  |
| **影响的产品区域**         | 总帐、税务 |
| **部署选项**              | 所有 |
| **状态**                         | 已从带平台更新 20 的 Finance and Operations 8.1 开始移除。 |


### <a name="profit-tax-register-wizard"></a>利润税登记向导
为新利润税登记创建模板的功能。 此功能为新登记创建 X++ 对象，其然后被创建为添加了适当的计算逻辑的模板。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 功能与 Finance and Operations 延伸性模型不兼容。 |
| **被另一个功能取代？**   | 无 |
| **影响的产品区域**         | 税金 |
| **部署选项**              | 所有 |
| **状态**                         | 已从带平台更新 20 的 Finance and Operations 8.1 开始移除。 |


## <a name="finance-and-operations-80-with-platform-update-15"></a>带平台更新 15 的 Finance and Operations 8.0
此版本中未移除或弃用任何功能。 平台更新 15 是累积功能，其中包含平台更新 13、14 和 15 中的新增功能或更改功能。

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>具有平台更新 12 的 Finance and Operations Enterprise edition 7.3

### <a name="personalized-product-recommendations"></a>个性化产品建议 
从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。 有关详细信息，请参阅[产品建议概览](../../../commerce/product-recommendations.md)。  

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。  |
| **被另一个功能取代？**   | 编号 但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。   |
| **影响的产品区域**         | POS 中的个性化产品建议。                                                    |
| **部署选项**              | 全部                                                                                      |
| **状态**                         |从 2018 年 2 月 15 日开始移除。 这将影响运行 Dynamics 365 for Operations 1611 及更高版本的客户。  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>电子申报 (ER) 功能列表扩展
可以引入在 ER 表达式生成器中使用的自定义功能（有关详细信息，请参阅[扩展电子申报 (ER) 功能列表](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)）的这一特性不再受支持。 由于 ER API 发生变更，从 ER 表达式生成器调用内置函数的 API 变成内部 API，并且无法再进行扩展。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 代码密封计划  |
| **被另一个功能取代？**   | 无。 每当需要一个新的内置函数时，必须向 ER 框架团队提交新扩展请求。<br><br>在 ER 团队开发请求的函数时，作为临时解决方案，可以将需要的逻辑作为一种自定义应用程序类方法进行编程。 此方法可以作为引用该自定义应用程序类的**应用程序\类**类型的已添加 ER 数据源的属性在 ER 表达式中访问。  |
| **影响的产品区域**         | 电子申报框架                                                      |
| **部署选项**              | 所有                                                                                      |
| **状态**                         | 从 Finance and Operations Enterprise edition 7.3 开始移除。    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>按物料组的库存和按库存维度的库存帐龄分析表

这两个分析表在 Finance and Operations 中不再受支持。 相反，可使用**库存帐龄**分析表改善用户体验。

|   |  |
|--------------|-----------------------|
| **折旧的原因**       | 重复的功能  |
| **被另一个功能取代？** | 是。 这两个分析表已替换为**库存帐龄**分析表。     |
| **影响的产品区域**       | 库存管理、成本管理        |
| **部署选项**        | 全部|
| **状态**                       | 已弃用：两个分析表的菜单项在版本 7.3 中已移除。 但这些分析表的代码仍然保留在产品中。 在将来的发行中计划移除该代码。 |

### <a name="power-bi-content-packs-available-on-appsource"></a>AppSource 中的 Power BI 内容包
[Microsoft AppSource](https://appsource.microsoft.com) 站点上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包因为 Microsoft Power BI 中的产品更新而被弃用。 过去将这些内容包部署到 PowerBI.com 的系统管理窗体在 Finance and Operations 中也被弃用。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Microsoft Power BI 中进行产品更新。 |
| **被另一个功能取代？**   | [AppSource](https://appsource.microsoft.com) 站点上提供的**成本管理**、**财务绩效**和**零售渠道绩效**内容包将被分析应用程序替代，以便在数据库级别集成解决方案。 有关分析应用程序的详细信息，请参阅[工作区中的嵌入式 Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md)。    |
| **影响的产品区域**         | 成本管理、财务和零售                                                                                               |
| **部署选项**              | 仅适用于云（在本地部署中不再支持与 PowerBI.com 集成）。                                                                                                            |
| **状态**                         | 已弃用：移除功能的目标时间范围为 2018 年第二季度。    |

### <a name="standard-ui-in-data-management-workspace"></a>数据管理工作区中的标准 UI

数据管理中的标准 UI 为旧 UI，是当用户访问数据管理工作区时呈现给用户的默认 UI。

|   |  |
|------------------|-------------------------|
| **弃用/移除的原因** | 我们正努力在新的 UI 中为用户提供新的体验。             |
| **被另一个功能取代？**   | 新 UI 称为*增强型视图*，它将取代旧 UI。            |
| **影响的产品区域**         | 数据管理工作区                                                     |
| **部署选项**              | 全部                                                                           |
| **状态**                         | 已弃用：移除功能的目标时间范围为 2018 年第二季度。 |

### <a name="excise-sales-tax-service-tax-for-india"></a>适用于印度的消费税、销售税、服务税

这些税项已归入印度 GST。

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **移除或弃用的原因**       | 这些税项已归入印度 GST。                          |
| **被另一个功能取代？**            | 印度 GST                                                              |
| **影响的产品区域**                  | 税金                                                                     |
| **部署选项**                       | 所有模块                                                   |
| **状态**                                  | 已弃用：尚未确定此功能的移除日期。 |    

### <a name="file-validation-utility-fvu-for-india"></a>印度文件验证实用工具 (FVU)

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **移除或弃用的原因**       | 缺少客户使用                                                  |
| **被另一个功能取代？**            | 无                                                                      |
| **影响的产品区域**                  | 印度预缴税金                                                  |
| **部署选项**                       | 所有模块                                                                    |
| **状态**                                  | 已弃用：尚未确定此功能的移除日期。   |        

### <a name="tdstcs-certificate-for-india"></a>印度 TDS/TCS 证书

用户可从政府门户下载。

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **移除或弃用的原因**       | 缺少客户使用                                                  |
| **被另一个功能取代？**            | 无                                                                      |
| **影响的产品区域**                  | 印度预缴税金                                                  |
| **部署选项**                       | 所有模块                                                                   |
| **状态**                                  | 已弃用：尚未确定此功能的移除日期。     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>导出/导入 (EXIM) 印度激励方案


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **移除或弃用的原因**       | 缺少客户使用                                                  |
| **被另一个功能取代？**            | 无                                                                      |
| **影响的产品区域**                  | 导入和导出                                                       |
| **部署选项**                       | 所有模块                                                                    |
| **状态**                                  | 已弃用：尚未确定此功能的移除日期。  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>个性化产品建议 
从 2018 年 2 月 15 日开始，零售商再也不能显示有关销售点 (POS) 设备的个性化产品建议。 有关详细信息，请参阅[产品建议概览](../../../commerce/product-recommendations.md)。  

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。  |
| **被另一个功能取代？**   | 编号 但是，我们计划在 2018 年春季之后恢复此功能，以利用新的建议服务。   |
| **影响的产品区域**         | POS 中的个性化产品建议。                                                    |
| **部署选项**              | 全部                                                                                      |
| **状态**                         |从 2018 年 2 月 15 日开始移除。 这将影响运行 Dynamics 365 for Retail 7.2 及更高版本的客户。 |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>具有平台更新 8 的 Finance and Operations Enterprise edition（2017 年 7 月）

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>记帐币种和申报币种的币种转换

引入欧元时，也引入了记帐币种和申报币种的币种转换。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | “复制法人”功能作为替代方法的使用和添加受限。      |
| **被另一个功能取代？**   | 否，但是增加了“复制法人”和“配置”功能，从而可以更轻松地迁移到核心需求不断变化的公司。 |
| **影响的产品区域**         | 财务管理     |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。   |


### <a name="warehouse-mobile-devices-portal"></a>仓库移动设备门户

仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。 Finance and Operations 中不再支持此组件。 一个可提高用户体验的本机应用已替代 WMDP 的功能。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 重复的功能。       |
| **被另一个功能取代？**   | 是。 此功能已被 Finance and Operations - Warehousing 取代。 有关设置和先决条件的详细信息，请参阅[安装和配置仓库应用概述](../../../supply-chain/warehousing/install-configure-warehousing-app.md)。 |
| **影响的产品区域**         | 仓库管理，运输管理     |
| **部署选项**              | 仓库移动设备门户 (WMDP) 是用于本地自行部署的单独组件。               |
| **状态**                         | 已弃用：移除功能的目标时间范围为 2019 年第四季度。   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>用于手动匹配的高级银行对帐匹配规则

匹配规则用于在对帐工作表中手动匹配单据时选择和标记银行单据。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 有限使用。                                                                         |
| **被另一个功能取代？**   | 编号 应使用列筛选功能查找用于对帐的单据。 |
| **影响的产品区域**         | 现金和银行管理                                                               |
| **部署选项**              | 所有                                                                                    |
| **状态**                         | 从 2017 年 7 月开始移除。                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>带平台更新 3 的 Dynamics 365 for Operations 1611

### <a name="aeb-payment-formats-for-spain"></a>西班牙的 AEB 付款格式

Consejo Superior Bancario 付款格式过去用于将汇款文件发送到客户付款和供应商付款的银行。 由 Asociación Española de Banca 确定这些格式的内容。 它包含 Cuaderno 19、32、58、34。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                  |
| **被另一个功能取代？**   | 是，西班牙的 ISO20022 贷方转帐和直接借记付款格式 |
| **影响的产品区域**         | 应付账款，应收账款                                    |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。           |

### <a name="bank-payments-transfer-for-lithuania"></a>立陶宛银行付款转帐

过去使用立陶宛付款转账 (LT) 导出格式生成并打印银行付款转账。 立陶宛市场于 2005 年开始使用 LITAS，统一电子银行系统。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                        |
| **被另一个功能取代？**   | 是，立陶宛 ISO20022 贷方转帐付款格式     |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>挪威 BBS Direkte Remittering 付款格式

BBS Direkte Remittering 付款格式包括客户收款导出（直接借记）和返回消息导入。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。  |
| **被另一个功能取代？**   | 挪威的 AvtaleGiro 客户付款格式可用于生成直接借记消息。 未来版本中将实施返回消息导入。 |
| **影响的产品区域**         | 应付账款，应收账款   |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>西班牙会计科目表工具

西班牙会计科目表要求重大更改时使用此工具。 用户可以导入新的 Microsoft Excel 或文本格式的会计科目表，也可以导入财务报表。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 有限使用                                                  |
| **被另一个功能取代？**   | 无                                                             |
| **影响的产品区域**         | 总帐                                                 |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="dom80-payment-format-for-belgium"></a>比利时的 Dom80 付款格式

付款托收的比利时传统付款格式（直接借记）。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                          |
| **被另一个功能取代？**   | 是，比利时 ISO 20022 直接借记付款格式         |
| **影响的产品区域**         | 应收帐款                                            |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="dtaezag-payment-formats-for-switzerland"></a>瑞士的 DTA/EZAG 付款格式

DTA/EZAG 格式集成在 ESR 系统中，因为他们可以持有参考编号。 由于参考编号不是必需的，因此可以使用这些格式处理任何供应商付款。 银行帐户位置不在“Postfinance”的公司使用这些格式。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                        |
| **被另一个功能取代？**   | 是，瑞士 ISO20022 贷方转帐付款格式   |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>奥地利 EDIFACT-DIRDEB 付款格式

付款托收的 EDIFACT-DIRDEB 付款格式（直接借记）。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                          |
| **被另一个功能取代？**   | 是，奥地利 ISO 20022 直接借记付款格式         |
| **影响的产品区域**         | 应收帐款                                            |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="edivat-for-belgium"></a>比利时的 EDIVAT

EDIVAT 是比利时通过安全电子邮件进行电子申报的已过时的标准做法。 Dynamics AX 2012 保留启用历史数据访问权限的只读解决方案。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此功能不再使用。                           |
| **被另一个功能取代？**   | 无                                                             |
| **影响的产品区域**         | 总帐                                                 |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>挪威的 eGiro EDIFACT CREMUL 付款导入格式

eGiro 基于国际 UN EDIFACT CREMUL（多重贷记通知消息）标准，用于客户付款的自动过帐。 在 Dynamics AX 中，eGiro 作为客户付款导入格式实施。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                                     |
| **被另一个功能取代？**   | 可以，可以被 ISO20022 Camt.054 通知导入取代。 |
| **影响的产品区域**         | 应收帐款                                                                       |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                            |

### <a name="external-inventory-for-poland"></a>波兰的外部库存

来自供应商用于销售且无需购买的货物的证据。 在外部库存中处理的货物不影响标准库存，可以销售，然后被自动购买。 此流程创建实际库存变动。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 替换为另一个功能                                    |
| **被另一个功能取代？**   | 是，为核心入站托运功能                |
| **影响的产品区域**         | 应付账款，库存管理                         |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="financial-reports-generator-for-eastern-europe"></a>东欧的财务报表生成器

用于设置会计和纳税报表的数据收集，以及用于将数据导出到 XLS 和 DOC 报表模板的工具。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 有限使用                                                                            |
| **被另一个功能取代？**   | 编号 工具在未来版本中将被电子申报配置所取代。 |
| **影响的产品区域**         | 总帐                                                                           |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>芬兰的客户付款交易记录导入

您可以为从银行提供的外部文件导入客户付款交易记录的芬兰付款选择导入格式。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                                     |
| **被另一个功能取代？**   | 可以，可以被 ISO20022 Camt.054 通知导入取代。 |
| **影响的产品区域**         | 应收帐款                                                                       |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>付款交易记录导入到芬兰的总帐日志帐中

用于芬兰将会计交易记录导入到总帐的特定格式。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                                     |
| **被另一个功能取代？**   | 可以，可以被使用高级银行对帐单的 ISO20022 Camt.053 银行对帐单导入取代。 |
| **影响的产品区域**         | 应收帐款                                                                       |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>比利时与 Isabel 同步 (CIS) 集成

Isabel 是欧洲电子银行的框架和比利时的事实标准。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 与 Isabel 客户端的集成已停止。   |
| **被另一个功能取代？**   | 编号 付款格式不再使用，被比利时的 ISO20022 贷方转帐付款格式所取代。 |
| **影响的产品区域**         | 应付帐款     |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>修改西班牙的会计科目表和会计规则

此功能用于修改西班牙的会计科目表和会计规则。 它映射帐户，以帮助将旧的会计科目表转换到新的会计科目表，将上一个会计年度与新的会计年度相比较，即使是当它们过帐到不同的科目编号时。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 有限使用                                                  |
| **被另一个功能取代？**   | 无                                                             |
| **影响的产品区域**         | 总帐                                                 |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori 供应商付款格式

传统意大利贷方转帐付款格式

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                          |
| **被另一个功能取代？**   | 是，意大利 ISO20022 贷方转帐付款格式         |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="payment-export-formats-for-estonia"></a>爱沙尼亚付款导出格式

Telehansa 和 Teleservice 格式为银行付款导出使用。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                        |
| **被另一个功能取代？**   | 是，爱沙尼亚 ISO20022 贷方转帐付款格式       |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="payment-file-archive-for-norway"></a>挪威付款文件存档

在生成付款文件时，文件存档自动存档所有创建的文件，甚至包括以前写入或读取的文件。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 替换为另一个功能                                        |
| **被另一个功能取代？**   | 是，电子申报已存档作业                            |
| **影响的产品区域**         | 应付账款，应收账款，组织管理 |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。     |

### <a name="payment-import-formats-for-estonia"></a>爱沙尼亚付款导入格式

Telehansa 和 TeleTeenus 格式为银行付款导入使用。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                                    |
| **被另一个功能取代？**   | 可以，可以被 ISO20022 Camt.054 银行通知导入取代。 |
| **影响的产品区域**         | 应收帐款                                                                        |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                             |

### <a name="payroll-information-in-human-resources"></a>人力资源中的工资单信息

人力资源工资单信息

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此功能已由工资单和人力资源页取代。  |
| **被另一个功能取代？**   | **福利**、**收入**和已经位于美国工资单中的其他相关页已被重新配置，现在是核心人力资源配置的一部分，可帮助支持外部工资单处理。 此功能可通过使用**人力资源 1** \> **工资单**配置键访问到。 |
| **影响的产品区域**         | 人力资源、工资单   |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除。    |

### <a name="performance-management-goal-workflow"></a>绩效管理目标工作流

绩效管理包括目标管理和与绩效审核集成。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 绩效管理经过重新设计，减少了目标页数，以简化流程。                 |
| **被另一个功能取代？**   | 编号 目标通过经理自助服务门户对经理可见，并且可由经理进行更改和查看。 |
| **影响的产品区域**         | 人力资本管理       |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除。    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>瑞典的 Postgirot 和 Postgirot Utland 付款格式

瑞典的 Postgirot 和 Postgirot Utland 付款格式。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                        |
| **被另一个功能取代？**   | 是，瑞典 ISO20022 贷方转帐付款格式        |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="radio-frequency-identifier"></a>射频标识

无线射频标识 (RFID) 是一种使用电子标签存储标识数据的数据收集技术和一种捕获标识数据的无行视域需求阅读器。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低客户使用率和有限功能集。   |
| **被另一个功能取代？**   | 无                                              |
| **影响的产品区域**         | 库存管理                            |
| **状态**                         | 从 Dynamics 365 for Operations 1611 开始移除。 |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>有关拉脱维亚国家发票编号的报表

拉脱维亚法律提供有关销售发票应如何编号的特定规则。 此功能允许您基于用户或用户组向销售发票分配具体编号。 之后您可以生成报表或 XML 文件。 您还可以打印有关已使用发票编号的报表。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 国家发票编号不必再进行维护。 不再要求有关已使用发票编号的报表。 |
| **被另一个功能取代？**   | 无       |
| **影响的产品区域**         | 应收帐款    |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>设置立陶宛公司的经理和会计主管的姓名

公司经理和会计主管的姓名可以在公司信息中指定，并用于不同的本地报表打印输出。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 替换为另一个功能                                     |
| **被另一个功能取代？**   | 是，专员设置可用于同一个目的。   |
| **影响的产品区域**         | 应付账款、应收账款、现金和银行管理 |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。  |

### <a name="shipping-carrier-interface"></a>装运承运人界面

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 重复的功能   |
| **被另一个功能取代？**   | 部分由运输管理取代 |
| **影响的产品区域**         | 销售和市场营销、库存管理  |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除。  |

### <a name="telepay-payment-formats-for-norway"></a>挪威 Telepay 付款格式

Telepay 付款格式包括供应商付款导出（贷方转帐）和客户付款托收（直接借记）。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                                                        |
| **被另一个功能取代？**   | 可以，可以被挪威的 ISO20022 贷方转帐付款格式和 AvtaleGiro 客户付款格式，以及 pain.002 和 camt.054 银行通知返回文件导入取代。 |
| **影响的产品区域**         | 应付账款，应收账款                                                          |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>芬兰的供应商付款导出格式

两个导出付款格式可用于芬兰。 LM02 (FI) 用于国内付款，LUM2 (FI) 用于国外付款。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 付款格式不再使用。                        |
| **被另一个功能取代？**   | 是，芬兰 ISO20022 贷方转帐付款格式       |
| **影响的产品区域**         | 应付帐款                                               |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="warehouse-management-ii"></a>仓库管理 II

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | **库存管理**模块中可用的仓库管理 II 解决方案 (WMS II) 与在 Dynamics AX 2012 R3 中发布的**仓库管理模块**中的功能重复。                                                                         |
| **被另一个功能取代？**   | 在 AX 2012 R3、Dynamics AX 2012 R3 CU8 和 Dynamics AX 2012 R3 CU9 中发布的**仓库管理模块**取代仓库管理 II 功能。 新模块具有比仓库管理 II 更高级的功能和更灵活的仓库管理流程。 |
| **影响的产品区域**         | 库存管理、销售和市场营销、采购   |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除。    |

### <a name="worker-reminders-in-human-resources"></a>人力资源中的工作人员提醒

人力资源工资单信息

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低使用率                                                           |
| **被另一个功能取代？**   | 无                                                                  |
| **影响的产品区域**         | 人力资源                                                     |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除 |

### <a name="workflow-for-creating-goals"></a>创建目标的工作流

管理员工目标创建的工作流是多个可用工作流的其中一个，帮助协调绩效管理流程。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 绩效管理在 Finance and Operations 中已经完全重新设计。     |
| **被另一个功能取代？**   | 经过重新设计的绩效管理功能能够更好地控制目标内容、用来跟踪进度的衡量指标以及支持文档的附加。 目标可以存储为模板并重复使用。 此功能可以帮助您更加快速地为您的员工设置额外目标。 |
| **影响的产品区域**         | 人力资本管理                 |
| **状态**                         | 从 Dynamics 365 for Operations 版本 1611 开始移除。 |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>能够取消对供应商发票的更改

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 性能改进        |
| **被另一个功能取代？**   | 无                             |
| **影响的产品区域**         | 应付帐款               |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。 |

### <a name="aif-axd-and-axbc-integrations"></a>AIF、Axd 和 AxBC 集成

在应用集成框架 (AIF) 中，数据可以通过显示为服务的业务逻辑与外部系统交换。 Dynamics AX 包括基于文档和 .NET Business Connector (AxBC) 的服务。 文档是通过使用 XML 创建的。 XML 包括标题信息，添加该信息的目的是创建可在 Dynamics AX 内外传送的*消息*。 文档的示例包括销售订单和采购订单。 但是，几乎所有实体（例如客户）都可以被文档代表。 基于文档的服务使用 **Axd \<Document\>** 类。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | AIF 和 AxDs 的体系结构不能扩展到云服务。 批量导入有性能问题。                                        |
| **被另一个功能取代？**   | 此功能由数据导入/导出框架取代，该框架支持重复执行的批量导入/导出。 对于 AxBC，我们建议您使用实际表。 |
| **影响的产品区域**         | AxDs、AxBC 和 AIF   |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。   |

### <a name="billing-code-rate-scripts"></a>计费代码费率脚本

过去使用计费脚本计算计费代码的计费费率。 此脚本要求使用 C Sharp 或 Visual Basic 编程语言进行自定义开发。 在当前版本的 Dynamics AX 中，不支持**计费代码费率脚本**。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Dynamics AX 7.0 中未添加对自定义 C Sharp 或 Visual Basic 脚本的支持。 |
| **被另一个功能取代？**   | 否                                                                                      |
| **影响的产品区域**         | 公共部门，应收帐款                                    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                                          |

### <a name="boms-without-bom-versions"></a>没有物料清单版本的物料清单

当禁用**物料清单版本**配置键时，物料清单版本在所有窗体中处于隐藏状态，系统将在已发布的产品和物料清单之间强制 1:1 关系。 在 Dynamics AX 的当前版本中，**物料清单版本**配置键不能禁用。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 使用配置键控制物料清单版本不会在云环境中扩展。 |
| **被另一个功能取代？**   | 无                                                                                      |
| **影响的产品区域**         | 产品信息管理、库存管理                                    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                                          |

### <a name="brazilian-bordero"></a>巴西 Bordero

巴西公司的特定付款方式

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 对巴西 Bordero 付款方式的支持已经在巴西本地化中被中断。 |
| **被另一个功能取代？**   | 无   |
| **影响的产品区域**         | 应付帐款   |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="brazilian-sintegra-statement"></a>巴西 Sintegra 报表

ICMS 税联邦报税单

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此报表在巴西的部分州不再适用。 |
| **被另一个功能取代？**   | 编号 在某些特定情况下，用户可以使用通用电子申报工具配置报表。 |
| **影响的产品区域**         | 会计帐簿    |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>巴西的 SCAN NF-e 意外事故模式

(SCAN) 意外事故环境用于在 Secretaria da Fazenda (SEFAZ) 环境不可用时生成、导出和导入 Nota Fiscal eletrônica (NF-e) 的状态。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此意外事故方法在巴西所有州中不再适用。 |
| **被另一个功能取代？**   | 无                                                                          |
| **影响的产品区域**         | 应收帐款                                                         |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。              |

### <a name="business-analyzer"></a>业务分析器

此移动应用程序能让用户查看关键业务度量。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此功能已被另一个功能取代。   |
| **被另一个功能取代？**   | Microsoft Power BI 的监控财务业绩目录包将包括已经在 Business Analyzer 中可用的关键财务度量。 |
| **影响的产品区域**         | 总帐      |
| **状态**                         | 已弃用：业务分析器的使用已被弃用。    |

### <a name="business-statistics"></a>业务统计

设置业务统计查询，以帮助您分析组织的绩效

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 商业智能 (BI)、低客户使用率和有限功能集的传统方法 |
| **被另一个功能取代？**   | Dynamics AX 的当前版本的新 BI 解决方案                                      |
| **影响的产品区域**         | 采购、应付账款、销售和市场营销、应收账款         |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>更改发票审核日记帐的单据日期功能

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低使用率                                                               |
| **被另一个功能取代？**   | 是。 可以更改已过帐供应商交易记录的单据日期。 |
| **影响的产品区域**         | 应付帐款                                                        |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>针对荷兰的 ClieOp03 付款格式

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 该格式不再适用于荷兰，因为它已被 SEPA 功能取代。 |
| **被另一个功能取代？**   | SEPA 付款导出  |
| **影响的产品区域**         | 所有模块     |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。   |

### <a name="compliance-center"></a>遵从性中心

遵从性中心是一个企业门户站点，用于管理与 Sarbanes-Oxley 法案有关的遵从性计划的文档要求。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 缺少客户使用。 Microsoft SharePoint 包括和遵从性中心功能相同的功能。 |
| **被另一个功能取代？**   | 无   |
| **影响的产品区域**         | 符合性和内部控制  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。    |

### <a name="connector-for-microsoft-dynamics"></a>Connector for Microsoft Dynamics

此工具用于集成从 Microsoft Dynamics CRM 到 Dynamics ERP 应用程序的重要数据。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此功能已被另一个功能取代。 |
| **被另一个功能取代？**   | Common Data Service                                      |
| **影响的产品区域**         | Dynamics 的连接器                         |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>容器单位和多维现有量

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 重复的功能 |
| **被另一个功能取代？**   | 是。 自 AX 2012 起，此功能已由合并的批次订单功能集替换。 此功能集包括合并的现有量视图。 |
| **影响的产品区域**         | 产品信息控制管理、生产控制、库存管理、销售和市场营销  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。 |

### <a name="cue-group-metadata"></a>提示组元数据

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 提示组用于在 FactBox 区域中显示一个或多个提示。 由于父窗体中的记录更改会导致提示组中每个提示对应一个查询，因此它的接受程度有限，而且还存在性能顾虑。 |
| **被另一个功能取代？**   | 无      |
| **影响的产品区域**         | 所有模块    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。  |

### <a name="cue-metadata"></a>提示元数据

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 提示元数据仅限于计数或合计信息。    |
| **被另一个功能取代？**   | 引入了磁贴元数据，可为建模提供更多灵活性。 例如，您可以对当前计数、导航和关键绩效指标 (KPI) 进行建模。 计数磁贴元数据是提示元数据的直接取代。 |
| **影响的产品区域**         | 所有模块           |
| **状态**                         | 从 Dynamics AX 7.0 开始移除      |

### <a name="danish-check-format"></a>丹麦支票格式

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 对丹麦支票格式布局的支持已终止，并且报告已经从 DK 本地化中删除。 |
| **被另一个功能取代？**   | 无    |
| **影响的产品区域**         | 所有模块    |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。  |

### <a name="data-partitions"></a>数据分区

数据分区在 Dynamics AX 数据库中提供数据的逻辑界定。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 数据分区在 Dynamics AX 2012 R2 引入以启用数据隔离。 在常见情况中，公司有子公司，一个子公司的数据不应对另一个子公司可见，即使两个子公司均由相同的 IT 部门管理。 不过，整个程序都需要额外的脚本和管理开销来创建新的分区并填充数据，以及备份分区数据。 在云中，在其中我们有访问平台即服务 (PaaS) 数据库服务（Microsoft Azure SQL 数据库）的权限，则使用数据库作为隔离容器比在程序中执行隔离要高效得多。 不管是子公司、多个租户，或只为规模需要进行数据分区，我们认为通过多个 Finance and Operations 实例都可以更好地处理这种情况。 |
| **被另一个功能取代？**   | 如果数据库级别分隔是关键问题，使用数据分区的客户必须使用多个 Finance and Operations 实例。    |
| **影响的产品区域**         | 所有模块  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。  |


### <a name="database-and-file-share-storage-for-attachments"></a>数据库和文件共享附件存储

Dynamics AX 2012 允许在数据库和文件共享中存储附件。 这两个选项都不再受支持。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 云托管的环境无法再与本地文件共享通信，因此文件共享存储不再受支持。 为了支持 Azure Blob 存储，数据库存储已弃用。 Azure Blob 存储相当于数据库中的存储，因为文档仅可以通过 Finance and Operations 客户端窗体进行访问。 这提供额外好处，即提供存储不会对数据库的性能造成不利影响。 Blob 存储是文档管理的默认存储机制并立即生效。 |
| **被另一个功能取代？**   | 为了支持 Azure Blob 存储，数据库存储已弃用。   |
| **影响的产品区域**         | 所有模块  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。   |

### <a name="delimitation"></a>界定

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 找不到该功能的使用。 |
| **被另一个功能取代？**   | 无                                     |
| **影响的产品区域**         | 考勤管理                    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。         |

### <a name="desktop-client"></a>桌面客户端

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Dynamics AX 客户端体验已被重新设计，可提高在多个平台和设备上的可用性。                      |
| **被另一个功能取代？**   | 新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。 |
| **影响的产品区域**         | 所有模块  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。   |

### <a name="direct-database-connection"></a>直接数据库连接

在 Dynamics AX 2012 R3 中，Retail Modern POS 可以直接连接到与 Enterprise POS 方式相似的通道 DB。 这是除通过 Retail Server 的 Retail Modern POS 通信的标准通信方法以外的方法。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 直接数据库连接要求较低的安全协议，主要用于达到最高性能级别。 由于 Finance and Operations 中性能和安全性提高，此功能现在导致的问题比解决的问题更多。 |
| **被另一个功能取代？**   | 编号 现在只支持标准零售服务器通信。  |
| **影响的产品区域**         | 通道 DB/Retail Modern POS   |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。  |

### <a name="dutch-swift-mt940"></a>荷兰 SWIFT MT940

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 现在使用的是通用功能，而不是本地化功能。                    |
| **被另一个功能取代？**   | 是，此功能已被高级银行对帐功能取代。 |
| **影响的产品区域**         | 所有模块                                                                              |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz（针对德国的 XBRL）

此功能专门针对德国 eBilanz 分类提供了可扩展业务报告语言 (XBRL) 输出。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 缺少客户使用  |
| **被另一个功能取代？**   | 此功能尚未被另一个功能取代，不过，多个提供丰富 XBRL 功能的专用 XBRL 程序包对德国市场可用。 |
| **影响的产品区域**         | Management Reporter      |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。  |

### <a name="enterprise-portal-client"></a>企业门户客户端

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 提供了一个客户端平台。  |
| **被另一个功能取代？**   | 新的 Web 客户端基于已经过修改可提供丰富 Web 平台的桌面窗体元数据和编程模型。 |
| **影响的产品区域**         | 所有模块  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。   |

### <a name="environmental-sustainability"></a>环境可持续性

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低客户使用率和有限功能集  |
| **被另一个功能取代？**   | 无              |
| **影响的产品区域**         | 遵从性和内部控制、应付账款  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。 |

### <a name="form-activex-and-managed-host-controls"></a>窗体 ActiveX 和托管主机控件

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | ActiveX 和托管主机控件基于已废弃的桌面客户端。 |
| **被另一个功能取代？**   | 可扩展控件框架支持构建新的基于 HTML、CSS 和 JavaScript 的控件，并且是 Microsoft Visual Studio 工具环境中的一流控件。 |
| **影响的产品区域**         | 所有模块     |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。       |

### <a name="generate-prenotes-by-using-a-batch"></a>通过使用批处理生成预验证

预验证生成无法通过使用批处理完成，但仍可以由用户完成。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 在通过使用批处理生成预验证文件时，没有窗体持续存在并且显示生成的预验证文件。 |
| **被另一个功能取代？**   | 预验证仍可以生成，并且用户能够控制该文件的保存位置。   |
| **影响的产品区域**         | 应付账款、应收账款、现金和银行管理  |
| **状态**                         | 从 AX 7.0 开始移除。    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>德国 DTAUS 付款导出和帐户对账单导入（合计和交易记录）

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 该格式不再适用于德国，因为它已被单一欧元支付区 (SEPA) 功能取代。                    |
| **被另一个功能取代？**   | 是，此功能已被 SEPA 付款导出和高级银行对帐功能（用于导入帐户对账单）取代。 |
| **影响的产品区域**         | 所有模块  |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>国内币种的德国 DTAZV 付款格式

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 该格式不再适用于德国，因为它已被 SEPA 功能取代。 |
| **被另一个功能取代？**   | SEPA 付款导出    |
| **影响的产品区域**         | 应付帐款   |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。    |

### <a name="german-mt940-import"></a>德国 MT940 导入

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 现在使用的是通用功能，而不是本地化功能。                    |
| **被另一个功能取代？**   | 是，此功能已被高级银行对帐功能取代。 |
| **影响的产品区域**         | 所有模块                                                                              |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。                           |

### <a name="german-xml-eu-sales-list"></a>德国 XML 欧盟销售清单

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 不再支持德国欧盟销售清单报表的 XML 格式。 仅 ELMA5 文本文件格式可用于将欧盟销售清单报表提交给德国税务局。 |
| **被另一个功能取代？**   | 无         |
| **影响的产品区域**         | 税金        |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。   |

### <a name="gl-ssrs-reports"></a>GL SSRS 报表

包括以下菜单项的报表已被删除：**试算平衡表(汇总)**、**试算平衡表(明细)**、**会计科目表**、**审计线索**、**余额**和**余额表**。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 财务 Microsoft SQL Server Reporting Services (SSRS) 报表已经被 Management Reporter 功能和默认报表取代。 |
| **被另一个功能取代？**   | Management Reporter（在 Dynamics AX 的当前版本中标记为**财务报告**。）    |
| **影响的产品区域**         | 总帐   |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart 和 FormPart 元数据

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | InfoPart 和 FormPart 元数据支持为两个不同的客户端创建 FactBox。 |
| **被另一个功能取代？**   | InfoPart 元数据，是一种简化的窗体定义，由升级工具转换为窗体。 引用窗体的 FormPart 元数据已被升级工具所创建的更直接引用取代。 |
| **影响的产品区域**         | 所有模块    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。        |

### <a name="main-account-list-page"></a>主科目列表页

法人的帐户列表和相关余额信息

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 余额信息现在在**试算余额表**列表页上按帐户和维度提供。  |
| **被另一个功能取代？**   | **主科目**包含**主科目**列表页所包含的相同科目列表。 **主科目**中的网格视图还显示一个更小的、如网格般的视图。 |
| **影响的产品区域**         | 总帐      |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>马来西亚和新加坡银行现金流量报表

此功能能让用户打印现金流量报表，以显示特定日期范围或所选银行帐户的现金流入量和流出量的交易记录和详细信息。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 同样的信息可以从查询银行交易记录中获得。 |
| **被另一个功能取代？**   | 查询银行交易记录                                            |
| **影响的产品区域**         | 现金和银行管理                                                |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。          |

### <a name="mexican-cfd-electronic-invoice"></a>墨西哥 CFD 电子发票

此功能支持通过使用 Comprobante Fiscal Digital (CFD) 方法生成墨西哥电子发票，在该方法中公司通过请求来自政府的相关主管机构签署发票。 此功能还提供一个每月报表，其包括在该期间签发的所有电子发票。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此方法不再适用。 通过使用 CFD 方法生成电子发票已被税务主管机构废弃，并已被 Comprobante Fiscal Digital a través de Internet (CFDI) 方法取代，在该方法中签名委托给第三方提供商 (PAC)。 删除了每月报表，并且，查询选项能让用户查询历史交易记录。 |
| **被另一个功能取代？**   | 无    |
| **影响的产品区域**         | 应收账款、项目   |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="mexico-realized-and-unrealized-vat"></a>墨西哥实现和未实现的增值税

Dynamics AX 2012 通过使用“未实现的增值税”的墨西哥特定功能管理未实现的增值税 (VAT)。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 重复的功能  |
| **被另一个功能取代？**   | 是，此功能已被使用核心提供的标准特定销售增值税功能取代。 |
| **影响的产品区域**         | 税金   |
| **状态**                         | 已弃用：尚未确定此功能的移除日期。 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook 集成


|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 此功能已被 Microsoft Exchange Server 集成取代。 |
| **被另一个功能取代？**   | 是                                                                            |
| **影响的产品区域**         | Sales and Marketing                                                            |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>库存和仓库管理日记帐的专用锁定

库存和仓库日记帐不再支持针对所选用户将日记帐标记为专用的功能。 仅支持针对用户组将日记帐锁定为专用和在编辑期间锁定的流程。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 找不到该功能的使用。 |
| **被另一个功能取代？**   | 无                                     |
| **影响的产品区域**         | 库存管理                   |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。         |

### <a name="product-builder"></a>产品生成器

产品生成器用于从销售订单、采购订单、生产订单、销售报价单、项目报价单或物料需求动态配置物料。 基于具有建模变量的产品模型，用户可以选择值以满足用户需求并获取具有物料清单和工艺路线的唯一产品变型。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 产品生成器向最终用户显示了 X++ 代码，在 Dynamics AX 的当前版本中不受支持。 它已被删除，从而避免在重叠的、庞大的代码库中进行重复的维护工作。  |
| **被另一个功能取代？**   | 是。 已经公布在将来的版本中弃用产品生成器的 Dynamics AX 2012 中引入了基于约束的配置。 在基础产品上选择基于约束的配置技术，以启用配置。 若要了解更多信息，请参阅[产品配置概述](../../../supply-chain/pim/build-product-configuration-model.md)。 |
| **影响的产品区域**         | 产品信息管理、销售和市场营销  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。      |

### <a name="production-floor-app"></a>生产车间应用
这是适用于运行 Windows 8.1 RT 和 Windows 8.1 Pro 的平板设备的应用。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 通过对基于 Web 的客户端的更改，可以通过本机 Dynamics AX 7.0 客户端提供类似的功能。 作业卡设备提供为触摸和平板窗体因子优化的生产车间用户界面。 |
| **被另一个功能取代？**   | 是。 作业卡设备是 Dynamics AX 7.0 的一个本机部分。                                                                           |
| **影响的产品区域**         | 生产控制                                                |
| **状态**                         | 已弃用：从 Microsoft Store 的删除日期尚未为此功能设置。                                                |


### <a name="rename-product-dimension"></a>重命名产品维度

此功能能让您将三个标准维度（大小、颜色或样式）之一的名称更改为一个更好地满足您的业务需求的名称。 重命名包括其中使用了产品维度名称的所有标签。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Dynamics AX 的当前版本在运行时不支持标签。 |
| **被另一个功能取代？**   | 无                                                                            |
| **影响的产品区域**         | 产品信息管理                                                |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                                |

### <a name="retail-server-connectivity-using-http"></a>使用 HTTP 的零售服务器连接

在 Dynamics AX 2012 R3 中，零售服务器可以使用 HTTP 通信（不受安全保护）运行。 这是除使用 HTTPS 的标准通信之外的方法。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 因为新的安全要求，现在只支持使用 TLS 1.2（或更高版本，如果可用）的安全通信。 自助服务安装程序将自动配置此通信的计算机。 |
| **被另一个功能取代？**   | 编号 现在只支持标准 HTTPS 通信。 |
| **影响的产品区域**         | 零售服务器  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。 |

### <a name="role-center-pages"></a>角色中心页

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 角色中心页基于已废弃的企业门户平台而构建，该平台已被 Dynamics AX 的当前版本中的新 Web 客户端平台取代。 |
| **被另一个功能取代？**   | 新工作区窗体模式为用户提供一个以流程为中心的设计，从而便于访问该流程中的常用任务。                       |
| **影响的产品区域**         | 所有模块    |
| **状态**                         | 从 Dynamics AX 7.0 开始移除   |

### <a name="sales-tax-jurisdictions"></a>销售税区域

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低客户使用率和有限功能集 |
| **被另一个功能取代？**   | 无                                           |
| **影响的产品区域**         | 美国销售税                                 |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。               |

### <a name="sites-services"></a>站点服务

站点服务允许您构建将您的业务流程扩展到 Internet 的网站，而无需 IT 支持。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Dynamics AX 的 Microsoft Azure 基础结构具有可以使用的新功能（例如，Azure 站点）。 |
| **被另一个功能取代？**   | 无   |
| **影响的产品区域**         | 人力资源招聘、案例管理、询价、供应商注册、机会和市场活动协作工作区  |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS 需求预测策略

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 新的云体系结构中不支持设计此功能。 |
| **被另一个功能取代？**   | Azure 机器学习需求预测策略                           |
| **影响的产品区域**         | 主计划                                                              |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>供应商发票池(不包括过帐)详细信息

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低使用率。 此功能已被具有工作流功能的发票日记帐取代。 |
| **被另一个功能取代？**   | 发票日记帐的工作流功能。     |
| **影响的产品区域**         | 应付帐款 |
| **状态**                         | 从 Dynamics AX 7.0 开始移除。    |


### <a name="virtual-company-accounts"></a>虚拟公司帐户

Dynamics AX 中不再支持虚拟公司功能。 虚拟公司功能允许用户设置可以由一组公司共享的表。 有关该功能的描述，请参阅[公司帐户和虚拟公司帐户](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx)。 该功能的工作原理是将表分组到集合，然后集合分配给虚拟公司，即现有的“实际”公司的组。 创建查询，以便虚拟公司中的所有公司可以访问关联表集合的表中的数据。

|   |  | 
|------------|--------------------|
| **弃用/移除的原因** | - 将数据存储在表中之前，必须先设置虚拟公司。 将虚拟公司更新到现有实施上是很困难的。<br><br>- 由于 Dynamics AX 的当前版本中有如此多数据标准化，要了解将什么添加到表集合将会很困难。 例如，要知道共享哪些表很难。 还必须添加从虚拟公司中的表引用的所有表。 由于表标准化，即使遍布许多表中的简单主数据也必须是虚拟公司的一部分。 此处所犯的任何错误都将导致功能问题。<br><br>- 当表是虚拟公司的一部分时，它会丢失有关数据来源的信息，并且只记录虚拟公司。   |
| **被另一个功能取代？** | 全局表可用于使表可从所有公司访问到。 当前不替换。 |   
| **影响的产品区域**       | 所有模块 |   
| **状态**                       | 从 Dynamics AX 7.0 开始移除。   |   

### <a name="windows-8-tablet-app"></a>Windows 8 平板电脑应用

Windows 8 平板电脑应用提供用于费用录入和审核的功能。

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | Finance and Operations 与平板电脑兼容。 无需再使用平板电脑应用。    |
| **被另一个功能取代？**   | 编号          |
| **影响的产品区域**         | 费用报销管理   |
| **状态**                         | 已移除：此功能仅对 Dynamics AX 2012 R3 可用。 |

### <a name="workplanner"></a>工作进度表

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 低使用率 |
| **被另一个功能取代？**   | 否，但从**模板组**页打开的**模板关系**页支持与弃用的**工作进度表**页相同的业务方案。 |
| **影响的产品区域**         | 考勤管理     |
| **状态**                         | 此代码尚未移除。 但窗体 JmgWorkPlanner 未迁移。    |

### <a name="x-financial-statements"></a>X++ 财务报表

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>弃用/移除的原因</strong> |                         此功能已被另一个功能取代。                         |
|  <strong>被另一个功能取代？</strong>  | Management Reporter（在 Dynamics AX 的当前版本中标记为<strong>财务报告</strong>。） |
|     <strong>影响的产品区域</strong>     |                                              总帐                                              |
|             <strong>状态</strong>             |                                      从 Dynamics AX 2012 开始移除                                      |

