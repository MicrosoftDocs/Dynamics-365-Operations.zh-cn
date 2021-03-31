---
title: 基于约束的产品配置的基于属性的销售价
description: 本主题描述了如何使用基于组件和属性，而不是物理物料清单和工艺路线的销售价构建销售价模型。
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65ab96c71fa44d6acad0bcb5cd7a65321109b93d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221959"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a><span data-ttu-id="b3957-103">基于约束的产品配置的基于属性的销售价</span><span class="sxs-lookup"><span data-stu-id="b3957-103">Attribute-based sales prices for constraint-based product configuration</span></span>

<span data-ttu-id="b3957-104">本主题描述了如何使用基于组件和属性，而不是物理物料清单和工艺路线的销售价构建销售价模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-104">This topic describes how to build sales price models with sales prices based on components and attributes rather than on the physical bill of material and the route.</span></span> <span data-ttu-id="b3957-105">您可以为每个产品配置模型构建多个销售价模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-105">You can build several sales price models for each product configuration model.</span></span>

## <a name="set-relevant-product-information-management-parameters"></a><span data-ttu-id="b3957-106">设置相关的产品信息管理参数</span><span class="sxs-lookup"><span data-stu-id="b3957-106">Set relevant product information management parameters</span></span>

<span data-ttu-id="b3957-107">在开始构建价格模型之前，您必须定义一个默认货币，以供在构建销售价模型时使用。</span><span class="sxs-lookup"><span data-stu-id="b3957-107">Before you start building your price models, you must define a default currency, which is used when you build your sales price models.</span></span> <span data-ttu-id="b3957-108">您还可以选择是否附加一个 Microsoft Excel 文件，其中包含所有订单或报价行的价格明细。</span><span class="sxs-lookup"><span data-stu-id="b3957-108">You can also choose whether to attach a Microsoft Excel file with a price breakdown for all order or quotation lines.</span></span> <span data-ttu-id="b3957-109">价格明细使您能够与客户共享有关如何达成配置产品的特定销售价的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b3957-109">The price breakdown will enable you to share details with customers about how you arrived at a specific sales price for a configured product.</span></span>

<span data-ttu-id="b3957-110">若要设置默认货币：</span><span class="sxs-lookup"><span data-stu-id="b3957-110">To set your default currency:</span></span>

1. <span data-ttu-id="b3957-111">转到 **产品信息管理 \> 设置 \> 产品信息管理参数**。</span><span class="sxs-lookup"><span data-stu-id="b3957-111">Go to  **Product information management \> Setup \> Product information management parameters**.</span></span>
1. <span data-ttu-id="b3957-112">打开 **基于约束的产品配置模型** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="b3957-112">Open the **Constraint-Based product configuration models** tab.</span></span>
1. <span data-ttu-id="b3957-113">打开 **默认货币** 下拉列表，然后选择您的货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-113">Open the **Default currency** drop-down list and select your currency.</span></span>

    <span data-ttu-id="b3957-114">![为基于约束的产品配置设置默认货币](media/prod-config-currency.png "为基于约束的产品配置设置默认货币")</span><span class="sxs-lookup"><span data-stu-id="b3957-114">![Set the default currency for constraint-based product configuration](media/prod-config-currency.png "Set the default currency for constraint-based product configuration")</span></span>

1. <span data-ttu-id="b3957-115">如果您想附加一个包含所有订单或报价行的价格明细的 Excel 文件，请在 **价格模型** 部分中，将 **附加** 设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b3957-115">If you'd like to attach an Excel file with a price breakdown for all order or quotation lines, then in the **Price model** section, set **Attach** to *Yes*.</span></span>

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a><span data-ttu-id="b3957-116">构建您的销售价模型</span><span class="sxs-lookup"><span data-stu-id="b3957-116">Build your sales price models</span></span>

<span data-ttu-id="b3957-117">若要构建销售价模型：</span><span class="sxs-lookup"><span data-stu-id="b3957-117">To build a sales price model:</span></span>

