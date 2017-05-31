---
title: "使用“在新窗口中打开”图标并行显示页面"
description: "本文说明如何在 Microsoft Dynamics 365 for Operations 中并行显示页面。"
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b6985b600fb7eb84f7e3db8d49561eab24341a03
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>使用“在新窗口中打开”图标并行显示页面

[!include[banner](../includes/banner.md)]


本文说明如何在 Microsoft Dynamics 365 for Operations 中并行显示页面。

Microsoft Dynamics 365 for Operations 可帮助您高效地执行任务。 在某些情况下，您可能需要并行查看多个页面以快速完成任务。 例如，您可能希望在多个日记帐中验证或输入行。 为此，您通常必须在显示日记帐列表的页面与显示给定日记帐行的页面之间来回切换。 但是，利用**“在新窗口中打开”**功能，您可以并行显示这些页面，以便快速执行任务。 继续上面提到的示例，在查看行时，您可以单击**“在新窗口中打开”**图标。 [![“在新窗口中打开”图标](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) 单击**在新窗口中打开**图标将在新的弹出浏览器中打开行页面，然后将历史记录中的原始浏览器导航回显示了日记帐列表的页面。 然后，您可以并行显示这两个页面。 在查看完日记帐后，可以在日记帐列表页面上更改所选日记帐，而且弹出窗口中的行页面将自动显示新选定日记帐的行。 [![并行显示页面](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) 由于返回这些页面的数据之间存在的关系，将会发生动态链接和刷新。 如果系统未意识到数据之间的关系，则弹出窗口将不会自动刷新以响应它源自的窗口中的更改。 某些页面具有多个视图，如网格视图、标题视图和详细信息视图。 **“在新窗口中打开”**图标会导致整个页面在新的浏览器窗口中打开。 因此，您无法使用**“在新窗口中打开”**功能并行保留同一页面的视图。 但是，几乎所有此类页面都有一个导航列表，可用来在记录之间切换并实现类似体验。 在使用“**在新窗口中打开**”功能之前，您应先将浏览器的弹出阻止程序配置为允许来自 Dynamics 365 for Operations 站点的 URL 的弹出窗口。 例如，您可允许来自“\*.dynamics.com”的弹出窗口。 **“在新窗口中打开”**功能仅在窗口中已打开多个页面时适用。 此外，弹出窗口将在未打开多个页面时（即，该窗口中的最后一个页面关闭时）自动关闭。 Dynamics 365 for Operations 还在您导航到该应用程序中的其他区域时关闭打开的页面。 因此，如果您打开弹出窗口并导航到该应用程序中的其他区域，则弹出窗口将自动关闭，因为系统已将这些窗口中的页面关闭。 弹出窗口中的顶部栏显示有关页面已在其中打开且只读的公司的信息。 弹出窗口还依赖主 Dynamics 365 for Operations 浏览器窗口。 如果关闭或刷新主窗口，则所有打开的弹出窗口将变为只读。 这意味着，您仍可查看这些窗口中的信息，但将无法与其进行交互。




