---
title: 设置费率主数据
description: 此过程显示如何设置费率主数据。
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423460"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="3dd67-103">设置费率主数据</span><span class="sxs-lookup"><span data-stu-id="3dd67-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3dd67-104">此过程显示如何设置费率主数据。</span><span class="sxs-lookup"><span data-stu-id="3dd67-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="3dd67-105">物流经理通常根据与承运人签订的合同设置费率主数据。</span><span class="sxs-lookup"><span data-stu-id="3dd67-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="3dd67-106">在此场景中，您将设置航空承运人的费率主数据。</span><span class="sxs-lookup"><span data-stu-id="3dd67-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="3dd67-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="3dd67-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="3dd67-108">设置分解主数据</span><span class="sxs-lookup"><span data-stu-id="3dd67-108">Set up break master</span></span>

1. <span data-ttu-id="3dd67-109">转到 **运输管理 > 设置 > 评级 > 分解主数据**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="3dd67-110">分解主数据用于定义价格结构及其中断点。</span><span class="sxs-lookup"><span data-stu-id="3dd67-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="3dd67-111">价格结构使用基于物理维度的分层定价方式。</span><span class="sxs-lookup"><span data-stu-id="3dd67-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="3dd67-112">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-112">Select **New**.</span></span>
1. <span data-ttu-id="3dd67-113">在 **分解主数据** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="3dd67-114">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="3dd67-115">在 **数据类型** 字段中，选择数据类型。</span><span class="sxs-lookup"><span data-stu-id="3dd67-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="3dd67-116">在 **比较** 字段中，输入请求的比较类型（使用运算符）。</span><span class="sxs-lookup"><span data-stu-id="3dd67-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="3dd67-117">在 **分解单位** 字段中，输入分解单位。</span><span class="sxs-lookup"><span data-stu-id="3dd67-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="3dd67-118">在 **详细信息** 部分，根据需要为定价结构创建任意数量的分解。</span><span class="sxs-lookup"><span data-stu-id="3dd67-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="3dd67-119">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="3dd67-120">设置费率主数据</span><span class="sxs-lookup"><span data-stu-id="3dd67-120">Set up rate master</span></span>

1. <span data-ttu-id="3dd67-121">转到 **运输管理 > 设置 > 评级 > 费率主数据**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="3dd67-122">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-122">Select **New**.</span></span>
1. <span data-ttu-id="3dd67-123">在 **费率主数据** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="3dd67-124">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="3dd67-125">在 **评级元数据 ID** 字段中，选择下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="3dd67-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="3dd67-126">评级元数据 ID 将确定费率主数据所需的数据，因为其定义使用此费率主数据的运输管理引擎预期的元数据。</span><span class="sxs-lookup"><span data-stu-id="3dd67-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="3dd67-127">在本示例中，选择 P2P 选项。</span><span class="sxs-lookup"><span data-stu-id="3dd67-127">For this example, select the P2P option.</span></span> <span data-ttu-id="3dd67-128">这已经在演示数据中定义。</span><span class="sxs-lookup"><span data-stu-id="3dd67-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="3dd67-129">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3dd67-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="3dd67-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="3dd67-131">设置基本费率</span><span class="sxs-lookup"><span data-stu-id="3dd67-131">Set up rate base</span></span>

1. <span data-ttu-id="3dd67-132">选择 **基准费率**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="3dd67-133">基本费率确定承运人的费率，并且可用于设置关税结构，因为其构成分解主数据中定义的中断点的费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="3dd67-134">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-134">Select **New**.</span></span>
3. <span data-ttu-id="3dd67-135">在 **基准费率** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="3dd67-136">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="3dd67-137">在 **分解主数据** 字段中，选择下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="3dd67-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3dd67-138">分解主数据用于定义价格结构及其中断点。</span><span class="sxs-lookup"><span data-stu-id="3dd67-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="3dd67-139">价格结构使用基于物理维度的分层定价方式。</span><span class="sxs-lookup"><span data-stu-id="3dd67-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="3dd67-140">在本示例中，使用重量。</span><span class="sxs-lookup"><span data-stu-id="3dd67-140">For this example, use weight.</span></span> <span data-ttu-id="3dd67-141">这已经在演示数据中定义。</span><span class="sxs-lookup"><span data-stu-id="3dd67-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="3dd67-142">在列表中，选择突出显示的行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3dd67-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="3dd67-143">展开 **详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="3dd67-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="3dd67-144">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-144">Select **New**.</span></span>
10. <span data-ttu-id="3dd67-145">在 **卸货地邮政编码起始编号** 字段中，键入“30301”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="3dd67-146">在 **卸货地邮政编码结束编号** 字段中，键入“30318”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="3dd67-147">在 **卸货国家/地区** 字段中，键入“美国”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="3dd67-148">在 **<1.00 磅** 字段中，键入“100”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="3dd67-149">如果负荷的总重量少于 1 磅，插入每磅费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="3dd67-150">在 **<5.00 磅** 字段中，键入“300”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="3dd67-151">如果负荷的总重量少于 5 磅，插入每磅费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="3dd67-152">在 **<20.00 磅** 字段中，键入“500”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="3dd67-153">如果负荷的总重量少于 20 磅，插入每磅费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="3dd67-154">在 **<100.00 磅** 字段中，键入“1000”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="3dd67-155">如果负荷的总重量少于 100 磅，插入每磅费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="3dd67-156">在 **<1,000.00 磅** 字段中，键入“3000”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="3dd67-157">如果负荷的总重量少于 1000 磅，插入每磅费率。</span><span class="sxs-lookup"><span data-stu-id="3dd67-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="3dd67-158">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-158">Select **Save**.</span></span>
19. <span data-ttu-id="3dd67-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3dd67-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="3dd67-160">分配基本费率</span><span class="sxs-lookup"><span data-stu-id="3dd67-160">Assign rate base</span></span>

1. <span data-ttu-id="3dd67-161">展开 **基准费率分配** 部分。</span><span class="sxs-lookup"><span data-stu-id="3dd67-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="3dd67-162">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-162">Select **New**.</span></span>
    * <span data-ttu-id="3dd67-163">对于每个费率主数据，您可以有几个基本费率分配。</span><span class="sxs-lookup"><span data-stu-id="3dd67-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="3dd67-164">这使得可能根据目的地、服务或不同的基本费率，为每个承运人创建多个不同的价格点。</span><span class="sxs-lookup"><span data-stu-id="3dd67-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="3dd67-165">在此过程将只创建基本费率分配。</span><span class="sxs-lookup"><span data-stu-id="3dd67-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="3dd67-166">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3dd67-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="3dd67-167">在 **基准费率** 字段中，选择下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="3dd67-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3dd67-168">在列表中，选择突出显示的行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3dd67-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="3dd67-169">在 **服务** 字段中，选择下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="3dd67-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3dd67-170">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3dd67-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3dd67-171">在列表中，选择突出显示的行中的链接。</span><span class="sxs-lookup"><span data-stu-id="3dd67-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="3dd67-172">在 **提货邮政编码** 字段中，键入“98052”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="3dd67-173">指定哪些邮政编码对于此基本费率分配是有效的。</span><span class="sxs-lookup"><span data-stu-id="3dd67-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="3dd67-174">在 **提货国家/地区** 字段中，键入“美国”。</span><span class="sxs-lookup"><span data-stu-id="3dd67-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="3dd67-175">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3dd67-175">Select **Save**.</span></span>
