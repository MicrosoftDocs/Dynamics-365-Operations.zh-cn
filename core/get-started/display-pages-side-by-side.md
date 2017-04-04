---
title: "使用“在新窗口中打开”图标并行显示页面"
description: "本文说明如何在 Microsoft Dynamics 365 for Operations 中并行显示页面。"
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 940d086f9c99af54bfcc7911ee7272f9eccba464
ms.lasthandoff: 03/31/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>使用“在新窗口中打开”图标并行显示页面

本文说明如何在 Microsoft Dynamics 365 for Operations 中并行显示页面。

Microsoft Dynamics 365 for Operations 可帮助您高效地执行任务。 在某些情况下，您可能需要并行查看多个页面以快速完成任务。 例如，您可能希望在多个日记帐中验证或输入行。 为此，您通常必须在显示日记帐列表的页面与显示给定日记帐行的页面之间来回切换。 但是，利用**“在新窗口中打开”**功能，您可以并行显示这些页面，以便快速执行任务。 继续上面提到的示例，在查看行时，您可以单击**“在新窗口中打开”**图标。 [![打开在新窗口] (图标。/media/open 在新窗口 icon.png)](。**单击在新窗口中打开**图标的/media/open 在新窗口 icon.png) 在历史记录中打开在新行，以弹出窗口查看器的页面导航原始浏览器，然后返回到查看日志列表中选择该页。 然后，您可以并行显示这两个页面。 在查看完日记帐后，可以在日记帐列表页面上更改所选日记帐，而且弹出窗口中的行页面将自动显示新选定日记帐的行。 [![页查看由端侧] (。{{/media/pages:/media/pages-show-side-by-side.png}} {{显示：/media/pages-show-side-by-side.png}} {{端：/media/pages-show-side-by-side.png}} {{由：/media/pages-show-side-by-side.png}} {{side.png:/media/pages-show-side-by-side.png}})](。{{/media/pages:/media/pages-show-side-by-side.png}} {{显示：/media/pages-show-side-by-side.png}} {{端：/media/pages-show-side-by-side.png}} {{由：/media/pages-show-side-by-side.png}}) {{side.png:/media/pages-show-side-by-side.png}}动态链接和刷新发生因为存在返回页这些数据之间的关系。 如果系统未意识到数据之间的关系，则弹出窗口将不会自动刷新以响应它源自的窗口中的更改。 某些页面具有多个视图，如网格视图、标题视图和详细信息视图。 **“在新窗口中打开”**图标会导致整个页面在新的浏览器窗口中打开。 因此，您无法使用**“在新窗口中打开”**功能并行保留同一页面的视图。 但是，几乎所有此类页面都有一个导航列表，可用来在记录之间切换并实现类似体验。 在使用“**在新窗口中打开**”功能之前，您应先将浏览器的弹出阻止程序配置为允许来自 Dynamics 365 for Operations 站点的 URL 的弹出窗口。 为例，您可以允许 .dynamics.com 的”从“\*弹出窗口的形式出现。 **“在新窗口中打开”**功能仅在窗口中已打开多个页面时适用。 此外，弹出窗口将在未打开多个页面时（即，该窗口中的最后一个页面关闭时）自动关闭。 Dynamics 365 for Operations 还在您导航到该应用程序中的其他区域时关闭打开的页面。 因此，如果您打开弹出窗口并导航到该应用程序中的其他区域，则弹出窗口将自动关闭，因为系统已将这些窗口中的页面关闭。 弹出窗口中的顶部栏显示有关页面已在其中打开且只读的公司的信息。 弹出窗口还依赖主 Dynamics 365 for Operations 浏览器窗口。 如果关闭或刷新主窗口，则所有打开的弹出窗口将变为只读。 这意味着，您仍可查看这些窗口中的信息，但将无法与其进行交互。


