---
title: 设置作业组件
description: 本文介绍工作中可包含的概念性元素，并提供有关如何在组织中使用这些元素的示例。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 69759c0488563a904f6e80afacb1802611ab1930
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430248"
---
# <a name="set-up-the-components-of-a-job"></a>设置作业组件

本文介绍工作中可包含的概念性元素，并提供有关如何在组织中使用这些元素的示例。 

必须先设置一些参考信息，才能创建工作。 创建的工作只能有一个名称。 但是，通过添加更多信息（如职称“，可以为向其分配工作的职位提供默认值。 此外，还可以将输入的一些信息用于筛选特定工作的薪酬计划。 如果要设置可用于筛选特定工作的薪酬计划的资格，应在设置工作之前设置工作职能和工作类型。 通过提供这些默认值，可以在为工作添加职位时节约时间。 

某些工作详细信息（如职称、类型和职能）有时效性。 如果今天创建了工作，但未及时添加这些详细信息，然后在创建日期之后查看该工作，将不显示这些详细信息。 因此，即使暂时不需要这些参考信息，也应该创建其中的一部分。 这样就可以在创建新工作时向其添加这些信息。

## <a name="job-titles"></a>职称
创建工作前，您必须为这些工作设置职称。 职位从这些职位所关联的作业中继承工作职称。 

可使用**职称**页面维护职称，可通过使用搜索功能打开该页面。 在 **职称** 页面中，输入计划用于工作的职称。

## <a name="job-types"></a>工作类型
可使用工作类型将类似的工作分组为类别。 不需要工作类型。 但是，如果您在设置薪酬管理的资格规则时计划使用作业类型，则您应在设置作业前设置作业类型。 例如，工作类型可以是全职、兼职或工资和小时工资。. 可通过使用**工作类型**页面维护工作类型。 在**工作类型**页面中，输入工作类型的名称和简要描述。 在**免除情况**字段中，选择以下选项之一以指示拥有此工作类型工作的公平劳动标准法案 (FLSA) 免除情况。

-   **免除** – 工作从 FLSA 规定下的加班时间中免除。
-   **不免除** – 工作不从 FLSA 规定下的加班时间中免除。
-   **不使用** – FLSA 覆盖范围不适用。

## <a name="job-functions"></a>工作职能
工作职能介绍高级别智能类别，并关联高级别职责。 不需要工作职能。 可以将工作职能与工作类型一起使用，以筛选用于特定工作的薪酬计划。 可以通过在**资格规则**页面中设置资格规则，将工作职能和工作类型与薪酬计划相关联。 然后可以将一组级别附加到应用于工作类型与工作职的特定组合的薪酬计划，该组合是您通过资格规则定义的。 （这些功能适用于固定薪酬计划和可变薪酬计划。）但是，如果您在设置薪酬管理的资格规则时计划使用工作职能，那么应该在设置作业前就设置好工作职能。 下表显示工作职能的一些示例。

| 作业           | 工作职能         |
|---------------|----------------------|
| 销售经理 | 中级经理    |
| 会计师    | 专业人员        |

可通过使用**工作职能**页面维护工作职能。 在**工作职能**页面中，输入工作职能的标识代码和简要描述。

## <a name="job-tasks"></a>作业任务
工作任务描述担任某项工作的职位的工作人员必须完成的基本任务。 同一工作任务可以添加到多个工作，以及使用这些工作任务的工作的职位。 下表显示工作任务的一些示例。

<table>
<thead>
<tr class="header">
<th>作业</th>
<th>作业任务</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>销售经理</td>
<td><ul>
<li><strong>Perf-review</strong> – 查看每个销售人员的作业绩效。</li>
<li><strong>Abs-review</strong> – 批准或拒绝每个销售人员的缺勤请求或登记。</li>
</ul></td>
</tr>
<tr class="even">
<td>会计师</td>
<td><strong>FIN-Report</strong> – 向首席财务官呈交每周财务报表。</td>
</tr>
</tbody>
</table>

可通过使用**工作任务**页面维护工作任务。 在**工作任务**页面中，输入工作任务的名称和描述。 在**注释**字段中，可以选择输入更多信息。 无需更改此处输入的注释，即可针对特定工作更新注释。

## <a name="areas-of-responsibility"></a>职责范围
可使用职责范围指示担任工作的职位的工作人员负责的工作角色、流程和产品。 例如，对于名为“会计师”的工作，一个职责范围可能是“产品 A 的财务申报”。 可通过使用**职责范围**页面维护职责范围，您可以通过使用搜索功能找到此页面。 在**职责范围**页面中，输入职责范围的名称和描述。 在**注释**字段中，可以选择输入更多信息。 无需更改此处输入的注释，即可针对特定工作更新注释。

## <a name="steps-for-creating-a-job"></a>作业创建步骤
请参阅[定义新作业](../fin-and-ops/hr/tasks/define-new-jobs.md)一文了解创建新作业的分步过程。 
