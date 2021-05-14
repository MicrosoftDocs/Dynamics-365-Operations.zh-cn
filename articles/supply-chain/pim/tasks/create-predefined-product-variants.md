---
title: 创建预定义的产品变型
description: 此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938194"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="5077f-103">预定义的产品变型</span><span class="sxs-lookup"><span data-stu-id="5077f-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="5077f-104">示例场景：创建预定义的产品变型</span><span class="sxs-lookup"><span data-stu-id="5077f-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="5077f-105">此示例场景演示如何使用产品维度的组合创建基础产品的产品变型。</span><span class="sxs-lookup"><span data-stu-id="5077f-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="5077f-106">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="5077f-106">Make demo data available</span></span>

<span data-ttu-id="5077f-107">要使用此处建议的值来练习此场景，必须安装演示数据，并且必须选择 *USMF* 法人。</span><span class="sxs-lookup"><span data-stu-id="5077f-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="5077f-108">步骤 1：创建基础产品</span><span class="sxs-lookup"><span data-stu-id="5077f-108">Step 1: Create a product master</span></span>

<span data-ttu-id="5077f-109">创建基础产品：</span><span class="sxs-lookup"><span data-stu-id="5077f-109">To create a product master:</span></span>

1. <span data-ttu-id="5077f-110">转到 **产品信息管理 > 产品 > 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="5077f-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="5077f-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5077f-111">Select **New**.</span></span>
1. <span data-ttu-id="5077f-112">如果 **产品编号** 字段尚未显示数字，则输入一个值。</span><span class="sxs-lookup"><span data-stu-id="5077f-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="5077f-113">仅当未为此字段设置编号规则时才需要此操作。</span><span class="sxs-lookup"><span data-stu-id="5077f-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="5077f-114">在 **产品名称** 字段中输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="5077f-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="5077f-115">在 **产品维度组** 字段中，选择产品维度组 *SizeCol*（尺寸和颜色）。</span><span class="sxs-lookup"><span data-stu-id="5077f-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="5077f-116">选择 **确定** 创建并打开新基础产品。</span><span class="sxs-lookup"><span data-stu-id="5077f-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="5077f-117">步骤 2：添加产品维度</span><span class="sxs-lookup"><span data-stu-id="5077f-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="5077f-118">此示例显示如何手动输入产品维度。</span><span class="sxs-lookup"><span data-stu-id="5077f-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="5077f-119">您还可以选择选择包括您要使用的产品维度值的尺寸、颜色或样式组。</span><span class="sxs-lookup"><span data-stu-id="5077f-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="5077f-120">添加产品维度：</span><span class="sxs-lookup"><span data-stu-id="5077f-120">To add product dimensions:</span></span>

1. <span data-ttu-id="5077f-121">在您的新基础产品仍然打开的情况下，在操作窗格上选择 **产品维度**。</span><span class="sxs-lookup"><span data-stu-id="5077f-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="5077f-122">打开 **尺寸** 选项卡，在工具栏上选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="5077f-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="5077f-123">对新行进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="5077f-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="5077f-124">**尺寸：** 选择一个尺寸值。</span><span class="sxs-lookup"><span data-stu-id="5077f-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="5077f-125">**名称：** 为尺寸输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="5077f-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="5077f-126">在工具栏上选择 **新建**，使用新的 **尺寸** 和 **名称** 向网格添加第二个尺寸。</span><span class="sxs-lookup"><span data-stu-id="5077f-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="5077f-127">打开 **颜色** 选项卡，在工具栏上选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="5077f-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="5077f-128">对新行进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="5077f-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="5077f-129">**颜色：** 选择一个颜色值。</span><span class="sxs-lookup"><span data-stu-id="5077f-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="5077f-130">**名称：** 为颜色输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="5077f-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="5077f-131">在工具栏上选择 **新建**，使用新的 **颜色** 和 **名称** 向网格添加第二个颜色。</span><span class="sxs-lookup"><span data-stu-id="5077f-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="5077f-132">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5077f-132">Select **Save**.</span></span>
1. <span data-ttu-id="5077f-133">关闭页面返回到新基础产品。</span><span class="sxs-lookup"><span data-stu-id="5077f-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="5077f-134">步骤 3：生成产品变型</span><span class="sxs-lookup"><span data-stu-id="5077f-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="5077f-135">此节介绍未启用 *变型建议页改进* 功能时如何生成产品变型。</span><span class="sxs-lookup"><span data-stu-id="5077f-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="5077f-136">有关如何在该功能可用时生成产品变型的详细信息，请参阅下一节。</span><span class="sxs-lookup"><span data-stu-id="5077f-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="5077f-137">生成产品变型：</span><span class="sxs-lookup"><span data-stu-id="5077f-137">To generate product variants:</span></span>

