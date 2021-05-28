---
title: 工程更改管理常见问题解答
description: 本主题提供对有关工程更改管理功能的常见问题的解答。
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69232eed8520bafeb734ffad43b333bf9e36909e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018677"
---
# <a name="engineering-change-management-faq"></a><span data-ttu-id="1c2c8-103">工程更改管理常见问题解答</span><span class="sxs-lookup"><span data-stu-id="1c2c8-103">Engineering change management FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c2c8-104">本主题提供对有关工程更改管理功能的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-104">This topic provides answers to frequently asked questions about the engineering change management feature.</span></span>

## <a name="should-i-track-the-version-in-transactions"></a><span data-ttu-id="1c2c8-105">我应该在交易中跟踪版本吗？</span><span class="sxs-lookup"><span data-stu-id="1c2c8-105">Should I track the version in transactions?</span></span>

<span data-ttu-id="1c2c8-106">当您创建工程更改类别时，**工程更改类别详细信息** 页将提供一个名为 **在交易中跟踪版本** 的选项。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-106">When you create an engineering change category, the **Engineering change category details** page provides an option that is named **Track version in transactions**.</span></span> <span data-ttu-id="1c2c8-107">这是什么设置，它有什么作用？</span><span class="sxs-lookup"><span data-stu-id="1c2c8-107">What is this setting, and what does it do?</span></span>

- <span data-ttu-id="1c2c8-108">如果您将 **在交易中跟踪版本** 选项设置为 *是*，将筛选 **维度组** 字段，仅显示版本为有效维度的维度组。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-108">If you set the **Track version in transactions** option to *Yes*, the **Dimension group** field will be filtered so that it shows only dimension groups where version is an active dimension.</span></span>
- <span data-ttu-id="1c2c8-109">如果您将 **在交易中跟踪版本** 选项设置为 *否*，将筛选 **维度组** 字段，仅显示版本维度 **不** 是有效维度的维度组。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-109">If you set the **Track version in transactions** option to *No*, the **Dimension group** field will be filtered so that it shows only dimension groups where the version dimension is **not** an active dimension.</span></span>

### <a name="if-you-track-the-version-in-transactions"></a><span data-ttu-id="1c2c8-110">如果您在交易中跟踪版本</span><span class="sxs-lookup"><span data-stu-id="1c2c8-110">If you track the version in transactions</span></span>

<span data-ttu-id="1c2c8-111">对于您选择了版本为有效维度的维度组的工程类别，您将在交易中跟踪该类别产品的版本。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-111">For engineering categories where you've selected a dimension group where version is an active dimension, you will track versions in transactions for products in that category.</span></span> <span data-ttu-id="1c2c8-112">在这种情况下，工程产品将是基础产品，产品的每个版本将是使用版本维度的产品变型。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-112">In this case, the engineering product will be a product master, and each version of the product will be a product variant that uses the version dimension.</span></span> <span data-ttu-id="1c2c8-113">其他维度可以与版本维度一起使用。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-113">Other dimensions can be used together with the version dimension.</span></span>

<span data-ttu-id="1c2c8-114">在这种情况下，每个工程版本在所有流程中都将被视为变型。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-114">In this case, each engineering version will be treated as a variant in all processes.</span></span> <span data-ttu-id="1c2c8-115">因此，如果您在交易中有特定的变型（以便可以确定销售或购买了哪个变型），则必须管理每个版本的存货，主计划将计划每个版本的供应，等等。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-115">Therefore, if you have a specific variant in a transaction (so that you can determine which variant was sold or purchased), you must manage stock for each version, master planning will plan supply for each version, and so on.</span></span> <span data-ttu-id="1c2c8-116">如果您从市场上停用某个版本，则必须手动调整其生效开始日期和生效截止日期，让它们反映更改。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-116">If you retire a version from the market, you must manually adjust its effective-from and effective-to dates so that they reflect the change.</span></span> <span data-ttu-id="1c2c8-117">您还必须管理库存，以确保仓库中没有未使用的物料版本。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-117">You must also manage your inventory to make sure that you don't have unused versions of items in your warehouses.</span></span>

