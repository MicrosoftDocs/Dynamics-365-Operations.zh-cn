---
title: 在输入订单时搜索产品和产品变型
description: 当您手动创建销售订单行或采购订单行时，使用 **物料编号** 字段搜索产品和产品变型。 当您仅有配置字符串或一个产品维度可用时，它可以让您迅速找到产品变型。
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, PurchTablePart, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b99f668061f429baf56cddb957049833bd74939
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812731"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>在输入订单时搜索产品和产品变型

[!include [banner](../includes/banner.md)]

当您手动创建销售订单行或采购订单行时，使用 **物料编号** 字段搜索产品和产品变型。  当您仅有配置字符串或一个产品维度可用时，它可以让您迅速找到产品变型。

在某些情况下，拥有的太多往往不是最有利的情况，如果是当销售一系列类似产品，以及当您试图记住物料编号或产品搜索名称以查找要放在销售订单上的正确产品时。 您可以使用销售订单行或采购订单行上的 **物料编号** 字段作为搜索字段。 您可以输入产品名称的任何部分、编号或维度，获得显示与搜索词匹配的所有物料的查找。

## <a name="how-search-works"></a>搜索的工作方式
当您搜索产品或产品变型时，了解搜索功能如何查找与您输入的文本匹配的产品非常重要。 交付搜索结果中的关键搜索规则为：

-   搜索结果将返回所有匹配的记录，无论在哪个字段中输入搜索文本。
-   搜索文本需以完整的长度显示在匹配记录中。
-   即使是在匹配记录中的文本字符串的中间找到搜索文本，也会发生匹配。 不必出现在文本字符串的开头。
-   搜索文本即使含有空格，也会被视为单个文本字符串。

### <a name="examples"></a>示例

以下示例通过产品和产品变型说明如何在不同的环境中处理搜索。 **先决条件：** 在 **销售和市场营销 &gt; 设置 &gt; 搜索 &gt; 搜索参数 &gt; 搜索类型** 下，选择此 **完全匹配** 选项。

| 产品类型     | 产品名称    | 显示产品编号 | 物料编号 | 配置 |
|------------------|-----------------|------------------------|-------------|---------------|
| 独特产品 | SpeakerMidRange | D0001                  | D0001       | NA            |
| 产品变型  | 有源扬声器  | D0010:::Black：         | D0010       | 000005        |
| 产品变型  | 有源扬声器  | D0010:::White：         | D0010       | 白色         |

如果您在 **物料编号** 字段中键入“扬声器”，您将在查找结果中获得以上所有产品。 如果您在 **物料编号** 字段中键入“黑色”，您将在结果中获得第二个产品，因为它的显示产品编号中含有文本“黑色”。 这两个示例说明搜索不仅发生在字段的开头，在匹配记录的文本字符串的中间找到搜索文本时，也会发生匹配。  

如果您键入“05”，您在结果中将仅获得第二个产品变型，因为它的配置中含有“05”。 这说明搜索发生在 **搜索条件** 页上的所有已启用字段中。  

如果您键入“扬声器 05”，您不会获得任何结果。 这是因为搜索会查找输入的完整文本。 搜索不会尝试查找“扬声器”，然后将结果缩小到包含“05”的结果。  

使用 **销售和市场营销 &gt; 设置 &gt; 搜索 &gt; 搜索参数** 页上的 **结果数量** 字段可以限制搜索结果的数量。 如果您将此字段设置为 0，则将返回所有搜索结果。 例如如果您设置为 10，它将返回最多 10 个搜索结果。

## <a name="configure-the-product-search"></a>配置产品搜索
在可以使用产品和产品变型搜索功能之前，请执行以下步骤配置产品搜索。 [![配置产品搜索的 3 个步骤\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>步骤 1：在搜索条件中包括所有相关产品和产品变型标识符和维度

比如，您在搜索中可以使用的产品和产品变型标识符和维度包括 **产品名称、物料编号**、**显示产品编号、配置、颜色、尺寸、样式、搜索名称等**。  

转到 **销售和市场 &gt; 设置 &gt; 搜索 &gt; 搜索条件** 页面。 **搜索条件** 页允许您定义客户、目标客户和产品搜索的条件。 确保您使用产品搜索条件筛选页面。 为此，您可以切换至页面菜单中的 **产品**。  

要将显示产品编号添加到搜索条件，请单击页面菜单中的 **新建**。 这将在 **搜索条件** 网格中添加新的记录。 打开 **字段名称** 列查找并选择 **DisplayProductNumber**。 若要将产品配置添加到搜索条件，请在 **搜索条件** 网格中创建新记录，并选择 **字段名称** 列中的 **configId**。 同样，使用 **字段名称** **InventColorId** 对颜色维度创建记录，使用 **InventSizeId** 对尺寸维度创建记录，使用 **InventStyleId** 对样式维度创建记录。

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>第 2 步：填充用于产品搜索的数据库表格

在 **搜索条件** 页中，单击 **更新搜索数据** 按钮。 在 **更新搜索数据** 对话框中，确保将 **来源** 设置为 **产品**，然后单击 **确定**。 系统将在第 1 步指定的所有选定搜索条件聚合到一个表格中。 如果您有许多产品和产品变型，这一操作将非常耗时，因此您可能收到警告。 我们建议您安排在服务器不忙时在批处理服务器上进行搜索表填充。  

填充完表格之前，产品搜索不会提供正确的结果。 如果您无法获得任何搜索结果，请确保此表已填充。  

仅当修订搜索条件时，才须填充表格。 新发布的产品和变型自动添加到表格中。 已删除的产品和变型自动从表中移除。

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>第 3 步：在销售和采购订单行上启用产品搜索查找

您可以转到 **销售和市场营销 &gt; 设置 &gt; 搜索 &gt; 搜索参数**，将 **常规** 选项卡上的 **启用搜索查找** 设置为 **是**，启用此功能。  

对于销售订单行输入，默认行为是当您开始键入 **物料编号** 字段，然后按下 **Tab** 键时，打开 **产品搜索** 页。 **产品搜索** 页面在创建订单行期间更改上下文，因此可能被视为不需要自动插入。 如果您希望获得查找中的搜索结果，并且在订单行输入期间不丢失上下文，您可以使用搜索查找。 如果您搜索产品或产品变型，但在查找中不选择任何内容就按 **Tab** 键，将显示 **产品搜索** 页面。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]