---
title: "系统定义和用户定义的表约束"
description: "本文说明产品配置模型中的组件的表约束的两个类型 - 用户定义和系统定义。 表约束表示允许的属性组合的矩阵，在其中每行定义一组可能的属性值。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: b59452496f0ad47f1fe2ff034895a082a205dda9
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="b5753-104">系统定义和用户定义的表约束</span><span class="sxs-lookup"><span data-stu-id="b5753-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b5753-105">本文说明产品配置模型中的组件的表约束的两个类型 - 用户定义和系统定义。</span><span class="sxs-lookup"><span data-stu-id="b5753-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="b5753-106">表约束表示允许的属性组合的矩阵，在其中每行定义一组可能的属性值。</span><span class="sxs-lookup"><span data-stu-id="b5753-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="b5753-107">表约束表示产品配置模型中的组件允许的属性组合的矩阵。</span><span class="sxs-lookup"><span data-stu-id="b5753-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="b5753-108">表中的每行定义一组可能的属性值。</span><span class="sxs-lookup"><span data-stu-id="b5753-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="b5753-109">可在产品配置模型中声明两种类型的约束：</span><span class="sxs-lookup"><span data-stu-id="b5753-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="b5753-110">**表达式约束** – 创建一个表达式，用以定义属性之间的关系，以确保配置产品时仅可选择兼容值。</span><span class="sxs-lookup"><span data-stu-id="b5753-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="b5753-111">**表约束** – 创建定义指定的属性集允许的所有组合的表。</span><span class="sxs-lookup"><span data-stu-id="b5753-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="b5753-112">两种类型的表约束可用：用户定义的表约束和系统定义的表约束。</span><span class="sxs-lookup"><span data-stu-id="b5753-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="b5753-113">本文描述用户定义和系统定义的用于产品配置模型中的组件的表约束。</span><span class="sxs-lookup"><span data-stu-id="b5753-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="b5753-114">用户定义的表约束</span><span class="sxs-lookup"><span data-stu-id="b5753-114">User-defined table constraints</span></span>
<span data-ttu-id="b5753-115">用户定义的表约束是一种可于描述属性类型定义的属性值组合的矩阵。</span><span class="sxs-lookup"><span data-stu-id="b5753-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="b5753-116">例如，如果生产扬声器，您可以在用户定义的表约束中包括用于机柜表面处理和前格栅的列。</span><span class="sxs-lookup"><span data-stu-id="b5753-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="b5753-117">机柜表面处理的属性类型有四个值，前格栅的属性类型有三个值。</span><span class="sxs-lookup"><span data-stu-id="b5753-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="b5753-118">因此，如果不使用约束，有 4 × 3 = 12 个可能组合。</span><span class="sxs-lookup"><span data-stu-id="b5753-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="b5753-119">但是，在本示例中，只允许六个组合，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="b5753-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="b5753-120">此信息显示在**“编辑表约束”**页上的**“允许的组合”**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="b5753-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="b5753-121">机柜表面处理</span><span class="sxs-lookup"><span data-stu-id="b5753-121">Cabinet finish</span></span> | <span data-ttu-id="b5753-122">前格栅</span><span class="sxs-lookup"><span data-stu-id="b5753-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="b5753-123">黑</span><span class="sxs-lookup"><span data-stu-id="b5753-123">Black</span></span>          | <span data-ttu-id="b5753-124">黑</span><span class="sxs-lookup"><span data-stu-id="b5753-124">Black</span></span>       |
| <span data-ttu-id="b5753-125">黑</span><span class="sxs-lookup"><span data-stu-id="b5753-125">Black</span></span>          | <span data-ttu-id="b5753-126">金属</span><span class="sxs-lookup"><span data-stu-id="b5753-126">Metal</span></span>       |
| <span data-ttu-id="b5753-127">橡木</span><span class="sxs-lookup"><span data-stu-id="b5753-127">Oak</span></span>            | <span data-ttu-id="b5753-128">黑</span><span class="sxs-lookup"><span data-stu-id="b5753-128">Black</span></span>       |
| <span data-ttu-id="b5753-129">红木</span><span class="sxs-lookup"><span data-stu-id="b5753-129">Rosewood</span></span>       | <span data-ttu-id="b5753-130">白色</span><span class="sxs-lookup"><span data-stu-id="b5753-130">White</span></span>       |
| <span data-ttu-id="b5753-131">白色</span><span class="sxs-lookup"><span data-stu-id="b5753-131">White</span></span>          | <span data-ttu-id="b5753-132">黑</span><span class="sxs-lookup"><span data-stu-id="b5753-132">Black</span></span>       |
| <span data-ttu-id="b5753-133">白色</span><span class="sxs-lookup"><span data-stu-id="b5753-133">White</span></span>          | <span data-ttu-id="b5753-134">白色</span><span class="sxs-lookup"><span data-stu-id="b5753-134">White</span></span>       |

<span data-ttu-id="b5753-135">用户定义的表约束由工作方式与表达式约束系统的静态表输入定义。</span><span class="sxs-lookup"><span data-stu-id="b5753-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="b5753-136">使用用户定义的表约束时，该表的优点是通常比长表达式约束更易于创建、了解和维护。</span><span class="sxs-lookup"><span data-stu-id="b5753-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="b5753-137">系统定义的表约束</span><span class="sxs-lookup"><span data-stu-id="b5753-137">System-defined table constraints</span></span>
<span data-ttu-id="b5753-138">系统定义的表约束在表中的属性类型与字段之间创建动态映射。</span><span class="sxs-lookup"><span data-stu-id="b5753-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="b5753-139">当系统定义的表约束包括在产品配置模型中时，映射可确保显示表中的数据，而不是属性类型的值。</span><span class="sxs-lookup"><span data-stu-id="b5753-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="b5753-140">结果是动态约束，因为表内容可被修改（例如，由其他模块）。</span><span class="sxs-lookup"><span data-stu-id="b5753-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="b5753-141">创建系统定义的表约束时，选择一个表，（可选）定义要使用的查询，然后将这些属性类型与所选表中的字段关联。</span><span class="sxs-lookup"><span data-stu-id="b5753-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="b5753-142">字段的类型必须与属性类型的类型匹配。</span><span class="sxs-lookup"><span data-stu-id="b5753-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="b5753-143">在表约束可以在产品配置模型上生效之前，表约束必须包括在一个模型的组件上的约束中。</span><span class="sxs-lookup"><span data-stu-id="b5753-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="b5753-144">过程是创建新约束，选择表约束类型，然后选择要使用的表约束定义。</span><span class="sxs-lookup"><span data-stu-id="b5753-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="b5753-145">最后，表中的所有字段都必须映射到产品配置模型中的属性。</span><span class="sxs-lookup"><span data-stu-id="b5753-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="b5753-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5753-146">See also</span></span>
--------

[<span data-ttu-id="b5753-147">产品配置模型中的重要概念</span><span class="sxs-lookup"><span data-stu-id="b5753-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




