---
title: FORMAT ER 函数
description: 本主题提供有关 FORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b347a7209ee543f6bd687c2864203eb632d6a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688405"
---
# <a name="format-er-function"></a>FORMAT ER 函数

[!include [banner](../includes/banner.md)]

通过使用第 *N* 个参数替换出现的所有 **%N** 设定指定字符串的格式后，`FORMAT` 函数作为 *字符串* 值返回该字符串。

## <a name="syntax"></a>语法

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>参数

`string`：*字符串*

对必须设定格式的 *字符串* 类型的数据源的引用。 此参数是必需的。

`argument 1`：*字符串*

第一个参数，用于替换出现的 **%1**。 此参数是必需的。

`argument N`：*字符串*

第 *N* 个参数，用于替换出现的 **%2**、**%3**，依此类推。 其他参数是可选的。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

如果参数不是为参量提供，则参量在字符串中返回为 **"%N"**。 对于 *实数* 类型的值，默认字符串转换被限制为两位小数。

## <a name="example"></a>示例

在下图中，**PaymentModel** 数据源使用 **客户** 组件返回客户记录列表。 它使用 **ProcessingDate** 字段返回处理日期值。

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

在指定用于为所选客户生成电子文件的电子申报 (ER) 格式中，**PaymentModel** 被选择为数据源并控制流程。 如果所选客户在处理报表的日期停止，将引发异常以通知用户。 为此类处理控制设计的配方可以使用以下资源：

- 标签 SYS70894，具有以下文本：

    - **对于 EN-US 语言：**"Nothing to print"
    - **对于 DE 语言：**"Nichts zu drucken"

- 标签 SYS18389，具有以下文本：

    - **对于 EN-US 语言：**"Customer %1 is stopped for %2."
    - **对于 DE 语言：**"Debitor '%1' wird für %2 gesperrt."

这是一个可设计的表达式。

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

如果报表于 2015 年 12 月 17 日为 **Litware 零售** 客户处理，在 **EN-US** 区域性和 **EN-US** 语言中，此公式返回以下文本，其可能向用户呈现为异常消息：

*没有要打印的内容。客户 Litware 零售已于 2015 年 12 月 17 日停止。*

如果 2015 年 12 月 17 日为 **Litware 零售** 客户处理同一个报表，在 **DE** 区域性和 **DE** 语言中，此公式返回以下文本（使用不同的日期格式）：

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> 以下语法在标签的 ER 公式中应用：
>
> - **对于 Microsoft Dynamics 365 Finance 应用中资源的标签：** **\@X**，其中 **X** 是应用程序对象树 (AOT) 中的标签 ID
> - **对于位于 ER 配置中的标签：** **@"GER_LABEL:X"**，其中 **X** 是 ER 配置中的标签 ID

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]