---
title: Dynamics 365 for Talent（2019 年 9 月 10 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460441"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Dynamics 365 for Talent（2019 年 9 月 10 日）中的新增功能或更改

此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="candidate-e-mail-login"></a>应聘者电子邮件登录

应聘者现在可使用任何电子邮件地址创建帐户和登录 Talent 就职站点以申请工作和查询其申请状态。 这是对已经可以使用社交帐户或组织凭证登录 Talent 求职站点的补充。

### <a name="job-activation-and-posting"></a>工作激活和发布

我们已经对工作激活和发布进行了一些更改。 您需要向激活工作，才能将工作发布到 Talent 求职站点或任何外部职位面板，包括 LinkedIn 或 Broadbean。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2482。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>可以在沙盒和试用环境中启用预览功能。

配置新的 Talent 实例时，可指定实例类型为生产还是沙盒。 沙盒类型的实例可用于提前测试新功能。 如果需要将现有实例之一更新为沙盒实例类型，请联系支持以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](./provisioning-talent.md)。

### <a name="platform-update-29"></a>平台 update 29

有关平台更新 29 的其他详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 29（2019 年 10 月）中的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29)。

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>数据管理框架中的新可用工作库实体 (347202)

此发行版中推出了一个新的基础工作实体，用于导入/导出数据。 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>工作人员高级安全策略在职位层次结构中显示的职位不正确 (354868)

在此发行版中，用户的访问权限受限时，职位不再显示为开放且具有“空白”工作人员。

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>特定情况下工作窗体关闭框无法关闭窗体 (342467)

此发行版中有一项更改允许在任何情况下关闭工作窗体。

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>对人力资源经理角色锁定员工记录中的新案例 (337111)

由于此项更改，从员工窗体访问案例管理窗体时，不再锁定该窗体。

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>雇用结束日期始终默认为 23:59:59 (351492)

由于此项更改，在手动结束雇用时，您可以将雇用日期更改为非 23:59:59 时间。

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>无法通过数据管理为收入代码设置到期日期 (336604)

在此发行版中，可以通过 **PayrollWorkerPositionEarningCodeEntity** 实体设置将到期的收入代码。

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>员工发展分析报告不显示数据 (348737)

在本周的发行版中，已将员工技能分析更新为提供准确报告。

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>雇用日期/时间的期限不默认为一天的开始 (349101)

由于此项更改，开始日期/时间现在默认为一天的开始，而结束日期/时间默认为一天的结束。

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>在工作人员操作窗体中更改雇用结束日期会显示错误 (354092) 

此项更改更正了在工作人员操作中修改雇用结束日期时出现的问题。

### <a name="applying-onboarding-checklists-across-companies-338433"></a>在公司范围内应用入职核对清单 (338433)

此发行版现在可以为法人中，而不是在已登录法人中雇用的员工应用核对清单。

## <a name="in-preview"></a>预览模式

### <a name="streamlined-employee-entry-and-navigation"></a>简化的员工条目和导航

此功能现在可在沙盒环境中使用。 要打开此功能，请导航至 **系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。 选择 **增强的工作人员窗体和导航**。 这将为所有用户启用这些更改。 您可以随时关闭此选项。

有关详细信息，请参阅[简化的员工输入和导航](./streamlined-employee-entry.md)。
