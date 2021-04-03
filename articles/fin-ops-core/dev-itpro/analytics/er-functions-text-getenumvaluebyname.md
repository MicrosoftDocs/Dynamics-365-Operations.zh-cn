---
title: GETENUMVALUEBYNAME ER 函数
description: 本主题提供有关 GETENUMVALUEBYNAME 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570582"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="0c400-103">GETENUMVALUEBYNAME ER 函数</span><span class="sxs-lookup"><span data-stu-id="0c400-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c400-104">`GETENUMVALUEBYNAME` 函数通过使用指定为 *字符串* 值的枚举名称在指定的枚举数据源中搜索特定的 *枚举* 值。</span><span class="sxs-lookup"><span data-stu-id="0c400-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="0c400-105">如果找到 *枚举* 值，函数将返回此值。</span><span class="sxs-lookup"><span data-stu-id="0c400-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="0c400-106">否则，此函数将返回 **空** 枚举值。</span><span class="sxs-lookup"><span data-stu-id="0c400-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c400-107">语法</span><span class="sxs-lookup"><span data-stu-id="0c400-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="0c400-108">参数</span><span class="sxs-lookup"><span data-stu-id="0c400-108">Arguments</span></span>

<span data-ttu-id="0c400-109">`enumeration data source path`：*枚举*</span><span class="sxs-lookup"><span data-stu-id="0c400-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="0c400-110">下列枚举类型之一的数据源的有效路径：</span><span class="sxs-lookup"><span data-stu-id="0c400-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="0c400-111">电子申报 (ER) 模型枚举</span><span class="sxs-lookup"><span data-stu-id="0c400-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="0c400-112">ER 格式枚举</span><span class="sxs-lookup"><span data-stu-id="0c400-112">ER format enumeration</span></span>
- <span data-ttu-id="0c400-113">Microsoft Dynamics 365 Finance 枚举</span><span class="sxs-lookup"><span data-stu-id="0c400-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="0c400-114">`enumeration value text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0c400-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="0c400-115">代表单个枚举值的名称的字符串值。</span><span class="sxs-lookup"><span data-stu-id="0c400-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c400-116">返回值</span><span class="sxs-lookup"><span data-stu-id="0c400-116">Return values</span></span>

<span data-ttu-id="0c400-117">可空 *枚举*</span><span class="sxs-lookup"><span data-stu-id="0c400-117">Nullable *Enum*</span></span>

<span data-ttu-id="0c400-118">生成的枚举值。</span><span class="sxs-lookup"><span data-stu-id="0c400-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c400-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="0c400-119">Usage notes</span></span>

<span data-ttu-id="0c400-120">如果使用指定为 *字符串* 值的枚举值的名称未找到 *枚举* 值，不会引发异常。</span><span class="sxs-lookup"><span data-stu-id="0c400-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c400-121">示例 1</span><span class="sxs-lookup"><span data-stu-id="0c400-121">Example 1</span></span>

<span data-ttu-id="0c400-122">在下图中，数据模型中引入了 **ReportDirection** 枚举。</span><span class="sxs-lookup"><span data-stu-id="0c400-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="0c400-123">请注意，为枚举值定义标签。</span><span class="sxs-lookup"><span data-stu-id="0c400-123">Notice that labels are defined for the enumeration values.</span></span>

