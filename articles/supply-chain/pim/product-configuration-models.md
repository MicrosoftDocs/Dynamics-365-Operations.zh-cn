---
title: 产品配置模型概述
description: 本文定义与产品配置模型有关的术语和概念。 可通过产品配置模型构建可用于为单个产品配置大量产品变型的通用产品结构。
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26abf7afbbe3c6d0b4e13639d9f57f6e82fc9ad3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233791"
---
# <a name="product-configuration-models-overview"></a><span data-ttu-id="104aa-104">产品配置模型概述</span><span class="sxs-lookup"><span data-stu-id="104aa-104">Product configuration models overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="104aa-105">本文定义与产品配置模型有关的术语和概念。</span><span class="sxs-lookup"><span data-stu-id="104aa-105">This article defines terms and concepts that are relevant to product configuration models.</span></span> <span data-ttu-id="104aa-106">可通过产品配置模型构建可用于为单个产品配置大量产品变型的通用产品结构。</span><span class="sxs-lookup"><span data-stu-id="104aa-106">Product configuration models let you build a generic product structure that can be used to configure many product variants for a single product.</span></span>

<span data-ttu-id="104aa-107">创建产品配置模型是为了表示一般产品结构。</span><span class="sxs-lookup"><span data-stu-id="104aa-107">Product configuration models are created to represent a generic product structure.</span></span> <span data-ttu-id="104aa-108">设置产品配置模型后，您可以配置具有唯一物料清单 (BOM) 和唯一工艺路线的独特产品变型。</span><span class="sxs-lookup"><span data-stu-id="104aa-108">After you've set up a product configuration model, you can configure a distinct product variant that has a unique bill of materials (BOM) and a unique route.</span></span> <span data-ttu-id="104aa-109">产品模型配置使用陈述性约束和强制性计算来处理不同产品变型之间的关系和限制。</span><span class="sxs-lookup"><span data-stu-id="104aa-109">Product configuration models use both declarative constraints and imperative calculations to handle the relations and limitations between different product variants.</span></span> <span data-ttu-id="104aa-110">您可以配置销售订单、销售报价单、采购订单和生产订单上的物料。</span><span class="sxs-lookup"><span data-stu-id="104aa-110">You can configure items on sales orders, sales quotations, purchase orders, and production orders.</span></span> <span data-ttu-id="104aa-111">下表描述表基于约束的词语和概念。</span><span class="sxs-lookup"><span data-stu-id="104aa-111">The following table describes the table constraint–based terms and concepts.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="104aa-112">组件</span><span class="sxs-lookup"><span data-stu-id="104aa-112">Components</span></span></td>
<td><span data-ttu-id="104aa-113">组件是产品配置模型的主要构造块。</span><span class="sxs-lookup"><span data-stu-id="104aa-113">Components are the main building blocks of a product configuration model.</span></span> <span data-ttu-id="104aa-114">组件显示在<strong>基于约束的产品配置模型详细信息</strong>页上的一个树状结构中。</span><span class="sxs-lookup"><span data-stu-id="104aa-114">Components are displayed in a tree structure on the <strong>Constraint-based product configuration model details</strong> page.</span></span> <span data-ttu-id="104aa-115">组件可以包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="104aa-115">Components can contain the following elements:</span></span>
<ul>
<li><span data-ttu-id="104aa-116">属性</span><span class="sxs-lookup"><span data-stu-id="104aa-116">Attributes</span></span></li>
<li><span data-ttu-id="104aa-117">约束</span><span class="sxs-lookup"><span data-stu-id="104aa-117">Constraints</span></span></li>
<li><span data-ttu-id="104aa-118">计算</span><span class="sxs-lookup"><span data-stu-id="104aa-118">Calculations</span></span></li>
<li><span data-ttu-id="104aa-119">子组件</span><span class="sxs-lookup"><span data-stu-id="104aa-119">Subcomponents</span></span></li>
<li><span data-ttu-id="104aa-120">用户要求</span><span class="sxs-lookup"><span data-stu-id="104aa-120">User requirements</span></span></li>
<li><span data-ttu-id="104aa-121">物料清单行</span><span class="sxs-lookup"><span data-stu-id="104aa-121">BOM lines</span></span></li>
<li><span data-ttu-id="104aa-122">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="104aa-122">Route operations</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-123">属性</span><span class="sxs-lookup"><span data-stu-id="104aa-123">Attributes</span></span></td>
<td><span data-ttu-id="104aa-124">属性描述产品配置模型的所有功能。</span><span class="sxs-lookup"><span data-stu-id="104aa-124">Attributes describe all the features of the product configuration model.</span></span> <span data-ttu-id="104aa-125">您可以使用属性指定配置不同产品时可选择的功能。</span><span class="sxs-lookup"><span data-stu-id="104aa-125">You can use attributes to specify the features that can be selected when a distinct product is configured.</span></span> <span data-ttu-id="104aa-126">属性用于约束和条件中。</span><span class="sxs-lookup"><span data-stu-id="104aa-126">Attributes are used in constraints and conditions.</span></span> <span data-ttu-id="104aa-127">创建属性并将其添加到产品配置模型时，将引用相关属性类型。</span><span class="sxs-lookup"><span data-stu-id="104aa-127">When attributes are created and added to a product configuration model, the related attribute types are referenced.</span></span> <span data-ttu-id="104aa-128">可为属性设置默认值。</span><span class="sxs-lookup"><span data-stu-id="104aa-128">A default value can be set for an attribute.</span></span> <span data-ttu-id="104aa-129">配置产品配置模型时，配置用户界面 (UI) 中使用了默认值。</span><span class="sxs-lookup"><span data-stu-id="104aa-129">The default value is used in the configuration user interface (UI) when the product configuration model is configured.</span></span> <span data-ttu-id="104aa-130">您可以将属性指定为必需、只读或隐藏。</span><span class="sxs-lookup"><span data-stu-id="104aa-130">You can specify that an attribute is mandatory, read-only, or hidden.</span></span>
<ul>
<li><span data-ttu-id="104aa-131"><strong>必需</strong> – 配置产品时必须为属性设置一个值。</span><span class="sxs-lookup"><span data-stu-id="104aa-131"><strong>Mandatory</strong> – A value must be set for the attribute when the product is configured.</span></span></li>
<li><span data-ttu-id="104aa-132"><strong>只读</strong> – 属性值在配置会话期间显示，但是无法更改。</span><span class="sxs-lookup"><span data-stu-id="104aa-132"><strong>Read-only</strong> – The attribute value is displayed during a configuration session, but it can&#39;t be changed.</span></span></li>
<li><span data-ttu-id="104aa-133"><strong>隐藏</strong> – 属性值包括在约束和条件中，但是配置会话期间不显示。</span><span class="sxs-lookup"><span data-stu-id="104aa-133"><strong>Hidden</strong> – The attribute value is included in constraints and conditions, but isn&#39;t displayed during a configuration session.</span></span></li>
</ul>
<span data-ttu-id="104aa-134">您还可以为属性指定条件。</span><span class="sxs-lookup"><span data-stu-id="104aa-134">You can also specify a condition for attributes.</span></span> <span data-ttu-id="104aa-135">如果满足该条件，则必须为必需属性输入一个值。</span><span class="sxs-lookup"><span data-stu-id="104aa-135">If the condition is met, a value must be entered for the mandatory attribute.</span></span> <span data-ttu-id="104aa-136">条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。</span><span class="sxs-lookup"><span data-stu-id="104aa-136">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span> <span data-ttu-id="104aa-137">条件中引用的任何属性都是必需的。</span><span class="sxs-lookup"><span data-stu-id="104aa-137">Any attribute that is referenced in a condition becomes mandatory.</span></span> <span data-ttu-id="104aa-138">我们建议您在<strong>属性</strong>选项卡上将属性选为必需。这样可以更轻松地标识必需属性。</span><span class="sxs-lookup"><span data-stu-id="104aa-138">We recommend that you select attributes as mandatory on the <strong>Attributes</strong> tab. This can make it easier to identify mandatory attributes.</span></span> <span data-ttu-id="104aa-139">属性值是重用配置的重要环节。</span><span class="sxs-lookup"><span data-stu-id="104aa-139">Attribute values are an important part of reusing configurations.</span></span> <span data-ttu-id="104aa-140">系统使用属性值以确定是否存在匹配用户在配置会话期间所做选择的配置。</span><span class="sxs-lookup"><span data-stu-id="104aa-140">The system uses attribute values to determine whether a configuration exists that matches the selections that a user made during a configuration session.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-141">属性类型</span><span class="sxs-lookup"><span data-stu-id="104aa-141">Attribute types</span></span></td>
<td><span data-ttu-id="104aa-142">属性类型为用于产品配置模型的属性指定一组数据类型。</span><span class="sxs-lookup"><span data-stu-id="104aa-142">Attribute types specify the set of data types for attributes that are used in a product configuration model.</span></span> <span data-ttu-id="104aa-143">使用了以下属性类型：</span><span class="sxs-lookup"><span data-stu-id="104aa-143">The following attribute types are used:</span></span>
<ul>
<li><span data-ttu-id="104aa-144"><strong>整数</strong>，具有或不具有范围</span><span class="sxs-lookup"><span data-stu-id="104aa-144"><strong>Integer</strong> with or without a range</span></span></li>
<li><span data-ttu-id="104aa-145"><strong>小数</strong></span><span class="sxs-lookup"><span data-stu-id="104aa-145"><strong>Decimal</strong></span></span></li>
<li><span data-ttu-id="104aa-146"><strong>文本</strong>，具有或不具有固定列表</span><span class="sxs-lookup"><span data-stu-id="104aa-146"><strong>Text</strong> with or without a fixed list</span></span></li>
<li><span data-ttu-id="104aa-147"><strong>布尔值</strong></span><span class="sxs-lookup"><span data-stu-id="104aa-147"><strong>Boolean</strong></span></span></li>
</ul>
<span data-ttu-id="104aa-148">如果属性类型为<strong>布尔值</strong>、具有范围的<strong>整数</strong>或具有固定列表的<strong>文本</strong>，则在设置产品配置模型时，该组值会可用。</span><span class="sxs-lookup"><span data-stu-id="104aa-148">If the attribute type is <strong>Boolean</strong>, <strong>Integer</strong> with a range, or <strong>Text</strong> with a fixed list, the set of values is available when a product configuration model is set up.</span></span> <span data-ttu-id="104aa-149"><strong>注意：</strong>产品配置求解器仅识别下列属性类型：<strong>布尔值</strong>、具有固定列表的<strong>文本</strong>和具有范围的<strong>整数</strong>。</span><span class="sxs-lookup"><span data-stu-id="104aa-149"><strong>Note:</strong> The Product configuration solver recognizes only the following attribute types: <strong>Boolean</strong>, <strong>Text</strong> with a fixed list, and <strong>Integer</strong> with a range.</span></span> <span data-ttu-id="104aa-150">因此，只有这些属性类型可用于表达式约束和条件。</span><span class="sxs-lookup"><span data-stu-id="104aa-150">Therefore, only these attribute types can be used in expression constraints and conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-151">约束</span><span class="sxs-lookup"><span data-stu-id="104aa-151">Constraints</span></span></td>
<td><span data-ttu-id="104aa-152">约束描述产品配置模型的限制。</span><span class="sxs-lookup"><span data-stu-id="104aa-152">Constraints describe the restrictions of the product model configuration.</span></span> <span data-ttu-id="104aa-153">约束用于确保配置产品时仅选择了有效值。</span><span class="sxs-lookup"><span data-stu-id="104aa-153">Constraints are used to guarantee that only valid values are selected when a product is being configured.</span></span> <span data-ttu-id="104aa-154">约束可以是表达式约束，也可以是表约束：</span><span class="sxs-lookup"><span data-stu-id="104aa-154">Constraints can be either expression constraints or table constraints:</span></span>
<ul>
<li><span data-ttu-id="104aa-155">表达式约束仅用于与它们相关联的组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-155">Expression constraints can be used only for the component that they are tied to.</span></span> <span data-ttu-id="104aa-156">组件的表达式约束可以引用组件的子组件的属性。</span><span class="sxs-lookup"><span data-stu-id="104aa-156">The expression constraints for a component can reference attributes of the component&#39;s subcomponents.</span></span> <span data-ttu-id="104aa-157">产品配置求解器用于求解约束，并且编写约束时您必须使用求解器语法。</span><span class="sxs-lookup"><span data-stu-id="104aa-157">The Product configuration solver is used to solve the constraints, and you must use the solver syntax when you write the constraints.</span></span> <span data-ttu-id="104aa-158">有关详细信息，请参阅有关表达式约束和表约束的主题链接。</span><span class="sxs-lookup"><span data-stu-id="104aa-158">For more information, see the topic link about expression constraints and table constraints.</span></span></li>
<li><span data-ttu-id="104aa-159">必须定义表约束，然后才能将其应用到产品配置模型中的组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-159">Table constraints must be defined before they can be applied to a component in a product configuration model.</span></span> <span data-ttu-id="104aa-160">表约束可以是用户定义的，也可以是系统定义的。</span><span class="sxs-lookup"><span data-stu-id="104aa-160">Table constraints can be either user-defined or system-defined.</span></span> <span data-ttu-id="104aa-161">用户定义的表约束是一种可用于描述属性类型所定义的一组属性值组合的矩阵。</span><span class="sxs-lookup"><span data-stu-id="104aa-161">A user-defined table constraint is a type of matrix that can be used to describe the set of combinations for the attribute values that are defined by attribute types.</span></span> <span data-ttu-id="104aa-162">例如，如果生产扬声器，则用户定义的表约束的矩阵可能包含针对扬声器表面处理和格栅的列。</span><span class="sxs-lookup"><span data-stu-id="104aa-162">For example, if speakers are produced, the matrix for a user-defined table constraint might have columns for the speaker finish and grill.</span></span></li>
</ul><span data-ttu-id="104aa-163">
<strong>示例</strong>扬声器有四种表面处理：黑色、橡木、红木和白色。</span><span class="sxs-lookup"><span data-stu-id="104aa-163">
<strong>Example</strong> Speakers are available in four finishes: Black, Oak, Rosewood, and White.</span></span> <span data-ttu-id="104aa-164">扬声器可以具有三个前格栅之一：黑色、金属或白色。</span><span class="sxs-lookup"><span data-stu-id="104aa-164">The speakers can have one of three front grills: Black, Metal, or White.</span></span> <span data-ttu-id="104aa-165">黑色表面处理对所有格栅可用，但是其他表面处理仅限于特定格栅。</span><span class="sxs-lookup"><span data-stu-id="104aa-165">The Black finish is available for all grills, but the other finishes are limited to specific grills.</span></span> <span data-ttu-id="104aa-166">下表显示在<strong>编辑表约束</strong>页上的<strong>允许的组合</strong>选项卡中显示的信息的示例。</span><span class="sxs-lookup"><span data-stu-id="104aa-166">The following table shows an example of the information that is displayed on the <strong>Allowed combinations</strong> tab on the <strong>Edit table constraint</strong> page.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="104aa-167">机柜表面处理</span><span class="sxs-lookup"><span data-stu-id="104aa-167">Cabinet finish</span></span></th>
<th><span data-ttu-id="104aa-168">前格栅</span><span class="sxs-lookup"><span data-stu-id="104aa-168">Front grill</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="104aa-169">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-169">Black</span></span></td>
<td><span data-ttu-id="104aa-170">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-170">Black</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-171">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-171">Black</span></span></td>
<td><span data-ttu-id="104aa-172">金属</span><span class="sxs-lookup"><span data-stu-id="104aa-172">Metal</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-173">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-173">Black</span></span></td>
<td><span data-ttu-id="104aa-174">白色</span><span class="sxs-lookup"><span data-stu-id="104aa-174">White</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-175">橡木</span><span class="sxs-lookup"><span data-stu-id="104aa-175">Oak</span></span></td>
<td><span data-ttu-id="104aa-176">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-176">Black</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-177">红木</span><span class="sxs-lookup"><span data-stu-id="104aa-177">Rosewood</span></span></td>
<td><span data-ttu-id="104aa-178">白色</span><span class="sxs-lookup"><span data-stu-id="104aa-178">White</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-179">白色</span><span class="sxs-lookup"><span data-stu-id="104aa-179">White</span></span></td>
<td><span data-ttu-id="104aa-180">黑</span><span class="sxs-lookup"><span data-stu-id="104aa-180">Black</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-181">白色</span><span class="sxs-lookup"><span data-stu-id="104aa-181">White</span></span></td>
<td><span data-ttu-id="104aa-182">白色</span><span class="sxs-lookup"><span data-stu-id="104aa-182">White</span></span></td>
</tr>
</tbody>
</table>
<span data-ttu-id="104aa-183">系统定义的表约束表示 Supply Chain Management 表中属性类型与字段之间的映射。</span><span class="sxs-lookup"><span data-stu-id="104aa-183">A system-defined table constraint represents a mapping between an attribute type and a field in a Supply Chain Management table.</span></span> <span data-ttu-id="104aa-184">系统定义的表约束将属性类型与字段动态链接。</span><span class="sxs-lookup"><span data-stu-id="104aa-184">A system-defined table constraint dynamically links the attribute type to the field.</span></span> <span data-ttu-id="104aa-185">链接能让产品配置模型中的属性反映 Supply Chain Management 表中的字段的数据。</span><span class="sxs-lookup"><span data-stu-id="104aa-185">The link enables the attribute in a product configuration model to reflect the data of the field in the Supply Chain Management table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-186">计算</span><span class="sxs-lookup"><span data-stu-id="104aa-186">Calculations</span></span></td>
<td><span data-ttu-id="104aa-187">计算表示对约束的补充。</span><span class="sxs-lookup"><span data-stu-id="104aa-187">Calculations represent a supplement to constraints.</span></span> <span data-ttu-id="104aa-188">您可以使用计算对<strong>小数</strong>和<strong>整数</strong>类型的属性执行算术运算，或执行涉及具有固定列表的<strong>文本</strong>和<strong>布尔值</strong>类型的属性的逻辑运算。</span><span class="sxs-lookup"><span data-stu-id="104aa-188">You can use a calculation to perform arithmetic operations on attributes of the <strong>Decimal</strong> and <strong>Integer</strong> types, or logical operations that involve attributes of the <strong>Text</strong> with a fixed list and <strong>Boolean</strong> types.</span></span> <span data-ttu-id="104aa-189">计算具有一个目标属性，可用于保留计算表达式的结果。</span><span class="sxs-lookup"><span data-stu-id="104aa-189">A calculation has a target attribute that will hold the result of the calculation expression.</span></span> <span data-ttu-id="104aa-190">计算表达式是使用表达式编辑器构建的。</span><span class="sxs-lookup"><span data-stu-id="104aa-190">The calculation expression is built by using the expression editor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-191">子组件</span><span class="sxs-lookup"><span data-stu-id="104aa-191">Subcomponents</span></span></td>
<td><span data-ttu-id="104aa-192">子组件反映产品配置模型的树状结构。</span><span class="sxs-lookup"><span data-stu-id="104aa-192">Subcomponents reflect the tree structure of the product configuration model.</span></span> <span data-ttu-id="104aa-193">您可以使用子组件构造产品配置模型的结构。</span><span class="sxs-lookup"><span data-stu-id="104aa-193">You can use subcomponents to build the structure of the product configuration model.</span></span> <span data-ttu-id="104aa-194">子组件将引用现有组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-194">Subcomponents reference existing components.</span></span> <span data-ttu-id="104aa-195">因此，子组件将促进在多个产品配置模型中重复使用组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-195">Therefore, subcomponents encourage the reuse of components in multiple product configuration models.</span></span> <span data-ttu-id="104aa-196">在子组件的<strong>物料清单行详细信息</strong>页上，您可以为子组件选择不同的值。</span><span class="sxs-lookup"><span data-stu-id="104aa-196">On the <strong>BOM line details</strong> page for a subcomponent, you can select a distinct value for the subcomponent.</span></span> <span data-ttu-id="104aa-197">或者，您可以选择设置产品配置模型时为其选择了值的属性。</span><span class="sxs-lookup"><span data-stu-id="104aa-197">Alternatively, you can select an attribute that the value is selected for when the product configuration model is set up.</span></span> <span data-ttu-id="104aa-198">若要将产品包括为组件或子组件，您必须在创建产品时在<strong>创建产品</strong>页上指定以下内容：</span><span class="sxs-lookup"><span data-stu-id="104aa-198">To include a product as a component or subcomponent, you must specify the following information on the <strong>Create product</strong> page when you create the product:</span></span>
<ul>
<li><span data-ttu-id="104aa-199">在<strong>产品类型</strong>字段中，选择<strong>物料</strong>。</span><span class="sxs-lookup"><span data-stu-id="104aa-199">In the <strong>Product type</strong> field, select <strong>Item</strong>.</span></span></li>
<li><span data-ttu-id="104aa-200">在<strong>产品子类型</strong>字段中，选择<strong>基础产品</strong>。</span><span class="sxs-lookup"><span data-stu-id="104aa-200">In the <strong>Product subtype</strong> field, select <strong>Product master</strong>.</span></span></li>
<li><span data-ttu-id="104aa-201">在<strong>配置技术</strong>字段中，选择<strong>基于约束的配置</strong>。</span><span class="sxs-lookup"><span data-stu-id="104aa-201">In the <strong>Configuration technology</strong> field, select <strong>Constraint-based configuration</strong>.</span></span></li>
</ul>
<span data-ttu-id="104aa-202">您可以查看已发布产品是否可用作<strong>已发布产品详细信息</strong>页的<strong>常规</strong>选项卡上的组件或子组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-202">You can view whether a released product can be used as a component or subcomponent on the <strong>General</strong> tab of the <strong>Released product details</strong> page.</span></span> <span data-ttu-id="104aa-203">如果<strong>基于约束的配置</strong>在<strong>配置技术</strong>字段中被选定，则产品可以用作组件或子组件。</span><span class="sxs-lookup"><span data-stu-id="104aa-203">If <strong>Constraint-based configuration</strong> is selected in the <strong>Configuration technology</strong> field, the product can be used as a component or subcomponent.</span></span> <span data-ttu-id="104aa-204">您可以隐藏子组件，以便配置会话期间不会向用户显示。</span><span class="sxs-lookup"><span data-stu-id="104aa-204">You can hide subcomponents so that they aren&#39;t displayed to the user during a configuration session.</span></span> <span data-ttu-id="104aa-205">与子组件关联的属性、子组件和用户要求也是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="104aa-205">Attributes, subcomponents, and user requirements that are related to the subcomponent are also hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-206">用户要求</span><span class="sxs-lookup"><span data-stu-id="104aa-206">User requirements</span></span></td>
<td><span data-ttu-id="104aa-207">用户要求表示用户要求与特定组件和属性之间的抽象。</span><span class="sxs-lookup"><span data-stu-id="104aa-207">User requirements represent an abstraction between user requirements and specific components and attributes.</span></span> <span data-ttu-id="104aa-208">您不能将用户要求映射到物料。</span><span class="sxs-lookup"><span data-stu-id="104aa-208">You can&#39;t map a user requirement to an item.</span></span> <span data-ttu-id="104aa-209">例如，客户要购买家庭影院系统。</span><span class="sxs-lookup"><span data-stu-id="104aa-209">For example, a customer is shopping for a home theater system.</span></span> <span data-ttu-id="104aa-210">销售代表可以询问客户计划将系统安装所在的房间的大小，以便确定需要多少瓦特。</span><span class="sxs-lookup"><span data-stu-id="104aa-210">The sales representative might ask about the size of the room where the customer plans to install the system, to determine how many watts are required.</span></span> <span data-ttu-id="104aa-211">在此示例中，房间大小可以是用户要求，它可以帮助确定特定组件的合适属性值。</span><span class="sxs-lookup"><span data-stu-id="104aa-211">In this example, the room size can be a user requirement that helps determine the appropriate attribute value for a specific component.</span></span> <span data-ttu-id="104aa-212">您可以隐藏用户要求，以便配置会话期间不会向用户显示。</span><span class="sxs-lookup"><span data-stu-id="104aa-212">You can hide user requirements so that they aren&#39;t displayed to the user during a configuration session.</span></span> <span data-ttu-id="104aa-213">与用户要求关联的属性、子组件和用户要求也是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="104aa-213">Attributes, subcomponents, and user requirements that are related to the user requirement are also hidden.</span></span> <span data-ttu-id="104aa-214">您可以编写条件。以便控制用户要求是否可以处于隐藏状态。</span><span class="sxs-lookup"><span data-stu-id="104aa-214">You can write a condition to control whether a user requirement can be hidden.</span></span> <span data-ttu-id="104aa-215">您必须使用优化建模语言 (OML) 语法编写条件。</span><span class="sxs-lookup"><span data-stu-id="104aa-215">You must write the condition by using Optimization Modeling Language (OML) syntax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="104aa-216">物料清单行</span><span class="sxs-lookup"><span data-stu-id="104aa-216">BOM lines</span></span></td>
<td><span data-ttu-id="104aa-217">物料清单行表示产品配置模型中组件的各个物料。</span><span class="sxs-lookup"><span data-stu-id="104aa-217">BOM lines represent the individual materials of the components in the product configuration model.</span></span> <span data-ttu-id="104aa-218">在<strong>物料清单行详细信息</strong>页上，所有物料都可供选择。</span><span class="sxs-lookup"><span data-stu-id="104aa-218">On the <strong>BOM line details</strong> page, all items are available for selection.</span></span> <span data-ttu-id="104aa-219">可以将条件添加到物料清单行，以便根据设置产品配置模型时的用户选择，为不同产品变型选择的物料清单行可以有所不同。</span><span class="sxs-lookup"><span data-stu-id="104aa-219">A condition can be added to the BOM line, so that the BOM lines that are selected for a distinct product variant can vary, based on the user&#39;s selection when the product configuration model is set up.</span></span> <span data-ttu-id="104aa-220">条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。</span><span class="sxs-lookup"><span data-stu-id="104aa-220">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span> <span data-ttu-id="104aa-221">在<strong>物料清单行详细信息</strong>页上，您可以选择一个不同的值。</span><span class="sxs-lookup"><span data-stu-id="104aa-221">On the <strong>BOM line details</strong> page, you can select a distinct value.</span></span> <span data-ttu-id="104aa-222">或者，您可以映射到设置产品配置模型时为其选择了值的属性。</span><span class="sxs-lookup"><span data-stu-id="104aa-222">Alternatively, you can map to an attribute that the value is selected for when the product configuration model is set up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="104aa-223">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="104aa-223">Route operations</span></span></td>
<td><span data-ttu-id="104aa-224">在<strong>工艺路线工序详细信息</strong>页上，您可以选择一个不同的值。</span><span class="sxs-lookup"><span data-stu-id="104aa-224">On the <strong>Route operation details</strong> page, you can select a distinct value.</span></span> <span data-ttu-id="104aa-225">或者，您可以映射到设置产品配置模型时为其选择了值的属性。</span><span class="sxs-lookup"><span data-stu-id="104aa-225">Alternatively, you can map to an attribute that the value is selected for when the product configuration model is set up.</span></span> <span data-ttu-id="104aa-226">已编写条件，如表达式约束。</span><span class="sxs-lookup"><span data-stu-id="104aa-226">Conditions are written like expression constraints.</span></span> <span data-ttu-id="104aa-227">条件是必须要满足的表达式，以便将属性、物料清单行和工艺路线工序包括在产品配置模型中。</span><span class="sxs-lookup"><span data-stu-id="104aa-227">Conditions are expressions that must be met for attributes, BOM lines, and route operations to be included in a product configuration model.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]