---
title: 航行状态设置
description: 本主题介绍如何建立用户可以分配给航行的状态值。
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500878"
---
# <a name="voyage-status-setup"></a>航行状态设置

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

在 **航行状态** 页上，建立用户可以分配给航行的状态值集。 用户可以将航行状态值分配给航行的所有级别：航行、装运集装箱、帐页、采购订单和物料（采购订单行和转移单行）。 它们用于两个目的：

- 通知用户航行、装运集装箱、帐页、采购订单或物料（采购订单行和转移单行）的状态。
- 通过阻止修改或删除限制成本区域的使用。

要设置航行状态，转到 **登陆成本 \> 设置 \> 航行状态**。 在那里，您可以使用操作窗格上的按钮添加、删除和编辑状态。

每个成本区域有自己的航行状态集和层次结构。 因此，在 **航行状态** 页上，在 **成本区域** 字段中，您必须首先选择要查看或为其创建航行状态的成本区域。 然后，对于每个航行状态，根据需要设置下表中所述的字段。 请注意，航行状态还可以由系统事件自动更改，如使用跟踪控制中心建立的规则。

| 字段 | 说明 |
|---|---|
| 航行状态 | 输入航行状态的名称。 |
| 说明 | 输入航行状态的描述。 |
| 修改 | 如果允许用户修改具有此状态的航行，选中此复选框。 |
| Delete | 如果允许用户删除具有此状态的航行，选中此复选框。 |
| 强制 | 选中此复选框可以让航行状态变为强制信息，这样不会被跳过。 |
| 父对象 | 使用此字段可以在状态值之间建立层次结构。 航行状态只能在层次结构中从父状态向下更改为子状态之一（手动或自动）。

> [!NOTE]
> 您只需要设置组织使用的特定航行状态。 典型的航行状态包括 *已确认*、*在途货物*、*已接收*、*成本计算就绪* 和 *已计算成本*。 但是，其他状态可能会显示。
