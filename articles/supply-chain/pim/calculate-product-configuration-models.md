---
title: 产品配置模型的计算常见问题
description: 本主题描述产品配置模型的计算。并说明如何与约束一起使用计算。
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7fac3ec6df53dcc6e459f62f76d856a11d294b6
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981344"
---
# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="b68ef-103">产品配置模型的计算常见问题</span><span class="sxs-lookup"><span data-stu-id="b68ef-103">Calculations for product configuration models FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b68ef-104">本主题描述产品配置模型的计算。并说明如何与约束一起使用计算。</span><span class="sxs-lookup"><span data-stu-id="b68ef-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="b68ef-105">计算可以用于算术运算或逻辑运算。</span><span class="sxs-lookup"><span data-stu-id="b68ef-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="b68ef-106">它们补充产品配置模型的表达式约束。</span><span class="sxs-lookup"><span data-stu-id="b68ef-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="b68ef-107">您可以在**基于约束的产品配置模型详细信息**页上定义计算，然后在表达式编辑器中构建计算表达式。</span><span class="sxs-lookup"><span data-stu-id="b68ef-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="b68ef-108">有关详细信息，请参阅“创建计算”。</span><span class="sxs-lookup"><span data-stu-id="b68ef-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="b68ef-109">计算是什么？</span><span class="sxs-lookup"><span data-stu-id="b68ef-109">What is a calculation?</span></span>
<span data-ttu-id="b68ef-110">计算是您在产品配置模型中可以使用的元素。</span><span class="sxs-lookup"><span data-stu-id="b68ef-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="b68ef-111">在您配置产品时，通过能够让您使用小数来计算值，计算可以补充约束。</span><span class="sxs-lookup"><span data-stu-id="b68ef-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="b68ef-112">此外，与约束相比，计算具有更大的可用运算符集。</span><span class="sxs-lookup"><span data-stu-id="b68ef-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="b68ef-113">与约束相似，计算与产品配置模型中的特定组件关联，且其不能被其他组件重用或共享。</span><span class="sxs-lookup"><span data-stu-id="b68ef-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="b68ef-114">计算和约束之间的重要差异在于计算是必需的（单向），而约束是说明性的（双向）。</span><span class="sxs-lookup"><span data-stu-id="b68ef-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="b68ef-115">有关约束的详细信息，请参阅[产品配置模型中的表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。</span><span class="sxs-lookup"><span data-stu-id="b68ef-115">For more information about constraints, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="b68ef-116">计算包含目标属性和计算表达式。</span><span class="sxs-lookup"><span data-stu-id="b68ef-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="b68ef-117">目标属性是什么？</span><span class="sxs-lookup"><span data-stu-id="b68ef-117">What is a target attribute?</span></span>
<span data-ttu-id="b68ef-118">目标属性是一种接收计算表达式结果的属性。</span><span class="sxs-lookup"><span data-stu-id="b68ef-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="b68ef-119">在下面的表达式中，目标属性是桌布度量：</span><span class="sxs-lookup"><span data-stu-id="b68ef-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="b68ef-120">**表达式：** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span><span class="sxs-lookup"><span data-stu-id="b68ef-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="b68ef-121">**DecimalAttribute1** 是桌子长度，而 **decimalAttribute2** 是桌布长度。</span><span class="sxs-lookup"><span data-stu-id="b68ef-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="b68ef-122">如果 **decimalAttribute2** 大于或等于 **decimalAttribute1**，则表达式返回 **True** 值到目标属性。</span><span class="sxs-lookup"><span data-stu-id="b68ef-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="b68ef-123">否则，该表达式返回 **False** 值。</span><span class="sxs-lookup"><span data-stu-id="b68ef-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="b68ef-124">因此，如果桌布长度等于或超过桌子长度，则可接受桌布度量。</span><span class="sxs-lookup"><span data-stu-id="b68ef-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="b68ef-125">对目标属性可以设置何种属性类型？</span><span class="sxs-lookup"><span data-stu-id="b68ef-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="b68ef-126">除了没有固定列表的文本，产品配置器支持的所有属性类型均可设置为目标属性。</span><span class="sxs-lookup"><span data-stu-id="b68ef-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="b68ef-127">目标属性的值可以限制计算中输入属性的值吗？</span><span class="sxs-lookup"><span data-stu-id="b68ef-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="b68ef-128">不能，目标属性的值不能限制输入属性的值，因为计算是单向的。</span><span class="sxs-lookup"><span data-stu-id="b68ef-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="b68ef-129">因此，目标属性的值基于输入属性值的更改设置，但是，该目标值的更改不影响输入属性的值。</span><span class="sxs-lookup"><span data-stu-id="b68ef-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="b68ef-130">此行为与约束的行为不同。</span><span class="sxs-lookup"><span data-stu-id="b68ef-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="b68ef-131">约束出现在两个方向。</span><span class="sxs-lookup"><span data-stu-id="b68ef-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="b68ef-132">示例</span><span class="sxs-lookup"><span data-stu-id="b68ef-132">Example</span></span>