<span data-ttu-id="1c2c8-118">虽然此选项需要进行更多管理工作，但是如果您需要每个交易中使用的特定版本具有较高的可追溯性，我们建议使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-118">Although this option requires more management effort, we recommend it if you require high traceability of the specific versions that are used in each transaction.</span></span>

### <a name="if-you-dont-track-the-version-in-transactions"></a><span data-ttu-id="1c2c8-119">如果您不在交易中跟踪版本</span><span class="sxs-lookup"><span data-stu-id="1c2c8-119">If you don't track the version in transactions</span></span>

<span data-ttu-id="1c2c8-120">对于您选择了版本 **不** 是有效维度的维度组的工程类别，您 **不** 会在交易中跟踪该类别产品的版本。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-120">For engineering categories where you've selected a dimension group where version is **not** an active dimension, you will **not** track versions in transactions for products in that category.</span></span> <span data-ttu-id="1c2c8-121">在这种情况下，如果您不使用任何其他维度，工程产品将是独特产品。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-121">In this case, if you don't use any other dimension, the engineering product will be a distinct product.</span></span> <span data-ttu-id="1c2c8-122">产品仍会版本化，您可以管理有关特定版本的信息（例如，物料清单 \[BOM] 和工艺路线），但无法跟踪每个交易中使用了哪个特定版本。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-122">The product will still be versioned, and you can manage information about specific versions (for example, their bill of materials \[BOM] and route), but you won't be able to trace which specific version was used in each transaction.</span></span> <span data-ttu-id="1c2c8-123">生效开始日期和生效截止日期指示每个版本的有效性。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-123">The effective-from and effective-to dates indicate the validity of each version.</span></span>

<span data-ttu-id="1c2c8-124">此选项更易于管理，因为如果要从一个版本更改为另一个版本，只需按更改顺序进行所需的更改，然后在工程版本中更新生效开始日期和生效截止日期。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-124">This option is much easier to manage, because if you want to change from one version to another, you just have to make the required changes in a change order, and then update the effective-from and effective-to dates in the engineering version.</span></span> <span data-ttu-id="1c2c8-125">然后，生产流程将为产品（及其特定版本）选取所需的物料清单和工艺路线。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-125">The production processes will then pick up the required BOM and route for the product (and its specific version).</span></span>

<span data-ttu-id="1c2c8-126">大多数组织选择此选项，是因为它提供版本和更改管理，而不会增加在每个交易、库存和主计划期间跟踪版本的额外开销。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-126">Most organizations choose this option because it provides version and change management, but it doesn't add the extra overhead of tracking the version in each transaction, in inventory, and during master planning.</span></span>

## <a name="which-fields-are-copied-to-the-released-item-template"></a><span data-ttu-id="1c2c8-127">哪些字段会被复制到已发布物料模板？</span><span class="sxs-lookup"><span data-stu-id="1c2c8-127">Which fields are copied to the released item template?</span></span>

<span data-ttu-id="1c2c8-128">工程公司创建工程产品时，该产品将作为工程公司中的已发布产品创建。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-128">When an engineering company creates an engineering product, that product is created as a released product in the engineering company.</span></span> <span data-ttu-id="1c2c8-129">创建的已发布产品基于所选的 *已发布物料模板*。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-129">The released product that is created is based on the selected *released item template*.</span></span> <span data-ttu-id="1c2c8-130">（已发布物料模板本身是一个现有的已发布产品。）当产品发布到运营公司时，也会使用已发布物料模板。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-130">(The released item template is itself an existing released product.) The released item template is also used when the product is released to an operational company.</span></span> <span data-ttu-id="1c2c8-131">在每种情况下，已发布物料模板会为已发布产品定义大多数字段值，这些值来自关联的 **已发布产品详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-131">In each case, the released item template defines most of the field values for the released product, and those values come from the associated **Released product details** page.</span></span>

<span data-ttu-id="1c2c8-132">下表显示了在这些流程中复制的字段。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-132">The following tables shows the fields that are copied during these processes.</span></span>

