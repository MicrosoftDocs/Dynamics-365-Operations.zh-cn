---
title: GUIDVALUE ER 函数
description: 本主题提供有关 GUIDVALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685946"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="53045-103">GUIDVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="53045-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53045-104">`GUIDVALUE` 函数将 *字符串* 类型的指定输入转换为 *GUID* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="53045-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="53045-105">语法</span><span class="sxs-lookup"><span data-stu-id="53045-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="53045-106">参数</span><span class="sxs-lookup"><span data-stu-id="53045-106">Arguments</span></span>

<span data-ttu-id="53045-107">`input`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="53045-107">`input`: *String*</span></span>

<span data-ttu-id="53045-108">*字符串* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="53045-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="53045-109">返回值</span><span class="sxs-lookup"><span data-stu-id="53045-109">Return values</span></span>

<span data-ttu-id="53045-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="53045-110">*GUID*</span></span>

<span data-ttu-id="53045-111">生成的全局唯一标识符 (GUID) 值。</span><span class="sxs-lookup"><span data-stu-id="53045-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="53045-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="53045-112">Usage notes</span></span>

<span data-ttu-id="53045-113">若要执行反向转换（即，将指定的 *GUID* 数据类型的输入转换为 *字符串* 数据类型的数据项），您可以使用 [TEXT](er-functions-text-text.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="53045-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="53045-114">示例</span><span class="sxs-lookup"><span data-stu-id="53045-114">Example</span></span>

<span data-ttu-id="53045-115">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="53045-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="53045-116">包含表达式 `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` 的 *计算字段* 类型的 **myID** 数据源</span><span class="sxs-lookup"><span data-stu-id="53045-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="53045-117">引用 UserInfo 表的 *表记录* 类型的 **Users** 数据源</span><span class="sxs-lookup"><span data-stu-id="53045-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="53045-118">然后，您可以使用 `FILTER (Users, Users.objectId = myID)` 等表达式来按 *GUID* 数据类型的 **objectId** 字段筛选 UserInfo 表。</span><span class="sxs-lookup"><span data-stu-id="53045-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53045-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="53045-119">Additional resources</span></span>

[<span data-ttu-id="53045-120">文本函数</span><span class="sxs-lookup"><span data-stu-id="53045-120">Text functions</span></span>](er-functions-category-text.md)
