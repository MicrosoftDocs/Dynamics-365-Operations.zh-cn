---
title: 物料清单设计器功能
description: 本主题介绍如何使用物料清单设计器页设计和使用物料清单 (BOM) 的树状结构。
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c97e58f6f608efd3b964e7fad229a00e1ae603a
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677823"
---
# <a name="bom-designer-functionality"></a><span data-ttu-id="47f0a-103">物料清单设计器功能</span><span class="sxs-lookup"><span data-stu-id="47f0a-103">BOM designer functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47f0a-104">本主题介绍如何使用物料清单设计器页设计和使用物料清单 (BOM) 的树状结构。</span><span class="sxs-lookup"><span data-stu-id="47f0a-104">This topic describes how you can use the BOM designer page to design and work with tree structures for bills of materials (BOMs).</span></span> <span data-ttu-id="47f0a-105">您可以单击“设置”选择不同的配置并指定要在树的行上显示哪些信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-105">You can click Setup to select different configurations and specify what information appears on the lines of the tree.</span></span>

<span data-ttu-id="47f0a-106">从**已发布产品**页打开**物料清单设计器**页后，后者将显示对所选物料有效且针对所选物料进行了审核的物料清单 (BOM) 的层次结构、物料的默认订单站点和实际日期。</span><span class="sxs-lookup"><span data-stu-id="47f0a-106">When you open the **BOM designer** page from the **Released products** page, it displays the hierarchy of bills of materials (BOMs) that are active and approved for the selected item, the default order site of the item, and the actual date.</span></span>  

<span data-ttu-id="47f0a-107">单击**筛选器**以更改视图中的初始选择。</span><span class="sxs-lookup"><span data-stu-id="47f0a-107">Click **Filter** to change the initial selection in the view.</span></span> <span data-ttu-id="47f0a-108">通过将显示原则设置为**选定/有效或选定**，您可以选择要在视图中使用的单个物料清单和工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-108">By setting the display principle to **Selected/Active or Selected**, you can select individual BOM or route versions to use in the view.</span></span> <span data-ttu-id="47f0a-109">您可以选择要在物料清单设计器中显示或维护的尚未审核和无效的物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-109">You can select non-approved and non-active BOM versions to show or maintain in the BOM designer.</span></span>  

<span data-ttu-id="47f0a-110">**注意：** 如果您从**物料清单**列表页打开了物料清单设计器，该设计器不会显示工艺路线信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-110">**Note:** If you open the BOM designer from the **Bills of materials** list page, it doesn't display route information.</span></span> <span data-ttu-id="47f0a-111">当前，物料清单或工艺路线版本的选择是物料清单和工艺路线版本的属性，适用于物料清单设计器的所有实例。</span><span class="sxs-lookup"><span data-stu-id="47f0a-111">Currently, the selection of a BOM or route version is a property of the BOM and route version, and applies to all instances of the BOM designer.</span></span>  

<span data-ttu-id="47f0a-112">以下各节将介绍物料清单设计器的各个选项卡上可用的功能。</span><span class="sxs-lookup"><span data-stu-id="47f0a-112">The following sections describe the functionality that is available on the various tabs of the BOM designer.</span></span>

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a><span data-ttu-id="47f0a-113">使用物料清单设计器分析物料清单结构</span><span class="sxs-lookup"><span data-stu-id="47f0a-113">Analyzing a BOM structure by using the BOM designer</span></span>
<span data-ttu-id="47f0a-114">物料清单设计器有两个部分：</span><span class="sxs-lookup"><span data-stu-id="47f0a-114">The BOM designer has two sections:</span></span>