1. <span data-ttu-id="b3957-118">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="b3957-118">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b3957-119">选择目标产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-119">Select the target product configuration model.</span></span>
1. <span data-ttu-id="b3957-120">在“操作”窗格上，打开 **模型** 选项卡，然后从 **设置** 组中，选择 **价格模型**。</span><span class="sxs-lookup"><span data-stu-id="b3957-120">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price models**.</span></span>
1. <span data-ttu-id="b3957-121">**价格模型** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="b3957-121">The **Price models** page opens.</span></span>
1. <span data-ttu-id="b3957-122">选择一个价格模型或向网格中添加一个新模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-122">Select a price model or add a new one to the grid.</span></span>
1. <span data-ttu-id="b3957-123">选择 **编辑** 以打开所选模型的编辑页面，该页面将提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="b3957-123">Select **Edit** to open the edit page for your selected model, which provides the following features:</span></span>
    - <span data-ttu-id="b3957-124">表格的标题显示默认货币，您可以在价格设置中添加新货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-124">The header of the form shows the default currency and lets you add new currencies for your price setup.</span></span>
    - <span data-ttu-id="b3957-125">左侧窗格显示了产品模型的所有组件和用户要求。</span><span class="sxs-lookup"><span data-stu-id="b3957-125">The left pane shows all the components and user requirements of the product model.</span></span> <span data-ttu-id="b3957-126">产品模型树中的每个节点都可以具有一个基价表达式和可选数量的表达式规则。</span><span class="sxs-lookup"><span data-stu-id="b3957-126">Each node in the product model tree can have one base-price expression and an optional number of expression rules.</span></span> <span data-ttu-id="b3957-127">表达式规则由条件和表达式组成，每个表达式规则都包含一个有助于控制产品价格的产品选项。</span><span class="sxs-lookup"><span data-stu-id="b3957-127">An expression rule consists of a condition and an expression and each expression rule covers a product option that helps control the price of the product.</span></span>
    - <span data-ttu-id="b3957-128">当您构建条件和表达式时，可以使用与产品模型中的计算相同的运算符。</span><span class="sxs-lookup"><span data-stu-id="b3957-128">When you build your conditions and expressions, you have the same operators available as for calculations in a product model.</span></span> <span data-ttu-id="b3957-129">表达式编辑器还支持条件和表达式。</span><span class="sxs-lookup"><span data-stu-id="b3957-129">The expression editor also supports both conditions and expressions.</span></span>
1. <span data-ttu-id="b3957-130">在左列中选择一个节点，然后使用上一步中描述的功能为其建立定价规则（另请参阅此过程之后提供的示例）。</span><span class="sxs-lookup"><span data-stu-id="b3957-130">Select a node in the left column and then use the features described in the previous step to establish pricing rules for it (see also the example provided after this procedure).</span></span> <span data-ttu-id="b3957-131">根据需要为每个节点重复此步骤。</span><span class="sxs-lookup"><span data-stu-id="b3957-131">Repeat this step for each node as needed.</span></span>

<span data-ttu-id="b3957-132">下面的示例显示基价为 899.95 欧元的静态数字，可以根据客户选择的配置，通过以下五个表达式规则中的一个或多个对其进行修改：</span><span class="sxs-lookup"><span data-stu-id="b3957-132">The following example shows a base price of a static number of 899.95 EUR, which can be modified by one or more of the following five expression rules, depending on the configuration selected by the customer:</span></span>

- <span data-ttu-id="b3957-133">对于白色机箱饰面，减去 59.95 欧元。</span><span class="sxs-lookup"><span data-stu-id="b3957-133">For white cabinet finish, subtract 59.95 EUR.</span></span>
- <span data-ttu-id="b3957-134">对于转角保护，增加 35.95 欧元。</span><span class="sxs-lookup"><span data-stu-id="b3957-134">For corner protection, add 35.95 EUR.</span></span>
- <span data-ttu-id="b3957-135">对于正面金属格栅，增加 89.95 欧元。</span><span class="sxs-lookup"><span data-stu-id="b3957-135">For a metal front grill, add 89.95 EUR.</span></span>
- <span data-ttu-id="b3957-136">对于红木机箱饰面，增加 119.95 欧元。</span><span class="sxs-lookup"><span data-stu-id="b3957-136">For rosewood cabinet finish, add 119.95 EUR.</span></span>
- <span data-ttu-id="b3957-137">对于每单元扬声器高度，增加 12.95 欧元。</span><span class="sxs-lookup"><span data-stu-id="b3957-137">Add 12.95 EUR for each unit of speaker height.</span></span>

