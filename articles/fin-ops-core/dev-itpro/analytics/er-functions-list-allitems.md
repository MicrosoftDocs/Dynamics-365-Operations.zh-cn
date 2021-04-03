---
title: ALLITEMS ER 函数
description: 本主题提供有关 ALLITEMS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559216"
---
# <a name="allitems-er-function"></a><span data-ttu-id="05517-103">ALLITEMS ER 函数</span><span class="sxs-lookup"><span data-stu-id="05517-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05517-104">`ALLITEMS` 函数作为内存内选择运行，作为代表与指定路径匹配的所有项目的记录列表返回一个新的平展 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="05517-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="05517-105">语法</span><span class="sxs-lookup"><span data-stu-id="05517-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="05517-106">参数</span><span class="sxs-lookup"><span data-stu-id="05517-106">Arguments</span></span>

<span data-ttu-id="05517-107">`path`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="05517-107">`path`: *Record list*</span></span>

<span data-ttu-id="05517-108">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="05517-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="05517-109">返回值</span><span class="sxs-lookup"><span data-stu-id="05517-109">Return values</span></span>

<span data-ttu-id="05517-110">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="05517-110">*Record list*</span></span>

<span data-ttu-id="05517-111">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="05517-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="05517-112">使用说明</span><span class="sxs-lookup"><span data-stu-id="05517-112">Usage notes</span></span>

<span data-ttu-id="05517-113">路径必须定义为 *记录列表* 数据类型的数据源元素的有效数据源路径。</span><span class="sxs-lookup"><span data-stu-id="05517-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="05517-114">路径字符串和日期等数据元素应会在电子申报 (ER) 表达式生成器中设计时引发错误。</span><span class="sxs-lookup"><span data-stu-id="05517-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="05517-115">我们不建议您对可能包含大量数据的交易记录数据源使用此函数。</span><span class="sxs-lookup"><span data-stu-id="05517-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="05517-116">而是考虑使用 [ALLTEMSQUERY](er-functions-list-allitemsquery.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="05517-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="05517-117">示例 1</span><span class="sxs-lookup"><span data-stu-id="05517-117">Example 1</span></span>

<span data-ttu-id="05517-118">如果输入 `SPLIT("abcdef" , 2)` 作为数据源 **DS**，表达式 `COUNT( ALLITEMS (DS))` 将返回 **3**。</span><span class="sxs-lookup"><span data-stu-id="05517-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="05517-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="05517-119">Example 2</span></span>

<span data-ttu-id="05517-120">如果输入 **Vend** 作为引用 VendTable 应用程序表的 *记录列表* 数据类型的数据源，表达式 `ALLITEMS (Vend.'<Relations'.ContactPerson)` 将返回具有 **ContactPerson** 表结构并包含可以使用 **ContactPerson.ContactForParty == VendTable.Party** 关系访问的所有联系人，且可用于所引用供应商表中的所有供应商的记录的平展列表。</span><span class="sxs-lookup"><span data-stu-id="05517-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05517-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="05517-121">Additional resources</span></span>

[<span data-ttu-id="05517-122">列表函数</span><span class="sxs-lookup"><span data-stu-id="05517-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]