-   <span data-ttu-id="47f0a-115">物料清单结构的树视图。</span><span class="sxs-lookup"><span data-stu-id="47f0a-115">The tree view of the BOM structure.</span></span>
-   <span data-ttu-id="47f0a-116">详细信息部分中，显示所选数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-116">The details section, which shows details of the selected data.</span></span> <span data-ttu-id="47f0a-117">当您选择树视图中的节点时，详细信息部分中的 FastTabs 将基于该节点进行更新：</span><span class="sxs-lookup"><span data-stu-id="47f0a-117">When you select a node in the tree view, the FastTabs in the details section are updated based on that node:</span></span>
    -   <span data-ttu-id="47f0a-118">**物料清单行详细信息** - 显示在树视图中选择的物料清单行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-118">**BOM line details** – Shows the details of the BOM line that is selected in the tree view.</span></span>
    -   <span data-ttu-id="47f0a-119">**物料数据** - 显示在所选节点中使用的主要物料的详细信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-119">**Item data** – Shows the details of the main item or the item that is used in the selected node.</span></span> <span data-ttu-id="47f0a-120">您可以单击**编辑已发布产品**以维护所选物料。</span><span class="sxs-lookup"><span data-stu-id="47f0a-120">You can click **Edit released product** to maintain the selected item.</span></span>
    -   <span data-ttu-id="47f0a-121">**物料清单** - 显示与所选节点相关的物料清单的标题。</span><span class="sxs-lookup"><span data-stu-id="47f0a-121">**BOM** – Shows the header of the BOM that is related to the selected node.</span></span>
    -   <span data-ttu-id="47f0a-122">**工艺路线** - 显示与所选节点相关的工艺路线的标题。</span><span class="sxs-lookup"><span data-stu-id="47f0a-122">**Route** – Shows the header of the route that is related to the selected node.</span></span>
    -   <span data-ttu-id="47f0a-123">**工艺路线工序** -显示工艺路线的工序的预览。</span><span class="sxs-lookup"><span data-stu-id="47f0a-123">**Route operations** – Shows a preview of the operations for the route.</span></span> <span data-ttu-id="47f0a-124">当物料清单行分配给所选的特定工序后，该工序将标记为**工序中需要的组件**。</span><span class="sxs-lookup"><span data-stu-id="47f0a-124">When a BOM line that is assigned to a specific operation is selected, the operation is marked as **Component needed at operations**.</span></span>

