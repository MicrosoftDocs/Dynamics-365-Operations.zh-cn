---
title: 产品配置模型中的表达式约束和表约束
description: 本主题介绍的是表达式约束和表约束的使用。 约束控制的对象是您在配置销售订单、销售报价单、采购订单或生产订单的产品时您可以选择的属性值。 您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d85d10113e7cc4e95a25efe7fee6d1f23990694
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208452"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="6cc4a-105">产品配置模型中的表达式约束和表约束</span><span class="sxs-lookup"><span data-stu-id="6cc4a-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cc4a-106">本主题介绍的是表达式约束和表约束的使用。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="6cc4a-107">约束控制的对象是您在配置销售订单、销售报价单、采购订单或生产订单的产品时您可以选择的属性值。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="6cc4a-108">您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="6cc4a-109">约束用于控制您在配置销售订单、销售报价单、采购订单或生产订单的产品时可以选择的属性值。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="6cc4a-110">您可以根据自己喜欢的构建约束方式来选择使用表达式约束或表约束。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="6cc4a-111">什么是表达式约束？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-111">What are expression constraints?</span></span>
<span data-ttu-id="6cc4a-112">表达式约束的特性是使用算术和布尔运算符和函数的表达式。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="6cc4a-113">表达式约束是为产品配置模型中的特定组件而写的。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="6cc4a-114">它不能为其他组件重用或共享。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="6cc4a-115">但是，组件的表达式约束可以引用组件的子组件的特性。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="6cc4a-116">什么是表约束？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-116">What are table constraints?</span></span>
<span data-ttu-id="6cc4a-117">约束表列出了在配置产品时允许属性值的组合。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="6cc4a-118">表约束定义可以被广泛使用。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="6cc4a-119">当您为产品配置模型中的组件创建一个表约束时，您要选择一个表约束定义。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="6cc4a-120">若要创建合理的组合，您要给组件添加特定类型的属性。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="6cc4a-121">每个属性类型具有一个特定值。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="6cc4a-122">表约束示例</span><span class="sxs-lookup"><span data-stu-id="6cc4a-122">Example of a table constraint</span></span>

<span data-ttu-id="6cc4a-123">此示例显示如何如何将扬声器的配置限制到特定的机柜表面处理和格栅。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="6cc4a-124">第一个表显示通常可用于配置的机柜表面处理和格栅。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="6cc4a-125">这些值是针对**机柜表面处理**和**格栅**属性类型定义的。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="6cc4a-126">属性类型</span><span class="sxs-lookup"><span data-stu-id="6cc4a-126">Attribute type</span></span> | <span data-ttu-id="6cc4a-127">值</span><span class="sxs-lookup"><span data-stu-id="6cc4a-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="6cc4a-128">机柜表面处理</span><span class="sxs-lookup"><span data-stu-id="6cc4a-128">Cabinet finish</span></span> | <span data-ttu-id="6cc4a-129">黑色、橡木、红木、白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="6cc4a-130">前格栅</span><span class="sxs-lookup"><span data-stu-id="6cc4a-130">Front grill</span></span>    | <span data-ttu-id="6cc4a-131">黑色、金属、白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-131">Black, Metal, White</span></span>         |

<span data-ttu-id="6cc4a-132">下一个表显示由**颜色和表面处理**表约束定义的组合。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="6cc4a-133">通过使用此表约束，您可以配置具有橡木表面处理和黑色格栅的扬声器、具有红木表面处理和白色格栅的扬声器，等等。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="6cc4a-134">完成</span><span class="sxs-lookup"><span data-stu-id="6cc4a-134">Finish</span></span>         | <span data-ttu-id="6cc4a-135">格栅</span><span class="sxs-lookup"><span data-stu-id="6cc4a-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="6cc4a-136">橡木</span><span class="sxs-lookup"><span data-stu-id="6cc4a-136">Oak</span></span>            | <span data-ttu-id="6cc4a-137">黑色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-137">Black</span></span>                       |
| <span data-ttu-id="6cc4a-138">红木</span><span class="sxs-lookup"><span data-stu-id="6cc4a-138">Rosewood</span></span>       | <span data-ttu-id="6cc4a-139">白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-139">White</span></span>                       |
| <span data-ttu-id="6cc4a-140">白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-140">White</span></span>          | <span data-ttu-id="6cc4a-141">黑色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-141">Black</span></span>                       |
| <span data-ttu-id="6cc4a-142">白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-142">White</span></span>          | <span data-ttu-id="6cc4a-143">白色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-143">White</span></span>                       |
| <span data-ttu-id="6cc4a-144">黑色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-144">Black</span></span>          | <span data-ttu-id="6cc4a-145">黑色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-145">Black</span></span>                       |
| <span data-ttu-id="6cc4a-146">黑</span><span class="sxs-lookup"><span data-stu-id="6cc4a-146">Black</span></span>          | <span data-ttu-id="6cc4a-147">金属</span><span class="sxs-lookup"><span data-stu-id="6cc4a-147">Metal</span></span>                       | 

