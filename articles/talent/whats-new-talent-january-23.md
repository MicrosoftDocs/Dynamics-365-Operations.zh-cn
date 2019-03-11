---
title: Dynamics 365 for Talent Core HR（2019 年 1 月 23 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 135be837a82af8cee22d83c015a78da3b89b7978
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303358"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Dynamics 365 for Talent Core HR（2019 年 1 月 23 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

**内部版本 8.1.2121**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="changes"></a>更改

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>创建新的固定薪酬记录时导入员工固定薪酬不工作
对员工固定薪酬实体进行了更改以在导入后检索薪酬级别。 在此版本前，将显示一条消息，指示需要级别。

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>从请假对话框中删除最小余额字段
已从**请假**对话框中删除了**最小余额**字段。 此更改会影响可以请假的所有区域。

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>薪酬级别的数据升级未在所有方案中更新
已进行了更改以更新固定薪酬计划中的薪酬级别。 此更改将填充分配给员工的工作的固定计划中的薪酬级别。

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>管理更改页面的工资单信息仅在作为系统管理员登录后可用
此更改允许具有工资管理员角色的员工在职位的**更改日程表 > 管理更改**页访问工资单信息。

### <a name="job-fields-default-to-positions"></a>工作字段默认为职位
在更改职位中的工作时，工作字段将默认为职位。 预警消息将显示，提供接受默认值或保留这些字段的现有值的选项。

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>试用期和日历没有为将来雇用的员工显示。
通过此更改，**试用期**和**日历**字段已添加到**管理更改**页以允许将来以及过去员工的数据输入。

### <a name="platform-update-23"></a>平台 update 23
细微缺陷修复作为平台更新 23 的一部分包括在内。 有关详细信息，请参阅 [Dynamics 365 for Finance and Operations 平台更新 23（2019 年 1 月）的新增功能和更改内容](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23)。 
