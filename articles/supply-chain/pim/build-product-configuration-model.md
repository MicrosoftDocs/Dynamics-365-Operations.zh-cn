---
title: 产品配置概览
description: “将产品配置为可满足特定要求”这一需求在“企业对企业”和“企业对消费者”关系中都正在成为规则而不是特例。
author: cvocph
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, ConfigPartOf
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b7d1186b4141a18e1283505713e67018927672d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422659"
---
# <a name="product-configuration-overview"></a><span data-ttu-id="b335f-103">产品配置概览</span><span class="sxs-lookup"><span data-stu-id="b335f-103">Product configuration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b335f-104">“将产品配置为可满足特定要求”这一需求在“企业对企业”和“企业对消费者”关系中都正在成为规则而不是特例。</span><span class="sxs-lookup"><span data-stu-id="b335f-104">The need to configure products to meet special requirements is becoming the rule rather than the exception, in both business-to-business and business-to-consumer relationships.</span></span>

<span data-ttu-id="b335f-105">支持配置对订单方案的制造商拥有更仔细地贴近客户需求的机会。</span><span class="sxs-lookup"><span data-stu-id="b335f-105">A manufacturer that supports configure-to-order scenarios has an opportunity to tend more carefully to customer needs.</span></span> <span data-ttu-id="b335f-106">此外，通过以通用组件（而不是成品）的形式贮存半成品，制造商可以减少与库存有关的成本本。</span><span class="sxs-lookup"><span data-stu-id="b335f-106">Additionally, by stocking semi-finished goods in the form of generic components instead of finished products, the manufacturer can reduce the capital that is tied to inventory.</span></span>  

<span data-ttu-id="b335f-107">从制造到贮存理念到配置到订购理念的成功转变需要仔细分析产品结构、产品系列的标识以及组件化。</span><span class="sxs-lookup"><span data-stu-id="b335f-107">A successful move from a manufacture-to-stock setup to a configure-to-order setup requires careful analysis of the product structures, identification of product families, and componentization.</span></span> <span data-ttu-id="b335f-108">为了减少部件数和最大程度地减少处理中的货物数，您务必了解产品接口和基于可重用性进行设计。</span><span class="sxs-lookup"><span data-stu-id="b335f-108">To reduce the number of parts and minimize the number of goods that are in process, it's very important that you understand the product interfaces, and that you design for reusability.</span></span>  

<span data-ttu-id="b335f-109">有几个产品配置建模原则，例如基于规则、基于维度和基于约束的建模。</span><span class="sxs-lookup"><span data-stu-id="b335f-109">There are several product configuration modeling principles, such as rule-based, dimension-based, and constraint-based modeling.</span></span> <span data-ttu-id="b335f-110">研究表明，与其他建模原则相比，基于约束的方法可在模型中减少大约 50% 的代码行数。</span><span class="sxs-lookup"><span data-stu-id="b335f-110">Studies show that the constraint-based methodology can reduce the number of code lines in models by about 50 percent compared to other modeling principles.</span></span> <span data-ttu-id="b335f-111">因此，此方法可降低总拥有成本 (TCO)。</span><span class="sxs-lookup"><span data-stu-id="b335f-111">Therefore, this methodology can reduce the total cost of ownership (TCO).</span></span> <span data-ttu-id="b335f-112">通过从以 X++ 代码为基础的基于规则的模型转为基于约束的模型，您在维护产品模型时不再需要开发人员许可证。</span><span class="sxs-lookup"><span data-stu-id="b335f-112">By moving from a rule-based model that is based on X++ code to a constraint-based model, you no longer require a developer license in order to maintain product models.</span></span>

## <a name="product-configuration"></a><span data-ttu-id="b335f-113">产品配置</span><span class="sxs-lookup"><span data-stu-id="b335f-113">Product configuration</span></span>
<span data-ttu-id="b335f-114">在工业化时代，人们在生产品质优良、功能丰富且价格实惠的产品方面取得了巨大成就。</span><span class="sxs-lookup"><span data-stu-id="b335f-114">The industrialization period has led to great achievements in producing high-quality and feature-rich products at affordable prices.</span></span> <span data-ttu-id="b335f-115">规模经济使工业化世界内的大多数人都能购买我们视为日常生活中必不可少的一部分的汽车、电视、家用电器和其他商品。</span><span class="sxs-lookup"><span data-stu-id="b335f-115">The economies of scale have made it possible for most people in the industrialized world to buy cars, TVs, household appliances, and other goods that most of us consider a necessary part of our everyday life.</span></span>  