![数据模型枚举的可用值](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="0c400-125">下图显示以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="0c400-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="0c400-126">**$Direction** 数据源在 ER 报表中配置。</span><span class="sxs-lookup"><span data-stu-id="0c400-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="0c400-127">此数据源是根据 **ReportDirection** 模型枚举配置的。</span><span class="sxs-lookup"><span data-stu-id="0c400-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="0c400-128">`$IsArrivals` 表达式设计为将基于模型枚举的 **$Direction** 数据源用作此函数的参数。</span><span class="sxs-lookup"><span data-stu-id="0c400-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="0c400-129">此比较表达式的值为 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0c400-129">The value of this comparison expression is **TRUE**.</span></span>

![数据模型枚举的示例](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="0c400-131">示例 2</span><span class="sxs-lookup"><span data-stu-id="0c400-131">Example 2</span></span>

<span data-ttu-id="0c400-132">`GETENUMVALUEBYNAME` 和 [`LISTOFFIELDS`](er-functions-list-listoffields.md) 函数可让您作为文本值提取支持的枚举的值和标签。</span><span class="sxs-lookup"><span data-stu-id="0c400-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="0c400-133">（支持的枚举有应用程序枚举、数据模型枚举和格式枚举。）</span><span class="sxs-lookup"><span data-stu-id="0c400-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="0c400-134">在下图中，模型映射中引入了 **TransType** 数据源。</span><span class="sxs-lookup"><span data-stu-id="0c400-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="0c400-135">此数据源引用 **LedgerTransType** 应用程序枚举。</span><span class="sxs-lookup"><span data-stu-id="0c400-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![引用应用程序枚举的模型映射的数据源](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="0c400-137">下图显示了在模型映射中配置的 **TransTypeList** 数据源。</span><span class="sxs-lookup"><span data-stu-id="0c400-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="0c400-138">此数据源是根据 **TransType** 应用程序枚举配置的。</span><span class="sxs-lookup"><span data-stu-id="0c400-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="0c400-139">`LISTOFFIELDS` 函数用于将所有枚举值作为包含字段的记录列表返回。</span><span class="sxs-lookup"><span data-stu-id="0c400-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="0c400-140">这样，每个枚举值的详细信息都将公开。</span><span class="sxs-lookup"><span data-stu-id="0c400-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="0c400-141">将使用 `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` 表达式为 **TransTypeList** 数据源配置 **EnumValue** 字段。</span><span class="sxs-lookup"><span data-stu-id="0c400-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="0c400-142">此字段为此列表中的每个记录返回枚举值。</span><span class="sxs-lookup"><span data-stu-id="0c400-142">This field returns an enumeration value for every record in this list.</span></span>

![作为记录列表返回选定枚举的所有枚举值的模型映射的数据源](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="0c400-144">下图显示了在模型映射中配置的 **VendTrans** 数据源。</span><span class="sxs-lookup"><span data-stu-id="0c400-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="0c400-145">此数据源从 **VendTrans** 应用程序表返回供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="0c400-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="0c400-146">每个交易记录的分类帐类型由 **TransType** 字段的值定义。</span><span class="sxs-lookup"><span data-stu-id="0c400-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="0c400-147">将使用 `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` 表达式为 **VendTrans** 数据源配置 **TransTypeTitle** 字段。</span><span class="sxs-lookup"><span data-stu-id="0c400-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="0c400-148">此字段以文本形式返回当前交易记录的枚举值的标签（如果此枚举值可用）。</span><span class="sxs-lookup"><span data-stu-id="0c400-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="0c400-149">否则，将返回一个空字符串值。</span><span class="sxs-lookup"><span data-stu-id="0c400-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="0c400-150">**TransTypeTitle** 字段将绑定到数据模型的 **LedgerType** 字段，让此信息可以在使用该数据模型作为数据源的每个 ER 格式中使用。</span><span class="sxs-lookup"><span data-stu-id="0c400-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![返回供应商交易记录的模型映射的数据源](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="0c400-152">下图显示了如何使用[数据源调试器](er-debug-data-sources.md)测试配置的模型映射。</span><span class="sxs-lookup"><span data-stu-id="0c400-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![使用数据源调试器测试配置的模型映射](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="0c400-154">数据模型的 **LedgerType** 字段预期将公开交易记录类型的标签。</span><span class="sxs-lookup"><span data-stu-id="0c400-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="0c400-155">如果您计划将这种方法用于大量交易记录数据，则必须考虑执行性能。</span><span class="sxs-lookup"><span data-stu-id="0c400-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="0c400-156">有关详细信息，请参阅[跟踪 ER 格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="0c400-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c400-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="0c400-157">Additional resources</span></span>

[<span data-ttu-id="0c400-158">文本函数</span><span class="sxs-lookup"><span data-stu-id="0c400-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="0c400-159">跟踪电子申报格式的执行以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="0c400-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="0c400-160">LISTOFFIELDS ER 函数</span><span class="sxs-lookup"><span data-stu-id="0c400-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="0c400-161">FIRSTORNULL ER 函数</span><span class="sxs-lookup"><span data-stu-id="0c400-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="0c400-162">WHERE ER 函数</span><span class="sxs-lookup"><span data-stu-id="0c400-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]