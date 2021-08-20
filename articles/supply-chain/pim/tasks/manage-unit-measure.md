---
title: 管理度量单位
description: 本主题介绍如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746931"
---
# <a name="manage-units-of-measure"></a>管理度量单位

[!include [banner](../../includes/banner.md)]

本主题介绍如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。

## <a name="open-the-units-page"></a>打开单位页面

要创建并使用系统中提供的度量单位，请转到 **组织管理 \> 设置 \> 单位 \> 单位**。

本主题的其余几节介绍您可以在 **单位** 页执行的操作。

## <a name="create-standard-units-and-conversions"></a>创建标准单位和转换

如果您的系统尚未包括公制和/或美国惯用系统 (USCS) 的最常用度量单位，单位设置向导可以帮助您快速开始使用基本的单位定义和转换。 要完成此向导，在操作窗格上选择 **单位创建向导**，然后按照屏幕上的说明操作。

## <a name="create-or-edit-a-unit-of-measure"></a>创建或编辑度量单位

要创建或编辑度量单位，请按照下列步骤操作。

1. 按以下步骤之一：

    - 要编辑现有单位，在列表窗格中选择它。
    - 要创建新单位，在操作窗格上选择 **新建**。

1. 在记录的标头上，设置以下字段：

    - **单位** – 输入用于以系统语言引用单位的 ID 或符号。 此 ID 或符号通常是单位的常用缩写，如每个是 *ea*，厘米是 *cm*。
    - **描述** – 为单位输入系统语言的描述性名称。 此名称通常是单位的完整名称，如 *每个* 或者 *厘米*。

1. 在 **常规** 快速选项卡上，设置以下字段：<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **单位类** – 选择单位度量的属性（如长度、面积、质量或数量）。
    - **单位系统** – 选择单位所属的度量系统（*公制单位* 或 *美国惯用单位*）。
    - **基础单位** – 将此选项设置为 *是* 可以将当前单位用作其单位类的基础单位。 在这种情况下，您只需指定单位类中基础单位和每个其他单位之间的换算系数。 然后，系统可以在该单位类中的所有单位之间进行转换。 因此，设置转换更加容易。

        例如，如果加仑是 *体积* 单位类的基础单位，您只需设置从夸脱到加仑以及从品脱到加仑的换算系数。 然后，系统还可以从夸脱转换为品脱。

        每个单位类只能有一个基础单位。

    - **系统单位** – 将此选项设置为 *是* 可以将当前单位用作其单位类中所有未指定度量的假定单位。 例如，如果用于输入数量的字段不允许指定单位（或如果用户未选择单位），系统将使用设置为 *数量* 单位类的系统单位的单位。 每个单位类只能有一个系统单位。
    - **小数精度** – 指定为当前单位指定或转换为它应该舍入的值的小数位数。

1. 在操作窗格上，选择 **保存**。

## <a name="define-unit-translations"></a>定义单位转换

要为 ID 或符号以及度量单位的描述定义翻译，请按照下列步骤操作。

1. 创建或选择要为其创建翻译的单位。
1. 在操作窗格上，选择 **单位文本**。

    **单位文本** 页将出现。 您将使用此页面为所选单位的 ID 或符号定义翻译。 然后可以将这些翻译用于客户特定语言或供应商特定语言的外部文档。

1. 在操作窗格上，选择 **新建**。
1. 在 **语言** 字段中，选择要将单位 ID 或符号翻译成的语言。
1. 在 **文本** 字段中，输入所选语言的单位 ID 或符号的翻译。
1. 在操作窗格上，选择 **保存**。
1. 关闭该页面。
1. 在 **操作窗格** 上，选择 **翻译的单位描述**。

    **翻译的单位描述** 页将出现。 您将使用此页面为所选单位定义语言特定描述。

1. 在操作窗格上，选择 **新建**。
1. 在 **语言** 字段中，选择要将单位描述翻译成的语言。
1. 在 **描述** 字段中，输入所选语言的单位描述的翻译。
1. 在操作窗格上，选择 **保存**。
1. 关闭该页面。

## <a name="define-unit-conversion-rules"></a>定义单位换算规则

要定义度量单位之间的转换规则，请按照下列步骤操作。

1. 创建或选择要为其定义转换规则的单位。
1. 在操作窗格上，选择 **单位转换**。

    **单位转换** 页将出现。 您将使用此页面定义将单位类中的所选单位与其他单位进行相互转换的规则。

1. 选择以下选项卡之一，具体取决于您要设置的转换类型：

    - **标准转换** – 为所有产品设置标准转换规则。
    - **类内转换** – 为同一单位类中的单位设置产品特定转换规则。
    - **类间转换** – 为不同单位类中的单位设置产品特定转换规则。

1. 按以下步骤之一：

    - 要创建新转换，在工具栏上选择 **新建**。
    - 要编辑现有转换，在网格中选择转换，然后在工具栏上选择 **编辑**。

1. 在出现的下拉对话框中，设置以下字段：

    - **产品** – 选择转换将应用的特定产品。 此字段仅可用于类内和类间转换。
    - **公式布局** – 将此字段设置为 *简单* 将指定具有单个系数的简单转换。 将其设置为 *高级* 将设置更复杂的方程式。 高级方程式的格式因单位类而异。
    - **源单位** – 此字段显示所选单位。 通常，您不应更改此值。 （如果您确实更改了此值，则必须在保存后打开所选单位的 **单位转换** 页，查看新转换。）
    - **目标单位** – 选择要转换的单位。
    - **舍入** – 根据所选单位的 **小数精度** 值选择应舍入的小数（*最近*、*向上* 或 *向下*）。
    - **转换公式** – 使用下拉对话框顶部的其余字段指定两个单位之间的转换公式。 可用字段会有所不同，具体取决于您选择的单位类和公式布局。

1. 选择 **确定**。
1. 关闭该页面。

> [!TIP]
> 您还可以针对每个产品变型设置单位转换。 有关详细信息，请参阅[按照产品变型的度量单位转换](../uom-conversion-per-product-variant.md)。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