<span data-ttu-id="b335f-116">随着很多产品变为日用品，人们需要将它们区分开来。</span><span class="sxs-lookup"><span data-stu-id="b335f-116">As many products have become commodities, a need to differentiate them has arisen.</span></span> <span data-ttu-id="b335f-117">制造商对这一挑战的即时响应使得每个产品的变型也随之产生，以便让客户有更多替代选择。</span><span class="sxs-lookup"><span data-stu-id="b335f-117">The immediate response of manufacturers to this challenge has been to create variants of each product, so that customers have more alternatives.</span></span> <span data-ttu-id="b335f-118">此策略导致预测难题增加，并导致库存成本和过时的未售出产品增多。</span><span class="sxs-lookup"><span data-stu-id="b335f-118">This strategy has led to increased forecast challenges, and also to an increase in inventory cost and unsold products that become obsolete.</span></span>  

<span data-ttu-id="b335f-119">通过采用配置到订购理念，制造商有机会满足客户对独有产品的需求，同时减少和消除过时的库存物料。</span><span class="sxs-lookup"><span data-stu-id="b335f-119">By adopting a configure-to-order philosophy, manufactures have an opportunity to meet customer demand for unique products while reducing or eliminating obsolete inventory items.</span></span> <span data-ttu-id="b335f-120">当制造到贮存理念转变为配置到订购理念时，随之而来的一个直接难题是必须平衡对较短的前置时间的需求与较低的库存水平。</span><span class="sxs-lookup"><span data-stu-id="b335f-120">When a manufacture-to-stock philosophy is shifted to a configure-to-order philosophy, one immediate challenge that arises is that the need for short lead times must be balanced against low inventory levels.</span></span>  

<span data-ttu-id="b335f-121">对此，成功的关键在于仔细分析产品组合和寻找产品功能和流程中的模式。</span><span class="sxs-lookup"><span data-stu-id="b335f-121">The key to success here is to carefully analyze the product portfolio, and to look for patterns in both product features and processes.</span></span> <span data-ttu-id="b335f-122">目的是确定可由同一台设备制造并在所有变型中使用的通用组件。</span><span class="sxs-lookup"><span data-stu-id="b335f-122">The goal is to identify generic components that can be manufactured by the same equipment and used in all variants.</span></span>  

<span data-ttu-id="b335f-123">新产品配置功能集包括提供产品配置模型结构的视觉概览的用户界面 (UI)，并包括不必编译的描述性约束语法。</span><span class="sxs-lookup"><span data-stu-id="b335f-123">The new Product configuration feature set includes a user interface (UI) that provides a visual overview of the product configuration model structure, and also a declarative constraint syntax that doesn't have to be compiled.</span></span> <span data-ttu-id="b335f-124">因此，希望支持配置实践的公司可以更轻松地上路。</span><span class="sxs-lookup"><span data-stu-id="b335f-124">Therefore, companies that want to support a configuration practice can get started more easily.</span></span> <span data-ttu-id="b335f-125">如以下章节所述，产品设计人员不再需要开发人员的支持即可构建产品配置模型、测试该模型，然后将该模型发布到销售组织。</span><span class="sxs-lookup"><span data-stu-id="b335f-125">As the following sections explain, a product designer no longer requires the support of a developer to build a product configuration model, test it, and release it to the sales organization.</span></span>

## <a name="building-a-product-configuration-model"></a><span data-ttu-id="b335f-126">构建产品配置模型</span><span class="sxs-lookup"><span data-stu-id="b335f-126">Building a product configuration model</span></span>
<span data-ttu-id="b335f-127">用户可通过几种方法构建产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b335f-127">There are several approaches that a user can take to build a product configuration model.</span></span> <span data-ttu-id="b335f-128">一种方法是执行一个顺序流 - 先创建所有引用数据（如基础产品、独特产品和运营资源），然后将这些数据作为组件、物料清单 (BOM) 行、工艺路线工序和产品配置模型的其他因素包含。</span><span class="sxs-lookup"><span data-stu-id="b335f-128">One option is to follow a sequential flow by first creating all the reference data, such as product masters, distinct products, and operational resources, and then including them as components, bill of materials (BOM) lines, route operations, and other elements of the product configuration model.</span></span> <span data-ttu-id="b335f-129">或者，您也可以通过先创建模型然后在需要时添加引用数据来选择更具迭代性的方法。</span><span class="sxs-lookup"><span data-stu-id="b335f-129">Alternatively, you can select a more iterative approach by first creating the model and then adding reference data as the need arises.</span></span>

