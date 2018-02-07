---
title: "配方设计器"
description: "本主题说明如何使用配方设计器来分析和维护树视图中的配方。"
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: d9b61e545067db592545d5fbce7b4315c51a8bf8
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="formula-designer"></a><span data-ttu-id="acdc6-103">配方设计器</span><span class="sxs-lookup"><span data-stu-id="acdc6-103">Formula designer</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="acdc6-104">本主题说明如何使用配方设计器来分析和维护树视图中的配方。</span><span class="sxs-lookup"><span data-stu-id="acdc6-104">This topic explains how to use the formula designer to analyze and maintain formulas in a tree view.</span></span>

<span data-ttu-id="acdc6-105">从**已发布的产品**打开**配方设计器**后，左窗格中的树显示已发布的产品的联产品的列表和成分的层次结构。</span><span class="sxs-lookup"><span data-stu-id="acdc6-105">When you open the **Formula designer** page from the **Released products** page, the tree in the left pane shows the list of co-products and the hierarchy of ingredients for the released product.</span></span> <span data-ttu-id="acdc6-106">结构衍生自有效且对所选物料及其成分、物料的默认订单站点和实际日期进行审核的配方的层次结构。</span><span class="sxs-lookup"><span data-stu-id="acdc6-106">The structure is derived from the hierarchy of formulas that are active and approved for the selected item and its ingredients, the default order site of the item, and the actual date.</span></span>

<span data-ttu-id="acdc6-107">单击**设置**可选择不同的配置并指定要在树的行上显示哪些信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-107">Click **Setup** to select different configurations and specify what information appears on the lines of the tree.</span></span>

<span data-ttu-id="acdc6-108">单击**“筛选器”**以更改视图中的初始选择。</span><span class="sxs-lookup"><span data-stu-id="acdc6-108">Click **Filter** to change the initial selection in the view.</span></span> <span data-ttu-id="acdc6-109">如果将显示原则设置为**选定/有效**或**选定**，可以选择要在视图中使用的单个配方或工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-109">If you set the display principle to **Selected/Active** or **Selected**, you can select individual formula or route versions to use in the view.</span></span> <span data-ttu-id="acdc6-110">您可以选择要在配方设计器中显示或维护的未经审核和无效的配方版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-110">You can select non-approved and non-active formula versions to show or maintain in the formula designer.</span></span>  

> [!NOTE]
> <span data-ttu-id="acdc6-111">如果您从**物料清单**列表页打开了**配方设计器**页，该设计器不会显示工艺路线信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-111">If you open the **Formula designer** page from the **Bills of materials** list page, it doesn't show route information.</span></span> <span data-ttu-id="acdc6-112">目前，配方的选择或工艺路线版本应用于配方设计器的所有实例。</span><span class="sxs-lookup"><span data-stu-id="acdc6-112">Currently, the selection of a formula or route version applies to all instances of the formula designer.</span></span>  

<span data-ttu-id="acdc6-113">以下各节将介绍物料清单设计器中可用的功能。</span><span class="sxs-lookup"><span data-stu-id="acdc6-113">The following sections describe the functionality that is available in the BOM designer.</span></span>

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a><span data-ttu-id="acdc6-114">使用配方设计器分析配方结构</span><span class="sxs-lookup"><span data-stu-id="acdc6-114">Analyze a formula structure by using the formula designer</span></span>
<span data-ttu-id="acdc6-115">配方设计器有两个部分：</span><span class="sxs-lookup"><span data-stu-id="acdc6-115">The formula designer has two sections:</span></span>

