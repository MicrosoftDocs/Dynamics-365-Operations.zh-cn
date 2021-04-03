---
title: 检查配置的 ER 组件以防止运行时问题
description: 本主题说明如何检查配置的电子申报 (ER) 组件，以防止可能发生的运行时问题。
author: NickSelin
manager: AnnBe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86db6dc27a8a76e90494e3dc7a7cc9c828f9ec37
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574117"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="a3cfb-103">检查配置的 ER 组件以防止运行时问题</span><span class="sxs-lookup"><span data-stu-id="a3cfb-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3cfb-104">配置的每个[电子申报 (ER)](general-electronic-reporting.md) [格式](general-electronic-reporting.md#FormatComponentOutbound)和[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components)组件都可以在设计时[验证](er-fillable-excel.md#validate-an-er-format)。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="a3cfb-105">在此验证期间，将运行一致性检查以帮助防止可能发生的运行时问题，例如执行错误和性能降级。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="a3cfb-106">对于发现的每个问题，检查都会提供问题元素的路径。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-106">For every issue that is found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="a3cfb-107">对于某些问题，可以使用自动修复。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="a3cfb-108">默认情况下，在以下情况下，将自动对包含先前提到的 ER 组件的 ER 配置应用验证：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="a3cfb-109">[导入](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER 配置的一个新[版本](general-electronic-reporting.md#component-versioning)到您的 Microsoft Dynamics 365 Finance 实例中。.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="a3cfb-110">将可编辑 ER 配置的 [状态](general-electronic-reporting.md#component-versioning)从 **草稿** 更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="a3cfb-111">通过应用新的基础版本[重定](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)可编辑 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="a3cfb-112">您可以显式运行此验证。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-112">You can explicitly run this validation.</span></span> <span data-ttu-id="a3cfb-113">选择以下三个选项之一，然后按照提供的步骤操作：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="a3cfb-114">选项 1：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-114">Option 1:</span></span>

    1. <span data-ttu-id="a3cfb-115">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a3cfb-116">在左窗格的配置树中，选择包含 ER 格式或 ER 模型映射组件的所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="a3cfb-117">在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a3cfb-118">在操作窗格上，选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a3cfb-119">选项 2，对于 ER 格式：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="a3cfb-120">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a3cfb-121">在左窗格的配置树中，选择包含 ER 格式组件的所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="a3cfb-122">在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a3cfb-123">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a3cfb-124">在 **格式设计器** 页的操作窗格上，选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a3cfb-125">选项 3，对于 ER 模型映射：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="a3cfb-126">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a3cfb-127">在左窗格的配置树中，选择包含 ER 模型映射组件的所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="a3cfb-128">在 **版本** 快速选项卡上，选择所选 ER 配置所需的版本。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a3cfb-129">在操作窗格上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a3cfb-130">在 **模型到数据源映射** 页面的操作窗格中，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="a3cfb-131">在 **模型映射设计器** 页面的操作窗格中，选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="a3cfb-132">若要在导入配置时跳过验证，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="a3cfb-133">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a3cfb-134">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a3cfb-135">将 **导入后验证配置** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="a3cfb-136">要在更改或重定版本状态时跳过验证，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="a3cfb-137">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a3cfb-138">在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a3cfb-139">将 **配置状态更改时跳过验证并重定基本值** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="a3cfb-140">ER 使用以下类别为一致性检查检验分组：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="a3cfb-141">**可执行性** – 用于检测运行时可能发生的严重问题的检查。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-141">**Executability** – Inspections that detect critical issues that might occur at runtime.</span></span> <span data-ttu-id="a3cfb-142">这些问题大多数为 **错误** 级。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="a3cfb-143">**性能** – 用于检测可能导致执行配置的 ER 组件不完整的检查。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="a3cfb-144">这些问题大多数为 **警告** 级。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="a3cfb-145">**数据完整性** – 用于检测可能导致数据丢失或运行时问题的问题的检查。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="a3cfb-146">这些问题大多数为 **警告** 级。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="a3cfb-147">检查列表</span><span class="sxs-lookup"><span data-stu-id="a3cfb-147">List of inspections</span></span>

<span data-ttu-id="a3cfb-148">下表提供 ER 提供的检查的概览。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="a3cfb-149">有关这些检查的详细信息，请使用第一列中的链接转到本主题的相关部分。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="a3cfb-150">这些部分介绍了 ER 提供的组件针对的组件类型，以及如何重新配置 ER 组件以帮助防止问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a3cfb-151">姓名</span><span class="sxs-lookup"><span data-stu-id="a3cfb-151">Name</span></span></th>
<th><span data-ttu-id="a3cfb-152">类别</span><span class="sxs-lookup"><span data-stu-id="a3cfb-152">Category</span></span></th>
<th><span data-ttu-id="a3cfb-153">等级</span><span class="sxs-lookup"><span data-stu-id="a3cfb-153">Level</span></span></th>
<th><span data-ttu-id="a3cfb-154">消息</span><span class="sxs-lookup"><span data-stu-id="a3cfb-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a3cfb-155"><a href='#i1'>类型转换</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="a3cfb-156">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-156">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-157">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-157">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-158">不能将类型为 &lt;type&gt; 的表达式转换为类型为 &lt;type&gt; 的字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a3cfb-159"><b>运行时错误：</b>类型异常</span><span class="sxs-lookup"><span data-stu-id="a3cfb-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-160"><a href='#i2'>类型兼容性</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="a3cfb-161">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-161">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-162">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-162">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-163">配置的表达式不能用作当前格式元素到数据源的绑定，因为此表达式返回的数据类型 &lt;type&gt; 的值超出了类型为 &lt;type&gt; 的当前格式元素支持的数据类型范围。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a3cfb-164"><b>运行时错误：</b>类型异常</span><span class="sxs-lookup"><span data-stu-id="a3cfb-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-165"><a href='#i3'>缺少配置元素</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="a3cfb-166">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-166">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-167">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-167">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-168">未找到路径 &lt;path&gt;。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="a3cfb-169"><b>运行时错误：</b>未找到配置元素 &lt;path&gt;</span><span class="sxs-lookup"><span data-stu-id="a3cfb-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-170"><a href='#i4'>带 FILTER 函数的表达式的可执行性</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="a3cfb-171">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-171">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-172">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-172">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-173">FILTER 函数的列表表达式无法查询。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="a3cfb-174"><b>运行时错误：</b>不支持筛选。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a3cfb-175">验证配置以获得有关此问题的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="a3cfb-176"><a href='#i5'>GROUPBY 数据源的可执行性</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="a3cfb-177">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-177">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-178">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-178">Error</span></span></td>
<td><span data-ttu-id="a3cfb-179">路径 &lt;path&gt; 不支持查询。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-180">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-180">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-181">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-181">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-182">不能使用查询执行按函数分组。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="a3cfb-183"><b>运行时错误</b>：不能使用查询执行按函数分组。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-184"><a href='#i6'>JOIN 数据源的可执行性</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="a3cfb-185">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-185">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-186">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-186">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-187">不能在查询中联接不是筛选器的列表 &lt;path&gt;。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="a3cfb-188"><b>运行时错误：</b>函数联接的数据源应该是错误调用的筛选表达式计算字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-189"><a href='#i7'>FILTER 与 WHERE 函数的偏好对比</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="a3cfb-190">绩效</span><span class="sxs-lookup"><span data-stu-id="a3cfb-190">Performance</span></span></td>
<td><span data-ttu-id="a3cfb-191">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-191">Warning</span></span></td>
<td><span data-ttu-id="a3cfb-192">从性能的角度来看，相比 WHERE，更倾向于对表达式使用 FILTER 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="a3cfb-193">选择“修复”以自动替换它。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-194"><a href='#i8'>ALLITEMSQUERY 相比 ALLITEMS 函数的偏好对比</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="a3cfb-195">绩效</span><span class="sxs-lookup"><span data-stu-id="a3cfb-195">Performance</span></span></td>
<td><span data-ttu-id="a3cfb-196">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-196">Warning</span></span></td>
<td><span data-ttu-id="a3cfb-197">从性能的角度来看，相比 ALLITEMS，更倾向于对表达式使用 ALLITEMSQUERY 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="a3cfb-198">选择“修复”以自动替换它。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-199"><a href='#i9'>空列表用例的注意事项</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="a3cfb-200">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-200">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-201">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-202">列表 &lt;path&gt; 不检查空列表用例，因此会在运行时生成错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="a3cfb-203">请为空列表用例添加检查。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="a3cfb-204"><b>运行时错误：</b>&lt;path&gt; 处列表为空</span><span class="sxs-lookup"><span data-stu-id="a3cfb-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="a3cfb-205"><b><a href='#i9a'>潜在问题</a>：</b>行填充一次，而填充来源数据源中则包含多个记录</span><span class="sxs-lookup"><span data-stu-id="a3cfb-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-206"><a href='#i10'>带 FILTER 函数的表达式的可执行性（高速缓存）</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="a3cfb-207">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-207">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-208">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-208">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-209">FILTER 函数不能应用于所选类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="a3cfb-210">仅当未高速缓存且无手动添加的嵌套数据源时，Table 记录类型的数据源才适用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="a3cfb-211"><b>运行时错误：</b>不支持筛选。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a3cfb-212">验证配置以获得有关此问题的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-213"><a href='#i11'>缺少绑定</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="a3cfb-214">可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-214">Executability</span></span></td>
<td><span data-ttu-id="a3cfb-215">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-216">路径 &lt;path&gt;在使用模型的映射时没有到任何数据源的绑定。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="a3cfb-217"><b>运行时错误：</b>未绑定路径 &lt;path&gt;</span><span class="sxs-lookup"><span data-stu-id="a3cfb-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-218"><a href='#i12'>未链接模板</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="a3cfb-219">数据完整性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-219">Data integrity</span></span></td>
<td><span data-ttu-id="a3cfb-220">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-220">Warning</span></span></td>
<td><span data-ttu-id="a3cfb-221">文件 &lt;name&gt; 未链接到任何文件组件，因此将在更改了配置版本状态后被移除。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-222"><a href='#i13'>不同步格式</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a3cfb-223">数据完整性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-223">Data integrity</span></span></td>
<td><span data-ttu-id="a3cfb-224">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-224">Warning</span></span></td>
<td><span data-ttu-id="a3cfb-225">Excel 工作表 &lt;sheet name&gt; 中无定义的名称 &lt;component name&gt;</span><span class="sxs-lookup"><span data-stu-id="a3cfb-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-226"><a href='#i14'>不同步格式</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-226"><a href='#i14'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a3cfb-227">数据完整性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-227">Data integrity</span></span></td>
<td><span data-ttu-id="a3cfb-228">警告</span><span class="sxs-lookup"><span data-stu-id="a3cfb-228">Warning</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-229">Word 模板文件中不存在 &lt;标记的 Word 内容控件&gt; 标记</span><span class="sxs-lookup"><span data-stu-id="a3cfb-229">&lt;Tagged Word content control&gt; tag does not exist in Word template file</span></span></p>
<p><span data-ttu-id="a3cfb-230"><b>运行时错误：</b>Word 模板文件中不存在 &lt;标记的 Word 内容控件&gt; 标记。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-230"><b>Runtime error:</b> &lt;Tagged Word content control&gt; tag does not exist in Word template file.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-231"><a href='#i15'>没有默认映射</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-231"><a href='#i15'>No default mapping</a></span></span></td>
<td><span data-ttu-id="a3cfb-232">数据完整性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-232">Data integrity</span></span></td>
<td><span data-ttu-id="a3cfb-233">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-233">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-234">&lt;逗号分隔的配置名称&gt; 配置中的 &lt;模型名称（根描述符）&gt; 数据模型存在多个模型映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-234">More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a3cfb-235">将其中一个配置设置为默认配置</span><span class="sxs-lookup"><span data-stu-id="a3cfb-235">Set one of the configurations as default</span></span></p>
<p><span data-ttu-id="a3cfb-236"><b>运行时错误：</b>&lt;逗号分隔的配置名称&gt; 配置中的 &lt;模型名称（根描述符）&gt; 数据模型存在多个模型映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-236"><b>Runtime error:</b> More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a3cfb-237">将其中一个配置设置为默认配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-237">Set one of the configurations as default.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a3cfb-238"><a href='#i16'>页眉或页脚组件的设置不一致</a></span><span class="sxs-lookup"><span data-stu-id="a3cfb-238"><a href='#i16'>Inconsistent setting of Header or Footer components</a></span></span></td>
<td><span data-ttu-id="a3cfb-239">数据完整性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-239">Data integrity</span></span></td>
<td><span data-ttu-id="a3cfb-240">错误​</span><span class="sxs-lookup"><span data-stu-id="a3cfb-240">Error</span></span></td>
<td>
<p><span data-ttu-id="a3cfb-241">页眉/页脚（&lt;组件类型：页眉或页脚&gt;）不一致</span><span class="sxs-lookup"><span data-stu-id="a3cfb-241">Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent</span></span></p>
<p><span data-ttu-id="a3cfb-242"><b>运行时：</b>如果执行了已配置的 ER 格式的草稿版本，则会在运行时使用最后配置的组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-242"><b>Runtime:</b> The last configured component is used at runtime if the draft version of the configured ER format is executed.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="a3cfb-243">类型转换</span><span class="sxs-lookup"><span data-stu-id="a3cfb-243">Type conversion</span></span>

<span data-ttu-id="a3cfb-244">ER 检查数据模型字段的数据类型是否与配置为该字段的绑定的表达式的数据类型兼容。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-244">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="a3cfb-245">如果数据类型不兼容，将在 ER 模型映射设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-245">If the data types are incompatible, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-246">您收到的消息指出 ER 无法将 A 类型的表达式转换为 B 类型的字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-246">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="a3cfb-247">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-247">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-248">开始同时配置 ER 数据模型和 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-248">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a3cfb-249">在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-249">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![X 字段和整数数据类型已添加到“数据模型”页面上的数据模型树中](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a3cfb-251">在模型映射设计器内的 **数据源** 窗格中，添加一个 **计算字段** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-251">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a3cfb-252">将新数据源命名为 **Y**，然后对其进行配置，以使其包含表达式 `INTVALUE(100)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-252">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a3cfb-253">将 **X** 绑定到 **Y**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-253">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a3cfb-254">在数据模型设计器中，将 **X** 字段的数据类型从 **整数** 更改为 **Int64**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-254">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a3cfb-255">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-255">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![验证模型映射设计器页上的可编辑模型映射组件](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="a3cfb-257">选择 **验证** 检查 **配置** 页上所选 ER 配置的模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-257">Select **Validate** to inspect the model mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![检查“配置”页面上的模型映射组件](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="a3cfb-259">请注意，发生了验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-259">Notice that a validation error occurs.</span></span> <span data-ttu-id="a3cfb-260">消息说明 **Y** 数据源的 `INTVALUE(100)` 表达式返回的 **整数** 类型的值不能存储在 **Int64** 类型的 **X** 数据模型字段中。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-260">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="a3cfb-261">下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-261">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![“格式设计器”页上的运行时错误](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-263">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-263">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-264">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-264">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-265">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-265">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-266">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-266">Option 1</span></span>

<span data-ttu-id="a3cfb-267">通过更改数据模型字段的数据类型更新数据模型结构，使其与为该字段的绑定配置的表达式的数据类型相匹配。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-267">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="a3cfb-268">对于前面的示例，**X** 字段的数据类型必须更改回 **整数**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-268">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-269">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-269">Option 2</span></span>

<span data-ttu-id="a3cfb-270">通过更改与数据模型字段绑定的数据源的表达式更新模型映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-270">Update the model mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="a3cfb-271">对于前面的示例，**Y** 数据源的表达式必须更改为 `INT64VALUE(100)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-271">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="a3cfb-272">类型兼容性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-272">Type compatibility</span></span>

<span data-ttu-id="a3cfb-273">ER 检查格式元素的数据类型是否与配置为该格式元素的绑定的表达式的数据类型兼容。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-273">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="a3cfb-274">如果数据类型不兼容，将在 ER Operations 设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-274">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="a3cfb-275">收到的消息表示配置的表达式不能用作当前格式元素到数据源的绑定，因为此表达式返回的数据类型 A 的值超出了类型为 B 的当前格式元素支持的数据类型范围。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-275">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="a3cfb-276">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-276">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-277">开始同时配置 ER 数据模型和 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-277">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a3cfb-278">在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-278">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="a3cfb-279">在格式结构树中，添加 **数值** 类型的格式元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-279">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="a3cfb-280">将新格式元素命名为 **Y**。在 **数值类型** 字段中，为数据类型选择 **整数**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-280">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="a3cfb-281">将 **X** 绑定到 **Y**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-281">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a3cfb-282">在格式结构树中，将 **Y** 格式元素的数据类型从 **整数** 更改为 **Int64**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-282">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a3cfb-283">选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-283">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![在“格式设计器”页面上验证类型兼容性](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="a3cfb-285">请注意，发生了验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-285">Notice that a validation error occurs.</span></span> <span data-ttu-id="a3cfb-286">该消息指出配置的表达式只能接受 **Int64** 值。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-286">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="a3cfb-287">因此，不能在 **Y** 格式元素中输入类型为 **整数** 的 **X** 数据模型字段值。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-287">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-288">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-288">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-289">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-289">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-290">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-290">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-291">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-291">Option 1</span></span>

<span data-ttu-id="a3cfb-292">通过更改 **数值** 格式元素的数据类型更新数据模型结构，使其与为该元素的绑定配置的表达式的数据类型相匹配。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-292">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="a3cfb-293">在前面的示例中， **X** 格式元素的 **数值类型** 值必须更改回 **整数**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-293">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-294">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-294">Option 2</span></span>

<span data-ttu-id="a3cfb-295">通过将表达式从 `model.X` 更改为 `INT64VALUE(model.X)`，更新 **X** 格式元素的格式映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-295">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="a3cfb-296">缺少配置元素</span><span class="sxs-lookup"><span data-stu-id="a3cfb-296">Missing configuration element</span></span>

<span data-ttu-id="a3cfb-297">ER 检查绑定表达式中是否仅包含在可编辑 ER 组件中配置的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-297">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="a3cfb-298">对于每个包含可编辑 ER 组件中缺少的数据源的绑定，将在 ER Operations 设计器或 ER 模型映射设计器中发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-298">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model mapping designer.</span></span>

<span data-ttu-id="a3cfb-299">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-299">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-300">开始同时配置 ER 数据模型和 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-300">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a3cfb-301">在数据模型树中，添加一个名为 **X** 的字段，然后选择 **整数** 作为数据类型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-301">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![“数据模型”页面上包含 X 字段和整数数据类型的数据模型树](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a3cfb-303">在模型映射设计器内的 **数据源** 窗格中，添加一个 **计算字段** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-303">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a3cfb-304">将新数据源命名为 **Y**，然后对其进行配置，以使其包含表达式 `INTVALUE(100)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-304">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a3cfb-305">将 **X** 绑定到 **Y**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-305">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a3cfb-306">在模型映射设计器的 **数据源** 窗格中，删除 **Y** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-306">In the model mapping designer, in the **Data sources** pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="a3cfb-307">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-307">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![检查模型映射设计器页上的可编辑 ER 模型映射组件](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="a3cfb-309">请注意，发生了验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-309">Notice that a validation error occurs.</span></span> <span data-ttu-id="a3cfb-310">该消息指出，**X** 数据模型字段的绑定中包含引用 **Y** 数据源的路径，但找不到此数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-310">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-311">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-311">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-312">选择 **取消绑定** 通过删除缺少的数据源绑定自动解决此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-312">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-313">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-313">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-314">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-314">Option 1</span></span>

<span data-ttu-id="a3cfb-315">取消绑定 **X** 数据模型字段以停止引用不存在的 **Y** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-315">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-316">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-316">Option 2</span></span>

<span data-ttu-id="a3cfb-317">在模型映射设计器的 **数据源** 窗格中，再次添加 **Y** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-317">In the model mapping designer, in the **Data sources** pane, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="a3cfb-318">带 FILTER 函数的表达式的可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-318">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="a3cfb-319">内置的 [FILTER](er-functions-list-filter.md) ER 函数用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-319">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a3cfb-320">**记录列表** 类型的数据源用作此函数的参数，并指定调用的应用程序源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-320">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="a3cfb-321">ER 检查是否可以为 `FILTER` 函数中引用的数据源建立直接 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-321">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="a3cfb-322">如果无法建立直接查询，ER 模型映射设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-322">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-323">您收到的消息指出在运行时不能运行其中包含 `FILTER` 函数的 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-323">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span>

<span data-ttu-id="a3cfb-324">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-324">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-325">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-325">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-326">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-326">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-327">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-327">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-328">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-328">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a3cfb-329">添加一个类型为 **计算字段** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-329">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="a3cfb-330">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum="US-101")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-330">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a3cfb-331">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **Vendor** 数据源中的 `FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-331">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="a3cfb-332">通过向裁剪后的供应商帐号添加 **计算字段** 类型的嵌套字段，修改 **Vendor** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-332">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a3cfb-333">将这个新的嵌套字段命名为 **$AccNumber**，然后对其进行配置，以使其包含表达式 `TRIM(Vendor.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-333">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="a3cfb-334">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询 **Vendor** 数据源中的 `FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-334">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![验证是否可以在“模型映射设计器”页面上查询表达式](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="a3cfb-336">请注意，发生了验证错误，因为 **Vendor** 数据源中包含一个类型为 **计算字段** 的嵌套字段，并且该嵌套字段不允许将 **FilteredVendor** 数据源的表达式转换为直接 SQL 语句。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-336">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a3cfb-337">下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-337">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![在“格式设计器”页面运行可编辑格式时发生的运行时错误](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-339">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-339">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-340">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-340">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-341">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-341">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-342">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-342">Option 1</span></span>

<span data-ttu-id="a3cfb-343">不是向 **Vendor** 数据源添加类型为 **计算字段** 的嵌套字段，而是将 **$AccNumber** 嵌套字段添加到 **FilteredVendor** 数据源，并进行配置，以使其包含表达式 `TRIM(FilteredVendor.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-343">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="a3cfb-344">这样，`FILTER(Vendor, Vendor.AccountNum="US-101")` 表达式就可以在 SQL 级运行，之后再计算 **$ AccNumber** 嵌套字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-344">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-345">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-345">Option 2</span></span>

<span data-ttu-id="a3cfb-346">将 **FilteredVendor** 数据源的表达式从 `FILTER(Vendor, Vendor.AccountNum="US-101")` 更改为 `WHERE(Vendor, Vendor.AccountNum="US-101")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-346">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a3cfb-347">建议不要更改包含大量数据的表（事务表）的表达式，因为将提取所有记录，并且将在内存中选择所需的记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-347">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="a3cfb-348">因此，这种方法可能会导致性能低下。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-348">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a3cfb-349">有关详细信息，请参阅 [WHERE ER 函数](er-functions-list-where.md)。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-349">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="a3cfb-350">GROUPBY 数据源的可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-350">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="a3cfb-351">**GROUPBY** 数据源将查询结果拆分为多组记录，通常是为了对各组执行一项或多项聚合。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-351">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="a3cfb-352">可以配置每个 **GROUPBY** 数据源，以使其在数据库级或在内存中运行。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-352">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a3cfb-353">如果配置了 **GROUPBY** 数据源以使其在数据库级运行，ER 将检查是否可建立对该数据源中引用的数据源的直接 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-353">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="a3cfb-354">如果无法建立直接查询，ER 模型映射设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-354">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-355">您收到的消息指出，运行时不能运行配置的 **GROUPBY** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-355">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="a3cfb-356">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-356">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-357">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-357">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-358">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-358">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-359">将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-359">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a3cfb-360">添加一个类型为 **分组依据** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-360">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="a3cfb-361">将新数据源命名为 **GroupedTrans**，然后按照下面的方法配置：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-361">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="a3cfb-362">选择 **Trans** 数据源作为应分组的记录的来源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-362">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="a3cfb-363">在 **执行位置** 字段中，选择 **查询** 以指定要在数据库级运行此数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-363">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![在“编辑分组依据参数”页面上配置数据源](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="a3cfb-365">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **GroupedTrans** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-365">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="a3cfb-366">通过向裁剪后的供应商帐号添加 **计算字段** 类型的嵌套字段，修改 **Trans** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-366">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a3cfb-367">将新数据源命名为 **$AccNumber**，然后对其进行配置，以使其包含表达式 `TRIM(Trans.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-367">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![在“模型映射设计器”页面中配置数据源](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="a3cfb-369">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **GroupedTrans** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-369">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![验证 ER 模型映射组件，并验证是否可在“模型映射设计器”页面中查询 GroupedTrans 数据源](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="a3cfb-371">请注意，发生了验证错误，因为 **Trans** 数据源中包含一个类型为 **计算字段** 的嵌套字段，并且该嵌套字段不允许调用要转换为直接 SQL 语句的 **GroupedTrans** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-371">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a3cfb-372">下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-372">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![在“格式设计器”页面上忽略了警告时发生的运行时错误](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-374">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-374">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-375">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-375">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-376">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-376">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-377">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-377">Option 1</span></span>

<span data-ttu-id="a3cfb-378">不是向 **Trans** 数据源添加类型为 **计算字段** 的嵌套字段，而是为 **GroupedTrans** 数据源的 **GroupedTrans.lines** 项添加 **$AccNumber** 嵌套字段，并进行配置，以使其包含表达式 `TRIM(GroupedTrans.lines.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-378">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="a3cfb-379">这样，**GroupedTrans** 数据源就可以在 SQL 级运行，之后再计算 **$ AccNumber** 嵌套字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-379">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-380">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-380">Option 2</span></span>

<span data-ttu-id="a3cfb-381">将 **GroupedTrans** 数据源的 **执行位置** 字段值从 **查询** 更改为 **在内存中**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-381">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a3cfb-382">建议不要更改包含大量数据的表（事务表）的值，因为将提取所有记录，并且将在内存中执行分组和聚合。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-382">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="a3cfb-383">因此，这种方法可能会导致性能低下。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-383">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="a3cfb-384">JOIN 数据源的可执行性</span><span class="sxs-lookup"><span data-stu-id="a3cfb-384">Executability of a JOIN data source</span></span>

<span data-ttu-id="a3cfb-385">[JOIN](er-join-data-sources.md) 数据源根据相关字段合并两个或更多数据库表中的记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-385">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="a3cfb-386">可以配置每个 **JOIN** 数据源，以使其在数据库级或在内存中运行。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-386">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a3cfb-387">如果配置了 **JOIN** 数据源以使其在数据库级运行，ER 将检查是否可建立对该数据源中引用的数据源的直接 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-387">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="a3cfb-388">如果无法使用至少一个引用数据源建立直接 SQL 查询，ER 模型映射设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-388">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-389">您收到的消息指出，运行时不能运行配置的 **JOIN** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-389">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="a3cfb-390">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-390">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-391">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-391">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-392">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-392">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-393">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-393">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-394">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-394">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a3cfb-395">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-395">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="a3cfb-396">将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-396">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="a3cfb-397">添加一个 **计算字段** 类型的数据源作为 **Vendor** 数据源的嵌套字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-397">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="a3cfb-398">将新数据源命名为 **FilteredTrans**，然后对其进行配置，以使其包含表达式 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-398">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="a3cfb-399">添加一个类型为 **联接** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-399">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="a3cfb-400">将新数据源命名为 **JoinedList**，然后按照下面的方法配置：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-400">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="a3cfb-401">将 **Vendor** 数据源作为要联接的第一组记录添加。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-401">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="a3cfb-402">将 **Vendor.FilteredTrans** 数据源作为要联接的第二组记录添加。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-402">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="a3cfb-403">选择 **INNER** 作为类型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-403">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="a3cfb-404">在 **执行** 字段中，选择 **查询** 以指定要在数据库级运行此数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-404">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![在“联接设计器”页面中配置数据源](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="a3cfb-406">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **JoinedList** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-406">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="a3cfb-407">将 **Vendor.FilteredTrans** 数据源的表达式从 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` 更改为 `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-407">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="a3cfb-408">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件，然后验证是否可查询配置的 **JoinedList** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-408">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![验证可编辑模型映射组件，然后在“模型映射设计器”页面中验证是否可查询 JoinedList 数据源](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="a3cfb-410">请注意，发生了验证错误，因为 **Vendor.FilteredTrans** 数据源无法转换为直接 SQL 调用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-410">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="a3cfb-411">此外，直接 SQL 调用不允许调用要转换为直接 SQL 语句的 **JoinedList** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-411">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![“模型映射设计器”页面中验证 JoinedList 数据源失败导致的运行时错误](./media/er-components-inspections-06c.png)

<span data-ttu-id="a3cfb-413">下图显示了如果忽略此警告并选择 **运行** 以运行配置为使用模型映射的格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-413">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![在“格式设计器”页面上运行可编辑格式](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-415">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-415">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-416">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-416">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-417">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-417">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-418">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-418">Option 1</span></span>

<span data-ttu-id="a3cfb-419">按照警告的建议，将 **Vendor.FilteredTrans** 数据源的表达式从 `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` 更改为 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-419">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![“模型映射设计器”页面中更新后的数据源表达式](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="a3cfb-421">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-421">Option 2</span></span>

<span data-ttu-id="a3cfb-422">将 **JoinedList** 数据源的 **执行位置** 字段值从 **查询** 更改为 **在内存中**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-422">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a3cfb-423">建议不要更改包含大量数据的表（事务表）的值，因为将提取所有记录，并且将在内存中发生联接。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-423">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="a3cfb-424">因此，这种方法可能会导致性能低下。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-424">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a3cfb-425">将显示验证警告，以便告知您此风险。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-425">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="a3cfb-426">FILTER 与 WHERE 函数的偏好对比</span><span class="sxs-lookup"><span data-stu-id="a3cfb-426">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="a3cfb-427">内置的 [FILTER](er-functions-list-filter.md) ER 函数用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-427">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a3cfb-428">[WHERE](er-functions-list-where.md) 函数从给定源获取所有记录，然后在内存中选择记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-428">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="a3cfb-429">**记录列表** 类型的数据源用作这两个函数的参数，并指定源以获取记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-429">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="a3cfb-430">ER 检查是否可以为 **WHERE** 函数中引用的数据源建立直接 SQL 调用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-430">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="a3cfb-431">如果无法建立直接调用，ER 模型映射设计器中会发生验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-431">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-432">您收到的消息建议您使用 **FILTER** 函数而不是 **WHERE** 函数来帮助提高效率。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-432">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="a3cfb-433">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-433">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-434">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-434">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-435">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-435">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-436">将新数据源命名为 **Trans**。在 **表** 字段中，选择 **VendTrans** 指定该数据源将请求 VendTrans 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-436">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a3cfb-437">添加一个 **计算字段** 类型的数据源作为 **Vendor** 数据源的嵌套字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-437">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="a3cfb-438">将新数据源命名为 **FilteredTrans**，然后对其进行配置，以使其包含表达式 `WHERE(Trans, Trans.AccountNum="US-101")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-438">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a3cfb-439">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-439">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a3cfb-440">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-440">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-441">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-441">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a3cfb-442">添加一个类型为 **计算字段** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-442">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="a3cfb-443">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `WHERE(Vendor, Vendor.AccountNum="US-101")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-443">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="a3cfb-444">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-444">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![检查模型映射设计器页上的可编辑模型映射组件](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="a3cfb-446">请注意，验证警告建议对 **FilteredVendor** 和 **FilteredTrans** 数据源使用 **FILTER** 函数，而不是 **WHERE** 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-446">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![建议在“模型映射设计器”页面上使用 FILTER 函数，而不是 WHERE 函数](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-448">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-448">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-449">选择 **修复** 以将 **WHERE** 函数替换为这种检查的 **警告** 选项卡上网格中显示的所有数据源的表达式中的 **FILTER** 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-449">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a3cfb-450">或者，您可以在网格中选择单个警告的行，然后选择 **修复所选**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-450">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a3cfb-451">在这种情况下，仅在所选警告中提到的数据源中自动更改表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-451">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![选择“修复”以在“模型映射设计器”页面上将 WHERE 函数自动替换为 FILTER 函数](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-453">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-453">Manual resolution</span></span>

<span data-ttu-id="a3cfb-454">可以通过将 **WHERE** 函数替换为 **FILTER** 函数，手动调整验证网格中所有数据源的表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-454">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="a3cfb-455">ALLITEMSQUERY 相比 ALLITEMS 函数的偏好对比</span><span class="sxs-lookup"><span data-stu-id="a3cfb-455">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="a3cfb-456">内置的 [ALLITEMS](er-functions-list-allitems.md) 和 [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER 函数返回一个平展 **记录列表** 值，该值由表示与指定路径匹配的所有项的记录的列表构成。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-456">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="a3cfb-457">ER 检查是否可以为 **ALLITEMS** 函数中引用的数据源建立直接 SQL 调用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-457">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="a3cfb-458">如果无法建立直接调用，ER 模型映射设计器中会发生验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-458">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-459">您收到的消息建议您使用 **ALLITEMSQUERY** 函数而不是 **ALLITEMS** 函数来帮助提高效率。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-459">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="a3cfb-460">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-460">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-461">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-461">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-462">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-462">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-463">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-463">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-464">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-464">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a3cfb-465">添加一个类型为 **计算字段** 的数据源，以便获取多个供应商的记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-465">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="a3cfb-466">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-466">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="a3cfb-467">添加一个类型为 **计算字段** 的数据源，以便获取筛选后的所有供应商的交易。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-467">Add a data source of the **Calculated field** type to get the transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="a3cfb-468">将新数据源命名为 **FilteredVendorTrans**，然后对其进行配置，以使其包含表达式 `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-468">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="a3cfb-469">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-469">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![检查“模型映射设计器”页上的可编辑模型映射组件](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="a3cfb-471">请注意，发生了验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-471">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a3cfb-472">此消息建议为 **FilteredVendorTrans** 数据源使用 **ALLITEMSQUERY** 函数，而不是 **ALLITEMS** 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-472">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![建议在“模型映射设计器”页面上使用 ALLITEMSQUERY 函数，而不是 ALLITEMS 函数](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-474">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-474">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-475">选择 **修复** 以将 **ALLITEMS** 函数替换为这种检查的 **警告** 选项卡上网格中显示的所有数据源的表达式中的 **ALLITEMSQUERY** 函数。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-475">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a3cfb-476">或者，您可以在网格中选择单个警告的行，然后选择 **修复所选**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-476">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a3cfb-477">在这种情况下，仅在所选警告中提到的数据源中自动更改表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-477">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![在“模型映射设计器”页面上选择“修复所选”](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-479">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-479">Manual resolution</span></span>

<span data-ttu-id="a3cfb-480">可以通过将 **ALLITEMS** 函数替换为 **ALLITEMSQUERY** 函数，手动调整验证网格中提及的所有数据源的表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-480">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="a3cfb-481">空列表用例的注意事项</span><span class="sxs-lookup"><span data-stu-id="a3cfb-481">Consideration of empty list cases</span></span>

<span data-ttu-id="a3cfb-482">可以配置 ER 格式或模型映射组件以获取类型为 **记录列表** 的数据源的字段值。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-482">You can configure your ER format or model mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="a3cfb-483">ER 将检查您的设计是否考虑以下方案：调用的数据源中不包含任何记录（即为空），以防从不存在的记录获取值时发生运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-483">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="a3cfb-484">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-484">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-485">开始同时配置 ER 数据模型、ER 模型映射和 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-485">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a3cfb-486">在数据模型树中，添加一个名称为 **Root3** 的根项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-486">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a3cfb-487">通过添加一个类型为 **记录列表** 的嵌套项，修改 **Root3** 项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-487">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a3cfb-488">将这个新的嵌套项命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-488">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a3cfb-489">按照以下方法修改 **Vendor** 项：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-489">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a3cfb-490">添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **Name**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-490">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a3cfb-491">添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **AccountNumber**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-491">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![在“数据模型”页面上添加嵌套字段](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="a3cfb-493">在模型映射设计器内的 **数据源** 窗格中，添加一个 **Dynamics 365 for Operations \\ 表记录** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-493">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a3cfb-494">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-494">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-495">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-495">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a3cfb-496">添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中搜索供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-496">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a3cfb-497">将新数据源命名为 **RequestedAccountNum**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-497">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a3cfb-498">在 **标签** 字段中，输入 **供应商帐号**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-498">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a3cfb-499">在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-499">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a3cfb-500">添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-500">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a3cfb-501">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-501">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a3cfb-502">按照以下方法将数据模型项绑定到配置的数据源：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-502">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a3cfb-503">将 **FilteredVendor** 绑定到 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-503">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a3cfb-504">将 **FilteredVendor.AccountNum** 绑定到 **Vendor.AccountNumber**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-504">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="a3cfb-505">将 **FilteredVendor.'name()'** 绑定到 **Vendor.Name**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-505">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![在“模型映射设计器”页面中绑定数据模型项](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="a3cfb-507">在格式结构树中，添加以下项，以便生成一个 XML 格式且包含供应商详细信息的传出文档：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-507">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="a3cfb-508">添加 **Statement** 根 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-508">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a3cfb-509">为 **Statement** XML 元素添加嵌套的 **Party** XML 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-509">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a3cfb-510">为 **Party** XML 元素添加以下嵌套的 XML 属性：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-510">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a3cfb-511">姓名</span><span class="sxs-lookup"><span data-stu-id="a3cfb-511">Name</span></span>
        - <span data-ttu-id="a3cfb-512">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a3cfb-512">AccountNum</span></span>

14. <span data-ttu-id="a3cfb-513">按照以下方法将格式元素绑定到提供的数据源：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-513">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a3cfb-514">将 **Statement\\Party\\Name** 格式元素绑定到 **model.Vendor.Name** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-514">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a3cfb-515">将 **Statement\\Party\\AccountNum** 格式元素绑定到 **model.Vendor.AccountNumber** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-515">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a3cfb-516">选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-516">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![在“格式设计器”页面上验证绑定到数据源的格式元素](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="a3cfb-518">请注意，发生了验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-518">Notice that a validation error occurs.</span></span> <span data-ttu-id="a3cfb-519">此消息表示，如果 `model.Vendor` 列表为空，在运行时可能为配置的 **Statement\\Party\\Name** 和 **Statement\\Party\\AccountNum** 格式组件引发错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-519">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![有关配置的格式组件的潜在错误的验证错误](./media/er-components-inspections-09d.png)

<span data-ttu-id="a3cfb-521">下图显示了如果忽略此警告，选择 **运行** 以运行格式，然后选择不存在的供应商的帐号，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-521">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="a3cfb-522">因为请求的供应商不存在，`model.Vendor` 列表将为空（即，其中将不包含任何记录）。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-522">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![格式映射运行期间发生的运行时错误](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-524">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-524">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-525">对于 **警告** 选项卡上网格中的所选行，可以选择 **取消绑定**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-525">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="a3cfb-526">将从格式元素中自动删除 **路径** 列中指向的绑定。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-526">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-527">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-527">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-528">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-528">Option 1</span></span>

<span data-ttu-id="a3cfb-529">您可以将 **Statement\\Party\\Name** 格式元素绑定到 `model.Vendor` 数据源项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-529">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="a3cfb-530">在运行时，此绑定首先调用 `model.Vendor` 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-530">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="a3cfb-531">当 `model.Vendor` 返回空记录列表时，将不运行嵌套的格式元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-531">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="a3cfb-532">因此，此格式配置不发生验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-532">Therefore, no validation warnings occur for this format configuration.</span></span>

![在“格式设计器”页面上将格式元素绑定到数据源项](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="a3cfb-534">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-534">Option 2</span></span>

<span data-ttu-id="a3cfb-535">将 **Statement\\Party\\Name** 格式元素的绑定从 `model.Vendor.Name` 更改为 `FIRSTORNULL(model.Vendor).Name`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-535">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="a3cfb-536">更新后的绑定将有条件地把类型为 **记录列表** 的 `model.Vendor` 数据源的第一个记录转换为类型为 **记录** 的新数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-536">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="a3cfb-537">这个新数据源中包含同一组字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-537">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="a3cfb-538">如果 `model.Vendor` 数据源中至少有一个记录，则将使用 `model.Vendor` 数据源的第一个记录的字段的值填充该记录的字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-538">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="a3cfb-539">在这种情况下，更新后的绑定将返回供应商名称。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-539">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="a3cfb-540">否则，将使用创建的记录的每个字段的数据类型默认值填充这些字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-540">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="a3cfb-541">在此情况下，返回的 **字符串** 数据类型默认值为空白字符串。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-541">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="a3cfb-542">因此，绑定到 `FIRSTORNULL(model.Vendor).Name` 表达式时，**Statement\\Party\\Name** 格式元素不会发生验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-542">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![更改后的绑定解决了“格式设计器”页面上的验证警告](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="a3cfb-544">选项 3</span><span class="sxs-lookup"><span data-stu-id="a3cfb-544">Option 3</span></span>

<span data-ttu-id="a3cfb-545">如果要显式指定当类型为 **记录列表** 的 `model.Vendor` 数据源中不包含任何记录时在生成的文档中输入的数据（此示例中为文本 **不可用**），请将 **Statement\\Party\\Name** 格式元素的绑定从 `model.Vendor.Name` 更改为 `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-545">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="a3cfb-546">也可以使用表达式 `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-546">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="a3cfb-547">其他注意事项</span><span class="sxs-lookup"><span data-stu-id="a3cfb-547">Additional consideration</span></span>

<span data-ttu-id="a3cfb-548">此检查还会向您警示另一个潜在问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-548">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="a3cfb-549">默认情况下，在将 **Statement\\Party\\Name** 和 **Statement\\Party\\AccountNum** 格式元素绑定到类型为 **记录列表** 的 `model.Vendor` 数据源的相应字段时，这些绑定将运行，并采用 `model.Vendor` 数据源第一个记录的相应字段（如果该列表非空）。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-549">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="a3cfb-550">因为尚未将 **Statement\\Party** 格式元素与 `model.Vendor` 数据源绑定，因此在格式执行期间将不针对 `model.Vendor` 数据源的每个记录迭代 **Statement\\Party** 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-550">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="a3cfb-551">相反，如果记录列表中包含多个记录，则仅使用该列表的第一个记录中的信息填充生成的文档。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-551">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="a3cfb-552">因此，如果该格式用于使用有关 `model.Vendor` 数据源中的所有供应商的信息填充生成的文档，可能会出错。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-552">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="a3cfb-553">若要解决此问题，请将 **Statement\\Party** 元素与 `model.Vendor` 数据源绑定。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-553">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="a3cfb-554">带 FILTER 函数的表达式的可执行性（高速缓存）</span><span class="sxs-lookup"><span data-stu-id="a3cfb-554">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="a3cfb-555">多个内置 ER 函数（包括 [FILTER](er-functions-list-filter.md) 和 [ALLITEMSQUERY](er-functions-list-allitemsquery.md)）用于通过下达一个 SQL 调用以访问应用程序表、视图或数据实体来获取记录列表形式的所需数据。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-555">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a3cfb-556">**记录列表** 类型的数据源用作这些函数中每一个的参数，并指定调用的应用程序源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-556">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="a3cfb-557">ER 检查是否可以为这些函数之一中引用的数据源建立直接 SQL 调用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-557">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="a3cfb-558">如果因为数据源标记成了[已高速缓存](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)导致无法建立直接调用，ER 模型映射设计器中会发生验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-558">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a3cfb-559">您收到的消息指出在运行时不能运行其中包含这些函数之一的 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-559">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="a3cfb-560">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-560">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-561">开始配置 ER 模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-561">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a3cfb-562">添加一个类型为 **Dynamics 365 for Operations \\ 表记录** 的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-562">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a3cfb-563">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-563">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-564">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-564">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a3cfb-565">添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中搜索供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-565">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="a3cfb-566">将新数据源命名为 **RequestedAccountNum**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-566">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a3cfb-567">在 **标签** 字段中，输入 **供应商帐号**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-567">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a3cfb-568">在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-568">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="a3cfb-569">添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-569">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="a3cfb-570">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-570">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="a3cfb-571">将配置的 **Vendor** 数据源标记为已高速缓存。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-571">Mark the configured **Vendor** data source as cached.</span></span>

    ![在“模型映射设计器”页上配置模型映射组件](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="a3cfb-573">选择 **验证** 检查 **模型映射设计器** 页上的可编辑模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-573">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![在“模型映射设计器”页面上验证应用于高速缓存供应商数据源的 FILTER 函数](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="a3cfb-575">请注意，发生了验证错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-575">Notice that a validation error occurs.</span></span> <span data-ttu-id="a3cfb-576">该消息指出不能将 **FILTER** 函数应用于高速缓存的 **Vendor** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-576">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="a3cfb-577">下图显示了如果忽略此警告并选择 **运行** 以运行格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-577">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![在“格式设计器”页面运行格式映射期间发生的运行时错误](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-579">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-579">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-580">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-580">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-581">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-581">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-582">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-582">Option 1</span></span>

<span data-ttu-id="a3cfb-583">删除 **Vendor** 数据源中的 **Cache** 标志。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-583">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="a3cfb-584">然后，**FilteredVendor** 数据源将变为可执行，但是每次调用 **FilteredVendor** 数据源时，都将访问 VendTable 表中引用的 **Vendor** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-584">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-585">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-585">Option 2</span></span>

<span data-ttu-id="a3cfb-586">将 **FilteredVendor** 数据源的表达式从 `FILTER(Vendor, Vendor.AccountNum="US-101")` 更改为 `WHERE(Vendor, Vendor.AccountNum="US-101")`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-586">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a3cfb-587">在此情况下，仅在首次调用 **Vendor** 数据源时，才能访问 VendTable 表中引用的 **Vendor** 数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-587">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="a3cfb-588">但是，将在内存中选择记录。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-588">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="a3cfb-589">因此，这种方法可能会导致性能低下。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-589">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="a3cfb-590">缺少绑定</span><span class="sxs-lookup"><span data-stu-id="a3cfb-590">Missing binding</span></span>

<span data-ttu-id="a3cfb-591">当您配置 ER 格式组件时，基本 ER 数据模型将作为 ER 格式的默认数据源提供。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-591">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="a3cfb-592">运行配置的 ER 格式时，将使用基本模型的[默认模型映射](er-country-dependent-model-mapping.md)使用应用程序数据填充数据模型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-592">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="a3cfb-593">如果您将格式元素绑定到未绑定到当前作为可编辑格式的默认模型映射选择的模型映射中的任何数据源的数据模型项，ER 格式设计器将显示警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-593">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model mapping that is currently selected as the default model mapping for the editable format.</span></span> <span data-ttu-id="a3cfb-594">运行时不能运行这种绑定，因为运行的格式不能使用应用程序数据填充绑定的元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-594">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="a3cfb-595">因此，在运行时会发生错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-595">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="a3cfb-596">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-596">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-597">开始同时配置 ER 数据模型、ER 模型映射和 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-597">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a3cfb-598">在数据模型树中，添加一个名称为 **Root3** 的根项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-598">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a3cfb-599">通过添加一个类型为 **记录列表** 的新嵌套项，修改 **Root3** 项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-599">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a3cfb-600">将这个新的嵌套项命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-600">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a3cfb-601">按照以下方法修改 **Vendor** 项：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-601">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a3cfb-602">添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **Name**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-602">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a3cfb-603">添加一个类型为 **字符串** 的嵌套字段，然后将其命名为 **AccountNumber**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-603">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![在“数据模型”页面上向供应商项添加嵌套字段](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="a3cfb-605">在模型映射设计器内的 **数据源** 窗格中，添加一个 **Dynamics 365 for Operations \\ 表记录** 类型的数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-605">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a3cfb-606">将新数据源命名为 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-606">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a3cfb-607">在 **表** 字段中，选择 **VendTable** 指定此数据源将请求 VendTable 表。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-607">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a3cfb-608">添加一个类型为 **常规 \\ 用户输入参数** 的数据源，以便在运行时对话框中查询供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-608">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a3cfb-609">将新数据源命名为 **RequestedAccountNum**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-609">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a3cfb-610">在 **标签** 字段中，输入 **供应商帐号**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-610">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a3cfb-611">在 **Operations 数据类型名称** 字段中，保留默认值 **描述**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-611">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a3cfb-612">添加一个类型为 **计算字段** 的数据源，以便筛选查询的供应商。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-612">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a3cfb-613">将新数据源命名为 **FilteredVendor**，然后对其进行配置，以使其包含表达式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-613">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a3cfb-614">按照以下方法将数据模型项绑定到配置的数据源：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-614">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a3cfb-615">将 **FilteredVendor** 绑定到 **Vendor**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-615">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a3cfb-616">将 **FilteredVendor.AccountNum** 绑定到 **Vendor.AccountNumber**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-616">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3cfb-617">**Vendor.Name** 数据模型字段保持未绑定。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-617">The **Vendor.Name** data model field remains unbound.</span></span>

    ![绑定到配置的数据源的数据模型项，以及“模型映射设计器”页面中取消绑定的数据模型项](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="a3cfb-619">在格式结构树中，添加以下项，以便生成一个 XML 格式且包含查询的供应商的详细信息的传出文档：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-619">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="a3cfb-620">添加 **Statement** 根 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-620">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a3cfb-621">为 **Statement** XML 元素添加嵌套的 **Party** XML 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-621">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a3cfb-622">为 **Party** XML 元素添加以下嵌套的 XML 属性：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-622">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a3cfb-623">姓名</span><span class="sxs-lookup"><span data-stu-id="a3cfb-623">Name</span></span>
        - <span data-ttu-id="a3cfb-624">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a3cfb-624">AccountNum</span></span>

14. <span data-ttu-id="a3cfb-625">按照以下方法将格式元素绑定到提供的数据源：</span><span class="sxs-lookup"><span data-stu-id="a3cfb-625">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a3cfb-626">将 **Statement\\Party** 格式元素绑定到 `model.Vendor` 数据源项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-626">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="a3cfb-627">将 **Statement\\Party\\Name** 格式元素绑定到 **model.Vendor.Name** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-627">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a3cfb-628">将 **Statement\\Party\\AccountNum** 格式元素绑定到 **model.Vendor.AccountNumber** 数据源字段。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-628">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a3cfb-629">选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-629">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![在“格式设计器”页面上验证 ER 格式组件](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="a3cfb-631">请注意，发生了验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-631">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a3cfb-632">此消息指出 **model.Vendor.Name** 数据源字段未绑定到模型映射中配置供格式使用的任何数据源。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-632">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model mapping that is configured to be used by the format.</span></span> <span data-ttu-id="a3cfb-633">因此，在运行时不能填充 **Statement\\Party\\Name** 格式，并且可能会发生运行时异常。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-633">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![在“格式设计器”页面上验证 ER 格式元素](./media/er-components-inspections-11d.png)

<span data-ttu-id="a3cfb-635">下图显示了如果忽略此警告并选择 **运行** 以运行格式，将出现的运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-635">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![在“格式设计器”页面上运行可编辑格式](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-637">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-637">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-638">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-638">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-639">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-639">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-640">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-640">Option 1</span></span>

<span data-ttu-id="a3cfb-641">通过为 **model.Vendor.Name** 数据源字段添加绑定来修改配置的模型映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-641">Modify the configured model mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-642">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-642">Option 2</span></span>

<span data-ttu-id="a3cfb-643">通过删除 **Statement\\Party\\Name** 格式元素的绑定修改配置的格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-643">Modify the configured format by removing the binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="a3cfb-644">未链接模板</span><span class="sxs-lookup"><span data-stu-id="a3cfb-644">Not linked template</span></span>

<span data-ttu-id="a3cfb-645">在 [手动](er-fillable-excel.md#manual-entry)配置 ER 格式组件以使用模板生成传出文档时，必须手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需模板，并在添加的 **Excel\\File** 元素中选择该附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-645">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a3cfb-646">这样，您指示添加的元素将在运行时填充所选模板。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-646">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a3cfb-647">在配置 [状态](general-electronic-reporting.md#component-versioning)为 **草稿** 的格式组件版本时，可以向可编辑组件添加多个模板，然后在 **Excel\\File** 元素中选择每个模板以运行 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-647">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="a3cfb-648">这样，您可以看到在运行时如何填充不同的模板。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-648">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="a3cfb-649">如果有模板未在任何 **Excel\\File** 元素中选中，ER 格式设计器将警告您，当模板的状态从 **草稿** 更改为 **已完成** 时，将从可编辑 ER 格式组件版本删除这些模板。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-649">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="a3cfb-650">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-650">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-651">开始配置 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-651">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a3cfb-652">在格式结构树中，添加 **Excel\\File** 元素。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-652">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="a3cfb-653">为您刚才添加的 **Excel\\File** 元素添加一个 Excel 工作簿文件 **A.xlsx** 作为附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-653">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a3cfb-654">使用 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中配置的文档类型指定 ER 格式模板的存储。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-654">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="a3cfb-655">为 **Excel\\File** 元素再添加一个 Excel 工作簿文件 **B.xlsx** 作为附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-655">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="a3cfb-656">使用用于工作簿文件A 的同一种文档类型。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-656">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="a3cfb-657">在 **Excel\\File** 元素中，选择工作簿文件 A。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-657">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="a3cfb-658">选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-658">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![在“格式设计器”页面上验证工作簿文件的可编辑格式组件](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="a3cfb-660">请注意，发生了验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-660">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a3cfb-661">该消息指出工作簿文件 B.xlsx 未链接到任何组件，并且将在更改配置版本状态后将其删除。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-661">The message states that workbook file B.xlsx isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-662">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-662">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-663">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-663">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-664">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-664">Manual resolution</span></span>

<span data-ttu-id="a3cfb-665">通过删除所有未链接到任何 **Excel\\File** 元素的所有模板来修改配置的格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-665">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="a3cfb-666">不同步格式</span><span class="sxs-lookup"><span data-stu-id="a3cfb-666">Not synced format</span></span>

<span data-ttu-id="a3cfb-667">在 [配置](er-fillable-excel.md) ER 格式组件以使用 Excel 模板生成传出文档时，可以手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需模板，并在添加的 **Excel\\File** 元素中选择该附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-667">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a3cfb-668">这样，您指示添加的元素将在运行时填充所选模板。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-668">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a3cfb-669">由于添加的 Excel 模板是外部设计的，因此可编辑的 ER 格式中可能包含添加的模板中缺少的 Excel 名称。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-669">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="a3cfb-670">ER 格式设计器会警告您有关引用添加的 Excel 模板中不包含的名称的 ER 格式元素的属性之间的任何不一致之处。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-670">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="a3cfb-671">以下步骤显示可能会如何发生此问题。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-671">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a3cfb-672">开始配置 ER 格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-672">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a3cfb-673">在格式结构树中，添加 **Excel\\File** 元素 **Report**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-673">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="a3cfb-674">为您刚才添加的 **Excel\\File** 元素添加一个 Excel 工作簿文件 **A.xlsx** 作为附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-674">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a3cfb-675">使用 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中配置的文档类型指定 ER 格式模板的存储。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-675">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a3cfb-676">确保添加的 Excel 工作簿中不包含名称 **ReportTitle**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-676">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="a3cfb-677">将 **Excel\\Cell** 元素 **Title** 作为 **Report** 元素的嵌套元素添加。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-677">Add the **Excel\\Cell** element **Title** as a nested element of the **Report** element.</span></span> <span data-ttu-id="a3cfb-678">在 **Excel 范围** 字段中，输入 **ReportTitle**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-678">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="a3cfb-679">选择 **验证** 检查 **格式设计器** 页上的可编辑格式组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-679">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![在“格式设计器”页面上验证嵌套元素和字段](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="a3cfb-681">请注意，发生了验证警告。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-681">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a3cfb-682">此消息指出您正在使用的 Excel 模板的工作表 **Sheet1** 中无名称 **ReportTitle**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-682">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![有关 Excel 模板的 Sheet1中无名称 ReportTitle 的验证警告](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-684">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-684">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-685">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-685">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-686">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-686">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-687">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-687">Option 1</span></span>

<span data-ttu-id="a3cfb-688">通过删除引用模板中缺少的 Excel 名称的所有元素来修改配置的格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-688">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-689">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-689">Option 2</span></span>

<span data-ttu-id="a3cfb-690">通过导入 Excel 模板[更新](er-fillable-excel.md#template-import)可编辑 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-690">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="a3cfb-691">将与导入的 Excel 模板的结构[同步](modify-electronic-reporting-format-reapply-excel-template.md)可编辑 ER 格式的结构。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-691">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="a3cfb-692">其他注意事项</span><span class="sxs-lookup"><span data-stu-id="a3cfb-692">Additional consideration</span></span>

<span data-ttu-id="a3cfb-693">要了解如何在[业务文档管理](er-business-document-management.md)的模板编辑器中将格式结构与 ER 模板同步，请参阅[更新业务文档模板的结构](er-bdm-update-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-693">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a><span data-ttu-id="a3cfb-694">未与 Word 模板格式同步</span><span class="sxs-lookup"><span data-stu-id="a3cfb-694">Not synced with a Word template format</span></span>

<span data-ttu-id="a3cfb-695">在 [配置](er-fillable-excel.md) ER 格式组件以使用 Word 模板生成传出文档时，可以手动添加 **Excel\\File** 元素，作为可编辑组件的附件添加所需 Word 模板，并在添加的 **Excel\\File** 元素中选择该附件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-695">When you [configure](er-fillable-excel.md) an ER format component to use a Word template to generate an outbound document, you can manually add the **Excel\\File** element, add the required Word template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span>

> [!NOTE]
> <span data-ttu-id="a3cfb-696">附加 Word 文档后，ER 格式设计器将可编辑元素显示为 **Word\\File**。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-696">When the Word document is attached, the ER format designer presents the editable element as **Word\\File**.</span></span>

<span data-ttu-id="a3cfb-697">这样，您指示添加的元素将在运行时填充所选模板。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-697">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a3cfb-698">由于添加的 Word 模板是外部设计的，因此可编辑的 ER 格式中可能包含添加的模板中缺少的 Word 内容控件引用。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-698">Because the added Word template has been externally designed, the editable ER format might contain references to Word content controls that are missing from the added template.</span></span> <span data-ttu-id="a3cfb-699">ER 格式设计器会警告您有关引用添加的 Excel 模板中不包含的内容控件的 ER 格式元素的属性之间的任何不一致之处。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-699">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to content controls that aren't included in the added Word template.</span></span>

<span data-ttu-id="a3cfb-700">有关显示此问题可能如何发生的示例，请参见[配置可编辑格式以禁止显示摘要部分](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control)。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-700">For an example that shows how this issue might occur, see [Configure the editable format to suppress the summary section](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-701">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-701">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-702">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-702">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-703">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-703">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-704">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-704">Option 1</span></span>

<span data-ttu-id="a3cfb-705">通过从格式元素中删除验证警告中提到的 **已移除** 公式来修改配置的格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-705">Modify the configured format by deleting the **Removed** formula from the format element that is mentioned in the validation warning.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-706">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-706">Option 2</span></span>

<span data-ttu-id="a3cfb-707">修改使用的 Word 模板，方法是向相关 Word 内容控件[添加](er-design-configuration-word-suppress-controls.md#tag-control)必需的标记。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-707">Modify the using Word template by [adding](er-design-configuration-word-suppress-controls.md#tag-control) the required tag to the relevant Word content control.</span></span>

## <a name="no-default-mapping"></a><a id="i15"></a><span data-ttu-id="a3cfb-708">没有默认映射</span><span class="sxs-lookup"><span data-stu-id="a3cfb-708">No default mapping</span></span>

<span data-ttu-id="a3cfb-709">当[缺少绑定](#i11)检查完成后，将根据相关模型映射组件的绑定来评估检查的格式绑定。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-709">When the [Missing binding](#i11) inspection is done, the inspected format bindings are evaluated against the bindings of the relevant model mapping component.</span></span> <span data-ttu-id="a3cfb-710">因为你可以导入[一些](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER 模型映射配置到您的 Finance 实例，并且每个配置可能都包含适用的模型映射组件，所以必须选择一个配置作为默认配置。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-710">Because you can import [several](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER model mapping configurations to your Finance instance, and each configuration might contain the applicable model mapping component, one configuration must be selected as the default configuration.</span></span> <span data-ttu-id="a3cfb-711">否则，当您尝试运行、编辑或验证检查的 ER 格式时，将发生异常，并且您将收到以下消息：“\<configuration names separated by comma\> 配置中的 \<model name (root descriptor)\> 数据模型存在多个模型映射。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-711">Otherwise, when you try to run, edit, or validate the inspected ER format, an exception will occur, and you will receive the following message: "More than one model mapping exists for the \<model name (root descriptor)\> data model in the configurations \<configuration names separated by comma\>.</span></span> <span data-ttu-id="a3cfb-712">将其中一个配置设置为默认配置。”</span><span class="sxs-lookup"><span data-stu-id="a3cfb-712">Set one of the configurations as default."</span></span>

<span data-ttu-id="a3cfb-713">有关显示此问题可能如何发生以及如何解决的示例，请参见[管理单个模型根的多个派生映射](er-multiple-model-mappings.md)。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-713">For an example that shows how this issue might occur and how it can be fixed, see [Manage several derived mappings for a single model root](er-multiple-model-mappings.md).</span></span>

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a><span data-ttu-id="a3cfb-714">页眉或页脚组件的设置不一致</span><span class="sxs-lookup"><span data-stu-id="a3cfb-714">Inconsistent setting of Header or Footer components</span></span>

<span data-ttu-id="a3cfb-715">当你 [配置](er-fillable-excel.md) ER 格式组件以使用 Excel 模板生成出站文档时，您可以添加 **Excel\\页眉** 组件以填充 Excel 工作簿中工作表顶部的页眉。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-715">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can add the **Excel\\Header** component to fill in headers at the top of a worksheet in an Excel workbook.</span></span> <span data-ttu-id="a3cfb-716">您也可以添加 **Excel\\页脚** 组件以填充工作表底部的页脚。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-716">You can also add the **Excel\\Footer** component to fill in footers at the bottom of a worksheet.</span></span> <span data-ttu-id="a3cfb-717">对于您添加的每个 **Excel\\页眉** 或者 **Excel\\页脚** 组件，您必须设置 **页眉/页脚外观** 属性，以指定要为其运行组件的页面。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-717">For every **Excel\\Header** or **Excel\\Footer** component that you add, you must set the **Header/footer appearance** property to specify the pages that the component is run for.</span></span> <span data-ttu-id="a3cfb-718">因为你可以为单个 **工作表** 组件配置一些 **Excel\\页眉** 或 **Excel\\页脚** 组件，并且您可以为 Excel 工作表中的不同类型页面生成不同的页眉或页脚，因此必须为 **页眉/页脚外观** 属性的特定值配置单个 **Excel\\页眉** 或 **Excel\\页脚** 组件。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-718">Because you can configure several **Excel\\Header** or **Excel\\Footer** components for a single **Sheet** component, and you can generate different headers or footers for different type of pages in an Excel worksheet, you must configure a single **Excel\\Header** or **Excel\\Footer** component for a specific value of the **Header/footer appearance** property.</span></span> <span data-ttu-id="a3cfb-719">如果为 **页眉/页脚外观** 属性的特定值配置了多个 **Excel\\页眉** 或 **Excel\\页脚** 组件，则会发生验证错误，并且您会收到以下错误消息：“页眉/页脚（&lt;组件类型：页眉或页脚&gt;）不一致。”</span><span class="sxs-lookup"><span data-stu-id="a3cfb-719">If more than one **Excel\\Header** or **Excel\\Footer** component is configured for a specific value of the **Header/footer appearance** property, a validation error occurs, and you receive the following error message: "Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent."</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a3cfb-720">自动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-720">Automatic resolution</span></span>

<span data-ttu-id="a3cfb-721">没有用于自动修复此问题的选项。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-721">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a3cfb-722">手动解决</span><span class="sxs-lookup"><span data-stu-id="a3cfb-722">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a3cfb-723">选项 1</span><span class="sxs-lookup"><span data-stu-id="a3cfb-723">Option 1</span></span>

<span data-ttu-id="a3cfb-724">通过删除其中一个不一致的 **Excel\\页眉** 或 **Excel\\页脚** 组件来修改配置的格式。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-724">Modify the configured format by deleting one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a3cfb-725">选项 2</span><span class="sxs-lookup"><span data-stu-id="a3cfb-725">Option 2</span></span>

<span data-ttu-id="a3cfb-726">修改其中一个不一致的 **Excel\\页眉** 或 **Excel\\页脚** 组件的 **页眉/页脚外观** 属性值。</span><span class="sxs-lookup"><span data-stu-id="a3cfb-726">Modify the value of the **Header/footer appearance** property for one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3cfb-727">其他资源</span><span class="sxs-lookup"><span data-stu-id="a3cfb-727">Additional resources</span></span>

[<span data-ttu-id="a3cfb-728">ALLITEMS ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-728">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="a3cfb-729">ALLITEMSQUERY ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-729">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="a3cfb-730">INT64VALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-730">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="a3cfb-731">INTVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-731">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="a3cfb-732">FILTER ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-732">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="a3cfb-733">WHERE ER 函数</span><span class="sxs-lookup"><span data-stu-id="a3cfb-733">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="a3cfb-734">在 ER 模型映射中使用 JOIN 数据源从多个应用程序表中获取数据</span><span class="sxs-lookup"><span data-stu-id="a3cfb-734">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="a3cfb-735">跟踪电子申报格式的执行以解决性能问题</span><span class="sxs-lookup"><span data-stu-id="a3cfb-735">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="a3cfb-736">业务文档管理概览</span><span class="sxs-lookup"><span data-stu-id="a3cfb-736">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="a3cfb-737">禁止在生成的报告中使用 Word 内容控件</span><span class="sxs-lookup"><span data-stu-id="a3cfb-737">Suppress Word content controls in generated reports</span></span>](er-design-configuration-word-suppress-controls.md)

[<span data-ttu-id="a3cfb-738">管理单个模型根的多个派生映射</span><span class="sxs-lookup"><span data-stu-id="a3cfb-738">Manage several derived mappings for a single model root</span></span>](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