### <a name="components"></a><span data-ttu-id="b335f-130">组件</span><span class="sxs-lookup"><span data-stu-id="b335f-130">Components</span></span>

<span data-ttu-id="b335f-131">产品配置模型包含通过子组件关系绑定在一起的一个或多个组件。</span><span class="sxs-lookup"><span data-stu-id="b335f-131">A product configuration model consists of one or more components that are tied together through subcomponent relationships.</span></span> <span data-ttu-id="b335f-132">组件只需定义一次便能在一个或多个产品配置模型中多次使用。</span><span class="sxs-lookup"><span data-stu-id="b335f-132">Components are defined one time, and can then be used many times in one or more product configuration models.</span></span> <span data-ttu-id="b335f-133">组件是产品配置模型的主构建基块，几乎所有有关模型的信息都与组件相关。</span><span class="sxs-lookup"><span data-stu-id="b335f-133">The components are the main building blocks of a product configuration model, and nearly all information about the model is related to them.</span></span>

### <a name="attributes"></a><span data-ttu-id="b335f-134">属性</span><span class="sxs-lookup"><span data-stu-id="b335f-134">Attributes</span></span>

<span data-ttu-id="b335f-135">每个组件都有标识其属性的一个或多个属性。</span><span class="sxs-lookup"><span data-stu-id="b335f-135">Each component has one or more attributes that identify its properties.</span></span> <span data-ttu-id="b335f-136">属性是用户将在配置过程中选择的内容。</span><span class="sxs-lookup"><span data-stu-id="b335f-136">The attributes are what users will choose during the configuration process.</span></span> <span data-ttu-id="b335f-137">属性通过约束或计算中的包含来控制组件间或组件内关系。</span><span class="sxs-lookup"><span data-stu-id="b335f-137">Attributes control both inter-component and intra-component relationships through inclusion in constraints or calculations.</span></span> <span data-ttu-id="b335f-138">通过应用于物料清单行的条件，属性可用于确定已配置产品所包含的实体部件。</span><span class="sxs-lookup"><span data-stu-id="b335f-138">Through conditions that are applied to BOM lines, the attributes can be used to determine which physical parts the configured product will consist of.</span></span> <span data-ttu-id="b335f-139">此外，属性还可通过映射机制控制物料清单行的属性。</span><span class="sxs-lookup"><span data-stu-id="b335f-139">Additionally, an attribute can control the property of a BOM line through a mapping mechanism.</span></span> <span data-ttu-id="b335f-140">与包含和属性设置有关的工艺路线工序存在类似的功能。</span><span class="sxs-lookup"><span data-stu-id="b335f-140">Similar functionality exists for route operations regarding both inclusion and property settings.</span></span>

>[!NOTE]
> <span data-ttu-id="b335f-141">创建属性类型时，请避免为属性类型域创建大量的值。</span><span class="sxs-lookup"><span data-stu-id="b335f-141">When you create attribute types, avoid creating a high number of values for the attribute type domain.</span></span> <span data-ttu-id="b335f-142">这样做可能会导致产品配置器的速度降低。</span><span class="sxs-lookup"><span data-stu-id="b335f-142">Doing so could cause slowdowns in the product configurator.</span></span> 

### <a name="expression-constraints"></a><span data-ttu-id="b335f-143">表达式约束 </span><span class="sxs-lookup"><span data-stu-id="b335f-143">Expression constraints</span></span>

