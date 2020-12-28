---
title: 设计生产车间执行界面
description: 此主题介绍如何为每个配置设计用户界面内容。
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664264"
---
# <a name="design-the-production-floor-execution-interface"></a>设计生产车间执行界面

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

您可以为生产车间执行界面使用的每个配置设计用户界面内容。 例如，一个工作单元中的工作人员可能需要能够在生产车间打开作业说明，而在另一个工作单元，则不需要说明。 在这种情况下，应创建两个配置，一个带有打开文档附件的按钮，另一个没有此按钮。

## <a name="design-a-tab"></a>设计选项卡

在 **配置生产车间执行** 页上，您可以通过选择操作窗格上的 **设计选项卡** 来创建和配置选项卡。

每个选项卡分为四个部分，如下图所示。

![选项卡布局](media/pfe-tab-layout.png "选项卡布局")

图中显示了以下元素：

1. 主工具栏
1. 辅助工具栏
1. 主视图
1. 详细视图

要创建和配置新选项卡，请按照以下步骤操作：

1. 转到 **生产控制 &gt; 设置 &gt; 制造执行**。

1. 在操作窗格上选择 **设计选项卡** 打开 **设计选项卡** 页。

    ![设计选项卡页](media/pfe-design-tabs.png "设计选项卡页")

1. 在操作窗格上选择 **新建**。

1. 在页面标题中进行以下设置：

    - **选项卡名称** - 为选项卡指定名称。
    - **主视图** - 在两个预定义的作业列表（*活动作业* 或 *所有作业*）之间进行选择。
    - **详细信息视图** - 在空白值或 **作业详细信息** 之间选择。 如果选择空白值，选项卡中将没有详细视图。如果选择 **作业详细信息**，详细视图将包含在主视图中的作业列表中选择的作业的详细描述。

1. 在 **主工具栏** 部分，选择哪些按钮应该在主工具栏中可用。 **可用操作** 列显示可以添加的所有按钮的列表。 **所选操作** 列显示当前配置中包含的所有按钮的列表。 根据需要在列之间使用按钮在列之间移动所选项。 使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。

1. 在 **辅助工具栏** 部分，选择哪些按钮应该在辅助工具栏中可用。 **可用操作** 列显示可以添加的所有按钮的列表。 **所选操作** 列显示当前配置中包含的所有按钮的列表。 根据需要在列之间使用按钮在列之间移动所选项。 使用 **所选操作** 列旁边的向上和向下按钮控制按钮在用户界面的显示顺序。

## <a name="associate-a-tab-with-a-configuration"></a>将选项卡与配置关联

设计完所需的所有选项卡后，可以将它们与配置关联。

1. 转到 **生产控制 &gt; 设置 &gt; 配置生产车间执行**。

    ![配置生产车间执行](media/pfe-config-prod-floor-execution.png "配置生产车间执行")

1. 在 **选项卡选择** 快速选项卡上，选择 **添加**。

1. 一个新行将添加到网格中。 对于这个新行，选择要添加到配置中的选项卡的名称。

1. 根据需要继续添加其他选项卡。

1. 根据需要使用工具栏上的 **上移** 和 **下移** 按钮排列选项卡。 选项卡将按照以上屏幕截图中显示的顺序从左到右显示（顶部的选项卡显示在左侧）。
