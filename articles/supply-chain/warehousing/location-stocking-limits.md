---
title: 库位库存限制
description: 本主题介绍库位库存限制的功能。
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607271"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="27748-103">库位库存限制</span><span class="sxs-lookup"><span data-stu-id="27748-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27748-104">您可以使用 **库位库存限制** 页面（**仓库管理 \> 设置 \> 仓库 \> 库位库存限制**）控制仓库库位的负荷容量，而不必使用更高级的流程进行物理产品的体积计算。</span><span class="sxs-lookup"><span data-stu-id="27748-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="27748-105">库位库存限制的目的是评估库位可以容纳的最大数量。</span><span class="sxs-lookup"><span data-stu-id="27748-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="27748-106">您可以在三个级别中的任何一个上设置该功能，每个级别在 **库位库存限制** 页面上都有自己的选项卡：</span><span class="sxs-lookup"><span data-stu-id="27748-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="27748-107">产品</span><span class="sxs-lookup"><span data-stu-id="27748-107">Products</span></span>
- <span data-ttu-id="27748-108">产品变型</span><span class="sxs-lookup"><span data-stu-id="27748-108">Product variants</span></span>
- <span data-ttu-id="27748-109">集装箱类型</span><span class="sxs-lookup"><span data-stu-id="27748-109">Container types</span></span>

<span data-ttu-id="27748-110">对于每个级别，您可以定义不同的字段值。</span><span class="sxs-lookup"><span data-stu-id="27748-110">For each level, you can define different field values.</span></span> <span data-ttu-id="27748-111">然后，系统将基于每行的 **数量** 和 **单位** 值评估特定库位的容量。</span><span class="sxs-lookup"><span data-stu-id="27748-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="27748-112">它将首先选择最详细的匹配记录。</span><span class="sxs-lookup"><span data-stu-id="27748-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="27748-113">例如，在 **库位配置文件 ID** 字段中具有值的行将先于仅在 **仓库** 字段中具有值的行进行评估。</span><span class="sxs-lookup"><span data-stu-id="27748-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="27748-114">还将基于使用的库位库存限制记录的 **数量值** 评估剩余容量。</span><span class="sxs-lookup"><span data-stu-id="27748-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="27748-115">在页面的 **产品** 部分中，您可以定义以下字段值以搜索库位库存限制：</span><span class="sxs-lookup"><span data-stu-id="27748-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="27748-116">仓库</span><span class="sxs-lookup"><span data-stu-id="27748-116">Warehouse</span></span>
- <span data-ttu-id="27748-117">库位模板 ID</span><span class="sxs-lookup"><span data-stu-id="27748-117">Location profile ID</span></span>
- <span data-ttu-id="27748-118">库位</span><span class="sxs-lookup"><span data-stu-id="27748-118">Location</span></span>
- <span data-ttu-id="27748-119">包装大小类别 ID</span><span class="sxs-lookup"><span data-stu-id="27748-119">Pack size category ID</span></span>
- <span data-ttu-id="27748-120">物料编号</span><span class="sxs-lookup"><span data-stu-id="27748-120">Item number</span></span>
- <span data-ttu-id="27748-121">单位</span><span class="sxs-lookup"><span data-stu-id="27748-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="27748-122">您不必为每个库位库存限制记录定义 **单位** 值。</span><span class="sxs-lookup"><span data-stu-id="27748-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="27748-123">库位容量计算将基于库存单位数量。</span><span class="sxs-lookup"><span data-stu-id="27748-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="27748-124">如果没有为使用的值定义单位转换，将跳过库位库存限制记录，就像为其定义了另一个 **物料编号** 值一样。</span><span class="sxs-lookup"><span data-stu-id="27748-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="27748-125">示例 – 采购订单接收</span><span class="sxs-lookup"><span data-stu-id="27748-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="27748-126">此示例基于干净的 *USMF* 演示数据集，其中在 **库位库存限制** 页面的 **产品变型** 选项卡上设置以下值。</span><span class="sxs-lookup"><span data-stu-id="27748-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="27748-127">仓库</span><span class="sxs-lookup"><span data-stu-id="27748-127">Warehouse</span></span> | <span data-ttu-id="27748-128">库位模板 ID</span><span class="sxs-lookup"><span data-stu-id="27748-128">Location profile ID</span></span> | <span data-ttu-id="27748-129">物料编号</span><span class="sxs-lookup"><span data-stu-id="27748-129">Item number</span></span> | <span data-ttu-id="27748-130">大小</span><span class="sxs-lookup"><span data-stu-id="27748-130">Size</span></span> | <span data-ttu-id="27748-131">数量</span><span class="sxs-lookup"><span data-stu-id="27748-131">Quantity</span></span> | <span data-ttu-id="27748-132">单位</span><span class="sxs-lookup"><span data-stu-id="27748-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="27748-133">24</span><span class="sxs-lookup"><span data-stu-id="27748-133">24</span></span>        | <span data-ttu-id="27748-134">FLOOR</span><span class="sxs-lookup"><span data-stu-id="27748-134">FLOOR</span></span>               | <span data-ttu-id="27748-135">D0013</span><span class="sxs-lookup"><span data-stu-id="27748-135">D0013</span></span>       | <span data-ttu-id="27748-136">一</span><span class="sxs-lookup"><span data-stu-id="27748-136">M</span></span>    | <span data-ttu-id="27748-137">300</span><span class="sxs-lookup"><span data-stu-id="27748-137">300</span></span>      | <span data-ttu-id="27748-138">位</span><span class="sxs-lookup"><span data-stu-id="27748-138">Ea</span></span>   |
| <span data-ttu-id="27748-139">24</span><span class="sxs-lookup"><span data-stu-id="27748-139">24</span></span>        | <span data-ttu-id="27748-140">FLOOR</span><span class="sxs-lookup"><span data-stu-id="27748-140">FLOOR</span></span>               | <span data-ttu-id="27748-141">D0013</span><span class="sxs-lookup"><span data-stu-id="27748-141">D0013</span></span>       | <span data-ttu-id="27748-142">L</span><span class="sxs-lookup"><span data-stu-id="27748-142">L</span></span>    | <span data-ttu-id="27748-143">240</span><span class="sxs-lookup"><span data-stu-id="27748-143">240</span></span>      | <span data-ttu-id="27748-144">位</span><span class="sxs-lookup"><span data-stu-id="27748-144">Ea</span></span>   |
| <span data-ttu-id="27748-145">24</span><span class="sxs-lookup"><span data-stu-id="27748-145">24</span></span>        | <span data-ttu-id="27748-146">FLOOR</span><span class="sxs-lookup"><span data-stu-id="27748-146">FLOOR</span></span>               | <span data-ttu-id="27748-147">D0013</span><span class="sxs-lookup"><span data-stu-id="27748-147">D0013</span></span>       | <span data-ttu-id="27748-148">六</span><span class="sxs-lookup"><span data-stu-id="27748-148">S</span></span>    | <span data-ttu-id="27748-149">360</span><span class="sxs-lookup"><span data-stu-id="27748-149">360</span></span>      | <span data-ttu-id="27748-150">位</span><span class="sxs-lookup"><span data-stu-id="27748-150">Ea</span></span>   |

