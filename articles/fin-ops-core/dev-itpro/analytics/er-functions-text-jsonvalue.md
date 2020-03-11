---
title: JSONVALUE ER 函数
description: 本主题提供有关 JSONVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041142"
---
# <span data-ttu-id="788f7-103"><a name="JSONVALUE">JSONVALUE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="788f7-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="788f7-104">`JSONVALUE` 函数分析在指定路径访问且格式为 JavaScript Object Notation (JSON) 的数据，并提取具有指定 ID 的标量值。</span><span class="sxs-lookup"><span data-stu-id="788f7-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="788f7-105">然后将提取的标量值返回为*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="788f7-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="788f7-106">语法</span><span class="sxs-lookup"><span data-stu-id="788f7-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="788f7-107">参数</span><span class="sxs-lookup"><span data-stu-id="788f7-107">Arguments</span></span>

<span data-ttu-id="788f7-108">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="788f7-108">`input`: *String*</span></span>

<span data-ttu-id="788f7-109">包含 JSON 数据的*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="788f7-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="788f7-110">`path`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="788f7-110">`path`: *String*</span></span>

<span data-ttu-id="788f7-111">JSON 数据的标量值的标识符。</span><span class="sxs-lookup"><span data-stu-id="788f7-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="788f7-112">返回值</span><span class="sxs-lookup"><span data-stu-id="788f7-112">Return values</span></span>

<span data-ttu-id="788f7-113">*字符串*</span><span class="sxs-lookup"><span data-stu-id="788f7-113">*String*</span></span>

<span data-ttu-id="788f7-114">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="788f7-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="788f7-115">示例</span><span class="sxs-lookup"><span data-stu-id="788f7-115">Example</span></span>

<span data-ttu-id="788f7-116">**JsonField** 数据源包含 JSON 格式的以下数据：**{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。</span><span class="sxs-lookup"><span data-stu-id="788f7-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="788f7-117">在此例中，表达式 `JSONVALUE (JsonField, "BuildNumber")` 返回*字符串*数据类型的以下值：**"7.3.1234.1"**。</span><span class="sxs-lookup"><span data-stu-id="788f7-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="788f7-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="788f7-118">Additional resources</span></span>

[<span data-ttu-id="788f7-119">文本函数</span><span class="sxs-lookup"><span data-stu-id="788f7-119">Text functions</span></span>](er-functions-category-text.md)
