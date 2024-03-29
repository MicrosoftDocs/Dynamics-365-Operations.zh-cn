---
title: 显示生产车间执行界面中的休假余额
description: 本文提供了一个示例场景，展示了如何设置 Microsoft Dynamics 365 Supply Chain Management，以便它使用工资统计数据为工作人员提供本年度休假余额的概览。
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852264"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>显示生产车间执行界面中的休假余额

[!include [banner](../includes/banner.md)]

本文提供了一个示例场景，展示了如何设置 Microsoft Dynamics 365 Supply Chain Management，以便它使用工资统计数据为每个工作人员提供本年度休假余额的概览。 工作人员将能够在生产车间执行界面的 **我的一天** 对话框中查看他们的休假余额。

此方案使用丹麦假日法，休假年度从 9 月 1 日到 8 月 31 日。 在此方案中，您的公司雇用了一名新工作人员，并将为该员工提供 10 天的剩余假期作为当前休假年度的剩余时间。

## <a name="turn-on-the-required-features"></a>开启必需功能

若要运行此方案，您必须在 *功能管理* 中启用[生产车间执行界面的“我的一天”视图](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)功能。 有关如何针对生产车间执行界面启用此功能和其他功能的信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。

## <a name="make-sample-data-available"></a>提供示例数据

若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。 此外，开始前，还必须选择 **USMF** 法人。

## <a name="create-a-new-pay-type"></a>创建新的付薪类型

首先创建一个新的 *付薪类型*，该付薪类型将跟踪工作人员获得的休假天数（也称为其 *休假余额*）。 通常，付薪类型用于计算工作人员的薪水。 但是，您在此处创建的付薪类型将用于计算余额。

1. 转到 **考勤管理 \> 设置 \> 工资单 \> 付薪类型**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行上，设置以下值：

    - **付薪类型：** *5151-1*
    - **说明**：*工作人员休假天数的计数器*
    - **包括在导出中**：*否*

## <a name="update-the-pay-agreement"></a>更新付薪协议

在本节中，您将添加新的付薪类型，并设置用于定义如何在登记休假天数时调整每个工作人员的休假余额的规则，从而编辑现有的 *付薪协议*。

1. 转到 **考勤管理 \> 设置 \> 工资单 \> 付薪协议**。
1. 选择要在其中设置休假政策的付薪协议。 （如果您正在处理标准 USMF 示例数据，则只有一个 *人员* 付薪协议。）
1. 请确保所选付薪协议对当前日期有效。 如果您正在处理标准 USMF 示例数据，则 **人员** 付薪协议的 *结束日期* 字段可能会设置为过去的日期。 根据需要更改该值，以便结束日期在将来的一两年中。
1. 在操作窗格上选择 **协议行**。
1. 在 **付薪协议行** 页面的 **概览** 快速选项卡上，在工具栏上设置以下值：

    - 在第一个下拉列表中，选择 **星期一**。
    - 在第二个下拉列表中，选择 **缺勤**。

1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行上，将 **付薪类型** 字段设置为您为此方案创建的付薪类型 (*5151-1*)。 将所有其他字段设置为其默认值。
1. 在仍选择新行的同时，在 **常规** 快速选项卡上设置以下值：

    - **缺勤代码**：*休假*
    - **使用固定数量**：*是*
    - **常数**：*-1*

1. 在操作窗格上，选择 **复制这一天**。
1. 在 **复制这一天** 对话框中，设置以下值：

    - **星期二**、**星期三**、**星期四** 和 **星期五**：*是*
    - **覆盖**：*是*
    - **缺勤**：*是*

1. 选择 **确定**。

## <a name="create-a-payroll-statistic-group"></a>创建工资统计组

*工资统计组* 用于设置一段时间内的工作人员登记统计信息。 在此方案中，您将使用工资单统计组来计算工作人员在休假期间获得的休假天数。 在丹麦，休假期为 9 月 1 日到 8 月 31 日。

1. 转到 **考勤管理 \> 设置 \> 工资单 \> 工资统计组**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行上，设置以下值：

    - **工资统计组**：*VAC*
    - **描述**：*休假余额*
    - **转入**：*否*

1. 在仍选择新行的同时，在操作窗格上选择 **设置**。
1. 在 **设置** 页上的操作窗格上，选择 **新建** 在网格中添加一行。
1. 在新行上，将 **付薪类型** 字段设置为 *5151-1*。
1. 在 **期间代码** 字段中选择并按住（或右键单击），然后选择 **查看详细信息**。 您现在可以设置您稍后将分配给此字段的期间代码。
1. 在 **期间类型** 页上的操作窗格上，选择 **新建** 在网格中添加一行。
1. 在新行上，设置以下值：

    - **期间类型**：*VacYear*
    - **描述**：*休假年度*
    - **频率**：*年*

