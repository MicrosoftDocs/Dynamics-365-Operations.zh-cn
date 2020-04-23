---
title: Dynamics 365 Finance 中已删除或弃用的功能
description: 本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
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
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175100"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

本主题介绍 Dynamics 365 Finance 中已经删除或计划删除的功能。

- *已移除*的功能在产品中不再可用。
- *已弃用*的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)中提供了有关 Finance and Operations应用中的对象的详细信息。 可比较这些报告的不同版本，以了解 Finance and Operations 应用各版本中已更改或已删除的对象。

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
