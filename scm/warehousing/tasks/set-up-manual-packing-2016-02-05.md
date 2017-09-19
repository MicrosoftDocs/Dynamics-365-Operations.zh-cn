--- 
title: "设置人工装箱（仅 2016 年 2 月和 5 月）"
description: "包装流程允许您验证并将产品包装到集装箱中。"
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="db448-103">设置人工装箱（仅 2016 年 2 月和 5 月）</span><span class="sxs-lookup"><span data-stu-id="db448-103">Set up manual packing (February & May 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db448-104">包装流程允许您验证并将产品包装到集装箱中。</span><span class="sxs-lookup"><span data-stu-id="db448-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="db448-105">在此流程中，仓库工作人员从存储位置的拣选产品并将它们移到包装站，他们在包装站检查物料数量和类型，并将其分配到相应的集装箱。</span><span class="sxs-lookup"><span data-stu-id="db448-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="db448-106">在完全包装容器时，可以封闭它并将其移至出货台，然后产品可进行装运。</span><span class="sxs-lookup"><span data-stu-id="db448-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="db448-107">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="db448-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="db448-108">此过程仅适用于 Dynamics 365 for Operations 的 2016 年 2 月 和 2016 年 5 月版本。</span><span class="sxs-lookup"><span data-stu-id="db448-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="db448-109">设置位置配置文件</span><span class="sxs-lookup"><span data-stu-id="db448-109">Set up location profiles</span></span>
1. <span data-ttu-id="db448-110">转到“仓库管理”>“设置”>“仓库”>“位置模板”。</span><span class="sxs-lookup"><span data-stu-id="db448-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="db448-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="db448-111">Click New.</span></span>
    * <span data-ttu-id="db448-112">位置配置文件可用于包装站，并包含位置信息和规则。</span><span class="sxs-lookup"><span data-stu-id="db448-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="db448-113">在“位置模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="db448-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="db448-115">在“位置格式”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="db448-116">在“位置类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="db448-117">选择“允许混合物料”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="db448-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="db448-118">选择“允许混合库存状态”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="db448-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="db448-119">选择“覆盖批处理天数的规则”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="db448-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="db448-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="db448-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="db448-121">设置仓库管理的参数</span><span class="sxs-lookup"><span data-stu-id="db448-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="db448-122">转到“仓库管理”>“设置”>“仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="db448-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="db448-123">单击“包装”选项卡。</span><span class="sxs-lookup"><span data-stu-id="db448-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="db448-124">在“包装库位的模板 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="db448-125">选择要用于包装的位置配置文件。</span><span class="sxs-lookup"><span data-stu-id="db448-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="db448-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="db448-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="db448-127">设置集装箱类型</span><span class="sxs-lookup"><span data-stu-id="db448-127">Set up container types</span></span>
1. <span data-ttu-id="db448-128">转到“仓库管理”>“设置”>“集装箱”>“集装箱类型”。</span><span class="sxs-lookup"><span data-stu-id="db448-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="db448-129">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="db448-129">Click New.</span></span>
    * <span data-ttu-id="db448-130">您可以定义要使用的集装箱类型：</span><span class="sxs-lookup"><span data-stu-id="db448-130">You can define the types of containers to use.</span></span> <span data-ttu-id="db448-131">您可以指定集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和重量。</span><span class="sxs-lookup"><span data-stu-id="db448-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="db448-132">属性是允许您在集装箱类型添加额外维度的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="db448-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="db448-133">在“集装箱类型代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="db448-134">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="db448-135">在“皮重”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="db448-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="db448-136">在“最大重量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="db448-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="db448-137">在“体积”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="db448-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="db448-138">在“长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="db448-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="db448-139">在“宽度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="db448-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="db448-140">在“高度”字段中输入数字。</span><span class="sxs-lookup"><span data-stu-id="db448-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="db448-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="db448-141">Click Save.</span></span>
12. <span data-ttu-id="db448-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="db448-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="db448-143">设置包装模板</span><span class="sxs-lookup"><span data-stu-id="db448-143">Set up packing profiles</span></span>
1. <span data-ttu-id="db448-144">转到“仓库管理”>“设置”>“包装”>“包装模板”。</span><span class="sxs-lookup"><span data-stu-id="db448-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="db448-145">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="db448-145">Click New.</span></span>
3. <span data-ttu-id="db448-146">在“包装模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="db448-147">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="db448-148">在“集装箱封闭模板 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="db448-149">集装箱封闭模板 ID 是可选的，是此包装模板的默认封闭集装箱模板。</span><span class="sxs-lookup"><span data-stu-id="db448-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="db448-150">在“集装箱 ID 模式”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="db448-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="db448-151">此选项确定在创建集装箱时集装箱 ID 是否自动生成，或是否手动创建集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="db448-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="db448-152">在“集装箱类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="db448-153">默认情况下，在创建新集装箱时，将使用集装箱类型。</span><span class="sxs-lookup"><span data-stu-id="db448-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="db448-154">选择“在集装箱封闭时自动创建集装箱”复选框。</span><span class="sxs-lookup"><span data-stu-id="db448-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="db448-155">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="db448-155">Click Save.</span></span>
10. <span data-ttu-id="db448-156">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="db448-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="db448-157">设置集装箱封闭模板</span><span class="sxs-lookup"><span data-stu-id="db448-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="db448-158">转到“仓库管理”>“设置”>“集装箱”>“集装箱封闭模板”。</span><span class="sxs-lookup"><span data-stu-id="db448-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="db448-159">集装箱封闭模板定义在集装箱封闭时发生的情况。</span><span class="sxs-lookup"><span data-stu-id="db448-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="db448-160">您可以设置多个封闭集装箱模板。</span><span class="sxs-lookup"><span data-stu-id="db448-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="db448-161">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="db448-161">Click New.</span></span>
3. <span data-ttu-id="db448-162">在“集装箱封闭模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="db448-163">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="db448-164">在“显示时间”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="db448-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="db448-165">指定在封闭集装箱或确认装运时是否显示。</span><span class="sxs-lookup"><span data-stu-id="db448-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="db448-166">请注意，显示要求运输管理。</span><span class="sxs-lookup"><span data-stu-id="db448-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="db448-167">显示必须在运输引擎中实施以正常工作。</span><span class="sxs-lookup"><span data-stu-id="db448-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="db448-168">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="db448-169">在“最终装运的默认位置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="db448-170">这将是封闭集装箱后产品将移到的位置。</span><span class="sxs-lookup"><span data-stu-id="db448-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="db448-171">此位置必须具有在仓库参数中定义的位置模板。</span><span class="sxs-lookup"><span data-stu-id="db448-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="db448-172">在“重量单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="db448-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="db448-173">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="db448-173">Click Save.</span></span>

