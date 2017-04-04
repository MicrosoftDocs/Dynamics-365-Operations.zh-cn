---
title: "导航搜索"
description: "此文章在 Microsoft Dynamics 365 中说明如何搜索功能使用导航到页操作。"
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>导航搜索

此文章在 Microsoft Dynamics 365 中说明如何搜索功能使用导航到页操作。

工序的 Dynamics 365。在行业和类别提供功能。 应用程序由多个区域页和帮助您执行不同任务。 快速查找您需要完成您的任务的页面，使用导航搜索功能。 要使用此功能，请单击**“搜索”**图标以显示**“搜索”**框。 然后，您可以在该框中键入一个或多个词。 系统将立即在该应用程序中搜索与您输入的词匹配的相关页面。 例如，您可键入“供应商发票”作为输入，然后系统将显示匹配该输入的结果。 **注意：****“搜索”**框可帮助您查找并导航至页面。 它不会帮助您查找特定的数据或操作。 

[] (![搜索"框。/media/search-box.png)](。/media/search-box.png) 中搜索功能还可充当一个强大方式角色。您迅速导航到特定页。 例如，如果是，您频繁使用的职员**应付帐款付款日志** "页面中，您可以输入“付款日志在”搜索"框。 由于是"页输入标题的完全不一致，列出该页顶部，搜索结果，您可以迅速导航到它。 

搜索![[] (为付款日志。/media/searching 为付款 journal.png)](。/media/searching 为付款 journal.png) 

搜索结果页查看列出标题以及所在的路径。 此列表可帮助您了解页面在该应用程序中的位置。 还帮助您区分结果中的两个或两个以上的相似页面。 当您搜索页面时，您的输入将针对页面标题及其导航路径进行匹配。 例如，如果您输入“应收”** **在"搜索"框中，为您要查看结果页可供您在应收帐款。--即使页标题不包括应收的 Word“”。 

[搜索为这字应收帐款![] (。/media/search 为这 receivable.png 字)](。/media/search 为这 receivable.png 字) 

在管理和安全，仅搜索中所在风险功能：

-   当前配置中已启用的页面（通过 Configuration Key）。
-   用户基于其角色有权访问的页面

搜索结果的列表最多包含 10 个项。 如果您在结果中未找到所查找的内容，则应尝试精炼或更新输入。 从开发角度来看，此导航搜索功能是非常易于使用的，因为在菜单项的部署和其在搜索结果中显示的能力之间几乎没有任何延迟。 只要菜单项链接到导航窗格或仪表板，它们就会自动变为可搜索。 此导航搜索功能还包含一种面向高级用户的高级请求功能：能够基于技术窗体名称快速导航到页面。 许多用户对此系统非常熟悉，他们了解所使用的确切窗体名称。 如果您是这类用户中的一员，则可以在所查找的窗体的名称的前面输入 **form:**。 例如，如果输入 **form: vendinvoice**，则搜索结果将显示窗体名称以 **vendinvoice** 为开头的所有页面。 

[![搜索为窗体 vendinvoice] (。/media/search 为 vendinvoice.png] 窗体)(。/media/search 为 vendinvoice.png 窗体)