<span data-ttu-id="6cc4a-148">您可以创建系统定义的表约束和用户定义的表约束</span><span class="sxs-lookup"><span data-stu-id="6cc4a-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="6cc4a-149">有关详细信息，请参阅[系统定义的和用户定义的表约束](system-defined-user-defined-table-constraints.md)。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="6cc4a-150">应使用何种语法来编写约束？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="6cc4a-151">编写约束时，必须使用优化建模语言 (OML) 语法。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="6cc4a-152">此系统使用 Microsoft Solver Foundation 约束求解器来求解这些约束。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="6cc4a-153">我应该使用表约束还是表达式约束？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="6cc4a-154">您可以使用表达式约束或表约束，具体取决于您喜欢生成约束的方式。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="6cc4a-155">您建立的表约束为一个矩阵表，而表达式约束则是单个报表。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="6cc4a-156">在您配置产品时，可以随意使用约束条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="6cc4a-157">以下示例显示两种方法有何不同。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="6cc4a-158">当您使用以下设置约束配置产品时，这些组合是允许的：</span><span class="sxs-lookup"><span data-stu-id="6cc4a-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="6cc4a-159">颜色为黑色、大小为 30 或 50 的产品</span><span class="sxs-lookup"><span data-stu-id="6cc4a-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="6cc4a-160">颜色为红色、大小为 20 的产品</span><span class="sxs-lookup"><span data-stu-id="6cc4a-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="6cc4a-161">表约束设置</span><span class="sxs-lookup"><span data-stu-id="6cc4a-161">Table constraint setup</span></span>

| <span data-ttu-id="6cc4a-162">颜色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-162">Color</span></span> | <span data-ttu-id="6cc4a-163">大小</span><span class="sxs-lookup"><span data-stu-id="6cc4a-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="6cc4a-164">黑</span><span class="sxs-lookup"><span data-stu-id="6cc4a-164">Black</span></span> | <span data-ttu-id="6cc4a-165">30</span><span class="sxs-lookup"><span data-stu-id="6cc4a-165">30</span></span>   |
| <span data-ttu-id="6cc4a-166">黑</span><span class="sxs-lookup"><span data-stu-id="6cc4a-166">Black</span></span> | <span data-ttu-id="6cc4a-167">50</span><span class="sxs-lookup"><span data-stu-id="6cc4a-167">50</span></span>   |
| <span data-ttu-id="6cc4a-168">红色</span><span class="sxs-lookup"><span data-stu-id="6cc4a-168">Red</span></span>   | <span data-ttu-id="6cc4a-169">20</span><span class="sxs-lookup"><span data-stu-id="6cc4a-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="6cc4a-170">表达式约束设置</span><span class="sxs-lookup"><span data-stu-id="6cc4a-170">Expression constraint setup</span></span>