<span data-ttu-id="b3957-138">![价格模型示例](media/prod-config-rules-example.png "价格模型示例")</span><span class="sxs-lookup"><span data-stu-id="b3957-138">![Example price model](media/prod-config-rules-example.png "Example price model")</span></span>

## <a name="add-support-for-multiple-currencies"></a><span data-ttu-id="b3957-139">添加对多种货币的支持</span><span class="sxs-lookup"><span data-stu-id="b3957-139">Add support for multiple currencies</span></span>

<span data-ttu-id="b3957-140">当销售可配置产品时，系统检查是否已明确以客户的货币设置价格。</span><span class="sxs-lookup"><span data-stu-id="b3957-140">When a configurable product is sold, the system checks whether the prices have been set explicitly in the currency of the customer.</span></span> <span data-ttu-id="b3957-141">如果是，则使用显式值。</span><span class="sxs-lookup"><span data-stu-id="b3957-141">If so, the explicit values are used.</span></span> <span data-ttu-id="b3957-142">如果不是，系统将使用为销售公司建立的货币汇率，将默认货币值转换为客户的货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-142">If not, the system uses the currency exchange rates established for the sales company to convert the default currency value to the customer's currency.</span></span>

<span data-ttu-id="b3957-143">若要使用其他货币添加显式价格：</span><span class="sxs-lookup"><span data-stu-id="b3957-143">To add explicit prices in an additional currency:</span></span>

