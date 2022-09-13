---
title: 手动处理销售和转移行领料异常
description: 本文介绍管理员如何为库存交易手动领料（或取消领料）来解决因损坏的销售订单和转移单数据引起的问题。
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403643"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>手动处理销售和转移行领料异常

[!include [banner](../includes/banner.md)]

手动处理销售和转移行领料异常让管理员能够解决因损坏的销售订单和转移单数据引起的问题。 它让受信任用户可以在仓库流程已经在进行时为与销售订单和转移单行相关的库存交易手动领料（或取消领料）。

此处所述的功能应仅在系统无法以通常方式完成处理仓库流程堆栈的情况下使用。 默认情况下，仅允许具有系统管理员角色的用户使用它。 不过，您可以根据需要将 *针对销售行手动领料* 权限分配给其他角色，来授予对此功能的访问权限。

## <a name="turn-on-this-feature-for-your-system"></a>为您的系统启用此功能

在使用本文介绍的功能之前，必须在系统中将其打开。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查这些功能状态并开启这些功能。 在 **功能管理** 工作区中，这些功能使用以下名称列出：

- *针对管理员或类似的受信任用户的销售行手动领料服务*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的，无法关闭。）
- *针对管理员或类似的受信任用户的转移行手动领料服务*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>更正与销售订单或转移单行相关的交易

使用以下过程更正与销售订单或转移单行相关的交易。

1. 根据您必须更正的订单类型，执行以下步骤之一：

    - 要更正与销售订单相关的交易，转到 **仓库管理 \> 定期任务 \> 清理 \> 针对销售行手动领料**。
    - 要更正与转移单相关的交易，转到 **仓库管理 \> 定期任务 \> 清理 \> 针对转移行手动领料**。

1. 在 **针对销售行手动领料** 或 **针对转移行手动领料** 页面上，使用网格顶部的筛选器找到您要查找的行，然后在上部网格中选择目标订单行。
1. 使用靠下部分的 **库存交易**、**负荷行**、**工作行** 和 **集装箱行** 选项卡查看关于所选行的更多信息。 这些选项卡上的信息提供相关仓库流程及其状态的基本概览。
1. 在操作窗格上，选择 **领料** 在库存交易的 **领料** 页面上打开所选订单行。 即使是对已经发布到仓库的订单行，也可以完成此步骤。 （通常，已经发布到仓库的订单行无法在 **领料** 页面打开。）

    > [!NOTE]
    > 在打开 **领料** 页面时，您可能会收到不同的警告。 执行这些警告建议的任何操作。 例如，您可能会收到有关链接到仓库工作的订单行的警告。 在这种情况下，在手动更正之前尝试使用标准[取消工作](cancel-warehouse-work.md)功能来取消工作是合理的。

1. 选择 **交易** 网格中的行，然后选择 **交易** 工具栏上的 **添加领料行**。
1. 所选行将被移到 **领料行** 网格。 为缺少必需信息的任何列设置适当的值。 （例如，指定应从其领料/取消领料的物料的位置和牌照。）
1. 在 **领料行** 工具栏上选择 **确认全部领料**。

## <a name="correct-load-line-quantities"></a>更正负荷行数量

使用以下过程更正负荷行数量。

1. 根据您必须更正的订单类型，执行以下步骤之一：

    - 要更正与销售订单相关的交易，转到 **仓库管理 \> 定期任务 \> 清理 \> 针对销售行手动领料**。
    - 要更正与转移单相关的交易，转到 **仓库管理 \> 定期任务 \> 清理 \> 针对转移行手动领料**。

1. 在 **针对销售行手动领料** 或 **针对转移行手动领料** 页面上，使用网格顶部的筛选器找到您要查找的行，然后在上部网格中选择目标订单行。
1. 在靠下部分的 **负荷行** 选项卡上，选择工具栏上的 **手动更正负荷行**。
1. 在 **手动更正负荷行** 页面的 **库存交易** 网格中，查看与所选负荷行相关的库存交易。
1. 在上部网格中，根据需要更正以下列中的负荷行数量：

    - **已创建的工作数量**
    - **领料数量**
    - **计划的越库配送数量**

    系统将验证您对这些列所做的任何更改。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
