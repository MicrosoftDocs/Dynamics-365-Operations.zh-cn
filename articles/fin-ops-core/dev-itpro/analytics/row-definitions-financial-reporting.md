---
title: 财务报表设计器中的行定义
description: 行定义是报表组件或构建基块，在财务报表上指定每一行的内容。
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.form: FinancialReports
ms.openlocfilehash: 3325f76f991ea6d2a1b6131f299460e529d63d38
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802437"
---
# <a name="row-definitions-in-financial-report-designer"></a>财务报表设计器中的行定义

[!include [banner](../includes/banner.md)]

行定义是报表组件或构建基块，在财务报表上指定每一行的内容。 可将行定义与列定义、报告结构树定义和报表定义组合以创建可由多个公司使用的构建基块组。

## <a name="create-a-row-definition"></a>创建行定义

1. 在 Report designer 的导航窗格中，单击 **行定义**。
2. 在 **文件** 菜单上，单击 **新建**，然后单击 **行定义**。 有关每个单元格内容的详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)。

## <a name="open-a-row-definition"></a>打开行定义
1. 在 Report designer 的导航窗格中，单击 **行定义**。
2. 双击要打开的行定义的名称。
3. 要查看与行定义关联的任何构建基块，请右键单击行定义，然后选择 **关联**。

## <a name="contents-of-a-row-definition"></a> 行定义的内容
行定义最多可以包含 20,000 个财务维度行并且可以包含以下信息：

- 通过创建节标题、行和空格为报表添加意义的描述性文本，如 **现金** 或 **总收入**
- 财务数据的链接，可以在 Microsoft Dynamics 365 Finance 中包含维度值

    > [!NOTE]
    > 您可以设置一个行定义，以便在每次生成报表时，从财务维度系统中提取数据。

- 基于链接的财务数据的行汇总和公式

通常，行定义中的每个行包含下列类型的信息：

- 对财务维度系统的引用
- 基于数据的汇总或计算
- 格式设置

有两种方法可以在行定义中输入信息︰

- 在新行定义中手动输入行信息。 有关详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)。
- 使用报表设计器可以直接从财务维度拉取行信息。 有关详细信息，请参阅[修改行定义单元格](modify-row-definition-cells-financial-reporting.md)中的“相关/行/单位”部分。

## <a name="add-dimensions-in-a-row-definition"></a> 在行定义中添加维度
维度是数据和值的交集。 可在报表设计器中对数据和值进行分组。 然后可以进一步分类和分析交易记录。 您可使用 **从维度插入行** 对话框同时向行定义添加多个行。 此对话框将针对每个维度显示一列。 下表描述了您可以为每个维度指定的信息。

