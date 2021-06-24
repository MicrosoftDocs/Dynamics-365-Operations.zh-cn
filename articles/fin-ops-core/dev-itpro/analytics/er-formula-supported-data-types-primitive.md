---
title: 电子申报公式支持的原始数据类型
description: 本主题提供有关电子申报 (ER) 公式支持的原始数据类型的信息。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d5e6bb5e070ebbcdb7e99b1b70010acd5fca5ac
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224079"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a><span data-ttu-id="9b7da-103">电子申报公式支持的原始数据类型</span><span class="sxs-lookup"><span data-stu-id="9b7da-103">Supported primitive data types for Electronic reporting formulas</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b7da-104">本主题提供有关[电子申报 (ER)](general-electronic-reporting.md) 表达式支持的原始数据类型的信息。</span><span class="sxs-lookup"><span data-stu-id="9b7da-104">This topic provides information about the primitive data types that are supported in [Electronic reporting (ER)](general-electronic-reporting.md) expressions.</span></span> <span data-ttu-id="9b7da-105">下面是原始数据类型的列表：</span><span class="sxs-lookup"><span data-stu-id="9b7da-105">Here is a list of the primitive data types:</span></span>

- [<span data-ttu-id="9b7da-106">布尔</span><span class="sxs-lookup"><span data-stu-id="9b7da-106">boolean</span></span>](#boolean)
- [<span data-ttu-id="9b7da-107">日期</span><span class="sxs-lookup"><span data-stu-id="9b7da-107">date</span></span>](#date)
- [<span data-ttu-id="9b7da-108">日期/时间</span><span class="sxs-lookup"><span data-stu-id="9b7da-108">datetime</span></span>](#datetime)
- [<span data-ttu-id="9b7da-109">枚举</span><span class="sxs-lookup"><span data-stu-id="9b7da-109">enumeration</span></span>](#enumeration)
- [<span data-ttu-id="9b7da-110">guid</span><span class="sxs-lookup"><span data-stu-id="9b7da-110">guid</span></span>](#guid)
- [<span data-ttu-id="9b7da-111">整数</span><span class="sxs-lookup"><span data-stu-id="9b7da-111">integer</span></span>](#integer)
- [<span data-ttu-id="9b7da-112">int64</span><span class="sxs-lookup"><span data-stu-id="9b7da-112">int64</span></span>](#int64)
- [<span data-ttu-id="9b7da-113">实数</span><span class="sxs-lookup"><span data-stu-id="9b7da-113">real</span></span>](#real)
- [<span data-ttu-id="9b7da-114">字符串</span><span class="sxs-lookup"><span data-stu-id="9b7da-114">string</span></span>](#string)

## <a name="boolean"></a><a name="boolean"></a><span data-ttu-id="9b7da-115">布尔</span><span class="sxs-lookup"><span data-stu-id="9b7da-115">Boolean</span></span>

<span data-ttu-id="9b7da-116">*布尔* 原始数据类型包含评估为 *true* 或 *false* 的值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-116">The *boolean* primitive data type contains a value that is evaluated as either *true* or *false*.</span></span> <span data-ttu-id="9b7da-117">您可以在预计 *布尔* 表达式的情况下，使用保留的文本关键字 **True** 和 **False**。</span><span class="sxs-lookup"><span data-stu-id="9b7da-117">You can use the reserved literal keywords **True** and **False** wherever a *boolean* expression is expected.</span></span> <span data-ttu-id="9b7da-118">默认值为 *false*。</span><span class="sxs-lookup"><span data-stu-id="9b7da-118">The default value is *false*.</span></span>

<span data-ttu-id="9b7da-119">*布尔* 的内部表示为 *整数*。</span><span class="sxs-lookup"><span data-stu-id="9b7da-119">The internal representation of a *boolean* is an *integer*.</span></span> <span data-ttu-id="9b7da-120">*整数* 值 0（零）评估为 *false*，所有其他 *整数* 值评估为 *true*。</span><span class="sxs-lookup"><span data-stu-id="9b7da-120">The *integer* value 0 (zero) is evaluated as *false*, and all other *integer* values are evaluated as *true*.</span></span> <span data-ttu-id="9b7da-121">当您 [验证](general-electronic-reporting-formula-designer.md#TestFormula)在 [ER 公式设计器](er-advanced-formula-editor.md)中返回 *布尔* 的配置表达式时，如果表达式返回 *false*，测试结果窗格显示 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="9b7da-121">When you [validate](general-electronic-reporting-formula-designer.md#TestFormula) a configured expression that returns a *boolean* in the [ER formula designer](er-advanced-formula-editor.md), the test result pane presents *0* (zero) when an expression returns *false*.</span></span> <span data-ttu-id="9b7da-122">否则，测试结果窗格显示 *1*。</span><span class="sxs-lookup"><span data-stu-id="9b7da-122">Otherwise, the test result pane presents *1*.</span></span>

<span data-ttu-id="9b7da-123">*布尔* 没有隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-123">A *boolean* has no implicit conversions.</span></span> <span data-ttu-id="9b7da-124">但是，您可以使用 [TEXT](er-functions-text-text.md) 函数将 *布尔* 显式转换为 *字符串*。</span><span class="sxs-lookup"><span data-stu-id="9b7da-124">However, you can use the [TEXT](er-functions-text-text.md) function to explicitly converts a *boolean* to a *string*:</span></span>

- <span data-ttu-id="9b7da-125">*false* 值转换为文本字符串 **False**。</span><span class="sxs-lookup"><span data-stu-id="9b7da-125">The *false* value is converted to the text string **False**.</span></span>
- <span data-ttu-id="9b7da-126">*true* 值转换为文本字符串 **True**。</span><span class="sxs-lookup"><span data-stu-id="9b7da-126">The *true* value is converted to the text string **True**.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7da-127">此转换不依赖于提供的语言和文化[上下文](er-design-multilingual-reports.md)。</span><span class="sxs-lookup"><span data-stu-id="9b7da-127">This conversion doesn't depend on the provided language and culture [context](er-design-multilingual-reports.md).</span></span>

<span data-ttu-id="9b7da-128">比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *布尔* 数据类型一起使用的运算符类型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-128">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *boolean* data type.</span></span> <span data-ttu-id="9b7da-129">以下运算符可用于比较两个 *布尔* 值：\<\> 和 =。</span><span class="sxs-lookup"><span data-stu-id="9b7da-129">The following operators can be used to compare two *boolean* values: \<\> and =.</span></span>

## <a name="date"></a><a name="date"></a><span data-ttu-id="9b7da-130">日期</span><span class="sxs-lookup"><span data-stu-id="9b7da-130">Date</span></span>

<span data-ttu-id="9b7da-131">*日期* 原始数据类型包含日、月和年。</span><span class="sxs-lookup"><span data-stu-id="9b7da-131">The *date* primitive data type contains the day, month, and year.</span></span> <span data-ttu-id="9b7da-132">可以使用以下函数启动日期：</span><span class="sxs-lookup"><span data-stu-id="9b7da-132">Dates can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="9b7da-133">DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-133">DATEVALUE</span></span>](er-functions-datetime-datevalue.md)
- [<span data-ttu-id="9b7da-134">NULLDATE</span><span class="sxs-lookup"><span data-stu-id="9b7da-134">NULLDATE</span></span>](er-functions-datetime-nulldate.md)
- [<span data-ttu-id="9b7da-135">SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="9b7da-135">SESSIONTODAY</span></span>](er-functions-datetime-sessiontoday.md)
- [<span data-ttu-id="9b7da-136">TODAY</span><span class="sxs-lookup"><span data-stu-id="9b7da-136">TODAY</span></span>](er-functions-datetime-today.md)

<span data-ttu-id="9b7da-137">*日期* 数据类型可以保留 1900 年 1 月 1 日和 2154 年 12 月 31 日之间的日期。</span><span class="sxs-lookup"><span data-stu-id="9b7da-137">The *date* data type can hold dates between January 1, 1900, and December 31, 2154.</span></span> <span data-ttu-id="9b7da-138">默认值为 **null**，内部表示为 1900 年 1 月 1 日的日期。</span><span class="sxs-lookup"><span data-stu-id="9b7da-138">The default value is **null**, and the internal representation is the date January 1, 1900.</span></span>

<span data-ttu-id="9b7da-139">*数据* 没有隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-139">A *date* has no implicit conversions.</span></span> <span data-ttu-id="9b7da-140">但是，您可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-140">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="9b7da-141">DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-141">DATEFORMAT</span></span>](er-functions-datetime-dateformat.md)
- [<span data-ttu-id="9b7da-142">DATETODATETIME</span><span class="sxs-lookup"><span data-stu-id="9b7da-142">DATETODATETIME</span></span>](er-functions-datetime-datetodatetime.md)
- [<span data-ttu-id="9b7da-143">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-143">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="9b7da-144">[ADDDAYS](er-functions-datetime-adddays.md) 函数可让您从日期中添加和减去天数。</span><span class="sxs-lookup"><span data-stu-id="9b7da-144">The [ADDDAYS](er-functions-datetime-adddays.md) function lets you add and subtract days from dates.</span></span> <span data-ttu-id="9b7da-145">通过这种方式，您可以将特定天数的日期移动到将来和过去。</span><span class="sxs-lookup"><span data-stu-id="9b7da-145">In this way, you can move the date a specific number of days into the future and the past.</span></span> <span data-ttu-id="9b7da-146">[DAYS](er-functions-datetime-days.md) 函数可让您将日期相互减去并计算天数差异。</span><span class="sxs-lookup"><span data-stu-id="9b7da-146">The [DAYS](er-functions-datetime-days.md) function lets you subtract dates from each other and calculate the difference in days.</span></span> <span data-ttu-id="9b7da-147">有关转换 *日期* 值的详细信息，请参阅[日期和时间类别中的 ER 函数列表](er-functions-category-datetime.md)。</span><span class="sxs-lookup"><span data-stu-id="9b7da-147">For more information about the transformation of *date* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="9b7da-148">比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *日期* 数据类型一起使用的运算符类型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-148">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *date* data type.</span></span> <span data-ttu-id="9b7da-149">以下运算符可用于比较两个 *日期* 值：\<\>、\<, \<=, =, \> 和 \>=。</span><span class="sxs-lookup"><span data-stu-id="9b7da-149">The following operators can be used to compare two *date* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="datetime"></a><a name="datetime"></a><span data-ttu-id="9b7da-150">DateTime</span><span class="sxs-lookup"><span data-stu-id="9b7da-150">Datetime</span></span>

<span data-ttu-id="9b7da-151">*日期/时间* 原始数据类型结合 *日期* 类型和一个表示自午夜以来经过的时间的值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-151">The *datetime* primitive data type combines the *date* type and a value that represents the time that has passed since midnight.</span></span> <span data-ttu-id="9b7da-152">时间以小时、分钟、秒和秒的分数表示。</span><span class="sxs-lookup"><span data-stu-id="9b7da-152">The time is expressed in hours, minutes, seconds, and fractions of a second.</span></span> <span data-ttu-id="9b7da-153">*日期/时间* 值还保留与时区相关的信息。</span><span class="sxs-lookup"><span data-stu-id="9b7da-153">A *datetime* value also holds information about the time zone.</span></span>

<span data-ttu-id="9b7da-154">*日期/时间* 数据类型可以保留 1900 年 1 月 1 日（1900-01-01T00:00:00.0000000+00:00，采用往返[格式](/dotnet/standard/base-types/standard-date-and-time-format-strings)）和 2154 年 12 月 31 日（2154/12/31T11:59:59.9999999+00:00，采用往返格式）之间的日期。</span><span class="sxs-lookup"><span data-stu-id="9b7da-154">The *datetime* data type can hold dates between January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip [format](/dotnet/standard/base-types/standard-date-and-time-format-strings)) and December 31, 2154 (2154/12/31T11:59:59.9999999+00:00 in the round-trip format).</span></span> <span data-ttu-id="9b7da-155">*日期/时间* 的最小时间单位是千万分之一秒。</span><span class="sxs-lookup"><span data-stu-id="9b7da-155">The smallest unit of time in a *datetime* is one ten millionth of a second.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7da-156">当针对小时使用 **hh** [说明符](/dotnet/standard/base-types/standard-date-and-time-format-strings)时，高于 12:59:59:9999999 的时间值不能解释为有效时间。</span><span class="sxs-lookup"><span data-stu-id="9b7da-156">When the **hh** [specifier](/dotnet/standard/base-types/standard-date-and-time-format-strings) is used for hours, time values above 12:59:59:9999999 can't be interpreted as valid times.</span></span>
>
> <span data-ttu-id="9b7da-157">当针对小时使用 **HH** 说明符时，高于 23:59:59:9999999 的时间值不能解释为有效时间。</span><span class="sxs-lookup"><span data-stu-id="9b7da-157">When the **HH** specifier is used for hours, time values above 23:59:59:9999999 can't be interpreted as valid times.</span></span>

<span data-ttu-id="9b7da-158">默认值为 **null**，内部表示为 1900 年 1 月 1 日的日期（1900-01-01T00:00:00.0000000+00:00，采用往返格式）。</span><span class="sxs-lookup"><span data-stu-id="9b7da-158">The default value is **null**, and the internal representation is the date January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip format).</span></span>

<span data-ttu-id="9b7da-159">可以使用以下函数启动日期/时间：</span><span class="sxs-lookup"><span data-stu-id="9b7da-159">Datetimes can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="9b7da-160">DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-160">DATETIMEVALUE</span></span>](er-functions-datetime-datetimevalue.md)
- [<span data-ttu-id="9b7da-161">NULNULLDATETIMELDATE</span><span class="sxs-lookup"><span data-stu-id="9b7da-161">NULNULLDATETIMELDATE</span></span>](er-functions-datetime-nulldatetime.md)
- [<span data-ttu-id="9b7da-162">SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="9b7da-162">SESSIONNOW</span></span>](er-functions-datetime-sessionnow.md)
- [<span data-ttu-id="9b7da-163">NOW</span><span class="sxs-lookup"><span data-stu-id="9b7da-163">NOW</span></span>](er-functions-datetime-now.md)

<span data-ttu-id="9b7da-164">*日期/时间* 没有隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-164">A *datetime* has no implicit conversions.</span></span> <span data-ttu-id="9b7da-165">但是，您可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-165">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="9b7da-166">DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-166">DATETIMEFORMAT</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="9b7da-167">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-167">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="9b7da-168">有关转换 *日期/时间* 值的详细信息，请参阅[日期和时间类别中的 ER 函数列表](er-functions-category-datetime.md)。</span><span class="sxs-lookup"><span data-stu-id="9b7da-168">For more information about the transformation of *datetime* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="9b7da-169">比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *日期/时间* 数据类型一起使用的运算符类型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-169">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *datetime* data type.</span></span> <span data-ttu-id="9b7da-170">以下运算符可用于比较两个 *日期/时间* 值：\<\>、\<, \<=, =, \> 和 \>=。</span><span class="sxs-lookup"><span data-stu-id="9b7da-170">The following operators can be used to compare two *datetime* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="enumeration"></a><a name="enumeration"></a><span data-ttu-id="9b7da-171">枚举</span><span class="sxs-lookup"><span data-stu-id="9b7da-171">Enumeration</span></span>

<span data-ttu-id="9b7da-172">*枚举* 原始数据类型是文本的列表。</span><span class="sxs-lookup"><span data-stu-id="9b7da-172">The *enumeration* primitive data type is a list of literals.</span></span> <span data-ttu-id="9b7da-173">您可以使用在应用程序[源代码](../dev-ref/xpp-data-primitive.md#enum)中定义的枚举。</span><span class="sxs-lookup"><span data-stu-id="9b7da-173">You can use enumerations that are defined in the application [source code](../dev-ref/xpp-data-primitive.md#enum).</span></span> <span data-ttu-id="9b7da-174">您还可以在 ER [数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components)和 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件中引入自己的枚举。</span><span class="sxs-lookup"><span data-stu-id="9b7da-174">You can also introduce your own enumerations in the ER [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) and ER [format](general-electronic-reporting.md#FormatComponentOutbound) components.</span></span>

<span data-ttu-id="9b7da-175">应用程序 *枚举* 可用于任何 ER 模型映射和 ER 格式的表达式中。</span><span class="sxs-lookup"><span data-stu-id="9b7da-175">An application *enumeration* can be used in expressions of any ER model mapping and ER format.</span></span>

<span data-ttu-id="9b7da-176">下图显示了您可以如何将 **CustVendCorrectiveReasonCode** 模型枚举添加到可编辑的 ER 数据模型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-176">The following illustration shows how you can add the **CustVendCorrectiveReasonCode** model enumeration to the editable ER data model.</span></span>

<span data-ttu-id="9b7da-177">[![在 ER 数据模型设计器中配置模型枚举](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span><span class="sxs-lookup"><span data-stu-id="9b7da-177">[![Configuring a model enumeration in the ER data model designer](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span></span>

<span data-ttu-id="9b7da-178">模型 *枚举* 可用于已在引入了 *枚举* 的数据模型下创建的任何 ER 模型映射和 ER 格式的表达式中。</span><span class="sxs-lookup"><span data-stu-id="9b7da-178">A model *enumeration* can be used in expressions of any ER model mapping and ER format that were created under a data model where the *enumeration* was introduced.</span></span>

<span data-ttu-id="9b7da-179">下图显示了您可以如何将 **Natura 冲销费用子类别的列表** 格式枚举添加到可编辑的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b7da-179">The following illustration shows how you can add the **List of Natura reverse charge subcategories** format enumeration to the editable ER format.</span></span>

<span data-ttu-id="9b7da-180">[![在 ER 格式设计器中配置格式枚举](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span><span class="sxs-lookup"><span data-stu-id="9b7da-180">[![Configuring a format enumeration in the ER format designer](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span></span>

<span data-ttu-id="9b7da-181">格式 *枚举* 仅可用于引入了 *枚举* 的 ER 格式的表达式中。</span><span class="sxs-lookup"><span data-stu-id="9b7da-181">A format *enumeration* can be used only in expressions of the ER format where the *enumeration* was introduced.</span></span>

<span data-ttu-id="9b7da-182">您必须使用适当类型的 ER 数据源，将特定枚举作为常量或作为值（运行 ER 解决方案的用户在运行时在对话框中定义）引入到配置的 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="9b7da-182">You must use the appropriate type of ER data sources to bring a specific enumeration to a configured ER component as a constant or as a value that the user who is running an ER solution defined in the dialog box at runtime.</span></span>

- <span data-ttu-id="9b7da-183">可以使用 **Dynamics 365 for Operations \ 枚举** 和 **常规 \ 用户输入参数** 数据源访问应用程序枚举。</span><span class="sxs-lookup"><span data-stu-id="9b7da-183">Application enumerations can be accessed by using the **Dynamics 365 for Operations \ Enumeration** and **General \ User input parameters** data sources.</span></span> <span data-ttu-id="9b7da-184">下图显示了您可以如何将引用 **NoYes** 应用程序枚举的 **appenumNoYes** 和 **uipNoYes** 数据源添加到可编辑的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b7da-184">The following illustration shows how you can add to the editable ER format the **appenumNoYes** and **uipNoYes** data sources that refer to the **NoYes** application enumeration.</span></span>

    <span data-ttu-id="9b7da-185">[![在 ER 格式设计器中添加应用程序枚举数据源](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span><span class="sxs-lookup"><span data-stu-id="9b7da-185">[![Adding application enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span></span>

- <span data-ttu-id="9b7da-186">可以使用 **数据模型 \ 枚举** 和 **数据模型 \ 枚举用户输入参数** 数据源访问数据模型枚举。</span><span class="sxs-lookup"><span data-stu-id="9b7da-186">Data model enumerations can be accessed by using the **Data model \ Enumeration** and **Data model \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="9b7da-187">下图显示了您可以如何将引用 **CustVendCorrectiveReasonCode** 数据模型枚举的 **CustVendCorrectiveReasonCode** 数据源添加到可编辑的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b7da-187">The following illustration shows how you can add to the editable ER format the **CustVendCorrectiveReasonCode** data source that refers to the **CustVendCorrectiveReasonCode** data model enumeration.</span></span>

    <span data-ttu-id="9b7da-188">[![在 ER 格式设计器中添加模型枚举数据源](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span><span class="sxs-lookup"><span data-stu-id="9b7da-188">[![Adding model enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span></span>

- <span data-ttu-id="9b7da-189">可以使用 **格式 \ 枚举** 和 **格式 \ 枚举用户输入参数** 数据源访问格式枚举。</span><span class="sxs-lookup"><span data-stu-id="9b7da-189">Format enumerations can be accessed by using the **Format \ Enumeration** and **Format \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="9b7da-190">下图显示了您可以如何将引用 **Natura 冲销费用子类别** 格式枚举的 **NaturaReverseCharge** 数据源添加到可编辑的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="9b7da-190">The following illustration shows how you can add to the editable ER format the **NaturaReverseCharge** data source that refers to the **Natura reverse charge subcategories** format enumeration.</span></span>

    <span data-ttu-id="9b7da-191">[![在 ER 格式设计器中添加格式枚举数据源](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span><span class="sxs-lookup"><span data-stu-id="9b7da-191">[![Adding format enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span></span>

<span data-ttu-id="9b7da-192">*枚举* 没有隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-192">An *enumeration* has no implicit conversions.</span></span> <span data-ttu-id="9b7da-193">但是，您可以使用 [TEXT](er-functions-text-text.md) 转换函数将 *枚举* 转换为文本字符串。</span><span class="sxs-lookup"><span data-stu-id="9b7da-193">However, you can use the [TEXT](er-functions-text-text.md) conversion function to convert an *enumeration* to a text string.</span></span> <span data-ttu-id="9b7da-194">此转换与语言无关。</span><span class="sxs-lookup"><span data-stu-id="9b7da-194">This conversion isn't language dependent.</span></span> <span data-ttu-id="9b7da-195">若要了解您可以如何将 *枚举* 值与特定于语言的相应标签相关联，请参阅 [LISTOFFIELDS](er-functions-list-listoffields.md) 和 [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) 函数的使用示例。</span><span class="sxs-lookup"><span data-stu-id="9b7da-195">To learn how you can associate an *enumeration* value with the appropriate language-specific labels, see the usage examples for the [LISTOFFIELDS](er-functions-list-listoffields.md) and [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) functions.</span></span>

<span data-ttu-id="9b7da-196">比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *枚举* 数据类型一起使用的运算符类型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-196">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *enumeration* data type.</span></span> <span data-ttu-id="9b7da-197">以下运算符可用于比较两个 *枚举* 值：\<\> 和 =。</span><span class="sxs-lookup"><span data-stu-id="9b7da-197">The following operators can be used to compare two *enumeration* values: \<\> and =.</span></span>

## <a name="guid"></a><a name="guid"></a><span data-ttu-id="9b7da-198">Guid</span><span class="sxs-lookup"><span data-stu-id="9b7da-198">Guid</span></span>

<span data-ttu-id="9b7da-199">*guid* 原始数据类型保留全局唯一标识符 (GUID) 值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-199">The *guid* primitive data type holds a globally unique identifier (GUID) value.</span></span> <span data-ttu-id="9b7da-200">GUID 是可用于所有计算机和网络的值，只需要唯一标识符即可。</span><span class="sxs-lookup"><span data-stu-id="9b7da-200">A GUID is a value that can be used across all computers and networks, wherever a unique identifier is required.</span></span> <span data-ttu-id="9b7da-201">该数字不太可能重复。</span><span class="sxs-lookup"><span data-stu-id="9b7da-201">It's unlikely that the number will be duplicated.</span></span> <span data-ttu-id="9b7da-202">有效的 GUID 满足以下所有规范：</span><span class="sxs-lookup"><span data-stu-id="9b7da-202">A valid GUID meets all the following specifications:</span></span>

- <span data-ttu-id="9b7da-203">必须有 32 个十六进制数字。</span><span class="sxs-lookup"><span data-stu-id="9b7da-203">There must be 32 hexadecimal digits.</span></span>
- <span data-ttu-id="9b7da-204">此外，必须在以下位置嵌入四个破折号：8-4-4-4-12。</span><span class="sxs-lookup"><span data-stu-id="9b7da-204">In addition, there must be four dash characters that are embedded at the following locations: 8-4-4-4-12.</span></span>
- <span data-ttu-id="9b7da-205">此外，可以选择在字符串的开头和结尾添加大括号 \{\}。</span><span class="sxs-lookup"><span data-stu-id="9b7da-205">In addition, optional braces \{\} can be added at the beginning and end of the string.</span></span> <span data-ttu-id="9b7da-206">例如，**\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** 和 **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** 都是有效的 GUID 字符串。</span><span class="sxs-lookup"><span data-stu-id="9b7da-206">For example, both **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** and **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** are valid GUID strings.</span></span>
- <span data-ttu-id="9b7da-207">因此，总共必须有 36 或 38 个字符，具体取决于是否添加大括号。</span><span class="sxs-lookup"><span data-stu-id="9b7da-207">Therefore, there must be a total of 36 or 38 characters, depending on whether braces are added.</span></span>
- <span data-ttu-id="9b7da-208">用作十六进制数字的字母可以是大写 (A–F)、小写 (a–f) 或大小写混合。</span><span class="sxs-lookup"><span data-stu-id="9b7da-208">The letters that are used as hexadecimal digits can be uppercase (A–F), lowercase (a–f), or mixed.</span></span>

<span data-ttu-id="9b7da-209">可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-209">The following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="9b7da-210">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-210">GUIDVALUE</span></span>](er-functions-text-guidvalue.md)
- [<span data-ttu-id="9b7da-211">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-211">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="9b7da-212">比较 [运算符](er-formula-language.md#Operators)是唯一可以与 *guid* 数据类型一起使用的运算符类型。</span><span class="sxs-lookup"><span data-stu-id="9b7da-212">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *guid* data type.</span></span> <span data-ttu-id="9b7da-213">以下运算符可用于比较两个 *guid* 值：\<\> 和 =。</span><span class="sxs-lookup"><span data-stu-id="9b7da-213">The following operators can be used to compare two *guid* values: \<\> and =.</span></span>

## <a name="integer"></a><a name="integer"></a><span data-ttu-id="9b7da-214">整数</span><span class="sxs-lookup"><span data-stu-id="9b7da-214">Integer</span></span>

<span data-ttu-id="9b7da-215">*整数* 原始数据类型表示没有小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="9b7da-215">The *integer* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="9b7da-216">整数用作重复语句中的控制变量或记录列表中的索引。</span><span class="sxs-lookup"><span data-stu-id="9b7da-216">Integers are used as control variables in repetitive statements or as indexes in record lists.</span></span>

<span data-ttu-id="9b7da-217">*整数* 文本是直接在 ER [表达式](general-electronic-reporting-formula-designer.md#formula-designer-overview)（公式）中输入的整数，例如 **12345**。</span><span class="sxs-lookup"><span data-stu-id="9b7da-217">An *integer* literal is the integer as it's entered directly in an ER [expression](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formula), such as **12345**.</span></span> <span data-ttu-id="9b7da-218">*整数* 是 32 位宽。</span><span class="sxs-lookup"><span data-stu-id="9b7da-218">An *integer* is 32-bits wide.</span></span> <span data-ttu-id="9b7da-219">默认值为 **0**，内部表示是一个长数字。</span><span class="sxs-lookup"><span data-stu-id="9b7da-219">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="9b7da-220">*整数* 会自动转换为 *实数*.</span><span class="sxs-lookup"><span data-stu-id="9b7da-220">An *integer* is automatically converted to a *real*.</span></span>

<span data-ttu-id="9b7da-221">此外，可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-221">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="9b7da-222">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-222">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="9b7da-223">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-223">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="9b7da-224">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-224">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="9b7da-225">*整数* 的范围为 \[-2,147,483,647 : 2,147,483,647\]。</span><span class="sxs-lookup"><span data-stu-id="9b7da-225">The range of an *integer* is \[-2,147,483,647 : 2,147,483,647\].</span></span> <span data-ttu-id="9b7da-226">此范围的所有整数都可用作文本。</span><span class="sxs-lookup"><span data-stu-id="9b7da-226">All integers of this range can be used as literals.</span></span>

<span data-ttu-id="9b7da-227">所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *整数* 数据类型一起使用。</span><span class="sxs-lookup"><span data-stu-id="9b7da-227">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *integer* data type.</span></span>

## <a name="int64"></a><a name="int64"></a><span data-ttu-id="9b7da-228">Int64</span><span class="sxs-lookup"><span data-stu-id="9b7da-228">Int64</span></span>

<span data-ttu-id="9b7da-229">*int64* 原始数据类型表示没有小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="9b7da-229">The *int64* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="9b7da-230">*Int64* 值用作重复语句中的控制变量或记录标识符。</span><span class="sxs-lookup"><span data-stu-id="9b7da-230">*Int64* values are used as control variables in repetitive statements or as record identifiers.</span></span>

<span data-ttu-id="9b7da-231">*int64* 是 64 位宽。</span><span class="sxs-lookup"><span data-stu-id="9b7da-231">An *int64* is 64-bits wide.</span></span> <span data-ttu-id="9b7da-232">默认值为 **0**，内部表示是一个长数字。</span><span class="sxs-lookup"><span data-stu-id="9b7da-232">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="9b7da-233">*int64* 会自动转换为 *实数*.</span><span class="sxs-lookup"><span data-stu-id="9b7da-233">An *int64* is automatically converted to a *real*.</span></span>

<span data-ttu-id="9b7da-234">此外，可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-234">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="9b7da-235">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-235">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="9b7da-236">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-236">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="9b7da-237">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-237">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="9b7da-238">*int64* 的范围为 \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\]。</span><span class="sxs-lookup"><span data-stu-id="9b7da-238">The range of an *int64* is \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].</span></span>

<span data-ttu-id="9b7da-239">所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *int64* 数据类型一起使用。</span><span class="sxs-lookup"><span data-stu-id="9b7da-239">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *int64* data type.</span></span>

## <a name="real"></a><a name="real"></a><span data-ttu-id="9b7da-240">实数</span><span class="sxs-lookup"><span data-stu-id="9b7da-240">Real</span></span>

<span data-ttu-id="9b7da-241">除了整数之外，*实数* 原始数据类型也可以保留十进制值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-241">The *real* primitive data type can hold decimal values in addition to integers.</span></span> <span data-ttu-id="9b7da-242">您可以在预计 *实数* 的任何位置使用十进制文本。</span><span class="sxs-lookup"><span data-stu-id="9b7da-242">You can use decimal literals anywhere that a *real* is expected.</span></span> <span data-ttu-id="9b7da-243">十进制文本是在代码中直接输入的十进制，例如 **2.19**。</span><span class="sxs-lookup"><span data-stu-id="9b7da-243">A decimal literal is the decimal as it's entered directly in code, such as **2.19**.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7da-244">在 ER 表达式中，句点 (.) 始终用作十进制分隔符。</span><span class="sxs-lookup"><span data-stu-id="9b7da-244">In ER expressions, a period (.) is always used as the decimal separator.</span></span>

<span data-ttu-id="9b7da-245">实数可用于所有表达式，并且可与比较运算符和算术运算符一起使用。</span><span class="sxs-lookup"><span data-stu-id="9b7da-245">Reals can be used in all expressions, and they can be used with both comparison and arithmetic operators.</span></span> <span data-ttu-id="9b7da-246">*实数* 具有 16 位有效数字的精度。</span><span class="sxs-lookup"><span data-stu-id="9b7da-246">A *real* has a precision of 16 significant digits.</span></span> <span data-ttu-id="9b7da-247">*实数* 的默认值为 **0.0**，内部表示为二进制编码数字 (BCD)。</span><span class="sxs-lookup"><span data-stu-id="9b7da-247">The default value for a *real* is **0.0**, and the internal representation is a binary-coded digital (BCD) number.</span></span> <span data-ttu-id="9b7da-248">BCD 编码可以精确表示 0.1 的倍数的值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-248">The BCD encoding enables exact representations of values that are multiples of 0.1.</span></span> <span data-ttu-id="9b7da-249">*实数* 变量的范围为 -(10)<sup>127</sup> 到 (10)<sup>127</sup>。</span><span class="sxs-lookup"><span data-stu-id="9b7da-249">The range of a *real* variable is -(10)<sup>127</sup> through (10)<sup>127</sup>.</span></span> <span data-ttu-id="9b7da-250">在 ER 表达式中，此范围内的所有实数都可以用作文本。</span><span class="sxs-lookup"><span data-stu-id="9b7da-250">All reals in this range can be used as literals in ER expressions.</span></span>

<span data-ttu-id="9b7da-251">*实数* 没有隐式转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-251">A *real* has no implicit conversions.</span></span> <span data-ttu-id="9b7da-252">但是，您可以使用以下函数显式将 *实数* 转换为其他数据类型，并将其他数据类型转换为 *实数*：</span><span class="sxs-lookup"><span data-stu-id="9b7da-252">However, you can use the following functions to explicitly convert a *real* to other data types and other data types to a *real*:</span></span>

- [<span data-ttu-id="9b7da-253">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-253">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="9b7da-254">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-254">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="9b7da-255">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-255">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="9b7da-256">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-256">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="9b7da-257">VALUE</span><span class="sxs-lookup"><span data-stu-id="9b7da-257">VALUE</span></span>](er-functions-conversion-value.md)

<span data-ttu-id="9b7da-258">所有比较和数学 [运算符](er-formula-language.md#Operators)都可以与 *实数* 数据类型一起使用。</span><span class="sxs-lookup"><span data-stu-id="9b7da-258">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *real* data type.</span></span>

## <a name="string"></a><a name="string"></a><span data-ttu-id="9b7da-259">字符串</span><span class="sxs-lookup"><span data-stu-id="9b7da-259">String</span></span>

<span data-ttu-id="9b7da-260">*字符串* 原始数据类型表示用作文本、帐号、地址和电话号码的字符串序列。</span><span class="sxs-lookup"><span data-stu-id="9b7da-260">The *string* primitive data type represents a sequence of characters that are used as texts, account numbers, addresses, and telephone numbers.</span></span>

<span data-ttu-id="9b7da-261">*字符串* 文本是字符，用双引号 ("") 引起来。</span><span class="sxs-lookup"><span data-stu-id="9b7da-261">*String* literals are characters that are enclosed in quotation marks ("").</span></span> <span data-ttu-id="9b7da-262">可以在 ER 表达式中预计 *字符串* 值的任何位置使用 *字符串* 文本。</span><span class="sxs-lookup"><span data-stu-id="9b7da-262">*String* literals can be used wherever *string* values are expected in ER expressions.</span></span> <span data-ttu-id="9b7da-263">您可以在逻辑表达式中使用字符串，例如比较。</span><span class="sxs-lookup"><span data-stu-id="9b7da-263">You can use strings in logical expressions, such as comparisons.</span></span> <span data-ttu-id="9b7da-264">还可以使用 **\&** 运算符或 [CONCATENATE](er-functions-text-concatenate.md) 函数串联 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="9b7da-264">You can also concatenate *string* values by using the **\&** operator or the [CONCATENATE](er-functions-text-concatenate.md) function.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7da-265">如果串联两个 *字符串* 值，并且想要生成的 *字符串* 跨越多行，请在值之间使用换行符分隔符。</span><span class="sxs-lookup"><span data-stu-id="9b7da-265">If you concatenate two *string* values, and you want the resulting *string* to span more than one line, use the line break separator between the values.</span></span> <span data-ttu-id="9b7da-266">对于 TEXT 输出，此分隔符可以是使用 [CHAR](er-functions-text-char.md)(10) 或 CHAR(13) 表达式生成的字符。</span><span class="sxs-lookup"><span data-stu-id="9b7da-266">For the TEXT output, this separator can be a character that is generated by using the [CHAR](er-functions-text-char.md)(10) or CHAR(13) expression.</span></span> <span data-ttu-id="9b7da-267">对于 HTML，它可以是 **\<br\>** 标记。</span><span class="sxs-lookup"><span data-stu-id="9b7da-267">For HTML, it can be the **\<br\>** tag.</span></span>

<span data-ttu-id="9b7da-268">*字符串* 的默认值为没有字符的空白文本字符串，内部表示为字符列表。</span><span class="sxs-lookup"><span data-stu-id="9b7da-268">The default value for a *string* is a blank text string that has no characters, and the internal representation is a list of characters.</span></span>

<span data-ttu-id="9b7da-269">字符串没有自动转换。</span><span class="sxs-lookup"><span data-stu-id="9b7da-269">There are no automatic conversions for strings.</span></span> <span data-ttu-id="9b7da-270">但是，可以使用以下显式转换函数：</span><span class="sxs-lookup"><span data-stu-id="9b7da-270">However, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="9b7da-271">CHAR</span><span class="sxs-lookup"><span data-stu-id="9b7da-271">CHAR</span></span>](er-functions-text-char.md)
- [<span data-ttu-id="9b7da-272">FORMAT</span><span class="sxs-lookup"><span data-stu-id="9b7da-272">FORMAT</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="9b7da-273">LEFT</span><span class="sxs-lookup"><span data-stu-id="9b7da-273">LEFT</span></span>](er-functions-text-left.md)
- [<span data-ttu-id="9b7da-274">LEN</span><span class="sxs-lookup"><span data-stu-id="9b7da-274">LEN</span></span>](er-functions-text-len.md)
- [<span data-ttu-id="9b7da-275">MID</span><span class="sxs-lookup"><span data-stu-id="9b7da-275">MID</span></span>](er-functions-text-mid.md)
- [<span data-ttu-id="9b7da-276">PADLEFT</span><span class="sxs-lookup"><span data-stu-id="9b7da-276">PADLEFT</span></span>](er-functions-text-padleft.md)
- [<span data-ttu-id="9b7da-277">REPLACE</span><span class="sxs-lookup"><span data-stu-id="9b7da-277">REPLACE</span></span>](er-functions-text-replace.md)
- [<span data-ttu-id="9b7da-278">RIGHT</span><span class="sxs-lookup"><span data-stu-id="9b7da-278">RIGHT</span></span>](er-functions-text-right.md)
- [<span data-ttu-id="9b7da-279">TEXT</span><span class="sxs-lookup"><span data-stu-id="9b7da-279">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="9b7da-280">TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="9b7da-280">TRANSLATE</span></span>](er-functions-text-translate.md)
- [<span data-ttu-id="9b7da-281">TRIM</span><span class="sxs-lookup"><span data-stu-id="9b7da-281">TRIM</span></span>](er-functions-text-trim.md)
- [<span data-ttu-id="9b7da-282">UPPER</span><span class="sxs-lookup"><span data-stu-id="9b7da-282">UPPER</span></span>](er-functions-text-upper.md)

<span data-ttu-id="9b7da-283">有关转换 *字符串* 值的详细信息，请参阅[文本类别的 ER 函数列表](er-functions-category-text.md)。</span><span class="sxs-lookup"><span data-stu-id="9b7da-283">For more about the transformation of *string* values, see [List of ER functions of the text category](er-functions-category-text.md).</span></span>

<span data-ttu-id="9b7da-284">*字符串* 可以保留无限数量的字符。</span><span class="sxs-lookup"><span data-stu-id="9b7da-284">A *string* can hold an indefinite number of characters.</span></span>

<span data-ttu-id="9b7da-285">所有比较 [运算符](er-formula-language.md#Operators)都可以与 *字符串* 数据类型一起使用。</span><span class="sxs-lookup"><span data-stu-id="9b7da-285">All comparison [operators](er-formula-language.md#Operators) can be used with the *string* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b7da-286">其他资源</span><span class="sxs-lookup"><span data-stu-id="9b7da-286">Additional resources</span></span>

- [<span data-ttu-id="9b7da-287">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="9b7da-287">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9b7da-288">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="9b7da-288">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="9b7da-289">支持的复合数据类型</span><span class="sxs-lookup"><span data-stu-id="9b7da-289">Supported composite data types</span></span>](er-formula-supported-data-types-composite.md)
