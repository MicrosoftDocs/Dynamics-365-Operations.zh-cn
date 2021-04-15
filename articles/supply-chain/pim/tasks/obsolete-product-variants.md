---
title: 查找过时产品变型
description: 此过程显示如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。
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
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807984"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="9a707-103">查找过时产品变型</span><span class="sxs-lookup"><span data-stu-id="9a707-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a707-104">此过程显示如何查找过时的已发布产品或产品变型以及如何将产品生命周期状态关联到过时的产品。</span><span class="sxs-lookup"><span data-stu-id="9a707-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="9a707-105">先决条件：您需要至少先定义一个对于计划无效的产品生命周期状态，然后才能够播放此任务指南。</span><span class="sxs-lookup"><span data-stu-id="9a707-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="9a707-106">运行模拟</span><span class="sxs-lookup"><span data-stu-id="9a707-106">Run a simulation</span></span>
1. <span data-ttu-id="9a707-107">转到“产品信息管理”>“定期任务”>“更改过时产品的生命周期状态”。</span><span class="sxs-lookup"><span data-stu-id="9a707-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="9a707-108">在“新产品生命周期状态”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9a707-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="9a707-109">在“运行没有更新产品数据的模拟”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="9a707-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="9a707-110">在“排除在此天数内创建的产品”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a707-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="9a707-111">在“排除交易中使用的产品(以天数为单位)”字段中输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9a707-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="9a707-112">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="9a707-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9a707-113">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="9a707-113">Click Filter.</span></span>
8. <span data-ttu-id="9a707-114">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="9a707-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9a707-115">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="9a707-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="9a707-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9a707-116">Click OK.</span></span>
11. <span data-ttu-id="9a707-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9a707-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="9a707-118">如果您预期搜索大量产品，建议批量运行模拟。</span><span class="sxs-lookup"><span data-stu-id="9a707-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="9a707-119">此外，请确保模拟不会在公司大部分的有效工作时间期间运行。</span><span class="sxs-lookup"><span data-stu-id="9a707-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="9a707-120">查看模拟结果</span><span class="sxs-lookup"><span data-stu-id="9a707-120">Review the simulation results</span></span>
1. <span data-ttu-id="9a707-121">转到“产品信息管理”>“查询和报告”>“产品生命周期状态维护历史记录”。</span><span class="sxs-lookup"><span data-stu-id="9a707-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="9a707-122">在此页上，您可以查看模拟结果并评估在不通过模拟运行更新时有多少产品和产品变型将与新产品生命周期状态关联。</span><span class="sxs-lookup"><span data-stu-id="9a707-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="9a707-123">运行已过时产品的产品生命周期状态的更新</span><span class="sxs-lookup"><span data-stu-id="9a707-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="9a707-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9a707-124">Close the page.</span></span>
2. <span data-ttu-id="9a707-125">转到“产品信息管理”>“定期任务”>“更改过时产品的生命周期状态”。</span><span class="sxs-lookup"><span data-stu-id="9a707-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="9a707-126">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="9a707-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="9a707-127">请注意，上一次选择已保存。</span><span class="sxs-lookup"><span data-stu-id="9a707-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="9a707-128">在“运行没有更新产品数据的模拟”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="9a707-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="9a707-129">展开“后台运行”部分。</span><span class="sxs-lookup"><span data-stu-id="9a707-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="9a707-130">根据受影响的产品和产品变型的数量，考虑批量运行此作业。</span><span class="sxs-lookup"><span data-stu-id="9a707-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="9a707-131">请确保不在公司的大部分有效工作时间运行较大的更新作业。</span><span class="sxs-lookup"><span data-stu-id="9a707-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="9a707-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9a707-132">Click OK.</span></span>
7. <span data-ttu-id="9a707-133">转到“产品信息管理”>“查询和报告”>“产品生命周期状态维护历史记录”。</span><span class="sxs-lookup"><span data-stu-id="9a707-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="9a707-134">查看更改的已发布产品和产品变型。</span><span class="sxs-lookup"><span data-stu-id="9a707-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="9a707-135">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="9a707-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]