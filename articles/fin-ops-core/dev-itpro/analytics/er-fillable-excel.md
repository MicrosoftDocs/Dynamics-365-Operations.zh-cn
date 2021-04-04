---
title: 设计配置以生成 Excel 格式的文档
description: 本主题介绍如何设计电子报告 (ER) 格式以填写 Excel 模板，然后生成 Excel 格式的传出文档。
author: NickSelin
manager: AnnBe
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a82afcdeb45bad79a008c3135ef332cf01c0b580
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574165"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="adb3e-103">设计用于生成 Excel 格式文档的配置</span><span class="sxs-lookup"><span data-stu-id="adb3e-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adb3e-104">可以设计一种[电子申报 (ER)](general-electronic-reporting.md) 格式配置，该配置中有一个 ER [格式组件](general-electronic-reporting.md#FormatComponentOutbound)可配置来生成 Microsoft Excel 工作簿格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="adb3e-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="adb3e-105">必须为此用途使用特定 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="adb3e-106">若要了解此功能，请执行[设计用于生成 OPENXML 格式的报表的配置](tasks/er-design-reports-openxml-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="adb3e-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="adb3e-107">添加新的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="adb3e-107">Add a new ER format</span></span>

<span data-ttu-id="adb3e-108">添加新的 ER 格式配置以生成 Excel 工作簿格式的传出文档时，必须为格式的 **格式类型** 属性选择 **Excel** 值，或将 **格式类型** 属性保留为空。</span><span class="sxs-lookup"><span data-stu-id="adb3e-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="adb3e-109">如果选择 **Excel**，可以将格式配置为只能生成 Excel 格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="adb3e-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="adb3e-110">如果将属性保留为空，可以将格式配置为使用 ER 框架支持的任何格式生成传出文档。</span><span class="sxs-lookup"><span data-stu-id="adb3e-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="adb3e-111">若要配置此配置的 ER 格式组件，请在操作窗格上选择 **设计器**，然后打开要用于在 ER 操作设计器中进行编辑的 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![配置页面](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="adb3e-113">Excel 文件组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="adb3e-114">手动输入</span><span class="sxs-lookup"><span data-stu-id="adb3e-114">Manual entry</span></span>

<span data-ttu-id="adb3e-115">必须向配置的 ER 格式添加 **Excel\\文件** 组件，才能生成 Excel 格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="adb3e-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\File 组件](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="adb3e-117">若要指定传出文档的布局，请向 **Excel\\文件** 组件添加一个扩展名为 .xlsx 的 Excel 工作簿充当传出文档的模板。</span><span class="sxs-lookup"><span data-stu-id="adb3e-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-118">手动附加模板时，必须使用已经在 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中为此目的配置的[文档类型](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types)。</span><span class="sxs-lookup"><span data-stu-id="adb3e-118">When you manually attach a template, you must use a [document type](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![向“Excel\文件”组件添加附件](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="adb3e-120">若要指定在运行配置的 ER 格式时如何填写附加的模板，必须向 **Excel\\文件** 组件添加嵌套的 **工作表**、**范围** 和 **单元格** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="adb3e-121">每个嵌套组件必须与一个 Excel 命名项关联。</span><span class="sxs-lookup"><span data-stu-id="adb3e-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="adb3e-122">导入模板</span><span class="sxs-lookup"><span data-stu-id="adb3e-122">Template import</span></span>

<span data-ttu-id="adb3e-123">可以选择操作窗格 **导入** 选项卡上的 **从 Excel 导入**，以将新模板导入到空白 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="adb3e-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="adb3e-124">在此示例中，将自动创建一个 **Excel\\文件** 组件，并为其附加导入的模板。</span><span class="sxs-lookup"><span data-stu-id="adb3e-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="adb3e-125">还将根据发现的 Excel 命名项列表自动创建所有必需 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![选择“从 Excel 导入”](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="adb3e-127">如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="adb3e-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="adb3e-128">工作表组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-128">Sheet component</span></span>

<span data-ttu-id="adb3e-129">**工作表** 组件指示必须填写的 Excel 工作簿附件的工作表。</span><span class="sxs-lookup"><span data-stu-id="adb3e-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="adb3e-130">Excel 模板中的工作表的名称在此组件的 **工作表** 属性中定义。</span><span class="sxs-lookup"><span data-stu-id="adb3e-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-131">此组件对其中包含单个工作表的 Excel 工作簿可选。</span><span class="sxs-lookup"><span data-stu-id="adb3e-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="adb3e-132">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **工作表** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：</span><span class="sxs-lookup"><span data-stu-id="adb3e-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="adb3e-133">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将把适当的工作表放入生成的文档中。</span><span class="sxs-lookup"><span data-stu-id="adb3e-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="adb3e-134">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，生成的文档中将不包含工作表。</span><span class="sxs-lookup"><span data-stu-id="adb3e-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![工作表组件的示例](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="adb3e-136">范围组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-136">Range component</span></span>

<span data-ttu-id="adb3e-137">**范围** 组件指示此 ER 组件必须控制的 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="adb3e-138">范围的名称在此组件的 **Excel 范围** 属性中定义。</span><span class="sxs-lookup"><span data-stu-id="adb3e-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="adb3e-139">**复制方向** 属性指定是否在生成的文档中重复范围和如何重复范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="adb3e-140">如果 **复制方向** 属性设置为 **不复制**，生成的文档中将不重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="adb3e-141">如果 **复制方向** 属性设置为 **垂直**，生成的文档中将重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="adb3e-142">将把复制的每个范围放到 Excel 模板中原始范围下。</span><span class="sxs-lookup"><span data-stu-id="adb3e-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="adb3e-143">复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。</span><span class="sxs-lookup"><span data-stu-id="adb3e-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="adb3e-144">如果 **复制方向** 属性设置为 **水平**，生成的文档中将重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="adb3e-145">将把复制的每个范围放到 Excel 模板中原始范围右侧。</span><span class="sxs-lookup"><span data-stu-id="adb3e-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="adb3e-146">复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。</span><span class="sxs-lookup"><span data-stu-id="adb3e-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="adb3e-147">若要详细了解水平复制，请执行[使用可水平扩展的范围在 Excel 报表中动态添加列](tasks/er-horizontal-1.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="adb3e-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="adb3e-148">**范围** 组件可以有其他嵌套 ER 组件，用于在相应 Excel 命名范围中输入值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="adb3e-149">如果使用 **文本** 组的任何组件输入值，将把该值在 Excel 范围中作为文本值输入。</span><span class="sxs-lookup"><span data-stu-id="adb3e-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="adb3e-150">使用此模式根据应用程序中定义的语言环境为输入的值设置格式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="adb3e-151">如果使用  **Excel** 组的 **单元格** 组件输入值，该值将在 Excel 范围中作为该 **单元格** 组件的绑定定义的数据类型（如 **字符串**、**实数** 或 **整数**）的值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="adb3e-152">使用此模式让 Excel 应用程序根据打开传出文档的本地计算机的区域设置来为输入的值设置格式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="adb3e-153">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **范围** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：</span><span class="sxs-lookup"><span data-stu-id="adb3e-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="adb3e-154">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="adb3e-155">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，将不在生成的文档中填写相应范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="adb3e-156">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，生成的文档中将包含这些行和列，但显示为隐藏行和隐藏列。</span><span class="sxs-lookup"><span data-stu-id="adb3e-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="adb3e-157">单元格组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-157">Cell component</span></span>

<span data-ttu-id="adb3e-158">**单元格** 组件用于填写 Excel 命名列、形状和图片。</span><span class="sxs-lookup"><span data-stu-id="adb3e-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="adb3e-159">若要指示 **单元格** ER 组件必须填写的 Excel 命名对象，必须在 **单元格** 组件的 **Excel 范围** 属性中指定该对象的名称。</span><span class="sxs-lookup"><span data-stu-id="adb3e-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="adb3e-160">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **单元格** 组件的 **启用** 属性以指定是否必须在生成的文档中填写该对象：</span><span class="sxs-lookup"><span data-stu-id="adb3e-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="adb3e-161">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应对象。</span><span class="sxs-lookup"><span data-stu-id="adb3e-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="adb3e-162">此 **单元格** 组件的绑定指定放入相应对象中的值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="adb3e-163">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，将不在生成的文档中填写相应对象。</span><span class="sxs-lookup"><span data-stu-id="adb3e-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="adb3e-164">将配置 **单元格** 组件以在单元格中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="adb3e-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="adb3e-165">在此情况下，将在单元格中把该值作为相同数据类型的值输入。</span><span class="sxs-lookup"><span data-stu-id="adb3e-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="adb3e-166">配置 **单元格** 组件以在 Excel 形状中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="adb3e-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="adb3e-167">在此情况下，将在 Excel 形状中把该值作为该形状的文本输入。</span><span class="sxs-lookup"><span data-stu-id="adb3e-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="adb3e-168">对于非 **字符串** 事件类型的值，将自动转换为文本。</span><span class="sxs-lookup"><span data-stu-id="adb3e-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-169">可以配置 **单元格** 组件以仅在支持形状文本属性时填写形状。</span><span class="sxs-lookup"><span data-stu-id="adb3e-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="adb3e-170">配置 **单元格** 组件以在 Excel 图片中输入值时，可以与返回以二进制格式表示图像的 **容器** 数据类型的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="adb3e-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="adb3e-171">在这种情况下，值将作为图像输入到 Excel 图片中。</span><span class="sxs-lookup"><span data-stu-id="adb3e-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-172">将把每个 Excel 图片和形状视为通过其右上角锚定到特定 Excel 单元格或范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="adb3e-173">如果要复制 Excel 图片或形状，必须将锚定的单元格或范围配置为复制的单元格或范围。</span><span class="sxs-lookup"><span data-stu-id="adb3e-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="adb3e-174">若要详细了解如何嵌入图像和形状，请参阅[使用 ER 在生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="adb3e-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="adb3e-175">分页符组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-175">Page break component</span></span>

<span data-ttu-id="adb3e-176">**分页符** 组件强制 Excel 新分页。</span><span class="sxs-lookup"><span data-stu-id="adb3e-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="adb3e-177">如果希望使用 Excel 的默认分页，则无需此组件，但是如果希望 Excel 按照您的 ER 格式构造分页，应使用此组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="footer-component"></a><span data-ttu-id="adb3e-178">页脚组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-178">Footer component</span></span>

<span data-ttu-id="adb3e-179">**页脚** 组件用于在 Excel 工作簿中生成的工作表底部填充页脚。</span><span class="sxs-lookup"><span data-stu-id="adb3e-179">The **Footer** component is used to fill in footers at the bottom of a generated worksheet in an Excel workbook.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-180">您可以为每个 **工作表** 组件添加此组件，以在生成的 Excel 工作簿中为不同的工作表指定不同的页脚。</span><span class="sxs-lookup"><span data-stu-id="adb3e-180">You can add this component for every **Sheet** component to specify different footers for different worksheets in a generated Excel workbook.</span></span>

<span data-ttu-id="adb3e-181">配置单个 **页脚** 组件时，您可以使用 **页眉/页脚外观** 属性指定组件所用于的页面。</span><span class="sxs-lookup"><span data-stu-id="adb3e-181">When you configure an individual **Footer** component, you can use the **Header/footer appearance** property to specify the pages that the component is used for.</span></span> <span data-ttu-id="adb3e-182">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="adb3e-182">The following values are available:</span></span>

- <span data-ttu-id="adb3e-183">**任何** – 对父 Excel 工作表的任何页面运行配置的 **页脚** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-183">**Any** – Run the configured **Footer** component for any page of the parent Excel worksheet.</span></span>
- <span data-ttu-id="adb3e-184">**第一个** – 只对父 Excel 工作表的第一个页面运行配置的 **页脚** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-184">**First** – Run the configured **Footer** component for only the first page of the parent Excel worksheet.</span></span>
- <span data-ttu-id="adb3e-185">**偶数** – 只对父 Excel 工作表的偶数页面运行配置的 **页脚** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-185">**Even** – Run the configured **Footer** component for only the even pages of the parent Excel worksheet.</span></span>
- <span data-ttu-id="adb3e-186">**奇数** – 只对父 Excel 工作表的奇数页面运行配置的 **页脚** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-186">**Odd** – Run the configured **Footer** component for only the odd pages of the parent Excel worksheet.</span></span>

<span data-ttu-id="adb3e-187">对于单个 **工作表** 组件，您可以添加一些 **页脚** 组件，其中每个组件都具有不同的 **页眉/页脚外观** 属性值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-187">For a single **Sheet** component, you can add several **Footer** components, each of which has a different value for the **Header/footer appearance** property.</span></span> <span data-ttu-id="adb3e-188">这样，您可以为 Excel 工作表中的不同类型的页面生成不同的页脚。</span><span class="sxs-lookup"><span data-stu-id="adb3e-188">In this way, you can generate different footers for different type of pages in an Excel worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-189">确保添加到单个 **工作表** 组件的每个 **页脚** 组件都具有不同的 **页眉/页脚外观** 属性值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-189">Make sure that each **Footer** component that you add to a single **Sheet** component has a different value for the **Header/footer appearance** property.</span></span> <span data-ttu-id="adb3e-190">否则，会出现[验证错误](er-components-inspections.md#i16)。</span><span class="sxs-lookup"><span data-stu-id="adb3e-190">Otherwise, a [validation error](er-components-inspections.md#i16) occurs.</span></span> <span data-ttu-id="adb3e-191">您收到的错误消息会通知您有关不一致的情况。</span><span class="sxs-lookup"><span data-stu-id="adb3e-191">The error message that you receive notifies you about the inconsistency.</span></span>

<span data-ttu-id="adb3e-192">在添加的 **页脚** 组件下面，添加 **文本\\字符串**、**文本\\日期时间** 或其他类型的所需嵌套组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-192">Under the added **Footer** component, add the required nested components of the **Text\\String**, **Text\\DateTime**, or other type.</span></span> <span data-ttu-id="adb3e-193">配置这些组件的绑定，以指定页面页脚的填充方式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-193">Configure the bindings for those components to specify how your page footer is filled in.</span></span>

<span data-ttu-id="adb3e-194">您也可以使用特殊[格式代码](https://docs.microsoft.com/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers)正确格式化生成的页脚的内容。</span><span class="sxs-lookup"><span data-stu-id="adb3e-194">You can also use special [formatting codes](https://docs.microsoft.com/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) to correctly format the content of a generated footer.</span></span> <span data-ttu-id="adb3e-195">要了解如何使用此方法，请执行本主题后面的[示例 1](#example-1) 中的步骤。</span><span class="sxs-lookup"><span data-stu-id="adb3e-195">To learn how to use this approach, follow the steps in [Example 1](#example-1), later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-196">配置 ER 格式时，请务必考虑 Excel [限制](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3)，以及单个页眉或页脚的最大字符数。</span><span class="sxs-lookup"><span data-stu-id="adb3e-196">When you configure ER formats, be sure to consider the Excel [limit](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) and the maximum number of characters for a single header or footer.</span></span>

## <a name="header-component"></a><span data-ttu-id="adb3e-197">页眉组件</span><span class="sxs-lookup"><span data-stu-id="adb3e-197">Header component</span></span>

<span data-ttu-id="adb3e-198">**页眉** 组件用于在 Excel 工作簿中生成的工作表顶部填充页眉。</span><span class="sxs-lookup"><span data-stu-id="adb3e-198">The **Header** component is used to fill in headers at the top of a generated worksheet in an Excel workbook.</span></span> <span data-ttu-id="adb3e-199">其使用方式与 **页脚** 组件使用方式一样。</span><span class="sxs-lookup"><span data-stu-id="adb3e-199">It's used like the **Footer** component.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="adb3e-200">编辑添加的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="adb3e-200">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="adb3e-201">更新模板</span><span class="sxs-lookup"><span data-stu-id="adb3e-201">Update a template</span></span>

<span data-ttu-id="adb3e-202">可以选择操作窗格 **导入** 选项卡上的 **从 Excel 更新**，以将更新后的模板导入到可编辑的 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="adb3e-202">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="adb3e-203">在此过程中，将把所选 **Excel\\文件** 组件的模板替换为新模板。</span><span class="sxs-lookup"><span data-stu-id="adb3e-203">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="adb3e-204">将与更新后 ER 模板的内容同步可编辑 ER 格式的内容。</span><span class="sxs-lookup"><span data-stu-id="adb3e-204">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="adb3e-205">如果在可编辑格式中找不到 ER 格式组件，将为每个 Excel 名称自动创建一个新 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-205">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="adb3e-206">如果找不到合适的 Excel 名称，则会从可编辑的 ER 格式中删除每个 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-206">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="adb3e-207">如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="adb3e-207">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="adb3e-208">如果可编辑 ER 格式中最初包含 **工作表** 元素，建议在导入更新后的模板时，将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="adb3e-208">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="adb3e-209">否则，将从头开始创建原始 **工作表** 元素的所有嵌套元素。</span><span class="sxs-lookup"><span data-stu-id="adb3e-209">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="adb3e-210">因此，更新后的 ER 中将不包含重新创建的格式元素的所有绑定。</span><span class="sxs-lookup"><span data-stu-id="adb3e-210">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![在“从 Excel 更新”对话框中创建 Excel 工作表格式元素](./media/er-excel-format-update-template.png)

<span data-ttu-id="adb3e-212">若要详细了解此功能，请执行[通过重新应用 Excel 模板修改电子报告格式](modify-electronic-reporting-format-reapply-excel-template.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="adb3e-212">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="adb3e-213">验证 ER 格式</span><span class="sxs-lookup"><span data-stu-id="adb3e-213">Validate an ER format</span></span>

<span data-ttu-id="adb3e-214">验证可编辑的 ER 格式时，将执行一致性检查以确保当前所用 Excel 模板中包含 Excel 名称。</span><span class="sxs-lookup"><span data-stu-id="adb3e-214">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="adb3e-215">将通知您任何不一致。</span><span class="sxs-lookup"><span data-stu-id="adb3e-215">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="adb3e-216">将为某些不一致提供用于自动解决问题的选项。</span><span class="sxs-lookup"><span data-stu-id="adb3e-216">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![验证错误消息](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="adb3e-218">控制 Excel 公式的计算</span><span class="sxs-lookup"><span data-stu-id="adb3e-218">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="adb3e-219">如果生成的传出文档为 Microsoft Excel 工作簿格式，该文档的某些单元格中可能包含 Excel 公式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-219">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="adb3e-220">如果启用了 **支持在电子申报框架中使用 EPPlus 库** 功能，可以通过更改正在使用的 Excel 模板中的 **计算选项** 的[参数](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows)值来控制何时计算公式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-220">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="adb3e-221">如果选择 **自动**，则每次为生成的文档附加新的范围、单元格等时，都将重新计算所有依赖 公式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-221">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="adb3e-222">这可能会导致包含多个相关公式的 Excel 模板出现性能问题。</span><span class="sxs-lookup"><span data-stu-id="adb3e-222">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="adb3e-223">如果选择 **手动**，则可避免在生成文档时重新计算公式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-223">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="adb3e-224">使用 Excel 打开生成的文档进行预览时，将手动强制重新计算公式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-224">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="adb3e-225">如果配置的 ER 目标位置需要使用生成的文档，但 Excel 中无预览（PDF 转换、电子邮件等），请不要使用此选项，因为生成的文档中包含的公式中可能不包含值。</span><span class="sxs-lookup"><span data-stu-id="adb3e-225">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.) because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="example-1-format-footer-content"></a><a name="example-1"></a><span data-ttu-id="adb3e-226">示例 1：格式化页脚内容</span><span class="sxs-lookup"><span data-stu-id="adb3e-226">Example 1: Format footer content</span></span>

1. <span data-ttu-id="adb3e-227">使用提供的 ER 配置[生成](er-generate-printable-fti-forms.md)可打印的自由文本发票 (FTI) 文档。</span><span class="sxs-lookup"><span data-stu-id="adb3e-227">Use the provided ER configurations to [generate](er-generate-printable-fti-forms.md) a printable free text invoice (FTI) document.</span></span>
2. <span data-ttu-id="adb3e-228">查看生成的文档的页脚。</span><span class="sxs-lookup"><span data-stu-id="adb3e-228">Review the footer of the generated document.</span></span> <span data-ttu-id="adb3e-229">请注意，它包含有关文档中的当前页码和页面总数的信息。</span><span class="sxs-lookup"><span data-stu-id="adb3e-229">Notice that it contains information about the current page number and the total number of pages in the document.</span></span>

    ![查看以 Excel 格式生成的文档的页脚](./media/er-fillable-excel-footer-1.gif)

3. <span data-ttu-id="adb3e-231">在 ER 格式设计器中，[打开](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format)样本 ER 格式以供审核。</span><span class="sxs-lookup"><span data-stu-id="adb3e-231">In the ER format designer, [open](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) the sample ER format for review.</span></span>

    <span data-ttu-id="adb3e-232">**发票** 工作表的页脚是根据位于 **页脚** 组件下面的两个 **字符串** 组件的设置生成的：</span><span class="sxs-lookup"><span data-stu-id="adb3e-232">The footer of the **Invoice** worksheet is generated based on the settings of two **String** components that reside under the **Footer** component:</span></span>

    - <span data-ttu-id="adb3e-233">第一个 **字符串** 组件填写以下特殊格式代码以强制 Excel 应用特定格式：</span><span class="sxs-lookup"><span data-stu-id="adb3e-233">The first **String** component fills in the following special formatting codes to force Excel to apply specific formatting:</span></span>

        - <span data-ttu-id="adb3e-234">**&C** – 将页脚文本居中对齐。</span><span class="sxs-lookup"><span data-stu-id="adb3e-234">**&C** – Align the footer text in the center.</span></span>
        - <span data-ttu-id="adb3e-235">**&"Segoe UI,Regular"&8** – 以大小为 8 磅的 "Segoe UI Regular" 字体显示页脚文本。</span><span class="sxs-lookup"><span data-stu-id="adb3e-235">**&"Segoe UI,Regular"&8** – Present the footer text in the "Segoe UI Regular" font at a size of 8 points.</span></span>

    - <span data-ttu-id="adb3e-236">第二个 **字符串** 组件填充的文本包含当前文档中的当前页码和页面总数。</span><span class="sxs-lookup"><span data-stu-id="adb3e-236">The second **String** component fills in the text that contains the current page number and the total number of pages in the current document.</span></span>

    ![在“格式设计器”页面上查看页脚 ER 格式组件](./media/er-fillable-excel-footer-2.png)

4. <span data-ttu-id="adb3e-238">自定义示例 ER 格式以修改当前页面页脚：</span><span class="sxs-lookup"><span data-stu-id="adb3e-238">Customize the sample ER format to modify the current page footer:</span></span>

    1. <span data-ttu-id="adb3e-239">[创建](er-quick-start2-customize-report.md#DeriveProvidedFormat)派生的 **普通发票 (Excel) 自定义** ER 格式，此格式基于样本 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-239">[Create](er-quick-start2-customize-report.md#DeriveProvidedFormat) a derived **Free text invoice (Excel) custom** ER format that is based on the sample ER format.</span></span>
    2. <span data-ttu-id="adb3e-240">为 **发票** 工作表的 **页脚** 组件添加第一对新 **字符串** 组件：</span><span class="sxs-lookup"><span data-stu-id="adb3e-240">Add the first new pair of **String** components for the **Footer** component of the **Invoice** worksheet:</span></span>

        1. <span data-ttu-id="adb3e-241">添加一个 **字符串** 组件，使公司名称左对齐并以 8 磅的 "Segoe UI Regular" 字体(**"&L&"Segoe UI,Regular"&8"**) 显示。</span><span class="sxs-lookup"><span data-stu-id="adb3e-241">Add a **String** component that aligns the company name on the left and presents it in 8-point "Segoe UI Regular" font (**"&L&"Segoe UI,Regular"&8"**).</span></span>
        2. <span data-ttu-id="adb3e-242">添加一个填写公司名称的 **字符串** 组件 (**model.InvoiceBase.CompanyInfo.Name**)。</span><span class="sxs-lookup"><span data-stu-id="adb3e-242">Add a **String** component that fills in the company name (**model.InvoiceBase.CompanyInfo.Name**).</span></span>

    3. <span data-ttu-id="adb3e-243">为 **发票** 工作表的 **页脚** 组件添加第二对新 **字符串** 组件：</span><span class="sxs-lookup"><span data-stu-id="adb3e-243">Add the second new pair of **String** components for the **Footer** component of the **Invoice** worksheet:</span></span>

        1. <span data-ttu-id="adb3e-244">添加一个 **字符串** 组件，使处理日期右对齐并以 8 磅的 "Segoe UI Regular" 字体(**"&R&"Segoe UI,Regular"&8"**) 显示。</span><span class="sxs-lookup"><span data-stu-id="adb3e-244">Add a **String** component that aligns the processing date on the right and presents it in 8-point "Segoe UI Regular" font (**"&R&"Segoe UI,Regular"&8"**).</span></span>
        2. <span data-ttu-id="adb3e-245">添加一个以自定义格式 (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**) 填写处理日期的 **字符串** 组件。</span><span class="sxs-lookup"><span data-stu-id="adb3e-245">Add a **String** component that fills in the processing date in a custom format (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).</span></span>

        ![在“格式设计器”页面上查看页脚 ER 格式组件](./media/er-fillable-excel-footer-3.png)

    4. <span data-ttu-id="adb3e-247">[完成](er-quick-start2-customize-report.md#CompleteDerivedFormat)草稿版本的派生 **普通发票 (Excel) 自定义** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-247">[Complete](er-quick-start2-customize-report.md#CompleteDerivedFormat) the draft version of the derived **Free text invoice (Excel) custom** ER format.</span></span>

5. <span data-ttu-id="adb3e-248">[配置](er-generate-printable-fti-forms.md#configure-print-management)打印管理，以使用派生的 **普通发票 (Excel) 自定义** ER 格式，而不是示例 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="adb3e-248">[Configure](er-generate-printable-fti-forms.md#configure-print-management) Print management to use the derived **Free text invoice (Excel) custom** ER format instead of the sample ER format.</span></span>
6. <span data-ttu-id="adb3e-249">生成可打印的 FTI 文档，并查看生成的文档的页脚。</span><span class="sxs-lookup"><span data-stu-id="adb3e-249">Generate a printable FTI document, and review the footer of the generated document.</span></span>

    ![查看以 Excel 格式生成的文档的页脚](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a><span data-ttu-id="adb3e-251">其他资源</span><span class="sxs-lookup"><span data-stu-id="adb3e-251">Additional resources</span></span>

[<span data-ttu-id="adb3e-252">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="adb3e-252">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="adb3e-253">设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="adb3e-253">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="adb3e-254">通过重新应用 Excel 模板修改电子报告格式</span><span class="sxs-lookup"><span data-stu-id="adb3e-254">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="adb3e-255">使用可水平扩展的范围在 Excel 报表中动态添加列</span><span class="sxs-lookup"><span data-stu-id="adb3e-255">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="adb3e-256">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="adb3e-256">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="adb3e-257">配置电子申报 (ER) 以便将数据导入 Power BI</span><span class="sxs-lookup"><span data-stu-id="adb3e-257">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