| <span data-ttu-id="1c2c8-133">快速选项卡</span><span class="sxs-lookup"><span data-stu-id="1c2c8-133">FastTab</span></span> | <span data-ttu-id="1c2c8-134">在工程公司中创建产品时复制的字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-134">Fields that are copied on product creation in the engineering company</span></span> | <span data-ttu-id="1c2c8-135">发布到运营公司时复制的字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-135">Fields that are copied on release to an operational company</span></span> |
|---|---|---|
| <span data-ttu-id="1c2c8-136">**常规**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-136">**General**</span></span> | <span data-ttu-id="1c2c8-137">**管理** 部分的所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-137">All fields in the **Administration** section</span></span> | <span data-ttu-id="1c2c8-138">为工程公司复制的相同字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-138">The same fields that are copied for the engineering company</span></span> |
| <span data-ttu-id="1c2c8-139">**采购**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-139">**Purchase**</span></span> | <span data-ttu-id="1c2c8-140">所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-140">All fields</span></span> | <span data-ttu-id="1c2c8-141">除 **单位** 外的所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-141">All fields except **Unit**</span></span> |
| <span data-ttu-id="1c2c8-142">**销售**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-142">**Sell**</span></span> | <span data-ttu-id="1c2c8-143">以下部分的所有字段：**销售订单**、**管理**、**纳税**、**价格更新**、**基本销售价**、**费用**、**折扣** 和 **替代产品**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-143">All fields in the following sections: **Sales order**, **Administration**, **Taxation**, **Price update**, **Base sales price**, **Charges**, **Discounts**, and **Alternative product**</span></span> | <span data-ttu-id="1c2c8-144">为工程公司复制的所有相同字段（除 **单位** 外）</span><span class="sxs-lookup"><span data-stu-id="1c2c8-144">All the same fields that are copied for the engineering company, except **Unit**</span></span> |
| <span data-ttu-id="1c2c8-145">**外贸**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-145">**Foreign trade**</span></span> | <span data-ttu-id="1c2c8-146">所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-146">All fields</span></span> | <span data-ttu-id="1c2c8-147">所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-147">All fields</span></span> |
| <span data-ttu-id="1c2c8-148">**管理库存**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-148">**Manage inventory**</span></span> | <span data-ttu-id="1c2c8-149">*除* 了 **物理维度** 和 **实际称重** 外的所有字段和部分</span><span class="sxs-lookup"><span data-stu-id="1c2c8-149">All fields and sections *except* **Physical dimensions** and **Catch weight**</span></span> | <span data-ttu-id="1c2c8-150">为工程公司复制的所有相同字段（除 **单位** 外）</span><span class="sxs-lookup"><span data-stu-id="1c2c8-150">All the same fields that are copied for the engineering company, except **Unit**</span></span> |
| <span data-ttu-id="1c2c8-151">**工程师**、**计划**、**管理成本**、**管理项目**、**财务维度** 和 **仓库**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-151">**Engineer**, **Plan**, **Manage costs**, **Manage projects**, **Financial dimensions**, and **Warehouse**</span></span> | <span data-ttu-id="1c2c8-152">所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-152">All fields</span></span> | <span data-ttu-id="1c2c8-153">除 **物料清单单位** 外的所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-153">All fields except **BOM Unit**</span></span> |
| <span data-ttu-id="1c2c8-154">**产品变型**</span><span class="sxs-lookup"><span data-stu-id="1c2c8-154">**Product variants**</span></span> | <span data-ttu-id="1c2c8-155">**默认产品变型** 部分的所有字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-155">All fields in the **Default product variant** section</span></span> | <span data-ttu-id="1c2c8-156">为工程公司复制的相同字段</span><span class="sxs-lookup"><span data-stu-id="1c2c8-156">The same fields that are copied for the engineering company</span></span> |

<span data-ttu-id="1c2c8-157">除了上表中显示的字段之外，所有默认订单设置都从已发布物料模板复制而来，无论是在工程公司中创建产品还是向运营公司发布产品时。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-157">In addition to the fields that are shown in the previous table, all default order settings are copied from the released item template, both when the product is created in the engineering company and when it's released to an operational company.</span></span> <span data-ttu-id="1c2c8-158">（要查看已发布物料模板的默认订单设置，打开相关的 **已发布产品详细信息** 页，然后在操作窗格上，在 **管理库存** 选项卡上，选择 **默认订单设置**。）</span><span class="sxs-lookup"><span data-stu-id="1c2c8-158">(To view the default order settings for a released item template, open the relevant **Released product details** page, and then, on the Action Pane, on the **Manage inventory** tab, select **Default order settings**.)</span></span>

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a><span data-ttu-id="1c2c8-159">我应该为工程产品创建单独的法人还是应该使用现有法人？</span><span class="sxs-lookup"><span data-stu-id="1c2c8-159">Should I create a separate legal entity for engineering products or use an existing legal entity?</span></span>

