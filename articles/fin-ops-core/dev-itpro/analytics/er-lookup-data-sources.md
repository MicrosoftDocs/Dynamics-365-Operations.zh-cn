---
title: 配置查找数据源以使用 ER 应用程序特定的参数
description: 本主题说明如何配置电子报告 (ER) 格式的查找数据源以使用 ER 应用程序特定的参数。
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 682910350832e441ed13c716c0c18200a3b7865d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351065"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>配置查找数据源以使用 ER 应用程序特定的参数 

[!include[banner](../includes/banner.md)]

[电子报告 (ER)](general-electronic-reporting.md) 应用程序特定的参数功能使您可以以 ER 格式配置数据筛选，使其基于一组抽象规则。 可以将这组规则配置为使用以 ER 格式提供的 **查找** 类型的数据源。 然后，您可以使用基于相应 ER 格式的 **查找** 数据源的设置以及当前法人数据自动生成的用户界面 (UI)，指定 ER 组件设计器之外的实际规则。 最终，当执行此 ER 格式时，将通过 ER 格式的 **查找** 数据源访问指定的规则。

> [!NOTE]
> 使用可编辑 ER 格式的已配置数据源指定哪些应用程序数据用于配置实际规则。

使用 [ER Operations 设计器](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base)将 **查找** 数据源引入到 ER 格式中。 必须配置数据源以描述抽象规则的外观，包括以下内容：

   - 某些数据类型的参数集，提供其值以指定单个规则。
   - 当将此规则视为最适合的规则时，单个规则返回的某些数据类型的值类型。

您可以配置以下类型的 **查找** 数据源，具体取决于任何已配置规则返回的值类型：

   - 在必须返回模型枚举值时，使用 **数据模型\查找** 类型。
   - 在必须返回应用程序枚举值或应用程序 [扩展数据类型](../extensibility/extensible-edts.md)值时，使用 **Dynamics 365 Operations\查找** 类型。
   - 在必须返回格式枚举值时，使用 **格式枚举\查找** 类型。

下图显示了如何以示例 ER 格式配置格式枚举。

   ![显示格式枚举作为已配置查找数据源的基础。](./media/er-lookup-data-sources-img1.gif)

下图显示了配置为在生成报告的不同部分中报告不同类型税务的格式组件。

   ![显示格式部分以分别报告不同类型的税务。](./media/er-lookup-data-sources-img2.png)

下图显示了 ER Operations 设计器如何允许添加 **格式枚举\查找** 类型的数据源。  添加的数据源配置为返回 `List of taxation levels` 格式枚举的值。

   ![添加格式枚举\查找类型的 ER 数据源。](./media/er-lookup-data-sources-img3.gif)

下图显示了如何将添加的数据源配置为使用 **模型** 数据源的 **Model.Data.Tax** 记录列表的 **代码** 字段作为必须为每个配置规则指定的参数。

![配置格式枚举\查找类型的已添加数据源的参数。](./media/er-lookup-data-sources-img4.gif)

添加的 `Model.Data.Tax` 数据源配置为通过访问 **TaxTable** 应用程序表的记录为每个配置规则指定税码。

   ![查看格式枚举\查找类型的单个公司查找数据源。](./media/er-lookup-data-sources-img5.gif)

您可以使用与已配置数据源的结构自动对齐的 UI 为选择的 ER 格式设置查找规则。 当前，此 UI 要求对于每个规则，都指定返回的值作为 `List of taxation levels` 格式枚举值，以及指定税码作为参数。

   ![设置已配置数据源的规则。](./media/er-lookup-data-sources-img6.gif)

下图显示了如何配置 **计算字段** 类型的 `Model.Data.Summary.LevelByLookup` 数据源以调用提供所需参数的已配置 **查找** 数据源。 若要在运行时处理此调用，ER 按定义的顺序浏览已配置规则的列表，以找到满足所提供条件的第一个规则。 在此示例中，该规则包含与提供的税码匹配的税码。 因此，找到最适合的规则，此数据源返回为找到的规则配置的枚举值。

> [!NOTE]
> 如果找不到适用的规则，则会引发异常。 若要防止这些异常，请在规则列表的末尾配置其他规则，以处理提供非配置值或未提供值的情况。 相应地使用 **\*非空白\***和 **\*空白\***选项。  
>
> ![添加数据源以调用已配置的查找数据源。](./media/er-lookup-data-sources-img7.png)

当您针对可编辑的查找数据源将 **跨公司** 选项设置为 **是** 时，将新的所需 **公司** 参数添加到此数据源的参数集。 当调用查找数据源时，必须在运行时指定 **公司** 参数的值。 当在运行时指定公司代码时，为此公司配置的规则用于查找最适合的规则，并返回相应的值。 下图显示了如何执行此操作以及如何更改可编辑数据源的参数集。

   ![查看格式枚举\查找类型的跨公司查找数据源。](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> 分别选择每个公司以为可编辑 ER 格式的此查找数据源配置规则集。 当使用未完成其查找设置的公司代码调用跨公司查找时，将在运行时引发异常。
>
> 确保向使用跨公司 **查找** 数据源运行 ER 格式的用户授予权限，以访问此数据源范围内的每个公司的数据。 否则，将在运行时引发异常。

从版本 10.0.19 开始，将提供 **查找** 数据源的扩展功能。 当针对可编辑查找数据源将 **扩展** 选项设置为 **是** 时，已配置查找数据源将转换为提供其他功能以分析配置规则集的结构数据源。 下图显示了此转换。

   ![查看格式枚举\查找类型的结构查找数据源。](./media/er-lookup-data-sources-img9.gif)

- **查找** 子项设计为一个函数，用于基于提供的参数集从可配置规则集中查找最适合的规则。
- **IsLookupResultSet** 子项设计为一个函数，用于接受基本枚举数据源的提供值，并在规则集包含至少一个将提供的枚举值配置为返回值的规则时，返回 *布尔* 值 **True**。 当没有规则配置为返回提供的枚举值时，此函数返回 *布尔* 值 **False**。
- **设置** 子项设计为一个函数，用于返回已配置规则集作为记录列表的记录。 已配置规则的返回值和参数集在每个返回的记录中显示为相关数据类型的字段：

    - 返回值显示为 **查找结果** 字段。
    - 配置的参数显示为具有参数名称的字段（在此示例中为 **代码** 字段）。

有关如何配置 **查找** 数据源的详细信息，请参阅[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)。 若要了解如何设置查找规则，请参阅[为每个法人设置 ER 格式的参数](er-app-specific-parameters-set-up.md)。

## <a name="additional-resources"></a>其他资源

[配置电子报告格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)

[为每个法人设置电子报告格式的参数](er-app-specific-parameters-set-up.md)
