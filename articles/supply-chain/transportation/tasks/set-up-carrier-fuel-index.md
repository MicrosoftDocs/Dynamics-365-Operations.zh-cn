--- 
title: "设置承运人燃油指数"
description: "本指南介绍了如何创建燃油指数区域、燃油指数和承运人燃油指数。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a6a02c2eca3cecc8b7519a5951a958aa5bc637b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="852c7-103">设置承运人燃油指数</span><span class="sxs-lookup"><span data-stu-id="852c7-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="852c7-104">本指南介绍了如何创建燃油指数区域、燃油指数和承运人燃油指数。</span><span class="sxs-lookup"><span data-stu-id="852c7-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="852c7-105">燃油指数区域指定燃油指数应该应用到哪个区域，燃油指数指定特定时间段的燃油价格。</span><span class="sxs-lookup"><span data-stu-id="852c7-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="852c7-106">若要反映燃料价格随时间的变化，可将多个燃油指数与承运人关联。</span><span class="sxs-lookup"><span data-stu-id="852c7-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="852c7-107">这些任务通常由运输协调员完成。</span><span class="sxs-lookup"><span data-stu-id="852c7-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="852c7-108">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="852c7-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="852c7-109">创建燃油指数区域</span><span class="sxs-lookup"><span data-stu-id="852c7-109">Create a fuel index region</span></span>
1. <span data-ttu-id="852c7-110">转到“运输管理”>“设置”>“燃油指数”>“燃油指数区域”。</span><span class="sxs-lookup"><span data-stu-id="852c7-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="852c7-111">首先您必须创建不同的区域，这些区域供您操作和计算不同的燃油附加费。</span><span class="sxs-lookup"><span data-stu-id="852c7-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="852c7-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="852c7-112">Click New.</span></span>
3. <span data-ttu-id="852c7-113">在“区域”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="852c7-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="852c7-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="852c7-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="852c7-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="852c7-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="852c7-116">创建燃料指数</span><span class="sxs-lookup"><span data-stu-id="852c7-116">Create a fuel index</span></span>
1. <span data-ttu-id="852c7-117">转到“运输管理”>“设置”>“燃油指数”>“燃油指数”。</span><span class="sxs-lookup"><span data-stu-id="852c7-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="852c7-118">对于您已设置的区域，您需要输入燃料的当前价格。</span><span class="sxs-lookup"><span data-stu-id="852c7-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="852c7-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="852c7-119">Click New.</span></span>
3. <span data-ttu-id="852c7-120">在“区域”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="852c7-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="852c7-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="852c7-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="852c7-122">在“每加仑油价”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="852c7-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="852c7-123">在“生效开始日期和时间”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="852c7-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="852c7-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="852c7-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="852c7-125">创建承运人燃油指数</span><span class="sxs-lookup"><span data-stu-id="852c7-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="852c7-126">转到“运输管理”>“设置”>“燃油指数”>“承运人燃油指数”。</span><span class="sxs-lookup"><span data-stu-id="852c7-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="852c7-127">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="852c7-127">Click New.</span></span>
3. <span data-ttu-id="852c7-128">在“承运人燃料指数”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="852c7-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="852c7-129">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="852c7-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="852c7-130">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="852c7-130">Click New.</span></span>
6. <span data-ttu-id="852c7-131">在“生效开始日期和时间”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="852c7-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="852c7-132">在“PPG 发件人”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="852c7-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="852c7-133">在此示例中，您可以设置“PPG 发件人”字段为 1.95。</span><span class="sxs-lookup"><span data-stu-id="852c7-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="852c7-134">在“PPG 收件人”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="852c7-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="852c7-135">在此示例中，您可以设置“PPG 收件人”字段为 2。</span><span class="sxs-lookup"><span data-stu-id="852c7-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="852c7-136">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="852c7-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="852c7-137">在此示例中，您可以设置百分比为 3。</span><span class="sxs-lookup"><span data-stu-id="852c7-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="852c7-138">在“货币”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="852c7-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="852c7-139">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="852c7-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="852c7-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="852c7-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="852c7-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="852c7-141">Click Save.</span></span>


