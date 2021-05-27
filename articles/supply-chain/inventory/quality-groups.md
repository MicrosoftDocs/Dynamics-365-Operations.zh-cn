---
title: 物料质量组
description: 本主题介绍如何使用和创建物料质量组来对产品进行逻辑分组，以便可以将其分配给质量关联来自动生成质检订单。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022244"
---
# <a name="item-quality-groups"></a><span data-ttu-id="b5119-103">物料质量组</span><span class="sxs-lookup"><span data-stu-id="b5119-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5119-104">质量组表示物料的公共测试要求。</span><span class="sxs-lookup"><span data-stu-id="b5119-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b5119-105">本主题介绍如何使用和创建物料质量组来对产品进行逻辑分组，以便可以将其分配给质量关联来自动生成质检订单。</span><span class="sxs-lookup"><span data-stu-id="b5119-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="b5119-106">要设置、编辑和查看分配给质量组的物料或分配给物料的质量组，转到 **库存管理 \> 设置 \> 质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="b5119-107">在 **测试组** 页上定义测试要求后，您可以定义用于自动生成质检订单的规则。</span><span class="sxs-lookup"><span data-stu-id="b5119-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b5119-108">为了简化该流程，您不为各个物料定义规则。</span><span class="sxs-lookup"><span data-stu-id="b5119-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="b5119-109">而是可以在 **质量关联** 页为质量组定义规则。</span><span class="sxs-lookup"><span data-stu-id="b5119-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="b5119-110">物料质量组示例</span><span class="sxs-lookup"><span data-stu-id="b5119-110">Example of an item quality group</span></span>

<span data-ttu-id="b5119-111">某制造公司采购的多种原材料具有相同的进货检查测试要求。</span><span class="sxs-lookup"><span data-stu-id="b5119-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b5119-112">因此，公司定义了一个质量组，然后将与原材料关联的物料编号分配给该组。</span><span class="sxs-lookup"><span data-stu-id="b5119-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b5119-113">之后，公司采购一个新类型的原材料，具有相同的测试要求。</span><span class="sxs-lookup"><span data-stu-id="b5119-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b5119-114">公司不是为新物料设置新的测试要求，而是将新物料的物料编号添加到现有的质量组。</span><span class="sxs-lookup"><span data-stu-id="b5119-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="b5119-115">这家公司还生产具有相同测试要求的物料，并装运具有相同装运前测试要求的物料。</span><span class="sxs-lookup"><span data-stu-id="b5119-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b5119-116">因此，公司定义两个附加质量组，然后将相关物料编号分配给每个组。</span><span class="sxs-lookup"><span data-stu-id="b5119-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="b5119-117">创建质检组</span><span class="sxs-lookup"><span data-stu-id="b5119-117">Create a quality group</span></span>

<span data-ttu-id="b5119-118">要创建质量组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b5119-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b5119-119">转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b5119-120">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b5119-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b5119-121">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="b5119-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b5119-122">**质量组** – 为质量组输入唯一 ID 或名称。</span><span class="sxs-lookup"><span data-stu-id="b5119-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="b5119-123">**描述** – 输入质量组的详细描述。</span><span class="sxs-lookup"><span data-stu-id="b5119-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="b5119-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b5119-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="b5119-125">手动向质量组添加物料</span><span class="sxs-lookup"><span data-stu-id="b5119-125">Manually add items to a quality group</span></span>

