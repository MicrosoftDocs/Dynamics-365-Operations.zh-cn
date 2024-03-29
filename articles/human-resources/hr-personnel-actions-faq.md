---
title: 人事行动常见问题
description: 如果您的组织使用人事行动，本文包括对可能有的问题的解答。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8882fd00c68dc3cafcb4ecf1b2fe351a9e7f5741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874298"
---
# <a name="personnel-actions-faq"></a>人事变动常见问题解答


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

如果您的组织使用人事行动，本文包括对可能有的问题的解答。 人事行动是执行特定与人事相关任务时必须完成的附加步骤。 

可能需要人事行动的任务示例如：
 - 当您创建新职位时。 
 - 修改现有职位值。 
 - 雇用新的工作人员。 
 - 转移工作人员。 
 - 更改工作人员薪酬。 
 - 更改职位分配。 
 - 使工作人员离职。

> [!NOTE]
> 仅当 **人力资源共享参数** 页上的 **人事行动** 选项卡中的 **启用工作人员变动** 和 **启用职位变动** 字段设置为 **是** 时，人事行动才可用。 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>如何判断我的组织是否需要人事行动？
当您创建新职位、更改现有职位、雇用新工作人员、转移工作人员、更改工作人员薪酬、更改职位分配、中止人员或工作人员入职离开时，如果要求您选择人事行动，则您的组织需要人事行动。 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>职位行动和工作人员行动之间有何差异？
有两种人事行动类型：

- **职位** 行动 –对现有职位或新职位执行职位行动。 例如，如果更改现有职位上的值或创建新的季节职位时，可能需要职位行动。 

- **工作人员** 行动 – 对现有员工或新员工执行工作人员行动。 例如，当雇用新员工或提升现有员工时，可能需要工作人员行动。 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>人事行动状态的意思是什么？
人事行动可具有以下状态：

- **草稿** – 如果使用了工作流，未提交行动。 如果不使用工作流，未完成行动。
- **正在审核** –人事行动已提交到工作流，但工作流未完成。
- **等待批准** – 工作流已完成，但仍在处理更改。 **已取消** – 工作流已取消或人事行动已撤回。 **已拒绝** – 审批者否决行动请求。
- **处理行动** –行动请求已得到批准，正在处理更改。
- **工作流已完成** –工作流已完成，更改已处理。 **失败** – 因为信息过期导致工作流失败。 单击 **重新启用** 以显示最新信息并继续。
- **已完成** –已成功创建或修改职位，或者成功雇用、转移、解雇员工或更改其薪酬。 **错误** – 由于除信息过期以外的其他原因导致的问题。 打开 **人事行动消息日志** 以确定出错原因。
- **已拒绝** –批准人拒绝行动请求。

## <a name="can-i-delete-a-personnel-action"></a>我是否可以删除人事行动？
您可以删除状态为 **草稿**、**错误**、**失败** 或 **已取消** 的人事行动。 仅可以在 **Human Resources 共享参数** 页面上 **允许删除完成的工作人员行动** 选项已设置为 **是** 时，才删除具有 **已完成** 状态的人事行动。

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>检查人事行动请求状态的最快捷方法是什么？
打开任何 **人事行动** 列表页然后选择一个人事行动。

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>如果人事行动请求失败，我该做什么？
如果人事行动请求失败，请执行以下步骤解决错误并重新提交请求：

> 1. 在 **操作窗格** 上单击 **错误文本** 按钮查看描述问题的消息文本。
> 
> 2. 在 **操作窗格** 上单击 **重新启用** 可加载最新信息并将人事行动状态设置回 **草稿**。
> 
> 3. 解决该错误，然后单击 **完成** 或 **提交**。

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>当完成最终批准时使用工作流，人事行动会发生什么？
如果没有任何错误，人事行动变为只读。 （您可以查看有关 **所有工作人员行动** 列表页面上的历史记录，不过，您不能更改人事行动。）当人事行动的状态为 **已完成** 时，职位或工作人员记录已更新。 若要查看已执行的更改，可打开 **职位** 或 **工作人员** 列表页。

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>当我在付费率字段中输入一个非零值时，为何受到如下错误？ “该值不在其有效范围内 - 它必须介于 0.00 和 0.00 之间”
收到此消息是因为 **工作** 页中的 **级别** 字段对于与所选职位关联的工作为空。

为了解决此错误，请执行以下步骤：

> 1. 在 **工作人员职位分配** 页上，单击 **职位** 字段。  
> 2. 单击 **工作** 字段值打开 **工作** 页。
> 3. 在操作窗格中单击 **编辑**。
> 4. 单击 **薪酬** 选项卡。
> 5. 在 **级别** 字段中选择一个级别。
> 6. 关闭 **工作** 页面。
> 7. 关闭 **职位** 页面。
> 8. 返回到 **工作人员** 页上的 **薪酬** 选项卡，选择 **固定薪酬**。  在 **职位** 字段中选择 **新建** 并输入员工的职位。  在 **计划** 字段中输入一个值，然后在 **付薪比率** 字段中输入员工的薪酬。

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>为什么无法在工作人员行动页的标头中更改生效日期？
因为使用行动类型的最合理日期填充该字段，因此不能更改生效日期。

例如：

- **解雇工作人员** 操作的标题的生效日期是您在 **终止日期** 字段中输入的日期。
- **雇用工作人员** 操作的生效日期是您在 **雇用开始日期** 字段中输入的日期。
- **转移工作人员** 操作的生效日期是您在 **分配开始日期** 字段中输入的日期。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
