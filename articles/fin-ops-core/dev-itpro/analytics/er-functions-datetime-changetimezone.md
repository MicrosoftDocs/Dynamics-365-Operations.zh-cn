---
title: CHANGETIMEZONE ER 函数
description: 本文提供有关 CHANGETIMEZONE 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: d732fd8bd44c4c131f376919b2546a7ecf668495
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286110"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER 函数

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` 函数返回一个协调世界时（格林威治标准时间 \[GMT\]）的 *[日期/时间](er-formula-supported-data-types-primitive.md#datetime)* 值，此值从一个时区中的给定日期/时间值转换为另一个时区中的日期/时间值。

## <a name="syntax"></a>语法

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>参数

`datetime`：*日期时间*

表示要转换的日期/时间值的协调世界时时区的日期/时间值。

`base time zone`：*[字符串](er-formula-supported-data-types-primitive.md#string)*

给定日期/时间值在转换前进入的时区的名称。

`target time zone`：*字符串*

转换后的日期/时间值在转换过程中进入的时区的名称。

## <a name="return-values"></a>返回值

*日期时间*

生成的协调世界时时区的日期/时间值。

## <a name="usage-notes"></a>使用说明

要指定源时区和目标时区，您可以使用[互联网编号分配机构 (IANA)](https://www.iana.org/) [提供](https://data.iana.org/time-zones/releases/)或 Microsoft Windows [支持](/windows-hardware/manufacture/desktop/default-time-zones)的时区名称。

在运行时，如果在 IANA 列表或 Windows 注册表中找不到提供的名称，将引发异常“时区‘\<time zone name\>’不存在”。

对于遵守夏令时的时区，转换会考虑协调世界时夏令时偏移。 转换期间将使用有关此偏移的最新可用信息。

## <a name="example-1"></a>示例 1

在此示例中，使用 Windows 的时区名称。

您配置 **计算字段** 类型的 **DSX** 数据源。 它包含以下表达式。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

如果将 **计算字段** 类型的 **DSY** 数据源的表达式配置为 `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`，**DSX** 数据源将返回文本 **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**。 此文本显示，6 月 1 日提供的两个时区之间的时间差超过 24 小时。 因此，转换后的日期/时间值比给定的日期/时间值早一天，因为基本时区早于目标时区。

如果将 **计算字段** 类型的 **DSY** 数据源的表达式配置为 `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`，**DSX** 数据源将返回文本 **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**。 此文本显示，12 月 1 日提供的两个时区之间的时间差不到 24 小时。 因此，转换后的日期/时间值等于给定日期/时间值。

> [!NOTE]
> 相同表达式为同一对时区返回了不同的提供和转换的日期/时间值差值，因为提供的时区在给定日期/时间遵守不同的协调世界时夏令时偏移。

## <a name="example-2"></a>示例 2

在此示例中，使用 IANA 时区名称。

您配置 **计算字段** 类型的 **DSX** 数据源。 它包含以下表达式。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

如果将 **计算字段** 类型的 **DSY** 数据源的表达式配置为 `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`，**DSX** 数据源将返回文本 **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**。 此文本显示，6 月 1 日提供的两个时区之间的时间差超过 24 小时。 因此，转换后的日期/时间值比给定的日期/时间值早一天，因为基本时区早于目标时区。

如果将 **计算字段** 类型的 **DSY** 数据源的表达式配置为 `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`，**DSX** 数据源将返回文本 **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**。 此文本显示，12 月 1 日提供的两个时区之间的时间差不到 24 小时。 因此，转换后的日期/时间值等于给定日期/时间值。

## <a name="example-3"></a>示例 3

您配置 **计算字段** 类型的 **DSX** 数据源。 它包含以下表达式。

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

如果将 **计算字段** 类型的 **DSY** 数据源的表达式配置为 `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`，**DSX** 数据源将返回文本 **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**。 此文本显示，6 月 1 日提供的两个时区之间的时间差超过 24 小时。 因此，转换后的日期/时间值比给定的日期/时间值晚一天，因为目标时区早于基本时区。

## <a name="example-4"></a>示例 4

您可能会以不包含时区信息的文本形式收到来自外部来源的日期/时间戳。 但是，您可能知道来源所运营的时区。 例如，您从在西班牙运营的服务收到日期/时间戳 **01/12/2021 12:55:00**。 要将此日期/时间值正确保存到数据库，请完成以下转换：

- 配置 **计算字段** 类型的 **DSY** 数据源以将日期/时间戳从文本转换为协调世界时日期/时间值。

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- 配置 **计算字段** 类型的 **DSX** 数据源，让转换后的日期/时间值作为外部来源时区的日期/时间值进入协调世界时。

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> 当您使用 `CHANGETIMEZONE` 函数进行日期/时间转换时，请注意任何日期/时间值都作为协调世界时时区中的值存储在数据库中。 此值在应用程序页面上显示之前就已经转换了。 转换将[设置](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md)的时区视为当前登录的应用程序用户的首选时区。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