## <a name="selecting-a-bom-and-route"></a><span data-ttu-id="47f0a-125">选择物料清单和工艺路线</span><span class="sxs-lookup"><span data-stu-id="47f0a-125">Selecting a BOM and route</span></span>
<span data-ttu-id="47f0a-126">为物料清单和工艺路线应用的筛选器将显示在物料清单设计器的标题中。</span><span class="sxs-lookup"><span data-stu-id="47f0a-126">The filter that is applied for the BOM and route is displayed in the header of the BOM designer.</span></span> <span data-ttu-id="47f0a-127">您可以使用**筛选器**对话框更改筛选器。</span><span class="sxs-lookup"><span data-stu-id="47f0a-127">You can change the filter by using the **Filter** dialog box.</span></span> <span data-ttu-id="47f0a-128">下表描述了此对话框中的字段。</span><span class="sxs-lookup"><span data-stu-id="47f0a-128">The following table describes the fields in this dialog box.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="47f0a-129">字段</span><span class="sxs-lookup"><span data-stu-id="47f0a-129">Field</span></span></th>
<th><span data-ttu-id="47f0a-130">描述</span><span class="sxs-lookup"><span data-stu-id="47f0a-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="47f0a-131">产品维度</span><span class="sxs-lookup"><span data-stu-id="47f0a-131">Product dimensions</span></span></td>
<td><span data-ttu-id="47f0a-132">如果选中的成品是基础产品，您可以定义主要选择的可用产品维度。</span><span class="sxs-lookup"><span data-stu-id="47f0a-132">If the selected finished product is a product master, you can define the active product dimensions for the main selection.</span></span> <span data-ttu-id="47f0a-133"><strong>注意：</strong>如果您为其打开物料清单设计器的产品不是基础产品，则在<strong>筛选器</strong>对话框中无法选择产品维度。</span><span class="sxs-lookup"><span data-stu-id="47f0a-133"><strong>Note:</strong> If you open the BOM designer for a product that isn&#39;t a product master, no product dimensions can be selected in the <strong>Filter</strong> dialog box.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f0a-134">站点</span><span class="sxs-lookup"><span data-stu-id="47f0a-134">Site</span></span></td>
<td><span data-ttu-id="47f0a-135">更改为其显示物料清单树的站点。</span><span class="sxs-lookup"><span data-stu-id="47f0a-135">Change the site that the BOM tree is displayed for.</span></span> <span data-ttu-id="47f0a-136">默认站点是成品的默认库存值。</span><span class="sxs-lookup"><span data-stu-id="47f0a-136">The default site is the default inventory site of the finished item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47f0a-137">显示原则</span><span class="sxs-lookup"><span data-stu-id="47f0a-137">Display principle</span></span></td>
<td><span data-ttu-id="47f0a-138">选择应用于当前物料清单结构和当前工艺路线的版本显示原则：</span><span class="sxs-lookup"><span data-stu-id="47f0a-138">Select the version display principle that applies to the current BOM structure and the current route:</span></span>
<ul>
<li><span data-ttu-id="47f0a-139">当该原则设置为<strong>有效或选定/有效</strong>时，将找到此日期的有效物料清单或工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-139">When the principle is set to <strong>Active or Selected/Active</strong>, the valid BOM or route version for this date is found.</span></span></li>
<li><span data-ttu-id="47f0a-140">当该原则设置为<strong>选定/有效或选定</strong>时，您可以通过单击<strong>物料清单</strong> &gt; <strong>物料清单版本</strong>或<strong>工艺路线</strong> &gt; <strong>工艺路线版本</strong>来选择物料清单版本或工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-140">When the principle is set to <strong>Selected/Active or Selected</strong>, you can select a BOM version or route version by clicking <strong>BOM</strong> &gt; <strong>BOM versions</strong> or <strong>Route</strong> &gt; <strong>Route versions</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f0a-141">版本日期</span><span class="sxs-lookup"><span data-stu-id="47f0a-141">Version date</span></span></td>
<td><span data-ttu-id="47f0a-142">输入用于物料清单和工艺路线的版本日期。</span><span class="sxs-lookup"><span data-stu-id="47f0a-142">Enter the version date for the BOM and route.</span></span> <span data-ttu-id="47f0a-143">该版本用于标识要在特定日期（由物料清单版本设置中的版本日期确定）使用的物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-143">The version identifies which BOM version is used on a specific date, as determined by the version dates in the BOM version setup.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47f0a-144">起始数量</span><span class="sxs-lookup"><span data-stu-id="47f0a-144">From quantity</span></span></td>
<td><span data-ttu-id="47f0a-145">通过选择特定起始数量来筛选版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-145">Filter the versions by selecting a specific from quantity.</span></span> <span data-ttu-id="47f0a-146">如果您设置了一个值，则可以选择不同的物料清单和工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-146">If you set a value, different BOM and route versions might be selected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f0a-147">仅显示有效项</span><span class="sxs-lookup"><span data-stu-id="47f0a-147">Show valid only</span></span></td>
<td><span data-ttu-id="47f0a-148">当您选中此复选框时，树结构将仅显示具有有效日期的物料清单行。</span><span class="sxs-lookup"><span data-stu-id="47f0a-148">When you select the check box, the tree structure shows only BOM lines that have valid dates.</span></span> <span data-ttu-id="47f0a-149">右键单击或双击物料清单行以打开<strong>编辑物料清单行</strong>页，您可以在其中查看该物料清单行的生效日期。</span><span class="sxs-lookup"><span data-stu-id="47f0a-149">Right-click or double-click a BOM line to open the <strong>Edit BOM line</strong> page, where you can see the validity dates for that BOM line.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="47f0a-150">当您使用物料清单设计器审查或编辑包括一个或多个虚拟级别的物料清单时，与顶级物料关联的工艺路线通常涵盖整个物料清单层次结构。</span><span class="sxs-lookup"><span data-stu-id="47f0a-150">When you use the BOM designer to review or edit BOMs that consist of one or more levels of phantoms, the route that is associated with the top item typically spans the complete BOM hierarchy.</span></span> <span data-ttu-id="47f0a-151">要简化概览，您可以通过单击**视图** &gt; **锁定工艺路线** 来锁定显示屏中的顶级工艺路线。</span><span class="sxs-lookup"><span data-stu-id="47f0a-151">To simplify the overview, you can lock the top-level route in the display by clicking **View** &gt; **Lock route**.</span></span> <span data-ttu-id="47f0a-152">要解锁工艺路线，请单击**视图** &gt; **解锁工艺路线**。</span><span class="sxs-lookup"><span data-stu-id="47f0a-152">To unlock the route, click **View** &gt; **Unlock route**.</span></span>

