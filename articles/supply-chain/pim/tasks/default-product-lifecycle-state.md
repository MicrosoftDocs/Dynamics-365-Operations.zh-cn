---
title: 创建默认的产品生命周期状态
description: 此过程显示如何创建默认产品生命周期状态以及如何将默认状态与已发布产品关联。
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 796ed31ea045ab969c0afd8a4cf9036e05b6b168
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149982"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="dae94-103">创建默认的产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="dae94-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dae94-104">此过程显示如何创建默认产品生命周期状态以及如何将默认状态与已发布产品关联。</span><span class="sxs-lookup"><span data-stu-id="dae94-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="dae94-105">创建默认的生命周期状态</span><span class="sxs-lookup"><span data-stu-id="dae94-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="dae94-106">转到“产品信息管理”>“设置”>“产品生命周期状态”。</span><span class="sxs-lookup"><span data-stu-id="dae94-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="dae94-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dae94-107">Click New.</span></span>
3. <span data-ttu-id="dae94-108">在“状态”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="dae94-109">在发布到“法人”字段时在“默认”中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="dae94-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="dae94-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dae94-111">在“对于计划有效”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="dae94-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="dae94-112">如果新发布的产品不应包含在主计划中，请选择“否”。</span><span class="sxs-lookup"><span data-stu-id="dae94-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="dae94-113">如果应包含在主计划中，则将控制留为默认值“是”。</span><span class="sxs-lookup"><span data-stu-id="dae94-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="dae94-114">创建新的已发布产品</span><span class="sxs-lookup"><span data-stu-id="dae94-114">Create a new released product</span></span>
1. <span data-ttu-id="dae94-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dae94-115">Close the page.</span></span>
2. <span data-ttu-id="dae94-116">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="dae94-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="dae94-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dae94-117">Click New.</span></span>
4. <span data-ttu-id="dae94-118">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="dae94-119">在“产品名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="dae94-120">在“搜索名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="dae94-121">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="dae94-122">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="dae94-123">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="dae94-124">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="dae94-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dae94-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="dae94-126">默认产品生命周期状态是一种全局定义。</span><span class="sxs-lookup"><span data-stu-id="dae94-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="dae94-127">将产品更改为有效状态</span><span class="sxs-lookup"><span data-stu-id="dae94-127">Change the product to an active state</span></span>
1. <span data-ttu-id="dae94-128">在“产品生命周期状态”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dae94-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="dae94-129">假设您设置了活动状态，您现在可以选择此活动状态来允许产品用于主计划和物料清单级别计算。</span><span class="sxs-lookup"><span data-stu-id="dae94-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="dae94-130">显然，这只在为一致计划指定了所需的所有产品详细信息时才有意义。</span><span class="sxs-lookup"><span data-stu-id="dae94-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