<span data-ttu-id="b335f-144">基于约束的产品配置模型的使用暗示在用户为各种属性选择值时存在一些限制。</span><span class="sxs-lookup"><span data-stu-id="b335f-144">Use of a constraint-based product configuration model implies that some limitations exist when the user selects values for the various attributes.</span></span> <span data-ttu-id="b335f-145">此类限制可借助优化建模语言 (OML) 作为表达式约束来实施。</span><span class="sxs-lookup"><span data-stu-id="b335f-145">Such limitations can be implemented as expression constraints by using the Optimization Modeling Language (OML).</span></span> <span data-ttu-id="b335f-146">或者，约束也可以表约束的形式实施。</span><span class="sxs-lookup"><span data-stu-id="b335f-146">Alternatively, a constraint can be implemented in the form of a table constraint.</span></span>

### <a name="table-constraints"></a><span data-ttu-id="b335f-147">表约束</span><span class="sxs-lookup"><span data-stu-id="b335f-147">Table constraints</span></span>

<span data-ttu-id="b335f-148">表约束可以是用户定义的，也可以是系统定义的。</span><span class="sxs-lookup"><span data-stu-id="b335f-148">Table constraints can be user-defined or system-defined.</span></span>  

<span data-ttu-id="b335f-149">用户定义的表约束由用户构建。</span><span class="sxs-lookup"><span data-stu-id="b335f-149">A user-defined table constraint is built by the user.</span></span> <span data-ttu-id="b335f-150">用户选择用于表示表列的属性类型的组合，然后输入来自所选属性类型的域并用于在表约束中形成行的值。</span><span class="sxs-lookup"><span data-stu-id="b335f-150">The user selects a combination of attribute types to represent the columns of the table and then enters values from the domains of the selected attribute types to form the rows in the table constraint.</span></span>  

<span data-ttu-id="b335f-151">系统定义的表约束通过以下方式定义：选择要用作引用的表，然后从此表中选择用于在约束中形成列的字段。</span><span class="sxs-lookup"><span data-stu-id="b335f-151">A system-defined table constraint is defined by selecting which table to use as a reference and then selecting fields from this table to form the columns in the constraint.</span></span> <span data-ttu-id="b335f-152">表约束的行是在配置时呈现的 Supply Chain Management 表的行。</span><span class="sxs-lookup"><span data-stu-id="b335f-152">The rows of the table constraint are the rows of the Supply Chain Management table that are present at configuration time.</span></span>  

<span data-ttu-id="b335f-153">可通过引用表约束定义并将模型中的相关属性映射到表约束中的列来将表约束包含在产品配置模型中。</span><span class="sxs-lookup"><span data-stu-id="b335f-153">A table constraint is included in a product configuration model by referencing the table constraint definition and mapping the relevant attributes in the model to the columns in the table constraint.</span></span>

### <a name="calculations"></a><span data-ttu-id="b335f-154">计算</span><span class="sxs-lookup"><span data-stu-id="b335f-154">Calculations</span></span>

<span data-ttu-id="b335f-155">计算表示用于在配置模型中执行算术运算的机制。</span><span class="sxs-lookup"><span data-stu-id="b335f-155">Calculations represent a mechanism for performing arithmetic operations in a configuration model.</span></span> <span data-ttu-id="b335f-156">例如，计算可确定某件特定原材料的长度或抛光工序的处理时间。</span><span class="sxs-lookup"><span data-stu-id="b335f-156">For example, a calculation can determine the length of a specific piece of raw material or the processing time for a polishing operation.</span></span> <span data-ttu-id="b335f-157">计算是必不可少的，请在包含在计算表达式中的所有属性值都变得可用后为目标属性设置值。</span><span class="sxs-lookup"><span data-stu-id="b335f-157">Calculations are imperative and set the value for a target attribute after all the attribute values that are included in the calculation expression become available.</span></span>

### <a name="subcomponents"></a><span data-ttu-id="b335f-158">子组件</span><span class="sxs-lookup"><span data-stu-id="b335f-158">Subcomponents</span></span>

<span data-ttu-id="b335f-159">子组件表示产品配置模型结构中的节点。</span><span class="sxs-lookup"><span data-stu-id="b335f-159">Subcomponents represent the nodes in the product configuration model structure.</span></span> <span data-ttu-id="b335f-160">对于每个子组件关系，必须指定一个引用，该引用针对的是将变型配置技术设置为基于约束的配置的基础产品。</span><span class="sxs-lookup"><span data-stu-id="b335f-160">For each subcomponent relationship, a reference must be specified to a product master that has the variant configuration technology set to constraint-based configuration.</span></span>

