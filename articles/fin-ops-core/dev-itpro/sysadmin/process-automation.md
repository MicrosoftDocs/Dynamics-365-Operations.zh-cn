---
title: 流程自动化
description: 本主题详细介绍如何通过流程自动化简单计划批处理服务器将运行的流程。
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690038"
---
# <a name="process-automation"></a>流程自动化

[!include[banner](../includes/banner.md)]

可通过流程自动化简单计划批处理服务器将运行的流程。 最终用户可通过更新后的计划工作日历视图查看和处理计划的工作和已完成的工作。

## <a name="administration"></a>系统管理

系统管理模块中**设置**菜单下提供所有流程自动化的集中管理页面。 此页将列出系统中设置的所有自动化流程（系列）。 还将允许您直接从此页面添加新的流程自动化。 设置系列后，可以从此列表管理每个系列。 可以选择编辑整个系列，将其删除，查看列表视图中的所有发生次数，或在要暂停计划的工作一段时间时禁用系列。 

禁用此功能后，将不会显示在功能管理中禁用的任何流程。 此外，流程自动化计划引擎不会为禁用的功能计划任何事件或后台流程。 重新启用此功能将导致过去计划的任何事件或后台流程立即运行。

## <a name="calendar-view"></a>日历视图 
流程自动化的一个主要优势是，可以在简单的日历视图中查看计划的工作。  可通过此视图一次查看一周的工作。 您将在**流程自动化**页面右侧看到此视图。 将使用为所选系列计划的工作填充此视图。 

[![流程自动化日历](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>发生次数更改
可以修改每个发生次数，不会影响其来源系列定义的其他发生次数。 可以从日历编辑计划的工作的发生次数，方法是选择**查看/编辑**按钮，然后选择**发生次数**。 这样就可以访问系列设置向导中最初显示的所有设置，并且可以为所选发生次数进行一次性更改。 也可以通过在日历视图中选择**禁用**按钮关闭计划的工作的发生次数。 

## <a name="developer-documentation"></a>开发人员文档 
现在正在撰写开发人员文档，以便让开发人员可以扩展流程自动化框架。 此问题介绍如何创建通过流程自动化向导计划的批处理服务器需要运行的自定义流程，并自动在日历视图中显示。
