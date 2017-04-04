---
title: "操作搜索"
description: "文章此工序中 Microsoft Dynamics 365 中对行动搜索功能。 搜索将操作以帮助和运行在页面上的操作。"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>操作搜索

文章此工序中 Microsoft Dynamics 365 中对行动搜索功能。 搜索将操作以帮助和运行在页面上的操作。

<a name="introduction"></a>简介
------------

页面在工序 365 的 Microsoft Dynamics 中主要公开操作窗格上的命令，出现该页顶部将显示在工具栏和页面的不同部分的标准操作窗格。 在以前版本的中，一键提示功能让您快速按 Alt 键并通过一系列的字母访问在操作窗格的所有按钮。 

[] (![keyTipsAX6。/media/keytipsax6.png)](。但是/media/keytipsax6.png)，在当前版本工序的 Dynamics /media/keytipsax6.png，键提示不可用，但按操作搜索功能取代了。 这一新的功能允许您迅速搜索和运行所有可见操作窗格中的按钮。

## <a name="using-action-search"></a>使用操作搜索
若要使用操作搜索功能，请执行以下步骤。

1.  在操作窗格上，单击**操作搜索**字段。 （**操作搜索**字段包含一个放大镜图标。）
2.  键入按钮的名称的所有或部分您要运行。 您还可以搜索将通过使用从按钮“路径的词语”。 (有关详细信息，请参阅此文章的下一部分)。通常，在此情况下，您输入了两到四字符后，该按钮执行结果列表的顶端将显示。
3.  在结果列表中查找和运行按钮（通过使用您的鼠标或键盘）。

该按钮运行后，焦点返回到您在页面的最后一个位置，以便您可以继续工作。 

[] (操作![搜索字段。/media/action 搜索 field.png)](。/media/action 搜索 field.png)

您还可以通过按 Ctrl+/ 或 Alt+Q 开始操作搜索。 再次按键盘快捷方式将焦点返回到您在页面上的最后一个位置。

## <a name="understanding-the-results-list"></a>了解结果列表
通常，工序中 Dynamics 365，必须知道位置和按钮的上下文充分了解该按钮的用途。 因此，附加信息。每物料显示结果列表正确，帮助您了解哪些按钮出现在列表中。 特别是按钮“路径”将显示。 该路径可能包括以下相关 UI 元素的标签：

-   “操作窗格”选项卡
-   按钮组
-   菜单按钮（如果按钮在菜单按钮内）
-   菜单分隔符（如果按钮在菜单按钮内的命名组内）
-   页面上的组或选项卡（例如，快速选项卡的名称）

例如，您在**操作搜索**字段中键入 **tot**，现在正在检查结果列表。 第一个条目，将命名的按钮** **合计，请突出显示。 **销售订单** **按钮 &gt; 查看路径**还显示。 **路径的销售订单**部件对应于操作窗格上的销售订单** **选项卡上，并且，路径的** **部件查看对应于该选项卡视图** **的组。 **同样，总折扣**按钮的路径 (**销售** &gt; ** **则计算) 通知您此按钮在定位**计算** ** **销售组的操作窗格的选项卡。 因此，此帮助"按钮信息将由您的搜索操作触发正确地了解结果 (如果您选择该列表中该按钮)。 

操作![[] (与搜索字段数据。{{/media/action:/media/action-search-field-with-data.png}} {{搜索：/media/action-search-field-with-data.png}} {{字段：/media/action-search-field-with-data.png}} {{与：/media/action-search-field-with-data.png}} {{data.png:/media/action-search-field-with-data.png}})](。{{/media/action:/media/action-search-field-with-data.png}} {{搜索：/media/action-search-field-with-data.png}} {{字段：/media/action-search-field-with-data.png}} {{与：/media/action-search-field-with-data.png}} {{data.png:/media/action-search-field-with-data.png}}) 

在之前的示例中，操作搜索在页面顶部显示了标准操作窗格的结果。 但是，操作搜索还显示位于页面其他位置的可见工具栏的结果。 例如，您按照上的搜索** **现有库存量按** **销售订单行 FastTab 中。 在这种情况下，结果列表的路径 (按钮**销售订单行** &gt; **库存** &gt; ** **视图) 通知您此按钮位于库存** **菜单按钮的**视图**标题下在销售订单行 FastTab ** **。 

[] (![现有库存量。/media/on 现有量- inventory.png)](。/media/on 现有量- inventory.png)

## <a name="action-search-vs-navigation-search"></a>操作搜索与导航搜索
而出于搜索操作查找和页面上运行的行动，则查找和导航的单独搜索机制到 Dynamics 中 365 页的操作。 有关此功能的详细信息，请参阅搜索所在 [] () 中 search.md 文章。


