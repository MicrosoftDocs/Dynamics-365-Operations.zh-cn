---
title: 创建产品生命周期状态以从主计划中排除产品
description: 此过程显示如何创建从主计划和物料清单级别计算中排除产品的新产品生命周期状态。
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818029"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="559bd-103">创建产品生命周期状态以从主计划中排除产品</span><span class="sxs-lookup"><span data-stu-id="559bd-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="559bd-104">此过程显示如何创建从主计划和物料清单级别计算中排除产品的新产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="559bd-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="559bd-105">创建过时状态</span><span class="sxs-lookup"><span data-stu-id="559bd-105">Create an obsolete state</span></span>
1. <span data-ttu-id="559bd-106">转到“产品信息管理”>“设置”>“产品生命周期状态”。</span><span class="sxs-lookup"><span data-stu-id="559bd-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="559bd-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="559bd-107">Click New.</span></span>
3. <span data-ttu-id="559bd-108">在“状态”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="559bd-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="559bd-109">在“对于计划有效”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="559bd-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="559bd-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="559bd-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="559bd-111">将过时状态与已发布产品关联</span><span class="sxs-lookup"><span data-stu-id="559bd-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="559bd-112">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="559bd-112">Close the page.</span></span>
2. <span data-ttu-id="559bd-113">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="559bd-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="559bd-114">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="559bd-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="559bd-115">例如，使用值“M00”在“搜索名称”字段中进行筛选。</span><span class="sxs-lookup"><span data-stu-id="559bd-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="559bd-116">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="559bd-116">Click Edit.</span></span>
5. <span data-ttu-id="559bd-117">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="559bd-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="559bd-118">在“产品生命周期状态”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="559bd-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]