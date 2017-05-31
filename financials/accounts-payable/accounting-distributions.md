---
title: "会计分配"
description: "本文提供有关会计分配的信息并介绍可用于处理它们的选项。 会计分配用于将原始凭证的货币金额分配到特定会计科目。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 96ff984310ce5877c37a22f182064a5038d71752
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="accounting-distributions"></a>会计分配

[!include[banner](../includes/banner.md)]


本文提供有关会计分配的信息并介绍可用于处理它们的选项。 会计分配用于将原始凭证的货币金额分配到特定会计科目。 

会计分配是由每个原始凭证使用和扩展的程序范围的功能，如采购订单、供应商发票、支出报表和普通发票。 默认情况下，默认会计分配为每个原始凭证行和货币金额生成，并有条件地为修改启用。 

> [!Note] 
> 某些凭证还支持标题凭证货币金额，例如订单和发票的费用。 

一般会计分配功能提供处理会计分配的以下选项：

-   **分摊金额** – 查看和修改单独凭证标题行和任何子行的会计分配，例如税金或费用。
    -   对于顶部货币金额分配（父分配），主科目和财务维度可以在网格中的 Segmented Entry 控件中直接编辑。 延伸价格是这样一个父分配的典型示例。
    -   分配金额基于的凭证的条款币种。 通常，此币种是交易记录币种。 会计和申报币种金额作为子分类帐会计的一部分生成。
    -   分配显示会计日期和会计事件。 通常，会计事件设置为**无**，直到凭证已过帐/记入日记帐。 此时，会计事件将变为**原始**。 在分配过帐后，就不能修改分配。
    -   **分解**按钮可以针对父分配启用。 **分解**生成新的会计分配，并且，分解可以基于百分比、金额或数量。
    -   **平均分配**按钮可以与**分解**结合使用来在所有分配之间自动平均分配金额。
    -   **重置**按钮在多个分配存在时，可以针对父分配启用。 **重置**通过删除所有现有分配和重新生成默认分配撤消对分配的所有手动修改。
    -   所有子分配，例如折扣、费用和销售税，始终遵循父分配。 您可以在**引用** &gt; **父信息**查看父/子关系。
    -   主科目和财务维度还可能对子项是可编辑的。
    -   会计分配的财务维度按照凭证可扩展的默认模式。 有关详细信息，请参阅相关文章。
    -   差异匹配可能在匹配方案中生成，例如供应商发票和采购订单之间的匹配。 您可以在**引用** &gt; **凭证信息**中查看会计分配之间的匹配关系。
    -   **更正**按钮显示并针对支持更正的凭证启用。 **更正**创建新的分配。 首先，创建撤消原始分配的分配。 不能修改这些分配。 接下来，创建新的正确会计分配。 如果原始分配无法修改，这些分配可以修改。
    -   当行与项目关联时，**项目详细信息**按钮作为扩展启用。 项目会计分配可以修改详细信息，例如融资来源和记录属性。
    -   您可以在**引用**中查看当前凭证会计状态。 状态针对整个凭证，并指示凭证是在进行中或已完成。
-   ** 查看分配** – 查看凭证中所有行和货币金额的会计分配。 您无法从此视图修改会计分配。


有关详细信息，请参阅[会计分配和普通发票的子分类日记帐条目](accounting-distributions-subledger-journal-entries-vendor-invoices.md)。



