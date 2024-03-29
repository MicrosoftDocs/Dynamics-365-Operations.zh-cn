---
title: 导航搜索
description: 本文说明如何使用搜索功能来导航到页面。
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292328"
---
# <a name="navigation-search"></a>导航搜索

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

本文说明如何使用搜索功能来导航到页面。

此应用程序包括大量区域和页面，可帮助您执行各种任务。 要快速查找完成任务所需的页面，请使用导航搜索功能。

要使用此功能，请单击 **搜索** 图标以显示 **搜索** 框。 然后，您可以在该框中键入一个或多个词。 系统将立即在该应用程序中搜索与您输入的词匹配的相关页面。 例如，您可键入“供应商发票”作为输入，然后系统将显示匹配该输入的结果。

> [!NOTE]
> **搜索** 框可帮助您查找并导航至页面。 它不会帮助您查找特定的数据或操作。

![搜索框。](media/navigation-search.png "搜索框")

## <a name="quickly-navigate-to-a-particular-page"></a>快速导航到特定页面

此导航搜索功能还是帮助您快速导航至某个特定页面的绝佳方式。 例如，如果您是一位经常使用 **付款日记帐** 页面的应付帐款文员，则可在 **搜索** 框中输入付款日记帐”。 由于该输入与页面标题完全匹配，因此将在搜索结果的顶部列出该页面，而且您可以快速导航到该页面。

此搜索结果列表显示页面标题以及导航路径。 这将在应用程序中显示页面的位置。 还帮助您区分结果中的两个或两个以上的相似页面。

当您搜索页面时，您的输入将针对页面标题及其导航路径进行匹配。 例如，如果您在 **搜索** 框中输入“应收”，则将在“应收帐款”区域中看到为您提供的页面的结果 – 即使页面标题不包含“应收”一词。

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>基于技术窗体名称快速导航到页面

此导航搜索功能还包含一种面向高级用户的高级请求功能：能够基于技术窗体名称快速导航到页面。 许多用户对此系统非常熟悉，他们了解所使用的确切窗体名称。 如果您是这类用户中的一员，则可以在所查找的窗体的名称的前面输入 **form:**。 例如，如果输入 **form: vendinvoice**，则搜索结果将显示窗体名称以 **vendinvoice** 为开头的所有页面。

## <a name="administration-and-security"></a>管理和安全

从管理和安全角度来看，此导航搜索功能仅显示两类结果：

- 当前配置中已启用的页面（通过 Configuration Key）。
- 用户基于其角色有权访问的页面。

搜索结果的列表最多包含 10 个项。 如果您在结果中未找到所查找的内容，则应尝试精炼或更新输入。

## <a name="development"></a>开发

从开发角度来看，此导航搜索功能易于使用，因为在菜单项的部署和其在搜索结果中显示的能力之间几乎没有任何延迟。 只要菜单项链接到导航窗格或仪表板，它们就会自动变为可搜索。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
