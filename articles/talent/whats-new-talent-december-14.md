---
title: Dynamics 365 Talent - Core HR（2018 年 12 月 14 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9887d22a513e820c35c51b6c702e2d9d34ab1214
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529748"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Dynamics 365 Talent - Core HR（2018 年 12 月 14 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**内部版本 8.1.2085**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="changes"></a>更改

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>美国 - 纳税年度 2018 1095-B 和 1095-C 窗体的 ACA（平价医疗法案）支持

每年，适用大型雇主 (ALE) 必须为每位全职员工提供 1095-C。 此外，如果雇主提供自保型保险，他们还必须根据所提供的健康计划向任何员工提供 1095-C（如果是 ALE）和 1095-B（如果是小型雇主）。 此功能同时为 1095-C 和 1095-B 提供可打印表单。

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>在导入期间，将忽略 HcmPerfJournalEntity 上的 SubmittedByPersonId 字段

在导入/导出绩效日记帐条目时，**提交者** 字段会被忽略。 通过此更改，值 **已导入/已导出** 将在导出时在表中反映此值，在导入时，系统将更新为导入文件中提供的值。

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>“休假和缺勤”工作区的“分析”选项卡显示非系统管理员角色的“OpenConnectionError”错误

通过此更新，在打开 **休假和缺勤** 工作区的 **分析** 选项卡时，不会发出错误。

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>从磁贴深化的员工自助服务“职位层次结构”无法获取父节点

已进行更改来更正当职位层次结构进行个性化设置以显示在现有工作区中并且在层次结构中选择了一个职位时出现的错误“获取父节点失败”。  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>必须是系统管理员才能够看到职位页面的“工资单”选项卡

已进行了更改以在现有权限中包含正确的安全元素：“维护工资单工作人员和职位详细信息”。 通过此更改，默认情况下，工资管理员将有权访问“职位”页面的“工资单”字段。

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>在向经理提交绩效审核并在提交说明中使用 %Reviews.PerfPeriod% 占位符时出错

已进行更改以更正在提交说明中使用 %Reviews.PerfPeriod% 占位符时出现的“空引用”错误。

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>当工作人员受聘日期是闰日时劳动力 Power BI 报表显示错误

通过此更改，闰日现在在 Power BI 中受支持。

### <a name="integration-between-core-hr-and-attract"></a>Core HR 与 Attract 之间的集成

已进行了更改以更新与要雇用的应聘者相关的 Core HR 与 Attract 之间的集成。 要使将要雇用的应聘者可以显示在 **人员管理** 工作区中，使用以下 Common Data Service 实体：

工作申请
- 状态描述需要设置为“已接受聘约”
-   提供应聘者和空缺职位

应聘者
-   提供应聘者信息

空缺职位
-   提供空缺职位 ID 和空缺职位参与者

空缺职位参与者
-   提供招聘经理

在将应聘者添加到“人员管理”时，应聘者现在还可以使用应聘者卡上的新选项消除。

## <a name="coming-soon"></a>即将到期

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>休假和缺勤：将来的休假和预测的休假余额

随着对允许员工预测休假和申请将来休假请求，而不会影响其当前休假余额的更改，显示休假余额的方式也在更改。 

当前显示的可用余额是包括截至今天的应计在内的可以请求的时间量，以及时间结束前的所有批准的休假请求。 

在预测功能发布时，显示的余额将更改为包括截至今天的应计和请求在内的当前休假余额。 员工和经理将在 **休假** 卡和 **休假余额** 窗口中的员工和经理自助服务中看到这些更新的余额。 HR 经理将在 **人员** 工作区和员工的 **指定休假计划** 窗口中看到这些更新的余额。

## <a name="known-issue"></a>已知问题

### <a name="mapping-errors-in-the-integration-with-finance"></a>Finance 集成中的映射错误

以下问题已在用于将 Talent 与 Dynamics 365 Finance 集成的当前模板中发现。 新模板将很快发布并应用到创建的所有新集成项目中。 对于现有的集成项目，可以更新任务映射。 请参阅下表了解更新的映射。 

>[!NOTE]
> “职位到职位父作业分配”任务不集成数据。 这是当前正在研究的问题。 当前映射没有解决方法。 

“部门到运营单位”任务需要更新以下映射。

| 现有源字段          | 新源字段 |
| -------------------------------|------------------|
| cdm_description（描述）  | cdm_name（名称）  |

还需要添加其他映射。 选择上一个 **无** 字段添加以下映射。

| 源字段                   | 目标字段    |
| -------------------------------|----------------------|
| cdm_description（描述）  | NAMEALIAS (NAMEALIAS)|

更新的映射应如以下图像所示。

![“部门到运营单位”任务](./media/DepartmentMapping.png)


“作业到作业详细信息”任务需要更新以下映射。

| 现有源字段          | 新源字段                   |
| -------------------------------|------------------------------------|
| cdm_name（名称）                | cdm_description（描述）      |
| cdm_name（描述）         | cdm_jobdescription（作业描述）|


更新的映射应如下方图像所示。

![“作业到作业详细信息”任务](./media/JobMapping.png)

“工作人员到工作”任务需要更新以下映射。

| 现有源字段                 | 新源字段                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1（电子邮件地址 1）   | cdm_primaryemailaddress（主要电子邮件地址 |
| cdm_telephone1（电话 1）          | cdm_primarytelephone（主电话）       |

“性别”字段转换也需要更新。 为“性别”选择 **fn**（功能）映射类型并更新以下值映射。

| Common Data Service 值                   | Finance and Operations 值                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | 男                                             |
| 75440001                    | 女                                           |
| 75440002                    | None                                             | 
| 75440003                    | 非特定                                      |

更新的映射应如以下图像所示。

![“工作人员到工作人员”任务](./media/WorkerMapping.png)

![“性别”字段转换](./media/WorkerTransform.png)