-   <span data-ttu-id="acdc6-116">配方结构的树视图。</span><span class="sxs-lookup"><span data-stu-id="acdc6-116">The tree view of the formula structure.</span></span>
-   <span data-ttu-id="acdc6-117">详细信息部分中，显示所选数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-117">The details section, which shows details of the selected data.</span></span> <span data-ttu-id="acdc6-118">当您选择树视图中的节点时，详细信息部分中的 FastTabs 将基于该节点进行更新：</span><span class="sxs-lookup"><span data-stu-id="acdc6-118">When you select a node in the tree view, the FastTabs in the details section are updated based on that node:</span></span>
    -   <span data-ttu-id="acdc6-119">**配方行详细信息** - 查看在树视图中选择的配方行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-119">**Formula line details** – View the details of the formula line that is selected in the tree view.</span></span>
    -   <span data-ttu-id="acdc6-120">**物料数据** - 查看主要物料或在所选节点中使用的物料的详细信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-120">**Item data** – View the details of the main item or the item that is used in the selected node.</span></span> <span data-ttu-id="acdc6-121">您可以单击**“编辑已发布产品”**以维护所选物料。</span><span class="sxs-lookup"><span data-stu-id="acdc6-121">You can click **Edit released product** to maintain the selected item.</span></span>
    -   <span data-ttu-id="acdc6-122">**工艺路线** - 查看与所选节点相关的配方的标题。</span><span class="sxs-lookup"><span data-stu-id="acdc6-122">**Formula** – View the header of the formula that is related to the selected node.</span></span>
    -   <span data-ttu-id="acdc6-123">**工艺路线** - 查看与所选节点相关的工艺路线的标题。</span><span class="sxs-lookup"><span data-stu-id="acdc6-123">**Route** – View the header of the route that is related to the selected node.</span></span>
    -   <span data-ttu-id="acdc6-124">**工艺路线工序** - 查看工艺路线的工序的预览。</span><span class="sxs-lookup"><span data-stu-id="acdc6-124">**Route operations** – View a preview of the operations for the route.</span></span> <span data-ttu-id="acdc6-125">当物料清单行 (BOM) 分配给所选的特定工序后，该工序将标记为**工序中需要的组件**。</span><span class="sxs-lookup"><span data-stu-id="acdc6-125">When a bill of materials (BOM) line that is assigned to a specific operation is selected, the operation is marked as **Component needed at operations**.</span></span>

