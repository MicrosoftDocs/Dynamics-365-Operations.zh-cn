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
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="607b2-103">设计用于生成 Excel 格式文档的配置</span><span class="sxs-lookup"><span data-stu-id="607b2-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="607b2-104">可以设计一种[电子申报 (ER)](general-electronic-reporting.md) 格式配置，该配置中有一个 ER [格式组件](general-electronic-reporting.md#FormatComponentOutbound)可配置来生成 Microsoft Excel 工作簿格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="607b2-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="607b2-105">必须为此用途使用特定 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="607b2-106">若要了解此功能，请执行[设计用于生成 OPENXML 格式的报表的配置](tasks/er-design-reports-openxml-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="607b2-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="607b2-107">添加新的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="607b2-107">Add a new ER format</span></span>

<span data-ttu-id="607b2-108">添加新的 ER 格式配置以生成 Excel 工作簿格式的传出文档时，必须为格式的 **格式类型** 属性选择 **Excel** 值，或将 **格式类型** 属性保留为空。</span><span class="sxs-lookup"><span data-stu-id="607b2-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="607b2-109">如果选择 **Excel**，可以将格式配置为只能生成 Excel 格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="607b2-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="607b2-110">如果将属性保留为空，可以将格式配置为使用 ER 框架支持的任何格式生成传出文档。</span><span class="sxs-lookup"><span data-stu-id="607b2-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="607b2-111">若要配置此配置的 ER 格式组件，请在操作窗格上选择 **设计器**，然后打开要用于在 ER 操作设计器中进行编辑的 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![配置页面](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="607b2-113">Excel 文件组件</span><span class="sxs-lookup"><span data-stu-id="607b2-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="607b2-114">手动输入</span><span class="sxs-lookup"><span data-stu-id="607b2-114">Manual entry</span></span>

<span data-ttu-id="607b2-115">必须向配置的 ER 格式添加 **Excel\\文件** 组件，才能生成 Excel 格式的传出文档。</span><span class="sxs-lookup"><span data-stu-id="607b2-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\File 组件](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="607b2-117">若要指定传出文档的布局，请向 **Excel\\文件** 组件添加一个扩展名为 .xlsx 的 Excel 工作簿充当传出文档的模板。</span><span class="sxs-lookup"><span data-stu-id="607b2-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="607b2-118">手动附加模板时，必须使用已经在 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中为此目的配置的[文档类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)。</span><span class="sxs-lookup"><span data-stu-id="607b2-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![向“Excel\文件”组件添加附件](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="607b2-120">若要指定在运行配置的 ER 格式时如何填写附加的模板，必须向 **Excel\\文件** 组件添加嵌套的 **工作表**、**范围** 和 **单元格** 组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="607b2-121">每个嵌套组件必须与一个 Excel 命名项关联。</span><span class="sxs-lookup"><span data-stu-id="607b2-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="607b2-122">导入模板</span><span class="sxs-lookup"><span data-stu-id="607b2-122">Template import</span></span>

<span data-ttu-id="607b2-123">可以选择操作窗格 **导入** 选项卡上的 **从 Excel 导入**，以将新模板导入到空白 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="607b2-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="607b2-124">在此示例中，将自动创建一个 **Excel\\文件** 组件，并为其附加导入的模板。</span><span class="sxs-lookup"><span data-stu-id="607b2-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="607b2-125">还将根据发现的 Excel 命名项列表自动创建所有必需 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![选择“从 Excel 导入”](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="607b2-127">如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="607b2-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="607b2-128">工作表组件</span><span class="sxs-lookup"><span data-stu-id="607b2-128">Sheet component</span></span>

<span data-ttu-id="607b2-129">**工作表** 组件指示必须填写的 Excel 工作簿附件的工作表。</span><span class="sxs-lookup"><span data-stu-id="607b2-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="607b2-130">Excel 模板中的工作表的名称在此组件的 **工作表** 属性中定义。</span><span class="sxs-lookup"><span data-stu-id="607b2-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="607b2-131">此组件对其中包含单个工作表的 Excel 工作簿可选。</span><span class="sxs-lookup"><span data-stu-id="607b2-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="607b2-132">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **工作表** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：</span><span class="sxs-lookup"><span data-stu-id="607b2-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="607b2-133">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将把适当的工作表放入生成的文档中。</span><span class="sxs-lookup"><span data-stu-id="607b2-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="607b2-134">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，生成的文档中将不包含工作表。</span><span class="sxs-lookup"><span data-stu-id="607b2-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![工作表组件的示例](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="607b2-136">范围组件</span><span class="sxs-lookup"><span data-stu-id="607b2-136">Range component</span></span>

<span data-ttu-id="607b2-137">**范围** 组件指示此 ER 组件必须控制的 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="607b2-138">范围的名称在此组件的 **Excel 范围** 属性中定义。</span><span class="sxs-lookup"><span data-stu-id="607b2-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="607b2-139">**复制方向** 属性指定是否在生成的文档中重复范围和如何重复范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="607b2-140">如果 **复制方向** 属性设置为 **不复制**，生成的文档中将不重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="607b2-141">如果 **复制方向** 属性设置为 **垂直**，生成的文档中将重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="607b2-142">将把复制的每个范围放到 Excel 模板中原始范围下。</span><span class="sxs-lookup"><span data-stu-id="607b2-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="607b2-143">复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。</span><span class="sxs-lookup"><span data-stu-id="607b2-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="607b2-144">如果 **复制方向** 属性设置为 **水平**，生成的文档中将重复相应 Excel 范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="607b2-145">将把复制的每个范围放到 Excel 模板中原始范围右侧。</span><span class="sxs-lookup"><span data-stu-id="607b2-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="607b2-146">复制数量由与此 ER 组件绑定的 **记录列表** 类型的数据源中的记录数量定义。</span><span class="sxs-lookup"><span data-stu-id="607b2-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="607b2-147">若要详细了解水平复制，请执行[使用可水平扩展的范围在 Excel 报表中动态添加列](tasks/er-horizontal-1.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="607b2-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="607b2-148">**范围** 组件可以有其他嵌套 ER 组件，用于在相应 Excel 命名范围中输入值。</span><span class="sxs-lookup"><span data-stu-id="607b2-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="607b2-149">如果使用 **文本** 组的任何组件输入值，将把该值在 Excel 范围中作为文本值输入。</span><span class="sxs-lookup"><span data-stu-id="607b2-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="607b2-150">使用此模式根据应用程序中定义的语言环境为输入的值设置格式。</span><span class="sxs-lookup"><span data-stu-id="607b2-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="607b2-151">如果使用  **Excel** 组的 **单元格** 组件输入值，该值将在 Excel 范围中作为该 **单元格** 组件的绑定定义的数据类型（如 **字符串**、**实数** 或 **整数**）的值。</span><span class="sxs-lookup"><span data-stu-id="607b2-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="607b2-152">使用此模式让 Excel 应用程序根据打开传出文档的本地计算机的区域设置来为输入的值设置格式。</span><span class="sxs-lookup"><span data-stu-id="607b2-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="607b2-153">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **范围** 组件的 **启用** 属性以指定是否必须将组件放入生成的文档中：</span><span class="sxs-lookup"><span data-stu-id="607b2-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="607b2-154">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="607b2-155">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，将不在生成的文档中填写相应范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="607b2-156">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，并且此范围不表示整行或整列，生成的文档中将包含这些行和列，但显示为隐藏行和隐藏列。</span><span class="sxs-lookup"><span data-stu-id="607b2-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="607b2-157">单元格组件</span><span class="sxs-lookup"><span data-stu-id="607b2-157">Cell component</span></span>

<span data-ttu-id="607b2-158">**单元格** 组件用于填写 Excel 命名列、形状和图片。</span><span class="sxs-lookup"><span data-stu-id="607b2-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="607b2-159">若要指示 **单元格** ER 组件必须填写的 Excel 命名对象，必须在 **单元格** 组件的 **Excel 范围** 属性中指定该对象的名称。</span><span class="sxs-lookup"><span data-stu-id="607b2-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="607b2-160">在 ER 操作设计器的 **映射** 选项卡上，可以配置 **单元格** 组件的 **启用** 属性以指定是否必须在生成的文档中填写该对象：</span><span class="sxs-lookup"><span data-stu-id="607b2-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="607b2-161">如果将 **启用** 属性的表达式配置为在运行时返回 **True**，或者如果根本不配置任何表达式，将在生成的文档中填写相应对象。</span><span class="sxs-lookup"><span data-stu-id="607b2-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="607b2-162">此 **单元格** 组件的绑定指定放入相应对象中的值。</span><span class="sxs-lookup"><span data-stu-id="607b2-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="607b2-163">如果将 **启用** 属性的表达式配置为在运行时返回 **False**，将不在生成的文档中填写相应对象。</span><span class="sxs-lookup"><span data-stu-id="607b2-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="607b2-164">将配置 **单元格** 组件以在单元格中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="607b2-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="607b2-165">在此情况下，将在单元格中把该值作为相同数据类型的值输入。</span><span class="sxs-lookup"><span data-stu-id="607b2-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="607b2-166">配置 **单元格** 组件以在 Excel 形状中输入值时，可以与返回原始数据类型（如 **字符串**、**实数** 或 **整数**）的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="607b2-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="607b2-167">在此情况下，将在 Excel 形状中把该值作为该形状的文本输入。</span><span class="sxs-lookup"><span data-stu-id="607b2-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="607b2-168">对于非 **字符串** 事件类型的值，将自动转换为文本。</span><span class="sxs-lookup"><span data-stu-id="607b2-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="607b2-169">可以配置 **单元格** 组件以仅在支持形状文本属性时填写形状。</span><span class="sxs-lookup"><span data-stu-id="607b2-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="607b2-170">配置 **单元格** 组件以在 Excel 图片中输入值时，可以与返回以二进制格式表示图像的 **容器** 数据类型的值的数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="607b2-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="607b2-171">在这种情况下，值将作为图像输入到 Excel 图片中。</span><span class="sxs-lookup"><span data-stu-id="607b2-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="607b2-172">将把每个 Excel 图片和形状视为通过其右上角锚定到特定 Excel 单元格或范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="607b2-173">如果要复制 Excel 图片或形状，必须将锚定的单元格或范围配置为复制的单元格或范围。</span><span class="sxs-lookup"><span data-stu-id="607b2-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="607b2-174">若要详细了解如何嵌入图像和形状，请参阅[使用 ER 在生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="607b2-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="607b2-175">分页符组件</span><span class="sxs-lookup"><span data-stu-id="607b2-175">Page break component</span></span>

<span data-ttu-id="607b2-176">**分页符** 组件强制 Excel 新分页。</span><span class="sxs-lookup"><span data-stu-id="607b2-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="607b2-177">如果希望使用 Excel 的默认分页，则无需此组件，但是如果希望 Excel 按照您的 ER 格式构造分页，应使用此组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="607b2-178">编辑添加的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="607b2-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="607b2-179">更新模板</span><span class="sxs-lookup"><span data-stu-id="607b2-179">Update a template</span></span>

<span data-ttu-id="607b2-180">可以选择操作窗格 **导入** 选项卡上的 **从 Excel 更新**，以将更新后的模板导入到可编辑的 ER 格式中。</span><span class="sxs-lookup"><span data-stu-id="607b2-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="607b2-181">在此过程中，将把所选 **Excel\\文件** 组件的模板替换为新模板。</span><span class="sxs-lookup"><span data-stu-id="607b2-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="607b2-182">将与更新后 ER 模板的内容同步可编辑 ER 格式的内容。</span><span class="sxs-lookup"><span data-stu-id="607b2-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="607b2-183">如果在可编辑格式中找不到 ER 格式组件，将为每个 Excel 名称自动创建一个新 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="607b2-184">如果找不到合适的 Excel 名称，则会从可编辑的 ER 格式中删除每个 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="607b2-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="607b2-185">如果要创建可编辑 ER 格式的可选 **工作表** 元素，请将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="607b2-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="607b2-186">如果可编辑 ER 格式中最初包含 **工作表** 元素，建议在导入更新后的模板时，将 **创建 Excel 工作表格式元素** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="607b2-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="607b2-187">否则，将从头开始创建原始 **工作表** 元素的所有嵌套元素。</span><span class="sxs-lookup"><span data-stu-id="607b2-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="607b2-188">因此，更新后的 ER 中将不包含重新创建的格式元素的所有绑定。</span><span class="sxs-lookup"><span data-stu-id="607b2-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![在“从 Excel 更新”对话框中创建 Excel 工作表格式元素](./media/er-excel-format-update-template.png)

<span data-ttu-id="607b2-190">若要详细了解此功能，请执行[通过重新应用 Excel 模板修改电子报告格式](modify-electronic-reporting-format-reapply-excel-template.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="607b2-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="607b2-191">验证 ER 格式</span><span class="sxs-lookup"><span data-stu-id="607b2-191">Validate an ER format</span></span>

<span data-ttu-id="607b2-192">验证可编辑的 ER 格式时，将执行一致性检查以确保当前所用 Excel 模板中包含 Excel 名称。</span><span class="sxs-lookup"><span data-stu-id="607b2-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="607b2-193">将通知您任何不一致。</span><span class="sxs-lookup"><span data-stu-id="607b2-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="607b2-194">将为某些不一致提供用于自动解决问题的选项。</span><span class="sxs-lookup"><span data-stu-id="607b2-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![验证错误消息](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="607b2-196">控制 Excel 公式的计算</span><span class="sxs-lookup"><span data-stu-id="607b2-196">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="607b2-197">如果生成的传出文档为 Microsoft Excel 工作簿格式，该文档的某些单元格中可能包含 Excel 公式。</span><span class="sxs-lookup"><span data-stu-id="607b2-197">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="607b2-198">如果启用了 **支持在电子申报框架中使用 EPPlus 库** 功能，可以通过更改正在使用的 Excel 模板中的 **计算选项** 的[参数](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows)值来控制何时计算公式。</span><span class="sxs-lookup"><span data-stu-id="607b2-198">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="607b2-199">如果选择 **自动**，则每次为生成的文档附加新的范围、单元格等时，都将重新计算所有依赖 公式。</span><span class="sxs-lookup"><span data-stu-id="607b2-199">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="607b2-200">这可能会导致包含多个相关公式的 Excel 模板出现性能问题。</span><span class="sxs-lookup"><span data-stu-id="607b2-200">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="607b2-201">如果选择 **手动**，则可避免在生成文档时重新计算公式。</span><span class="sxs-lookup"><span data-stu-id="607b2-201">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="607b2-202">使用 Excel 打开生成的文档进行预览时，将手动强制重新计算公式。</span><span class="sxs-lookup"><span data-stu-id="607b2-202">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="607b2-203">如果配置的 ER 目标位置需要使用生成的文档，但 Excel 中无预览（PDF 转换、电子邮件等），请不要使用此选项，因为生成的文档中包含的公式中可能不包含值。</span><span class="sxs-lookup"><span data-stu-id="607b2-203">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.)because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="607b2-204">其他资源</span><span class="sxs-lookup"><span data-stu-id="607b2-204">Additional resources</span></span>

[<span data-ttu-id="607b2-205">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="607b2-205">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="607b2-206">设计以 OPENXML 格式生成报表的配置</span><span class="sxs-lookup"><span data-stu-id="607b2-206">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="607b2-207">通过重新应用 Excel 模板修改电子报告格式</span><span class="sxs-lookup"><span data-stu-id="607b2-207">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="607b2-208">使用可水平扩展的范围在 Excel 报表中动态添加列</span><span class="sxs-lookup"><span data-stu-id="607b2-208">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="607b2-209">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="607b2-209">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="607b2-210">配置电子申报 (ER) 以便将数据导入 Power BI</span><span class="sxs-lookup"><span data-stu-id="607b2-210">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
