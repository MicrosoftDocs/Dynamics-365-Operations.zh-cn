---
title: “时间和出勤”中的缺勤登记
description: 本文说明如何处理“时间和出勤”中的缺勤登记。
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a613edbe42d1bfb1d2ee43ee1cb2f1e0ab49a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890761"
---
# <a name="absence-registration-in-time-and-attendance"></a>“时间和出勤”中的缺勤登记

[!include [banner](../includes/banner.md)]

本文描述缺勤的概念并说明如何处理“时间和出勤”中的缺勤。

## <a name="absence-that-is-based-on-regular-work-hours"></a>基于正常工作时间的缺勤

工作人员在其正常工作时间不工作的任何工时都被视为缺勤。 正常工时在工作人员的标准时间模板中定义。

例如，工作人员使用的工作日模板的上班打卡时间是上午 7:00，下班打卡时间是下午 3:00。 如果工作人员在上午 9:00 打卡，他在当天上午 7:00 到 9:00 这段时间会被视为缺勤。

在这种情况下，工作人员会被提示输入其缺勤原因。 他们可以通过选择考勤代码来指定原因。

## <a name="absence-codes"></a>考勤代码

缺勤代码定义缺勤的各种类型。 缺勤代码由公司定义。

缺勤代码可能应用不同规则。 例如，可以将缺勤代码配置为扣减或准予付薪。

例如，公司定义了工作人员在迟到且没有正当理由时使用的 **迟到** 缺勤代码。 公司还定义了工作人员用于参加内部课程所花费时间的 **内部课程** 缺勤代码。 这些缺勤代码可以进行设置，以便 **迟到** 时从工作人员的付薪中减扣，而 **内部课程** 不减扣。

您可以设置自动缺勤代码。 这些缺勤代码可用于在未登记缺勤时计算工作人员的工时。 工作人员的时间模板确定是使用标准工时还是弹性工时的缺勤代码。

### <a name="set-up-standard-time-and-flex-time"></a>设置标准工时和弹性工时

- 通过使用 **时间和出勤参数** 页的 **自动插入缺勤** 和 **自动插入弹性-** 选项来配置标准工时和弹性工时的参数。

## <a name="absence-groups"></a>缺勤组

缺勤代码被分组到缺勤组。 您可以使用缺勤组将具有共同特征的缺勤代码分组。 示例包括正常缺勤或由于看医生、陪审员义务或孩子生病所导致缺勤的缺勤代码。

## <a name="planned-absence"></a>计划缺勤

如果您知道某个工作人员将在某个时间段内缺勤（如预计休假），您可以使用计划缺勤。 您通过配置考勤代码来设置计划缺勤，以便考虑计划缺勤。 在设置计划缺勤时，当计算用户工时登记时不会向您提示该缺勤期间的缺勤代码。 计划缺勤可针对单个工作人员定义，也可以定义批处理作业来批量更新多名工作人员的计划缺勤。

### <a name="set-up-planned-absence"></a>设置计划缺勤

1. 选择 **人力资源**&gt;**工作人员**&gt;**员工**，然后选择一名员工。
2. 选择 **时间**&gt;**分配时间** &gt;**缺勤时间登记**，然后设置计划缺勤。

## <a name="interrupted-planned-absence"></a>中断的计划缺勤

如果您在设置计划缺勤时应用 **中断** 选项，那么当工作人员在计划缺勤期间登录，该计划缺勤将被中断。 计划缺勤将被标记为 **中断**，这不会对将来计算造成任何影响。

### <a name="set-up-a-planned-absence-for-interruption"></a>设置要中断的计划缺勤

1. 打开 **缺勤时间登记** 页，如设置计划缺勤的过程中所述。
2. 选择 **中断**。

在工时通过车间终端或车间设备登记时应用 **中断** 选项。 如果登记在计算和审核页面或 **电子工时记录卡** 页输入，则不应用此选项。

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>在弹性模板中使用缺勤的示例

以下三个示例显示如何在具有弹性期间的模板中计算缺勤。

这些示例使用以下模板。

| 上班打卡 | 标准时间    | 休息             | 标准时间 | 弹性-        | 下班打卡 | 弹性+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 上午 8 点     | 上午 9 点到 11:30 | 中午 11:30 到 12 点 | 中午 12 点到下午 3 点 | 下午 3 点到 4 点 | 下午 4 点      | 下午 4 点到 6 点 |

### <a name="example-1-signing-out-during-a-flex--period"></a>示例 1：在“弹性-”期间注销

工作人员在上午 8:00 上班打卡，在下午 3:30 下班打卡。 在这种情况下，因为工作人员在“弹性-”期间下班打卡，不会计算缺勤时间，将从工作人员的弹性结余中扣减半小时。

### <a name="example-2-signing-out-in-during-standard-time-period"></a>示例 2：在“标准时间”期间注销

工作人员在上午 8:00 上班打卡，在下午 2:30 下班打卡。 在这种情况下，因为工作人员在“标准时间”期间注销，从下午 2:30 到 4 点将被计算为缺勤时间，并会登记 1.5 小时的缺勤时间。 需要填写该期间的缺勤代码。

### <a name="example-3-signing-out-during-a-flex-period"></a>示例 3：在“弹性+”期间注销

工作人员在上午 8:00 上班打卡，在下午 4:30 下班打卡。 在这种情况下，因为工作人员在“弹性+”期间下班打卡，不会计算缺勤时间，工作人员的弹性结余将增加半小时。

## <a name="absence-in-the-calculation-and-approval-process"></a>计算和审核流程中的缺勤

必须先计算和审核工作人员工时登记，然后才能将其作为付薪项转移到工资系统。

审核人可以更改工作人员的工时登记。 审核人甚至可以更改工作人员已登记的任何缺勤。 如果审核人手动输入具有缺勤代码的时段，则该期间的缺勤代码不会被“时间和出勤参数”中的默认缺勤代码覆盖。

例如，工作人员在上午 10 点上班打卡并选择指示他迟到的缺勤代码。 后来，该工作人员告知他的主管他从上午 8 点到 10 点之间是去看医生。 看医生不应扣减工作人员的付薪。 因此，在这种情况下，主管可以手动输入指示这两个小时是病假的缺勤代码，以此来调整从上午 8 点到 10 点的两小时缺勤。

### <a name="calculate-and-approve-absence"></a>计算和审核缺勤

- 选择 **出勤时间** &gt; **查看和审核** &gt; **审核或计算**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]