<span data-ttu-id="6cc4a-171">(颜色 == “黑色” & (尺寸 == “30” | 尺寸 == “50”)) | (颜色 ==“红色” & 大小 = “20” ）</span><span class="sxs-lookup"><span data-stu-id="6cc4a-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="6cc4a-172">当我编写表达式约束时，我应该使用运算符还是中缀表示法？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="6cc4a-173">您既可以使用运算符又可以使用中缀表示法来编写表达式约束。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="6cc4a-174">对于**Min**、**Max**和**Abs**运算符，您不能使用中缀表示法。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="6cc4a-175">这些运算符作为标准运算符包括在大多数编程语言中。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="6cc4a-176">在编写表达式约束时，我可以使用哪些运算符和中缀表示法？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="6cc4a-177">下表列出的是您在产品配置模型中为组件编写表达式约束时，可以使用的运算符和中缀表示法。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="6cc4a-178">第一个表中的示例显示如何使用中缀表示法或运算符编写表达式。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cc4a-179">操作员</span><span class="sxs-lookup"><span data-stu-id="6cc4a-179">Operator</span></span></th>
<th><span data-ttu-id="6cc4a-180">描述</span><span class="sxs-lookup"><span data-stu-id="6cc4a-180">Description</span></span></th>
<th><span data-ttu-id="6cc4a-181">语法</span><span class="sxs-lookup"><span data-stu-id="6cc4a-181">Syntax</span></span></th>
<th><span data-ttu-id="6cc4a-182">示例</span><span class="sxs-lookup"><span data-stu-id="6cc4a-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6cc4a-183">提示</span><span class="sxs-lookup"><span data-stu-id="6cc4a-183">Implies</span></span></td>
<td><span data-ttu-id="6cc4a-184">如果第一个条件为 false，则为 true；第二个条件为 true 或两者都为 true。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="6cc4a-185">提示[a, b]，中缀：a -: b</span><span class="sxs-lookup"><span data-stu-id="6cc4a-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-186"><strong>运算符：</strong>Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="6cc4a-187"><strong>中缀表示法：</strong>x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="6cc4a-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cc4a-188">并</span><span class="sxs-lookup"><span data-stu-id="6cc4a-188">And</span></span></td>
<td><span data-ttu-id="6cc4a-189">只有所有条件为 true，则为 true。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="6cc4a-190">如果条件数为 0 （零），则产生 <strong>True</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-192"><strong>运算符：</strong>And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="6cc4a-193"><strong>中缀表示法：</strong>x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="6cc4a-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cc4a-194">或</span><span class="sxs-lookup"><span data-stu-id="6cc4a-194">Or</span></span></td>
<td><span data-ttu-id="6cc4a-195">如有条件为 true，则为 true。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-195">This is true if any condition is true.</span></span> <span data-ttu-id="6cc4a-196">如果条件数为 0 (零)，则产生 <strong>False</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-198"><strong>运算符：</strong>Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="6cc4a-199"><strong>中缀表示法：</strong>x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="6cc4a-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cc4a-200">加</span><span class="sxs-lookup"><span data-stu-id="6cc4a-200">Plus</span></span></td>
<td><span data-ttu-id="6cc4a-201">这将合计其条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-201">This sums its conditions.</span></span> <span data-ttu-id="6cc4a-202">如果条件数为 0 （零），则产生 <strong>0</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-204"><strong>运算符：</strong>Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="6cc4a-205"><strong>中缀表示法：</strong>x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cc4a-206">减</span><span class="sxs-lookup"><span data-stu-id="6cc4a-206">Minus</span></span></td>
<td><span data-ttu-id="6cc4a-207">这就否定了此参数。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-207">This negates its argument.</span></span> <span data-ttu-id="6cc4a-208">它必须只有一个条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6cc4a-209">减[expr]，中缀：-expr</span><span class="sxs-lookup"><span data-stu-id="6cc4a-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-210"><strong>运算符：</strong>Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="6cc4a-211"><strong>中缀表示法：</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cc4a-212">绝对值</span><span class="sxs-lookup"><span data-stu-id="6cc4a-212">Abs</span></span></td>
<td><span data-ttu-id="6cc4a-213">取其条件的绝对值。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="6cc4a-214">它必须只有一个条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6cc4a-215">绝对值[expr]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="6cc4a-216"><strong>运算符：</strong>Abs[x]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cc4a-217">时间</span><span class="sxs-lookup"><span data-stu-id="6cc4a-217">Times</span></span></td>
<td><span data-ttu-id="6cc4a-218">取其条件的产物。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-218">This takes the product of its conditions.</span></span> <span data-ttu-id="6cc4a-219">如果条件数为 0 （零），则产生 <strong>1</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-221"><strong>运算符：</strong>Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="6cc4a-222"><strong>中缀表示法：</strong>x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cc4a-223">能力</span><span class="sxs-lookup"><span data-stu-id="6cc4a-223">Power</span></span></td>
<td><span data-ttu-id="6cc4a-224">取指数。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-224">This takes an exponential.</span></span> <span data-ttu-id="6cc4a-225">它从右到左求幂。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="6cc4a-226">（换言之，它是权限相关。）因此，<strong>Power[a, b, c]</strong> 等于 <strong>Power[a, Power[b, c]]</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="6cc4a-227">只有指数为正常数时才可以使用 <strong>Power</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="6cc4a-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-229"><strong>运算符：</strong>Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="6cc4a-230"><strong>中缀表示法：</strong>x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cc4a-231">最大值</span><span class="sxs-lookup"><span data-stu-id="6cc4a-231">Max</span></span></td>
<td><span data-ttu-id="6cc4a-232">生成最大条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-232">This produces the largest condition.</span></span> <span data-ttu-id="6cc4a-233">如果条件数为 0 (零)，则生成结果为<strong>无穷大</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-234">最大值[args]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-234">Max[args]</span></span></td>
<td><span data-ttu-id="6cc4a-235"><strong>运算符：</strong>Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cc4a-236">最小值</span><span class="sxs-lookup"><span data-stu-id="6cc4a-236">Min</span></span></td>
<td><span data-ttu-id="6cc4a-237">生成最小条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-237">This produces the smallest condition.</span></span> <span data-ttu-id="6cc4a-238">如果条件数为 0 (零)，则生成结果为<strong>无穷大</strong>。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="6cc4a-239">最小值[args]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-239">Min[args]</span></span></td>
<td><span data-ttu-id="6cc4a-240"><strong>运算符：</strong>Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cc4a-241">不</span><span class="sxs-lookup"><span data-stu-id="6cc4a-241">Not</span></span></td>
<td><span data-ttu-id="6cc4a-242">生成其条件的相反逻辑。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="6cc4a-243">它必须只有一个条件。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6cc4a-244">非[expr]，中缀：!expr</span><span class="sxs-lookup"><span data-stu-id="6cc4a-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="6cc4a-245"><strong>运算符：</strong>Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="6cc4a-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="6cc4a-246"><strong>中缀表示法：</strong>!x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="6cc4a-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6cc4a-247">下表示例显示的是如何编写中缀表示法。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="6cc4a-248">中缀表示法</span><span class="sxs-lookup"><span data-stu-id="6cc4a-248">Infix notation</span></span>   |                                          <span data-ttu-id="6cc4a-249">说明</span><span class="sxs-lookup"><span data-stu-id="6cc4a-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="6cc4a-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-250">x + y + z</span></span>     |                                           <span data-ttu-id="6cc4a-251">增加额</span><span class="sxs-lookup"><span data-stu-id="6cc4a-251">Addition</span></span>                                            |
|    <span data-ttu-id="6cc4a-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="6cc4a-253">乘</span><span class="sxs-lookup"><span data-stu-id="6cc4a-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="6cc4a-254">x - y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-254">x - y</span></span>       | <span data-ttu-id="6cc4a-255">二进制减法的转换方式与第二个数为负的二进制加法相同。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="6cc4a-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="6cc4a-257">具有右关联的求幂</span><span class="sxs-lookup"><span data-stu-id="6cc4a-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="6cc4a-258">!x</span><span class="sxs-lookup"><span data-stu-id="6cc4a-258">!x</span></span>         |                                          <span data-ttu-id="6cc4a-259">布尔值“非”。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="6cc4a-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-260">x -: y</span></span>       |                                      <span data-ttu-id="6cc4a-261">布尔值影响</span><span class="sxs-lookup"><span data-stu-id="6cc4a-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="6cc4a-262">x</span><span class="sxs-lookup"><span data-stu-id="6cc4a-262">x</span></span>         |                                               <span data-ttu-id="6cc4a-263">y</span><span class="sxs-lookup"><span data-stu-id="6cc4a-263">y</span></span>                                               |
|     <span data-ttu-id="6cc4a-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-264">x & y & z</span></span>     |                                          <span data-ttu-id="6cc4a-265">布尔值“与”</span><span class="sxs-lookup"><span data-stu-id="6cc4a-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="6cc4a-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-266">x == y == z</span></span>    |                                           <span data-ttu-id="6cc4a-267">等式</span><span class="sxs-lookup"><span data-stu-id="6cc4a-267">Equality</span></span>                                            |
|    <span data-ttu-id="6cc4a-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-268">x != y != z</span></span>    |                                           <span data-ttu-id="6cc4a-269">明确的</span><span class="sxs-lookup"><span data-stu-id="6cc4a-269">Distinct</span></span>                                            |
|  <span data-ttu-id="6cc4a-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="6cc4a-271">小于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-271">Less than</span></span>                                           |
|  <span data-ttu-id="6cc4a-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="6cc4a-273">大于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-273">Greater than</span></span>                                          |
| <span data-ttu-id="6cc4a-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="6cc4a-275">小于等于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="6cc4a-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="6cc4a-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="6cc4a-277">大于等于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="6cc4a-278">(x)</span><span class="sxs-lookup"><span data-stu-id="6cc4a-278">(x)</span></span>        |                           <span data-ttu-id="6cc4a-279">括号覆盖默认优先级顺序。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="6cc4a-280">为什么我的表达式约束验证为错误？</span><span class="sxs-lookup"><span data-stu-id="6cc4a-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="6cc4a-281">您不能使用预留的关键字作为产品配置模型中的属性、组件或子组件的求解器名称。</span><span class="sxs-lookup"><span data-stu-id="6cc4a-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="6cc4a-282">下面是不能使用的预留关键字的列表：</span><span class="sxs-lookup"><span data-stu-id="6cc4a-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="6cc4a-283">上限</span><span class="sxs-lookup"><span data-stu-id="6cc4a-283">Ceiling</span></span>
-   <span data-ttu-id="6cc4a-284">分项指标</span><span class="sxs-lookup"><span data-stu-id="6cc4a-284">Element</span></span>
-   <span data-ttu-id="6cc4a-285">相等</span><span class="sxs-lookup"><span data-stu-id="6cc4a-285">Equal</span></span>
-   <span data-ttu-id="6cc4a-286">场地</span><span class="sxs-lookup"><span data-stu-id="6cc4a-286">Floor</span></span>
-   <span data-ttu-id="6cc4a-287">如果</span><span class="sxs-lookup"><span data-stu-id="6cc4a-287">If</span></span>
-   <span data-ttu-id="6cc4a-288">小于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-288">Less</span></span>
-   <span data-ttu-id="6cc4a-289">大于</span><span class="sxs-lookup"><span data-stu-id="6cc4a-289">Greater</span></span>
-   <span data-ttu-id="6cc4a-290">提示</span><span class="sxs-lookup"><span data-stu-id="6cc4a-290">Implies</span></span>
-   <span data-ttu-id="6cc4a-291">日志</span><span class="sxs-lookup"><span data-stu-id="6cc4a-291">Log</span></span>
-   <span data-ttu-id="6cc4a-292">最大</span><span class="sxs-lookup"><span data-stu-id="6cc4a-292">Max</span></span>
-   <span data-ttu-id="6cc4a-293">分钟</span><span class="sxs-lookup"><span data-stu-id="6cc4a-293">Min</span></span>
-   <span data-ttu-id="6cc4a-294">减</span><span class="sxs-lookup"><span data-stu-id="6cc4a-294">Minus</span></span>
-   <span data-ttu-id="6cc4a-295">加</span><span class="sxs-lookup"><span data-stu-id="6cc4a-295">Plus</span></span>
-   <span data-ttu-id="6cc4a-296">功率</span><span class="sxs-lookup"><span data-stu-id="6cc4a-296">Power</span></span>
-   <span data-ttu-id="6cc4a-297">时间</span><span class="sxs-lookup"><span data-stu-id="6cc4a-297">Times</span></span>
-   <span data-ttu-id="6cc4a-298">时隙</span><span class="sxs-lookup"><span data-stu-id="6cc4a-298">Slot</span></span>
-   <span data-ttu-id="6cc4a-299">型号</span><span class="sxs-lookup"><span data-stu-id="6cc4a-299">Model</span></span>
-   <span data-ttu-id="6cc4a-300">决策</span><span class="sxs-lookup"><span data-stu-id="6cc4a-300">Decision</span></span>
-   <span data-ttu-id="6cc4a-301">目标</span><span class="sxs-lookup"><span data-stu-id="6cc4a-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="6cc4a-302">其他资源</span><span class="sxs-lookup"><span data-stu-id="6cc4a-302">Additional resources</span></span>
--------

[<span data-ttu-id="6cc4a-303">创建一个表达式约束</span><span class="sxs-lookup"><span data-stu-id="6cc4a-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="6cc4a-304">将计算添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="6cc4a-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



