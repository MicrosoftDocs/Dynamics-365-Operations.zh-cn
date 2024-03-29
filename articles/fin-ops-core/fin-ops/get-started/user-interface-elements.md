---
title: 用户界面元素
description: 本文介绍应用中的用户界面 (UI) 元素。
author: jasongre
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: de6e4f8472cf73fb1d9874a57442622c0da23b54
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275933"
---
# <a name="user-interface-elements"></a>用户界面元素


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

本文介绍应用中使用的用户界面 (UI) 元素。 浏览界面之前，务必了解构成界面的元素的名称和功能。

## <a name="overview"></a>概览

- **操作窗格** - 导航栏下面的条。 可在此处选择选项卡来更改页面中显示的记录。 可在此处编辑和保存记录。  
- **速见表** - 可在此窗格中查看特定记录的信息和执行特定记录的活动。  
- **速见表窗格** 可在此处滚动浏览速见表中要查看的记录的不同方面。  
- **筛选器窗格** - 在某些页面中，可通过选择 **显示筛选器** 来打开此窗格。 可用于缩小此页面中显示的结果的范围。  
- **导航栏** - 界面顶部的条。 其中包含 **Dynamics 365 门户**、**搜索**、**公司选择器**、**操作中心**、**设置**、**帮助和支持** 和用户配置文件。  
- **导航列表** - 在某些页面中，可滚动浏览此窗格以查找特定记录。 记录的详细信息将在被收集后在该页中显示。  
- **导航窗格** - 最左侧的窗格。 可在此处找到本产品中的任何页面。  
- **页面** - 界面的聚焦中心。 在其他 UI 组件中进行的选择将影响此处显示哪些记录。  
- **窗格** -最右侧的窗格。 在某些情况下，需要更改并保存记录的某些方面时，将打开此窗格。  
- **选项卡** - 当涉及到操作窗格时，这是在操作窗格中选择给定选项后显示的选项菜单。  

![下图显示这些元素在界面中的放置。](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a>选项卡、字段和部分

*选项卡* 是为了在页面中打开记录的另一方面而在页面中进行的选择。 通常可用于更改特定 *字段* 或用于进行键入的 UI 元素。 

*快速选项卡* 是具有允许同时显示多个选项卡这一额外优点的选项卡。 可以通过选择其后紧随的向下箭头展开快速选项卡。

![下图显示选项卡和快速选项卡的示例。](media/user-interface-02.png)

*部分* 类似选项卡。单词“部分”通常用于描述页面中组织特定类别信息的任何区域。 下图中，“摘要”、“订单和收藏”及“链接”都是部分。

![下图显示选项卡和部分的示例。](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a>对话框和下拉菜单

*对话框* 是进行特定选择以更改或创建记录时打开的窗格。 对话框中包含可用于通过键入进行输入的字段。 有时，可通过给定字段选择向下箭头，用于打开可供选择的选项的列表。 这称为 *下拉菜单*。 在下图中，**类型** 和 **客户组** 字段中包含用于打开下拉菜单的选项。

![下图显示对话框的示例。](media/user-interface-04.png)

在某些情况下，选择给定按钮时，将在该按钮旁边打开对话框。 这称为 *下拉对话框*。 在下图中，选择了 **截止日期** 按钮，从而打开了一个下拉对话框。

![下图显示下拉对话框的示例。](media/user-interface-05.png)

## <a name="notifications"></a>通知

对您查看的对象进行的特定更改将显示为 *通知*。 通知可以在已更改了特定客户的信息时通知您，或者可以在系统无法接受您在特定字段中添加的输入时提醒您。 可以在[预警概览](../get-started/alerts-overview.md)中了解如何自定义收到的通知与哪些信息有关。

通知通过多种方式显示。
- **功能标注** - 在字段、选项卡或其他按钮旁边显示，用于提供有关功能用途的说明。 
- **操作中心** - 将在导航栏中“操作中心”按钮旁边显示一个框，其中包含通知。 可通过选择 **操作中心** 查看有关通知的详细信息。  
- **消息栏** - 在操作窗格下方显示。  

下图显示这些类型的通知的示例。

![下图显示通知的示例。](media/user-interface-06.png)

- **消息框** - 在界面上方显示，必须与其交互后才能继续使用本产品。  

![下图显示消息框的示例。](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a>工具栏、网格和列表

*工具栏* 中包含工具，例如，用于添加字段或删除记录的功能。 有时，工具栏在页面中 *网格* 上方显示。 此区域（即网格）是为包含多列数据的记录行提供的名称。 并非所有网格的上方都有工具栏。

*列表* 是为可滚动浏览的记录集合提供的名称。 可以通过选择将这些记录提取到页面中。 此操作通常将打开一个网格。

![下图显示工具栏、网格和列表的示例。](media/user-interface-08.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