<span data-ttu-id="b5119-126">要手动向质量组添加物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5119-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b5119-127">转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b5119-128">选择要添加物料的质量组。</span><span class="sxs-lookup"><span data-stu-id="b5119-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="b5119-129">在操作窗格上，选择 **物料**。</span><span class="sxs-lookup"><span data-stu-id="b5119-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="b5119-130">在 **质量组中的物料** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="b5119-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b5119-131">然后，对于新行，将 **物料编号** 字段设置为要添加的物料编号。</span><span class="sxs-lookup"><span data-stu-id="b5119-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="b5119-132">对必须添加的其他每个物料重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="b5119-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="b5119-133">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="b5119-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="b5119-134">向质量组添加多个物料</span><span class="sxs-lookup"><span data-stu-id="b5119-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="b5119-135">要向质量组添加多个物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5119-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b5119-136">转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b5119-137">创建或选择要添加物料的质量组。</span><span class="sxs-lookup"><span data-stu-id="b5119-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="b5119-138">在操作窗格上，选择 **添加物料**。</span><span class="sxs-lookup"><span data-stu-id="b5119-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="b5119-139">在 **查询** 对话框中，输入要添加的物料的筛选条件。</span><span class="sxs-lookup"><span data-stu-id="b5119-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="b5119-140">例如，您可以筛选特定物料组中的所有物料。</span><span class="sxs-lookup"><span data-stu-id="b5119-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="b5119-141">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5119-141">Select **OK**.</span></span>
1. <span data-ttu-id="b5119-142">在 **添加物料** 对话框中，网格将显示与查询匹配的所有物料。</span><span class="sxs-lookup"><span data-stu-id="b5119-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="b5119-143">查看结果。</span><span class="sxs-lookup"><span data-stu-id="b5119-143">Review the results.</span></span>

    <span data-ttu-id="b5119-144">如果需要任何更改，选择 **选择** 返回到 **查询** 对话框，然后调整您的查询。</span><span class="sxs-lookup"><span data-stu-id="b5119-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="b5119-145">当结果包括要添加的所有物料时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b5119-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="b5119-146">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b5119-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="b5119-147">手动将物料与质量组关联</span><span class="sxs-lookup"><span data-stu-id="b5119-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="b5119-148">要手动将物料与质量组关联，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5119-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b5119-149">转到 **库存管理 \> 设置 \> 质量控制 \> 物料质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="b5119-150">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b5119-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b5119-151">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="b5119-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b5119-152">**物料编号** – 选择要添加的物料编号。</span><span class="sxs-lookup"><span data-stu-id="b5119-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="b5119-153">**质量组** – 选择要分配给物料的质量组。</span><span class="sxs-lookup"><span data-stu-id="b5119-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="b5119-154">对必须添加的物料和质量组的每个其他组合重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="b5119-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="b5119-155">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="b5119-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="b5119-156">从“已发布产品”页手动添加质量组</span><span class="sxs-lookup"><span data-stu-id="b5119-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="b5119-157">要从 **已发布产品** 页手动添加质量组，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b5119-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="b5119-158">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="b5119-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b5119-159">选择您要向其分配质量组的产品。</span><span class="sxs-lookup"><span data-stu-id="b5119-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="b5119-160">在操作窗格上 **管理库存** 选项卡的 **质量** 组中，选择 **物料质量组**。</span><span class="sxs-lookup"><span data-stu-id="b5119-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="b5119-161">在 **质量组中的物料** 页上的操作窗格上，选择 **新建** 在网格中添加一行。</span><span class="sxs-lookup"><span data-stu-id="b5119-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b5119-162">然后，对于新行，将 **质量组** 字段设置为要分配给产品的质量组。</span><span class="sxs-lookup"><span data-stu-id="b5119-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="b5119-163">对要分配给产品的每个其他质量组重复上一个步骤。</span><span class="sxs-lookup"><span data-stu-id="b5119-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="b5119-164">关闭页面。</span><span class="sxs-lookup"><span data-stu-id="b5119-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5119-165">其他资源</span><span class="sxs-lookup"><span data-stu-id="b5119-165">Additional resources</span></span>

- [<span data-ttu-id="b5119-166">质量管理测试仪器</span><span class="sxs-lookup"><span data-stu-id="b5119-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="b5119-167">质量管理测试</span><span class="sxs-lookup"><span data-stu-id="b5119-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="b5119-168">质量管理测试组</span><span class="sxs-lookup"><span data-stu-id="b5119-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="b5119-169">质量管理测试变量</span><span class="sxs-lookup"><span data-stu-id="b5119-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="b5119-170">质量关联</span><span class="sxs-lookup"><span data-stu-id="b5119-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
