---
title: SPLIT ER 函数
description: 本主题提供有关 SPLIT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853435"
---
# <a name="split-er-function"></a><span data-ttu-id="88343-103">SPLIT ER 函数</span><span class="sxs-lookup"><span data-stu-id="88343-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88343-104">`SPLIT` 函数将指定的输入字符串拆分为子字符串，并将结果作为新的 *记录列表* 值返回。</span><span class="sxs-lookup"><span data-stu-id="88343-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="88343-105">语法 1</span><span class="sxs-lookup"><span data-stu-id="88343-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="88343-106">此语法用于拆分指定的输入字符串为子字符串，每个子字符串具有指定的长度。</span><span class="sxs-lookup"><span data-stu-id="88343-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="88343-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="88343-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="88343-108">此语法用于根据指定的分隔符拆分指定的输入字符串为子字符串。</span><span class="sxs-lookup"><span data-stu-id="88343-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="88343-109">参数</span><span class="sxs-lookup"><span data-stu-id="88343-109">Arguments</span></span>

<span data-ttu-id="88343-110">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="88343-110">`input`: *String*</span></span>

<span data-ttu-id="88343-111">要拆分的文本。</span><span class="sxs-lookup"><span data-stu-id="88343-111">The text to split.</span></span>

<span data-ttu-id="88343-112">`length`：*整数*</span><span class="sxs-lookup"><span data-stu-id="88343-112">`length`: *Integer*</span></span>

<span data-ttu-id="88343-113">单个子字符串的最大长度。</span><span class="sxs-lookup"><span data-stu-id="88343-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="88343-114">`delimiter`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="88343-114">`delimiter`: *String*</span></span>

<span data-ttu-id="88343-115">用于分隔子字符串的分隔符。</span><span class="sxs-lookup"><span data-stu-id="88343-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="88343-116">返回值</span><span class="sxs-lookup"><span data-stu-id="88343-116">Return values</span></span>

<span data-ttu-id="88343-117">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="88343-117">*Record list*</span></span>

<span data-ttu-id="88343-118">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="88343-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="88343-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="88343-119">Usage notes</span></span>

<span data-ttu-id="88343-120">返回的列表的记录结构包括 *字符串* 类型的 **值** 字段。</span><span class="sxs-lookup"><span data-stu-id="88343-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="88343-121">返回的列表的每个记录在此字段中都包含生成的子字符串。</span><span class="sxs-lookup"><span data-stu-id="88343-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="88343-122">如果 `delimiter` 参数是空的，返回的新列表将包括一个具有 *字符串* 类型的 **值** 字段的记录。</span><span class="sxs-lookup"><span data-stu-id="88343-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="88343-123">此字段包含输入文本。</span><span class="sxs-lookup"><span data-stu-id="88343-123">This field contains the input text.</span></span>

<span data-ttu-id="88343-124">如果 `input` 参数为空，新的空列表将返回。</span><span class="sxs-lookup"><span data-stu-id="88343-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="88343-125">如果 `input` 或 `delimiter` 参数未指定（空），将引发应用程序异常。</span><span class="sxs-lookup"><span data-stu-id="88343-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="88343-126">示例 1</span><span class="sxs-lookup"><span data-stu-id="88343-126">Example 1</span></span>

<span data-ttu-id="88343-127">`SPLIT ("abcd", 3)` 返回包含具有 *字符串* 类型的 **值** 字段的两个记录的新列表。</span><span class="sxs-lookup"><span data-stu-id="88343-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="88343-128">第一个记录中的 **值** 字段包含文本 **"abc"**，第二个记录中的 **值** 字段包含文本 **"d"**。</span><span class="sxs-lookup"><span data-stu-id="88343-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="88343-129">示例 2</span><span class="sxs-lookup"><span data-stu-id="88343-129">Example 2</span></span>

<span data-ttu-id="88343-130">`SPLIT ("XAb aBy", "aB")` 返回包含具有 *字符串* 类型的 **值** 字段的三个记录的新列表。</span><span class="sxs-lookup"><span data-stu-id="88343-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="88343-131">第一个记录中的 **值** 字段包含文本 **"X"**，第二个记录中的 **值** 字段包含文本 **"&nbsp;"**，第三个记录中的 **值** 字段包含文本 **"y"**。</span><span class="sxs-lookup"><span data-stu-id="88343-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="88343-132">示例 3</span><span class="sxs-lookup"><span data-stu-id="88343-132">Example 3</span></span>

<span data-ttu-id="88343-133">您可以使用 [INDEX](er-functions-list-index.md) 函数访问指定输入字符串的各个元素。</span><span class="sxs-lookup"><span data-stu-id="88343-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="88343-134">如果输入 **计算字段** 类型的 **MyList** 数据源并且为其配置 `SPLIT("abc", 1)` 表达式，表达式 `INDEX(MyList,2).Value` 将返回文本 **“b”**。</span><span class="sxs-lookup"><span data-stu-id="88343-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="88343-135">示例 4</span><span class="sxs-lookup"><span data-stu-id="88343-135">Example 4</span></span>

<span data-ttu-id="88343-136">[ENUMERATE](er-functions-list-enumerate.md) 函数也可帮助您访问指定输入字符串的各个元素。</span><span class="sxs-lookup"><span data-stu-id="88343-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="88343-137">如果您首先输入 **计算字段** 类型的 **MyList** 数据源并且为其配置 `SPLIT("abc", 1)` 表达式，然后输入 **计算字段** 类型的 **EnumeratedList** 数据源并且为其配置 `ENUMERATE(MyList)` 表达式，表达式 `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` 将返回文本 **“b”**。</span><span class="sxs-lookup"><span data-stu-id="88343-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88343-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="88343-138">Additional resources</span></span>

[<span data-ttu-id="88343-139">列表函数</span><span class="sxs-lookup"><span data-stu-id="88343-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
