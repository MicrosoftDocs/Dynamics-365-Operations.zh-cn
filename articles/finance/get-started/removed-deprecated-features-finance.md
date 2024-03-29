---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本文介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 25d13aa26565e5753b87c843b43cf46f8276b642
ms.sourcegitcommit: 6c05bcd27e6ee72f01cb66e2cfd1e929e0365830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2022
ms.locfileid: "9854071"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

本文介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](/dynamics/s-e/global/axtechrefrep_61)中提供了有关财务和运营应用中的对象的详细信息。 可比较这些报告的不同版本，以了解财务和运营应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Finance 10.0.31 版本中已经删除或弃用的功能

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>付款模型下的 EDIFACT PAYMUL (AT) 配置

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** | 已替换为基于 ISO 20022 pain.001.001.09 的新格式。 | 
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 应用程序 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用：奥地利的银行将在 2022 年 11 月之前弃用用于跨境支付的 EDICFACT-PAYMUL，将替换为 XML 版本 pain.001.001.09N。 全局配置存储库下添加了一个新配置，支持用户完成跨境付款请求。 |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Finance 10.0.30 版本中已经删除或弃用的功能

### <a name="revenue-recognition"></a>收入确认

[收入确认](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** |由改进的功能[订阅计费](../../finance/accounts-receivable/subscription-billing-summary.md)替代
| **被另一个功能取代？**   | 是 |
| **影响的产品区域** | 应用程序 |
| **部署选项** | 所有 |
| **Status** | 已弃用：2023 年 4 月之后，Dynamics 365 Finance 中的收入确认功能不会再获得 bug 修复支持。 将要求客户使用改进的功能[订阅计费](../../finance/accounts-receivable/subscription-billing-summary.md)。 到 2023 年 10 月，收入确认功能将不能再使用。 将要求客户移至改进的功能订阅计费功能。 对于作为收入确认一部分的捆绑销售功能，目前没有计划的替换功能。|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Finance 10.0.29 版本中已经删除或弃用的功能

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>具有转让价格税的存货转移单

[具有转让价格税的存货转移单](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** | 替换为了改进的功能，即[印度的存货转移单](../../finance/localizations/apac-ind-stock-transfer.md)|
| **被另一个功能取代？**   | 是 |
| **影响的产品区域** | 应用程序 |
| **部署选项** | 所有 |
| **Status** | 已弃用：2023 年 4 月之后，**具有转让价格税的存货转移单** 功能将不再获得错误修复和安全修复的相关支持。 将要求客户使用改进的功能，即[印度的存货转移单](../../finance/localizations/apac-ind-stock-transfer.md)。 2023 年 10 月之后，**具有转让价格税的存货转移单** 功能将不再可用，并且将要求客户改用改进的功能。 |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>银行对帐单导入和付款确认文件导出

| &nbsp;  | &nbsp;  |
|---|---|
| **弃用/移除的原因** |取而代之的是改进的功能，导入银行对帐单和导出付款确认文件。| 
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 应用程序 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用：用于导入和导出文件的 XSLT 功能不会再获得 bug 修复和安全修复支持。 将要求客户使用改进的功能：[使用电子报告设置付款确认文件](../../finance/accounts-payable/set-up-positive-pay-er.md)和[使用电子报告设置高级银行对帐导入](../../finance/accounts-payable/import-bai2-er.md)。 2022 年 9 月之后，XSLT 功能将不再可用，客户将被要求迁移到改进后的功能。|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Finance 10.0.26 版本中已经删除或弃用的功能

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>芬兰销售税报表（基于申报代码设计）

[芬兰的销售税报表](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的增值税申报设计[芬兰增值税申报](../localizations/emea-fin-vat-declaration.md)。 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 应用程序 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用：到 2023 年 3 月 1 日，我们计划不再支持芬兰销售税报表（芬兰报表布局）。 而是在 **税申报** 模型下引入新的 **增值税申报 TXT (FI**) 和 **增值税申报 Excel (FI)** 电子报告 (ER) 格式。 |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Finance 10.0.24 版本中已经删除或弃用的功能

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>瑞典销售税报表（基于申报代码设计）

[瑞典销售税报表](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的增值税申报设计[瑞典增值税申报](../localizations/emea-swe-vat-declaration-sweden.md) |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 全部 |
| **Status**                         | 已弃用：到 2022 年 12 月 1 日，我们计划不再支持瑞典销售税报表（瑞典报表布局）。 而是在 **税申报** 模型下引入新的 **增值税申报 XML (SE**) 和 **增值税申报 Excel (SE)** 电子报告 (ER) 格式。 |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>奥地利增值税报表（基于申报代码设计）

[奥地利增值税报表详细信息](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的增值税申报设计[奥地利增值税申报](../localizations/emea-aut-vat-declaration-austria.md) |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 全部 |
| **Status**                         | 已弃用：到 2022 年 12 月 1 日，我们计划不再支持 **增值税申报模型** 下的 **增值税申报 (AT)** 电子报告 (ER) 格式。 而是在 **税申报** 模型下引入新的 **增值税申报 XML (AT)** 和 **增值税申报 Excel (AT)** 格式。 |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes-electronic-tax-declaration-log-menu-item-and-page-electronic-tax-declaration-setup-menu-item-and-page-german-report-layout-taxreport_de-ssrs-format"></a>德国 ELSTER 申报（基于申报代码设计）、\"电子纳税申报日志\"菜单项和页面、 \"电子纳税申报设置\"菜单项和页面、德国报表版式 (TaxReport_DE) SSRS 格式

[VAT 报表](../localizations/emea-de-vat-declaration.md)</br>
[设置德国的电子纳税申报设置](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的增值税申报设计[德国增值税申报](../localizations/emea-deu-vat-declaration-germany.md) |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 全部 |
| **Status**                         | 已弃用：到 2022 年 12 月 1 日，我们将不再支持 **Elster (DE)** 电子报告 (ER) 格式和 **Elster 模型**。 而是在 **税申报** 模型下引入新的 **增值税申报 XML (DE)** 和 **增值税申报 Excel (DE)** ER 格式。 我们也将不再支持 **税务** \> **申报** \> **销售税** \> **电子纳税申报日志** 菜单项和页面、**税务** \> **设置** \> **销售税** \> **电子纳税申报设置** 菜单项和页面、**税务** \> **设置** \> **销售税** \> **电子纳税证书** 菜单项和页面，以及德国报表版式 (TaxReport\_DE) SQL Server Reporting Services (SSRS) 格式。 [电子消息](../general-ledger/electronic-messaging.md)功能支持德国的增值税申报流程。 如需了解更多信息，请参阅[德国增值税申报](../localizations/emea-deu-vat-declaration-germany.md)。 |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes-electronic-ob-declaration-menu-item-and-page-dutch-report-layout-taxreport_nl-ssrs-format"></a>荷兰 OB 申报（基于申报代码设计）、\"电子 OB 申报\"菜单项和页面、荷兰报表版式 (TaxReport_NL) SSRS 格式

[OB 申报](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的增值税申报设计[荷兰增值税申报](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 全部 |
| **Status**                         | 已弃用：到 2022 年 12 月 1 日，我们将不再支持 **OB 申报 (NL)** 电子报告 (ER) 格式和 **OB 申报模型**。 而是在 **税申报** 模型下引入新的 **增值税申报 XML (NL)** 和 **增值税申报 Excel (NL)** ER 格式。 我们也将不再支持 **税务** \> **申报** \> **销售税** \> **电子 OB 申报** 菜单项和页面，以及荷兰报表版式 (TaxReport_NL) SSRS 格式。 [电子消息](../general-ledger/electronic-messaging.md)功能支持荷兰的增值税申报流程。 如需了解更多信息，请参阅[荷兰增值税申报](../localizations/emea-nl-vat-declaration-netherlands.md)。 |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Finance 10.0.20 版本中已经删除或弃用的功能

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>“RTIR 查询发票数据请求 (HU)”电子报告 (ER) 格式配置

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从与匈牙利语在线开票系统互操作的电子消息处理中排除 |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2022 年 4 月 15 日，我们计划不再支持“RTIR 查询发票数据请求 (HU)”格式配置。 |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>“德国审计文件输出”格式下的法国的“法国 FEC 审计文件”电子报告 (ER) 格式

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的“FEC 审计文件 (FR)”格式 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2022 年 5 月 1 日，我们计划不再支持“德国审计文件输出”格式下的法国的“法国 FEC 审计文件”电子报告 (ER) 格式。 而是在“数据导出模型”下引入新的 FEC 审计文件 (FR) 格式。 |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Finance 10.0.17 版本中已经删除或弃用的功能

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>作为电子报告配置的存储选项的 LCS 储存库

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新的监管配置服务 (RCS) 全局存储库 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | Dynamics 365 Finance、Supply Chain Management 和 Project Operations 产品|
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2022 年 4 月 1 日，我们计划不再支持 Microsoft Dynamics Lifecycle Services (LCS) 存储库作为电子报告 (ER) 配置的存储选项。 将发布新的 Microsoft ER 配置，以专门从全局存储库下载。 可以从 Dynamics 365 产品和 RCS 访问全局存储库。 有关详细信息，请参阅[从 RCS 导入 ER 配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)和 [Regulatory Configuration Service - Lifecycle Services 存储弃用](../localizations/rcs-lcs-repo-dep-faq.md)。 |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 版本中已经删除或弃用的功能

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>捷克共和国的“增值税申报 (CZ)”和“控制对帐单导出 (CZ)”电子报告格式

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 替换为新格式 |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2022 年 1 月 22 日，我们计划不再支持“增值税申报 (CZ)”、“控制对帐单导出 (CZ)”电子报告 (ER) 格式。 而是在“税申报”模型下引入新的增值税申报 XML (CZ)、增值税申报 Excel (CZ)、增值税控制对帐单 XML (CZ) 格式。 |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。 而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。 |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>SSRS 格式的英国“VAT 100”报表

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | “税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。 在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。 |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 版本中已经删除或弃用的功能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 不再支持 Internet Explorer 11

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 所有|
| **状态**                         | 已弃用。 2021 年 8 月之后将不再支持 Internet Explorer 11。|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 版本中已经删除或弃用的功能

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>未弃用：波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 非法律要求。  |
| **被另一个功能取代？**   | 是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK） |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 未弃用：我们计划从 2021 年 4 月 27 日开始继续支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。 已经引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。 |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 版本中已经删除或弃用的功能

### <a name="norwegian-standard-main-accounts"></a>挪威标准主科目

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 重新设计  |
| **被另一个功能取代？**   | 是（已被 ER 格式应用程序特定参数取代） |
| **影响的产品区域**         | 申请表 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。 |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 版本中已经删除或弃用的功能

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>“工作流请求更改”对话框中不再包含用户选择下拉列表

| &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 更改为带帐户组选择的功能。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 工作流 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。 请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

