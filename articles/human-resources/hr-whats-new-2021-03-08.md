---
title: Dynamics 365 Human Resources 中的新增功能或更改（2021 年 3 月 8 日）
description: 此主题介绍 2021 年 3 月 8 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b1e616f9bc72ab1f30f69671c673241096f3276
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687859"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Dynamics 365 Human Resources 中的新增功能或更改（2021 年 3 月 8 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4017。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 经理跨公司查看休假 | [经理跨公司查看员工休假](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [配置休假和缺勤参数](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 签发 |  说明 |
| --- | --- | --- |
| 486611 | 当 **在所有日历上禁用休假** 启用时，休假显示在休假日历上 | 如果启用了 **在所有日历上禁用休假**，在启用“休假和缺勤日历”增强功能时，休假信息将不再显示。|
| 508972 | 假期和缺勤银行交易实体缺少登记验证 | 使用休假和缺勤银行交易实体时，无法再导入未在计划中登记的员工。 |
| 554854 | 如果用户选项中的默认法人不同，更新雇用实体中的日历将出错 | 如果用户选项中的默认法人不同，使用雇用实体为员工更新日历不会再发生错误。 |
| 558347 | 加载启动页时，出现“无法在窗体配置中创建记录 (FormRunConfiguration)”。 | 加载启动页时，个性化设置将导致出现错误“无法在窗体配置中创建记录 (FormRunConfiguration)”。 |
| 557327 | 福利管理工作区：网格上方出现间隙。 | 修复了福利工作区中表格网格边框上出现意外间隙的用户体验问题。 |
| 557334 | 福利管理工作区：**期间** 选择下拉框应该仅出现在 **摘要** 选项卡中 | 现在，仅当福利工作区中的 **摘要** 选项卡处于活动状态时，才显示福利 **期间** 选择下拉框，而不会出现在 **处理结果** 和 **链接** 部分。 |
| 557336 | 福利管理工作区：**有已签出计划的打开的登记** 文本在磁贴视图中被截断 | 将磁贴视图中的文本更改为 **已检出计划...打开的登记** 以避免截断必要的上下文。 |

## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 限制员工编辑业务联系人详细信息 | [限制员工编辑业务联系人详细信息](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 经理为员工输入的技能可以通过工作流自动审核 | 即将推出。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]