## <a name="select-a-formula-and-route"></a><span data-ttu-id="acdc6-126">选择配方和工艺路线</span><span class="sxs-lookup"><span data-stu-id="acdc6-126">Select a formula and route</span></span>
<span data-ttu-id="acdc6-127">为配方和工艺路线应用的筛选器将显示在配方设计器的标题中。</span><span class="sxs-lookup"><span data-stu-id="acdc6-127">The filter that is applied for the formula and route is shown in the header of the formula designer.</span></span> <span data-ttu-id="acdc6-128">您可以使用**“筛选器”**对话框更改筛选器。</span><span class="sxs-lookup"><span data-stu-id="acdc6-128">You can change the filter by using the **Filter** dialog box.</span></span> <span data-ttu-id="acdc6-129">下表描述了此对话框中的字段。</span><span class="sxs-lookup"><span data-stu-id="acdc6-129">The following table describes the fields in this dialog box.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="acdc6-130">字段</span><span class="sxs-lookup"><span data-stu-id="acdc6-130">Field</span></span></th>
<th><span data-ttu-id="acdc6-131">描述</span><span class="sxs-lookup"><span data-stu-id="acdc6-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="acdc6-132">产品维度</span><span class="sxs-lookup"><span data-stu-id="acdc6-132">Product dimensions</span></span></td>
<td><span data-ttu-id="acdc6-133">如果选中的成品是基础产品，您可以定义主要选择的可用产品维度。</span><span class="sxs-lookup"><span data-stu-id="acdc6-133">If the selected finished product is a product master, you can define the active product dimensions for the main selection.</span></span> <span data-ttu-id="acdc6-134">请注意，如果您为其打开配方设计器的产品不是基础产品，则在<strong>筛选器</strong>对话框中无法选择产品维度。</span><span class="sxs-lookup"><span data-stu-id="acdc6-134">Note that if you open the formula designer for a product that isn't a product master, no product dimensions can be selected in the <strong>Filter</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acdc6-135">站点</span><span class="sxs-lookup"><span data-stu-id="acdc6-135">Site</span></span></td>
<td><span data-ttu-id="acdc6-136">更改为其显示成分树的站点。</span><span class="sxs-lookup"><span data-stu-id="acdc6-136">Change the site that the ingredient tree is shown for.</span></span> <span data-ttu-id="acdc6-137">默认站点是成品的默认库存值。</span><span class="sxs-lookup"><span data-stu-id="acdc6-137">The default site is the default inventory site of the finished item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acdc6-138">显示原则</span><span class="sxs-lookup"><span data-stu-id="acdc6-138">Display principle</span></span></td>
<td><p><span data-ttu-id="acdc6-139">选择适用于当前配方结构和当前工艺路线的版本显示原则：</span><span class="sxs-lookup"><span data-stu-id="acdc6-139">Select the version display principle that applies to the current formula structure and the current route:</span></span></p>
<ul>
<li><span data-ttu-id="acdc6-140">当原则设置为“有效”<strong></strong>或“选定/有效”<strong></strong>时，则会查找此日期的有效配方或工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-140">When the principle is set to <strong>Active</strong> or <strong>Selected/Active</strong>, the valid formula or route version for this date is found.</span></span></li>
<li><span data-ttu-id="acdc6-141">当该原则设置为<strong>选定/有效</strong>或<strong>选定</strong>时，您可以通过单击<strong>配方</strong> &gt; <strong>配方版本</strong> 或 <strong>工艺路线</strong> &gt; <strong>工艺路线版本</strong>来选择配方版本或工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-141">When the principle is set to <strong>Selected/Active</strong> or <strong>Selected</strong>, you can select a formula version or route version by clicking <strong>Formula</strong> &gt; <strong>Formula versions</strong> or <strong>Route</strong> &gt; <strong>Route versions</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acdc6-142">版本日期</span><span class="sxs-lookup"><span data-stu-id="acdc6-142">Version date</span></span></td>
<td><span data-ttu-id="acdc6-143">输入用于配方和工艺路线的版本日期。</span><span class="sxs-lookup"><span data-stu-id="acdc6-143">Enter the version date for the formula and route.</span></span> <span data-ttu-id="acdc6-144">该版本标识要在具体日期（由配方版本设置中的版本日期确定）上使用哪一配方版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-144">The version identifies which formula version is used on a specific date, based on the version dates in the formula version setup.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acdc6-145">起始数量</span><span class="sxs-lookup"><span data-stu-id="acdc6-145">From quantity</span></span></td>
<td><span data-ttu-id="acdc6-146">通过选择特定“起始”数量来筛选版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-146">Filter the versions by selecting a specific "from" quantity.</span></span> <span data-ttu-id="acdc6-147">如果您设置了一个值，则可以选择不同的配方和工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-147">If you set a value, different formula and route versions might be selected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acdc6-148">仅显示有效项</span><span class="sxs-lookup"><span data-stu-id="acdc6-148">Show valid only</span></span></td>
<td><span data-ttu-id="acdc6-149">当您选中此复选框时，树结构将仅显示具有有效日期的配方行。</span><span class="sxs-lookup"><span data-stu-id="acdc6-149">When you select the check box, the tree structure shows only formula lines that have valid dates.</span></span> <span data-ttu-id="acdc6-150">右键单击或双击配方行以打开<strong>编辑配方行</strong>页，您可以在其中查看该配方行的生效日期。</span><span class="sxs-lookup"><span data-stu-id="acdc6-150">Right-click or double-click a formula line to open the <strong>Edit formula line</strong> page, where you can see the validity dates for that formula line.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="acdc6-151">当您使用配方设计器审查或编辑包括一个或多个虚拟级别的配方时，与顶级物料关联的工艺路线通常涵盖整个配方层次结构。</span><span class="sxs-lookup"><span data-stu-id="acdc6-151">When you use the formula designer to review or edit formulas that consist of one or more levels of phantoms, the route that is associated with the top item typically spans the complete formula hierarchy.</span></span> <span data-ttu-id="acdc6-152">要简化概览，您可以通过单击**视图** &gt; **锁定工艺路线** 来锁定显示屏中的顶级工艺路线。</span><span class="sxs-lookup"><span data-stu-id="acdc6-152">To simplify the overview, you can lock the top-level route in the display by clicking **View** &gt; **Lock route**.</span></span> <span data-ttu-id="acdc6-153">要解锁工艺路线，请单击**视图** &gt; **解锁工艺路线**。</span><span class="sxs-lookup"><span data-stu-id="acdc6-153">To unlock the route, click **View** &gt; **Unlock route**.</span></span>

