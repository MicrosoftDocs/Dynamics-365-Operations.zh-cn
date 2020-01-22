---
title: 按照产品变型的度量单位转换
description: 本主题说明如何在产品变型中设置度量单位转换。
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935091"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="cb81c-103">按照产品变型的度量单位转换</span><span class="sxs-lookup"><span data-stu-id="cb81c-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb81c-104">本主题说明如何在产品变型中设置度量单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="cb81c-105">其中包括设置示例。</span><span class="sxs-lookup"><span data-stu-id="cb81c-105">It includes an example of the setup.</span></span>

<span data-ttu-id="cb81c-106">此功能使公司可以定义同一产品变型之间的不同单位换算。</span><span class="sxs-lookup"><span data-stu-id="cb81c-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="cb81c-107">以下示例将用于此主题。</span><span class="sxs-lookup"><span data-stu-id="cb81c-107">The following example is used in this topic.</span></span> <span data-ttu-id="cb81c-108">公司销售小、中、大和特大号 T 恤。</span><span class="sxs-lookup"><span data-stu-id="cb81c-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="cb81c-109">T 恤被定义作为产品，不同的尺寸被定义为产品变型。</span><span class="sxs-lookup"><span data-stu-id="cb81c-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="cb81c-110">T 恤按箱打包，一箱可以有五件 T 恤，除了特大号外，只剩放四件 T 恤的空间。</span><span class="sxs-lookup"><span data-stu-id="cb81c-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="cb81c-111">公司想要以单位**件**跟踪不同的 T 恤变型，但以单位**箱**销售 T 恤。</span><span class="sxs-lookup"><span data-stu-id="cb81c-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="cb81c-112">库存单位和销售单位之间的转换为 1 箱 = 5 件，除了变型“特大号”外，转换为 1 箱 = 4 件。</span><span class="sxs-lookup"><span data-stu-id="cb81c-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="cb81c-113">按变型为单位转换设置产品</span><span class="sxs-lookup"><span data-stu-id="cb81c-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="cb81c-114">产品变型只能为**产品子类型**：**产品基础**的产品创建。</span><span class="sxs-lookup"><span data-stu-id="cb81c-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="cb81c-115">有关详细信息，请参阅[创建基础产品](tasks/create-product-master.md)。</span><span class="sxs-lookup"><span data-stu-id="cb81c-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="cb81c-116">此功能没有为为实际称重流程设置的产品启用。</span><span class="sxs-lookup"><span data-stu-id="cb81c-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="cb81c-117">当创建具有已发布产品变型的基础产品时，可以设置每个变型的单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="cb81c-118">您可以在以下页面找到用于在产品或产品变型上下文中打开单位转换页面的菜单项。</span><span class="sxs-lookup"><span data-stu-id="cb81c-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="cb81c-119">**产品详细信息**页面</span><span class="sxs-lookup"><span data-stu-id="cb81c-119">**Product details** page</span></span>
-   <span data-ttu-id="cb81c-120">**已发布产品详细信息**页面</span><span class="sxs-lookup"><span data-stu-id="cb81c-120">**Released products details** page</span></span>
-   <span data-ttu-id="cb81c-121">**已发布产品变型**页面</span><span class="sxs-lookup"><span data-stu-id="cb81c-121">**Released product variants** page</span></span>

<span data-ttu-id="cb81c-122">当您在基础产品或已发布产品变型的上下文中打开**单位转换**页时，您可以选择是否要为产品或产品变型设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="cb81c-123">您通过在**创建转换的对象**字段中选择**产品变型**或**产品**来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="cb81c-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="cb81c-124">产品变型</span><span class="sxs-lookup"><span data-stu-id="cb81c-124">Product variant</span></span>

<span data-ttu-id="cb81c-125">如果您选择**产品变型**，那么您可以在**产品变型**字段中选择要为其设置单位转换的变型。</span><span class="sxs-lookup"><span data-stu-id="cb81c-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="cb81c-126">产品</span><span class="sxs-lookup"><span data-stu-id="cb81c-126">Product</span></span>

<span data-ttu-id="cb81c-127">如果您选择**产品**，则可以为基础产品设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="cb81c-128">此单位转换将应用于未定义单位转换的所有产品变型。</span><span class="sxs-lookup"><span data-stu-id="cb81c-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="cb81c-129">示例</span><span class="sxs-lookup"><span data-stu-id="cb81c-129">Example</span></span>

