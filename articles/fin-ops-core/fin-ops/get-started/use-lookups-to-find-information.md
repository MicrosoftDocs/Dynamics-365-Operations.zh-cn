---
title: 使用查询来查找信息
description: 在本主题中，您将了解查询功能，以及一些有用的提示，从而充分利用系统中的查询功能。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2672520ddf21e565edee5024d6886cabb18d6e94
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348620"
---
# <a name="find-information-by-using-lookups"></a>使用查询来查找信息

[!include [banner](../includes/banner.md)]

许多字段有查询功能，可帮助您轻松找到正确或需要的值。 已为查询增加了多项增强，提高了这些控件的可用性，提高了用户的工作效率。 在此主题中，您将了解这些新的查询功能，以及一些有用的提示，从而充分利用系统中的查询功能。

## <a name="responsive-lookups"></a>查询响应速度快

在以前版本中，与查询控件交互时，用户必须采取明确的操作才能打开下拉菜单。 具体方法可能是，在控件中键入星号 (\*) 以基于控件的当前值筛选查询，单击下拉按钮，或使用 **Alt**+**向下键** 键盘快捷方式。 已在以下方面修改了查询控件，以便更好地适应当前 Web 实践：

- 现在在键入时如果稍作暂停，将自动打开查询下拉菜单，并根据查询控件的值筛选下拉菜单内容。

    请注意，已弃用了键入星号 (\*) 后自动打开下拉菜单这一原有行为。

- 打开查询下拉菜单之后，将发生以下行为：

    - 光标留在查询控件中（而不是移到下拉菜单内），所以您可以继续修改控件的值。 但是，用户仍然可以使用 **向上键** 和 **向下键** 更改下拉菜单中的行，并输入以选中下拉菜单中的当前行。
    - 对查询控件的值进行任何修改之后，将调整下拉菜单的内容。

例如，假设一个查询字段的名称为 **城市**。

焦点到 **城市** 字段中后，可以通过键入一些字母（如“col”）查找所需城市。 停止键入后，查询将自动打开，并筛选出以“col”开头的城市。

[![typeaheadLookupExample。](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

此时，光标仍在查询字段中。 如果继续键入，让该值为“colum”，查询内容将自动调整以体现控件中的最新值。

![updateFilterLookupExample。](./media/updatefilterlookupexample.png)

即时焦点仍在查询控件中，您也可以使用 **向上键** 或 **向下键** 突出显示所选行。 如果按 **Enter**，将从查询中选中突出显示的行，并更新控件的值。

![changingSelectionLookup。](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>键入多个 ID

输入数据时，用户自然会尝试通过名称而不是表示实体的标识来确定实体（如客户还是供应商）。 许多（但不是所有）查询现在允许上下文数据录入。 用户可通过这项强大的功能在查询控件中键入 ID 或相应名称。

例如，创建销售订单时考虑 **客户帐户**。 此字段显示客户的 **帐户 ID**，但是创建销售订单时，用户通常更愿意为该字段输入 **帐户名称** 而不是 **帐户 ID**，如“Forest Wholesales”而不是“US-003”。

如果用户开始在查询控件中输入 **帐户 ID**，将按照上一部分中所述自动打开下拉菜单，而用户将看到如下所示的查询。

[![输入客户帐户 ID 时的上下文查询。](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

但是，用户现在也可以输入 **帐户名称** 的开头。 如果检测到此行为，用户将看到以下查询。 请注意 **名称** 列如何移动并成为查询中的第一列，以及如何根据 **名称** 列为查询排序和筛选。

[![输入客户名称时的上下文查询。](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>使用网格列标题以执行更高级的筛选和排序

前两部分中讨论的查询增强大大提高了用户根据查询中的 **ID** 或 **名称** 字段的“开始”搜索浏览查询中的行的能力。 但是，有些情况需要更高级的筛选（或排序）才能找到正确的行。 在这些情况下，用户需要使用查询中网格列标题内的筛选和排序选项。 例如，假设需要找到产品为正确的“电缆”的员工输入销售订单行。 在 **物料编号** 控件中键入“电缆”没有用，因为没有产品名称以“电缆”开始。

![emptyitemlookup。](./media/emptyitemlookup.png)

相反，用户需要清除查询控件的值，打开查询下拉菜单，然后使用网格列标题筛选下拉菜单，如下所示。 鼠标（或触控）用户只需单击（或点按）任何列标题即可访问该列的筛选和排序选项。 对于键盘用户，用户只需再次按 **Alt**+**向下键** 将焦点移到下拉菜单中，之后，用户可以切换到正确的列，然后按 **Ctrl**+**G** 打开网格列标题下拉菜单。

[![gridfilteritemlookup。](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

应用筛选器之后（见下图），用户可以照常找到并选择行。

![filtereditemlookup。](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]