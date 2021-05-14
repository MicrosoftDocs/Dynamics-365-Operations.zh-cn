---
title: 小于货车荷载 (LTL) 类
description: 本主题说明什么是小于货车荷载 (LTL) 类，并介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中进行设置。
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941802"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="38f4b-103">小于货车荷载 (LTL) 类</span><span class="sxs-lookup"><span data-stu-id="38f4b-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38f4b-104">小于货车荷载 (LTL) 类是一个货运类，用于对可以装运的物料进行分类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="38f4b-105">通常，每种类型的产品或商品都有全国汽车货运分类 (NMFC) 代码，该代码与 LTL 装运的特定货运类编号相对应。</span><span class="sxs-lookup"><span data-stu-id="38f4b-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="38f4b-106">LTL 货运类代表物料的类别，而 NMFC 代码与 18 个货运类中每个类的特定商品相关。</span><span class="sxs-lookup"><span data-stu-id="38f4b-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="38f4b-107">此功能让您可以使用您的系统执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="38f4b-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="38f4b-108">定义您的公司使用的 LTL 货运类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="38f4b-109">在 **NMFC 代码** 页上，将每个 LTL 类分配给 NMFC 代码。</span><span class="sxs-lookup"><span data-stu-id="38f4b-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="38f4b-110">有关详细信息，请参阅[全国汽车货运分类 (NMFC) 代码](nmfc-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="38f4b-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="38f4b-111">在 **产品** 页上为每个产品分配 NMFC 代码（因此分配其关联的 LTL 代码）。</span><span class="sxs-lookup"><span data-stu-id="38f4b-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="38f4b-112">准确评估分配了 NMFC 代码的每个产品的 LTL 类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="38f4b-113">通过检查国际 LTL 标准，确定每个 LTL 类的包装要求。</span><span class="sxs-lookup"><span data-stu-id="38f4b-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="38f4b-114">这样，您可以确保您的产品得到良好的保护，可以安全装运。</span><span class="sxs-lookup"><span data-stu-id="38f4b-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="38f4b-115">根据每种产品的 LTL 货运类，获取准确的装运估计信息。</span><span class="sxs-lookup"><span data-stu-id="38f4b-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="38f4b-116">此主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建 LTL 类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="38f4b-117">创建 LTL 类</span><span class="sxs-lookup"><span data-stu-id="38f4b-117">Create an LTL class</span></span>

<span data-ttu-id="38f4b-118">要创建 LTL 类，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="38f4b-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="38f4b-119">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="38f4b-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="38f4b-120">转到 **仓库管理 \> 设置 \> 库存 \> LTL 类**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="38f4b-121">转到 **运输管理 \> 设置 \> 运输标准 \> LTL 类**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="38f4b-122">在操作窗格上，选择 **新建** 创建一个 LTL 类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="38f4b-123">然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="38f4b-123">Then set the following fields:</span></span>

    - <span data-ttu-id="38f4b-124">**LTL 类** – 输入商品类型的公司内部 LTL 类标识符 (ID)。</span><span class="sxs-lookup"><span data-stu-id="38f4b-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="38f4b-125">大多数公司使用国际标准。</span><span class="sxs-lookup"><span data-stu-id="38f4b-125">Most companies use the international standard.</span></span> <span data-ttu-id="38f4b-126">在这种情况下，此字段的值将与 **类** 字段的值匹配。</span><span class="sxs-lookup"><span data-stu-id="38f4b-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="38f4b-127">但是，如果您的公司使用自己的标准，请输入符合该标准的代码。</span><span class="sxs-lookup"><span data-stu-id="38f4b-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="38f4b-128">**名称** – 输入一个将帮助您和其他用户为每个 NMFC 代码选择正确的 LTL 类的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="38f4b-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="38f4b-129">**类** – 输入商品类型的国际标准 LTL 类 ID。</span><span class="sxs-lookup"><span data-stu-id="38f4b-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="38f4b-130">您在此处输入的代码必须符合官方标准。</span><span class="sxs-lookup"><span data-stu-id="38f4b-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="38f4b-131">示例：设置 LTL 类</span><span class="sxs-lookup"><span data-stu-id="38f4b-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="38f4b-132">下面的示例演示如何设置可以用于不同类型产品的两个不同的 LTL 类。</span><span class="sxs-lookup"><span data-stu-id="38f4b-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="38f4b-133">转到 **仓库管理 \> 设置 \> 库存 \> LTL 类**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="38f4b-134">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="38f4b-135">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="38f4b-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="38f4b-136">**LTL 类**：*92.5*</span><span class="sxs-lookup"><span data-stu-id="38f4b-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="38f4b-137">**名称**：*计算机、显示器、冰箱*</span><span class="sxs-lookup"><span data-stu-id="38f4b-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="38f4b-138">**类**：*92.5*</span><span class="sxs-lookup"><span data-stu-id="38f4b-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="38f4b-139">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="38f4b-140">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="38f4b-141">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="38f4b-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="38f4b-142">**LTL 类**：*125*</span><span class="sxs-lookup"><span data-stu-id="38f4b-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="38f4b-143">**名称**：*小家电*</span><span class="sxs-lookup"><span data-stu-id="38f4b-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="38f4b-144">**类**：*125*</span><span class="sxs-lookup"><span data-stu-id="38f4b-144">**Class:** *125*</span></span>

1. <span data-ttu-id="38f4b-145">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="38f4b-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38f4b-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="38f4b-146">Additional resources</span></span>

- [<span data-ttu-id="38f4b-147">全国汽车货运分类 (NMFC) 代码</span><span class="sxs-lookup"><span data-stu-id="38f4b-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="38f4b-148">创建提单</span><span class="sxs-lookup"><span data-stu-id="38f4b-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