## <a name="add-and-edit-formulas-and-formula-lines"></a><span data-ttu-id="acdc6-154">添加和编辑配方和配方行</span><span class="sxs-lookup"><span data-stu-id="acdc6-154">Add and edit formulas and formula lines</span></span>
<span data-ttu-id="acdc6-155">使用**物料清单行**或**配方**功能修改配方行或配方。</span><span class="sxs-lookup"><span data-stu-id="acdc6-155">Use the **BOM lines** or **Formula** functions to modify the formula lines or formula.</span></span> <span data-ttu-id="acdc6-156">当您选择树中的某个节点时，该节点的类型将决定可用的功能。</span><span class="sxs-lookup"><span data-stu-id="acdc6-156">When you select a node in the tree, the type of the node determines the functions that are available.</span></span>

| <span data-ttu-id="acdc6-157">职能</span><span class="sxs-lookup"><span data-stu-id="acdc6-157">Function</span></span>                            | <span data-ttu-id="acdc6-158">说明</span><span class="sxs-lookup"><span data-stu-id="acdc6-158">Description</span></span>                                                                                               | <span data-ttu-id="acdc6-159">节点类型和条件</span><span class="sxs-lookup"><span data-stu-id="acdc6-159">Node type and conditions</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| <span data-ttu-id="acdc6-160">物料清单行 &gt; 编辑</span><span class="sxs-lookup"><span data-stu-id="acdc6-160">BOM lines &gt; Edit</span></span>                 | <span data-ttu-id="acdc6-161">打开可在其中编辑配方行属性的对话框。</span><span class="sxs-lookup"><span data-stu-id="acdc6-161">Open a dialog box where you can edit the formula line attributes.</span></span>                                         | <span data-ttu-id="acdc6-162">当选择了配方行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-162">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="acdc6-163">物料清单行 &gt; 删除</span><span class="sxs-lookup"><span data-stu-id="acdc6-163">BOM lines &gt; Delete</span></span>               | <span data-ttu-id="acdc6-164">删除所选配方的配方行。</span><span class="sxs-lookup"><span data-stu-id="acdc6-164">Delete a formula line from the selected formula.</span></span>                                                          | <span data-ttu-id="acdc6-165">当选择了配方行节点且未锁定配方的编辑功能时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-165">This function is available when a formula line node is selected, and the formula isn't locked for editing.</span></span> |
| <span data-ttu-id="acdc6-166">物料清单行 &gt; 在行前添加</span><span class="sxs-lookup"><span data-stu-id="acdc6-166">BOM lines &gt; Add before line</span></span>      | <span data-ttu-id="acdc6-167">打开一个对话框，您可在其中选择要包含在所选配方行前面的产品变型。</span><span class="sxs-lookup"><span data-stu-id="acdc6-167">Open a dialog box where you can select a product variant to include before the selected formula line.</span></span>     | <span data-ttu-id="acdc6-168">当选择了配方行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-168">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="acdc6-169">物料清单行 &gt; 添加到组件物料清单</span><span class="sxs-lookup"><span data-stu-id="acdc6-169">BOM lines &gt; Add to component BOM</span></span> | <span data-ttu-id="acdc6-170">打开一个对话框，您可在其中选择要包含在所选配方末尾的产品变型。</span><span class="sxs-lookup"><span data-stu-id="acdc6-170">Open a dialog box where you can select a product variant to include at the end of the selected formula.</span></span>   | <span data-ttu-id="acdc6-171">当所选节点具有选定的配方时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-171">This function is available when the node that is selected has a selected formula.</span></span> <span data-ttu-id="acdc6-172">如果此功能不可用，配方版本可能缺少选定的物料变型。</span><span class="sxs-lookup"><span data-stu-id="acdc6-172">If this function isn't available, a formula version might be missing for the selected item variant.</span></span> <span data-ttu-id="acdc6-173">在这种情况下，您可以单击**配方** &gt; **创建版本**以便为所选节点创建缺少的版本。</span><span class="sxs-lookup"><span data-stu-id="acdc6-173">In this case, you can click **Formula** &gt; **Create version** to create the missing version for the selected node.</span></span> |
| <span data-ttu-id="acdc6-174">物料清单行 &gt; 在行后添加</span><span class="sxs-lookup"><span data-stu-id="acdc6-174">BOM lines &gt; Add after line</span></span>       | <span data-ttu-id="acdc6-175">打开一个对话框，您可在其中选择要包含在所选配方行后面的产品变型。</span><span class="sxs-lookup"><span data-stu-id="acdc6-175">Open a dialog box where you can select a product variant to include after the selected formula line.</span></span>      | <span data-ttu-id="acdc6-176">当选择了配方行节点时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-176">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="acdc6-177">配方 &gt; 创建版本</span><span class="sxs-lookup"><span data-stu-id="acdc6-177">Formula &gt; Create version</span></span>         | <span data-ttu-id="acdc6-178">为所选节点的产品变型创建新的配方版本或配方。</span><span class="sxs-lookup"><span data-stu-id="acdc6-178">Create a new formula version or formula for the product variant of the selected node.</span></span>                     | <span data-ttu-id="acdc6-179">当选择的配方行节点链接到生产类型为**物料清单**或**配方**的物料时，此功能可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-179">This function is available when the formula line node that is selected is linked to an item that has a production type of **BOM** or **Formula**.</span></span> |
| <span data-ttu-id="acdc6-180">配方 &gt; 计算</span><span class="sxs-lookup"><span data-stu-id="acdc6-180">Formula &gt; Calculation</span></span>            | <span data-ttu-id="acdc6-181">打开一个对话框，您可以在其中为所选产品变型执行成本或销售价格计算。</span><span class="sxs-lookup"><span data-stu-id="acdc6-181">Open a dialog box where you can run the cost or sales price calculation for the selected product variant.</span></span> | <span data-ttu-id="acdc6-182">当所选节点与配方版本相关时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-182">This function is available when the node that is selected is related to a formula version.</span></span> |
| <span data-ttu-id="acdc6-183">配方 &gt; 检查</span><span class="sxs-lookup"><span data-stu-id="acdc6-183">Formula &gt; Check</span></span>                  | <span data-ttu-id="acdc6-184">验证并检查所选配方。</span><span class="sxs-lookup"><span data-stu-id="acdc6-184">Validate and check the selected formula.</span></span>                                                                  | <span data-ttu-id="acdc6-185">当所选节点与配方版本相关时，此字段可用。</span><span class="sxs-lookup"><span data-stu-id="acdc6-185">This function is available when the node that is selected is related to a formula version.</span></span> |

