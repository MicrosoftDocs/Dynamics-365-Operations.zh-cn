---
title: 产品配置模型计算
description: 本主题介绍如何在产品配置模型中为属性创建计算
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829610"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="596ee-103">产品配置模型计算</span><span class="sxs-lookup"><span data-stu-id="596ee-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="596ee-104">本主题介绍如何在产品配置模型中为属性创建计算。</span><span class="sxs-lookup"><span data-stu-id="596ee-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="596ee-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="596ee-105">Prerequisites</span></span>

<span data-ttu-id="596ee-106">计算用于产品配置模型中以计算产品的配置值。</span><span class="sxs-lookup"><span data-stu-id="596ee-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="596ee-107">必须存在相关的产品配置模型，然后才能开始设置计算。</span><span class="sxs-lookup"><span data-stu-id="596ee-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="596ee-108">有关配置模型和相关任务的设置流程的概述，请参阅[设置产品配置模型](set-up-maintain-product-configuration-model.md)。</span><span class="sxs-lookup"><span data-stu-id="596ee-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="596ee-109">创建计算</span><span class="sxs-lookup"><span data-stu-id="596ee-109">Create a calculation</span></span>

<span data-ttu-id="596ee-110">计算由一个表达式和一个目标属性组成。</span><span class="sxs-lookup"><span data-stu-id="596ee-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="596ee-111">有关详细信息，请参阅[产品配置模型的计算常见问题解答](calculate-product-configuration-models.md)。</span><span class="sxs-lookup"><span data-stu-id="596ee-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="596ee-112">若要为现有产品模型创建计算，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="596ee-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="596ee-113">转到 **产品信息管理 \> 通用 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="596ee-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="596ee-114">打开产品配置模型，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="596ee-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="596ee-115">在 **计算** 快速选项卡上，选择 **添加** 以添加计算，然后设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="596ee-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="596ee-116">**名称** – 输入计算的名称。</span><span class="sxs-lookup"><span data-stu-id="596ee-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="596ee-117">**描述** – 输入计算的描述。</span><span class="sxs-lookup"><span data-stu-id="596ee-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="596ee-118">**目标属性** – 选择要为其进行计算的属性。</span><span class="sxs-lookup"><span data-stu-id="596ee-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="596ee-119">选择 **编辑表达式**。</span><span class="sxs-lookup"><span data-stu-id="596ee-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="596ee-120">在 **输入计算** 对话框中，将所需的属性、运算符和值添加到表达式。</span><span class="sxs-lookup"><span data-stu-id="596ee-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="596ee-121">有关如何处理这些元素的详细信息，请参阅[产品配置模型中的表达式约束和表约束](expression-constraints-table-constraints-product-configuration-models.md)。</span><span class="sxs-lookup"><span data-stu-id="596ee-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="596ee-122">当表达式准备就绪时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="596ee-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="596ee-123">计算示例</span><span class="sxs-lookup"><span data-stu-id="596ee-123">Calculation examples</span></span>

<span data-ttu-id="596ee-124">本部分提供一些示例，显示了计算的工作方式。</span><span class="sxs-lookup"><span data-stu-id="596ee-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="596ee-125">示例 1</span><span class="sxs-lookup"><span data-stu-id="596ee-125">Example 1</span></span>

<span data-ttu-id="596ee-126">目标属性是布尔，此计算使用以下条件表达式：</span><span class="sxs-lookup"><span data-stu-id="596ee-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="596ee-127">如果 `decimalAttribute2` 大于或等于 `decimalAttribute1`，此表达式返回 *True* 值到目标属性。</span><span class="sxs-lookup"><span data-stu-id="596ee-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="596ee-128">否则，返回 *False* 值。</span><span class="sxs-lookup"><span data-stu-id="596ee-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="596ee-129">示例 2</span><span class="sxs-lookup"><span data-stu-id="596ee-129">Example 2</span></span>

<span data-ttu-id="596ee-130">本示例使用文本属性 `textFixedList` 作为目标属性。</span><span class="sxs-lookup"><span data-stu-id="596ee-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="596ee-131">此属性包含以下固定列表。</span><span class="sxs-lookup"><span data-stu-id="596ee-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="596ee-132">值</span><span class="sxs-lookup"><span data-stu-id="596ee-132">Value</span></span> | <span data-ttu-id="596ee-133">求解器值</span><span class="sxs-lookup"><span data-stu-id="596ee-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="596ee-134">A</span><span class="sxs-lookup"><span data-stu-id="596ee-134">A</span></span> | <span data-ttu-id="596ee-135">1a</span><span class="sxs-lookup"><span data-stu-id="596ee-135">1a</span></span> |
| <span data-ttu-id="596ee-136">B</span><span class="sxs-lookup"><span data-stu-id="596ee-136">B</span></span> | <span data-ttu-id="596ee-137">2b</span><span class="sxs-lookup"><span data-stu-id="596ee-137">2b</span></span> |
| <span data-ttu-id="596ee-138">C</span><span class="sxs-lookup"><span data-stu-id="596ee-138">C</span></span> | <span data-ttu-id="596ee-139">2c</span><span class="sxs-lookup"><span data-stu-id="596ee-139">2c</span></span> |

