---
title: Dynamics 365 Human Resources（2020 年 3 月 3 日）中的新增功能或更改
description: 本文介绍 2020 年 3 月 3 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4007daa51d661a2a6b67c323cfaf05c22543371
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128010"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Dynamics 365 Human Resources（2020 年 3 月 3 日）中的新增功能或更改

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2955。 某些标题中括号内的数字是 LCS 支持号码，供您参考。

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse 现已可用，并具有以下更改：

一个新的 Dataverse 解决方案很快将推出，其中包含以下更改：

| 说明 | 找零 |
| ----------------------------------------- | --- |
| **工作/职位** 实体更改 | 添加了 **薪酬区域**</br>添加了 **财务维度** |
| **工作人员** 实体更改 | 添加了 **姓名顺序**</br>添加了 **在家工作**</br>添加了 **语言**</br>添加了 **受聘日期**</br>添加了 **周年纪念日日期**</br>添加了 **原始雇用日期** |
| **雇用** 实体更改 | 添加了 **财务维度**</br>添加了 **离职原因**</br>**转变日期** 重命名为 **离职日期**</br>添加了 **试用日期** |
| **工作人员地址** 实体更改 | 添加了 **街道地址**</br>**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用 |
| 新的可变薪酬设置实体 | **可变薪酬计划类型**</br>**薪酬可变计划**</br>**股份行权规则**</br>**可变薪酬计划级别** |
| 新 **工作人员日历雇用** 实体 | 添加了 **工作日历实体** |
| 新 **工资单职位详细信息** 实体 | 添加了 **工资单职位详细信息** |
| 新 **职务** 实体 | 添加了 **职务**。 Human Resources 与 Dataverse 之间的同步流程中将包含新的 **职务** 实体。 其最初不是从 **工作职位** 或 **工作** 实体引用的。 |

在接下来的数周内，所有环境中将支持这些实体更改。 若要手动插入适用于 Human Resources 的最新 Dataverse 解决方案：

1.  转到 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com)。

2.  选择 **环境**。

3.  找到要升级的环境。 此环境应该对应于 Human Resources 中 **关于** 窗体内 **Common Data Service 信息** 部分中的 **环境名称**。

4.  选择环境以查看环境详细信息。

5.  在顶部的操作栏中选择 **管理解决方案**。 将打开一个新的浏览器窗口，并在您的环境的上下文中导航到 **Dynamics 365 管理中心**。

6.  在 **解决方案** 列表中，选择 **Dynamics 365 Human Resources 定位点**。

7.  选择 **升级** 应用最新解决方案。

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>休假等记数据实体的导入问题 (406082)

现在只要新等记日期晚于前一个计划的已到期登记日期，即可在同一类型的休假计划中为员工等记。

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>DMF 中 401k payrollWorkerEnrolledBenefitDetail 实体类导出贡献率时的问题 (420700)

此更改更正了 **payrollWorkerEnrolledBenefitDetail** 实体的导出功能，现在可以体现员工的当前贡献值。

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>在简化的工作人员窗体中进行搜索将导致“必须填写人员字段”消息 (402525)

搜索员工时，不再会收到有关必须填写 **人员** 字段的消息。

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>“添加更多技能”窗体中不显示“注释”字段值 (380134)

此更改解决了个性化员工自助服务中的 **添加更多技能** 窗体时的问题。

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>转移员工时多个固定薪酬计划不到期 (389466)

通过此更改，原职位的所有活动固定薪酬记录将在转移日期到期。

## <a name="in-preview"></a>预览模式

以下预览功能已于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="see-also"></a>请参阅

[Human Resources 中新增或更改的功能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]