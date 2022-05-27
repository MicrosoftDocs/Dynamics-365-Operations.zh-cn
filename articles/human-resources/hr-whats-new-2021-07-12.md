---
title: Dynamics 365 Human Resources 的新增功能或更改（2021 年 7 月 12 日）
description: 此主题介绍了 2021 年 7 月 12 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c01d00e7ede44c20e64fc4a8cd8646201caa3992
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686790"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Dynamics 365 Human Resources 的新增功能或更改（2021 年 7 月 12 日）

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍了 Dynamics 365 Human Resources 中的新增、更改或即将推出的功能。

有关更新流程和计划的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。

有关新功能及其预计的正式发布日期的详细信息，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="in-this-release"></a>在此发布中

此发布中包含以下新功能和缺陷修复。 更改适用于内部版本号 8.1.4353。

### <a name="new-features"></a>新功能

此发布通常提供以下功能。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
|  服务年限显示切换 | |此功能提供使用不同日期计算在 **简化的员工输入** 页面和 **人员** 页面显示的服务年限的选项。  这将在 [Human Resources 参数](/dynamics365/human-resources/hr-setup-parameters)中提供。 |


### <a name="bug-fixes"></a>缺陷修复

此发布中包含以下缺陷修复。

> [!NOTE]
> 我们的目标是尽快为您提供此信息。 我们可能会更新本主题，以包含在最初发布本主题之后将其纳入内部版本的缺陷修复。

| 问题编号 | 问题 |  说明 |
| --- | --- | --- |
| 595871 | Human Resources 中的“关于”窗格包含不正确的 Dataverse 术语 | 通过将 Common Data Service 更名为 Dataverse，Microsoft Dynamics 365 Human Resources 信息窗格中的术语已更新（**帮助和支持 > 关于**）。 |
| 598676 | 简化的员工输入窗体覆盖任务在使用“已保存视图”时可能会产生错误| 在 **工作人员** 页面，如果启用了“简化的员工输入”功能，在已保存视图上设置 **始终打开以进行编辑** 时，应用程序可能会失败。 |
| 592344 |仅当启用福利管理时，才会读取职位上的员工薪酬部分 | 员工薪酬信息是使用旧福利功能创建的。  启用福利管理后，字段将是只读的。 当福利管理打开且 HR 共享参数中的 **隐藏旧版福利窗体** 设置为 **是** 时，**员工薪酬** 选项卡将隐藏。 |
| 598617 | **HcmDiscussion** 窗体激活选项卡在应用个性化时导致无限循环 | 当网格和详细信息视图都启用 **始终打开以进行编辑** 时，在覆盖的任务方法中激活选项卡的代码与哪些控件应该具有焦点的个性化相冲突，并创建一个无限循环。 |
| 593553 | 绩效日记帐中的日记帐日期字段以 UTC 显示 | 绩效日记帐的 **日记帐日期** 字段以 UTC 时区显示，而不是系统日期设置中定义的时区，导致某些时区的日期不正确。 |
| 586930 | 为绩效目标打开活动打开了一个完全不同的记录 | 在“功能管理”中启用“绩效日记帐间接下属视图”功能后，在 **员工自助服务** 中的 **我的团队** 选项卡上选择间接下属的绩效目标，会打开某个员工而不是选定员工的目标。 |
| 569959 |  HcmPositionWorkerAssignmentV2 实体未将工作人员分配到职位 | 用户通过实体添加职位分配记录、发布失败时收到错误。 |
| 582259 | VETS 4212 报表使用 2017 窗体而不是 2020 窗体 | 已更新为 2020 格式。  要加载新格式，请转到 **报表配置**，删除左栏中的 VETS-4212 报表。 转到 **电子报告 - 存储库 - HR 资源**，选择 **打开**。  选择 **VETS-4212 PDF 打印输出**，然后选择 **导入**。|


## <a name="in-preview"></a>预览模式

以下新功能处于预览状态。 有关打开或关闭功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

| 功能 | 发布计划 | 文档 |
| --- | --- | --- |
| 福利管理工作区 | [福利管理工作区（预览）](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [福利管理工作区](hr-benefits-management-workspace.md) |
| 启用简化的工资单集成（工资单集成 API） | [启用与工资单提供商的简化集成](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [工资单集成 API](hr-admin-integration-payroll-api-introduction.md)|
|  让缺勤管理人员能够管理休假 | [让缺勤管理人员能够管理休假](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [配置缺勤管理人员角色](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  配置每个休假类型的附件要求 | [配置每个休假类型的附件要求](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  配置每个休假类型的休假单位 | [配置每个休假类型的休假单位](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[配置休假和缺勤类型](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 使员工能够标记为准备支付 | [使员工能够标记为准备支付](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [准备付款](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>即将推出

| 功能 | 明细 |
| --- | --- |
| 平台更新 10.0.20 (44) | 平台更新 10.0.20 计划于 2021 年 7 月 26 日在服务版本中开始推出。 有关详细信息，请参阅[财务和运营应用版本 10.0.20 的平台更新（2021 年 8 月）](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20)。 |

有关计划功能及其计划发布的完整列表，请参阅 [Dynamics 365 Human Resources 2021 年发布波次 1 概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)。

## <a name="see-also"></a>请参阅

[Human Resources 中的新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 发布第 1 波概述](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