1. <span data-ttu-id="5077f-138">在您的新基础产品仍然打开的情况下，在操作窗格上选择 **产品变型**。</span><span class="sxs-lookup"><span data-stu-id="5077f-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="5077f-139">在操作窗格上选择 **变型建议**。</span><span class="sxs-lookup"><span data-stu-id="5077f-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="5077f-140">系统将生成一个列表，其中包含您为产品定义的尺寸和颜色的所有可能组合。</span><span class="sxs-lookup"><span data-stu-id="5077f-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="5077f-141">在工具栏上选择 **全选**。</span><span class="sxs-lookup"><span data-stu-id="5077f-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="5077f-142">在此示例中，选择所有可能的变型。</span><span class="sxs-lookup"><span data-stu-id="5077f-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="5077f-143">如果您只想使用可能的产品维度组合的子集，则根据需要只选中所需的复选框。</span><span class="sxs-lookup"><span data-stu-id="5077f-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="5077f-144">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="5077f-144">Select **Create**.</span></span>
1. <span data-ttu-id="5077f-145">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5077f-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="5077f-146">改进的变型建议</span><span class="sxs-lookup"><span data-stu-id="5077f-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="5077f-147">*变型建议页改进* 功能将改进 **变型建议** 页，为具有大量产品维度组合的公司解决性能和可用性问题。</span><span class="sxs-lookup"><span data-stu-id="5077f-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="5077f-148">选择要生成变型建议的产品维度值的增强流程可以更快、更轻松地识别和发布相关的产品变型集。</span><span class="sxs-lookup"><span data-stu-id="5077f-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="5077f-149">此功能添加了以下改进：</span><span class="sxs-lookup"><span data-stu-id="5077f-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="5077f-150">**延迟生成变型建议**：**变型建议** 页在您第一次打开时不再显示建议。</span><span class="sxs-lookup"><span data-stu-id="5077f-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="5077f-151">您必须明确选择所需的值，然后选择 **建议** 按钮生成组合。</span><span class="sxs-lookup"><span data-stu-id="5077f-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="5077f-152">这使流程更具可见性和交互性。</span><span class="sxs-lookup"><span data-stu-id="5077f-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="5077f-153">**选择维度值：** 当您有多个维度值时，您通常会希望生成仅包含其中几个维度值的变型建议（如在引入一组新的颜色或样式时）。</span><span class="sxs-lookup"><span data-stu-id="5077f-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="5077f-154">通过改进的设计，您可以选择要生成产品变型建议的维度值。</span><span class="sxs-lookup"><span data-stu-id="5077f-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="5077f-155">这将显著提高所建议变型的相关性，并提高系统性能和用户生产率。</span><span class="sxs-lookup"><span data-stu-id="5077f-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="5077f-156">打开“变型建议页改进”功能</span><span class="sxs-lookup"><span data-stu-id="5077f-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="5077f-157">*变型建议页改进* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="5077f-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5077f-158">管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="5077f-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="5077f-159">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="5077f-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5077f-160">**模块**：*产品信息管理*</span><span class="sxs-lookup"><span data-stu-id="5077f-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="5077f-161">**功能名称**：*变型建议页改进*</span><span class="sxs-lookup"><span data-stu-id="5077f-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="5077f-162">使用改进的变型建议</span><span class="sxs-lookup"><span data-stu-id="5077f-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="5077f-163">在启用 *变型建议页改进* 功能时生成产品变型建议：</span><span class="sxs-lookup"><span data-stu-id="5077f-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="5077f-164">如上一节所述，打开或创建基础产品并向其添加所需的产品维度。</span><span class="sxs-lookup"><span data-stu-id="5077f-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="5077f-165">在基础产品打开的情况下，在操作窗格上选择 **产品变型**。</span><span class="sxs-lookup"><span data-stu-id="5077f-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="5077f-166">在操作窗格上选择 **变型建议**。</span><span class="sxs-lookup"><span data-stu-id="5077f-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="5077f-167">选择要用于每个维度的值。</span><span class="sxs-lookup"><span data-stu-id="5077f-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="5077f-168">在顶部工具栏上，选择 **建议**。</span><span class="sxs-lookup"><span data-stu-id="5077f-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="5077f-169">系统将生成一个列表，其中包含您选择的尺寸和颜色的所有可能组合。</span><span class="sxs-lookup"><span data-stu-id="5077f-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="5077f-170">在 **建议的变型** 快速选项卡上，选中要使用的每个产品维度组合的复选框，或在工具栏上选择 **全选** 全部选择。</span><span class="sxs-lookup"><span data-stu-id="5077f-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="5077f-171">选择 **创建** 将变型添加到当前的基础产品中。</span><span class="sxs-lookup"><span data-stu-id="5077f-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
