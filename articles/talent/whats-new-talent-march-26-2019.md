---
title: Dynamics 365 Talent（2019 年 3 月 26 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b23860a7eda0ec9d75cca04728b7fc11d01bf967
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812733"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Dynamics 365 Talent（2019 年 3 月 26 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="enhancements-to-interview-scheduling"></a>面试计划增强
面试计划进行了以下增强。

- 招聘人员或招聘经理现在可手动为面试官触发提交反馈提醒。 还可以为提醒配置关联的电子邮件模板。
- 与应聘者共享面试摘要时，面试安排人员可选择隐藏面试官的姓名，还可以选择在面试摘要视图中隐藏行。

## <a name="changes-in-onboard"></a>Onboard 中的更改

### <a name="embedded-images-in-activities"></a>活动中的嵌入图像
现在可直接在活动中嵌入图像。 除了可以复制和粘贴来自 Web 的图像，还可以从本地文件系统上传图像。 图像的大小限制为 1 MB。 如果图像过大，请调整其大小，然后再次尝试上传。

[![地理信息](./media/embedimages.png)](./media/embedimages.png)

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
**内部版本 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>在 Common Data Service 中选择实体时支持自定义字段 

以下 Common Data Service 实体现在支持在 Talent 中创建的客户字段：

- 工作线程
- 所属种族
- 退伍军人状态
- 语言代码
- 职位
- 作业类型
- 工作职能
- 位置
- 职位类型
 
### <a name="employment-history-not-displayed-chronologically"></a>工作经历不能按时间顺序显示
经过此项更改，工作经历页面现在独立于公司按时间顺序显示工作记录。 也可以使用排序选项按公司排序。

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>在安全中按公司限制用户时不显示固定薪酬计划。
在此版本中，在安全中按公司限制用户时现在显示固定薪酬计划。 将遵守所有安全设置，并且将显示用户有权访问的公司的固定薪酬计划。 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>在 Talent 中不能使用“在 Excel 中打开”选项删除工作记录
在此版本中，现在可在 Talent 中通过使用**在 Excel 中打开**选项删除工作记录。

### <a name="upgrade-to-common-data-service"></a>升级到 Common Data Service
很快将到达 Common Data Service 的升级截止时间。 请登录 Power Apps 管理员中心以确定是否需要升级您的数据库。 有关截止时间和必要升级步骤的详细信息，请参阅[升级到 Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)。

## <a name="in-preview"></a>预览模式

有关启用预览功能的信息，请参阅[访问 Microsoft Dynamics 365 Talent 中的预览功能](./access-preview-feature.md)。

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>允许为休假类型指定原因代码
组织可能需要与休假请求有关的更多信息。 若要获取此信息，需要员工在休假请求中加入原因代码。 在此版本中，现在可指定与给定休假类型关联的原因代码，并让员工在休假请求中选择原因代码。

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>配置提交特定休假类型的请假时需要的原因代码。
组织可能会要求当员工提交请假时为特定休假类型设置原因代码。 这可能是基于国家/地区的法规或公司政策的要求。 在此版本中，HR 可以指定哪些休假类型需要原因代码。 当员工提交的休假请求需要原因代码时，将实施此规则。

## <a name="coming-soon"></a>即将到期

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）
在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。 这些记录可能是有关管理层或地区员工的记录。 通过此更改，HR 可以管理和维护组织中不同员工组的薪酬计划。 您可以为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。 只有授予了访问权限的角色才能处理这些员工的薪酬。

###  <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装 Finance and Operations 的平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动为联系人派遣电子邮件通知。 

### <a name="duplicate-employee-checks-user-interface-changes"></a>重复员工检查：用户界面更改
借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。 您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。 为了避免中断数据输入，不会自动打开重复项窗体。