## <a name="adding-and-editing-boms-and-bom-lines"></a><span data-ttu-id="47f0a-153">添加和编辑物料清单和物料清单行</span><span class="sxs-lookup"><span data-stu-id="47f0a-153">Adding and editing BOMs and BOM lines</span></span>
<span data-ttu-id="47f0a-154">使用**物料清单行**或**物料清单**功能修改物料清单行或物料清单。</span><span class="sxs-lookup"><span data-stu-id="47f0a-154">Use the **BOM lines** or **BOM** functions to modify the BOM lines or BOM.</span></span> <span data-ttu-id="47f0a-155">当您选择树中的某个节点时，该节点的类型将决定可用的功能。</span><span class="sxs-lookup"><span data-stu-id="47f0a-155">When you select a node in the tree, the type of the node determines that functions that are available.</span></span>

| <span data-ttu-id="47f0a-156">职能</span><span class="sxs-lookup"><span data-stu-id="47f0a-156">Function</span></span>                            | <span data-ttu-id="47f0a-157">说明</span><span class="sxs-lookup"><span data-stu-id="47f0a-157">Description</span></span>                                                                                               | <span data-ttu-id="47f0a-158">节点类型和条件</span><span class="sxs-lookup"><span data-stu-id="47f0a-158">Node type and conditions</span></span>                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f0a-159">物料清单行 &gt; 编辑</span><span class="sxs-lookup"><span data-stu-id="47f0a-159">BOM lines &gt; Edit</span></span>                 | <span data-ttu-id="47f0a-160">打开可在其中编辑物料清单行属性的对话框。</span><span class="sxs-lookup"><span data-stu-id="47f0a-160">Open a dialog box where you can edit the BOM line attributes.</span></span>                                             | <span data-ttu-id="47f0a-161">当选择了物料清单行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-161">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="47f0a-162">物料清单行 &gt; 删除</span><span class="sxs-lookup"><span data-stu-id="47f0a-162">BOM lines &gt; Delete</span></span>               | <span data-ttu-id="47f0a-163">从所选物料清单中删除物料清单行。</span><span class="sxs-lookup"><span data-stu-id="47f0a-163">Delete a BOM line from the selected BOM.</span></span>                                                                  | <span data-ttu-id="47f0a-164">当选择了物料清单行节点且未锁定物料清单的编辑功能时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-164">This function is available when a BOM line node is selected, and the BOM isn't locked for editing.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="47f0a-165">物料清单行 &gt; 在行前添加</span><span class="sxs-lookup"><span data-stu-id="47f0a-165">BOM lines &gt; Add before line</span></span>      | <span data-ttu-id="47f0a-166">打开一个对话框，您可在其中选择要包含在所选物料清单行前面的产品变型。</span><span class="sxs-lookup"><span data-stu-id="47f0a-166">Open a dialog box where you can select a product variant to include before the selected BOM line.</span></span>         | <span data-ttu-id="47f0a-167">当选择了物料清单行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-167">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="47f0a-168">物料清单行 &gt; 添加到组件物料清单</span><span class="sxs-lookup"><span data-stu-id="47f0a-168">BOM lines &gt; Add to component BOM</span></span> | <span data-ttu-id="47f0a-169">打开一个对话框，您可在其中选择要包含在所选物料清单末尾的产品变型。</span><span class="sxs-lookup"><span data-stu-id="47f0a-169">Open a dialog box where you can select a product variant to include at the end of the selected BOM.</span></span>       | <span data-ttu-id="47f0a-170">当所选节点具有选定的物料清单时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-170">This function is available when the node that is selected has a selected BOM.</span></span> <span data-ttu-id="47f0a-171">如果此功能不可用，物料清单版本可能缺少选定的物料变型。</span><span class="sxs-lookup"><span data-stu-id="47f0a-171">If this function isn't available, a BOM version might be missing for the selected item variant.</span></span> <span data-ttu-id="47f0a-172">在这种情况下，您可以单击**物料清单** &gt; **创建版本**以便为所选节点创建缺少的版本。</span><span class="sxs-lookup"><span data-stu-id="47f0a-172">In this case, you can click **BOM** &gt; **Create version** to create the missing version for the selected node.</span></span> |
| <span data-ttu-id="47f0a-173">物料清单行 &gt; 在行后添加</span><span class="sxs-lookup"><span data-stu-id="47f0a-173">BOM lines &gt; Add after line</span></span>       | <span data-ttu-id="47f0a-174">打开一个对话框，您可在其中选择要包含在所选物料清单行后面的产品变型。</span><span class="sxs-lookup"><span data-stu-id="47f0a-174">Open a dialog box where you can select a product variant to include after the selected BOM line.</span></span>          | <span data-ttu-id="47f0a-175">当选择了物料清单行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-175">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="47f0a-176">物料清单 &gt; 创建版本</span><span class="sxs-lookup"><span data-stu-id="47f0a-176">BOM &gt; Create version</span></span>             | <span data-ttu-id="47f0a-177">为所选节点的产品变型创建新的物料清单版本或物料清单。</span><span class="sxs-lookup"><span data-stu-id="47f0a-177">Create a new BOM version or BOM for the product variant of the selected node.</span></span>                             | <span data-ttu-id="47f0a-178">当选择的物料清单行节点链接到生产类型为**物料清单**或**配方**的物料时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-178">This function is available when the BOM line node that is selected is linked to an item that has a production type of **BOM** or **Formula**.</span></span>                                                                                                                                                  |
| <span data-ttu-id="47f0a-179">物料清单 &gt; 计算</span><span class="sxs-lookup"><span data-stu-id="47f0a-179">BOM &gt; Calculation</span></span>                | <span data-ttu-id="47f0a-180">打开一个对话框，您可以在其中为所选产品变型执行成本或销售价格计算。</span><span class="sxs-lookup"><span data-stu-id="47f0a-180">Open a dialog box where you can run the cost or sales price calculation for the selected product variant.</span></span> | <span data-ttu-id="47f0a-181">当所选节点与物料清单版本相关时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-181">This function is available when the node that is selected is related to a BOM version.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="47f0a-182">物料清单 &gt; 检查</span><span class="sxs-lookup"><span data-stu-id="47f0a-182">BOM &gt; Check</span></span>                      | <span data-ttu-id="47f0a-183">验证并检查所选物料清单。</span><span class="sxs-lookup"><span data-stu-id="47f0a-183">Validate and check the selected BOM.</span></span>                                                                      | <span data-ttu-id="47f0a-184">当所选节点与物料清单版本相关时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="47f0a-184">This function is available when the node that is selected is related to a BOM version.</span></span>                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a><span data-ttu-id="47f0a-185">配置树视图</span><span class="sxs-lookup"><span data-stu-id="47f0a-185">Configuring the tree view</span></span>
<span data-ttu-id="47f0a-186">单击**设置**以自定义在物料清单设计器的树视图中显示的信息。</span><span class="sxs-lookup"><span data-stu-id="47f0a-186">Click **Setup** to customize the information that is shown in the tree view of the BOM designer.</span></span>