### <a name="user-requirements"></a><span data-ttu-id="b335f-161">用户要求</span><span class="sxs-lookup"><span data-stu-id="b335f-161">User requirements</span></span>

<span data-ttu-id="b335f-162">用户要求具有子组件的所有要素。</span><span class="sxs-lookup"><span data-stu-id="b335f-162">A user requirement has all the constituents of a subcomponent.</span></span> <span data-ttu-id="b335f-163">两者的唯一差别是用户要求不绑定到基础产品。</span><span class="sxs-lookup"><span data-stu-id="b335f-163">The only difference is that a user requirement isn't bound to a product master.</span></span> <span data-ttu-id="b335f-164">此差别的实际影响是在用户要求的上下文中定义的所有物料清单行或工艺路线工序都将折叠到父组件物料清单结构或工艺路线。</span><span class="sxs-lookup"><span data-stu-id="b335f-164">The practical effect of this difference is that any BOM lines or route operation that are defined in the context of a user requirement are collapsed into the parent component BOM structure or route.</span></span> <span data-ttu-id="b335f-165">此行为类似于虚拟物料清单的行为。</span><span class="sxs-lookup"><span data-stu-id="b335f-165">This behavior resembles the behavior of a phantom BOM.</span></span>

### <a name="bom-lines"></a><span data-ttu-id="b335f-166">物料清单行</span><span class="sxs-lookup"><span data-stu-id="b335f-166">BOM lines</span></span>

<span data-ttu-id="b335f-167">包含物料清单行是为了标识每个组件的制造物料清单。</span><span class="sxs-lookup"><span data-stu-id="b335f-167">BOM lines are included to identify the manufacturing BOM for each component.</span></span> <span data-ttu-id="b335f-168">物料清单行必须引用物料，所有物料属性可设置为固定值或映射到某个属性。</span><span class="sxs-lookup"><span data-stu-id="b335f-168">A BOM line must reference an item, and all item properties can be set to a fixed value or mapped to an attribute.</span></span>

### <a name="route-operations"></a><span data-ttu-id="b335f-169">工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="b335f-169">Route operations</span></span>

<span data-ttu-id="b335f-170">包含工艺路线工序是为了标识制造工艺路线。</span><span class="sxs-lookup"><span data-stu-id="b335f-170">Route operations are included to identify the manufacturing route.</span></span> <span data-ttu-id="b335f-171">工艺路线工序必须引用已定义的操作，所有操作属性可设置为固定值。</span><span class="sxs-lookup"><span data-stu-id="b335f-171">A route operation must reference a defined operation, and all operation properties can be set to a fixed value.</span></span> <span data-ttu-id="b335f-172">除资源需求之外的所有属性均可映射到某个属性（而不是值）。</span><span class="sxs-lookup"><span data-stu-id="b335f-172">All properties except resource requirements can be mapped to an attribute instead of a value.</span></span>

## <a name="validating-and-testing-a-product-configuration-model"></a><span data-ttu-id="b335f-173">验证和测试产品配置模型</span><span class="sxs-lookup"><span data-stu-id="b335f-173">Validating and testing a product configuration model</span></span>
<span data-ttu-id="b335f-174">产品配置模型的验证可在模型内的几个级别进行，因此可覆盖不同的范围。</span><span class="sxs-lookup"><span data-stu-id="b335f-174">Validation of a product configuration model can occur on several levels in the model and can therefore cover various scopes.</span></span> <span data-ttu-id="b335f-175">最低级别针对单个表达式约束。</span><span class="sxs-lookup"><span data-stu-id="b335f-175">The lowest level is for a single expression constraint.</span></span> <span data-ttu-id="b335f-176">在这种情况下，验证通常由产品设计人员执行，旨在确认表达式的语法的正确性。</span><span class="sxs-lookup"><span data-stu-id="b335f-176">In this case, validation is typically performed by the product designer to verify that the syntax of an expression is correct.</span></span>  

<span data-ttu-id="b335f-177">同样，物料清单行的条件或者工艺路线工序可以孤立地验证。</span><span class="sxs-lookup"><span data-stu-id="b335f-177">Similarly, a condition for a BOM line or a route operation can be validated in isolation.</span></span>  

