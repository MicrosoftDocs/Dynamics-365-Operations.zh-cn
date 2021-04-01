---
title: 设置装运承运人
description: 此主题显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ec19288f01ceb0bb3021cf549af1c38746785c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233575"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="d4df6-103">设置装运承运人</span><span class="sxs-lookup"><span data-stu-id="d4df6-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4df6-104">此主题显示如何设置装运承运人和定义详细信息，诸如服务、装运方式、运输招标、运输约束和装运费用。</span><span class="sxs-lookup"><span data-stu-id="d4df6-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="d4df6-105">运输协调员可将装运承运人分配给某个入站或出站装载。</span><span class="sxs-lookup"><span data-stu-id="d4df6-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="d4df6-106">创建新装运承运人</span><span class="sxs-lookup"><span data-stu-id="d4df6-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="d4df6-107">转到 **导航窗格 > 模块 > 运输管理 > 设置 > 承运人 > 装运承运人**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="d4df6-108">在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="d4df6-109">在 **装运承运人** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="d4df6-110">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d4df6-111">在 **模式** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="d4df6-112">填写装运承运人的一般信息</span><span class="sxs-lookup"><span data-stu-id="d4df6-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="d4df6-113">切换 **概览** 部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="d4df6-114">勾选或不勾选 **启用承运装运人** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d4df6-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="d4df6-115">在 **供应商帐户** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d4df6-116">选择向其分配装运承运人的供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="d4df6-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="d4df6-117">在 **运输招标类型** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="d4df6-118">选择 **手动** 以使用“运输招标”页面，或选择 **EDI** 来通过使用电子数据交换 (EDI) 更新招标信息。</span><span class="sxs-lookup"><span data-stu-id="d4df6-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="d4df6-119">勾选或不勾选 **启用承运评级** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d4df6-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="d4df6-120">创建装运承运人的必需服务</span><span class="sxs-lookup"><span data-stu-id="d4df6-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="d4df6-121">切换 **服务** 部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="d4df6-122">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-122">Select **New**.</span></span>
3. <span data-ttu-id="d4df6-123">在 **承运人服务** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="d4df6-124">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d4df6-125">在 **运输方法** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="d4df6-126">设置承运人的地址（可选）</span><span class="sxs-lookup"><span data-stu-id="d4df6-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="d4df6-127">切换 **地址** 部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="d4df6-128">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-128">Select **New**.</span></span>
3. <span data-ttu-id="d4df6-129">在 **名称或描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="d4df6-130">在 **国家/地区** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="d4df6-131">在 **邮政编码** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d4df6-132">在 **街道** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="d4df6-133">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="d4df6-134">设置装运承运人的评级资料。</span><span class="sxs-lookup"><span data-stu-id="d4df6-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="d4df6-135">切换 **评级资料** 部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="d4df6-136">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-136">Select **New**.</span></span>
3. <span data-ttu-id="d4df6-137">在 **评级资料** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="d4df6-138">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d4df6-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d4df6-139">在 **站点** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="d4df6-140">在 **仓库** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="d4df6-141">在 **费率引擎** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="d4df6-142">选择根据合同，您与承运人订立的费率引擎。</span><span class="sxs-lookup"><span data-stu-id="d4df6-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="d4df6-143">在 **费率主数据** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="d4df6-144">在 **运输时间引擎** 字段中，从下拉菜单中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d4df6-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="d4df6-145">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d4df6-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]