<span data-ttu-id="27748-151">为产品设置不同的度量单位产品变型。</span><span class="sxs-lookup"><span data-stu-id="27748-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="27748-152">这些变型与三个托盘 (PL) 的库位库存限制一致：</span><span class="sxs-lookup"><span data-stu-id="27748-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="27748-153">**尺寸 M：** 1 PL = 100 每个 (Ea)</span><span class="sxs-lookup"><span data-stu-id="27748-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="27748-154">**尺寸 L：** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="27748-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="27748-155">**尺寸 S：** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="27748-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="27748-156">因此，**库位配置文件 ID** 值设置为 *FLOOR* 的每个库位可以容纳物料编号 *D0013* 的 *3* 个 *PL*。</span><span class="sxs-lookup"><span data-stu-id="27748-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="27748-157">准备示例</span><span class="sxs-lookup"><span data-stu-id="27748-157">Prepare for the example</span></span>

<span data-ttu-id="27748-158">在此示例中，您将运行两行的采购订单接收流。</span><span class="sxs-lookup"><span data-stu-id="27748-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="27748-159">但是，您必须首先采用以下方式更新演示数据，以确保这些库位允许容纳混合物料，仅使用空库位 *FL-002* 到 *FL-004*，并且没有未结入库工作。</span><span class="sxs-lookup"><span data-stu-id="27748-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="27748-160">对于库位 *FL-001*，将 **库位配置文件** 字段的值从 *FLOOR* 更改为 *FLOOR-05*。</span><span class="sxs-lookup"><span data-stu-id="27748-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="27748-161">对于 *FLOOR* 库位配置文件，将 **允许混合物料** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="27748-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="27748-162">创建具有以下两行的采购订单。</span><span class="sxs-lookup"><span data-stu-id="27748-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="27748-163">仓库</span><span class="sxs-lookup"><span data-stu-id="27748-163">Warehouse</span></span> | <span data-ttu-id="27748-164">物料编号</span><span class="sxs-lookup"><span data-stu-id="27748-164">Item number</span></span> | <span data-ttu-id="27748-165">大小</span><span class="sxs-lookup"><span data-stu-id="27748-165">Size</span></span> | <span data-ttu-id="27748-166">数量</span><span class="sxs-lookup"><span data-stu-id="27748-166">Quantity</span></span> | <span data-ttu-id="27748-167">单位</span><span class="sxs-lookup"><span data-stu-id="27748-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="27748-168">24</span><span class="sxs-lookup"><span data-stu-id="27748-168">24</span></span>        | <span data-ttu-id="27748-169">D0013</span><span class="sxs-lookup"><span data-stu-id="27748-169">D0013</span></span>       | <span data-ttu-id="27748-170">六</span><span class="sxs-lookup"><span data-stu-id="27748-170">S</span></span>    | <span data-ttu-id="27748-171">4</span><span class="sxs-lookup"><span data-stu-id="27748-171">4</span></span>        | <span data-ttu-id="27748-172">PL</span><span class="sxs-lookup"><span data-stu-id="27748-172">PL</span></span>   |
    | <span data-ttu-id="27748-173">24</span><span class="sxs-lookup"><span data-stu-id="27748-173">24</span></span>        | <span data-ttu-id="27748-174">D0013</span><span class="sxs-lookup"><span data-stu-id="27748-174">D0013</span></span>       | <span data-ttu-id="27748-175">L</span><span class="sxs-lookup"><span data-stu-id="27748-175">L</span></span>    | <span data-ttu-id="27748-176">4</span><span class="sxs-lookup"><span data-stu-id="27748-176">4</span></span>        | <span data-ttu-id="27748-177">PL</span><span class="sxs-lookup"><span data-stu-id="27748-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="27748-178">处理示例</span><span class="sxs-lookup"><span data-stu-id="27748-178">Process the example</span></span>

