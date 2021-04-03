---
title: ALLITEMSQUERY ER 函数
description: 本主题提供有关 ALLITEMSQUERY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559595"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="511da-103">ALLITEMSQUERY ER 函数</span><span class="sxs-lookup"><span data-stu-id="511da-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="511da-104">`ALLITEMSQUERY` 函数返回一个联接的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="511da-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="511da-105">它返回一个新的平展 *记录列表* 值，此值由代表与指定路径匹配的所有项目的记录的列表组成。</span><span class="sxs-lookup"><span data-stu-id="511da-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="511da-106">语法</span><span class="sxs-lookup"><span data-stu-id="511da-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="511da-107">参数</span><span class="sxs-lookup"><span data-stu-id="511da-107">Arguments</span></span>

<span data-ttu-id="511da-108">`path`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="511da-108">`path`: *Record list*</span></span>

<span data-ttu-id="511da-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="511da-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="511da-110">必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="511da-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="511da-111">返回值</span><span class="sxs-lookup"><span data-stu-id="511da-111">Return values</span></span>

<span data-ttu-id="511da-112">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="511da-112">*Record list*</span></span>

<span data-ttu-id="511da-113">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="511da-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="511da-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="511da-114">Usage notes</span></span>

<span data-ttu-id="511da-115">指定的路径必须定义为 *记录列表* 数据类型的数据源元素的有效数据源路径。</span><span class="sxs-lookup"><span data-stu-id="511da-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="511da-116">同样必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="511da-116">It must also contain at least one relation.</span></span> <span data-ttu-id="511da-117">路径 *字符串* 和 *日期* 等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。</span><span class="sxs-lookup"><span data-stu-id="511da-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="511da-118">当此函数应用于 *记录列表* 数据类型的数据源，且该数据源引用可以使用 SQL 直接调用的应用程序对象（例如，表、实体或查询）时，它将作为连接的 SQL 查询运行。</span><span class="sxs-lookup"><span data-stu-id="511da-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="511da-119">否则，它将作为 [ALLITEMS](er-functions-list-allitems.md) 函数在内存内运行。</span><span class="sxs-lookup"><span data-stu-id="511da-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="511da-120">示例</span><span class="sxs-lookup"><span data-stu-id="511da-120">Example</span></span>

<span data-ttu-id="511da-121">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="511da-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="511da-122">引用 CustInvoiceTable 表的 *表记录* 类型的 **CustInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="511da-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="511da-123">包含表达式 `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 的 *计算字段* 类型的 **FilteredInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="511da-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="511da-124">包含表达式 `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 的 *计算字段* 类型的 **JourLines**</span><span class="sxs-lookup"><span data-stu-id="511da-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="511da-125">运行模型映射以调用 **JourLines** 数据源时，将运行以下 SQL 语句：</span><span class="sxs-lookup"><span data-stu-id="511da-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="511da-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="511da-126">Additional resources</span></span>

[<span data-ttu-id="511da-127">列表函数</span><span class="sxs-lookup"><span data-stu-id="511da-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]