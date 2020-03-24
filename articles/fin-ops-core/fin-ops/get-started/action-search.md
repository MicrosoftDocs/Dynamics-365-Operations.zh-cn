---
title: 操作搜索
description: 本文介绍操作搜索功能。 操作搜索可以帮助您在页面中找到操作并运行。
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd4d81f010149c762dac0f4e6fa912c2e2cef072
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112160"
---
# <a name="action-search"></a>操作搜索

[!include [banner](../includes/banner.md)]

本文介绍操作搜索功能。 操作搜索可以帮助您在页面中找到操作并运行。

## <a name="introduction"></a>简介

页面主要在操作窗格（页面顶部显示的标准操作窗格和页面各部分中显示的工具栏）中显示命令。 在以前版本中，“键提示”功能能够让您通过按下 Alt 键和一系列字母的方式快速访问“操作窗格”上的任何按钮。

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

“键提示”不再可用，已经替换为操作搜索功能。 这一新的功能允许您迅速搜索和运行所有可见操作窗格中的按钮。

## <a name="using-action-search"></a>使用操作搜索

若要使用操作搜索功能，请执行以下步骤。

1. 在操作窗格上，单击**操作搜索**字段。 （**操作搜索**字段包含一个放大镜图标。）
2. 键入您要运行的按钮的全部或部分名称。 您还可以使用按钮“路径”的字词进行搜索。 （有关详细信息，请参阅本文的下一个部分。）通常，在您键入了两个到四个字符后，按钮将出现在结果列表的顶部附近。
3. 在结果列表中查找和运行按钮（通过使用您的鼠标或键盘）。

该按钮运行后，焦点返回到您在页面的最后一个位置，以便您可以继续工作。

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

您还可以通过按 Ctrl+/ 或 Alt+Q 开始操作搜索。 再次按键盘快捷方式将焦点返回到您在页面上的最后一个位置。

## <a name="understanding-the-results-list"></a>了解结果列表

通常，必须知道按钮的位置和环境以充分了解该按钮的用途。 因此，每个物料的附加信息将显示在结果列表，可帮助您确切了解哪些按钮出现在列表中。 特别是按钮“路径”将显示。 该路径可能包括以下相关 UI 元素的标签：

- “操作窗格”选项卡
- 按钮组
- 菜单按钮（如果按钮在菜单按钮内）
- 菜单分隔符（如果按钮在菜单按钮内的命名组内）
- 页面上的组或选项卡（例如，快速选项卡的名称）

例如，您在**操作搜索**字段中键入 **tot**，现在正在检查结果列表。 名为**总计**的按钮的第一个条目将高亮显示。 **销售订单** &gt; **查看**的按钮路径也将显示。 路径的**销售订单**部分与“操作窗格”中的**销售订单**选项卡对应，路径的**查看**部分与该选项卡上的**查看**组对应。同样，**总折扣**按钮的路径（**销售** &gt; **计算**）告知您此按钮位于“操作窗格”的**销售**选项卡上的**计算**组中。 因此，此信息帮助您确切了解哪个按钮将由操作搜索触发（如果您在结果列表中选择该按钮）。

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

在之前的示例中，操作搜索在页面顶部显示了标准操作窗格的结果。 但是，操作搜索还显示位于页面其他位置的可见工具栏的结果。 例如，您搜索位于**销售订单行**快速选项卡的**现有库存量**按钮。 这种情况下，结果列表中的按钮路径（**销售订单行** &gt; **库存** &gt; **查看**）告知您此按钮位于**销售订单行**快速选项卡的**库存**菜单按钮上的**查看**标题下。

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> 有一些按钮在操作搜索中不显示。 包括下拉对话框按钮和子窗体的按钮。 

## <a name="action-search-vs-navigation-search"></a>操作搜索与导航搜索

操作搜索用于在页面上查找和运行操作，而查找和导航到页面存在单独的搜索机制。 有关该功能的详细信息，请参阅[导航搜索](navigation-search.md)一文。
