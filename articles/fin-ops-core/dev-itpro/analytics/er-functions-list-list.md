---
title: LIST ER 函数
description: 本主题提供有关 LIST 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: ee51b6da008d1c0fcfb303e9659f507629237333
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042013"
---
# <span data-ttu-id="f7bc8-103"><a name="LIST">LIST ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="f7bc8-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7bc8-104">`LIST` 函数返回一个*记录列表*值，此值由根据指定参数创建的新记录列表组成。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7bc8-105">语法</span><span class="sxs-lookup"><span data-stu-id="f7bc8-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="f7bc8-106">参数</span><span class="sxs-lookup"><span data-stu-id="f7bc8-106">Arguments</span></span>

<span data-ttu-id="f7bc8-107">`record 1`：*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="f7bc8-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="f7bc8-108">对*记录*数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="f7bc8-109">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-109">This argument is required.</span></span>

<span data-ttu-id="f7bc8-110">`record N`：*容器（记录）*</span><span class="sxs-lookup"><span data-stu-id="f7bc8-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="f7bc8-111">对*记录*数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="f7bc8-112">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f7bc8-113">返回值</span><span class="sxs-lookup"><span data-stu-id="f7bc8-113">Return values</span></span>

<span data-ttu-id="f7bc8-114">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="f7bc8-114">*Record list*</span></span>

<span data-ttu-id="f7bc8-115">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f7bc8-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="f7bc8-116">Usage notes</span></span>

<span data-ttu-id="f7bc8-117">创建的列表的结构仅包含在参数中提到的每个记录的结构中显示的字段。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="f7bc8-118">示例</span><span class="sxs-lookup"><span data-stu-id="f7bc8-118">Example</span></span>

<span data-ttu-id="f7bc8-119">您输入*容器*类型的数据源**记录 1**。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="f7bc8-120">此数据源包含*计算字段*类型的以下嵌套字段：</span><span class="sxs-lookup"><span data-stu-id="f7bc8-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="f7bc8-121">**代码：** 此字段包含返回*字符串*类型的的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="f7bc8-122">**金额：** 此字段包含返回*实数*类型的的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="f7bc8-123">然后，您输入*容器*类型的数据源**记录 2**。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="f7bc8-124">此数据源包含*计算字段*类型的以下嵌套字段：</span><span class="sxs-lookup"><span data-stu-id="f7bc8-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="f7bc8-125">**金额：** 此字段包含返回*实数*类型的的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="f7bc8-126">**IsValid：** 此字段包含返回*布尔值*类型的的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="f7bc8-127">在此例中，表达式 `LIST('Record 1', 'Record 2')` 返回包含两个记录的新列表。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="f7bc8-128">此列表的结构由一个*实数*类型的**金额**字段组成，因为此字段是被调用函数每个参数中显示的唯一字段。</span><span class="sxs-lookup"><span data-stu-id="f7bc8-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7bc8-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="f7bc8-129">Additional resources</span></span>

[<span data-ttu-id="f7bc8-130">列表函数</span><span class="sxs-lookup"><span data-stu-id="f7bc8-130">List functions</span></span>](er-functions-category-list.md)
