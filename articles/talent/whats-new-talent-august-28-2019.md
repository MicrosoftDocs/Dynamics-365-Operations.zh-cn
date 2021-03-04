---
title: Dynamics 365 for Talent 的新增功能或更改（2019 年 8 月 27 日）
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529796"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Dynamics 365 for Talent 的新增功能或更改（2019 年 8 月 27 日）

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2447。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为生产还是沙盒。 沙盒类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为生产实例类型。 如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](./provisioning-talent.md)。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>在经理自助服务中查看绩效的更多信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>如果员工存在于公司内，则不允许删除法人 (339849)

通过此更改，如果法人存在员工和其他相关数据，则无法移除或删除公司。

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>薪酬管理商业智能分析与薪酬工作区不匹配 (322493)

在此版本中，薪酬分析已经过调整，以准确反映分配给员工的计划。

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>工作流占位符 %company% 在通过工作流招聘员工时显示 DAT (343905)

在此版本中，公司占位符显示与新员工的雇用相关的法人。

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>CDSJobPosition 实体在设置了失效日期时显示错误 (349387)

在此版本中，**CDSJobPosition** 实体上的 **职位详细信息** 和 **职位持续时间** 数据源允许从 Common Data Service 到 **生效日期** 字段的编辑。 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>对于员工终止雇用，工作的最后一天将在分配结束日期填充 (332496)

此更改现在将职位的 **分配结束日期** 默认为 **雇用结束日期**。 您可以在输入数据时更改这些默认值。

### <a name="legal-entities-arent-limited-with-hire-338871"></a>法人不受雇用限制 (338871)
 
此更改将招聘流程限制为仅显示用户有权访问的法人。  

## <a name="in-preview"></a>预览模式

### <a name="streamlined-employee-entry-and-navigation"></a>简化的员工条目和导航

此功能现在可在沙盒和试用环境中使用。 要打开此功能，请导航至 **系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。 选择 **增强的工作人员窗体和导航**。 这为所有用户启用了这些更改。 您可以随时关闭此选项。

有关详细信息，请参阅[简化的员工输入和导航](./streamlined-employee-entry.md)。

## <a name="coming-soon"></a>即将到期

### <a name="platform-update-29"></a>平台 update 29

有关平台更新 29 的其他详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 29（2019 年 10 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]