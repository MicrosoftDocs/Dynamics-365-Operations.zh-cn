---
title: "计算物料消耗量"
description: "本文提供有关与物料消耗量的计算相关的不同选项的信息。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f674a1f0051ee4b228b8a92f717ef5348a452bed
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="62573-103">计算物料消耗量</span><span class="sxs-lookup"><span data-stu-id="62573-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="62573-104">本文提供有关与物料消耗量的计算相关的不同选项的信息。</span><span class="sxs-lookup"><span data-stu-id="62573-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="62573-105">与物料消耗量计算相关的以下选项在**物料清单**页的**行明细**快速选项卡的**设置**和**步骤消耗量**选项卡上可用。</span><span class="sxs-lookup"><span data-stu-id="62573-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="62573-106">变量和常量消耗量</span><span class="sxs-lookup"><span data-stu-id="62573-106">Variable and constant consumption</span></span>
<span data-ttu-id="62573-107">在**消耗量**字段中，您可以选择是否应将消耗量计算为一个常量数量或一个变量数量。</span><span class="sxs-lookup"><span data-stu-id="62573-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="62573-108">如果生产需要固定数量或量，选择**常量**，不论生产的数量是多少。</span><span class="sxs-lookup"><span data-stu-id="62573-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="62573-109">如果成品中需要的物料金额与生产的成品的数量成比例，则选择**变量**，这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="62573-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="62573-110">通过公式计算消耗量</span><span class="sxs-lookup"><span data-stu-id="62573-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="62573-111">在**公式**字段中，您可以设置计算物料消耗量的各个公式。</span><span class="sxs-lookup"><span data-stu-id="62573-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="62573-112">如果您使用默认值**标准**，消耗量不会从公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="62573-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="62573-113">以下公式与**高度**、**宽度**、**深度**、**密度**和**常量**字段一起使用：</span><span class="sxs-lookup"><span data-stu-id="62573-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="62573-114">高度 \* 常量</span><span class="sxs-lookup"><span data-stu-id="62573-114">Height \* Constant</span></span>
-   <span data-ttu-id="62573-115">高度 \* 宽度 \* 常量</span><span class="sxs-lookup"><span data-stu-id="62573-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="62573-116">高度 \* 宽度 \* 深度 \* 常量</span><span class="sxs-lookup"><span data-stu-id="62573-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="62573-117">(高度 \* 宽度 \* 深度/密度) \* 常量</span><span class="sxs-lookup"><span data-stu-id="62573-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="62573-118">进位和倍数</span><span class="sxs-lookup"><span data-stu-id="62573-118">Rounding up and multiples</span></span>
<span data-ttu-id="62573-119">**进位**和**倍数**字段共同让您舍入物料消耗量价值。</span><span class="sxs-lookup"><span data-stu-id="62573-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="62573-120">例如，您可以根据在其中为生产领取物料的物料处理单元舍入该值。</span><span class="sxs-lookup"><span data-stu-id="62573-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="62573-121">以下选项在**舍入**字段中可用：**数量**、**度量**和**消耗量**。</span><span class="sxs-lookup"><span data-stu-id="62573-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="62573-122">数量</span><span class="sxs-lookup"><span data-stu-id="62573-122">Quantity</span></span>

<span data-ttu-id="62573-123">如果您选择**数量**作为舍入机制，数量必须是指定数量的倍数。</span><span class="sxs-lookup"><span data-stu-id="62573-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="62573-124">例如，需要整数时，在**倍数**字段中选择 **1**。</span><span class="sxs-lookup"><span data-stu-id="62573-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="62573-125">数字然后舍入到被 1 整除的数量。</span><span class="sxs-lookup"><span data-stu-id="62573-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="62573-126">量化指标</span><span class="sxs-lookup"><span data-stu-id="62573-126">Measurement</span></span>

