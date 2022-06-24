---
title: 分派工作订单
description: 本文介绍如何在资产管理中分派工作订单。
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6b2349d04386a88237ec1cb650890718d41aa5a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863989"
---
# <a name="dispatch-work-order"></a>分派工作订单

[!include [banner](../../includes/banner.md)]

 

可使用 **分派** 功能将一个工作订单或工作订单作业分配给一位工人。

1. 单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 在列表中选择工作订单。

3. 在 **常规** 选项卡上，单击 **分派**。

4. 在 **分派工作订单** 对话框的 **工作人员** 字段中，选择工作人员。

5. 如果预计工时与预测工时不同，可在 **计划工时** 字段中插入预计工时。

6. 如果需要，可在 **计划开始时间** 字段中编辑开始日期和时间。

7. 如果计划流程应该遵守与已经为其他作业安排的资源有关的产能限制，请确保 **资产**、**工具** 和 **工作人员** 切换按钮设置为 **是**。 如果要查看有关计划流程的详细信息，请在 **详细** 切换按钮上选择 **是**。 这意味着在信息日志中显示有关为工作订单计算出的分数的详细信息。

8. 若要在日历中忽略休息日，请在 **忽略计划** 切换按钮上选择 **是**（适用于资产、工人和工具）。 若要忽略可能在工作订单中已选择的有关计划的限制，请在 **忽略已计划执行** 切换按钮上选择 **是**。 

    有关设置已计划执行的信息，请参阅[已计划执行](../setup-for-work-orders/scheduled-execution.md)部分。

9. 单击 **确定**。 将把工作订单生命周期状态自动更新为 **已计划** 生命周期状态指定的 **资产管理** > **设置** > **工作订单** > **生命周期模型**。

下图显示 **计划工作订单** 对话框中选择的分派的示例。

![图 1.](media/04-work-order-scheduling.png)

[!NOTE]
如果要删除对工作订单的计划，在 **所有工作订单** 中选择工作订单，然后单击 **常规** 选项卡上的 **删除计划**。如果删除计划，请记住要手动更新工作订单生命周期状态。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]