<span data-ttu-id="27748-179">您将首先接收尺寸 *S* 的单位 *PL* 的数量 *4*，并查看所创建工作的放置行库位。</span><span class="sxs-lookup"><span data-stu-id="27748-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="27748-180">然后，将接收尺寸 *L* 的单位 *PL* 的数量 *4*，并查看所创建工作的放置行库位。</span><span class="sxs-lookup"><span data-stu-id="27748-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="27748-181">在仓库应用中，使用 *24* 作为用户 ID 和 *1* 作为密码登录。</span><span class="sxs-lookup"><span data-stu-id="27748-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="27748-182">选择 **入库** \> **采购接收**。</span><span class="sxs-lookup"><span data-stu-id="27748-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="27748-183">接收尺寸 *S* 的物料编号 *D0013* 的 *4* *PL*。</span><span class="sxs-lookup"><span data-stu-id="27748-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="27748-184">查看所创建的储存工作。</span><span class="sxs-lookup"><span data-stu-id="27748-184">Review the putaway work that was created.</span></span> <span data-ttu-id="27748-185">应该会看到以下结果：</span><span class="sxs-lookup"><span data-stu-id="27748-185">You should see the following result:</span></span>

    - <span data-ttu-id="27748-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="27748-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="27748-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="27748-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="27748-188">接收尺寸 *L* 的物料编号 *D0013* 的 *4* *PL*。</span><span class="sxs-lookup"><span data-stu-id="27748-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="27748-189">查看所创建的储存工作。</span><span class="sxs-lookup"><span data-stu-id="27748-189">Review the putaway work that was created.</span></span> <span data-ttu-id="27748-190">应该会看到以下结果：</span><span class="sxs-lookup"><span data-stu-id="27748-190">You should see the following result:</span></span>

    - <span data-ttu-id="27748-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="27748-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="27748-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="27748-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="27748-193">根据结果，您可能会得出结论，系统未能分配正确的储存库位。</span><span class="sxs-lookup"><span data-stu-id="27748-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="27748-194">否则，为什么系统在最后一步中仅将尺寸 *L* 的 *1* *PL*（而不是 *2* *PL*）添加到库位 *FL-003*？</span><span class="sxs-lookup"><span data-stu-id="27748-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="27748-195">也就是说，为什么不是总共 *3* *PL* 储存到该库位？</span><span class="sxs-lookup"><span data-stu-id="27748-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="27748-196">为了说明这种明显的错误，您必须了解库位库存限制的选择标准。</span><span class="sxs-lookup"><span data-stu-id="27748-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="27748-197">系统选择最详细的匹配记录。</span><span class="sxs-lookup"><span data-stu-id="27748-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="27748-198">在此示例中，最详细的匹配记录是 **尺寸** 值是 *L*、**数量** 值是 *240* 和 **单位** 值是 *Ea* 的行。</span><span class="sxs-lookup"><span data-stu-id="27748-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="27748-199">因为您已在尺寸 *S* 的 *120* *Ea* 的数量的上次接收中有未结工作，因此剩余容量计算为 *240* – *120* = *120* *Ea*。</span><span class="sxs-lookup"><span data-stu-id="27748-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="27748-200">因此，剩余容量只能容纳 *80* *Ea* 的 *1* *PL*。</span><span class="sxs-lookup"><span data-stu-id="27748-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="27748-201">例如，您不能使用库位库存限制来控制在同一库位上具有不同数量的物料的补货。</span><span class="sxs-lookup"><span data-stu-id="27748-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="27748-202">在这种情况下，使用 *补货模板*。</span><span class="sxs-lookup"><span data-stu-id="27748-202">In this case, use a *replenishment template*.</span></span>
