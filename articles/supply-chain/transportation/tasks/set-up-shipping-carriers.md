---
title: 设置装运承运人
description: 此过程显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "314478"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="91371-103">设置装运承运人</span><span class="sxs-lookup"><span data-stu-id="91371-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91371-104">此过程显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。</span><span class="sxs-lookup"><span data-stu-id="91371-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="91371-105">运输协调员可将装运承运人分配给某个入站或出站装载。</span><span class="sxs-lookup"><span data-stu-id="91371-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="91371-106">创建新装运承运人</span><span class="sxs-lookup"><span data-stu-id="91371-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="91371-107">转到“运输管理”>“设置”>“承运人”>“装运承运人”。</span><span class="sxs-lookup"><span data-stu-id="91371-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="91371-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91371-108">Click New.</span></span>
3. <span data-ttu-id="91371-109">在“装运承运人”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="91371-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="91371-111">在“模式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="91371-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="91371-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="91371-114">填写装运承运人的一般信息</span><span class="sxs-lookup"><span data-stu-id="91371-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="91371-115">切换“概览”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="91371-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="91371-116">勾选或不勾选“启用承运装运人”复选框。</span><span class="sxs-lookup"><span data-stu-id="91371-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="91371-117">在“供应商”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="91371-118">选择向其分配装运承运人的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="91371-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="91371-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="91371-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="91371-121">在“运输招标类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="91371-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="91371-122">选择“手动使用运输招标”页面，或通过使用电子数据交换 (EDI) 选择 EDI 来更新招标信息。</span><span class="sxs-lookup"><span data-stu-id="91371-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="91371-123">勾选或不勾选“启用承运评级”复选框。</span><span class="sxs-lookup"><span data-stu-id="91371-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="91371-124">创建装运承运人的必需服务</span><span class="sxs-lookup"><span data-stu-id="91371-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="91371-125">切换“服务”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="91371-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="91371-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91371-126">Click New.</span></span>
3. <span data-ttu-id="91371-127">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="91371-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="91371-128">在“承运人服务”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="91371-129">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="91371-130">在“运输方法”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="91371-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="91371-132">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="91371-133">设置承运人的地址（可选）</span><span class="sxs-lookup"><span data-stu-id="91371-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="91371-134">切换“地址”部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="91371-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="91371-135">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91371-135">Click New.</span></span>
3. <span data-ttu-id="91371-136">在“名称”或“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="91371-137">在“国家/地区”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="91371-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="91371-139">在“邮政编码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="91371-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="91371-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="91371-142">在“街道”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="91371-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91371-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="91371-144">设置装运承运人的评级资料。</span><span class="sxs-lookup"><span data-stu-id="91371-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="91371-145">切换“评级资料”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="91371-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="91371-146">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="91371-146">Click New.</span></span>
3. <span data-ttu-id="91371-147">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="91371-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="91371-148">在“评级资料”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="91371-149">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="91371-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="91371-150">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="91371-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="91371-151">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="91371-152">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="91371-153">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="91371-154">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="91371-155">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="91371-156">在“费率引擎”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="91371-157">选择根据合同，您与承运人订立的费率引擎。</span><span class="sxs-lookup"><span data-stu-id="91371-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="91371-158">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="91371-159">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="91371-160">在“费率主数据”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="91371-161">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91371-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="91371-162">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="91371-163">在“运输时间引擎”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="91371-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="91371-164">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="91371-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="91371-165">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="91371-165">Click Save.</span></span>