<span data-ttu-id="b335f-178">验证还可对用户确定的表约束定义执行。</span><span class="sxs-lookup"><span data-stu-id="b335f-178">Validation can also be done for a user-defined table constraint definition.</span></span> <span data-ttu-id="b335f-179">在这种情况下，用户可验证为每个字段输入的值是否位于对应的属性类型的域内。</span><span class="sxs-lookup"><span data-stu-id="b335f-179">In this case, the user can verify that the values that are entered for each field are inside the domain of the corresponding attribute types.</span></span>  

<span data-ttu-id="b335f-180">最后，验证可对整个产品配置模型执行，以确认整个语法是否正确以及是否遵守了所有命名和建模约定。</span><span class="sxs-lookup"><span data-stu-id="b335f-180">Finally, validation can be done for a complete product configuration model to verify that the complete syntax is correct, and that all naming and modeling conventions have been respected.</span></span>

### <a name="testing"></a><span data-ttu-id="b335f-181">正在测试</span><span class="sxs-lookup"><span data-stu-id="b335f-181">Testing</span></span>

<span data-ttu-id="b335f-182">测试模型类似于运行实际配置会话。</span><span class="sxs-lookup"><span data-stu-id="b335f-182">Testing a model is similar to running an actual configuration session.</span></span> <span data-ttu-id="b335f-183">用户可浏览配置页面并验证模型结构是否支持配置流程。</span><span class="sxs-lookup"><span data-stu-id="b335f-183">The user can walk through the configuration pages and verify that the model structure supports the configuration process.</span></span> <span data-ttu-id="b335f-184">用户可验证属性值是否正确，以及属性描述是否指导用户选择了正确的值。</span><span class="sxs-lookup"><span data-stu-id="b335f-184">The user can verify that the attribute values are correct, and that the attribute descriptions guide the user to select the correct values.</span></span> <span data-ttu-id="b335f-185">最后，在测试会话完成后，系统将尝试创建对应于所选属性值的物料清单和工艺路线，并在出现任何问题时显示错误消息。</span><span class="sxs-lookup"><span data-stu-id="b335f-185">Finally, after a test session is completed, the system tries to create the BOM and the route that corresponds to the selected attribute values, and presents an error message if anything goes wrong.</span></span>

### <a name="the-configuration-page"></a><span data-ttu-id="b335f-186">管理页面</span><span class="sxs-lookup"><span data-stu-id="b335f-186">The configuration page</span></span>

<span data-ttu-id="b335f-187">要在组件之间导航，请单击 **下一个** 或单击产品配置模型树中的组件以将焦点设置在其上。</span><span class="sxs-lookup"><span data-stu-id="b335f-187">To navigate between components, click **Next**, or click a component in the product configuration model tree to set focus on it.</span></span>

## <a name="finalizing-a-model-for-configuration"></a><span data-ttu-id="b335f-188">为配置完成模型</span><span class="sxs-lookup"><span data-stu-id="b335f-188">Finalizing a model for configuration</span></span>
<span data-ttu-id="b335f-189">当产品配置模型已准备好在配置到订购方案中使用时，必须创建一个版本。</span><span class="sxs-lookup"><span data-stu-id="b335f-189">When a product configuration model is ready to be used in configure-to-order scenarios, a version must be created.</span></span> <span data-ttu-id="b335f-190">但是，有几个可改善建模经验的选项。</span><span class="sxs-lookup"><span data-stu-id="b335f-190">However, there are several options that can enhance the modeling experience.</span></span>

### <a name="user-interface"></a><span data-ttu-id="b335f-191">用户界面</span><span class="sxs-lookup"><span data-stu-id="b335f-191">User interface</span></span>

<span data-ttu-id="b335f-192">配置 UI 可通过在一个或多个子组件中引入属性组来修改。</span><span class="sxs-lookup"><span data-stu-id="b335f-192">The configuration UI can be modified by introducing attribute groups in one or more subcomponents.</span></span> <span data-ttu-id="b335f-193">此类分组可突出显示特定属性之间的关系并帮助配置用户识别焦点当前在产品中的区域。</span><span class="sxs-lookup"><span data-stu-id="b335f-193">Such a grouping can highlight the relationships between specific attributes and help the configuration user identify the area of the product that is currently in focus.</span></span>

