---
title: 电子申报公式支持的复合数据类型
description: 本主题提供有关电子申报 (ER) 公式支持的复合数据类型的信息。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ed9e62751b6be9fad6de3bf262d37d7977d192
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224078"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>电子申报公式支持的复合数据类型

[!include [banner](../includes/banner.md)]

本主题提供有关[电子申报 (ER)](general-electronic-reporting.md) 表达式支持的复合数据类型的信息。 复合数据类型包括[类](#class)、[容器](#container)、[记录](#record)、[记录列表](#record-list)和[对象](#object)。

## <a name="class"></a><a name="class"></a>分类

*类* 数据类型是指公共应用程序类。 在 ER 中，它表示为 [*记录*](#record)，其中包含引用类的每个公共方法的单独字段。 当参数化方法的调用时，还必须在配置为调用该方法的 ER 表达式中指定适当类型的所需参数。

在 ER [映射](general-electronic-reporting.md#data-model-and-model-mapping-components)和 [格式](general-electronic-reporting.md#FormatComponentOutbound)组件中，您可以添加表示为数据源并返回 *类* 类型的值的 **类** 数据源。 此数据源公开可在运行时调用的类的公共方法。

> [!NOTE]
> 只能从 ER 表达式调用返回值的方法。
>
> 只能从 ER 表达式调用参数范围为 0 到 8 的方法。

*类* 的默认值为 **null**。

下图显示了如何添加 **类** 类型的 **系统信息 (xInfo)** 数据源以创建 **(xInfo)** 应用程序类的实例并调用其 **productName()** 方法，从而接收当前应用程序的名称。 通过执行已为 ER 数据模型的 **软件名称 (SoftwareName)** 字段配置的 `xInfo.productName` 绑定，在运行时获取当前应用程序的名称。 此绑定调用在当前模型映射中表示为 **系统信息 (xInfo)** 数据源的 **xInfo** 应用程序类的 `productName()` 方法。

[![在 ER 模型映射设计器中配置类数据源](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

下图显示了如何配置 ER 格式以将提供的应用程序名称放入生成的单据中。 使用的数据模型的 **软件名称 (SoftwareName)** 字段已绑定到在 ER 格式的 **softwareUsed** XML 元素下嵌套的 **字符串** 组件。 因此，当前应用程序的名称在运行时放置到生成的 XML 格式单据的 **softwareUsed** XML 元素中。

[![在 ER 格式设计器中配置电子出库单据的结构](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>容器

*容器* 数据类型保存二进制内容。 *容器* 值可用于将特定信息从存储传递到生成的单据。 在 ER 框架中，此数据类型经常用于将媒体内容（例如公司徽标）放入生成的单据中。

> [!NOTE]
> 尽管每个媒体项都可以表示为 *容器* 值，但不是每个 *容器* 值都表示媒体项。 因此，如果您配置 ER 格式以使其使用 *容器* 将图像放入生成的单据中，但引用的 *容器* 不返回媒体内容，可能会引发类似于以下示例的异常：“执行代码时出错：二进制（对象），使用无效参数调用的方法 constructFromContainer。”

*容器* 的默认值为 **null**。

下图显示了如何将 *容器* 类型的 **位图（图像）** 字段绑定到 **销售发票** 模型映射中 **容器** 类型的数据模型 **徽标** 字段。 此绑定使公司徽标可用于专为 **销售发票** 根定义设计并在运行时使用此模型映射的任何 ER 格式。

[![在 ER 模型映射设计器中绑定容器类型的字段](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>录制

*记录* 是一系列命名字段，每个字段都与[原始](er-formula-supported-data-types-primitive.md)数据类型或复合数据类型的值关联。 通常，*记录* 用于表示记录列表的单个记录。 在这种情况下，每个项目都代表单独的字段、方法和关系。

*记录* 的默认值为 **空**。

> [!NOTE]
> 当获取空 *记录* 的字段值时，将返回适当数据类型的默认值。

可以使用以下函数获取 *记录*：

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

有关转换 *记录* 值的详细信息，请参阅[列表类别中的 ER 函数列表](er-functions-category-list.md)。

## <a name="record-list"></a><a name="record-list"></a>记录列表

*记录列表* 是 *记录* 类型的项目列表。 通常，*记录列表* 用于表示已从数据库表中提取的记录的列表。

默认情况下，*记录列表* 的记录按顺序访问。 若要访问特定记录，您可以使用 [INDEX](er-functions-list-index.md) 函数并指定 *整数* 索引。

*记录列表* 的默认值为 **空**。 您可以使用 [ISEMPTY](/er-functions-list-isempty.md) 函数评估 *记录列表* 是否为空。

> [!NOTE]
> 如果 *记录列表* 为空，在每次尝试在该列表中获取 *记录* 的字段值时都将在运行时引发异常。 若要了解如何帮助防止此类型的运行时异常，请参阅[空列表用例的注意事项](er-components-inspections.md#i9)。

可以使用以下函数启动 *记录列表*：

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

有关转换 *记录列表* 值的详细信息，请参阅[列表类别中的 ER 函数列表](er-functions-category-list.md)。 若要了解如何引入 *记录列表* 项目，使用应用程序数据填充它们，然后使用数据生成业务单据，请参阅[设计新 ER 解决方案以打印自定义报表](er-quick-start1-new-solution.md)。

## <a name="object"></a><a name="object"></a>对象

*对象* 是指 *类* 的有状态实例。 通常，*对象* 在源代码中启动。 然后，它将传递到 ER 模型映射，并提供执行上下文的详细信息。

*对象* 的默认值为 **null**。

下图显示如何添加 *对象* 类型的 **ReportDataContract** 数据源，以将生成的发票从源代码传递到 **项目发票** 模型映射。 例如，发票实例文本作为执行上下文的一部分传递。 通过执行为 ER 数据模型的 **注释** 字段配置的 `ReportDataContract.parmInvoiceInstanceText` 绑定，在运行时从源代码中获取此文本。 此绑定调用在当前模型映射中表示为 **ReportDataContract** 数据源的 **PSAProjInvoiceContract** 应用程序类的 `parmInvoiceInstanceText()` 方法。

[![在 ER 模型映射设计器中配置对象数据源](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

若要了解如何将执行上下文的详细信息从源代码传递到运行 ER 解决方案，请参阅[开发应用程序伪像以调用设计的报表](er-quick-start1-new-solution.md#DevelopCustomCode)。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子申报公式语言](er-formula-language.md)
- [支持的原始数据类型](er-formula-supported-data-types-primitive.md)
