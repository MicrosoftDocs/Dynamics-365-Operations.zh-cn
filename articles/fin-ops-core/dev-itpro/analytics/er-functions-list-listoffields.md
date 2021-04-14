---
title: LISTOFFIELDS ER 函数
description: 本主题提供有关 LISTOFFIELDS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4f394a557beaeb558f5c7065eefe16f4aadce6ac
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743766"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER 函数

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS` 函数返回一个 *记录列表* 值，此值基于指定的 *枚举* 或 *容器（记录）* 类型的参数的结构创建。

## <a name="syntax-1"></a>语法 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>语法 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>参数

`path`：数据源引用

下列数据类型之一的数据源的有效引用路径：

- 模型枚举
- 格式枚举
- 应用程序枚举
- 容器（记录）

`language`：*字符串*

表示语言代码的文本。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

创建的列表由具有以下字段的记录组成：

- **名称**（*字符串* 数据类型）
- **标签**（*字符串* 数据类型）
- **描述**（*字符串* 数据类型）
- **IsTranslated**（*布尔值* 数据类型）

如果 `path` 参数引用 *容器（记录）* 类型的数据源，对于引用的容器记录的每个字段，都会向创建的列表中添加一条新记录。 对于创建的每个记录，**名称** 字段将返回为其创建当前记录的引用容器记录的字段的名称。

如果 `path` 参数引用 *枚举* 类型之一的数据源，对于引用的枚举的每个枚举值，都会向创建的列表中添加一条新记录。 对于创建的每个记录，**名称** 字段将返回为其创建当前记录的引用枚举的值，**描述** 字段将返回该枚举的描述，**标签** 字段将返回该枚举的标签。

在运行时，使用语法 1 时，**标签** 和 **描述** 字段必须返回基于正在运行的电子申报 (ER) 格式的语言设置的值：

- 如果提供了所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于该语言的值，**IsTranslated** 字段将返回 **True**。
- 如果未提供所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于默认 **EN-US** 语言的值，**IsTranslated** 字段将返回 **False**。

在运行时，使用语法 2 时，**标签** 和 **描述** 字段必须返回基于定义为被调用函数的第二个参数的语言的值：

- 如果提供了所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于该语言的值，**IsTranslated** 字段将返回 **True**。
- 如果未提供所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于 **EN-US** 语言的值，**IsTranslated** 字段将返回 **False**。

## <a name="example-1"></a>示例 1

在下图中，ER 数据模型中引入了枚举。

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

下图显示以下详细信息：

- 模型枚举作为数据源插入了报表中。
- ER 表达式将模型枚举用作 `LISTOFFIELDS` 函数的参数。
- 使用创建的 ER 表达式将 *记录列表* 类型的数据源插入了报表中。

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

以下示例显示绑定到使用 `LISTOFFIELDS` 函数创建的 *记录列表* 类型数据源的 ER 格式元素。

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

下图显示运行设计的格式的结果。

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> 根据父 **FILE** 和 **FOLDER** 格式元素的语言设置，在 ER 格式的输出中输入了经过翻译的标签和说明文本。

## <a name="example-2"></a>示例 2

使用 *计算字段* 数据源类型为 **enumType** 数据模型枚举配置 **enumType\_de** 和 **enumType\_deCH** 数据源：

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

在此情况下，可使用以下表达式获取瑞士德语（如果该翻译可用）的枚举值标签。 如果瑞士德语翻译不可用，标签将为德语。

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]