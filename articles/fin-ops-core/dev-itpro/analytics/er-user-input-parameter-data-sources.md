---
title: 使用用户输入参数数据源指定报表的参数
description: 本主题说明如何使用用户输入参数数据源为您生成的报表指定参数。
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 4e431c9dd59080af17fa073547073037ba233288
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782307"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>使用用户输入参数数据源指定报表的参数

[!include[banner](../includes/banner.md)]

当您设计 [电子报告](general-electronic-reporting.md) (ER) [模型映射](er-overview-components.md#model-mapping-component)和 ER [格式](er-overview-components.md#format-component)组件时，您可以使用 *用户输入参数* 类型的数据源，以获取可在运行时在对话框数据输入字段中指定的必需值，然后开始执行 ER 格式。 本主题介绍了当前支持的 *用户输入参数* 数据源。

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>必需属性

必须为每个 *用户输入参数* 类型的数据源指定以下属性：

- 在 **名称** 字段中，输入数据源的内部名称。 您可以在配置的模型映射或格式组件的其他[表达式](er-formula-language.md)和绑定中使用此名称。

## <a name="optional-properties"></a><a name="optional-properties"></a>可选属性

（可选）可以为 *用户输入参数* 类型的数据源指定以下属性：

- 在 **标签** 字段中，指定运行时用于对话框中相关数据输入字段的标签。 您可以通过激活 **标签** 字段，然后选择 **翻译**，为不同的语言代码添加不同的标签文本。
- 在 **帮助** 字段中，如果选择了 **用户输入参数** 类型的可编辑数据源，则指定设计时在 **格式设计器** 页面或 *模型映射设计器* 页面底部显示的帮助文本。 此文本可能会提供有关数据源的其他详细信息，以帮助用户配置可编辑格式或模型映射组件。 您可以通过选择 **翻译** 为不同的语言代码添加不同的帮助文本。

    > [!NOTE]
    > **翻译** 按钮可用于添加[特定于语言的标签和文本](er-design-multilingual-reports.md#format-component)，只有在添加数据源、保存更改 ，然后重新打开要编辑的数据源后才可使用此按钮。

- 在 **只读** 字段中，配置一个返回 *[布尔值](er-formula-supported-data-types-primitive.md#boolean)* 的表达式。

    - 如果配置的表达式在运行时返回 **True** 值，则相关数据输入字段在对话框中显示为灰色，并且您无法更改其值。
    - 如果配置的表达式在运行时返回 **False** 值，或者未配置表达式，则相关数据输入字段在对话框中可用，并且您无法更改其值。

- 在 **默认值** 字段中，配置返回所引用参数类型的值的表达式。 此值可用于在运行时填写对话框中的相关数据输入字段的默认值。

    当您运行 ER 格式时，运行时在对话框的相关数据输入字段中输入的值将作为先前使用的值保存在内存中。 分别为每个字段、运行的 ER 格式、当前用户和当前组织（公司）保存了以前使用的值。

    - 如果 **默认值** 表达式返回的值应始终用作默认值，那么无论以前使用的值如何，请将 **始终重置为默认值** 选项设置为 **是**。
    - 如果仅在缺少以前使用的值时才应将 **默认值** 表达式值返回的值用作默认值，请将 **始终重置为默认值** 选项设置为 **是**。

    > [!NOTE]
    > 如果将 **始终重置为默认值** 选项设置为 **是**，则必须在 **默认值** 字段中配置表达式。

- 如果将 **允许多选** 选项设置为 **是**，则可以在运行时为配置的参数选择多个值。 如果将其设置为 **否**，则只能选择一个值。

    > [!NOTE]
    > 此选项不适用于所有 *用户输入参数* 类型。 在设计时，会引发异常以通知用户配置的用户输入参数不支持多选，并且只能选择或输入一个值。
    >
    > 如果将 **允许多选** 选项设置为 **是**，并且您在 **默认值** 字段中指定了一个表达式，则该表达式只能用于设置一个默认值。

- 选择 **编辑可见性** 选项以指定是否应在运行时将配置的参数显示在对话框中。

    > [!NOTE]
    > *用户输入参数* 类型的数据源的默认可见性取决于保存它们的 ER 组件。
    >
    > - 如果在格式组件中配置了数据源，则默认情况下该数据源可见。
    > - 如果在模型映射组件中配置了数据源，则仅当运行 ER 组件时数据源的值影响结果的情况下，此数据源才可见。 例如，您添加了一个数据源，但没有在当前模型映射组件的表达式和绑定中使用它。 在这种情况下，运行时相关数据输入字段默认不会显示在对话框中。 

    在 **公式设计器** 页面上的 **公式** 字段中，配置一个返回 *布尔值* 的表达式。

    - 如果配置的表达式在运行时返回 **True** 值，或者未配置表达式，则运行时相关数据输入字段在对话框中可见。
    - 如果配置的表达式返回 **False** 值，则运行时对话框中将隐藏相关数据输入字段。 当它在运行时被其他表达式调用时，它会根据其他设置返回默认值、先前使用的值或当前数据类型值的默认值。

## <a name="type-specific-properties"></a>特定于类型的属性

### <a name="application-dependent-user-input-parameter"></a>应用相关的用户输入参数

使用 **常规** \> **用户输入参数** 类型的数据源，以获取为 Microsoft Dynamics 365 Finance 应用程序的当前实例指定的数据类型的一个或多个必需值。 当您将此类型的数据源添加到 ER 组件时，请指定以下属性：

- 在 **Operations 数据类型名称(EDT，枚举)** 字段中，选择应用程序[扩展数据类型 (EDT)](../extensibility/extensible-edts.md) 或应用程序枚举。

> [!NOTE]
> 建议您查看在此 **用户输入参数** 类型的可编辑数据源中更改 **Operations 数据类型名称(EDT，枚举)** 引用时在 **只读** 和 *默认值* 字段中配置的表达式。

下图显示了在 **Instat XML (DE)** ER 格式配置中配置的 `$TaxRegNum` 数据源的属性。 此数据源配置为使用 *说明* EDT 在运行时在对话框中提供 **税务登记编号** 数据输入字段。

![“格式设计器”页面对话框中用户输入参数类型的数据源的属性。](./media/er-user-input-parameter-data-sources-01.png)

下图显示了运行 **Instat XML (DE)** ER 格式配置以[生成](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md)内部统计声明时，在运行时显示的对话框。 请注意，已配置的 **税务登记编号** 字段可用于数据输入。

![“内部统计”页面上正在运行的 ER 格式的“内部统计报表”对话框。](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>数据模型枚举用户输入参数

使用 **数据模型**\> **枚举用户输入参数** 类型的数据源，以获取单个数据模型[枚举](er-formula-supported-data-types-primitive.md#enumeration)所需的一个或多个值。 当您将此类型的数据源添加到 ER 组件时，请指定以下属性：

- 在 **模型** 字段中，指定对基础数据模型的引用。
- 在 **模型枚举** 字段中，指定对引用的数据模型枚举的引用。
- 在 **版本** 字段中，选择包含引用模型枚举的 ER 数据模型组件的修订编号。

    > [!TIP]
    > 在设计时，您可以将 **版本** 字段留空，以访问位于相应 ER 数据模型配置草稿版本中的引用数据模型组件的枚举列表。 这样，您可以同时编辑模型映射或格式组件的草稿版本，以及基础数据模型组件的草稿版本。
    >
    > 但是，请注意，**版本** 字段只能在模型映射或格式组件的草稿版本中留空。 当您将 ER 模型映射或格式配置的状态从 **草稿** 更改为 **已完成** 时，此字段将自动填写当前 Finance 实例中可用的最高模型修订编号。 如果您在基础数据模型的草稿版本中引入新枚举或新枚举值，并在可编辑模型映射或格式组件中引用它，请在您的 ER 模型映射或格式配置的草稿版本完成之前，完成基础数据模型配置的草稿版本。 否则，当您将模型映射或格式配置的状态从 **草稿** 更改为 **已完成** 时，将引发“找不到路径”异常。 该消息将通知您基本数据模型中缺少引用的枚举或枚举值。

下图显示了在 **Instat XML (DE) Contoso** ER 格式配置中配置的 `$ReportDirection` 数据源的属性。 已从 **Instat XML (DE)** 配置中 [派生](general-electronic-reporting.md#Configuration) **Instat XML (DE) Contoso** 配置。 此数据源配置为使用 *ReportDirection* 模型枚举在运行时在对话框中提供适当的查找字段。

![“格式设计器”页面对话框中用户输入参数类型的数据源的属性。](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>格式枚举用户输入参数

使用 **格式枚举** \> **枚举用户输入参数** 类型的数据源，以获取单个格式枚举所需的一个或多个值。 当您将此类型的数据源添加到 ER 组件时，请指定以下属性：

- 在 **格式枚举** 字段中，指定可编辑格式的枚举。

> [!NOTE]
> 这种类型的数据源只能在可编辑格式组件的范围内进行配置。

## <a name="additional-resources"></a>其他资源

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[从源代码启动 USER INPUT PARAMETER 类型的数据源值](er-initiate-uip-data-source-value-from-source-code.md)
