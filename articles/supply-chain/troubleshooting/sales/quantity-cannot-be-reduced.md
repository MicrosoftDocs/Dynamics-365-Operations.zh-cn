---
title: 取消销售订单时不能减少数量
description: 取消销售订单时不能减少数量。
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230828"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>取消销售订单时不能减少数量

错误代码：SYS138831

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 数量不能减少。 订单上的库存交易数量太少，因为数量或部分数量由输出订单或生产订单引用，或者针对其他交易进行标记。

## <a name="cause"></a>原因

如果工作与销售订单相关联，在取消和冲销工作之前，您不能取消销售订单。 即使与销售订单关联的工作已关闭，此要求也适用。

## <a name="resolution"></a>解决方法

若要解决此问题，请完成以下任务：

1. 取消未结工作。
1. 删除负荷。
1. 减少领料数量。

### <a name="cancel-open-work"></a>取消未结工作

若要取消未结工作，请按照下列步骤操作。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 在 **工作 ID** 字段中，指定您要取消的当前的 **工作状态** 值为 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的工作的 ID。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。

### <a name="delete-the-load"></a>删除负荷

若要删除负荷，请按照下列步骤操作。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 打开相关销售订单。
1. 在 **销售订单行** 快速选项卡上，选择 **仓库 \> 工作详细信息**。
1. 在 **工作** 页面的操作窗格上，在 **工作** 选项卡上的 **工作** 组中，选择 **取消工作**。
1. 确认 **工作状态** 字段设置为 *已取消*。
1. 关闭 **工作** 页面。
1. 在销售订单详细信息页面的 **销售订单行** 快速选项卡上，选择 **仓库 \> 加载详细信息**。
1. 在操作窗格上，选择 **删除**。
1. 选择 **是** 以确认要删除负荷。
1. 关闭 **负荷** 页面。

### <a name="reduce-the-picked-quantity"></a>减少领料数量

取消所有工作后，请按照以下步骤减少领料数量。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 打开相关销售订单。
1. 在 **销售订单行** 快速选项卡上，从工具栏中选择 **更新行 \> 领料**。
1. 在 **领料** 页面的 **交易** 部分中，选择 **发放状态** 字段设置为 *已领料* 的行。
1. 在 **交易** 部分中，从工具栏中选择 **添加领料行**。
1. 在 **领料行** 部分中，从工具栏中选择 **确认全部领料**。
1. 关闭 **领料** 页面。
1. 在销售订单详细信息页面的操作窗格上，在 **销售订单** 选项卡的 **维护** 组中，选择 **取消**。
1. 选择 **是** 以确认要取消销售订单。
