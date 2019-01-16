---
title: "Finance and Operations 客户端常见问题"
description: "本文提供对有关 Microsoft Dynamics 365 for Finance and Operations 客户端的常见问题的解答。"
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 74f85f7a1c390d1f21d0423a794ff16c7250d9fa
ms.contentlocale: zh-cn
ms.lasthandoff: 12/18/2018

---

# <a name="finance-and-operations-client-faq"></a>Finance and Operations 客户端常见问题

[!include [banner](../includes/banner.md)]

本文提供对有关 Microsoft Dynamics 365 for Finance and Operations 客户端的常见问题的解答。

## <a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>为何我在使用 Finance and Operations 时未加载符号？

您的浏览器上的安全设置可能阻止了符号正确加载。 要解决此问题，请尝试执行以下步骤：

- 如果在 Internet Explorer 中遇到了此问题，请单击**工具**，然后单击 **Internet 选项**。 在“Internet 选项”对话框中的**隐私**选项卡上，单击**自定义级别**，然后确保已选中**字体下载**选项。
- 否则，您可能必须将 Finance and Operations 站点添加到受信任站点的列表。

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>我的 Dynamics AX 2012 中没有功能区。 我是否能将“操作窗格”上的选项卡一直保持在打开状态？

我们计划很快实现此功能。 用户随后将能够选择一直将“操作窗格”上的选项卡保持在打开状态。 如果不这样选择，这些选项卡在不使用时将被折叠，以便为页面腾出更多的屏幕空间。

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>为何我有时候在右键单击时看到不同的快捷菜单？

如果您右键单击了可编辑字段（或者选择了文本），则会显示浏览器的快捷菜单。 此菜单使您可以访问**剪切**、**复制**和**粘贴**命令。 我们无法将这些命令嵌入到 Finance and Operations 快捷菜单中，因为出于安全原因，浏览器不允许我们以编程方式访问系统剪贴板。

如果您右键单击字段标签或右键单击只读控件的值，则会看到 Finance and Operations 快捷菜单。

为了使键盘访问更加容易，我们计划在将来实施可打开 Finance and Operations 快捷菜单的键盘快捷方式。

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Finance and Operations 中的“查看详细信息”功能在何处？

**查看详细信息**选项可通过两种方式访问：

- 如果某个控件拥有**查看详细信息**功能，并且该控件具有值，该值将显示为超链接。 您可以单击超链接以打开包含其他详细信息的页面。
- **查看详细信息**也是 Finance and Operations 快捷菜单上的选项。 有关在右键单击后何时显示 Finance and Operations 快捷菜单的详细信息，请参阅上一节。