| 选项                | 说明 |
|-----------------------|-------------|
| 维度             | 标识要添加到行定义的维度的模式。 此模式在维度的每个位置包含一个与号 (\#) 或数字符号 (#)。 通常，对“主科目”维度使用所有与号，对其他维度使用所有数字符号。 |
| 维度范围起始值 | 要添加到行定义中的此维度的第一个值。 |
| 维度范围结束值   | 要添加到行定义的此维度的最后一个值。 |

要向行定义添加维度，请完成下列步骤。

1. 在 Report designer 中，单击 **行定义**，然后打开行定义以修改。
2. 在 **编辑** 菜单上，单击 **插入维度中的行**。
3. 在 **插入维度中的行** 对话框的 **维度** 行中，选择要转移到行定义的维度所在的单元格，然后单击 **所有 &&&**。
4. 要将行定义限制到特定维度值范围，请在 **维度范围起始值** 单元格中输入起始维度值，然后在 **维度范围结束值** 单元格中输入结束维度值。 若要包含所选维度的所有值，请将这些单元格保留为空。

    > [!NOTE]
    > 维度范围中的通配符（\* 或 ?）可能并不会返回您需要的所有结果，具体取决于 ERP 数据库逐份打印数据的方式。

5. 在 **起始行代码** 字段中指定要添加到行定义的第一个维度值的行代码。
6. 在 **每行的增量** 字段中指定连续的行代码之间的间距。 例如，如果第一个行代码为 100，而增量值为 30，则第一批新的行具有代码 100、130、160、190 和 220。 使用为插入新的格式和公式行提供足够空间的增量值。
7. 单击 **OK**。 对于每个选定维度值，向行定义添加一行。

## <a name="adjust-rounding-in-a-row-definition"></a> 在行定义中调整运行化整
当您具有金额已化整的资产负债表时，总额可能不均衡。 例如，如果使用资产负债表报表中的化整选项，同时报表定义也指定化整。 您可以使用行定义中的 **化整调整** 选项以平衡资产负债表中的金额。 您可以关闭化整，或在报表定义的 **设置** 选项卡上进行修改。 下表显示如何化整金额。 在此表中，第 100 行和第 200 行的汇总在启用化整的情况下不同。

| 行代码 | 未化整的金额 | 化整到千分位的金额 |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| 总计    | 7,300                    | 8                                       |

要在资产负债表中调整化整，请完成下列步骤。

1. 在 Report designer 中，单击 **行定义**，然后打开行定义以修改。
2. 在 **编辑** 菜单上，单击 **舍入调整**。
3. 在 **舍入调整** 对话框中，输入下列值：

    - **化整调整行** – 应调整以平衡资产负债表的行的行代码。
    - **总资产行** - 资产负债表中包含总资产的行的行代码。
    - **总债务和权益行** - 资产负债表中包含总债务和权益的行的行代码。
    - **调整金额限制** – 通过自动调整指定限制的正整数。 此金额将与实际化整差异的绝对值进行比较。

    > [!NOTE]
    > 必须将这些行代码链接到您的财务数据。 也就是说，行的 **指向财务维度的链接** 单元格必须包含一个维度值。 请 **勿** 引用描述 (**DESC**)、计算 (**CALC**) 或汇总 (**TOT**) 行。

资产负债表中的金额现在将在启用化整时均匀平衡。

> [!NOTE]
> 根据为报表定义指定的 **化整精度** 选项来应用调整限制。 例如，如果您选择将报表化整到千分位并在 **调整金额限制** 字段中输入 **2**，则当 **化整调整行** 字段中标识的值增加或减少 2,000 以上时，您将收到一条警告消息。

## <a name="format-row-and-column-text"></a>设置行和列文本的格式
您可以通过更改字体和格式文本来自定义报表的外观。 以下各节描述如何设置报表行和列的外观。

### <a name="manage-font-styles"></a>管理字体样式

您可以创建和修改报表的字体样式。 然后可以将这些样式应用到文档中，或应用到报表中的特定行或列。

<table>
<tbody>
<tr>
<td><strong>创建字体样式</strong></td>
<td>
<ol>
<li>在 Report designer 的<strong>格式</strong>菜单上，单击<strong>样式和格式</strong>。</li>
<li>在<strong>样式和格式</strong>对话框中单击<strong>新建</strong>，然后为新样式输入一个唯一名称。</li>
<li>选择字体，然后单击<strong>确定</strong>。</li>
</ol>
</td>
</tr>
<tr>
<td><strong>修改字体样式</strong></td>
<td>
<ol>
<li>在 Report designer 的<strong>格式</strong>菜单上，单击<strong>样式和格式</strong>。</li>
<li>在<strong>样式和格式</strong>对话框中选择要修改的样式，然后单击<strong>修改</strong>。</li>
<li>选择字体，然后单击<strong>确定</strong>。</li>
</ol>
</td>
</tr>
<tr>
<td><strong>应用字体样式</strong></td>
<td>
<ol>
<li>在 Report designer 中，在定义或列定义中，或在页眉和页脚中，选择一个或多个行单元格。</li>
<li>在工具栏的<strong>样式</strong>列表中，选择字体样式。</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>设置行文本的格式

在行定义中指定的格式将覆盖列定义和报表定义中指定的格式。 可以通过使用格式工具栏上的控件来修改文本格式。 这些控件是标准的 Microsoft Windows 控件。

1. 在 Report designer 中，打开要修改的行定义。
2. 选择要设置格式的单元格。 要选择多个单元格，请在选择单元格的同时按住 Ctrl 键。
3. 单击要应用的格式的工具栏按钮。 例如，若要缩进行，请选择行，然后单击工具栏上的 **增加缩进** ![增加缩进。](media/indent.gif "增加缩进") 。

### <a name="adjust-columns-while-you-design-reports"></a>在设计报表时调整列

为了便于在行定义中查看正在处理的列，您可调整列宽，还可以在视图窗格中隐藏（最小化）或显示列。 您所做的修改只影响屏幕上列的外观。 它们并不影响报表中的列格式。

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>更改列在视图窗格中的宽度

1. 在 Report designer 中，打开要修改的行定义。
2. 在 **格式** 菜单上，选择 **列宽**。
3. 在 **列宽** 对话框中，输入值，然后单击 **确定**。 或者，您还可拖动列标题单元格的右边界来更改列宽。

### <a name="hide-columns-in-the-view-pane"></a>在视图窗格中隐藏列

1. 在 Report designer 中，打开要修改的行定义。
2. 选择要最小化的一列或多列。
3. 右键单击，然后单击 **隐藏**。

### <a name="show-all-hidden-columns-in-the-view-pane"></a>在视图窗格中显示所有隐藏列

1. 在 Report designer 中，打开要修改的行定义。
2. 右键单击要显示的最小化列，然后单击 **取消隐藏**。


## <a name="additional-resources"></a>其他资源

[财务报告](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