<span data-ttu-id="1c2c8-160">您的业务要求确定了您应该为工程产品创建新法人。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-160">Your business requirements determine whether you should create a new legal entity for engineering products.</span></span>

<span data-ttu-id="1c2c8-161">通过创建单独的工程公司，您可以保持工程数据分开，然后根据本地运营公司的需要添加修改。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-161">By creating a separate engineering company, you can keep engineering data separate and then add modifications as they are required for your local operational companies.</span></span> <span data-ttu-id="1c2c8-162">通过这种方式，您可以实现以下目标：</span><span class="sxs-lookup"><span data-stu-id="1c2c8-162">In this way, you can achieve the following goals:</span></span>

- <span data-ttu-id="1c2c8-163">在创建和管理工程产品的地方保留一个单独实体。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-163">Keep a separate entity where the engineering products are created and managed.</span></span>
- <span data-ttu-id="1c2c8-164">在产品准备好发布之前，防止工程产品与其余已发布产品一起出现。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-164">Prevent engineering products from appearing together with the rest of your released products until they are ready and released.</span></span>
- <span data-ttu-id="1c2c8-165">明确区分由工程数据和本地数据决定的数据。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-165">Clearly distinguish data that is dictated by engineering and local data.</span></span>

<span data-ttu-id="1c2c8-166">另一方面，如果满足以下条件，您可能应该将现有法人用作工程公司：</span><span class="sxs-lookup"><span data-stu-id="1c2c8-166">On the other hand, you should probably use an existing legal entity as an engineering company if the following conditions apply to you:</span></span>

- <span data-ttu-id="1c2c8-167">您的系统中只有一个法人，和/或您不需要明确区分所设计的产品。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-167">You have only one legal entity in your system, and/or you don't require a clear separation between products that are being engineered.</span></span>
- <span data-ttu-id="1c2c8-168">您不希望重复某些数据，如资源组、资源、操作和（可能）站点。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-168">You don't want to duplicate some data, such as resource groups, resources, operations, and (perhaps) sites.</span></span>

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a><span data-ttu-id="1c2c8-169">工程版本和变型的命名法是什么？</span><span class="sxs-lookup"><span data-stu-id="1c2c8-169">What is the nomenclature for engineering versions and variants?</span></span>

<span data-ttu-id="1c2c8-170">工程产品和产品变型的命名法采用下列方式：</span><span class="sxs-lookup"><span data-stu-id="1c2c8-170">The nomenclature for engineering products and product variants works in the following way:</span></span>

- <span data-ttu-id="1c2c8-171">对于工程产品（即，如果未使用维度，为独特产品，如果使用了任何维度，则为基础产品），在工程产品类别中定义编号规则命名法。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-171">For the engineering product (that is, the distinct product if no dimensions are used, or the product master if any dimension is used), the number rule nomenclature is defined in the engineering product category.</span></span> <span data-ttu-id="1c2c8-172">在那里，您可以选择使用编号规则、文本常量以及属性名称和值。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-172">There, you have the option to use a number sequence, text constants, and attribute names and values.</span></span>
- <span data-ttu-id="1c2c8-173">对于工程产品的每个变型（如果您的工程产品是基础产品，在您指定维度组的工程产品类别中设置变型），每个变型的编号规则命名法在维度组中定义。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-173">For each variant of an engineering product (if your engineering product is a product master, variants are set up in the engineering product category where you specify the dimension group), the number rule nomenclature for each variant is defined in the dimension group.</span></span> <span data-ttu-id="1c2c8-174">在这种情况下，您可以使用基础产品的产品 ID，以及维度值和名称。</span><span class="sxs-lookup"><span data-stu-id="1c2c8-174">In this case, you can use the product ID of the master, and the dimension values and names.</span></span>