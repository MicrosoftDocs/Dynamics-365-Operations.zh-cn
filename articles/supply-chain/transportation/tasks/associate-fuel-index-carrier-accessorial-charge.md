---
title: 将燃油指数作为附属费用与承运人关联
description: 本指南显示如何创建附属分配、承运人附加费用、燃油附加费的附属主数据，以及将承运人燃油指数与承运人关联。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016992"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="e11a3-103">将燃油指数作为附属费用与承运人关联</span><span class="sxs-lookup"><span data-stu-id="e11a3-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e11a3-104">本指南显示如何创建附属分配、承运人附加费用、燃油附加费的附属主数据，以及将承运人燃油指数与承运人关联。</span><span class="sxs-lookup"><span data-stu-id="e11a3-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="e11a3-105">您需要设置承运人燃油指数才能运行此指南。</span><span class="sxs-lookup"><span data-stu-id="e11a3-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="e11a3-106">您可以使用“设置承运人燃油指数”指南来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="e11a3-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="e11a3-107">这些设置任务通常由物流经理完成。</span><span class="sxs-lookup"><span data-stu-id="e11a3-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="e11a3-108">使用 USMF 演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="e11a3-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="e11a3-109">创建附属主数据</span><span class="sxs-lookup"><span data-stu-id="e11a3-109">Create an accessorial master</span></span>
1. <span data-ttu-id="e11a3-110">转到“运输管理”>“设置”>“评级”>“附属主数据”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="e11a3-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-111">Click New.</span></span>
3. <span data-ttu-id="e11a3-112">在“附属主数据”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="e11a3-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e11a3-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="e11a3-115">创建装运承运人附加费</span><span class="sxs-lookup"><span data-stu-id="e11a3-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="e11a3-116">转到“运输管理”>“设置”>“评级”>“承运人附加费”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="e11a3-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-117">Click New.</span></span>
3. <span data-ttu-id="e11a3-118">在“承运人附属 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="e11a3-119">在“装运承运人”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e11a3-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e11a3-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e11a3-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e11a3-121">在本示例中，选择卡车承运人。</span><span class="sxs-lookup"><span data-stu-id="e11a3-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="e11a3-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e11a3-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e11a3-123">在“承运人服务”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e11a3-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e11a3-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e11a3-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e11a3-125">在“附属主数据”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e11a3-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e11a3-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e11a3-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e11a3-127">在本示例中，选择新创建的附属主数据。</span><span class="sxs-lookup"><span data-stu-id="e11a3-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="e11a3-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="e11a3-129">创建附属分配</span><span class="sxs-lookup"><span data-stu-id="e11a3-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="e11a3-130">单击“附属分配”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="e11a3-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-131">Click New.</span></span>
3. <span data-ttu-id="e11a3-132">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e11a3-133">切换“标准”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="e11a3-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="e11a3-134">在此标准中，您可以选择始终应用燃油附加费或为此示例选择仅特定区域适用的燃油附加费。</span><span class="sxs-lookup"><span data-stu-id="e11a3-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="e11a3-135">在“发件人邮政编码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="e11a3-136">在“收件人邮政编码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e11a3-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="e11a3-137">切换“计算”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="e11a3-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="e11a3-138">在计算部分可以指定如何计算燃油附加费。</span><span class="sxs-lookup"><span data-stu-id="e11a3-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="e11a3-139">此计算取决于您选择作为计算基数的附属单位。</span><span class="sxs-lookup"><span data-stu-id="e11a3-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="e11a3-140">在“附加费用类型”字段中，选择“燃油附加费”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="e11a3-141">在“附属单位”字段中，选择“里程”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="e11a3-142">在“区域”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e11a3-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e11a3-143">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e11a3-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e11a3-144">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="e11a3-145">更新承运人评级资料</span><span class="sxs-lookup"><span data-stu-id="e11a3-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="e11a3-146">转到“运输管理”>“设置”>“承运人”>“装运承运人”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="e11a3-147">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="e11a3-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e11a3-148">切换“评级资料”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="e11a3-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="e11a3-149">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-149">Click Edit.</span></span>
5. <span data-ttu-id="e11a3-150">在“承运人燃油指数”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="e11a3-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e11a3-151">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e11a3-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e11a3-152">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="e11a3-152">Click Save.</span></span>

