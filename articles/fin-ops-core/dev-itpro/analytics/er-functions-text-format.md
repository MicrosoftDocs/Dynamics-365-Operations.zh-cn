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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09efeb6b5d8bd2ea452dbf7a9ddaeec2ab75c92
ms.sourcegitcommit: 0455a024185f79ecb82df61e6d994bd71dee5c10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2020
ms.locfileid: "2974284"
---
# <span data-ttu-id="a1a79-103"><a name="FORMAT">FORMAT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="a1a79-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1a79-104">通过使用第 *N* 个参数替换出现的所有 **%N** 设定指定字符串的格式后，`FORMAT` 函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="a1a79-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a79-105">语法</span><span class="sxs-lookup"><span data-stu-id="a1a79-105">Syntax</span></span>

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="a1a79-106">参数</span><span class="sxs-lookup"><span data-stu-id="a1a79-106">Arguments</span></span>

<span data-ttu-id="a1a79-107">`string`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a1a79-107">`string`: *String*</span></span>

<span data-ttu-id="a1a79-108">对必须设定格式的*字符串*类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="a1a79-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="a1a79-109">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="a1a79-109">This argument is required.</span></span>

<span data-ttu-id="a1a79-110">`argument 1`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a1a79-110">`argument 1`: *String*</span></span>

<span data-ttu-id="a1a79-111">第一个参数，用于替换出现的 **%1**。</span><span class="sxs-lookup"><span data-stu-id="a1a79-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="a1a79-112">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="a1a79-112">This argument is required.</span></span>

<span data-ttu-id="a1a79-113">`argument N`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a1a79-113">`argument N`: *String*</span></span>

<span data-ttu-id="a1a79-114">第 *N* 个参数，用于替换出现的 **%2**、**%3**，依此类推。</span><span class="sxs-lookup"><span data-stu-id="a1a79-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="a1a79-115">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="a1a79-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a1a79-116">返回值</span><span class="sxs-lookup"><span data-stu-id="a1a79-116">Return values</span></span>

<span data-ttu-id="a1a79-117">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a1a79-117">*String*</span></span>

<span data-ttu-id="a1a79-118">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="a1a79-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a1a79-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="a1a79-119">Usage notes</span></span>

<span data-ttu-id="a1a79-120">如果参数不是为参量提供，则参量在字符串中返回为 **"%N"**。</span><span class="sxs-lookup"><span data-stu-id="a1a79-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="a1a79-121">对于*实数*类型的值，默认字符串转换被限制为两位小数。</span><span class="sxs-lookup"><span data-stu-id="a1a79-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="a1a79-122">示例</span><span class="sxs-lookup"><span data-stu-id="a1a79-122">Example</span></span>

<span data-ttu-id="a1a79-123">在下图中，**PaymentModel** 数据源使用**客户**组件返回客户记录列表。</span><span class="sxs-lookup"><span data-stu-id="a1a79-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="a1a79-124">它使用 **ProcessingDate** 字段返回处理日期值。</span><span class="sxs-lookup"><span data-stu-id="a1a79-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="a1a79-125">在指定用于为所选客户生成电子文件的电子申报 (ER) 格式中，**PaymentModel** 被选择为数据源并控制流程。</span><span class="sxs-lookup"><span data-stu-id="a1a79-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="a1a79-126">如果所选客户在处理报表的日期停止，将引发异常以通知用户。</span><span class="sxs-lookup"><span data-stu-id="a1a79-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="a1a79-127">为此类处理控制设计的配方可以使用以下资源：</span><span class="sxs-lookup"><span data-stu-id="a1a79-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="a1a79-128">标签 SYS70894，具有以下文本：</span><span class="sxs-lookup"><span data-stu-id="a1a79-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="a1a79-129">**对于 EN-US 语言：**"Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="a1a79-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="a1a79-130">**对于 DE 语言：**"Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="a1a79-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="a1a79-131">标签 SYS18389，具有以下文本：</span><span class="sxs-lookup"><span data-stu-id="a1a79-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="a1a79-132">**对于 EN-US 语言：**"Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="a1a79-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="a1a79-133">**对于 DE 语言：**"Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="a1a79-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="a1a79-134">这是一个可设计的表达式。</span><span class="sxs-lookup"><span data-stu-id="a1a79-134">Here is the expression that can be designed.</span></span>

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="a1a79-135">如果报表于 2015 年 12 月 17 日为 **Litware 零售**客户处理，在 **EN-US** 区域性和 **EN-US** 语言中，此公式返回以下文本，其可能向用户呈现为异常消息：</span><span class="sxs-lookup"><span data-stu-id="a1a79-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="a1a79-136">*没有要打印的内容。客户 Litware 零售已于 2015 年 12 月 17 日停止。*</span><span class="sxs-lookup"><span data-stu-id="a1a79-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="a1a79-137">如果 2015 年 12 月 17 日为 **Litware 零售**客户处理同一个报表，在 **DE** 区域性和 **DE** 语言中，此公式返回以下文本（使用不同的日期格式）：</span><span class="sxs-lookup"><span data-stu-id="a1a79-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="a1a79-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="a1a79-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="a1a79-139">以下语法在标签的 ER 公式中应用：</span><span class="sxs-lookup"><span data-stu-id="a1a79-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="a1a79-140">**对于 Microsoft Dynamics 365 Finance 应用中资源的标签：** **\@X**，其中 **X** 是应用程序对象树 (AOT) 中的标签 ID</span><span class="sxs-lookup"><span data-stu-id="a1a79-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="a1a79-141">**对于位于 ER 配置中的标签：** **@"GER_LABEL:X"**，其中 **X** 是 ER 配置中的标签 ID</span><span class="sxs-lookup"><span data-stu-id="a1a79-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1a79-142">其他资源</span><span class="sxs-lookup"><span data-stu-id="a1a79-142">Additional resources</span></span>

[<span data-ttu-id="a1a79-143">文本函数</span><span class="sxs-lookup"><span data-stu-id="a1a79-143">Text functions</span></span>](er-functions-category-text.md)
