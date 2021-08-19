---
title: 无法更新负荷行，因为已发放的数量将为负数
description: 当更新或删除负荷行将导致负的已发放数量时，会出现此问题。
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728451"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>无法更新负荷行，因为已发放的数量将为负数

错误代码：@WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>故障特征

当更新或删除负荷行将导致负的已发放数量时，会出现此问题。 在这种情况下，当您尝试更新或删除负荷行时，系统将显示以下错误消息：

> 物料 %1、批次 %2 的已发放数量不能为复数。

因此，您无法更新或删除负荷行。

## <a name="cause"></a>原因

更新或删除负荷行后，系统将更新相关销售行 (*whsSalesLine.ReleaseQty*) 的已发放数量。 系统评估已发放数量，如果发现更新后该行的已发布数量为负数，则不会让您更新或删除该行。 每当您尝试通过各种操作来更新负荷行数量或度量单位时，都会进行此验证，例如删除负荷行、删除装运、更改负荷行的数量、减少领料数量和领料短缺。

此问题的最常见根本原因是用于未结负荷行的单位转换发生更改。 例如，发布销售订单时的单位转换为 *50 Ea = 1 PL*。 但是，在最终确定相关负荷装运之前，单位转换已更改为 *100 Ea = 1 PL*。

## <a name="resolution"></a>解决方法

解决方案是还原单位换算更改，更新或删除负荷行，然后重新实施转换。 在问题解决前，您必须防止处理其他包括导致问题的物料的负荷。 否则，新转换可能会用于已打开的其他负荷。

若要解决此问题，请完成以下任务：

1. 查看用于负荷行的单位转换。
2. 查看物料的当前单位转换，并进行调整以允许更新或删除负荷行。
3. 更新或删除负荷行，并恢复单位转换调整。

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>查看用于负荷行的单位转换

使用以下过程检查您的负荷行并记下用于负荷行的单位转换。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择包含无法删除或更新的负荷行的负荷。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 在上方网格中，选择相关的工作 ID。
1. 在页面底部的 **常规** 选项卡上，计算 **库存工作数量** 值与 **工作数量** 值之间的换算率。 记录此换算率。
1. 为所有相关工作 ID 重复此过程以确保使用了相同的转换。

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>查看物料的当前单位转换并进行调整

使用以下过程查看您的产品单位转换，并进行调整以确保单位转换与负荷行一致。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 打开相关产品以转到其 **相关产品详细信息** 页。
1. 在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **单位转换**。
1. 选择单位之间的转换，并使用您在上一节中找到的转换进行调整。

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>更新或删除负荷行，并恢复单位转换调整

使用以下过程根据需要处理负荷行并恢复单位换算。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 打开包含无法删除或更新的负荷行的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 根据需要继续执行所需操作。 （例如，删除负荷行或更改其数量。）
1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 打开相关产品以转到其 **相关产品详细信息** 页。
1. 在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **单位转换**。
1. 选择单位之间的转换，并恢复您在上一节中所做的调整。