<span data-ttu-id="62573-127">通常，当原材料采用特定尺寸时，选择**度量**作为舍入机制。</span><span class="sxs-lookup"><span data-stu-id="62573-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="62573-128">例如，成品需要一条 2 米金属管，金属管存储为 4.5 米长度。</span><span class="sxs-lookup"><span data-stu-id="62573-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="62573-129">在这种情况下，**度量**舍入机制可用于计算生产特定件数的成品需要多少个金属管。</span><span class="sxs-lookup"><span data-stu-id="62573-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="62573-130">对于此示例，**公式**字段设置为**高度 \* 常量**。</span><span class="sxs-lookup"><span data-stu-id="62573-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="62573-131">**高度**字段设置为 **2**，指示成品所需的管的长度。</span><span class="sxs-lookup"><span data-stu-id="62573-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="62573-132">**倍数**字段设置为 **4.5** 指示领取 4.5 米长的管。</span><span class="sxs-lookup"><span data-stu-id="62573-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="62573-133">计算如下：</span><span class="sxs-lookup"><span data-stu-id="62573-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="62573-134">10 件成品需要的倍数数：10 ÷ 2 = 5 件</span><span class="sxs-lookup"><span data-stu-id="62573-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="62573-135">总消耗量：4.5 × 5 = 22.5 米金属管</span><span class="sxs-lookup"><span data-stu-id="62573-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="62573-136">假定消耗每五个管报废 0.5 米管。</span><span class="sxs-lookup"><span data-stu-id="62573-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="62573-137">消耗量法</span><span class="sxs-lookup"><span data-stu-id="62573-137">Consumption</span></span>

<span data-ttu-id="62573-138">通常，当必须领取产品特定物料处理单元的完整数量的原材料时，选择**消耗量**作为舍入机制。</span><span class="sxs-lookup"><span data-stu-id="62573-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="62573-139">例如，2 夸脱涂料用于生产一件成品，涂料使用 25 夸脱罐领取。</span><span class="sxs-lookup"><span data-stu-id="62573-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="62573-140">在这种情况下，**消耗量**舍入机制可用于将消耗量舍入为 25 夸脱罐的整数。</span><span class="sxs-lookup"><span data-stu-id="62573-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="62573-141">如果必须生产 180 件成品，所需涂料数量计算为：</span><span class="sxs-lookup"><span data-stu-id="62573-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="62573-142">所需涂料，不包括废料：180 × 2 = 360 夸脱</span><span class="sxs-lookup"><span data-stu-id="62573-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="62573-143">罐数：360 ÷ 25 = 14.4，舍入为 15</span><span class="sxs-lookup"><span data-stu-id="62573-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="62573-144">所需涂料，包括废料：15 × 25 = 375 夸脱</span><span class="sxs-lookup"><span data-stu-id="62573-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="62573-145">步骤消耗量</span><span class="sxs-lookup"><span data-stu-id="62573-145">Step consumption</span></span>
<span data-ttu-id="62573-146">步骤消耗量用于计算数量间隔的常量消耗量。</span><span class="sxs-lookup"><span data-stu-id="62573-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="62573-147">如果在**设置**选项卡的**公式**字段中选择**步骤消耗量**，您可以在**步骤消耗量**选项卡上添加有关步骤的信息。固定消耗数量可以在生产数量的间隔中设置。</span><span class="sxs-lookup"><span data-stu-id="62573-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="62573-148">例如，如下表中所示设置步骤消耗量。</span><span class="sxs-lookup"><span data-stu-id="62573-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="62573-149">开始系列</span><span class="sxs-lookup"><span data-stu-id="62573-149">From series</span></span> | <span data-ttu-id="62573-150">数量</span><span class="sxs-lookup"><span data-stu-id="62573-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="62573-151">0.00</span><span class="sxs-lookup"><span data-stu-id="62573-151">0.00</span></span>        | <span data-ttu-id="62573-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="62573-152">10.0000</span></span>  |
| <span data-ttu-id="62573-153">100.00</span><span class="sxs-lookup"><span data-stu-id="62573-153">100.00</span></span>      | <span data-ttu-id="62573-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="62573-154">20.0000</span></span>  |
| <span data-ttu-id="62573-155">200.00</span><span class="sxs-lookup"><span data-stu-id="62573-155">200.00</span></span>      | <span data-ttu-id="62573-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="62573-156">40.0000</span></span>  |

<span data-ttu-id="62573-157">物料清单 (BOM) 数量为 1，生产数量为 110。</span><span class="sxs-lookup"><span data-stu-id="62573-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="62573-158">消耗量的公式为开始系列（数量）= 消耗量。</span><span class="sxs-lookup"><span data-stu-id="62573-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="62573-159">由于生产数量为 110，则落入“从 100 系列”。</span><span class="sxs-lookup"><span data-stu-id="62573-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="62573-160">因此数量为 20。</span><span class="sxs-lookup"><span data-stu-id="62573-160">Therefore, the quantity is 20.</span></span>




