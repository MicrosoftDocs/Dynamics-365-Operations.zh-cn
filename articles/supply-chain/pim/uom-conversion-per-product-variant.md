---
title: 按照产品变型的度量单位转换
description: 本主题说明如何为产品变型设置度量单位转换。 其中包括设置示例。
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423286"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="4ff99-104">按照产品变型的度量单位转换</span><span class="sxs-lookup"><span data-stu-id="4ff99-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ff99-105">本主题说明如何为各种产品变型设置度量单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="4ff99-106">您可以使用产品变型创建单个产品的差异，而不是创建多个必须维护的单品。</span><span class="sxs-lookup"><span data-stu-id="4ff99-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="4ff99-107">例如，指定尺寸和颜色的 T 恤就是一个产品变型。</span><span class="sxs-lookup"><span data-stu-id="4ff99-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="4ff99-108">以前只能为基础产品设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="4ff99-109">因此，所有产品变型的单位转换规则都相同。</span><span class="sxs-lookup"><span data-stu-id="4ff99-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="4ff99-110">但是，如果开启了 *产品变型的度量单位转换* 功能，并且您的 T 恤成箱出售，而一箱中可容纳的 T 恤数量取决于 T 恤的尺寸，现在可以设置不同 T 恤的尺寸与包装箱之间的单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="4ff99-111">在系统中开启此功能</span><span class="sxs-lookup"><span data-stu-id="4ff99-111">Turn on the feature in your system</span></span>

<span data-ttu-id="4ff99-112">如果尚未在系统中看到此功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，然后开启 *产品变型的度量单位转换* 功能。</span><span class="sxs-lookup"><span data-stu-id="4ff99-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="4ff99-113">按变型为单位转换设置产品</span><span class="sxs-lookup"><span data-stu-id="4ff99-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="4ff99-114">只能为基础产品创建产品变型。</span><span class="sxs-lookup"><span data-stu-id="4ff99-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="4ff99-115">有关详细信息，请参阅[创建基础产品](tasks/create-product-master.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff99-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="4ff99-116">为实际称重流程设置的产品不支持 *产品变型的度量单位转换* 功能。</span><span class="sxs-lookup"><span data-stu-id="4ff99-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="4ff99-117">若要将基础产品配置为支持按变型的单位转换，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4ff99-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="4ff99-118">转到 **产品信息管理 \> 产品 \> 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="4ff99-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="4ff99-119">创建或打开一个基础产品以转到其 **产品详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="4ff99-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="4ff99-120">将 **启用度量单位转换** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="4ff99-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="4ff99-121">在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **单位转换**。</span><span class="sxs-lookup"><span data-stu-id="4ff99-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="4ff99-122">将打开 **单位转换** 页。</span><span class="sxs-lookup"><span data-stu-id="4ff99-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="4ff99-123">选择以下选项卡之一：</span><span class="sxs-lookup"><span data-stu-id="4ff99-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="4ff99-124">**类别内部转换** – 如果要在属于同一个单位类别的单位之间转换，请选择此选项卡。</span><span class="sxs-lookup"><span data-stu-id="4ff99-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="4ff99-125">**类别之间的转换** – 如果要在属于不同单位类别的单位之间转换，请选择此选项卡。</span><span class="sxs-lookup"><span data-stu-id="4ff99-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="4ff99-126">选择 **新建** 添加新的单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="4ff99-127">将 **创建转换的对象** 字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="4ff99-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="4ff99-128">**产品** – 如果您选择此值，则可以为基础产品设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="4ff99-129">此单位转换用作没有为其定义任何单位转换的所有产品变型的应变计划。</span><span class="sxs-lookup"><span data-stu-id="4ff99-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="4ff99-130">**产品变型** – 如果您选择此值，则可以为特定产品变型设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="4ff99-131">请使用 **产品变型** 字段选择变型。</span><span class="sxs-lookup"><span data-stu-id="4ff99-131">Use the **Product variant** field to select the variant.</span></span>

    ![![添加新单位转换](media/uom-new-conversion.png "添加新单位转换")](media/uom-new-conversion.png "Adding a new unit conversion")

1. <span data-ttu-id="4ff99-133">请使用提供的其他字段设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="4ff99-134">选择 **确定** 保存新单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="4ff99-135">可以从下面的任何页面打开产品或产品变型的 **单位转换** 页：</span><span class="sxs-lookup"><span data-stu-id="4ff99-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="4ff99-136">产品详细信息</span><span class="sxs-lookup"><span data-stu-id="4ff99-136">Product details</span></span>
> - <span data-ttu-id="4ff99-137">已发布产品详细信息</span><span class="sxs-lookup"><span data-stu-id="4ff99-137">Released products details</span></span>
> - <span data-ttu-id="4ff99-138">已发布的产品变型</span><span class="sxs-lookup"><span data-stu-id="4ff99-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4ff99-139">示例场景</span><span class="sxs-lookup"><span data-stu-id="4ff99-139">Example scenario</span></span>