### <a name="templates"></a><span data-ttu-id="b335f-194">模板</span><span class="sxs-lookup"><span data-stu-id="b335f-194">Templates</span></span>

<span data-ttu-id="b335f-195">可创建一个或多个配置模板以加快配置流程。</span><span class="sxs-lookup"><span data-stu-id="b335f-195">One or more configuration templates can be created to speed up the configuration process.</span></span> <span data-ttu-id="b335f-196">或者，也可以创建模板以推销特定属性组合，例如在销售市场活动侧重于一组特定的产品功能时。</span><span class="sxs-lookup"><span data-stu-id="b335f-196">Alternatively, templates can be created to promote specific attribute combinations, such as when a sales campaign focuses on a specific set of product features.</span></span>

### <a name="translations"></a><span data-ttu-id="b335f-197">翻译</span><span class="sxs-lookup"><span data-stu-id="b335f-197">Translations</span></span>

<span data-ttu-id="b335f-198">如果产品将不同的国家/地区销售，则可以为显示在配置 UI 中的所有文本创建翻译。</span><span class="sxs-lookup"><span data-stu-id="b335f-198">If the product will be sold in different countries/regions, translations can be created for all text that appears in the configuration UI.</span></span> <span data-ttu-id="b335f-199">此文本不仅包含名称和描述字段，还包含属性文本值。</span><span class="sxs-lookup"><span data-stu-id="b335f-199">This text includes not only name and description fields, but also attribute text values.</span></span>

### <a name="versions"></a><span data-ttu-id="b335f-200">版本</span><span class="sxs-lookup"><span data-stu-id="b335f-200">Versions</span></span>

<span data-ttu-id="b335f-201">最终流程中的最后一个，也是最重要的一个步骤是为产品配置模型创建一个版本。</span><span class="sxs-lookup"><span data-stu-id="b335f-201">The last and most important step in the finalization process is to create a version for the product configuration model.</span></span> <span data-ttu-id="b335f-202">该版本表示基础产品之间的关系，您可为订单或报价单行上的配置选择该版本，也可为产品配置模型选择该版本。</span><span class="sxs-lookup"><span data-stu-id="b335f-202">The version represents the relationship between the product master, which can be selected for configuration on an order or quotation line, and the product configuration model.</span></span> <span data-ttu-id="b335f-203">版本必须经过审核和启用才能在配置会话中使用。</span><span class="sxs-lookup"><span data-stu-id="b335f-203">A version must be approved and activated before it can be used in a configuration session.</span></span>

## <a name="extending-a-product-configuration-model-through-the-api"></a><span data-ttu-id="b335f-204">通过 API 扩展产品配置模型</span><span class="sxs-lookup"><span data-stu-id="b335f-204">Extending a product configuration model through the API</span></span>
<span data-ttu-id="b335f-205">已实施专门的应用程序编程接口 (API)，以便让合作伙伴和具有开发人员许可证的其他人员扩展产品配置模型的功能。</span><span class="sxs-lookup"><span data-stu-id="b335f-205">A dedicated application programming interface (API) has been implemented, so that partners and others who have a developer license can extend the capabilities of a product configuration model.</span></span> <span data-ttu-id="b335f-206">这样做的主要目的是建立一个机制，让使用现有产品生成器的合作伙伴和客户将在产品生成器模型中嵌入的代码迁移到 API。</span><span class="sxs-lookup"><span data-stu-id="b335f-206">The main goal has been to establish a mechanism that lets partners and customers who use the existing Product Builder migrate the code that is embedded in Product Builder models to the API.</span></span> <span data-ttu-id="b335f-207">这样，他们就可以将其模型从产品生成器迁移到产品配置。</span><span class="sxs-lookup"><span data-stu-id="b335f-207">In this way, they can migrate their models from Product Builder to a product configuration.</span></span> <span data-ttu-id="b335f-208">但是，新合作伙伴和客户还可能受益于使用 API 扩展新产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b335f-208">However, new partners and customers can also benefit from using the API to extend new product configuration models.</span></span>

### <a name="pcadaptor-class"></a><span data-ttu-id="b335f-209">PCAdaptor 类</span><span class="sxs-lookup"><span data-stu-id="b335f-209">PCAdaptor class</span></span>

