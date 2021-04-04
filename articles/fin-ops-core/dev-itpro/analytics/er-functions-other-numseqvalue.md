---
title: NUMSEQVALUE ER 函数
description: 本主题提供有关 NUMSEQVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 23dc112651e4425b8020ee5c843509b4df83e810
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563310"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="43ff1-103">NUMSEQVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="43ff1-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43ff1-104">`NUMSEQVALUE` 函数根据指定的编号规则、作用域和作用域 ID 返回一个 *字符串* 值，该值表示新生成的编号规则值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="43ff1-105">作用域 ID 等于运行电子申报 (ER) 格式的上下文提供的公司代码。</span><span class="sxs-lookup"><span data-stu-id="43ff1-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="43ff1-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="43ff1-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="43ff1-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="43ff1-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="43ff1-108">语法 3</span><span class="sxs-lookup"><span data-stu-id="43ff1-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="43ff1-109">参数</span><span class="sxs-lookup"><span data-stu-id="43ff1-109">Arguments</span></span>

<span data-ttu-id="43ff1-110">`number sequence code`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="43ff1-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="43ff1-111">表示需要新值的编号规则的代码的文本值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="43ff1-112">`number sequence record ID`：*Int64*</span><span class="sxs-lookup"><span data-stu-id="43ff1-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="43ff1-113">一个 *Int64* 值，表示 NumberSequenceTable 表中记录的记录 ID，该表包含需要新值的编号规则的定义。</span><span class="sxs-lookup"><span data-stu-id="43ff1-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="43ff1-114">`scope type`：*枚举值*</span><span class="sxs-lookup"><span data-stu-id="43ff1-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="43ff1-115">**ERExpressionNumberSequenceScopeType** 枚举的枚举值，此枚举定义需要新值的编号规则的作用域。</span><span class="sxs-lookup"><span data-stu-id="43ff1-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="43ff1-116">可用作用域类型有 **共享**、**法人** 和 **公司**。</span><span class="sxs-lookup"><span data-stu-id="43ff1-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="43ff1-117">`scope ID`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="43ff1-117">`scope ID`: *String*</span></span>

<span data-ttu-id="43ff1-118">基于指定作用域类型确定作用域的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="43ff1-119">返回值</span><span class="sxs-lookup"><span data-stu-id="43ff1-119">Return values</span></span>

<span data-ttu-id="43ff1-120">*字符串*</span><span class="sxs-lookup"><span data-stu-id="43ff1-120">*String*</span></span>

<span data-ttu-id="43ff1-121">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43ff1-122">使用说明</span><span class="sxs-lookup"><span data-stu-id="43ff1-122">Usage notes</span></span>

<span data-ttu-id="43ff1-123">对于 **共享** 作用域类型，指定一个空字符串作为作用域 ID。</span><span class="sxs-lookup"><span data-stu-id="43ff1-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="43ff1-124">对于 **公司** 和 **法人** 作用域类型，指定公司代码作为作用域 ID。</span><span class="sxs-lookup"><span data-stu-id="43ff1-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="43ff1-125">如果您为这些作用域类型指定空字符串作为作用域 ID，则将使用当前的公司代码。</span><span class="sxs-lookup"><span data-stu-id="43ff1-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="43ff1-126">当使用语法 1 时，将为 **公司** 作用域类型请求编号规则，公司代码由运行 ER 格式的上下文提供。</span><span class="sxs-lookup"><span data-stu-id="43ff1-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="43ff1-127">示例 1</span><span class="sxs-lookup"><span data-stu-id="43ff1-127">Example 1</span></span>

<span data-ttu-id="43ff1-128">在您的 ER 格式中，您定义 *用户输入参数* 类型的 **AskNumSeq** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="43ff1-129">此数据源引用 **描述** 扩展数据类型 (EDT)。</span><span class="sxs-lookup"><span data-stu-id="43ff1-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="43ff1-130">接下来，定义 *计算字段* 类型的 **NumSeq** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="43ff1-131">此数据源包含表达式 `NUMSEQVALUE (AskNumSeq)`。</span><span class="sxs-lookup"><span data-stu-id="43ff1-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="43ff1-132">当调用 **NumSeq** 数据源时，它将返回通过在对话框中输入其代码在运行时指定的编号规则的新生成的值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="43ff1-133">为 **公司** 作用域类型请求编号规则。</span><span class="sxs-lookup"><span data-stu-id="43ff1-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="43ff1-134">公司代码由运行 ER 格式的上下文提供。</span><span class="sxs-lookup"><span data-stu-id="43ff1-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="43ff1-135">示例 2</span><span class="sxs-lookup"><span data-stu-id="43ff1-135">Example 2</span></span>

<span data-ttu-id="43ff1-136">以下数据源在模型映射中定义：</span><span class="sxs-lookup"><span data-stu-id="43ff1-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="43ff1-137">*表* 类型的 **LedgerParms** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="43ff1-138">此数据源引用 LedgerParameters 表。</span><span class="sxs-lookup"><span data-stu-id="43ff1-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="43ff1-139">*计算字段* 类型的 **NumSeq** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="43ff1-140">此数据源包含表达式 `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`。</span><span class="sxs-lookup"><span data-stu-id="43ff1-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="43ff1-141">在调用 **NumSeq** 数据源时，将返回在提供 ER 格式在其中运行的上下文的公司的总帐参数中配置的编号规则的新生成值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="43ff1-142">此编号规则唯一标识日记帐，并充当将交易记录链接在一起的批号。</span><span class="sxs-lookup"><span data-stu-id="43ff1-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="43ff1-143">示例 3</span><span class="sxs-lookup"><span data-stu-id="43ff1-143">Example 3</span></span>

<span data-ttu-id="43ff1-144">以下数据源在模型映射中定义：</span><span class="sxs-lookup"><span data-stu-id="43ff1-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="43ff1-145">Microsoft Dynamics 365 Finance *枚举* 类型的 **enumScope** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="43ff1-146">此数据源引用 **ERExpressionNumberSequenceScopeType** 枚举。</span><span class="sxs-lookup"><span data-stu-id="43ff1-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="43ff1-147">*计算字段* 类型的 **NumSeq** 数据源。</span><span class="sxs-lookup"><span data-stu-id="43ff1-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="43ff1-148">此数据源包含表达式 `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`。</span><span class="sxs-lookup"><span data-stu-id="43ff1-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="43ff1-149">在调用 **NumSeq** 数据源时，将返回为提供 ER 格式在其中运行的上下文的公司配置的 **Gene\_1** 编号规则的新生成值。</span><span class="sxs-lookup"><span data-stu-id="43ff1-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43ff1-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="43ff1-150">Additional resources</span></span>

[<span data-ttu-id="43ff1-151">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="43ff1-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]