1. <span data-ttu-id="b3957-144">打开价格模型的编辑页面，如[构建您的销售价模型](#build-price-model)中所述。</span><span class="sxs-lookup"><span data-stu-id="b3957-144">Open the edit page for your price model, as described in [Build your sales price models](#build-price-model).</span></span>
1. <span data-ttu-id="b3957-145">选择价格模型标题中的 **添加** 按钮以打开 **货币** 下拉对话框，其中列出了可用的货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-145">Select the **Add** button in the header of the price model to open the **Currencies** drop-down dialog box, which lists the available currencies.</span></span>
1. <span data-ttu-id="b3957-146">在 **货币** 下拉对话框中选择要添加的货币，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b3957-146">Select the currency you want to add in the **Currencies** drop-down dialog box and then select **OK**.</span></span>
1. <span data-ttu-id="b3957-147">现在，**当前货币** 下拉列表中包括您刚刚添加的货币，以及之前可能已添加的任何其他货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-147">The **Current currency** drop-down list now includes the currency that you just added, plus any other currencies that may have been added previously.</span></span> <span data-ttu-id="b3957-148">选择您的新货币，并注意 **表达式规则** 部分中的网格现在包括两个表达式字段：</span><span class="sxs-lookup"><span data-stu-id="b3957-148">Select your new currency and notice that the grid in the **Expression rules** section now includes two expression fields:</span></span>
    - <span data-ttu-id="b3957-149">**表达式** - 显示用于使用当前在 **当前货币** 中选择的货币查找价格的表达式（或常数值）。</span><span class="sxs-lookup"><span data-stu-id="b3957-149">**Expression** - Shows the expression (or constant value) for finding the price using the currency currently selected for **Current currency**.</span></span>
    - <span data-ttu-id="b3957-150">**默认表达式** - 显示用于使用当前的默认货币（显示在 **默认货币** 字段中）查找价格的表示式（或常数值）。</span><span class="sxs-lookup"><span data-stu-id="b3957-150">**Default expressions** - Shows the expression (or constant value) for finding the price using the default currently (shown in the **Default currency** field).</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3957-151">表达式规则的 **条件** 字段“只适用于”默认货币，这意味着您无法修改其他货币的条件。</span><span class="sxs-lookup"><span data-stu-id="b3957-151">The **Condition** field for the expression rules is "owned" by the default currency, which means that you can't modify the condition for other currencies.</span></span> <span data-ttu-id="b3957-152">当选择默认货币以外的货币作为 **当前货币** 时，也无法添加新的表达式规则。</span><span class="sxs-lookup"><span data-stu-id="b3957-152">You also can't add new expression rules while a currency other than the default currency is selected as the **Current currency**.</span></span>
1. <span data-ttu-id="b3957-153">针对当前货币，根据需要在 **表达式** 列中编辑值。</span><span class="sxs-lookup"><span data-stu-id="b3957-153">Edit values in the **Expression** column as needed for the current currency.</span></span>

<span data-ttu-id="b3957-154">在下面的示例中，_欧元_ 是默认货币，_美元_ 已添加为其他货币。</span><span class="sxs-lookup"><span data-stu-id="b3957-154">In the example below, _EUR_ is the default currency, and _USD_ has been added as an additional currency.</span></span>

<span data-ttu-id="b3957-155">![具有多种货币的模型示例](media/prod-config-rules-currency-example.png "具有多种货币的模型示例")</span><span class="sxs-lookup"><span data-stu-id="b3957-155">![Example of a model with multiple currencies](media/prod-config-rules-currency-example.png "Example of a model with multiple currencies")</span></span>

> [!NOTE]
> <span data-ttu-id="b3957-156">您不能添加唯一用于非默认货币的表达式规则。</span><span class="sxs-lookup"><span data-stu-id="b3957-156">You can't add expression rules that are unique for a non-default currency.</span></span> <span data-ttu-id="b3957-157">若要创建仅与默认货币以外的其他货币相关的表达式规则，请将默认货币的价格表达式设置为零。</span><span class="sxs-lookup"><span data-stu-id="b3957-157">To create expression rules that would be relevant only for a currency other than the default currency, set the price expression for the default currency to zero.</span></span> <span data-ttu-id="b3957-158">然后，为非默认货币设置适当的表达式。</span><span class="sxs-lookup"><span data-stu-id="b3957-158">Then set the appropriate expression for the non-default currency.</span></span>

## <a name="test-your-price-model"></a><span data-ttu-id="b3957-159">测试您的价格模型</span><span class="sxs-lookup"><span data-stu-id="b3957-159">Test your price model</span></span>

<span data-ttu-id="b3957-160">若要测试销售价在配置会话中的工作方式，请打开价格模型的编辑页面（如 [构建您的销售价模型](#build-price-model)中所述），然后在“操作”窗格中选择 **测试**。</span><span class="sxs-lookup"><span data-stu-id="b3957-160">To test how the sales prices work in a configuration session, open the edit page for your price model, as described in [Build your sales price models](#build-price-model) and then select  **Test** on the Action Pane.</span></span> <span data-ttu-id="b3957-161">**测试产品模型** 对话框将打开，您可以在其中执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="b3957-161">The **Test product model** dialog box opens, where you can do the following:</span></span>

- <span data-ttu-id="b3957-162">使用此处提供的配置设置选择产品选项，然后查看它们如何影响 **价格和装运日期** 中显示的值。</span><span class="sxs-lookup"><span data-stu-id="b3957-162">Use the configuration settings offered here to select product options and then see how they affect the value shown for **Price and ship date**.</span></span>
- <span data-ttu-id="b3957-163">选择 **查看价格明细** 以下载一个 Excel 文档，该文档显示了有关如何计算价格的完整详细信息。</span><span class="sxs-lookup"><span data-stu-id="b3957-163">Select **View price breakdown** to download an Excel document that shows full details about how the price was calculated.</span></span>

<span data-ttu-id="b3957-164">![测试您的产品模型](media/prod-config-test.png "测试您的产品模型")</span><span class="sxs-lookup"><span data-stu-id="b3957-164">![Test your product model](media/prod-config-test.png "Test your product model")</span></span>

<span data-ttu-id="b3957-165">下载的电子表格将每个有效价格元素的绝对值和贡献都显示为百分比。</span><span class="sxs-lookup"><span data-stu-id="b3957-165">The downloaded spreadsheet shows both the absolute value and the contribution as a percentage for each active price element.</span></span> <span data-ttu-id="b3957-166">如果在 **产品信息管理参数** 页面上设置 **附加** 价格模型选项，此 Excel 工作表将附加到订单或报价行。</span><span class="sxs-lookup"><span data-stu-id="b3957-166">If you have set the **Attach** price model option on the **Product information management parameters** page, this Excel sheet gets attached to the order or quotation line.</span></span>

<span data-ttu-id="b3957-167">![显示价格明细的 Excel 电子表格](media/prod-config-excel-example.png "显示价格明细的 Excel 电子表格")</span><span class="sxs-lookup"><span data-stu-id="b3957-167">![Excel spreadsheet showing price breakdown](media/prod-config-excel-example.png "Excel spreadsheet showing price breakdown")</span></span>

## <a name="set-up-selection-criteria-for-price-models"></a><span data-ttu-id="b3957-168">设置价格模型的选择标准</span><span class="sxs-lookup"><span data-stu-id="b3957-168">Set up selection criteria for price models</span></span>

<span data-ttu-id="b3957-169">在价格模型完成设置后，当配置报价或订单时，必须建立至少一个选择标准以选择价格模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-169">When your price models are in place, you must establish at least one selection criterion to pick up the price model when you configure to quote or to order.</span></span> <span data-ttu-id="b3957-170">您可以通过设置一个或多个查询来实现此操作。</span><span class="sxs-lookup"><span data-stu-id="b3957-170">You'll do this by setting up one or more queries.</span></span> <span data-ttu-id="b3957-171">通过与匹配的销售价模型相结合，这些查询在针对特定客户、地区、期间和其他标准确定销售价时提供了极大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="b3957-171">In a combination with matching sales price models, the queries provide great flexibility in targeting sales prices for particular customers, regions, periods, and other criteria.</span></span>

<span data-ttu-id="b3957-172">若要设置价格模型的选择标准：</span><span class="sxs-lookup"><span data-stu-id="b3957-172">To set up selection criteria for price models:</span></span>

1. <span data-ttu-id="b3957-173">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="b3957-173">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b3957-174">选择目标产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-174">Select the target product configuration model.</span></span>
1. <span data-ttu-id="b3957-175">在“操作”窗格上，打开 **模型** 选项卡，然后从 **设置** 组中，选择 **价格模型标准**。</span><span class="sxs-lookup"><span data-stu-id="b3957-175">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price model criteria**.</span></span> <span data-ttu-id="b3957-176">**价格模型标准** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="b3957-176">The **Price model criteria** page opens.</span></span>
1. <span data-ttu-id="b3957-177">如果所需的查询行还不存在，请在“操作”窗格上选择 **新建**，将新行添加到网格并为其进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="b3957-177">If the query row you need doesn't exist yet, select **New** on the Action Pane to add a new row to the grid and make the following settings for it:</span></span>
    - <span data-ttu-id="b3957-178">**名称** - 为此行输入名称。</span><span class="sxs-lookup"><span data-stu-id="b3957-178">**Name** - Enter a name for this row.</span></span>
    - <span data-ttu-id="b3957-179">**描述** - 简要描述查询及其用途。</span><span class="sxs-lookup"><span data-stu-id="b3957-179">**Description** - Briefly describe the query and what it is for.</span></span>
    - <span data-ttu-id="b3957-180">**价格模型** - 选择一个将在触发时应用查询的[价格模型](#build-price-model)（从当前的配置模型中）。</span><span class="sxs-lookup"><span data-stu-id="b3957-180">**Price model** - Select a [price model](#build-price-model) (from the current configuration model) that the query will apply when triggered.</span></span>
    - <span data-ttu-id="b3957-181">**订单类型** - 选择将应用查询的订单类型。</span><span class="sxs-lookup"><span data-stu-id="b3957-181">**Order type** - Select the type of order where the query will apply.</span></span>
    - <span data-ttu-id="b3957-182">**生效日期** - 指定将应用查询的第一天。</span><span class="sxs-lookup"><span data-stu-id="b3957-182">**Valid from** - Specify the first day when the query will apply.</span></span>
    - <span data-ttu-id="b3957-183">**到期日期** - 指定将应用查询的最后日期。</span><span class="sxs-lookup"><span data-stu-id="b3957-183">**Expire by** - Specify the last date when the query will apply.</span></span>

    <span data-ttu-id="b3957-184">![价格模型条件](media/prod-config-price-model-criteria.png "价格模型条件")</span><span class="sxs-lookup"><span data-stu-id="b3957-184">![Price model criteria](media/prod-config-price-model-criteria.png "Price model criteria")</span></span>

1. <span data-ttu-id="b3957-185">选择要定义的查询的行，然后在 **操作窗格** 上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b3957-185">Select the row for the query you want to define and then select **Edit** on the **Action Pane**.</span></span> <span data-ttu-id="b3957-186">查询设计器对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="b3957-186">The query designer dialog box opens.</span></span> <span data-ttu-id="b3957-187">它的工作方式与 Supply Chain Management 中的大多数查询设计器一样。</span><span class="sxs-lookup"><span data-stu-id="b3957-187">It works like most query designers in Supply Chain Management.</span></span> <span data-ttu-id="b3957-188">使用它来定义应用所选行的价格模型的条件。</span><span class="sxs-lookup"><span data-stu-id="b3957-188">Use it to define the conditions under which the price model for the row you selected should be applied.</span></span>

1. <span data-ttu-id="b3957-189">针对您需要的每个查询重复步骤 4-5。</span><span class="sxs-lookup"><span data-stu-id="b3957-189">Repeat steps 4-5 for each query you require.</span></span>
    > [!TIP]
    > <span data-ttu-id="b3957-190">您可以通过复制与需要添加的新行类似的现有行来节省时间。</span><span class="sxs-lookup"><span data-stu-id="b3957-190">You can save time by copying an existing row that is already similar to a new one that you need to add.</span></span> <span data-ttu-id="b3957-191">若要实现此操作，请选择目标行，然后在“操作”窗格上选择 **重复**。</span><span class="sxs-lookup"><span data-stu-id="b3957-191">To do this, select a target row and then select **Duplicate** on the Action Pane.</span></span>

1. <span data-ttu-id="b3957-192">完成设置条件后，请在 **价格模型标准** 列表中按正确顺序排列它们。</span><span class="sxs-lookup"><span data-stu-id="b3957-192">When you have finished setting up your criteria, arrange them into the proper order in the **Price model criteria** list.</span></span> <span data-ttu-id="b3957-193">若要重新定位一个行，请选择该行，然后在“操作”窗格中选择 **向上** 或 **向下**。</span><span class="sxs-lookup"><span data-stu-id="b3957-193">To reposition a row, select the row and then select **Up** or **Down** on the Action Pane.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b3957-194">在配置时，系统从列表顶部开始搜索，并使用与报价或订单行上的数据匹配的第一个查询。</span><span class="sxs-lookup"><span data-stu-id="b3957-194">At configuration time, the system starts searching from the top of the list and uses the first query that matches the data on the quote or the order line.</span></span> <span data-ttu-id="b3957-195">因此，您必须将最具体的查询放在首位。</span><span class="sxs-lookup"><span data-stu-id="b3957-195">Therefore, you must put your most specific queries on top.</span></span> <span data-ttu-id="b3957-196">如果将常规查询放在列表的顶部，即使在列表的最下方可能有针对配置的确切客户或目标客户的查询，也将使用该查询。</span><span class="sxs-lookup"><span data-stu-id="b3957-196">If you place a general query at the top of the list, this is the one that will be used even though there might be a query further down the list that targets the exact customer or prospect of the configuration.</span></span>

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a><span data-ttu-id="b3957-197">为产品模型版本设置基于属性的销售价</span><span class="sxs-lookup"><span data-stu-id="b3957-197">Set attribute-based sales prices for the product model version</span></span>

<span data-ttu-id="b3957-198">最后一步是为产品模型版本指定基于属性的销售价。</span><span class="sxs-lookup"><span data-stu-id="b3957-198">The final step is to specify attribute-based sales prices for the product model version.</span></span> <span data-ttu-id="b3957-199">若要实现此操作：</span><span class="sxs-lookup"><span data-stu-id="b3957-199">To do this:</span></span>

1. <span data-ttu-id="b3957-200">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="b3957-200">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b3957-201">选择目标产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b3957-201">Select the target product configuration model.</span></span>
1. <span data-ttu-id="b3957-202">在“操作”窗格上，打开 **模型** 选项卡，然后从 **产品模型详细信息** 组中，选择 **版本**。</span><span class="sxs-lookup"><span data-stu-id="b3957-202">On the Action Pane, open the **Model** tab and, from the **Product model details** group, select **Versions**.</span></span>
1. <span data-ttu-id="b3957-203">**版本** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="b3957-203">The **Versions** page opens.</span></span> <span data-ttu-id="b3957-204">确保将 **定价方法** 设置为 **基于属性**。</span><span class="sxs-lookup"><span data-stu-id="b3957-204">Make sure the **Pricing method** is set to **Attribute based**.</span></span>
    <span data-ttu-id="b3957-205">![将定价方法设置为基于属性](media/prod-config-versions.png "将定价方法设置为基于属性")</span><span class="sxs-lookup"><span data-stu-id="b3957-205">![Set the pricing method to attribute based](media/prod-config-versions.png "Set the pricing method to attribute based")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]