<span data-ttu-id="596ee-140">以下屏幕截图显示此属性的设置在您的系统中的外观。</span><span class="sxs-lookup"><span data-stu-id="596ee-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="596ee-141">![示例 2 的属性类型设置](media/model-calculations-example2.png "示例 2 的属性类型设置")</span><span class="sxs-lookup"><span data-stu-id="596ee-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="596ee-142">在以下条件语句中使用该属性：</span><span class="sxs-lookup"><span data-stu-id="596ee-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="596ee-143">如果 `integerAttribute` 小于 150，此语句将返回固定列表中第一条记录的文本值 *A*。否则，它将返回固定列表中第三条记录的文本值 *C*。</span><span class="sxs-lookup"><span data-stu-id="596ee-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="596ee-144">固定列表等效于从零开始的枚举 (enum)，并且其值由适当的整数值访问。</span><span class="sxs-lookup"><span data-stu-id="596ee-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="596ee-145">因此，第一个固定列表值 (*A*) 与 *0* 匹配，第二个值 (*B*) 与 *1* 匹配，第三个值 (*C*) 与 *2* 匹配。</span><span class="sxs-lookup"><span data-stu-id="596ee-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="596ee-146">示例 3</span><span class="sxs-lookup"><span data-stu-id="596ee-146">Example 3</span></span>

<span data-ttu-id="596ee-147">本示例使用上一个示例中的 `textFixedList` 目标属性。</span><span class="sxs-lookup"><span data-stu-id="596ee-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="596ee-148">它还使用另一个文本属性 `textAttribute`，其中包含以下固定列表。</span><span class="sxs-lookup"><span data-stu-id="596ee-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="596ee-149">值</span><span class="sxs-lookup"><span data-stu-id="596ee-149">Value</span></span> | <span data-ttu-id="596ee-150">求解器值</span><span class="sxs-lookup"><span data-stu-id="596ee-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="596ee-151">AA</span><span class="sxs-lookup"><span data-stu-id="596ee-151">AA</span></span> | <span data-ttu-id="596ee-152">1aa</span><span class="sxs-lookup"><span data-stu-id="596ee-152">1aa</span></span> |
| <span data-ttu-id="596ee-153">BB</span><span class="sxs-lookup"><span data-stu-id="596ee-153">BB</span></span> | <span data-ttu-id="596ee-154">2bb</span><span class="sxs-lookup"><span data-stu-id="596ee-154">2bb</span></span> |

<span data-ttu-id="596ee-155">以下屏幕截图显示此属性的设置在您的系统中的外观。</span><span class="sxs-lookup"><span data-stu-id="596ee-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="596ee-156">![示例 3 的属性类型设置](media/model-calculations-example3.png "示例 3 的属性类型设置")</span><span class="sxs-lookup"><span data-stu-id="596ee-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="596ee-157">使用以下条件语句计算 `textFixedList` 属性的值：</span><span class="sxs-lookup"><span data-stu-id="596ee-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="596ee-158">如果 `textAttribute` 值具有等于 *1aa* 的求解值，此表达式将返回 `textFixedList` 固定列表中第一条记录的文本值 *A*。否则，它将返回 `textFixedList` 固定列表中第三条记录的文本值 *C*。</span><span class="sxs-lookup"><span data-stu-id="596ee-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="596ee-159">条件语句必须使用属性的求解值。</span><span class="sxs-lookup"><span data-stu-id="596ee-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="596ee-160">在计算中只能使用固定列表文本属性。</span><span class="sxs-lookup"><span data-stu-id="596ee-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="596ee-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="596ee-161">See also</span></span>

- [<span data-ttu-id="596ee-162">产品配置模型的计算常见问题</span><span class="sxs-lookup"><span data-stu-id="596ee-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="596ee-163">将表达式约束添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="596ee-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="596ee-164">产品配置模型概述</span><span class="sxs-lookup"><span data-stu-id="596ee-164">Product configuration models overview</span></span>](product-configuration-models.md)