## <a name="configuring-the-tree-view"></a><span data-ttu-id="acdc6-186">配置树视图</span><span class="sxs-lookup"><span data-stu-id="acdc6-186">Configuring the tree view</span></span>
<span data-ttu-id="acdc6-187">单击**设置**以自定义在配方设计器的树视图中显示的信息。</span><span class="sxs-lookup"><span data-stu-id="acdc6-187">Click **Setup** to customize the information that is shown in the tree view of the formula designer.</span></span>

| <span data-ttu-id="acdc6-188">字段组</span><span class="sxs-lookup"><span data-stu-id="acdc6-188">Field group</span></span> | <span data-ttu-id="acdc6-189">说明</span><span class="sxs-lookup"><span data-stu-id="acdc6-189">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="acdc6-190">物料清单</span><span class="sxs-lookup"><span data-stu-id="acdc6-190">BOM</span></span>         | <span data-ttu-id="acdc6-191">使用该复选框可选择在树结构中显示的条件。</span><span class="sxs-lookup"><span data-stu-id="acdc6-191">Use the check boxes to select the criteria that are shown in the tree structure.</span></span> <span data-ttu-id="acdc6-192">配方设计器将在两个选项卡的底部显示所选条件。</span><span class="sxs-lookup"><span data-stu-id="acdc6-192">The formula designer shows the selected criteria at the bottom of both tabs.</span></span> |
| <span data-ttu-id="acdc6-193">工艺路线</span><span class="sxs-lookup"><span data-stu-id="acdc6-193">Route</span></span>       | <span data-ttu-id="acdc6-194">使用该复选框可选择对工艺路线显示的条件。</span><span class="sxs-lookup"><span data-stu-id="acdc6-194">Use the check boxes to select the criteria that are shown for the routes.</span></span> |

