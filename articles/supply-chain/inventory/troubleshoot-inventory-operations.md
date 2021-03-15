---
title: 库存操作故障排除
description: 此主题介绍如何解决使用库存操作时可能遇到的问题。
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967147"
---
# <a name="troubleshoot-inventory-operations"></a>库存操作故障排除

[!include [banner](../includes/banner.md)]

此主题介绍如何解决使用库存操作时可能遇到的问题。

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>我找不到库存日记帐的“工作流”下拉对话框。

### <a name="issue-description"></a>问题描述

在日记帐页上找不到 **工作流** 下拉对话框，或相关的工作流操作不可用。

发生此问题可能由于三个原因，如以下小节所述。

### <a name="issue-resolution-1"></a>解决问题 1

如果问题适用于所有用户，可能是由于未将审批工作流分配给日记帐名称。 若要解决此问题，请按照以下步骤操作。

1. 转到 **库存管理 &gt; 设置 &gt; 日记帐名称 &gt; 库存**。
1. 在列表窗格中，选择一个日记帐名称来打开其设置。
1. 在 **常规** 快速选项卡上，将 **审批工作流** 选项设置为 *是*。 如果提示确认更改，选择 **是**。
1. 在 **工作流** 字段中，选择要用于所选日记帐名称的工作流。

### <a name="issue-resolution-2"></a>解决问题 2

如果您的工作流使用自定义代码，在升级系统后可能会出现问题。 例如，在日记帐工作流中，**提交** 按钮可能为灰色，因此您无法选择它来审批提交。

如果 **提交** 按钮是灰显，您的工作流可能已自定义，这意味着工作流的方法 `FormDataUtil` 中的 `canSubmitToWorkflow()` 已扩展。 要解决此问题，更改您扩展 `canSubmitToWorkflow()` 方法的方式以使用以下示例中的结构。

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>解决问题 3

如果此问题仅适用于少数几个特定用户，有可能是这些用户没有对库存日记帐运行工作流操作所需的安全特权。 请验证是否每个受影响的用户都有 *维护库存日记帐工作流* 安全特权。 默认情况下，此特权分配给具有相同名称的职责，该职责适用于 *仓库工作人员* 和 *仓库经理* 角色。

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>我的库存日记帐停留在系统锁定状态，工作流批处理作业不工作。

### <a name="issue-description"></a>问题描述

您的其中一个库存日记帐被某个操作锁定，没有解锁。 例如，如果在过帐过程中发生未知错误（这是系统锁定操作），日记帐可能保持系统锁定状态。 在这种情况下，工作流工作项处理程序在进行锁定验证时将抛出错误。

### <a name="issue-resolution"></a>解决问题

请登录到 Supply Chain Management 的 SQL Server 实例，检查 **InventJournalTable.SystemBlocked** 是否设置为 *1*。 如果是，请确保该日记帐不应该处于锁定状态，然后将 **InventJournalTable.SystemBlocked** 重置为 *0*。

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>我的库存日记帐工作流一直没有完成，日记帐无法编辑或过帐。

### <a name="issue-description"></a>问题描述

提交日记帐审批工作流后，工作流处理将停止响应，您无法编辑或处理日记帐。

### <a name="issue-resolution"></a>解决问题

有几种原因可能导致工作流处理无法完成。 请检查以下问题：

- 转到 **库存管理 &gt; 设置 &gt; 库存管理工作流**，查看受影响的工作流的配置。 有关详细信息，请参阅[库存日记帐审批工作流](inventory-journal-workflow.md)。
- 工作流可能遇到异常或错误。 查看受影响的工作流的工作项历史记录是否包含终止工作流的应用程序错误。
- 库存日记帐只有在获得批准后才能进行更新或编辑。 如果撤回可用，您可以尝试撤回日记帐。 工作流批处理作业的执行可能由于多个原因被暂停。 有些原因可能是由工作流框架问题引起的。

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>库存日记帐工作流条件只能在日记帐级别应用，不能在行级别应用