1. 在仍选择新行的同时，在操作窗格上选择 **生成期间**。
1. 在 **生成期间** 对话框中，设置以下值：

    - **指定期间的开始日期**：*2021 年 9 月 1 日*
    - **期间的长度**：*5*

1. 选择 **确定**。
1. 关闭 **期间类型** 页面以返回到 **工资统计组** 页面。
1. 将 **期间代码** 字段设置为您刚才创建的期间类型 (*VacYear*)。

## <a name="create-a-statistical-balance-setup"></a>创建统计余额设置

在本节中，您将创建一个 *统计余额设置*，该设置链接到您在上一节中创建的工资统计组。 稍后，您会将此统计余额设置链接到生产车间执行界面中的 **我的一天** 视图。 然后，**我的一天** 视图将能够显示分配给关联工资统计组的付薪类型的休假余额。

1. 转到 **考勤管理 \> 设置 \> 工资单 \> 统计余额设置**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行上，设置以下值：

    - **工资统计组**：*VAC*
    - **外部名称**：*休假余额*
    - **弹性**：*无*

## <a name="create-a-manual-premium"></a>创建人工津贴

*人工津贴* 通常用于为工作人员的额外工作提供额外工资。 在这种情况下，您将创建一个人工津贴，您可以使用它为每个工作人员设置初始休假余额。

1. 转到 **考勤管理 \> 设置 \> 工资单 \> 人工津贴**。
1. 在操作窗格中，选择 **新建** 添加记录。
1. 在新记录中，设置以下值：

    - **津贴**：*VAC*
    - **说明**：*调整工作人员的休假余额*
    - **付薪类型**：*5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>设置工作人员的初始休假余额并调整一天

工资单管理员使用 **审核** 页面查看并审核工作人员的日常登记。 在此方案中，您将担任管理员的角色，以便您可以为工作人员设置初始休假余额并登记工作人员的休假天数。

1. 转到 **考勤管理 \> 查看和审核 \> 审核**。
1. 在 **审核** 对话框中，设置以下字段：

    - **审核组** - 选择您所属的审核组。 （如果您正在处理标准 USMF 示例数据，则只有一个 *AdmMan* 审核组。）
    - **查看整个组，1 天** - 选择此选项，然后将字段设置为当前日期。

1. 选择 **确定**。
1. **审核** 页面显示与您的条件匹配的记录列表。 选择要审核的工作人员。 如果您正在处理标准 USMF 示例数据，请选择工作人员 *000496* (*Christina Portra*)。
1. 授予所选工作人员 10 天的休假时间：

    1. 在仍选择此工作人员的同时，在操作窗格上选择 **津贴行**。
    1. 在 **津贴行** 页上的操作窗格上，选择 **新建** 在网格中添加一行。
    1. 在新行上，设置以下值：

        - **津贴**：*VAC*
        - **数量：** *10*

    1. 关闭 **津贴行** 页面。

1. 在 **审核** 页面上，登记工作人员在当前日期使用了其一个休假日的事实：

    1. 在仍选择此工作人员的同时，在页面下部的 **概览** 选项卡上，选择工具栏上的 **新建**，在网格中添加一行。
    1. 在新行上，设置以下值：

        - **日记帐登记类型**：*缺勤*
        - **参考**：*休假*

    1. 在页面的上半部分，选择工具栏上的 **转移** 以应用休假余额并计算扣缴。

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>配置生产车间执行界面，使其包括“我的一天”对话框

在此节中，您会将 **我的一天** 按钮添加到生产车间执行界面。 然后，工作人员可以使用此按钮打开 **我的一天** 对话框。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 配置生产车间执行**。
1. 选择一个配置，如 *默认值*。
1. 在操作窗格上，选择 **设计选项卡**。
1. 在 **设计选项卡** 页面上的列表窗格中，选择 *所有作业* 以查看该选项卡的设置。**主视图** 字段现在应显示 *所有作业* 的值。
1. 在操作窗格上，选择 **编辑**。
1. 在 **辅助工具栏** 快速选项卡上的 **可用操作** 列中，选择 **我的一天**。 然后选择右箭头按钮将其移到 **选定操作** 列。

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>在生产车间执行界面中检查您的余额

在本节中，您将以之前设置了其休假时间的工作人员身份登录生产车间执行界面。 然后，您将打开 **我的一天** 对话框以查看您的休假余额。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 生产车间执行**。
1. 如果提示您选择配置，请选择在此方案中之前设置的配置（*默认值*）。
1. 作为您在此方案中早期设置的用户进行登录。 如果您正在使用标准 USMF 示例数据，则您应能够通过在 *徽章 ID* 字段中输入 **123** 来登录。 此徽章 ID 对应于 Christina Portra。
1. 在左侧工具栏上选择 **我的一天**。
1. 检查对话框的 **余额** 部分。 此节现在应显示您的余额为 9 个休假日。