| <span data-ttu-id="47f0a-187">字段组</span><span class="sxs-lookup"><span data-stu-id="47f0a-187">Field group</span></span> | <span data-ttu-id="47f0a-188">描述</span><span class="sxs-lookup"><span data-stu-id="47f0a-188">Description</span></span>                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f0a-189">物料清单</span><span class="sxs-lookup"><span data-stu-id="47f0a-189">BOM</span></span>         | <span data-ttu-id="47f0a-190">使用该复选框可选择在树结构中显示的条件。</span><span class="sxs-lookup"><span data-stu-id="47f0a-190">Use the check boxes to select the criteria that are shown in the tree structure.</span></span> <span data-ttu-id="47f0a-191">物料清单设计器将在两个选项卡的底部显示所选条件。</span><span class="sxs-lookup"><span data-stu-id="47f0a-191">The BOM designer displays the selected criteria at the bottom of both tabs.</span></span> |
| <span data-ttu-id="47f0a-192">路线</span><span class="sxs-lookup"><span data-stu-id="47f0a-192">Route</span></span>       | <span data-ttu-id="47f0a-193">使用该复选框可选择对工艺路线显示的条件。</span><span class="sxs-lookup"><span data-stu-id="47f0a-193">Use the check boxes to select the criteria that are shown for the routes.</span></span>                                                                                    |