### <a name="issue-description"></a>问题描述

比如，如果您尝试对成本金额设置库存日记帐工作流条件，可能会遇到此问题。 您设置此条件，让步骤 1 仅在成本金额小于 100 时运行。 然后设置另一个条件，让步骤 2 仅在成本金额大于或等于 100 时运行。 然后，在工作流运行时，工作流历史记录将仅显示一行，第一个条件始终计算为 *true*，无论提交什么值。

### <a name="issue-workaround"></a>问题解决方法

在当前版本中，日记帐工作流条件只在日记帐级别应用，不在行级别应用。 此为有意行为。 我们建议您仅对日记帐级属性设置条件。

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>现有量列表页上的筛选器窗格没有按我预期的那样筛选结果。

### <a name="issue-description"></a>问题描述

**现有量列表** 页上筛选器窗格中的筛选器没有按您预期的那样筛选结果。

### <a name="issue-resolution"></a>解决问题

此为有意行为。

 **现有量列表** 页是从包含所有可用维度的详细现有库存量表组合而成的。 但是，此页面上的列表是一个摘要。 因此，它可能根据显示的维度通过聚合值来合并源表中的行。

在筛选器窗格中设置的筛选器将应用于源表，不应用于聚合列表。 此行为有时会产生意外结果，如[这些示例](inventory-on-hand-list.md#examples)所示。

但是， [网格中提供的筛选器](inventory-on-hand-list.md#grid-filters) *应用* 于聚合列表。 这些筛选器既包括位于网格顶部的快速筛选器，也包括每个列标题的筛选器。

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>单位和单位数量在库存日记帐中不能正常工作。

### <a name="issue-description"></a>问题描述

在库存日记帐中使用单位和数量时，您可能会遇到以下一个或两个问题：

- 为已发布产品设置转换单位时，在库存日记帐中看不到单位或数量，也无法在库存日记帐中更改单位。
- 您在库存日记帐中看到 **数量** 和 **单位** 字段，但是看不到 **单位数量** 字段。 如果您更改单位、输入数量和过帐日记帐，日记帐仍显示该数量的原始度量单位。

### <a name="issue-resolution"></a>解决问题

若要解决此问题，请按照以下步骤操作。

1. 在 **功能管理** 工作区，请确保 *在库存日记帐中使用度量单位和单位数量* 功能已开启。 此功能会将 **单位** 和 **单位数量** 字段添加到日记帐中。
1. 开启此功能后，通过以下方式使用 **数量**、**单位数量** 和 **单位** 字段：

    - **数量** – 使用为已发布产品定义的默认单位指定数量。 但是，默认单位本身不在此处显示。 如果在默认单位和 **单位** 字段中选择的单位之间设置了转换，**数量** 字段将根据 **单位数量** 和 **单位** 字段中的选择自动更新。
    - **单位数量** – 使用在 **单位** 字段中选择的单位指定数量。
    - **单位** – 在 **单位数量** 字段中选择要应用于值的单位。

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>我收到以下错误消息：“库存单位的最大小数位数为 0。”

### <a name="issue-description"></a>问题描述

当您尝试过帐库存交易或库存预留时，收到以下错误消息：“库存单位的最大小数位数为 0。”

当库存交易数量被指定为字段支持的精度级别以下的十进制值时，会发生此问题。 例如，为库存交易指定了数量 *0.5*，但仅支持整数数量。 因此，值应为 *1*，而不是 *0.5*。

### <a name="issue-resolution"></a>解决问题

1. 在 SQL Server 实例上运行以下脚本来舍入库存交易中的数量。 此脚本将更正 **inventTrans** 表中的值。

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. 在 **修复错误** 选项打开时运行现有量一致性检查。 此检查将更正 **inventSum** 表中的值。

> [!IMPORTANT]
> 强烈建议您根据环境的需要仔细编辑脚本，在测试环境中进行测试，然后在生产环境中运行脚本之前检查结果数据。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]