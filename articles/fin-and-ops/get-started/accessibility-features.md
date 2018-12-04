---
title: "辅助功能"
description: "本主题介绍为帮助残障用户使用 Dynamics 365 for Finance and Operations、Dynamics 365 for Retail 和 Dynamics 365 for Talent 而设计的功能。"
author: TLeforMicrosoft
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a67b51ced4bea11be258aed359a758d88294beb1
ms.openlocfilehash: bc48aa5ccf50705ef0c5087608798875953fe888
ms.contentlocale: zh-cn
ms.lasthandoff: 11/05/2018

---

# <a name="accessibility-features"></a>辅助功能

[!include [banner](../includes/banner.md)]

本主题介绍为帮助残障用户使用 Dynamics 365 for Finance and Operations、Dynamics 365 for Retail 和 Dynamics 365 for Talent 而设计的功能。 例如，有的功能供使用视觉辅助技术（如 Microsoft Windows Narrator）的人员使用。

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Narrator 和仅键盘访问

每个字段和控件都有一个标签和相应的快捷方式的描述。 屏幕阅读器可以读取标签和描述。

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>最常执行操作的快捷方式

对于多数用户，每天的系统使用涉及很多数据输入和键盘交互。 为了增强用户体验，我们创建了快捷方式来帮助您在专门操作的屏幕和快捷方式之间“跳跃”。 有关详细信息，请参阅[键盘快捷方式](shortcut-keys.md)。

## <a name="navigation-search"></a>导航搜索

使用导航窗格（最左边的空格）菜单访问的所有页面，也通过**搜索**框提供。 按 Alt+G 将焦点移至**搜索**框，然后键入页面的名称或描述。

![在搜索框中输入的“银行帐户”](media/6d08b0be32808221023e2aa92d69fd70.png  "在搜索框中输入的“银行帐户”")

有关详细信息，请参阅[导航搜索](navigation-search.md)。

> [!NOTE]
> 您只能直接导航到顶级页面。 二级页面取决于其父级页的信息或上下文。

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>仅键盘用户或低头数据输入的操作搜索

页面上提供的每个操作均可以通过 Tab 序列从键盘访问。 有关 Tab 序列的信息在此主题的后面部分提供。 若要更直接地运行操作，您可以使用操作搜索功能。

### <a name="example"></a>示例

您想要运行在“操作”窗格中**销售订单**选项卡上的**电子邮件通知**组中出现的**电子邮件通知日志**操作。

![“操作”窗格上的电子邮件通知日志操作](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg  "“操作”窗格上的“电子邮件通知日志”操作")

一个选择是使用您的键盘。 按 Ctrl+F6 将焦点移至“操作”窗格，然后反复按 Tab 在所有选项卡和操作之间移动，直到**电子邮件通知日志**操作获得焦点。

不过您还可以更直接地运行操作。 从页面的任何位置，按 Ctrl+Apostrophe (') 可以显示操作的搜索框。

![操作的搜索框](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg  "操作的搜索框")

在搜索框中，键入描述操作的文字。 操作已对您可用，您可以直接运行它。 例如，通过键入**电子邮件**、**通**（部分文字）或**日志**，您可以“跳”到电子邮件通知日志功能。

![在“搜索”框内输入的“电子邮件”](media/image4.png "在“搜索”框内输入的“电子邮件”") 

![在“搜索”框内输入的“通”](media/image5.png "在“搜索”框内输入的“通”")

![在“搜索”框内输入的“日志”](media/image6.png "在“搜索”框内输入的“日志”")

当您完成时，您可以再次按 Ctrl+Apostrophe，在运行操作搜索前将焦点返回到您正在处理的字段。

有关详细信息，请参阅[操作搜索](action-search.md)。

## <a name="tab-sequence"></a>Tab 序列

在每天的系统使用中，执行典型任务不需要填写每个字段。 因此，默认情况下，Tab 序列为“已优化”。 制表位只对典型情况所需的那些基本字段设置。

但是，您可能会发现经常用于执行任务的某些字段未包括在默认的 Tab 序列中。 在这种情况下，如果您使用 Windows Narrator，您可以使用 Windows Narrator 的键盘操作来访问这些字段并检查其内容。 或者，您可以打开**选项**页上的**增强的 Tab 序列**选项。 此选项让所有可编辑的只读字段成为 Tab 序列的一部分。 然后，您可以使用页面个性化来创建自定义 Tab 序列，并忽略不必作为 Tab 序列一部分的字段。 有关个性化的详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。

![“增强的选项卡序列”选项](media/8c0f12bbb3f26032997ef0ba95d89b6a.png  "“增强的选项卡序列”选项")

## <a name="form-patterns"></a>窗体模式

产品中约 90% 的页面基于一小组模式。 这些模式指*窗体模式*。 每个窗体模式用于提供在页面上最常执行的操作。 窗体模式帮助确保熟悉程度和轻松了解，因为频繁使用的操作和数据始终在不同页面的同一位置出现。 由于这些少量的窗体模式，在用户识别窗体模式后，他们可以轻松地了解系统，不论系统内的页数有多少。

若要了解有关窗体模式的详细信息，请参阅[窗体样式和模式](../../dev-itpro/user-interface/form-styles-patterns.md)。

## <a name="responsive-layout"></a>响应性强的布局

此产品主要在各种设备和窗体因子上使用，从最小的屏幕到具有最高分辨率的大屏幕。 我们的响应式布局引擎使用户可以放大到 200% 的缩放级别（或者，在某些情况下，会超过 200%）。

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>帮助开发人员和客户将可理解的想法与其自定义内容相结合的指导

若要更多了解有关启用辅助功能的 Microsoft 最佳实践，请参阅[窗体、产品和控件中的辅助功能](../../dev-itpro/user-interface/enable-accessibility.md)。

