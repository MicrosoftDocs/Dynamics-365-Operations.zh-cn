---
title: 物料合并 - 位置利用率
description: 本主题提供有关使仓库经理可以轻松查看和筛选整个仓库中各个位置的容量利用率的功能的信息。 经理可以直接从“物料合并”页面选择位置和创建库存移动工作来合并物料，从而更好地利用仓库空间。
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017176"
---
# <a name="item-consolidation---location-utilization"></a>物料合并 - 位置利用率

[!include [banner](../includes/banner.md)]

本主题提供有关使仓库经理可以轻松查看和筛选整个仓库中各个位置的容量利用率的功能的信息。 经理可以直接从 **物料合并** 页面选择位置和创建库存移动工作来合并物料，从而更好地利用仓库空间。

## <a name="turn-on-the-features"></a>开启功能

在使用本主题介绍的功能之前，必须在系统中将其打开。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查这些功能的状态，并在需要这些功能时将其开启。 按照列出的顺序打开以下两个功能。 （这两个功能都是针对 **仓库管理** 模块。）

1. 仓库库位状态
2. 物料合并库位利用率

## <a name="warehouse-location-status"></a>仓库库位状态

*仓库位置状态* 功能向 **位置** 页面添加四个新字段，来跟踪有关位置当前状态的其他信息：

- **物料编号** – 当前位于货位中的物料。 如果位置中有多个物料，此字段将为空。
- **最后一个活动的日期和时间** – 上次对货位执行的仓库事务的时间戳。
- **帐龄日期** – 将货位中的库存导入仓库时的日期。 此日期基于牌照的帐龄日期计算。 虽然此日期对于牌照跟踪位置是准确的，但是对不是牌照跟踪的位置来说可能不准确。
- **货位状态** – 货位的状态。 有四个值：

    - **未确定** – 位置模板不跟踪状态。 因此，当前状态未知。
    - **空** – 位置中当前无库存。
    - **正在领料** – 在位置上次为空后对该位置执行了出站事务。
    - **存储** – 自位置上次为空以来执行了入站事务。

这些字段使仓库经理可以更好地了解仓库中位置的状态。 还可以用于进行更高级的报告和筛选。

## <a name="set-up-item-consolidation-and-location-utilization"></a>设置物料合并和位置利用

本节介绍如何准备系统以使用物料合并和位置利用。 这些过程使用标准演示数据中的示例值。 如果您打算解演练主题后面提供的示例方案，请选择 **USMF** 法人（其包含标准演示数据），并创建本节中介绍的每个记录。 如果您不打算演练示例方案，可以将此处提供的值视为要使用这些功能必须完成的设置类型的示例。

### <a name="released-product"></a>已发布产品

1. 转到 **产品信息管理 \> 产品 \> 已发布产品** 。
1. 在 **物料编号** 字段中，选择 *M9201* ，然后打开详细信息页面。
1. 在“操作窗格”上的 **管理库存** 选项卡上，在 **仓库** 组中，选择 **物理维度** 。
1. 在 **物理维度** 页的“操作窗格”上，选择 **新建** 。

    新行将添加到网格中。 **物料编号** 字段将预设。

1. 在 **单位** 字段中，选择 *个* 。 行上的其余字段将自动设置。
1. 选择 **保存** ，然后关闭页面。

### <a name="location-profile"></a>位置模板

1. 转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板** 。
1. 在位置模板列表中，选择 **FLOOR-05** 。
1. 在操作窗格上，选择 **编辑** 。
1. 在 **常规** 快速选项卡上，确保将以下两个选项都设置为 *是* ：

    - 在库位中启用物料
    - 启用库位状态

1. 选择 **保存** 。

    > [!IMPORTANT]
    > 如果 **在位置中启用物料** 和 **启用位置状态** 选项已经设置为 *是* ，直接跳至步骤 10 中设置 **维度** 快速选项卡的说明。 如果尚未将选项设置为 *是* ，您必须在手动设置选项之后对 **仓库管理** 模块运行一致性检查。 在这种情况下，继续下一步。

1. 要运行一致性检查，转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查** 。
1. 在 **一致性检查** 对话框中，设置以下值：

    - **模块** ： *仓库管理*
    - **检查/修复** ： *检查*
    - **开始日期：** 将此字段保留为空。
    - **仓库位置状态一致性检查：** 选择此复选框。

1. 选择 **确定** 。

    > [!TIP]
    > 一致性检查完成后，您会收到一条通知。 打开[操作中心](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications)查看消息。 选择 **消息详细信息** 查看详细信息。
    >
    > 如果一致性检查的消息指示“发现仓库 XX 中位置 XXXX 的位置状态信息有误”，则必须再次运行一致性检查。 这次，将 **检查/修复** 字段设置为 *修复错误* 。 查看消息以确保没有发现错误。

