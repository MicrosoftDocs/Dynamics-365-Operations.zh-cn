---
title: 文档路线标签布局
description: 本文介绍如何使用格式设置方法打印标签上的值。
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708636"
---
# <a name="document-routing-label-layout"></a>文档路线标签布局

[!include [banner](../includes/banner.md)]

本文介绍如何为牌照、集装箱和波次标签创建布局。 另外还提供使用用于创建布局的 Zebra 编程语言 (ZPL) 的指南。

文档路线标签布局定义标签的布局方式以及标签上打印的数据。 请在设置移动设备菜单项和工作模板时配置打印触发点。

本文中的信息适用于所有文档路线标签布局，包括[牌照标签](tasks/license-plate-label-printing.md)、[集装箱标签](print-container-labels.md)和[波次标签](configure-wave-label-printing.md)布局。

如果打印设备可以解读收到的文本，您可以打印极为复杂的标签。 例如，其中包含条形码的 ZPL 布局可能类似以下示例。

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

在标签打印流程中，此示例中的文本 `$LicensePlateId$` 将替换为数据值。 几种广泛使用的标签生成工具可帮助您设置标签布局的文本的格式。 这些工具中许多都支持 `$FieldName$` 格式。 此外，Microsoft Dynamics 365 Supply Chain Management 在文档路线选择布局的字段映射中使用特殊格式设置逻辑。

若要查看将打印的值，请转到 **仓库管理 \> 查看和报表 \> 牌照标签**。

## <a name="turn-on-this-feature-for-your-system"></a>为您的系统启用此功能

如果您的系统尚未包含本文中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *增强的牌照标签布局* 功能。 （从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。）

## <a name="custom-number-formats"></a>自定义数字格式

可自定义使用采用以下格式的代码打印的数值字段值的格式设置。

```dos
$FieldName:FormatString$
```

下面是对此格式的说明：

- `FieldName` 是数据字段的名称（如 **Qty**）。
- `FormatString` 定义必须如何打印数据。

下面的示例显示如何自定义工作数量 (**Qty**) 字段：

- 若要始终显示四位数（将零用作占位符），请使用 `$Qty:0000$`。 例如，如果数量为 10，则标签将显示“0010”。
- 若要始终显示两位数，请使用 `$Qty:0.00$`。 例如，如果数量为 10，则标签将显示“10.00”。

有关可用数字格式字符串的完整列表，请参阅[自定义数值格式字符串](/dotnet/standard/base-types/custom-numeric-format-strings)。

## <a name="custom-string-formats"></a>自定义字符串格式

可使用以下字段和格式代码删除字符串的第一批字符。

```dos
$FieldName:#..$
```

下面，`#` 指定要跳过的字符数量。 例如，若要打印不包含前两个字符的系列货运包装箱代码 (SSCC) 牌照编号，请使用 `$LicensePlateId:2..$`。 在此示例中，牌照编号 0011111111111222221 将打印为“11111111111222221”。

## <a name="custom-datetime-formats"></a>自定义日期/时间格式

以下示例显示如何控制用于打印日期的格式。

```dos
$PrintedDate:dd-MM-yyyy$
```

在此示例中，日期 2020 年 4 月 30 日将被打印为“30-04-2020”。

有关可用日期/时间格式的完整列表，请参阅[自定义日期和时间格式字符串](/dotnet/standard/base-types/custom-date-and-time-format-strings)。

## <a name="print-individual-lines-from-multiline-data"></a>打印多行数据的单独行

如果一个数据字段中包含多行（即换行符分隔的行），可以使用以下格式打印单行。

```dos
$FieldName[#]$
```

下面，`#` 是要打印的行号。 （1 代表第一行。）

例如，您的系统中有一个 `AdditionalAddress` 字段存储下面的多行地址：

Contoso Inc.  
123 Street Name  
Some City, Some State

可使用下面的代码一次一行打印此地址。

| 代码 | 打印的文本 |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Street Name |
| `$AdditionalAddress[3]$` | Some City, Some State |

## <a name="print-and-format-from-a-display-method"></a>通过显示方法打印和设置格式

可使用以下格式通过显示方法进行打印。

```dos
$DisplayMethod()$
```

可以将此格式与本文中前面介绍的其他类型组合使用。 例如，您有一个显示方法名称为 `DisplayListOfItemsNumbers()`，而您希望打印此方法的第一个项目编号。 在这种情况下，可以使用以下代码。

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>有关如何打印标签的详细信息

有关如何设置和打印标签的详细信息，请参阅以下文章：

- [牌照标签打印](tasks/license-plate-label-printing.md)
- [打印集装箱标签](print-container-labels.md)
- [波次标签打印](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
