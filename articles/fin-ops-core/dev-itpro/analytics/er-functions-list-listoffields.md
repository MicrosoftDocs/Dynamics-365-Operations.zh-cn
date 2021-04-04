---
title: LISTOFFIELDS ER 函数
description: 本主题提供有关 LISTOFFIELDS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567656"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="82437-103">LISTOFFIELDS ER 函数</span><span class="sxs-lookup"><span data-stu-id="82437-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82437-104">`LISTOFFIELDS` 函数返回一个 *记录列表* 值，此值基于指定的 *枚举* 或 *容器（记录）* 类型的参数的结构创建。</span><span class="sxs-lookup"><span data-stu-id="82437-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="82437-105">语法 1</span><span class="sxs-lookup"><span data-stu-id="82437-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="82437-106">语法 2</span><span class="sxs-lookup"><span data-stu-id="82437-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="82437-107">参数</span><span class="sxs-lookup"><span data-stu-id="82437-107">Arguments</span></span>

<span data-ttu-id="82437-108">`path`：数据源引用</span><span class="sxs-lookup"><span data-stu-id="82437-108">`path`: Data source reference</span></span>

<span data-ttu-id="82437-109">下列数据类型之一的数据源的有效引用路径：</span><span class="sxs-lookup"><span data-stu-id="82437-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="82437-110">模型枚举</span><span class="sxs-lookup"><span data-stu-id="82437-110">Model enumeration</span></span>
- <span data-ttu-id="82437-111">格式枚举</span><span class="sxs-lookup"><span data-stu-id="82437-111">Format enumeration</span></span>
- <span data-ttu-id="82437-112">应用程序枚举</span><span class="sxs-lookup"><span data-stu-id="82437-112">Application enumeration</span></span>
- <span data-ttu-id="82437-113">容器（记录）</span><span class="sxs-lookup"><span data-stu-id="82437-113">Container (record)</span></span>

<span data-ttu-id="82437-114">`language`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="82437-114">`language`: *String*</span></span>

<span data-ttu-id="82437-115">表示语言代码的文本。</span><span class="sxs-lookup"><span data-stu-id="82437-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="82437-116">返回值</span><span class="sxs-lookup"><span data-stu-id="82437-116">Return values</span></span>

<span data-ttu-id="82437-117">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="82437-117">*Record list*</span></span>

<span data-ttu-id="82437-118">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="82437-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="82437-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="82437-119">Usage notes</span></span>

<span data-ttu-id="82437-120">创建的列表由具有以下字段的记录组成：</span><span class="sxs-lookup"><span data-stu-id="82437-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="82437-121">**名称**（*字符串* 数据类型）</span><span class="sxs-lookup"><span data-stu-id="82437-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="82437-122">**标签**（*字符串* 数据类型）</span><span class="sxs-lookup"><span data-stu-id="82437-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="82437-123">**描述**（*字符串* 数据类型）</span><span class="sxs-lookup"><span data-stu-id="82437-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="82437-124">**IsTranslated**（*布尔值* 数据类型）</span><span class="sxs-lookup"><span data-stu-id="82437-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="82437-125">如果 `path` 参数引用 *容器（记录）* 类型的数据源，对于引用的容器记录的每个字段，都会向创建的列表中添加一条新记录。</span><span class="sxs-lookup"><span data-stu-id="82437-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="82437-126">对于创建的每个记录，**名称** 字段将返回为其创建当前记录的引用容器记录的字段的名称。</span><span class="sxs-lookup"><span data-stu-id="82437-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="82437-127">如果 `path` 参数引用 *枚举* 类型之一的数据源，对于引用的枚举的每个枚举值，都会向创建的列表中添加一条新记录。</span><span class="sxs-lookup"><span data-stu-id="82437-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="82437-128">对于创建的每个记录，**名称** 字段将返回为其创建当前记录的引用枚举的值，**描述** 字段将返回该枚举的描述，**标签** 字段将返回该枚举的标签。</span><span class="sxs-lookup"><span data-stu-id="82437-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="82437-129">在运行时，使用语法 1 时，**标签** 和 **描述** 字段必须返回基于正在运行的电子申报 (ER) 格式的语言设置的值：</span><span class="sxs-lookup"><span data-stu-id="82437-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="82437-130">如果提供了所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于该语言的值，**IsTranslated** 字段将返回 **True**。</span><span class="sxs-lookup"><span data-stu-id="82437-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="82437-131">如果未提供所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于默认 **EN-US** 语言的值，**IsTranslated** 字段将返回 **False**。</span><span class="sxs-lookup"><span data-stu-id="82437-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="82437-132">在运行时，使用语法 2 时，**标签** 和 **描述** 字段必须返回基于定义为被调用函数的第二个参数的语言的值：</span><span class="sxs-lookup"><span data-stu-id="82437-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="82437-133">如果提供了所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于该语言的值，**IsTranslated** 字段将返回 **True**。</span><span class="sxs-lookup"><span data-stu-id="82437-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="82437-134">如果未提供所请求语言的标签和描述，**标签** 和 **描述** 字段将返回基于 **EN-US** 语言的值，**IsTranslated** 字段将返回 **False**。</span><span class="sxs-lookup"><span data-stu-id="82437-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="82437-135">示例 1</span><span class="sxs-lookup"><span data-stu-id="82437-135">Example 1</span></span>

<span data-ttu-id="82437-136">在下图中，ER 数据模型中引入了枚举。</span><span class="sxs-lookup"><span data-stu-id="82437-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="82437-137">下图显示以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="82437-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="82437-138">模型枚举作为数据源插入了报表中。</span><span class="sxs-lookup"><span data-stu-id="82437-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="82437-139">ER 表达式将模型枚举用作 `LISTOFFIELDS` 函数的参数。</span><span class="sxs-lookup"><span data-stu-id="82437-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="82437-140">使用创建的 ER 表达式将 *记录列表* 类型的数据源插入了报表中。</span><span class="sxs-lookup"><span data-stu-id="82437-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="82437-141">以下示例显示绑定到使用 `LISTOFFIELDS` 函数创建的 *记录列表* 类型数据源的 ER 格式元素。</span><span class="sxs-lookup"><span data-stu-id="82437-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="82437-142">下图显示运行设计的格式的结果。</span><span class="sxs-lookup"><span data-stu-id="82437-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="82437-143">根据父 **FILE** 和 **FOLDER** 格式元素的语言设置，在 ER 格式的输出中输入了经过翻译的标签和说明文本。</span><span class="sxs-lookup"><span data-stu-id="82437-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="82437-144">示例 2</span><span class="sxs-lookup"><span data-stu-id="82437-144">Example 2</span></span>

<span data-ttu-id="82437-145">使用 *计算字段* 数据源类型为 **enumType** 数据模型枚举配置 **enumType\_de** 和 **enumType\_deCH** 数据源：</span><span class="sxs-lookup"><span data-stu-id="82437-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="82437-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="82437-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="82437-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="82437-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="82437-148">在此情况下，可使用以下表达式获取瑞士德语（如果该翻译可用）的枚举值标签。</span><span class="sxs-lookup"><span data-stu-id="82437-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="82437-149">如果瑞士德语翻译不可用，标签将为德语。</span><span class="sxs-lookup"><span data-stu-id="82437-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="82437-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="82437-150">Additional resources</span></span>

[<span data-ttu-id="82437-151">列表函数</span><span class="sxs-lookup"><span data-stu-id="82437-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]