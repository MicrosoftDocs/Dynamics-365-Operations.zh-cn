---
title: Dynamics 365 Talent（2020 年 1 月 21 日）中的新增功能或更改的功能
description: 本文介绍 Microsoft Dynamics 365 Talent 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c0c303ec5d009fce0c975eb797f018b5e27a41eb
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982399"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Dynamics 365 Talent（2020 年 1 月 21 日）中的新增功能或更改的功能

[!include [banner](includes/banner.md)]

本文介绍 Dynamics 365 Talent 中的新增功能或更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。 我们在 Attract 中添加了功能，以支持我们最近的公告：[使用 Dynamics 365 Human Resources 建立更成功的员工队伍](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/)。

### <a name="download-environment-data"></a>下载环境数据

管理员可以下载其环境数据。 数据以标准 JSON 格式导出，所有作业、应聘者和配置均导出为压缩文件。 有关详细信息，请参阅[从 Attract 和 Onboard 导出数据](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)。

### <a name="restricting-access-to-environments-for-non-admin-users"></a>限制非管理员用户对环境的访问

管理员现在可以限制非管理员用户对环境的访问。 此操作无法撤消。 有关详细信息，请参阅[限制对 Attract 的访问](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract)。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

### <a name="exporting-onboarding-guides"></a>导出入职指南

用户现在可以以 Word 文档格式导出其所有入门指南和入门模板。 有关详细信息，请参阅[从 Attract 和 Onboard 导出数据](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data)。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2726。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>“验证雇用”窗体中最近的年度薪酬字段不一致 (392092)

此版本包含一项更改，该更改将根据**验证雇用**窗体上的公司选择器显示最新货币。

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>“称作”字段添加到了“反馈收件人”查找中 (407789)

在提供绩效反馈时，对工作人员的查找没有提供足够的信息来确定反馈是否将发送给正确的人员。 我们添加了一个**称作**列以帮助标识员工的唯一名称。
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>创建了 HcmWorkerPayrollInfo 记录但未与工作人员相关联 (394526)

此版本包括一项更改，以在未引用员工的情况下不写 HCMWorkerPayrollInfo 记录。

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>从职位层次结构导航时可以编辑部门 (341001)

如果已设置安全性以拒绝编辑部门，则在所有情况下导航到**部门**窗体时会禁用编辑。

## <a name="coming-soon"></a>即将到期

一个新的 Common Data Service 解决方案很快将推出，其中包含以下更改：

| 说明 | 找零 |
| --- | --- |
| **工作/职位**实体更改 | <ul><li>添加了**薪酬区域**</li><li>添加了**财务维度**</li></ul> |
| **工作人员**实体更改 | <ul><li>添加了**姓名顺序**</li><li>添加了**在家工作**</li><li>添加了**语言**</li><li>添加了**受聘日期**</li><li>添加了**周年纪念日日期**</li><li>添加了**原始雇用日期**</li></ul> |
| **雇用**实体更改 | <ul><li>添加了**财务维度**</li><li>添加了**离职原因**</li><li>**转变日期**重命名为**离职日期**</li><li>添加了**试用日期**</li></ul> |
| **工作人员地址**实体更改 | <ul><li>添加了**街道地址**</li><li>**地址行 1**、**地址行 2** 和**地址行 3** 标为弃用</li></ul> |
| 新的可变薪酬设置实体 | <ul><li>**可变薪酬计划类型**</li><li>**薪酬可变计划**</li><li>**股份行权规则**</li><li>**可变薪酬计划级别**</li></ul> |
| 新**工作人员日历雇用**实体 | <ul><li>添加了**工作日历实体**</li></ul> |
