---
title: "导航搜索"
description: "本文说明如何使用搜索功能导航到 Microsoft Dynamics 365 for Operations 中的页面。"
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

[!include[banner](../includes/banner.md)]


本文说明如何使用搜索功能导航到 Microsoft Dynamics 365 for Operations 中的页面。

Dynamics 365 for Operations 提供了面向一系列广泛的行业和类别的功能。 此应用程序包括大量区域和页面，可帮助您执行各种任务。 要快速查找完成任务所需的页面，请使用导航搜索功能。 要使用此功能，请单击**“搜索”**图标以显示**“搜索”**框。 然后，您可以在该框中键入一个或多个词。 系统将立即在该应用程序中搜索与您输入的词匹配的相关页面。 例如，您可键入“供应商发票”作为输入，然后系统将显示匹配该输入的结果。 **注意：****“搜索”**框可帮助您查找并导航至页面。 它不会帮助您查找特定的数据或操作。 

[![search-box](./media/search-box.png)](./media/search-box.png) 此导航搜索功能还是帮助您快速导航至某个特定页面的绝佳方式。 例如，如果您是一位经常使用**付款日记帐**页面的应付帐款文员，则可在搜索框中输入“付款日记帐”。 由于该输入与页面标题完全匹配，因此将在搜索结果的顶部列出该页面，而且您可以快速导航到该页面。 

[![searching-for-payment-journal](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

此搜索结果列表显示页面标题以及导航路径。 此列表可帮助您了解页面在该应用程序中的位置。 还帮助您区分结果中的两个或两个以上的相似页面。 当您搜索页面时，您的输入将针对页面标题及其导航路径进行匹配。 例如，如果您在 ** ** 搜索框中输入“应收”，则将在“应收帐款”区域中看到为您提供的页面的结果 - 即使页面标题不包含“应收”一词。 

[![search-for-the-word-receivable](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

从管理和安全角度来看，此导航搜索功能仅存在于：

-   当前配置中已启用的页面（通过 Configuration Key）。
-   用户基于其角色有权访问的页面

搜索结果的列表最多包含 10 个项。 如果您在结果中未找到所查找的内容，则应尝试精炼或更新输入。 从开发角度来看，此导航搜索功能是非常易于使用的，因为在菜单项的部署和其在搜索结果中显示的能力之间几乎没有任何延迟。 只要菜单项链接到导航窗格或仪表板，它们就会自动变为可搜索。 此导航搜索功能还包含一种面向高级用户的高级请求功能：能够基于技术窗体名称快速导航到页面。 许多用户对此系统非常熟悉，他们了解所使用的确切窗体名称。 如果您是这类用户中的一员，则可以在所查找的窗体的名称的前面输入 **form:**。 例如，如果输入 **form: vendinvoice**，则搜索结果将显示窗体名称以 **vendinvoice** 为开头的所有页面。 

[![search-for-form-vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)




