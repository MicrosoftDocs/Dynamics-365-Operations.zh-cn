---
title: ALLITEMSQUERY ER 函数
description: 本主题提供有关 ALLITEMSQUERY 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 99f2aa9863e36a2f2eb1db5d0569d2a82402969a
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070636"
---
# <span data-ttu-id="8c324-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="8c324-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c324-104">`ALLITEMSQUERY` 函数返回一个联接的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="8c324-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="8c324-105">它返回一个新的平展*记录列表*值，此值由代表与指定路径匹配的所有项目的记录的列表组成。</span><span class="sxs-lookup"><span data-stu-id="8c324-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c324-106">语法</span><span class="sxs-lookup"><span data-stu-id="8c324-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="8c324-107">参数</span><span class="sxs-lookup"><span data-stu-id="8c324-107">Arguments</span></span>

<span data-ttu-id="8c324-108">`path`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="8c324-108">`path`: *Record list*</span></span>

<span data-ttu-id="8c324-109">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="8c324-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="8c324-110">必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="8c324-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c324-111">返回值</span><span class="sxs-lookup"><span data-stu-id="8c324-111">Return values</span></span>

<span data-ttu-id="8c324-112">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="8c324-112">*Record list*</span></span>

<span data-ttu-id="8c324-113">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="8c324-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c324-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="8c324-114">Usage notes</span></span>

<span data-ttu-id="8c324-115">指定的路径必须定义为*记录列表*数据类型的数据源元素的有效数据源路径。</span><span class="sxs-lookup"><span data-stu-id="8c324-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="8c324-116">同样必须包含至少一个关系。</span><span class="sxs-lookup"><span data-stu-id="8c324-116">It must also contain at least one relation.</span></span> <span data-ttu-id="8c324-117">路径*字符串*和*日期*等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。</span><span class="sxs-lookup"><span data-stu-id="8c324-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="8c324-118">当此函数应用于*记录列表*数据类型的数据源，且该数据源引用可以使用 SQL 直接调用的应用程序对象（例如，表、实体或查询）时，它将作为连接的 SQL 查询运行。</span><span class="sxs-lookup"><span data-stu-id="8c324-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="8c324-119">否则，它将作为 [ALLITEMS](er-functions-list-allitems.md) 函数在内存内运行。</span><span class="sxs-lookup"><span data-stu-id="8c324-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="8c324-120">示例</span><span class="sxs-lookup"><span data-stu-id="8c324-120">Example</span></span>

<span data-ttu-id="8c324-121">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="8c324-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="8c324-122">引用 CustInvoiceTable 表的*表记录*类型的 **CustInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="8c324-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="8c324-123">包含表达式 `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 的*计算字段*类型的 **FilteredInv** 数据源</span><span class="sxs-lookup"><span data-stu-id="8c324-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="8c324-124">包含表达式 `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 的*计算字段*类型的 **JourLines**</span><span class="sxs-lookup"><span data-stu-id="8c324-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="8c324-125">运行模型映射以调用 **JourLines** 数据源时，将运行以下 SQL 语句：</span><span class="sxs-lookup"><span data-stu-id="8c324-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="8c324-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="8c324-126">Additional resources</span></span>

[<span data-ttu-id="8c324-127">列表函数</span><span class="sxs-lookup"><span data-stu-id="8c324-127">List functions</span></span>](er-functions-category-list.md)