1. 现在，您必须完成位置模板的设置。 转到 **仓库管理 \> 设置 \> 仓库 \> 位置模板** ，选择位置模板 **FLOOR-05** ，然后在“操作窗格”上选择 **编辑** 。
1. 在 **维度** 快速选项卡上，设置以下值：

    - **容量利用率百分比** ： *100*
    - **用于库存位置的容量法** ： *使用位置容量*
    - **实际位置高度** ： *10*
    - **实际位置宽度** ： *10*
    - **实际位置深度** ： *10*
    - **最大重量** ： *100*

1. 选择 **保存** 。

### <a name="mobile-device-menu-items"></a>移动设备菜单项

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项** 。
1. 在“操作窗格”上，选择 **新建** 创建用于排序的菜单项。
1. 在标题中，设置以下值：

    - **菜单项名称** ： *调入*
    - **标题** ： *调入*
    - **模式：***工作*
    - **使用现有工作** ： *否*

1. 在 **常规** 快速选项卡上，设置以下值：

    - **工作创建流程** ： *调入*
    - **库存调整类型** ： *调入*

1. 选择 **保存** 。

### <a name="mobile-device-menu"></a>移动设备菜单

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单** 。
1. 在菜单列表中，选择 **库存** 。
1. 在操作窗格上，选择 **编辑** 。
1. 在 **可用菜单和菜单项** 列表中，找到并选择 **调入** 菜单项。
1. 选择向右箭头按钮，将 **调入** 移至 **菜单结构** 列表中。 这样就将新菜单项添加到了所选菜单。
1. 选择 **保存** 。

### <a name="movement-types"></a>变动类型

1. 转到 **仓库管理 \> 设置 \> 库存 \> 移动类型** 。
1. 在“操作窗格”中，选择 **新建** ，然后设置以下值：

    - **移动类型代码** ： *CONSOLIDATE*
    - **描述** ： *合并位置*
    - **工作类 ID** ： *InvMov*

1. 选择 **保存** 。

## <a name="example-scenario"></a>示例场景

以下方案使用移动设备上的仓库应用对仓库中的两个位置进行库存 *调入* 。

### <a name="add-inventory-to-locations"></a>将库存添加到位置

1. 以为仓库 *51* 设置的用户身份登录到移动设备。
1. 转到 **库存 \> 调入** 。

    现在，您将进入第一个位置调整。

1. 在 **调入** 任务中，选择要进行库存调整的位置。 在 **位置** 字段中，选择 *LP-001* 。
1. 确认位置。
1. 为将添加到位置的物料创建牌照 ID。 在 **牌照** 字段中，输入 *LP00101* 。
1. 确认牌照。
1. 输入将添加到牌照的物料。 在 **ITEM** 字段中，输入 *M9201* 。
1. 确认物料。
1. 输入将添加的物料的数量。 在 **数量** 字段中，输入 *10* 。
1. 确认数量。

    您将收到“工作已完成”消息。 现在，您将进入第二个位置调整。

1. 在 **调入** 任务中，选择要进行库存调整的位置。 在 **位置** 字段中，选择 *LP-002* 。
1. 确认位置。
1. 为将添加到位置的物料创建牌照 ID。 在 **牌照** 字段中，输入 *LP00201* 。
1. 确认牌照。
1. 输入将添加到牌照的物料。 在 **ITEM** 字段中，输入 *M9201* 。
1. 确认物料。
1. 输入将添加的物料的数量。 在 **数量** 字段中，输入 *15* 。
1. 确认数量。

    您将收到“工作已完成”消息。

1. 选择“菜单”按钮（有时称为汉堡包或汉堡包按钮），然后选择 **取消** 退出 **调入** 任务。

### <a name="consolidate-locations"></a>合并位置

1. 转到 **仓库管理 \> 定期任务 \> 物料合并** 。
1. 在标题中，选择要进行合并的仓库。 在 **仓库** 字段中，输入 *51* 。

    将显示调整了 *M9201* 物料的每个位置的记录。 **利用率百分比** 列显示每个位置的容量利用率。

1. 要合并库存，请选择必须合并的所有位置，然后在“操作窗格”上，选择 **合并库存** 。
1. 在 **合并库存** 对话框中，指定应用于创建库存移动工作的位置和移动类型。 设置以下值：

    - **位置** ： *LP-001*
    - **移动类型代码** ： *CONSOLIDATE*

1. 选择 **确定** 。
1. 您将收到显示创建的移动工作的信息性消息。 记录移动工作 ID。

### <a name="view-movement-work"></a>查看移动工作

1. 转到 **仓库管理 \> 工作 \> 工作详细信息** 。
1. 查看创建的工作。 使用库存合并中的移动工作 ID 筛选或搜索工作网格。

    在此方案中，具有库存的现有位置被用作库存合并位置。 因此，仅创建了一个工作 ID。

    > [!NOTE]
   > 系统会为必须完成的每个移动创建一个工作 ID。 如果您指定的位置已经包含库存，将仅创建一个工作 ID。 如果指定新位置，将创建两个工作 ID。