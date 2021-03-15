---
title: 设计配置以生成 Excel 格式的文档
description: 本主题介绍如何设计电子报告 (ER) 格式以填写 Excel 模板，然后生成 Excel 格式的传出文档。
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094021"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>设计用于生成 Excel 格式文档的配置

[!include[banner](../includes/banner.md)]

可以设计一种[电子申报 (ER)](general-electronic-reporting.md) 格式配置，该配置中有一个 ER [格式组件](general-electronic-reporting.md#FormatComponentOutbound)可配置来生成 Microsoft Excel 工作簿格式的传出文档。 必须为此用途使用特定 ER 格式组件。

若要了解此功能，请执行[设计用于生成 OPENXML 格式的报表的配置](tasks/er-design-reports-openxml-2016-11.md)主题中的步骤。

## <a name="add-a-new-er-format"></a>添加新的 ER 格式

添加新的 ER 格式配置以生成 Excel 工作簿格式的传出文档时，必须为格式的 **格式类型** 属性选择 **Excel** 值，或将 **格式类型** 属性保留为空。

- 如果选择 **Excel**，可以将格式配置为只能生成 Excel 格式的传出文档。
- 如果将属性保留为空，可以将格式配置为使用 ER 框架支持的任何格式生成传出文档。

若要配置此配置的 ER 格式组件，请在操作窗格上选择 **设计器**，然后打开要用于在 ER 操作设计器中进行编辑的 ER 格式组件。

![配置页面](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel 文件组件

### <a name="manual-entry"></a>手动输入

必须向配置的 ER 格式添加 **Excel\\文件** 组件，才能生成 Excel 格式的传出文档。

![Excel\File 组件](./media/er-excel-format-add-file-component.png)

若要指定传出文档的布局，请向 **Excel\\文件** 组件添加一个扩展名为 .xlsx 的 Excel 工作簿充当传出文档的模板。

> [!NOTE]
> 手动附加模板时，必须使用已经在 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中为此目的配置的[文档类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)。

![向“Excel\文件”组件添加附件](./media/er-excel-format-add-file-component2.png)

若要指定在运行配置的 ER 格式时如何填写附加的模板，必须向 **Excel\\文件** 组件添加嵌套的 **工作表**、**范围** 和 **单元格** 组件。 每个嵌套组件必须与一个 Excel 命名项关联。

### <a name="template-import"></a>导入模板

可以选择操作窗格 **导入** 选项卡上的 **从 Excel 导入**，以将新模板导入到空白 ER 格式中。 在此示例中，将自动创建一个 **Excel\\文件** 组件，并为其附加导入的模板。 还将根据发现的 Excel 命名项列表自动创建所有必需 ER 组件。

![选择“从 Excel 导入”](./media/er-excel-format-import-template.png)

> [!NOTE]
> 如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。

## <a name="sheet-component"></a>工作表组件

**工作表** 组件指示必须填写的 Excel 工作簿附件的工作表。 Excel 模板中的工作表的名称在此组件的 **工作表** 属性中定义。

> [!NOTE]
> 此组件对其中包含单个工作表的 Excel 工作簿可选。

在 ER 操作设计器的 **映射** 选项卡上，可以配置 **工作表** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：

- 如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将把适当的工作表放入生成的文档中。
- 如果将 **启用** 属性的表达式配置为在运行时返回 **False**，生成的文档中将不包含工作表。

![工作表组件的示例](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>范围组件

**范围** 组件指示此 ER 组件必须控制的 Excel 范围。 范围的名称在此组件的 **Excel 范围** 属性中定义。

**复制方向** 属性指定是否在生成的文档中重复范围和如何重复范围。

- 如果 **复制方向** 属性设置为 **不复制**，生成的文档中将不重复相应 Excel 范围。
- 如果 **复制方向** 属性设置为 **垂直**，生成的文档中将重复相应 Excel 范围。 将把复制的每个范围放到 Excel 模板中原始范围下。 复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。
- 如果 **复制方向** 属性设置为 **水平**，生成的文档中将重复相应 Excel 范围。 将把复制的每个范围放到 Excel 模板中原始范围右侧。 复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。

若要详细了解水平复制，请执行[使用可水平扩展的范围在 Excel 报表中动态添加列](tasks/er-horizontal-1.md)中的步骤。

**范围** 组件可以有其他嵌套 ER 组件，用于在相应 Excel 命名范围中输入值。

- 如果使用 **文本** 组的任何组件输入值，将把该值在 Excel 范围中作为文本值输入。

    > [!NOTE]
    > 使用此模式根据应用程序中定义的语言环境为输入的值设置格式。

- 如果使用  **Excel** 组的 **单元格** 组件输入值，该值将在 Excel 范围中作为该 **单元格** 组件的绑定定义的数据类型（如 **字符串**、**实数** 或 **整数**）的值。

    > [!NOTE]
    > 使用此模式让 Excel 应用程序根据打开传出文档的本地计算机的区域设置来为输入的值设置格式。

在 ER 操作设计器的 **映射** 选项卡上，可以配置 **范围** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：

- 如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应范围。
- 如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，将不在生成的文档中填写相应范围。
- 如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，生成的文档中将包含这些行和列，但显示为隐藏行和隐藏列。

## <a name="cell-component"></a>单元格组件

**单元格** 组件用于填写 Excel 命名列、形状和图片。 若要指示 **单元格** ER 组件必须填写的 Excel 命名对象，必须在 **单元格** 组件的 **Excel 范围** 属性中指定该对象的名称。

在 ER 操作设计器的 **映射** 选项卡上，可以配置 **单元格** 组件的 **启用** 属性以指定是否必须在生成的文档中填写该对象：

- 如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应对象。 此 **单元格** 组件的绑定指定放入相应对象中的值。
- 如果将 **启用** 属性的表达式配置为在运行时返回 **False**，将不在生成的文档中填写相应对象。

将配置 **单元格** 组件以在单元格中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。 在此情况下，将在单元格中把该值作为相同数据类型的值输入。

配置 **单元格** 组件以在 Excel 形状中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。 在此情况下，将在 Excel 形状中把该值作为该形状的文本输入。 对于非 **字符串** 事件类型的值，将自动转换为文本。

> [!NOTE]
> 可以配置 **单元格** 组件以仅在支持形状文本属性时填写形状。

配置 **单元格** 组件以在 Excel 图片中输入值时，可以与返回以二进制格式表示图像的 **容器** 数据类型的值的数据源绑定。 在这种情况下，值将作为图像输入到 Excel 图片中。

> [!NOTE]
> 将把每个 Excel 图片和形状视为通过其右上角锚定到特定 Excel 单元格或范围。 如果要复制 Excel 图片或形状，必须将锚定的单元格或范围配置为复制的单元格或范围。

若要详细了解如何嵌入图像和形状，请参阅[使用 ER 在生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。

## <a name="page-break-component"></a>分页符组件

**分页符** 组件强制 Excel 新分页。 如果希望使用 Excel 的默认分页，则无需此组件，但是如果希望 Excel 按照您的 ER 格式构造分页，应使用此组件。

## <a name="edit-an-added-er-format"></a>编辑添加的 ER 格式

### <a name="update-a-template"></a>更新模板

可以选择操作窗格 **导入** 选项卡上的 **从 Excel 更新**，以将更新后的模板导入到可编辑的 ER 格式中。 在此过程中，将把所选 **Excel\\文件** 组件的模板替换为新模板。 将与更新后 ER 模板的内容同步可编辑 ER 格式的内容。

- 如果在可编辑格式中找不到 ER 格式组件，将为每个 Excel 名称自动创建一个新 ER 格式组件。
- 如果找不到合适的 Excel 名称，则会从可编辑的 ER 格式中删除每个 ER 格式组件。

> [!NOTE]
> 如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。
>
> 如果可编辑 ER 格式中最初包含 **工作表** 元素，建议在导入更新后的模板时，将 **创建 Excel 工作表格式元素** 选项设置为 **是**。 否则，将从头开始创建原始 **工作表** 元素的所有嵌套元素。 因此，更新后的 ER 中将不包含重新创建的格式元素的所有绑定。

![在“从 Excel 更新”对话框中创建 Excel 工作表格式元素](./media/er-excel-format-update-template.png)

若要详细了解此功能，请执行[通过重新应用 Excel 模板修改电子报告格式](modify-electronic-reporting-format-reapply-excel-template.md)中的步骤。

## <a name="validate-an-er-format"></a>验证 ER 格式

验证可编辑的 ER 格式时，将执行一致性检查以确保当前所用 Excel 模板中包含 Excel 名称。 将通知您任何不一致。 将为某些不一致提供用于自动解决问题的选项。

![验证错误消息](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>控制 Excel 公式的计算

如果生成的传出文档为 Microsoft Excel 工作簿格式，该文档的某些单元格中可能包含 Excel 公式。 如果启用了 **支持在电子申报框架中使用 EPPlus 库** 功能，可以通过更改正在使用的 Excel 模板中的 **计算选项** 的[参数](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows)值来控制何时计算公式。

- 如果选择 **自动**，则每次为生成的文档附加新的范围、单元格等时，都将重新计算所有依赖 公式。
    >[!NOTE]
    > 这可能会导致包含多个相关公式的 Excel 模板出现性能问题。
- 如果选择 **手动**，则可避免在生成文档时重新计算公式。
    >[!NOTE]
    > 使用 Excel 打开生成的文档进行预览时，将手动强制重新计算公式。
    > 如果配置的 ER 目标位置需要使用生成的文档，但 Excel 中无预览（PDF 转换、电子邮件等），请不要使用此选项，因为生成的文档中包含的公式中可能不包含值。

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[设计以 OPENXML 格式生成报表的配置](tasks\er-design-reports-openxml-2016-11.md)

[通过重新应用 Excel 模板修改电子报告格式](modify-electronic-reporting-format-reapply-excel-template.md)

[使用可水平扩展的范围在 Excel 报表中动态添加列](tasks/er-horizontal-1.md)

[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)

[配置电子申报 (ER) 以便将数据导入 Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]