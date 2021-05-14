---
title: 全国汽车货运分类 (NMFC) 代码
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用全国汽车货运分类 (NMFC) 代码
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941874"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="3191a-103">全国汽车货运分类 (NMFC) 代码</span><span class="sxs-lookup"><span data-stu-id="3191a-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3191a-104">全国汽车货运分类 (NMFC) 代码可帮助您对可以装运的物料进行分类。</span><span class="sxs-lookup"><span data-stu-id="3191a-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="3191a-105">NMFC 代码是用于对商品进行分组的符号。</span><span class="sxs-lookup"><span data-stu-id="3191a-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="3191a-106">它让运输公司能够根据卡车装配、装载问题、处理问题和易腐性等考虑事项对物料进行分类，从而评估要装运的货物。</span><span class="sxs-lookup"><span data-stu-id="3191a-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="3191a-107">商品将使用从 50 到 500 的数字范围分组到 18 个货运类之一。</span><span class="sxs-lookup"><span data-stu-id="3191a-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="3191a-108">商品被分组的类基于对四个运输特征的评估：密度、耐藏性、处理和责任。</span><span class="sxs-lookup"><span data-stu-id="3191a-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="3191a-109">这些特征共同确定商品的可运输性。</span><span class="sxs-lookup"><span data-stu-id="3191a-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="3191a-110">NMFC 代码与每个小于货车荷载 (LTL) 装运物料关联。</span><span class="sxs-lookup"><span data-stu-id="3191a-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="3191a-111">例如，可能为笔记本电脑分配了分类为 2.5 的 NMFC，而为电线分配了分类为 65 的 NMFC。</span><span class="sxs-lookup"><span data-stu-id="3191a-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="3191a-112">此功能可以帮助工作人员使用 NMFC 代码对 LTL 装运物料进行分类。</span><span class="sxs-lookup"><span data-stu-id="3191a-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="3191a-113">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="3191a-113">Here are some examples:</span></span>

- <span data-ttu-id="3191a-114">如果您的公司在提单 (BOL) 上包含货运描述，那么承运人将对装运的货物有所了解。</span><span class="sxs-lookup"><span data-stu-id="3191a-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="3191a-115">货运是一个重要的分类，因为很多运输公司的整个业务模型是基于所装运货物的类型。</span><span class="sxs-lookup"><span data-stu-id="3191a-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="3191a-116">此分类对于您的公司可能是必不可少的，因为它用于确定给定负荷的成本。</span><span class="sxs-lookup"><span data-stu-id="3191a-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="3191a-117">您的公司可以确定 LTL 物流运输公司的利润率。</span><span class="sxs-lookup"><span data-stu-id="3191a-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="3191a-118">此主题描述如何在 Microsoft Dynamics 365 Supply Chain Management 中使用 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="3191a-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3191a-119">先决条件</span><span class="sxs-lookup"><span data-stu-id="3191a-119">Prerequisites</span></span>

<span data-ttu-id="3191a-120">您必须先设置必须映射到 NMFC 代码的所有 LTL 货运类，然后才能够创建 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="3191a-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="3191a-121">LTL 货运类代表物料的类别，而 NMFC 代码与 18 个货运类中每个类的特定商品相关。</span><span class="sxs-lookup"><span data-stu-id="3191a-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="3191a-122">有关如何使用 LTL 类的详细信息，请参阅[小于货车荷载 (LTL) 类](ltl-class.md)。</span><span class="sxs-lookup"><span data-stu-id="3191a-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="3191a-123">创建 NMFC 代码</span><span class="sxs-lookup"><span data-stu-id="3191a-123">Create an NMFC code</span></span>

<span data-ttu-id="3191a-124">要创建 NMFC 代码，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3191a-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="3191a-125">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="3191a-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="3191a-126">转到 **仓库管理 \> 设置 \> 库存 \> NMFC 代码**。</span><span class="sxs-lookup"><span data-stu-id="3191a-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="3191a-127">转到 **运输管理 \> 设置 \> 运输标准 \> NMFC 代码**。</span><span class="sxs-lookup"><span data-stu-id="3191a-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="3191a-128">选择 **新建** 创建一个 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="3191a-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="3191a-129">然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="3191a-129">Then set the following fields:</span></span>

    - <span data-ttu-id="3191a-130">**NMFC 代码** – 输入商品类型的 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="3191a-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="3191a-131">**名称** – 为 NMFC 代码输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="3191a-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="3191a-132">**LTL 类** – 选择与 NMFC 代码关联的 LTL 类。</span><span class="sxs-lookup"><span data-stu-id="3191a-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="3191a-133">**BOL 处理单元** – 定义装运的默认处理类型。</span><span class="sxs-lookup"><span data-stu-id="3191a-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="3191a-134">示例：设置 NMFC 代码</span><span class="sxs-lookup"><span data-stu-id="3191a-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="3191a-135">下面的示例演示如何设置可以用于不同产品的两个不同的 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="3191a-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="3191a-136">转到 **仓库管理 \> 设置 \> 库存 \> NMFC 代码**。</span><span class="sxs-lookup"><span data-stu-id="3191a-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="3191a-137">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3191a-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3191a-138">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="3191a-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3191a-139">**NMFC 代码**：*92.5*</span><span class="sxs-lookup"><span data-stu-id="3191a-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="3191a-140">**名称**：*计算机*</span><span class="sxs-lookup"><span data-stu-id="3191a-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="3191a-141">**LTL 类**：*92.5*</span><span class="sxs-lookup"><span data-stu-id="3191a-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="3191a-142">**BOL 处理单元**：*单元*</span><span class="sxs-lookup"><span data-stu-id="3191a-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3191a-143">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3191a-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3191a-144">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3191a-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3191a-145">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="3191a-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3191a-146">**NMFC 代码**：*125*</span><span class="sxs-lookup"><span data-stu-id="3191a-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="3191a-147">**名称**：*手机*</span><span class="sxs-lookup"><span data-stu-id="3191a-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="3191a-148">**LTL 类**：*125*</span><span class="sxs-lookup"><span data-stu-id="3191a-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="3191a-149">**BOL 处理单元**：*单元*</span><span class="sxs-lookup"><span data-stu-id="3191a-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3191a-150">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3191a-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3191a-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="3191a-151">Additional resources</span></span>

- [<span data-ttu-id="3191a-152">小于货车荷载 (LTL) 类</span><span class="sxs-lookup"><span data-stu-id="3191a-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="3191a-153">创建提单</span><span class="sxs-lookup"><span data-stu-id="3191a-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