<span data-ttu-id="b68ef-133">在下面的表达式中，计算的目标是电源线的长度，并且输入值为颜色：</span><span class="sxs-lookup"><span data-stu-id="b68ef-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="b68ef-134">**表达式：**\[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="b68ef-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="b68ef-135">果您指定**绿色**为颜色属性的值，则设置电源线的长度为 **1.5**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="b68ef-136">如果您指定其他颜色，该长度设置为 **1.0**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="b68ef-137">但是，由于计算为单向，如果您指定长度为 **1.5**，计算不能将颜色属性的值设置为**绿色**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="b68ef-138">如果计算具有整数类型的目标属性，但是计算生成了一个小数，此时将发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="b68ef-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="b68ef-139">如果目标属性是整数类型，不过，计算生成小数，则只返回计算结果的整数部分。</span><span class="sxs-lookup"><span data-stu-id="b68ef-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="b68ef-140">移除小数部分，且不舍入结果。</span><span class="sxs-lookup"><span data-stu-id="b68ef-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="b68ef-141">例如，结果为 12.70 将显示为 12。</span><span class="sxs-lookup"><span data-stu-id="b68ef-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="b68ef-142">何时出现计算？</span><span class="sxs-lookup"><span data-stu-id="b68ef-142">When do calculations occur?</span></span>
<span data-ttu-id="b68ef-143">在为所有输入属性提供一个值时出现计算。</span><span class="sxs-lookup"><span data-stu-id="b68ef-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="b68ef-144">我可以覆盖为目标属性计算的值吗？</span><span class="sxs-lookup"><span data-stu-id="b68ef-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="b68ef-145">您可以覆盖为目标属性计算的值，除非目标属性被设置为隐藏或只读状态。</span><span class="sxs-lookup"><span data-stu-id="b68ef-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="b68ef-146">当处于隐藏或只读状态时，如何设置目标属性？</span><span class="sxs-lookup"><span data-stu-id="b68ef-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="b68ef-147">若要设置处于隐藏或只读状态的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b68ef-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="b68ef-148">单击**产品信息管理** &gt; **通用** &gt; **产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="b68ef-149">选择产品配置模型，然后在“操作窗格”上，单击 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="b68ef-150">在**基于约束的产品配置模型详细信息**页上，选择用作目标属性的属性。</span><span class="sxs-lookup"><span data-stu-id="b68ef-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="b68ef-151">在**属性**快速选项卡上，选择**隐藏**或**只读**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="b68ef-152">计算可以覆盖我设置的值吗？</span><span class="sxs-lookup"><span data-stu-id="b68ef-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="b68ef-153">编号</span><span class="sxs-lookup"><span data-stu-id="b68ef-153">No.</span></span> <span data-ttu-id="b68ef-154">在您配置产品时您设置的值即为所使用的值。</span><span class="sxs-lookup"><span data-stu-id="b68ef-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="b68ef-155">在计算中更改输入值时出现的计算不能覆盖您为特定属性提供的值。</span><span class="sxs-lookup"><span data-stu-id="b68ef-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="b68ef-156">如果我移除计算中的输入值会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="b68ef-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="b68ef-157">如果您移除计算中的输入值，目标属性的值也将被移除。</span><span class="sxs-lookup"><span data-stu-id="b68ef-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="b68ef-158">为什么我收到一条错误消息称我的模型处于冲突状态？</span><span class="sxs-lookup"><span data-stu-id="b68ef-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="b68ef-159">在计算包含错误或在一个或多个约束存在冲突时将显示此消息。</span><span class="sxs-lookup"><span data-stu-id="b68ef-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="b68ef-160">有关约束中冲突的详细信息，请参阅[产品配置模型中的表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。</span><span class="sxs-lookup"><span data-stu-id="b68ef-160">For more information about contradictions in constraints, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="b68ef-161">这是一些计算中可能出现错误的情况：</span><span class="sxs-lookup"><span data-stu-id="b68ef-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="b68ef-162">值除以 0（零）。</span><span class="sxs-lookup"><span data-stu-id="b68ef-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="b68ef-163">冲突存在于以下两个元素之间：</span><span class="sxs-lookup"><span data-stu-id="b68ef-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="b68ef-164">可用于属性的值与由约束限制的值</span><span class="sxs-lookup"><span data-stu-id="b68ef-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="b68ef-165">由计算产生的值</span><span class="sxs-lookup"><span data-stu-id="b68ef-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="b68ef-166">由计算返回的值超出属性的域之外。</span><span class="sxs-lookup"><span data-stu-id="b68ef-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="b68ef-167">示例是计算为 0 的从 \[1..10\] 的一个整数。</span><span class="sxs-lookup"><span data-stu-id="b68ef-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="b68ef-168">为什么即使在我成功验证了我的产品模型后仍收到错误消息？</span><span class="sxs-lookup"><span data-stu-id="b68ef-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="b68ef-169">验证中并不包括计算。</span><span class="sxs-lookup"><span data-stu-id="b68ef-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="b68ef-170">您必须测试产品配置模型以查找计算中的错误。</span><span class="sxs-lookup"><span data-stu-id="b68ef-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="b68ef-171">若要测试产品配置模型，请按照下面的步骤执行。</span><span class="sxs-lookup"><span data-stu-id="b68ef-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="b68ef-172">单击**产品信息管理** &gt; **通用** &gt; **产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="b68ef-173">选择产品配置模型，然后在“操作窗格”上，在**运行**组中单击**测试**。</span><span class="sxs-lookup"><span data-stu-id="b68ef-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>




