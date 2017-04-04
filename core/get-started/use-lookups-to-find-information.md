---
title: "使用查找信息查找"
description: "在工序的 Microsoft Dynamics 365 中，许多字段可能帮助您轻松查找正确或所需值的查找。 若干改进、添加到这些控件使更有效以及使用户更加具有生产上的查找。 {{在此：In}}主题，您将这些新获悉的查找功能，并接收一些帮助性提示可最佳使用的{{脱离：out_of}}在系统中进行查找。"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>使用查找信息查找

在工序的 Microsoft Dynamics 365 中，许多字段可能帮助您轻松查找正确或所需值的查找。 若干改进、添加到这些控件使更有效以及使用户更加具有生产上的查找。 {{在此：In}}主题，您将这些新获悉的查找功能，并接收一些帮助性提示可最佳使用的{{脱离：out_of}}在系统中进行查找。  

<a name="responsive-lookups"></a>响应式查找
------------------

在以前版本工序的 Dynamics 365，与交互，则查找控制，用户必须获取、行动时打开下拉菜单。 这可能是订单通过键入一个星号 (\*筛选) "控制的控制基于当前值的查找按钮，单击下拉，或者使用+** ** Alt **向下箭头**键盘快捷方式。 查找控制以下方面进行修改改善与当前网页/网站/web 惯例的对齐：

-   查找下拉菜单将自动打开现在，在键入的可变的停留后，将下拉菜单控制基于物料筛选查找的值。
    -   注意自动的期初旧行为下拉在键入星号后 (\*贬损)。
-   在查找下拉菜单打开之后，下将造成这一情况：
    -   在查找游标控制要维护 ({{而不是：instead_of}}移动到下拉菜单) 的焦点，以便您可以继续对控制的值的所有修改。 但是，用户仍可以使用**箭头** **和向下箭头**更改在下拉菜单中的行，并输入所在下拉菜单中的当前行。
    -   则任何修改对控制查找的值之后，下拉菜单中的内容将被调整。

例如，考虑查找字段调用** **城市。 

在作为在时**城市** "字段，可以开始确定您通过输入某些字母所需的城市，如“col”。  在停止键入后，将查找将自动打开，以筛选到”开始“col 的那些城市。 

[] (![typeaheadLookupExample。/media/typeaheadlookupexample.png)](。/media/typeaheadlookupexample.png) 

此时，游标仍在查找字段。 如果您最后键入值，因此是“colum，查找”内容自动调整反映控制的最新值。 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

即使焦点仍在查找控制中，您还可以使用突出显示您要选择的行的** ** **箭头或向下箭头**参数。 如果您按**输入**突出显示的行从查找将选择，并且控制的值将更新。 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>输入超过 ID
在输入数据时，尝试标识实体，例如是客户还是供应商。名称，而不是代表实体是自然的用户的标识符。 在工序的当前版本，许多，Dynamics 365 (但并非全部) 的查找现在允许环境的数据输入。 此功能强大的功能允许用户键入相应的名称或 ID 查找为控制。 

例如，考虑** **客户帐户字段，在创建销售订单时。 **此字段显示帐户 ID **的，但是用户，客户通常其输入** **科目名称{{而不是：instead_of}} **帐户 ID **此字段的，但创建一个销售订单，例如" {{而林批发“不是：instead_of}}”US-003 时”。

如果用户启动输入** **帐户 ID 查找为控制，下拉菜单将自动打开。该前面的部分中描述，并且会看到用户查找如下所示。

[![环境的查找，在客户帐户 ID 输入] (。/media/howtocontextuallookups-1.png)](。/media/howtocontextuallookups-1.png)

但是，用户现在还输入开始** **科目名称。 如果检测到这，则用户将看到以下"查找"。 通知**列名称**如何移动在查找的第一列，但并找到，如何基于** **名称列进行排序和筛选。

[![环境的查找，在客户端输入] (名称。/media/howtocontextuallookups-2.png)](。/media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>使用网格更高级筛选和排序的列标题
上面两个部分中讨论的查找改进特别会提高用户的能力导航基于的查找的行“以”** ID 的搜索或开始** ** **在查找名称"字段中。 不过，在更高级筛选或排序的条件 () 需要的查找正确的行。 在这些情况下，在信息查找中的网格列标题的用户要求用于筛选和排序的选项。 例如，考虑需要找到输入正确的“为电缆”产品的销售订单行的员工。 键入“电缆”到** **控制物料编号中不很有用，其中，尽管不以电缆开始“的产品名称”。 

![emptyitemlookup](./media/emptyitemlookup.png) 

而是使用网格列标题，用户需要清除值查找控制，打开查找下拉菜单和筛选"下拉菜单中，如下所示。 鼠标 (或联系人) (用户可以通过单击任何列标题或联系人) 访问该列中的筛选和排序的选项。 键盘对于用户，则用户需要按** Alt **+** ** **向下箭头**第二次焦点移至下拉菜单，在后，用户可能选项卡上为正确的列，然后按下 Ctrl+** ** ** G **打开网格列标题下拉菜单。 

[] (![gridfilteritemlookup。/media/gridfilteritemlookup.png)](。/media/gridfilteritemlookup.png) 

在应用筛选器 (参阅下面图像) 后，用户可以照常找到和选择一行。 

![filtereditemlookup](./media/filtereditemlookup.png)


