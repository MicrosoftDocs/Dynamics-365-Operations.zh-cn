---
title: "Dynamics 365 for Operations 客户端常见问题"
description: "本文提供对有关 Microsoft Dynamics 365 for Operations 客户端的常见问题的解答。"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 2c99b2e1f7ddecb61be62832ca1a8d3ac1fd21a8
ms.lasthandoff: 03/31/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Dynamics 365 for Operations 客户端常见问题

[!include[banner](../includes/banner.md)]


本文提供对有关 Microsoft Dynamics 365 for Operations 客户端的常见问题的解答。

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>为何我在使用 Dynamics 365 for Operations”时未加载符号？
-----------------------------------------------------------------

您的浏览器上的安全设置可能阻止了符号正确加载。 要解决此问题，请尝试执行以下步骤：

-   如果在 Internet Explorer 中遇到了此问题，请单击**工具**，然后单击 **Internet 选项**。  在“Internet 选项”对话框中的**隐私**选项卡上，单击**自定义级别**，然后确保已选中**字体下载**选项。
-   否则，您可能必须将 Dynamics 365 for Operation”站点添加受信任站点的列表。

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>我的 Dynamics AX 2012 中没有功能区。 我是否能将“操作窗格”上的选项卡一直保持在打开状态？
我们计划很快实现此功能。 用户随后将能够选择一直将“操作窗格”上的选项卡保持在打开状态。 如果不这样选择，这些选项卡在不使用时将被折叠，以便为页面腾出更多的屏幕空间。

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>为何我有时候在右键单击时看到不同的快捷菜单？
如果您右键单击了可编辑字段（或者选择了文本），则会显示浏览器的快捷菜单。 此菜单使您可以访问**“剪切”**、**“复制”**和**“粘贴”**命令。 我们无法将这些命令嵌入到 Dynamics 365 for Operations 快捷菜单中，因为出于安全原因，浏览器不允许我们以编程方式访问系统剪贴板。

如果您右键单击字段标签或右键单击只读控件的值，则会看到 Dynamics 365 for Operations 快捷菜单。

为了使键盘访问更加容易，我们计划在将来实施可打开 Dynamics 365 for Operations 快捷菜单的键盘快捷方式。

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations 中的“查看详细信息”功能在何处？
**“查看详细信息”**选项可通过两种方式访问：

-   如果某个控件拥有**“查看详细信息”**功能，并且该控件具有值，该值将显示为超链接。 您可以单击超链接以打开包含其他详细信息的页面。
-   **查看详细信息**也是 Dynamics 365 for Operations 快捷菜单上的选项。 有关在右击单击后何时显示 Dynamics 365 for Operations 快捷菜单的详细信息，请参阅上一节。





