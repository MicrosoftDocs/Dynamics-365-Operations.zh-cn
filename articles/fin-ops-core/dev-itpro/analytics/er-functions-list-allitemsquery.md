---
title: ALLITEMSQUERY ER 函数
description: 本主题提供有关 ALLITEMSQUERY 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746691"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="e67b6-103">ALLITEMSQUERY ER 函数</span><span class="sxs-lookup"><span data-stu-id="e67b6-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e67b6-104">`ALLITEMSQUERY` 函数返回一个联接的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="e67b6-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="e67b6-105">它返回一个新的平展 *记录列表* 值，此值由代表与指定路径匹配的所有项目的记录的列表组成。</span><span class="sxs-lookup"><span data-stu-id="e67b6-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67b6-106">语法</span><span class="sxs-lookup"><span data-stu-id="e67b6-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="e67b6-107">参数</span><span class="sxs-lookup"><span data-stu-id="e67b6-107">Arguments</span></span>

<span data-ttu-id="e67b6-108">`path`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="e67b6-108">`path`: *Record list*</span></span>

<span data-ttu-id="e67b6-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="e67b6-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="e67b6-110">必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="e67b6-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="e67b6-111">返回值</span><span class="sxs-lookup"><span data-stu-id="e67b6-111">Return values</span></span>

<span data-ttu-id="e67b6-112">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="e67b6-112">*Record list*</span></span>

<span data-ttu-id="e67b6-113">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="e67b6-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e67b6-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="e67b6-114">Usage notes</span></span>

<span data-ttu-id="e67b6-115">指定的路径必须定义为 *记录列表* 数据类型的数据源元素的有效数据源路径。</span><span class="sxs-lookup"><span data-stu-id="e67b6-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="e67b6-116">同样必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="e67b6-116">It must also contain at least one relation.</span></span> <span data-ttu-id="e67b6-117">路径 *字符串* 和 *日期* 等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。</span><span class="sxs-lookup"><span data-stu-id="e67b6-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="e67b6-118">当此函数应用于 *记录列表* 数据类型的数据源，且该数据源引用可以使用 SQL 直接调用的应用程序对象（例如，表、实体或查询）时，它将作为连接的 SQL 查询运行。</span><span class="sxs-lookup"><span data-stu-id="e67b6-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="e67b6-119">否则，它将作为 [ALLITEMS](er-functions-list-allitems.md) 函数在内存内运行。</span><span class="sxs-lookup"><span data-stu-id="e67b6-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="e67b6-120">示例</span><span class="sxs-lookup"><span data-stu-id="e67b6-120">Example</span></span>

<span data-ttu-id="e67b6-121">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="e67b6-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="e67b6-122">引用 CustInvoiceTable 表的 *表记录* 类型的 **CustInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="e67b6-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="e67b6-123">包含表达式 `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 的 *计算字段* 类型的 **FilteredInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="e67b6-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="e67b6-124">包含表达式 `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 的 *计算字段* 类型的 **JourLines**</span><span class="sxs-lookup"><span data-stu-id="e67b6-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="e67b6-125">运行模型映射以调用 **JourLines** 数据源时，将运行以下 SQL 语句：</span><span class="sxs-lookup"><span data-stu-id="e67b6-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="e67b6-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="e67b6-126">Additional resources</span></span>

[<span data-ttu-id="e67b6-127">列表函数</span><span class="sxs-lookup"><span data-stu-id="e67b6-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]