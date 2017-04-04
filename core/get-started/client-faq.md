---
title: "工序 FAQ Dynamics 365 的客户"
description: "文章回答此提供指向有关 Microsoft Dynamics 365 的常见问题工序为客户。"
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

# <a name="dynamics-365-for-operations-client-faq"></a>工序 FAQ Dynamics 365 的客户

文章回答此提供指向有关 Microsoft Dynamics 365 的常见问题工序为客户。

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>当我，为工序时，使用 Dynamics 365 符号为何未加载？
-----------------------------------------------------------------

您的浏览器上的安全设置可能阻止了符号正确加载。 要解决此问题，请尝试执行以下步骤：

-   如果您遇到在 Internet Explorer 的此问题，请单击** **工具，然后单击** ** Internet 选项。  在 Internet 选项，请在** **隐私选项卡上，单击**级的自定义**，并确定该字体下载** **选项。
-   否则，您可能需要添加运算站点的委托到 Dynamics 365 站点的列表。

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>我缺失从 Dynamics AX 2012 功能区的。 我可以一直保持为操作窗格选项卡打开？
我们计划很快实施此功能。 然后用户始终可以选择使在操作窗格的选项卡打开。 如果不这样选择，这些选项卡在不使用时将被折叠，以便为页面腾出更多的屏幕空间。

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>当我，右键单击时，为什么有时候看到不同的快捷菜单？
如果您右键单击了可编辑字段（或者选择了文本），则会显示浏览器的快捷菜单。 此菜单使您可以访问**“剪切”**、**“复制”**和**“粘贴”**命令。 因为，出于安全原因，我们不允许查看器设计程序访问系统剪贴板，我们不能是这些命令到工序快捷菜单的 Dynamics 365。

如果您右键单击字段的标签或控制的具有只读的值，您为工序快捷菜单将看到 Dynamics 365。

若要支持键盘访问更容易，我们在实施计划将来要打开工序快捷菜单的 Dynamics 365 的键盘快捷方式。

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>位置在 Dynamics 365 的功能。工序详细信息？
**“查看详细信息”**选项可通过两种方式访问：

-   如果某个控件拥有**“查看详细信息”**功能，并且该控件具有值，该值将显示为超链接。 您可以单击超链接以打开包含其他详细信息的页面。
-   **详细信息**也是在 Dynamics 365 的选项工序快捷菜单的。 有关{{的：For_more_information_about}} {{更：For_more_information_about}} {{多：For_more_information_about}}，{{信息：For_more_information_about}}在工序快捷菜单的 Dynamics 365 显示时，在您右键单击时，请参阅以前的部分。