<span data-ttu-id="cb81c-130">基础产品 **T 恤**有四个已发布的产品变型：小、中、大和特大。</span><span class="sxs-lookup"><span data-stu-id="cb81c-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="cb81c-131">T 恤按箱打包，一箱可以有五件 T 恤，除了特大号外，只剩放四件 T 恤的空间。</span><span class="sxs-lookup"><span data-stu-id="cb81c-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="cb81c-132">首先，请从 **T 恤**的“已发放产品详细信息”页打开**单位转换**页。</span><span class="sxs-lookup"><span data-stu-id="cb81c-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="cb81c-133">在**单位转换**页上，为已发布的产品变型“特大”设置单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="cb81c-134">**字段**</span><span class="sxs-lookup"><span data-stu-id="cb81c-134">**Field**</span></span>             | <span data-ttu-id="cb81c-135">**设置**</span><span class="sxs-lookup"><span data-stu-id="cb81c-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="cb81c-136">创建转换的对象</span><span class="sxs-lookup"><span data-stu-id="cb81c-136">Create conversion for</span></span> | <span data-ttu-id="cb81c-137">产品变型</span><span class="sxs-lookup"><span data-stu-id="cb81c-137">Product variant</span></span>         |
| <span data-ttu-id="cb81c-138">产品变型</span><span class="sxs-lookup"><span data-stu-id="cb81c-138">Product variant</span></span>       | <span data-ttu-id="cb81c-139">T 恤 : : 特大 : :</span><span class="sxs-lookup"><span data-stu-id="cb81c-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="cb81c-140">源单位</span><span class="sxs-lookup"><span data-stu-id="cb81c-140">From unit</span></span>             | <span data-ttu-id="cb81c-141">箱</span><span class="sxs-lookup"><span data-stu-id="cb81c-141">Boxes</span></span>                   |
| <span data-ttu-id="cb81c-142">系数</span><span class="sxs-lookup"><span data-stu-id="cb81c-142">Factor</span></span>                | <span data-ttu-id="cb81c-143">4</span><span class="sxs-lookup"><span data-stu-id="cb81c-143">4</span></span>                       |
| <span data-ttu-id="cb81c-144">目标单位</span><span class="sxs-lookup"><span data-stu-id="cb81c-144">To Unit</span></span>               | <span data-ttu-id="cb81c-145">件</span><span class="sxs-lookup"><span data-stu-id="cb81c-145">Pieces</span></span>                  |

<span data-ttu-id="cb81c-146">已发布的产品变型“小、中和大”在“箱”和“件”之间具有相同的单位转换，也就是说，您可以为基础产品的这些产品变型定义单位转换。</span><span class="sxs-lookup"><span data-stu-id="cb81c-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="cb81c-147">**字段**</span><span class="sxs-lookup"><span data-stu-id="cb81c-147">**Field**</span></span>             | <span data-ttu-id="cb81c-148">**设置**</span><span class="sxs-lookup"><span data-stu-id="cb81c-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="cb81c-149">创建转换的对象</span><span class="sxs-lookup"><span data-stu-id="cb81c-149">Create conversion for</span></span> | <span data-ttu-id="cb81c-150">产品</span><span class="sxs-lookup"><span data-stu-id="cb81c-150">Product</span></span>     |
| <span data-ttu-id="cb81c-151">产品</span><span class="sxs-lookup"><span data-stu-id="cb81c-151">Product</span></span>               | <span data-ttu-id="cb81c-152">T 恤</span><span class="sxs-lookup"><span data-stu-id="cb81c-152">T-Shirt</span></span>     |
| <span data-ttu-id="cb81c-153">源单位</span><span class="sxs-lookup"><span data-stu-id="cb81c-153">From unit</span></span>             | <span data-ttu-id="cb81c-154">箱</span><span class="sxs-lookup"><span data-stu-id="cb81c-154">Boxes</span></span>       |
| <span data-ttu-id="cb81c-155">系数</span><span class="sxs-lookup"><span data-stu-id="cb81c-155">Factor</span></span>                | <span data-ttu-id="cb81c-156">5</span><span class="sxs-lookup"><span data-stu-id="cb81c-156">5</span></span>           |
| <span data-ttu-id="cb81c-157">目标单位</span><span class="sxs-lookup"><span data-stu-id="cb81c-157">To Unit</span></span>               | <span data-ttu-id="cb81c-158">件</span><span class="sxs-lookup"><span data-stu-id="cb81c-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="cb81c-159">使用 Excel 更新单位转换</span><span class="sxs-lookup"><span data-stu-id="cb81c-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="cb81c-160">如果产品有多个具有不同单位转换的产品变型，从**单位转换**页将单位转换导出到 Excel 电子表格，更新转换，然后将其发布回 Supply Chain Management 是一个好主意。</span><span class="sxs-lookup"><span data-stu-id="cb81c-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="cb81c-161">导出到 Excel 并将编辑发布回 Supply Chain Mangement 的选项从**单位转换**页的“操作窗格”上的**在 Microsoft office 中打开**菜单项启用。</span><span class="sxs-lookup"><span data-stu-id="cb81c-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
