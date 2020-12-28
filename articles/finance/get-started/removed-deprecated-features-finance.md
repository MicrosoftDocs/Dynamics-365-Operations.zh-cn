---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689486"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 版本中已经删除或弃用的功能

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>比利时的“分类帐交易导出格式 (BE)”电子申报格式和相应的“分类帐交易导出 (BE)”模型

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 在“标准审核文件 (SAF-T)”模型下替换为了新的 ER 格式。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2021 年 12 月 1 日，我们计划不再支持“分类帐交易导出格式 (BE)”电子申报 (ER) 格式和相应的“分类帐交易导出 (BE)”模型。 而是在“标准审核文件 (SAF-T)”模型下引入新的“总帐数据导出 (BE)”格式以及“总帐数据模型映射”。 |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>SSRS 格式的英国“VAT 100”报表

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | “税申报模型”下已替换为新的 ER 格式 -“增值税申报 Excel (UK)”格式。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 申请 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：到 2021 年 12 月 1 日，我们计划不再支持 SSRS 格式的“增值税 100 报表”。 在 [MTD 增值税功能](../localizations/emea-gbr-mtd-vat-integration.md)中“税申报模型”下引入了新的“增值税申报 Excel (UK)”格式。 |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 版本中已经删除或弃用的功能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 不再支持 Internet Explorer 11

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品不再支持 Microsoft Internet Explorer 11，2021 年 8 月之后，不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户过渡到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 所有|
| **状态**                         | 已弃用。 2021 年 8 月之后将不再支持 Internet Explorer 11。|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 版本中已经删除或弃用的功能

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>波兰语 SSRS 报表：销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 非法律要求。  |
| **被另一个功能取代？**   | 是（包含增值税申报的标准审计文件的 Excel 格式 - JPK_VDEK） |
| **影响的产品区域**         | 申请表 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：我们计划从 2021 年 7 月 1 日开始不再支持 SSRS 报表：**销售增值税登记簿、采购增值税登记簿、欧盟增值税汇总登记簿 – 功能引用 PL-00014**。 将改为引入包含增值税申报的标准审计文件的 Excel 格式示例 (JPK_VDEK)。 |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 版本中已经删除或弃用的功能

### <a name="norwegian-standard-main-accounts"></a>挪威标准主科目

|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 重新设计  |
| **被另一个功能取代？**   | 是（已被 ER 格式应用程序特定参数取代） |
| **影响的产品区域**         | 申请表 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：我们计划从 2021 年 4 月 1 日开始不再支持与标准主科目有关的功能：“引用”字段、相关表、数据实体。 |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 版本中已经删除或弃用的功能

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>“工作流请求更改”对话框中不再包含用户选择下拉列表
|   |  |
|------------|--------------------|
| **弃用/移除的原因** | 更改为带帐户组选择的功能。  |
| **被另一个功能取代？**   | 是 |
| **影响的产品区域**         | 工作流 |
| **部署选项**              | 所有 |
| **状态**                         | 弃用：到 2020 年 12 月 1 日，我们计划不再支持不带帐户组选择的中国凭证类型设置。 请在 [10.0.7 的新增功能](whats-new-changed-10-0-7.md)中查找有关新设计的更多详细信息。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)。
