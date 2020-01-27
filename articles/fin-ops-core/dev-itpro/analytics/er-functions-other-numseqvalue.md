---
title: NUMSEQVALUE ER 函数
description: 本主题提供有关 NUMSEQVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915824"
---
# <a name="NUMSEQVALUE">NUMSEQVALUE ER 函数</a>

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` 函数根据指定的编号规则、作用域和作用域 ID 返回一个*字符串*值，该值表示新生成的编号规则值。 作用域 ID 等于运行电子申报 (ER) 格式的上下文提供的公司代码。

## <a name="syntax-1"></a>语法 1

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>语法 2

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>语法 3

```
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>参数

`number sequence code`：*字符串*

表示需要新值的编号规则的代码的文本值。

`number sequence record ID`：*Int64*

一个 *Int64* 值，表示 NumberSequenceTable 表中记录的记录 ID，该表包含需要新值的编号规则的定义。

`scope type`：*枚举值*

**ERExpressionNumberSequenceScopeType** 枚举的枚举值，此枚举定义需要新值的编号规则的作用域。 可用作用域类型有**共享**、**法人**和**公司**。

`scope ID`：*字符串*

基于指定作用域类型确定作用域的*字符串*值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

对于**共享**作用域类型，指定一个空字符串作为作用域 ID。

对于**公司**和**法人**作用域类型，指定公司代码作为作用域 ID。 如果您为这些作用域类型指定空字符串作为作用域 ID，则将使用当前的公司代码。

当使用语法 1 时，将为**公司**作用域类型请求编号规则，公司代码由运行 ER 格式的上下文提供。

## <a name="example-1"></a>示例 1

在您的 ER 格式中，您定义*用户输入参数*类型的 **AskNumSeq** 数据源。 此数据源引用**描述**扩展数据类型 (EDT)。 接下来，定义*计算字段*类型的 **NumSeq** 数据源。 此数据源包含表达式 `NUMSEQVALUE (AskNumSeq)`。 当调用 **NumSeq** 数据源时，它将返回通过在对话框中输入其代码在运行时指定的编号规则的新生成的值。 为**公司**作用域类型请求编号规则。 公司代码由运行 ER 格式的上下文提供。

## <a name="example-2"></a>示例 2

以下数据源在模型映射中定义：

- *表*类型的 **LedgerParms** 数据源。 此数据源引用 LedgerParameters 表。
- *计算字段*类型的 **NumSeq** 数据源。 此数据源包含表达式 `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`。

在调用 **NumSeq** 数据源时，将返回在提供 ER 格式在其中运行的上下文的公司的总帐参数中配置的编号规则的新生成值。 此编号规则唯一标识日记帐，并充当将交易记录链接在一起的批号。

## <a name="example-3"></a>示例 3

以下数据源在模型映射中定义：

- Microsoft Dynamics 365 Finance *枚举*类型的 **enumScope** 数据源。 此数据源引用 **ERExpressionNumberSequenceScopeType** 枚举。
- *计算字段*类型的 **NumSeq** 数据源。 此数据源包含表达式 `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`。

在调用 **NumSeq** 数据源时，将返回为提供 ER 格式在其中运行的上下文的公司配置的 **Gene\_1** 编号规则的新生成值。

## <a name="additional-resources"></a>其他资源

[其他（业务域特定的）函数](er-functions-category-other.md)
