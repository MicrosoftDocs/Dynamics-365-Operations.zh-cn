---
title: Dynamics 365 Human Resources 2021 年 9 月 20 日中的新增功能或更改
description: 此主题介绍了 2021 年 9 月 20 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fd8705c7735cb3c0945f71651fafa767a7addf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691573"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Dynamics 365 Human Resources 2021 年 9 月 20 日中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Microsoft Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4464。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
|---|---|---|
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md) |
| 使员工能够标记为准备支付 | [使员工能够标记为准备支付](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [准备付款](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 | 说明 |
|---|---|---|
| 619774 | 编辑地址说明未实时同步到 Dataverse。 | 编辑工作人员地址的说明时，更新后的说明未实时同步到 Dataverse。 已更新 **物流位置** 表中的订阅以发送更新。 |
| 614603| 未选择 **工作人员人事行动** 参数时 **工作人员** 页面上的错误。 | 雇用新工作人员或导航到 **工作人员** 页面时，显示了以下错误：“必须填写 **人事行动类型**”，即使已关闭 **人事行动** 也是如此。 |
| 615367 | **已批准的休假** 选项卡显示警告并且显示不正确。 | 如果在启用 **配置每个休假类型的休假单位** 功能之前将休假单位设置为 **天**，则 **已批准的休假** 选项卡会显示无效警告和不正确的列。 |


## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关如何开启或关闭的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
|---|---|---|
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 资格中的自定义字段 |[资格处理中的自定义字段支持](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [在资格处理中使用自定义字段](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| 福利报表 |[福利报表](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [福利报表](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>福利报表已知问题

| 问题 | 说明 |
|---|---|
| 福利报表的 **员工自助服务** 中的 **报表参数** 页不正确。 | 在 **员工自助服务** 中导航到 **福利报表** 时，**报表参数** 页面会显示 **要包括的记录** 和 **在后台运行** 快速选项卡。  需要删除这些内容。 |
| 福利报表的 **报表参数** 页中会显示已结束期间和将来期间。 | 导航到 **福利报表报告** 目标页面时，用户能够选择已结束或日期为将来的福利计划期间，这会导致空白页。 列表中仅应显示当前福利计划期间。 |
|通过电子邮件发送使用 GER 报表目标的报表时出错。 | 可将福利报表设置为使用 **GER 报表目标** 页面中的电子邮件参数。 完成设置并打印报表时，用户将收到格式设置错误，并且将不会发送福利报表。|


## <a name="coming-soon"></a>即将推出

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 2 概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)。

| 功能 | 明细 |
|---|---|
| 平台更新 10.0.21 (45) | 计划于 2021 年 10 月 4 日在服务版本中开始推出 平台更新 10.0.21。 有关详细信息，请参阅[财务和运营应用版本 10.0.21 的平台更新（2021 年 10 月）](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21)。 |
|绩效日记帐扩展报表视图 | 此功能将在下一次推出时默认启用。 |


## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 2 波概述](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