<span data-ttu-id="4ff99-140">在此方案中，一家公司公司销售小、中、大和特大号 T 恤。</span><span class="sxs-lookup"><span data-stu-id="4ff99-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="4ff99-141">T 恤被定义作为产品，不同的尺寸被定义为该产品的变型。</span><span class="sxs-lookup"><span data-stu-id="4ff99-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="4ff99-142">T 恤装在箱子里。</span><span class="sxs-lookup"><span data-stu-id="4ff99-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="4ff99-143">如果是小、中和大尺寸，每箱可以有五件。</span><span class="sxs-lookup"><span data-stu-id="4ff99-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="4ff99-144">但是，如果是特大尺寸，则每箱的空间只能放四件。</span><span class="sxs-lookup"><span data-stu-id="4ff99-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="4ff99-145">公司想要以单位 *件* 跟踪不同变型，但以单位 *箱* 销售。</span><span class="sxs-lookup"><span data-stu-id="4ff99-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="4ff99-146">对于小、中和大尺寸，库存单位与销售单位之间的转换为 1 箱 = 5 件。</span><span class="sxs-lookup"><span data-stu-id="4ff99-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="4ff99-147">对于特大尺寸，转换为 1 箱= 4 件。</span><span class="sxs-lookup"><span data-stu-id="4ff99-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="4ff99-148">从 **T 恤** 产品的 **已发布产品详细信息** 页，打开 **单位转换** 页。</span><span class="sxs-lookup"><span data-stu-id="4ff99-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="4ff99-149">在 **单位转换** 页，为 **特大** 已发布产品变型设置以下单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="4ff99-150">字段</span><span class="sxs-lookup"><span data-stu-id="4ff99-150">Field</span></span>                 | <span data-ttu-id="4ff99-151">设置</span><span class="sxs-lookup"><span data-stu-id="4ff99-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="4ff99-152">创建转换的对象</span><span class="sxs-lookup"><span data-stu-id="4ff99-152">Create conversion for</span></span> | <span data-ttu-id="4ff99-153">产品变型</span><span class="sxs-lookup"><span data-stu-id="4ff99-153">Product variant</span></span>         |
    | <span data-ttu-id="4ff99-154">产品变型</span><span class="sxs-lookup"><span data-stu-id="4ff99-154">Product variant</span></span>       | <span data-ttu-id="4ff99-155">T 恤 : : 特大 : :</span><span class="sxs-lookup"><span data-stu-id="4ff99-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="4ff99-156">源单位</span><span class="sxs-lookup"><span data-stu-id="4ff99-156">From unit</span></span>             | <span data-ttu-id="4ff99-157">箱</span><span class="sxs-lookup"><span data-stu-id="4ff99-157">Boxes</span></span>                   |
    | <span data-ttu-id="4ff99-158">系数</span><span class="sxs-lookup"><span data-stu-id="4ff99-158">Factor</span></span>                | <span data-ttu-id="4ff99-159">4</span><span class="sxs-lookup"><span data-stu-id="4ff99-159">4</span></span>                       |
    | <span data-ttu-id="4ff99-160">目标单位</span><span class="sxs-lookup"><span data-stu-id="4ff99-160">To Unit</span></span>               | <span data-ttu-id="4ff99-161">件</span><span class="sxs-lookup"><span data-stu-id="4ff99-161">Pieces</span></span>                  |

1. <span data-ttu-id="4ff99-162">因为 **小**、**中** 和 **大** 产品变型全部在单位 *箱* 和 *件* 之间具有相同的单位转换，所以您可以在基础产品中为这些产品变型定义以下单位转换。</span><span class="sxs-lookup"><span data-stu-id="4ff99-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="4ff99-163">字段</span><span class="sxs-lookup"><span data-stu-id="4ff99-163">Field</span></span>                 | <span data-ttu-id="4ff99-164">设置</span><span class="sxs-lookup"><span data-stu-id="4ff99-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="4ff99-165">创建转换的对象</span><span class="sxs-lookup"><span data-stu-id="4ff99-165">Create conversion for</span></span> | <span data-ttu-id="4ff99-166">产品</span><span class="sxs-lookup"><span data-stu-id="4ff99-166">Product</span></span> |
    | <span data-ttu-id="4ff99-167">产品</span><span class="sxs-lookup"><span data-stu-id="4ff99-167">Product</span></span>               | <span data-ttu-id="4ff99-168">T 恤</span><span class="sxs-lookup"><span data-stu-id="4ff99-168">T-Shirt</span></span> |
    | <span data-ttu-id="4ff99-169">源单位</span><span class="sxs-lookup"><span data-stu-id="4ff99-169">From unit</span></span>             | <span data-ttu-id="4ff99-170">箱</span><span class="sxs-lookup"><span data-stu-id="4ff99-170">Boxes</span></span>   |
    | <span data-ttu-id="4ff99-171">系数</span><span class="sxs-lookup"><span data-stu-id="4ff99-171">Factor</span></span>                | <span data-ttu-id="4ff99-172">5</span><span class="sxs-lookup"><span data-stu-id="4ff99-172">5</span></span>       |
    | <span data-ttu-id="4ff99-173">目标单位</span><span class="sxs-lookup"><span data-stu-id="4ff99-173">To Unit</span></span>               | <span data-ttu-id="4ff99-174">件</span><span class="sxs-lookup"><span data-stu-id="4ff99-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="4ff99-175">使用 Excel 更新单位转换</span><span class="sxs-lookup"><span data-stu-id="4ff99-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="4ff99-176">如果一个产品有大量采用不同单位转换的产品变型，最好将这些单位转换导出到 Microsoft Excel 工作簿，更新，然后发布回 Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="4ff99-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4ff99-177">若要将单位转换导出到 Excel，请在 **单位转换** 页的操作窗格上，选择 **在 Microsoft Office 中打开**。</span><span class="sxs-lookup"><span data-stu-id="4ff99-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ff99-178">其他资源</span><span class="sxs-lookup"><span data-stu-id="4ff99-178">Additional resources</span></span>

[<span data-ttu-id="4ff99-179">管理度量单位</span><span class="sxs-lookup"><span data-stu-id="4ff99-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
