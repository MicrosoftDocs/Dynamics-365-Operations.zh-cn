---
title: 使用部门、工作和职位组织您的员工
description: 本主题介绍有关部门、工作和职位的概念信息，这些是在人力资源中维护的组织元素。
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 717bf7dcbd9a7e19a6dc960648655fdbd3e2465a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694814"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a>使用部门、工作和职位组织您的员工


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

部门、作业和职位在人力资源中维护的组织元素。 本主题介绍有关这些元素的概念信息。 

以下示例用于说明本文中描述的概念。

|**部门**|**位置**|**作业**|
|---|---|---|
|**销售额**|销售经理（东部）|销售经理|
|**销售**|销售经理（西部）|销售经理|
|**销售**|销售经理（中部）|销售经理|
|**核算**|会计主管|会计经理|
|**核算**|会计-A|会计师|
|**人力资源**|人力资源经理（东部）|人力资源经理|
|**人力资源**|人力资源经理（西部）|人力资源经理|
|**人力资源**|人力资源经理（中部）|人力资源经理|


##  <a name="departments"></a>部门

部门是表示组织的类别或功能区域的运营单位，负责组织的特定区域（例如销售或核算）。 部门用于报告功能区域，并且可能具有损益责任。 此外，部门还可能包括成本中心组。 销售、核算和人力资源部门是组织中的部门的一些示例。

## <a name="jobs-and-positions"></a>作业和职位
作业是执行作业的人员需要承担的任务和责任的集合。 位置是工作的单个实例。 作业所需的职责范围、作业任务、工作职能、技能、教育信息和证书也是与作业关联职位所需的。

### <a name="job-tasks"></a>作业任务

您可以创建描述基本任务的作业任务，位于针对该作业的职位的工作人员必须完成该任务。 同一作业任务可以添加到多个作业，而针对这些作业的职位将继承这些作业任务。 下表中列出了一些工作任务示例。

| 作业           | 作业任务                                                |
|---------------|-------------------------------------------------------------|
| 销售经理 | Perf-review – 查看每个销售人员的作业绩效。    |
| 会计师    | Abs-review – 批准或拒绝每个销售人员的缺勤请求或登记。 |


### <a name="job-functions"></a>工作职能

工作职能就像作业任务。 工作职能描述分配给作业的一个或多个任务、职责或责任。 工作职能可分配给作业并用于设置和实现薪酬计划的资格规则。 下表中列出了一些工作职能示例。

| 作业           | 工作职能                                                |
|---------------|-------------------------------------------------------------|
| 销售经理 | Mng-people – 管理向您报告的人员。               |
| 会计师    | FIN-Review – 维护一组帐户的财务数据。 |

### <a name="job-types"></a>工作类型

使用作业类型将类似的作业分类到各类别。 作业类型就像工作职能一样，可分配给作业并用于设置和实现薪酬计划的资格规则。 下表中包含作业类型的一些示例：
-   全职
-   兼职
-   薪金
-   小时工资

### <a name="areas-of-responsibility"></a>职责范围

使用职责范围指示处于针对该作业的职位的工作人员将负责的工作角色、流程和产品。 名为“会计师”的工作的职责范围的一个示例可能是“产品 A 的财务报告”。

## <a name="positions"></a>位置

职位是更低级别的组织层次结构中的重要元素。 位置是工作的单个实例。 例如，职位“销售经理（东部）”只是与工作“销售经理”关联的职位。 各职位存在于部门中，并分配给工作人员。
### <a name="position-creation-and-maintenance"></a>职位创建和维护

-   您可以在易于访问的列表页中查看与职位先关的系统更改历史记录。
-   您可以创建您的用户可以在创建或修改职位时选择的原因代码。
-   您可以创建人事行动类型并将编号规则分配给人事操作。
-   您可以设置工作流，以便职位添加和更改可要求审核。

### <a name="position-duration"></a>职位持续时间
每个职位都具有职位处于有效状态的时间长度。 此时间长度被称为持续时间。 例如，夏季职位的持续时间可能为 2015 年 5 月 1 日至 2015 年 8 月 31 日。

### <a name="worker-assignments"></a>工作人员分配
在您将工作人员分配到职位时，您填写该职位。 您可以将工作人员分配到多个职位，但一次只能将一名工作人员分配到职位。

### <a name="reporting-relationships"></a>报告关系
职位是更低级别的组织层次结构中的重要元素。 在 **职位** 页面上，您可以指定某个职位向其进行报告的职位。 将工作人员分配到向另一个职位报告的职位时，创建分配给两个职位的工作人员之间的报告关系。 例如，职位“会计师-A”向职位“会计主管”报告。 Ana Bowman 被分配到职位“会计主管”，而 Felix Henderson 被分配到职位“会计师-A”。 这意味着 Felix Henderson 向 Ana Bowman 报告工作。 

如果您的组织使用矩阵层次结构或其他自定义层次结构，则可以设置职位层次结构类型，然后将报告关系添加到您设置的每个层次结构类型的职位。 例如，Olivia Wilson 是 Adventure Works 的总经理，被分配到职位“总经理”。 Olivia 管理用于清洗小机械的产品的开发。 Olivia 要求会计帮助为开发产品融资。 因此，她招聘 Felix Henderson 为会计。 Felix 直接向 Ana Bowman 报告，并与 Olivia Wilson 一起从事其与为开发小机械清洗剂融资相关的工作。 

对于前面的示例，您可以完成以下任务来设置 Felix Henderson 和 Ana Bowman 之间的工作关系：
1.  创建一个名为“小机械”的自定义职位层次结构类型，以创建包括负责从事小机械清洗剂产品工作的职位的层次结构。
2.  在“小机械”层次结构中，将总经理职位分配为会计师-A 职位向其进行报告的职位。

使用 **职位层次结构** 页面查看职位的报告结构。 如果您有多个职位层次结构，则可在 **职位层次结构** 中查看每个层次结构类型的层次结构。 此外，您还可按职位 ID 或分配到职位的工作人员的姓名搜索职位。 **职位层次结构** 是组织层次结构。

## <a name="date-effective-records"></a>生效日期记录
对于某些记录，可以指定对记录的将来的更改。 以下信息是生效日期。

<table>
<thead>
<tr class="header">
<th>记录</th>
<th>生效日期信息</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>作业</td>
<td><ul>
<li>某些详细的作业信息</li>
<li>作业分类信息</li>
<li>薪酬信息</li>
</ul></td>
</tr>
<tr class="even">
<td>位置</td>
<td><ul>
<li>某些详细的职位信息</li>
<li>工作人员分配</li>
<li>职位持续时间</li>
<li>职位层次结构</li>
</ul></td>
</tr>
</tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
