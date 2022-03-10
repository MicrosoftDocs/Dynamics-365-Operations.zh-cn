---
title: 负荷行上的重量字段与负荷上的重量字段不匹配
description: 负荷行上的重量字段与负荷上的重量字段不匹配
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756695"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>负荷行上的重量字段与负荷上的重量字段不匹配

错误代码：WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 负荷行上的重量字段与负荷 %1 上的重量字段不匹配。 请运行仓库负荷重量一致性检查来重新计算重量字段。

## <a name="cause"></a>原因

**净重** 和 **皮重** 字段在负荷行上设置为 *0*（零）。 但是，产品的重量度量的重量字段未设置为 *0*。 如果未在负荷行上设置重量字段，对负荷行上的数量进行任何更正都可能导致负荷上的重量计算不正确。 如果自创建负荷行以来更改了产品上的重量，可能会发生此问题。

## <a name="resolution"></a>解决方法

默认情况下，创建负荷行时，将在负荷行上输入来自产品的重量字段。 如果重量为零，可以使用 *仓库负荷重量一致性检查* 功能重新进行计算。

1. 转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**。
1. 在 **一致性检查** 对话框中，将 **模块** 字段设置为 *仓库管理*。
1. 将 **检查/修复** 字段设置为 *修复错误*。
1. 在复选框列表中，选中 **仓库负荷重量一致性检查** 复选框，并确保仅突出显示此复选框的行。
1. 在复选框列表的顶部，选择省略号按钮 (**...**)，然后选择菜单上的 **对话**。
1. 在 **仓库负荷重量一致性检查** 对话框中，设置以下字段来指定应运行一致性检查的条件：

    - **负荷 ID：** 指定负荷 ID。 保留为空白将检查所有负荷 ID。
    - **物料编号：** 指定物料编号。 保留为空白将检查所有物料。
    - **始终重新计算负荷上的重量：** 将此选项设置为 *是*。
    - **允许覆盖负荷行上的重量：** 将此选项设置为 *是*。

1. 选择 **确定** 关闭 **仓库负荷重量一致性检查** 对话框。
1. 选择省略号按钮，然后在菜单上选择 **执行**。

将根据您指定的条件重新计算重量。 选择 **消息详细信息** 链接可以查看一致性检查的结果。
