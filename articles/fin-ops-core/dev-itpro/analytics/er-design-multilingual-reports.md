---
title: 在电子报告中设计多语言报告
description: 本主题说明如何使用电子报告 (ER) 标签来设计和生成多语言报告。
author: NickSelin
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65efb8dbec925b5238acaa5d6769f3085e9715b9
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2020
ms.locfileid: "3444613"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>在电子报告中设计多语言报告

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>概览

作为业务用户，您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架根据各个国家或地区的法律要求配置必须生成的传出文档的格式。 当这些要求需要针对不同国家或地区以不同语言生成传出文档时，您可以配置一个包含语言相关资源的 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)。 这样，您可以重用此格式来生成各个国家或地区的传出文档。 您可能还希望使用一个 ER 格式为相应的客户、供应商、子公司或任何其他方生成不同语言的传出文档。

您可以将 ER 数据模型和模型映射配置为已配置的 ER 格式的数据源，来定义指定将哪些应用程序数据放入生成的文档的数据流。 作为 ER 配置[提供者](general-electronic-reporting.md#Provider)，您可以[发布](tasks/er-upload-configuration-into-lifecycle-services.md#upload-configuration-into-lcs)配置的[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)、[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)和[格式](general-electronic-reporting.md#FormatComponentOutbound)作为 ER 解决方案的组成部分，来生成特定的传出文档。 您还可以允许客户[上载](general-electronic-reporting-manage-configuration-lifecycle.md)已发布的 ER 解决方案，以便可以使用和定制该解决方案。 如果您希望客户讲其他语言，则可以配置 ER 组件，使其包含语言相关资源。 以此方式，可在设计时以客户的用户首选语言呈现可编辑 ER 组件的内容。

您可以将语言相关资源配置为 ER 标签。 然后，可以使用这些标签来配置 ER 组件以用于以下目的：

- 在设计时：

    - 以用户首选语言呈现已配置的 ER 组件的内容。

- 在运行时：

    - 为传出文档生成语言相关内容。
    - 以用户首选语言提供警告和错误消息。
    - 以用户首选语言提示必填字段。

可以在包含不同组件的每个 ER [配置](general-electronic-reporting.md#Configuration)中配置 ER 标签。 可以独立于 ER 数据模型、ER 模型映射和 ER 格式组件的已配置逻辑来维护标签。

每个 ER 标签由一个 ID 标识，该 ID 在保留该标签的 ER 配置范围内是唯一的。 每个标签可以包含 Microsoft Dynamics 365 Finance 的当前实例中支持的每种语言的标签文本。 这些受支持的语言包括已部署的自定义项的语言。

## <a name="entry"></a>条目

在设计 ER 数据模型、ER 模型映射或 ER 格式时，每当您选择一个可能包含可翻译上下文的字段时，就会显示**翻译**选项。 选择此选项时，可以将所选字段链接到**文本翻译**<a name="TextTranslationPane">窗格</a>上的 ER 标签。 您可以选择现有 ER 标签，也可以添加新 ER 标签（如果尚不可用）。 选择或添加 ER 标签时，可以为当前 Finance 实例支持的每种语言添加相关文本。

下图显示了如何在可编辑 ER 数据模型中完成此翻译。 在此示例中，可编辑**发票模型**的 **PurchaseOrder** 字段的**描述**属性被翻译为奥地利德语 (DE-AT) 和日语 (JA) 语言。

![在 ER 数据模型设计器中提供 ER 标签的翻译](./media/er-multilingual-labels-refer.png)

只能翻译位于可编辑 ER 组件中的标签的标签文本。 例如，如果为 ER 模型映射数据源的标签属性选择**翻译**，然后选择位于父 ER 数据模型中的 ER 标签，则会看到标签的内容，但是无法更改。 在这些情况下，**已翻译的文本**字段不可用，如下图所示。

![在 ER 模型映射设计器中查看提供的 ER 标签的翻译](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> 您无法使用设计器删除已在可编辑 ER 组件中输入的标签。

## <a name="scope"></a>作用域

ER 标签可以在 ER 组件的几个可翻译属性中引用。

### <a name="data-model-component"></a>数据模型组件

配置 ER 数据模型时，可以为其添加 ER 标签。 可以将模型项目的**标签**和**描述**属性、每个模型的字段以及每个<a id="LinkModelEnum"></a>模型枚举值链接到一个已添加到 ER 数据模型中的 ER 标签。

![在 ER 数据模型设计器中为描述属性提供翻译](./media/er-multilingual-labels-refer.png)

当以这种方式配置 ER 数据模型时，其内容将以每个用户的首选语言呈现给 ER 数据模型设计器的用户。 因此，简化了模型维护。 下图说明了将 DE-AT 和 JA 设置为首选语言的用户如何使用此功能。

![将 DE-AT 设置为首选语言的用户的 ER 数据模型设计器的布局](./media/er-multilingual-labels-refer-de.png)

![将 JA 设置为首选语言的用户的 ER 数据模型设计器的布局](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>模型映射组件

因为 ER 模型映射基于 ER 数据模型，所以所引用的数据模型元素的标签在模型映射设计器中以用户的首选语言显示。 下图显示了如何通过使用已添加到已配置数据模型中的**描述**属性的标签，在可编辑模型映射中解释 **PurchaseOrder** 字段的含义。 请注意，此标签以用户的首选语言（在此示例中为 DE-AT）呈现。

![将 DE-AT 设置为首选语言的用户的 ER 模型映射设计器的布局](./media/er-multilingual-labels-show-mapping.png)

当将**用户输入参数**数据源的**标签**属性配置为链接到 ER 标签时，与此数据源对应的参数字段将在运行时在用户对话框中以用户首选语言呈现给用户。

### <a name="format-component"></a>格式组件

配置 ER 格式时，可以为其添加 ER 标签。 可以将每个已配置数据源的**标签**和**帮助文本**属性链接到添加到 ER 格式的 ER 标签。 每个<a id="LinkFormatEnum"></a>格式枚举值的**标签**和**描述**属性也可以链接到可从可编辑 ER 格式访问的 ER 标签。

> [!NOTE]
> 您还可以将这些属性链接到父 ER 数据模型的一个 ER 标签，该标签可以重用为此 ER 数据模型配置的每种 ER 格式的模型标签。

当以这种方式配置 ER 格式时，格式的内容将以每个用户的首选语言呈现给 ER 操作设计器的用户。 因此，简化了配置逻辑的格式维护和分析。

因为 ER 格式基于 ER 数据模型，所以将在 ER 格式设计器中以用户首选语言呈现数据模型元素中引用的标签。

当将**用户输入参数**数据源的**标签**属性配置为链接到 ER 标签时，在运行时与用户对话框中的参数相对应的字段将作为提示呈现给用户。 下图显示了如何在设计时将**用户输入参数**数据源的**标签**属性链接到 ER 标签，以便在运行时以不同的用户首选语言向用户提示参数（为美国英语 (EN-US) 和 DE-AT 语言显示）。

![在 ER 操作设计器中提供用户输入参数的属性的翻译](./media/er-multilingual-labels-refer-format.png)

![运行时 EN-US 用户首选语言的 ER 供应商付款处理](./media/er-multilingual-labels-show-runtime-en.png)

![运行时 DE-AT 用户首选语言的 ER 供应商付款处理](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>表达式

要在 ER [表达式](er-formula-language.md)中使用标签，必须使用语法 **@"GER\_LABEL:X"**，其中前缀 **@** 表示操作数引用标签，**GER\_LABEL** 表示引入了 ER 标签，**X** 是 ER 标签 ID。

![在 ER 公式设计器中配置包含对 ER 标签的引用的 ER 表达式](./media/er-multilingual-labels-expression1.png)

要引用系统（应用程序）标签，请使用语法 **@"X"**，其中前缀 **@** 表示操作数引用标签，**X** 是系统标签 ID。

![在 ER 公式设计器中配置包含对应用程序标签的引用的 ER 表达式](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>模型映射

可以使用标签来配置 ER 模型映射的表达式。 当运行来生成传出文档的 ER 格式调用此映射时，执行的上下文将包括语言代码。 配置的表达式标签将使用为该上下文的语言配置的标签文本填充。

如果引用的标签没有对调用模型映射的格式执行上下文的语言的翻译，将改用 EN-US 语言的标签文本。

#### <a name="format"></a>格式

可以使用标签来配置 ER 格式的 ER 表达式。 当运行此格式来生成传出文档时，执行的上下文将包括语言代码。 配置的表达式标签将使用为该上下文的语言配置的标签文本填充。

![在 ER 公式设计器中提供可编辑 ER 表达式的 ER 标签的翻译](./media/er-multilingual-labels-refer-in-expression.png)

![在 ER 操作设计器中引用 ER 标签的数据绑定的示例](./media/er-multilingual-labels-refer-in-binding.png)

您可以配置 ER 格式的**文件**组件来以用户的首选语言生成报告。

![在 ER 操作设计器中设置 FILE 组件来以用户首选语言生成报告](./media/er-multilingual-labels-language-context-user.png)

如果以这种方式配置 ER 格式，将使用 ER 标签的相应文本生成报告。 下图显示了 EN-US 和 DE-AT 用户语言的报告示例。

![以 EN-US 用户首选语言生成的报告的预览](./media/er-multilingual-labels-report-preview-en.png)

![以 DE-AT 用户首选语言生成的报告的预览](./media/er-multilingual-labels-report-preview-de.png)

如果引用的标签没有对格式执行上下文的语言的翻译，将改用 EN-US 语言的标签文本。

## <a name="language"></a>语言

ER 支持多种为生成的报告指定语言的方式。 在**格式**选项卡上的**语言首选项**字段中，您可以选择以下值：

- **公司首选项** – 使用公司指定的语言生成报告。

    ![在 ER 操作设计器中指定公司首选语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-company.png)

- **用户首选项** – 使用用户首选语言生成报告。
- **明确定义** – 使用在设计时指定的语言生成报告。

    ![在 ER 操作设计器中指定设计时定义的语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-fixed.png)

- **运行时定义** – 使用在运行时指定的语言生成报告。 如果选择此值，请在**语言**字段中配置返回语言的语言代码的 ER 表达式，如相应客户的语言。

    ![在 ER 操作设计器中指定运行时定义的语言作为生成的报告的语言](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a>译文

您可以将所需的 ER 标签添加到可编辑 ER 组件中。 添加 ER 标签后，可以通过两种方式进行翻译：手动和自动。

### <a name="manual-translation"></a>手动翻译

在**文本翻译**[窗格](#TextTranslationPane)上添加 ER 标签时，可以将其手动翻译为当前 Finance 实例支持的所有语言。 您可以在**系统语言**或**用户语言**部分的**语言**字段中选择首选语言，并在相应的**已翻译的文本**字段中输入适当的文本，然后选择**翻译**。 对于每种必需的语言和添加的每个标签，必须重复此流程。

### <a name="automatic-translation"></a>自动翻译

ER 组件的配置是在可编辑 ER 组件所在的 ER 配置的草稿版本中完成的。

![提供对“草稿”状态下的配置版本的访问的 ER 配置页面](./media/er-multilingual-labels-configurations.png)

如本主题前面所述，您可以将所需的 ER 标签添加到可编辑 ER 组件中。 这样，您可以用 EN-US 语言指定 ER 标签的文本。 然后，您可以使用内置的 ER 函数导出 ER 组件的标签。 选择包含可编辑的 ER 组件的 ER 配置的草稿版本，然后选择**交换 \> 导出标签**。

![允许从选定的配置版本导出 ER 标签的 ER 配置页面](./media/er-multilingual-labels-export.png)

您可以导出所有标签，也可以导出在导出开始时指定的一种语言的标签。 标签将导出为包含 XML 文件的 zip 文件。 每个 XML 文件包含一种语言的标签。

![包含 DE-AT 语言的 ER 标签的导出文件的示例](./media/er-multilingual-labels-in-xml.png)

此格式用于通过外部翻译服务自动翻译标签，如 [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md)。 收到翻译的标签后，可以将它们重新导入到包含拥有这些标签的 ER 组件的 ER 配置的草稿版本中。 选择包含可编辑的 ER 组件的 ER 配置的草稿版本，然后选择**交换 \> 加载标签**。

![允许将 ER 标签导入到选定的配置版本的 ER 配置页面](./media/er-multilingual-labels-load.png)

翻译的标签将导入到所选的 ER 配置中。 此 ER 配置中存在的翻译的标签将被替换。 如果 ER 配置中缺少任何翻译的标签，将追加。

## <a name="lifecycle"></a>生命周期

可以编辑的 ER 组件的标签以及该组件的其他内容都保存在相应版本的 ER 配置中。

基本 ER 组件的标签可以在您创建以引入修改的 ER 组件的派生版本中引用。

ER 版本控制将控制向 ER 组件中的任何属性的标签分配。 对标签分配的更改将记录在已创建为所提供 ER 组件的派生版本的可编辑 ER 组件的更改列表（增量）中。 将派生版本重定为新的基本版本时，将验证这些更改。

## <a name="functions"></a>功能

内置的 [LISTOFFIELDS](er-functions-list-listoffields.md) ER 函数可以访问为某些 ER 组件项目配置的 ER 标签。

如本主题前面所述，每个[模型](#LinkModelEnum)或[格式](#LinkFormatEnum) ER 枚举的值的**标签**和**描述**属性，可以链接到可在适当的 ER 组件中访问的 ER 标签。 您可以使用 ER 枚举作为参数来配置调用 **LISTOFFIELDS**函数的 ER 表达式。 此表达式将返回一个列表，其中包含已定义为此函数的参数的 ER 枚举的每个值的记录。 每个记录均包含链接到 ER 枚举值的 ER 标签的值：

- 链接到**标签**属性的 ER 标签的值存储在返回记录的**标签**字段中。
- 链接到**描述**属性的 ER 标签的值存储在返回记录的**描述**字段中。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子报告功能](er-formula-language.md#functions)