<span data-ttu-id="b335f-210">API 是使用一组 **PCAdaptor** 类实施的，这些类可公开产品配置模型的数据结构。</span><span class="sxs-lookup"><span data-stu-id="b335f-210">The API is implemented by using a set of **PCAdaptor** classes that expose the data structure of the product configuration models.</span></span> <span data-ttu-id="b335f-211">必须为将扩展的每个模型创建 **PCAdaptor** 类的实例。</span><span class="sxs-lookup"><span data-stu-id="b335f-211">An instance of the **PCAdaptor** class must be created for each model that will be extended.</span></span> <span data-ttu-id="b335f-212">在配置会话完成后，系统将检查是否有此类的实例并在发现该实例后运行它。</span><span class="sxs-lookup"><span data-stu-id="b335f-212">After a configuration session is completed, the system checks for an instance of this class and runs it if it's found.</span></span>  

<span data-ttu-id="b335f-213">以下流程图概览了该流程。</span><span class="sxs-lookup"><span data-stu-id="b335f-213">The following flow diagram outlines the process.</span></span>  

<span data-ttu-id="b335f-214">[![流程图](./media/product_configuration_2.png)](./media/product_configuration_2.png)</span><span class="sxs-lookup"><span data-stu-id="b335f-214">[![Flow diagram](./media/product_configuration_2.png)](./media/product_configuration_2.png)</span></span>  

<span data-ttu-id="b335f-215">产品配置 API 流程图</span><span class="sxs-lookup"><span data-stu-id="b335f-215">Product configuration API flow diagram</span></span>

## <a name="product-configuration"></a><span data-ttu-id="b335f-216">产品配置</span><span class="sxs-lookup"><span data-stu-id="b335f-216">Product configuration</span></span>
<span data-ttu-id="b335f-217">产品配置可从以下位置执行：</span><span class="sxs-lookup"><span data-stu-id="b335f-217">Product configuration can be performed from the following places:</span></span>

-   <span data-ttu-id="b335f-218">销售订单行</span><span class="sxs-lookup"><span data-stu-id="b335f-218">Sales order line</span></span>
-   <span data-ttu-id="b335f-219">销售报价单行</span><span class="sxs-lookup"><span data-stu-id="b335f-219">Sales quotation line</span></span>
-   <span data-ttu-id="b335f-220">采购订单行</span><span class="sxs-lookup"><span data-stu-id="b335f-220">Purchase order line</span></span>
-   <span data-ttu-id="b335f-221">生产订单行</span><span class="sxs-lookup"><span data-stu-id="b335f-221">Production order line</span></span>
-   <span data-ttu-id="b335f-222">物料需求行（项目）</span><span class="sxs-lookup"><span data-stu-id="b335f-222">Item requirement line (project)</span></span>

<span data-ttu-id="b335f-223">配置的目的是打造满足用户要求的产品的不同变型。</span><span class="sxs-lookup"><span data-stu-id="b335f-223">The purpose of the configuration is to create a distinct variant of the product that meets the customer’s requirement.</span></span> <span data-ttu-id="b335f-224">将为每个新配置创建一个唯一配置 ID。</span><span class="sxs-lookup"><span data-stu-id="b335f-224">A unique configuration ID is created for each new configuration.</span></span> <span data-ttu-id="b335f-225">此 ID 通过库存启用跟踪。</span><span class="sxs-lookup"><span data-stu-id="b335f-225">This ID enables tracking through inventory.</span></span>

### <a name="multiple-sites-and-intercompany"></a><span data-ttu-id="b335f-226">多个站点和内部公司</span><span class="sxs-lookup"><span data-stu-id="b335f-226">Multiple sites and intercompany</span></span>

<span data-ttu-id="b335f-227">如果将对站点或者甚至是公司（不同于进行生产的站点或公司）执行配置，则会为供应公司内的供应商站点创建物料清单和工艺路线。</span><span class="sxs-lookup"><span data-stu-id="b335f-227">If configuration will be done at a site, or even a company, that differs from the site or company where production will occur, the BOM and the route will be created for and put at the supplier site in the supplying company.</span></span> <span data-ttu-id="b335f-228">产品变型将在参与供应链的所有公司中发布。</span><span class="sxs-lookup"><span data-stu-id="b335f-228">The product variant will be released in all companies that participate in the supply chain.</span></span>



