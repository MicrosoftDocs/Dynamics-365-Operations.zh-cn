---
title: 工程更改管理功能演练
description: 本主题提供一个端到端演练，显示如何使用工程更改管理。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 56e868f3050432db8d3b1721da435665f554d90d
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487913"
---
# <a name="engineering-change-management-feature-walkthrough"></a><span data-ttu-id="957dc-103">工程更改管理功能演练</span><span class="sxs-lookup"><span data-stu-id="957dc-103">Engineering change management feature walkthrough</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="957dc-104">本主题提供一个端到端演练，显示如何使用工程更改管理。</span><span class="sxs-lookup"><span data-stu-id="957dc-104">This topic provides an end-to-end walkthrough that shows how to work with engineering change management.</span></span> <span data-ttu-id="957dc-105">它演示了每个最重要的场景：</span><span class="sxs-lookup"><span data-stu-id="957dc-105">It goes through each of the most important scenarios:</span></span>

- <span data-ttu-id="957dc-106">基本功能配置</span><span class="sxs-lookup"><span data-stu-id="957dc-106">Basic feature configuration</span></span>
- <span data-ttu-id="957dc-107">工程公司如何创建新的工程产品</span><span class="sxs-lookup"><span data-stu-id="957dc-107">How an engineering company creates a new engineering product</span></span>
- <span data-ttu-id="957dc-108">工程公司如何向本地公司发布工程产品</span><span class="sxs-lookup"><span data-stu-id="957dc-108">How an engineering company releases an engineering product to a local company</span></span>
- <span data-ttu-id="957dc-109">本地公司如何审查和接受工程公司向其发布的产品</span><span class="sxs-lookup"><span data-stu-id="957dc-109">How a local company can review and accept a product that has been released to it by an engineering company</span></span>
- <span data-ttu-id="957dc-110">本地公司如何在标准交易中使用工程产品</span><span class="sxs-lookup"><span data-stu-id="957dc-110">How a local company can use an engineering product in standard transactions</span></span>
- <span data-ttu-id="957dc-111">如何将工程产品添加到销售订单</span><span class="sxs-lookup"><span data-stu-id="957dc-111">How to add an engineering product to a sales order</span></span>
- <span data-ttu-id="957dc-112">如何通过创建工程更改请求来请求对工程产品的更改</span><span class="sxs-lookup"><span data-stu-id="957dc-112">How to request changes to an engineering product by creating an engineering change request</span></span>
- <span data-ttu-id="957dc-113">如何通过创建工程更改订单来计划和实施请求的更改</span><span class="sxs-lookup"><span data-stu-id="957dc-113">How to schedule and implement requested changes by creating an engineering change order</span></span>
- <span data-ttu-id="957dc-114">如何发布已更改的产品</span><span class="sxs-lookup"><span data-stu-id="957dc-114">How to release a product that has been changed</span></span>

<span data-ttu-id="957dc-115">本主题中的所有练习都使用为 Microsoft Dynamics 365 Supply Chain Management 提供的标准示例数据。</span><span class="sxs-lookup"><span data-stu-id="957dc-115">All the exercises in this topic use the standard sample data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="957dc-116">此外，每个练习都以先前的练习为基础。</span><span class="sxs-lookup"><span data-stu-id="957dc-116">Additionally, each exercise builds on the previous exercise.</span></span> <span data-ttu-id="957dc-117">因此，我们建议您从头到尾依次进行练习，如果您以前从未使用过工程更改管理功能，更应如此。</span><span class="sxs-lookup"><span data-stu-id="957dc-117">Therefore, we recommend that you work through the exercises in order, from beginning to end, especially if you've never used the engineering change management feature before.</span></span> <span data-ttu-id="957dc-118">这样，您将完全了解该功能。</span><span class="sxs-lookup"><span data-stu-id="957dc-118">In this way, you will gain a complete understanding of the feature.</span></span>

## <a name="set-up-for-the-sample-scenario"></a><span data-ttu-id="957dc-119">设置示例场景</span><span class="sxs-lookup"><span data-stu-id="957dc-119">Set up for the sample scenario</span></span>

<span data-ttu-id="957dc-120">若要执行本主题中提供的示例场景，您必须首先通过提供演示数据并添加一些自定义记录来准备功能。</span><span class="sxs-lookup"><span data-stu-id="957dc-120">To follow the sample scenario that is provided in this topic, you must first prepare the feature by making demo data available and adding a few custom records.</span></span>

<span data-ttu-id="957dc-121">在尝试执行本主题其余部分中的任何练习之前，请遵循以下所有子部分中的说明。</span><span class="sxs-lookup"><span data-stu-id="957dc-121">Before you try to do any of the exercises in the rest of this topic, follow the instructions in all the following subsections.</span></span> <span data-ttu-id="957dc-122">这些子部分还介绍了几个重要的设置页面，当您为自己的组织设置工程更改管理时将使用这些页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-122">These subsections also introduce several important settings pages that you will use when you set up engineering change management for your own organization.</span></span>

### <a name="make-standard-demo-data-available"></a><span data-ttu-id="957dc-123">提供标准演示数据</span><span class="sxs-lookup"><span data-stu-id="957dc-123">Make standard demo data available</span></span>

<span data-ttu-id="957dc-124">在[已安装标准演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)的系统上工作。</span><span class="sxs-lookup"><span data-stu-id="957dc-124">Work on a system where the [standard demo data is installed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span></span> <span data-ttu-id="957dc-125">标准演示数据添加几个演示法人（公司和组织）的数据。</span><span class="sxs-lookup"><span data-stu-id="957dc-125">The standard demo data adds data for several demo legal entities (companies and organizations).</span></span> <span data-ttu-id="957dc-126">在进行练习时，您将使用导航栏右侧的公司选择器在设置为 *工程组织* 的一家公司 (*DEMF*) 和设置为 *运营组织* 的另一家公司 (*USMF*) 之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="957dc-126">As you work through the exercises, you will use the company picker on the right side of the navigation bar to switch between one company (*DEMF*) that is set up as an *engineering organization* and another company (*USMF*) that is set up as an *operational organization*.</span></span>

### <a name="set-up-an-engineering-organization"></a><span data-ttu-id="957dc-127">设置工程组织</span><span class="sxs-lookup"><span data-stu-id="957dc-127">Set up an engineering organization</span></span>

<span data-ttu-id="957dc-128">工程组织拥有工程数据，并负责产品设计和产品更改。</span><span class="sxs-lookup"><span data-stu-id="957dc-128">An engineering organization owns the engineering data, and is responsible for product design and product changes.</span></span> <span data-ttu-id="957dc-129">若要设置工程组织，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="957dc-129">To set up your engineering organizations, follow these steps.</span></span>

1. <span data-ttu-id="957dc-130">转到 **工程更改管理 &gt; 设置 &gt; 工程组织**。</span><span class="sxs-lookup"><span data-stu-id="957dc-130">Go to **Engineering change management &gt; Setup &gt; Engineering organizations**.</span></span>
1. <span data-ttu-id="957dc-131">选择 **新建** 以向网格添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-131">Select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-132">\**工程组织：\*\*\*DEMF*</span><span class="sxs-lookup"><span data-stu-id="957dc-132">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="957dc-133">\**组织名称：\*\*\*德国 Contoso 娱乐系统*</span><span class="sxs-lookup"><span data-stu-id="957dc-133">**Organization name:** *Contoso Entertainment System Germany*</span></span>

    <span data-ttu-id="957dc-134">![添加工程组织](media/engineering-org.png "添加工程组织")</span><span class="sxs-lookup"><span data-stu-id="957dc-134">![Adding an engineering organization](media/engineering-org.png "Adding an engineering organization")</span></span>

### <a name="set-up-the-version-product-dimension-group"></a><span data-ttu-id="957dc-135">设置版本产品维度组</span><span class="sxs-lookup"><span data-stu-id="957dc-135">Set up the version product dimension group</span></span>

1. <span data-ttu-id="957dc-136">转到 **产品信息管理 &gt; 设置 &gt; 维度和变型组 &gt; 产品维度组**。</span><span class="sxs-lookup"><span data-stu-id="957dc-136">Go to **Product information management &gt; Setup &gt; Dimensions and variant groups &gt; Product dimension groups**.</span></span>
1. <span data-ttu-id="957dc-137">选择 **新建** 以创建产品维度组。</span><span class="sxs-lookup"><span data-stu-id="957dc-137">Select **New** to create a product dimension group.</span></span>
1. <span data-ttu-id="957dc-138">将 **名称** 字段设置为 *版本*。</span><span class="sxs-lookup"><span data-stu-id="957dc-138">Set the **Name** field to *Version*.</span></span>
1. <span data-ttu-id="957dc-139">选择 **保存** 以保存新的维度并将值加载到 **产品维度** 快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="957dc-139">Select **Save** to save the new dimension and load values onto the **Product dimensions** FastTab.</span></span>
1. <span data-ttu-id="957dc-140">在 **产品维度** 快速选项卡上，将 **版本** 设置为有效的产品维度。</span><span class="sxs-lookup"><span data-stu-id="957dc-140">On the **Product dimensions** FastTab, set **Version** as an active product dimension.</span></span>

    <span data-ttu-id="957dc-141">![添加产品维度组](media/product-dimension-groups.png "添加产品维度组")</span><span class="sxs-lookup"><span data-stu-id="957dc-141">![Adding a product dimension group](media/product-dimension-groups.png "Adding a product dimension group")</span></span>

### <a name="set-up-product-lifecycle-states"></a><span data-ttu-id="957dc-142">设置产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="957dc-142">Set up product lifecycle states</span></span>

<span data-ttu-id="957dc-143">当工程产品经历生命周期时，您能够控制每个生命周期状态允许哪些交易这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="957dc-143">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="957dc-144">若要设置产品生命周期状态，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="957dc-144">To set up the product lifecycle states, follow these steps.</span></span>

1. <span data-ttu-id="957dc-145">转到 **工程更改管理 &gt; 设置 &gt; 产品生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="957dc-145">Go to **Engineering change management &gt; Setup &gt; Product lifecycle state**.</span></span>
1. <span data-ttu-id="957dc-146">选择 **新建** 以添加生命周期状态，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-146">Select **New** to add a lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-147">\**状态：\*\*\*运营*</span><span class="sxs-lookup"><span data-stu-id="957dc-147">**State:** *Operational*</span></span>
    - <span data-ttu-id="957dc-148">\**描述：\*\*\*运营*</span><span class="sxs-lookup"><span data-stu-id="957dc-148">**Description:** *Operational*</span></span>

1. <span data-ttu-id="957dc-149">选择 **保存** 以保存新的生命周期状态并将值加载到 **已启用业务流程** 快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="957dc-149">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="957dc-150">在 **已启用业务流程** 快速选项卡上，选择应该可用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="957dc-150">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="957dc-151">对于此示例，针对所有业务流程将 **策略** 字段设置为 *已启用*。</span><span class="sxs-lookup"><span data-stu-id="957dc-151">For this example, leave the **Policy** field set to *Enabled* for all business processes.</span></span>

    <span data-ttu-id="957dc-152">![为生命周期状态启用业务流程](media/product-lifecycle-states-1.png "为生命周期状态启用业务流程")</span><span class="sxs-lookup"><span data-stu-id="957dc-152">![Enabling business processes for a lifecycle state](media/product-lifecycle-states-1.png "Enabling business processes for a lifecycle state")</span></span>

1. <span data-ttu-id="957dc-153">选择 **新建** 以添加另一个生命周期状态，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-153">Select **New** to add another lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-154">\**状态：\*\*\*原型*</span><span class="sxs-lookup"><span data-stu-id="957dc-154">**State:** *Prototype*</span></span>
    - <span data-ttu-id="957dc-155">\**描述：\*\*\*原型*</span><span class="sxs-lookup"><span data-stu-id="957dc-155">**Description:** *Prototype*</span></span>

1. <span data-ttu-id="957dc-156">选择 **保存** 以保存新的生命周期状态并将值加载到 **已启用业务流程** 快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="957dc-156">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="957dc-157">在 **已启用业务流程** 快速选项卡上，选择应该可用的业务流程。</span><span class="sxs-lookup"><span data-stu-id="957dc-157">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="957dc-158">对于此示例，针对所有业务流程将 **策略** 字段设置为 *已启用，但有警告*。</span><span class="sxs-lookup"><span data-stu-id="957dc-158">For this example, set the **Policy** field to *Enabled with warning* for all business processes.</span></span>

    <span data-ttu-id="957dc-159">![为生命周期状态启用（有警告）业务流程](media/product-lifecycle-states-2.png "为生命周期状态启用（有警告）业务流程")</span><span class="sxs-lookup"><span data-stu-id="957dc-159">![Enabling (with warnings) business processes for a lifecycle state](media/product-lifecycle-states-2.png "Enabling (with warnings) business processes for a lifecycle state")</span></span>

### <a name="set-up-a-version-number-rule"></a><span data-ttu-id="957dc-160">设置版本号规则</span><span class="sxs-lookup"><span data-stu-id="957dc-160">Set up a version number rule</span></span>

1. <span data-ttu-id="957dc-161">转到 **工程更改管理 &gt; 设置 &gt; 产品版本号规则**。</span><span class="sxs-lookup"><span data-stu-id="957dc-161">Go to **Engineering change management &gt; Setup &gt; Product version number rule**.</span></span>
1. <span data-ttu-id="957dc-162">选择 **新建** 以添加规则，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-162">Select **New** to add a rule, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-163">\**名称：\*\*\*自动*</span><span class="sxs-lookup"><span data-stu-id="957dc-163">**Name:** *Auto*</span></span>
    - <span data-ttu-id="957dc-164">\**编号规则：\*\*\*自动*</span><span class="sxs-lookup"><span data-stu-id="957dc-164">**Number rule:** *Auto*</span></span>
    - <span data-ttu-id="957dc-165">\**格式：\*\*\*V-\#\#*</span><span class="sxs-lookup"><span data-stu-id="957dc-165">**Format:** *V-\#\#*</span></span>

    <span data-ttu-id="957dc-166">![添加产品版本号规则](media/version-number-rule.png "添加产品版本号规则")</span><span class="sxs-lookup"><span data-stu-id="957dc-166">![Adding a product version number rule](media/version-number-rule.png "Adding a product version number rule")</span></span>

### <a name="set-up-a-product-release-policy"></a><span data-ttu-id="957dc-167">设置产品发布策略</span><span class="sxs-lookup"><span data-stu-id="957dc-167">Set up a product release policy</span></span>

1. <span data-ttu-id="957dc-168">转到 **工程更改管理 &gt; 设置 &gt; 产品发布策略**。</span><span class="sxs-lookup"><span data-stu-id="957dc-168">Go to **Engineering change management &gt; Setup &gt; Product release policies**.</span></span>
1. <span data-ttu-id="957dc-169">选择 **新建** 以添加发布策略，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-169">Select **New** to add a release policy, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-170">\**名称：\*\*\*组件*</span><span class="sxs-lookup"><span data-stu-id="957dc-170">**Name:** *Components*</span></span>
    - <span data-ttu-id="957dc-171">\**描述\*\*\*组件*</span><span class="sxs-lookup"><span data-stu-id="957dc-171">**Description:** *Components*</span></span>

1. <span data-ttu-id="957dc-172">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-172">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="957dc-173">**产品类型**：*物料*</span><span class="sxs-lookup"><span data-stu-id="957dc-173">**Product type:** *Item*</span></span>
    - <span data-ttu-id="957dc-174">\**应用模板：\*\*\*始终*</span><span class="sxs-lookup"><span data-stu-id="957dc-174">**Apply templates:** *Always*</span></span>
    - <span data-ttu-id="957dc-175">\**有效：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="957dc-175">**Active:** *Yes*</span></span>

1. <span data-ttu-id="957dc-176">在 **所有产品** 快速选项卡上，选择 **添加** 以添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-176">On the **All products** FastTab, select **Add** to add a line, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-177">\**公司：\*\*\*DEMF*</span><span class="sxs-lookup"><span data-stu-id="957dc-177">**Company:** *DEMF*</span></span>
    - <span data-ttu-id="957dc-178">\**已发布产品模板：\*\*\*D0006*</span><span class="sxs-lookup"><span data-stu-id="957dc-178">**Template released product:** *D0006*</span></span>

1. <span data-ttu-id="957dc-179">选择 **添加** 再添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-179">Select **Add** to add another line, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-180">\**公司帐户 ID：\*\*\*USMF*</span><span class="sxs-lookup"><span data-stu-id="957dc-180">**Company accounts ID:** *USMF*</span></span>
    - <span data-ttu-id="957dc-181">\**已发布产品模板：\*\*\*D0006*</span><span class="sxs-lookup"><span data-stu-id="957dc-181">**Template released product:** *D0006*</span></span>
    - <span data-ttu-id="957dc-182">**接收 BOM：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-182">**Receive BOM:** Select this check box.</span></span>
    - <span data-ttu-id="957dc-183">**复制 BOM 审批：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-183">**Copy BOM approval:** Select this check box.</span></span>
    - <span data-ttu-id="957dc-184">**复制 BOM 激活：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-184">**Copy BOM activation:** Select this check box.</span></span>
    - <span data-ttu-id="957dc-185">**接收工艺路线：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-185">**Receive route:** Select this check box.</span></span>
    - <span data-ttu-id="957dc-186">**复制工艺路线审批：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-186">**Copy route approval:** Select this check box.</span></span>
    - <span data-ttu-id="957dc-187">**复制工艺路线激活：** 选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-187">**Copy route activation:** Select this check box.</span></span>

    <span data-ttu-id="957dc-188">![添加产品发布策略](media/product-release-policy.png "添加产品发布策略")</span><span class="sxs-lookup"><span data-stu-id="957dc-188">![Adding a product release policy](media/product-release-policy.png "Adding a product release policy")</span></span>

### <a name="set-up-an-engineering-product-category"></a><span data-ttu-id="957dc-189">设置工程产品类别</span><span class="sxs-lookup"><span data-stu-id="957dc-189">Set up an engineering product category</span></span> 

<span data-ttu-id="957dc-190">工程产品类别提供用于创建工程产品（即通过工程更改管理进行版本控制的产品）的基础。</span><span class="sxs-lookup"><span data-stu-id="957dc-190">Engineering product categories provide the basis for creating engineering products (that is, products that are versioned and controlled through engineering change management).</span></span> <span data-ttu-id="957dc-191">若要设置工程产品类别，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="957dc-191">To set up engineering product categories, follow these steps.</span></span>

1. <span data-ttu-id="957dc-192">转到 **工程更改管理 &gt; 工程产品类别详细信息**。</span><span class="sxs-lookup"><span data-stu-id="957dc-192">Go to **Engineering change management &gt; Engineering product category details**.</span></span>
1. <span data-ttu-id="957dc-193">选择 **新建** 以创建类别。</span><span class="sxs-lookup"><span data-stu-id="957dc-193">Select **New** to create a category.</span></span>
1. <span data-ttu-id="957dc-194">在 **详细信息** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-194">On the **Details** FastTab, set the following values:</span></span>

    - <span data-ttu-id="957dc-195">\**名称：\*\*\*组件*</span><span class="sxs-lookup"><span data-stu-id="957dc-195">**Name:** *Components*</span></span>
    - <span data-ttu-id="957dc-196">\**工程组织：\*\*\*DEMF*</span><span class="sxs-lookup"><span data-stu-id="957dc-196">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="957dc-197">**产品类型**：*物料*</span><span class="sxs-lookup"><span data-stu-id="957dc-197">**Product type:** *Item*</span></span>
    - <span data-ttu-id="957dc-198">\**跟踪交易中的版本：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="957dc-198">**Track version in transactions:** *Yes*</span></span>
    - <span data-ttu-id="957dc-199">\**产品维度组：\*\*\*版本*</span><span class="sxs-lookup"><span data-stu-id="957dc-199">**Product dimension group:** *Version*</span></span>
    - <span data-ttu-id="957dc-200">\**创建时的产品生命周期状态：\*\*\*运营*</span><span class="sxs-lookup"><span data-stu-id="957dc-200">**Product lifecycle state at creation:** *Operational*</span></span>
    - <span data-ttu-id="957dc-201">\**版本号规则：\*\*\*自动*</span><span class="sxs-lookup"><span data-stu-id="957dc-201">**Version number rule:** *Auto*</span></span>
    - <span data-ttu-id="957dc-202">\**强制实施有效性：\*\*\*否*</span><span class="sxs-lookup"><span data-stu-id="957dc-202">**Enforce effectivity:** *No*</span></span>
    - <span data-ttu-id="957dc-203">\**使用编号规则命名法：\*\*\*否*</span><span class="sxs-lookup"><span data-stu-id="957dc-203">**Use number rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="957dc-204">\**使用名称规则命名法：\*\*\*否*</span><span class="sxs-lookup"><span data-stu-id="957dc-204">**Use name rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="957dc-205">\**使用描述规则命名法：\*\*\*否*</span><span class="sxs-lookup"><span data-stu-id="957dc-205">**Use description rule nomenclature:** *No*</span></span>

1. <span data-ttu-id="957dc-206">在 **发布策略** 快速选项卡上，将 **产品发布策略** 设置为 *组件*。</span><span class="sxs-lookup"><span data-stu-id="957dc-206">On the **Release policy** FastTab, set the **Product release policy** field to *Components*.</span></span>
1. <span data-ttu-id="957dc-207">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-207">Select **Save**.</span></span>

    <span data-ttu-id="957dc-208">![添加工程产品类别](media/product-category-details.png "添加工程产品类别")</span><span class="sxs-lookup"><span data-stu-id="957dc-208">![Adding an engineering product category](media/product-category-details.png "Adding an engineering product category")</span></span>

### <a name="set-up-product-acceptance-conditions"></a><span data-ttu-id="957dc-209">设置产品接受条件</span><span class="sxs-lookup"><span data-stu-id="957dc-209">Set up product acceptance conditions</span></span>

1. <span data-ttu-id="957dc-210">使用导航栏右侧的公司选择器切换到 *USMF* 法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="957dc-210">Use the company picker on the right side of the navigation bar to switch to the *USMF* legal entity (company).</span></span>
1. <span data-ttu-id="957dc-211">转到 **工程更改管理 &gt; 设置 &gt; 工程更改管理参数**。</span><span class="sxs-lookup"><span data-stu-id="957dc-211">Go to **Engineering change management &gt; Setup &gt; Engineering change management parameters**.</span></span>
1. <span data-ttu-id="957dc-212">在 **发布控制** 选项卡上的 **产品接受** 部分中，将 **产品接受** 字段设置为 *手动*。</span><span class="sxs-lookup"><span data-stu-id="957dc-212">On the **Release control** tab, in the **Product acceptance** section, set the **Product acceptance** field to *Manual*.</span></span>

    <span data-ttu-id="957dc-213">![设置产品接受条件](media/engineering-change-management-parameters.png "设置产品接受条件")</span><span class="sxs-lookup"><span data-stu-id="957dc-213">![Setting up product acceptance conditions](media/engineering-change-management-parameters.png "Setting up product acceptance conditions")</span></span>

## <a name="create-a-new-engineering-product"></a><span data-ttu-id="957dc-214">创建新工程产品</span><span class="sxs-lookup"><span data-stu-id="957dc-214">Create a new engineering product</span></span>

<span data-ttu-id="957dc-215">工程产品是通过工程更改管理进行版本控制的产品。</span><span class="sxs-lookup"><span data-stu-id="957dc-215">An engineering product is a product that is versioned and controlled through engineering change management.</span></span> <span data-ttu-id="957dc-216">换句话说，您可以在其生命周期内控制更改，并且将使用工程更改订单保存更改信息。</span><span class="sxs-lookup"><span data-stu-id="957dc-216">In other words, you can control the changes during its life, and the change information will be saved using engineering change orders.</span></span> <span data-ttu-id="957dc-217">若要创建工程产品，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="957dc-217">To create engineering products, follow these steps.</span></span>

1. <span data-ttu-id="957dc-218">确保您在工程组织的法人中（对于此示例，在 *DEMF* 中）。</span><span class="sxs-lookup"><span data-stu-id="957dc-218">Make sure that you're in the legal entity of your engineering organization (*DEMF* for this example).</span></span> <span data-ttu-id="957dc-219">根据需要使用导航栏右侧的公司选择器。</span><span class="sxs-lookup"><span data-stu-id="957dc-219">Use the company picker on the right side of the navigation bar as required.</span></span>
1. <span data-ttu-id="957dc-220">通过执行以下步骤之一打开 **已发布产品** 页面：</span><span class="sxs-lookup"><span data-stu-id="957dc-220">Open the **Released products** page by following one of these steps:</span></span>

    - <span data-ttu-id="957dc-221">转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-221">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
    - <span data-ttu-id="957dc-222">转到 **工程更改管理 &gt; 通用 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-222">Go to **Engineering change management &gt; Common &gt; Released products**.</span></span>

1. <span data-ttu-id="957dc-223">在操作窗格的 **产品** 选项卡上的 **新建** 组中，选择 **工程产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-223">On the Action Pane, on the **Product** tab, in the **New** group, select **Engineering product**.</span></span>
1. <span data-ttu-id="957dc-224">在 **新产品** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-224">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="957dc-225">\**工程产品类别：\*\*\*组件*</span><span class="sxs-lookup"><span data-stu-id="957dc-225">**Engineering Product Category:** *Components*</span></span>
    - <span data-ttu-id="957dc-226">**产品编号**：*Z0001*</span><span class="sxs-lookup"><span data-stu-id="957dc-226">**Product number:** *Z0001*</span></span>
    - <span data-ttu-id="957dc-227">\**产品名称：\*\*\*扬声器组*</span><span class="sxs-lookup"><span data-stu-id="957dc-227">**Product name:** *Speaker set*</span></span>

    <span data-ttu-id="957dc-228">![添加工程产品](media/new-product-dialog.png "添加工程产品")</span><span class="sxs-lookup"><span data-stu-id="957dc-228">![Adding an engineering product](media/new-product-dialog.png "Adding an engineering product")</span></span>

    <span data-ttu-id="957dc-229">请注意，使用您之前设置的产品版本号规则自动设置 **版本** 字段。</span><span class="sxs-lookup"><span data-stu-id="957dc-229">Note that the **Version** field is automatically set by using the product version number rule that you set up earlier.</span></span>

1. <span data-ttu-id="957dc-230">选择 **确定** 创建产品，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="957dc-230">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="957dc-231">打开新产品的详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-231">The details page for the new product is opened.</span></span> <span data-ttu-id="957dc-232">请注意，某些字段（例如 **存储维度组**、**跟踪维度组** 和/或 **物料模型组**）中已经填写了值。</span><span class="sxs-lookup"><span data-stu-id="957dc-232">Notice that values are already filled in for some fields, such as **Storage dimension group**, **Tracking dimension group**, and/or **Item model group**.</span></span> <span data-ttu-id="957dc-233">这些字段已自动设置，因为产品已在 *DEMF* 法人中发布并使用 *组件* 产品发布策略，这与 *组件* 工程产品类别相关联。</span><span class="sxs-lookup"><span data-stu-id="957dc-233">These fields were automatically set because the product is being released in the *DEMF* legal entity and uses the *Components* product release policy, which is associated with the *Components* engineering product category.</span></span> <span data-ttu-id="957dc-234">因为您之前使用了物料 *D0006* 作为模板来为 *DEMF* 法人设置行，填写的值取自物料 *D0006*。</span><span class="sxs-lookup"><span data-stu-id="957dc-234">Because you previously used item *D0006* as a template to set up a line for the *DEMF* legal entity, the values that were filled in were taken from item *D0006*.</span></span>

    <span data-ttu-id="957dc-235">![已发布产品详细信息](media/product-details.png "已发布产品详细信息")</span><span class="sxs-lookup"><span data-stu-id="957dc-235">![Released product details](media/product-details.png "Released product details")</span></span>

1. <span data-ttu-id="957dc-236">在操作窗格的 **工程师** 选项卡上，在 **工程更改管理** 组中，选择 **工程版本** 以查看产品的版本。</span><span class="sxs-lookup"><span data-stu-id="957dc-236">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions** to view the versions of the product.</span></span>

    <span data-ttu-id="957dc-237">![工程版本](media/engineering-versions-list.png "工程版本")</span><span class="sxs-lookup"><span data-stu-id="957dc-237">![Engineering versions](media/engineering-versions-list.png "Engineering versions")</span></span>

1. <span data-ttu-id="957dc-238">在 **工程版本** 页面上，请注意该产品只有一个版本，并且该版本处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="957dc-238">On the **Engineering versions** page, notice that there is only one version for the product, and it's active.</span></span>
1. <span data-ttu-id="957dc-239">选择版本以查看其详细信息。</span><span class="sxs-lookup"><span data-stu-id="957dc-239">Select the version to view its details.</span></span>

    <span data-ttu-id="957dc-240">![工程版本详细信息](media/engineering-version-details.png "工程版本详细信息")</span><span class="sxs-lookup"><span data-stu-id="957dc-240">![Engineering version details](media/engineering-version-details.png "Engineering version details")</span></span>

1. <span data-ttu-id="957dc-241">在 **工程版本** 页面上的 **物料清单** 快速选项卡上，选择 **创建 BOM**。</span><span class="sxs-lookup"><span data-stu-id="957dc-241">On the **Engineering version** page, on the **Bill of material** FastTab, select **Create BOM**.</span></span>
1. <span data-ttu-id="957dc-242">在 **创建 BOM** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-242">In the **Create BOM** dialog box, set the following values:</span></span>

    - <span data-ttu-id="957dc-243">**BOM 编号：** Z0001</span><span class="sxs-lookup"><span data-stu-id="957dc-243">**BOM number:** Z0001</span></span>
    - <span data-ttu-id="957dc-244">**名称：** 扬声器组</span><span class="sxs-lookup"><span data-stu-id="957dc-244">**Name:** Speaker set</span></span>
    - <span data-ttu-id="957dc-245">**站点：** 1</span><span class="sxs-lookup"><span data-stu-id="957dc-245">**Site:** 1</span></span>

    <span data-ttu-id="957dc-246">![创建 BOM](media/create-bom.png "创建 BOM")</span><span class="sxs-lookup"><span data-stu-id="957dc-246">![Creating a BOM](media/create-bom.png "Creating a BOM")</span></span>

1. <span data-ttu-id="957dc-247">选择 **确定** 以添加 BOM，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="957dc-247">Select **OK** to add the BOM and close the dialog box.</span></span>
1. <span data-ttu-id="957dc-248">在 **物料清单** 快速选项卡上，选择 **物料清单**。</span><span class="sxs-lookup"><span data-stu-id="957dc-248">On the **Bill of materials** FastTab, select **Bill of material**.</span></span>
1. <span data-ttu-id="957dc-249">在 **物料清单** 页面上的 **物料清单行** 快速选项卡上，添加三行，每一行对应于物料编号 *D0001*、*D0003* 和 *D0006*。</span><span class="sxs-lookup"><span data-stu-id="957dc-249">On the **Bill of materials** page, on the **Bill of materials lines** FastTab, add three lines, one each for item numbers *D0001*, *D0003*, and *D0006*.</span></span>

    <span data-ttu-id="957dc-250">![添加 BOM 行](media/bom.png "添加 BOM 行")</span><span class="sxs-lookup"><span data-stu-id="957dc-250">![Adding BOM lines](media/bom.png "Adding BOM lines")</span></span>

1. <span data-ttu-id="957dc-251">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-251">Select **Save**.</span></span>
1. <span data-ttu-id="957dc-252">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-252">Close the page.</span></span>
1. <span data-ttu-id="957dc-253">在 **工程版本** 页面上的 **物料清单** 快速选项卡上，选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="957dc-253">On the **Engineering version** page, on the **Bill of material** FastTab, select **Approve**.</span></span>
1. <span data-ttu-id="957dc-254">在显示的对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="957dc-254">In the dialog box that appears, select **OK**.</span></span>

    <span data-ttu-id="957dc-255">![审核 BOM](media/approve-dialog.png "审核 BOM")</span><span class="sxs-lookup"><span data-stu-id="957dc-255">![Approving the BOM](media/approve-dialog.png "Approving the BOM")</span></span>

1. <span data-ttu-id="957dc-256">在 **工程版本** 页面上的 **物料清单** 快速选项卡上，选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="957dc-256">On the **Engineering version** page, on the **Bill of material** FastTab, select **Activate**.</span></span>
1. <span data-ttu-id="957dc-257">请注意，已针对 BOM 选中 **活动** 和 **已审核** 复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-257">Notice that the **Active** and **Approved** check boxes are selected for the BOM.</span></span>

    <span data-ttu-id="957dc-258">![活动和已审核 BOM](media/approved-bom.png "活动和已审核 BOM")</span><span class="sxs-lookup"><span data-stu-id="957dc-258">![Active and approved BOM](media/approved-bom.png "Active and approved BOM")</span></span>

1. <span data-ttu-id="957dc-259">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-259">Close the page.</span></span>

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a><span data-ttu-id="957dc-260">向本地公司发布工程产品</span><span class="sxs-lookup"><span data-stu-id="957dc-260">Release an engineering product to a local company</span></span>

<span data-ttu-id="957dc-261">该产品现已由工程部门设计。</span><span class="sxs-lookup"><span data-stu-id="957dc-261">The product has now been designed by the Engineering department.</span></span> <span data-ttu-id="957dc-262">对于此示例，产品是工程部门为客户设计的原型。</span><span class="sxs-lookup"><span data-stu-id="957dc-262">For this example, the product is a prototype that engineering has designed for a customer.</span></span> <span data-ttu-id="957dc-263">因为客户是 *USMF* 法人的客户，因此必须将产品发布给该法人。</span><span class="sxs-lookup"><span data-stu-id="957dc-263">Because the customer is a customer of the *USMF* legal entity, the product must be released to that legal entity.</span></span>

1. <span data-ttu-id="957dc-264">将法人设置为 *DEMF*。</span><span class="sxs-lookup"><span data-stu-id="957dc-264">Keep the legal entity set to *DEMF*.</span></span> <span data-ttu-id="957dc-265">（根据需要使用导航栏右侧的公司选择器。）</span><span class="sxs-lookup"><span data-stu-id="957dc-265">(Use the company picker on the right side of the navigation bar as required.)</span></span>
1. <span data-ttu-id="957dc-266">转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-266">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="957dc-267">选择产品 *Z0001*。</span><span class="sxs-lookup"><span data-stu-id="957dc-267">Select product *Z0001*.</span></span>
1. <span data-ttu-id="957dc-268">在操作窗格的 **产品** 选项卡上，在 **维护** 组中，选择 **发布产品结构** 以打开 **发布产品** 向导。</span><span class="sxs-lookup"><span data-stu-id="957dc-268">On the Action Pane, on the **Product** tab, in the **Maintain** group, select **Release product structure** to open the **Release products** wizard.</span></span>
1. <span data-ttu-id="957dc-269">在 **选择要发布的工程产品** 页面上，针对产品 *Z0001* 选中 **选择** 复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-269">On the **Select engineering products to release** page, select the **Select** check box for product *Z0001*.</span></span>

    <span data-ttu-id="957dc-270">![选择要发布的工程产品](media/select-eng-product-to-release.png "选择要发布的工程产品")</span><span class="sxs-lookup"><span data-stu-id="957dc-270">![Selecting the engineering products to release](media/select-eng-product-to-release.png "Selecting the engineering products to release")</span></span>

1. <span data-ttu-id="957dc-271">选择 **发布详细信息**。</span><span class="sxs-lookup"><span data-stu-id="957dc-271">Select **Release details**.</span></span>
1. <span data-ttu-id="957dc-272">将显示 **产品发布详细信息** 页面，您可以在其中查看将要发布的产品的详细信息及其产品结构。</span><span class="sxs-lookup"><span data-stu-id="957dc-272">The **Product release details** page appears, where you can review the details of the product that will be released, and its product structure.</span></span> <span data-ttu-id="957dc-273">请注意，**发送 BOM** 选项将设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="957dc-273">Notice that the **Send BOM** option is set to *Yes*.</span></span> <span data-ttu-id="957dc-274">因此，将发布 BOM 中的产品 *Z0001* 及其所有子物料。</span><span class="sxs-lookup"><span data-stu-id="957dc-274">Therefore, both product *Z0001* and all its child items from the BOM will be released.</span></span>

    <span data-ttu-id="957dc-275">您可以在左窗格中选择任何子物料以查看其详细信息。</span><span class="sxs-lookup"><span data-stu-id="957dc-275">You can select any child item in the left pane to review its details.</span></span> <span data-ttu-id="957dc-276">如果任何子物料具有 BOM，您还可以选择发布该子物料的 BOM。</span><span class="sxs-lookup"><span data-stu-id="957dc-276">If any child item has a BOM, you can also select to release the BOM of that child item.</span></span>

    <span data-ttu-id="957dc-277">![查看产品发布详细信息](media/product-release-details.png "查看产品发布详细信息")</span><span class="sxs-lookup"><span data-stu-id="957dc-277">![Reviewing the product release details](media/product-release-details.png "Reviewing the product release details")</span></span>

1. <span data-ttu-id="957dc-278">关闭页面以返回到 **发布产品** 向导。</span><span class="sxs-lookup"><span data-stu-id="957dc-278">Close the page to return to the **Release products** wizard.</span></span>
1. <span data-ttu-id="957dc-279">选择 **下一步** 以打开 **选择要发布的产品** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-279">Select **Next** to open the **Select products to release** page.</span></span> <span data-ttu-id="957dc-280">如果您选择了任何标准（非工程）产品，它们将显示在此页面上。</span><span class="sxs-lookup"><span data-stu-id="957dc-280">If you had selected any standard (non-engineering) products, they would appear on this page.</span></span> <span data-ttu-id="957dc-281">请注意，当您通过选择 **发布产品结构** 发布标准产品时，也将发布其 BOM 和工艺路线。</span><span class="sxs-lookup"><span data-stu-id="957dc-281">Note that when you release a standard product by selecting **Release product structure**, its BOM and route are also released.</span></span>

    <span data-ttu-id="957dc-282">![选择要发布的标准产品](media/select-std-product-to-release.png "选择要发布的标准产品")</span><span class="sxs-lookup"><span data-stu-id="957dc-282">![Selecting the standard products to release](media/select-std-product-to-release.png "Selecting the standard products to release")</span></span>

1. <span data-ttu-id="957dc-283">选择 **下一步** 以打开 **选择要发布的产品变型** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-283">Select **Next** to open the **Select product variants to release** page.</span></span> <span data-ttu-id="957dc-284">对于此示例，没有任何变型。</span><span class="sxs-lookup"><span data-stu-id="957dc-284">For this example, there aren't any variants.</span></span>
1. <span data-ttu-id="957dc-285">选择 **下一步** 以打开 **选择公司** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-285">Select **Next** to open the **Select companies** page.</span></span>
1. <span data-ttu-id="957dc-286">选择产品应发布到的公司。</span><span class="sxs-lookup"><span data-stu-id="957dc-286">Select the companies that the product should be released to.</span></span> <span data-ttu-id="957dc-287">对于此示例，选中 **USMF** 的复选框。</span><span class="sxs-lookup"><span data-stu-id="957dc-287">For this example, select the check box for **USMF**.</span></span>

    <span data-ttu-id="957dc-288">![选择要发布到的公司](media/select-release-companies.png "选择要发布到的公司")</span><span class="sxs-lookup"><span data-stu-id="957dc-288">![Selecting the companies to release to](media/select-release-companies.png "Selecting the companies to release to")</span></span>

1. <span data-ttu-id="957dc-289">选择 **下一步** 以打开 **确认选择** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-289">Select **Next** to open the **Confirm selection** page.</span></span>
1. <span data-ttu-id="957dc-290">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="957dc-290">Select **Finish**.</span></span>

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a><span data-ttu-id="957dc-291">审查并接受产品，然后在本地公司中发布该产品</span><span class="sxs-lookup"><span data-stu-id="957dc-291">Review and accept the product before you release it in the local company</span></span>

<span data-ttu-id="957dc-292">工程部门现已将信息发布给将使用该产品的本地公司。</span><span class="sxs-lookup"><span data-stu-id="957dc-292">The Engineering department has now released the information to the local companies where the product will be used.</span></span> <span data-ttu-id="957dc-293">对于本示例，该本地公司为 *USMF*。</span><span class="sxs-lookup"><span data-stu-id="957dc-293">For this example, the local company is *USMF*.</span></span>

<span data-ttu-id="957dc-294">因为您在 *USMF* 公司的 **工程更改管理参数** 页面上将 **产品接受** 字段设置为 *手动*，因此必须先手动接受产品，然后才能将其发布给该公司。</span><span class="sxs-lookup"><span data-stu-id="957dc-294">Because you set the **Product acceptance** field to *Manual* on the **Engineering change management parameters** page for the *USMF* company, products must be manually accepted before they are released to that company.</span></span> <span data-ttu-id="957dc-295">换句话说，必须先审查并接受产品，它们才能成为已发布产品。</span><span class="sxs-lookup"><span data-stu-id="957dc-295">In other words, they must be reviewed and accepted before they become released products.</span></span>

<span data-ttu-id="957dc-296">若要审查产品并在 *USMF* 公司中发布它，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="957dc-296">To review the product and release it in the *USMF* company, follow these steps.</span></span>

1. <span data-ttu-id="957dc-297">将法人设置为 *USMF*。</span><span class="sxs-lookup"><span data-stu-id="957dc-297">Set the legal entity to *USMF*.</span></span> <span data-ttu-id="957dc-298">（使用导航栏右侧的公司选择器。）</span><span class="sxs-lookup"><span data-stu-id="957dc-298">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="957dc-299">转到 **工程更改管理 &gt; 通用 &gt; 产品发布 &gt; 打开产品发布**。</span><span class="sxs-lookup"><span data-stu-id="957dc-299">Go to **Engineering change management &gt; Common &gt; Product releases &gt; Open product releases**.</span></span>

    <span data-ttu-id="957dc-300">**打开产品发布** 页面显示产品 *Z0001*，其状态为 *等待接受*。</span><span class="sxs-lookup"><span data-stu-id="957dc-300">The **Open product releases** page shows product *Z0001*, which has a status of *Pending acceptance*.</span></span>

    <span data-ttu-id="957dc-301">![未处理的产品发布](media/open-product-releases.png "未处理的产品发布")</span><span class="sxs-lookup"><span data-stu-id="957dc-301">![Open product releases](media/open-product-releases.png "Open product releases")</span></span>

1. <span data-ttu-id="957dc-302">在 **产品编号** 列中选择该值以打开 **产品发布详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-302">Select the value in the **Product number** column to open the **Product release details** page.</span></span> <span data-ttu-id="957dc-303">注意以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="957dc-303">Notice the following details:</span></span>

    - <span data-ttu-id="957dc-304">**常规** 快速选项卡显示有关产品发布的信息，例如发布公司（对于此示例为 *DEMF*）、发布站点 (*1*) 和接收站点 (*1*)。</span><span class="sxs-lookup"><span data-stu-id="957dc-304">The **General** FastTab shows information about the product release, such as the releasing company (*DEMF* for this example), the releasing site (*1*), and the receiving site (*1*).</span></span> <span data-ttu-id="957dc-305">因为您没有在 **发布产品** 向导中指定接收站点，因此将发布站点值复制到接收站点。</span><span class="sxs-lookup"><span data-stu-id="957dc-305">Because you didn't specify a receiving site in the **Release products** wizard, the the releasing site value is copied to the receiving site.</span></span>
    - <span data-ttu-id="957dc-306">**发布详细信息** 快速选项卡显示有关产品和已发布版本的信息。</span><span class="sxs-lookup"><span data-stu-id="957dc-306">The **Release details** FastTab shows information about the product and the version that was released.</span></span> <span data-ttu-id="957dc-307">在此处，您可以修改设置，例如生效日期。</span><span class="sxs-lookup"><span data-stu-id="957dc-307">Here, you can modify settings such as the effectivity dates.</span></span>
    - <span data-ttu-id="957dc-308">**工艺路线** 快速选项卡显示产品的工艺路线。</span><span class="sxs-lookup"><span data-stu-id="957dc-308">The **Route** FastTab shows the route of the product.</span></span> <span data-ttu-id="957dc-309">但是，对于此示例，您没有发布任何工艺路线。</span><span class="sxs-lookup"><span data-stu-id="957dc-309">However, for this example, you didn't release any routes.</span></span>

    <span data-ttu-id="957dc-310">![产品发布详细信息](media/product-release-details-2.png "产品发布详细信息")</span><span class="sxs-lookup"><span data-stu-id="957dc-310">![Product release details](media/product-release-details-2.png "Product release details")</span></span>

1. <span data-ttu-id="957dc-311">查看完信息后，您就可以准备接受产品，并通过这种方式在 *USMF* 公司中发布它。</span><span class="sxs-lookup"><span data-stu-id="957dc-311">When you've finished reviewing the information, you're ready to accept the product and, in this way, release it in the *USMF* company.</span></span> <span data-ttu-id="957dc-312">在操作窗格上，选择 **操作 &gt; 接受**。</span><span class="sxs-lookup"><span data-stu-id="957dc-312">On the Action Pane, select **Actions &gt; Accept**.</span></span>
1. <span data-ttu-id="957dc-313">现在，在 *USMF* 公司中发布产品。</span><span class="sxs-lookup"><span data-stu-id="957dc-313">The product is now released in the *USMF* company.</span></span> <span data-ttu-id="957dc-314">转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-314">Go to **Product information management &gt;Products &gt; Released products**.</span></span> <span data-ttu-id="957dc-315">您应该看到物料 *Z0001*。</span><span class="sxs-lookup"><span data-stu-id="957dc-315">You should see item *Z0001*.</span></span>

## <a name="use-the-product-in-transactions-in-the-local-company"></a><span data-ttu-id="957dc-316">在本地公司中使用交易中的产品</span><span class="sxs-lookup"><span data-stu-id="957dc-316">Use the product in transactions in the local company</span></span>

<span data-ttu-id="957dc-317">*USMF* 公司的主数据管理器想要确保产品处于 *原型* 状态，以确保用户在意外将其添加到您正在执行的流程时收到警告。</span><span class="sxs-lookup"><span data-stu-id="957dc-317">The master data manager for the *USMF* company wants to make sure that the product is in a *Prototype* state, to ensure that users will be warned if they accidentally add it to processes that they are working on.</span></span>

1. <span data-ttu-id="957dc-318">转到 **产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="957dc-318">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="957dc-319">选择产品 *Z0001* 以打开其详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-319">Select product *Z0001* to open its details page.</span></span> <span data-ttu-id="957dc-320">（您可以使用筛选器查找产品。）</span><span class="sxs-lookup"><span data-stu-id="957dc-320">(You can use the filter to find the product.)</span></span>
1. <span data-ttu-id="957dc-321">在操作窗格的 **工程师** 选项卡上，在 **工程更改管理** 组中，选择 **工程版本**。</span><span class="sxs-lookup"><span data-stu-id="957dc-321">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions**.</span></span>
1. <span data-ttu-id="957dc-322">在 **工程版本** 页面上，选择版本号 *V-01* 以打开其详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-322">On the **Engineering versions** page, select version number *V-01* to open its details page.</span></span>
1. <span data-ttu-id="957dc-323">在操作窗格的 **产品** 选项卡上，在 **生命周期状态** 组中，选择 **更改生命周期状态**。</span><span class="sxs-lookup"><span data-stu-id="957dc-323">On the Action Pane, on the **Product** tab, in the **Lifecycle state** group, select **Change lifecycle state**.</span></span>
1. <span data-ttu-id="957dc-324">在 **更改生命周期状态** 下拉对话框中，将 **状态** 字段设置为 *原型*，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="957dc-324">In the **Change lifecycle state** drop-down dialog box, set the **State** field to *Prototype*, and then select **OK**.</span></span>

    <span data-ttu-id="957dc-325">![更改生命周期状态](media/change-lifecycle-state.png "更改生命周期状态")</span><span class="sxs-lookup"><span data-stu-id="957dc-325">![Changing the lifecycle state](media/change-lifecycle-state.png "Changing the lifecycle state")</span></span>

## <a name="add-the-engineering-product-to-a-sales-order"></a><span data-ttu-id="957dc-326">将工程产品添加到销售订单</span><span class="sxs-lookup"><span data-stu-id="957dc-326">Add the engineering product to a sales order</span></span>

<span data-ttu-id="957dc-327">现在可以将产品出售给客户。</span><span class="sxs-lookup"><span data-stu-id="957dc-327">The product can now be sold to a customer.</span></span> <span data-ttu-id="957dc-328">若要将产品添加到销售订单，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="957dc-328">To add the product to a sales order, follow these steps.</span></span>

1. <span data-ttu-id="957dc-329">转到 **销售和营销 &gt; 销售订单 &gt; 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="957dc-329">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="957dc-330">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="957dc-330">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="957dc-331">在 **创建销售订单** 对话框中，将 **客户帐户** 字段设置为 *US-0002*，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="957dc-331">In the **Create sales order** dialog box, set the **Customer account** field to *US-0002*, and then select **OK**.</span></span>
1. <span data-ttu-id="957dc-332">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="957dc-332">The new sales order is opened.</span></span> <span data-ttu-id="957dc-333">在 **销售订单行** 快速选项卡上，添加一行，然后针对该行将 **物料编号** 设置为 *Z000*。</span><span class="sxs-lookup"><span data-stu-id="957dc-333">On the **Sales order lines** FastTab, add a row, and set the **Item number** field to *Z000* for it.</span></span>
1. <span data-ttu-id="957dc-334">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-334">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="957dc-335">您会收到一条警告消息，通知您该物料的状态为 *原型*。</span><span class="sxs-lookup"><span data-stu-id="957dc-335">You receive a warning message that informs you that the item has a status of *Prototype*.</span></span> <span data-ttu-id="957dc-336">但是，由于该消息只是警告，因此仍然创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="957dc-336">However, because the message is just a warning, the sales order was still created.</span></span>

    <span data-ttu-id="957dc-337">![工程产品的销售订单](media/sales-order-eng-product.png "工程产品的销售订单")</span><span class="sxs-lookup"><span data-stu-id="957dc-337">![Sales order for an engineering product](media/sales-order-eng-product.png "Sales order for an engineering product")</span></span>

## <a name="request-changes-in-the-engineering-product"></a><span data-ttu-id="957dc-338">在工程产品中请求更改</span><span class="sxs-lookup"><span data-stu-id="957dc-338">Request changes in the engineering product</span></span>

<span data-ttu-id="957dc-339">产品已发送给客户，但客户并不完全满意，并提供包括改进建议的反馈。</span><span class="sxs-lookup"><span data-stu-id="957dc-339">The product was sent to a customer, but the customer wasn't completely satisfied and provides feedback that includes suggestions for improvement.</span></span> <span data-ttu-id="957dc-340">当客户通过电话与销售人员交谈时，销售人员可以请求客户描述的更改。</span><span class="sxs-lookup"><span data-stu-id="957dc-340">While the customer is speaking with a sales clerk on the phone, the sales clerk can request the changes that the customer is describing.</span></span>

1. <span data-ttu-id="957dc-341">转到 **销售和营销 &gt; 销售订单 &gt; 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="957dc-341">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="957dc-342">查找并打开您在上一个练习中创建的销售订单。</span><span class="sxs-lookup"><span data-stu-id="957dc-342">Find and open the sales order that you created in the previous exercise.</span></span>
1. <span data-ttu-id="957dc-343">在 **销售订单行** 快速选项卡上，选择 **工程更改管理 &gt; 新工程更改请求**。</span><span class="sxs-lookup"><span data-stu-id="957dc-343">On the **Sales order lines** FastTab, select **Engineering change management &gt; New engineering change request**.</span></span>

    <span data-ttu-id="957dc-344">![根据销售订单创建工程更改请求](media/sales-order-eng-change-request.png "根据销售订单创建工程更改请求")</span><span class="sxs-lookup"><span data-stu-id="957dc-344">![Creating an engineering change request from a sales order](media/sales-order-eng-change-request.png "Creating an engineering change request from a sales order")</span></span>

1. <span data-ttu-id="957dc-345">根据客户的反馈填写工程更改请求。</span><span class="sxs-lookup"><span data-stu-id="957dc-345">Fill in the engineering change request, based on the customer's feedback.</span></span> <span data-ttu-id="957dc-346">对于此示例，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-346">For this example, set the following values:</span></span>

    - <span data-ttu-id="957dc-347">\**更改请求：\*\*\*555*</span><span class="sxs-lookup"><span data-stu-id="957dc-347">**Change request:** *555*</span></span>
    - <span data-ttu-id="957dc-348">\**标题：\*\*\*Z0001 客户更改*</span><span class="sxs-lookup"><span data-stu-id="957dc-348">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="957dc-349">\**优先级：\*\*\*低*</span><span class="sxs-lookup"><span data-stu-id="957dc-349">**Priority:** *low*</span></span>
    - <span data-ttu-id="957dc-350">**类别：** 设置更改</span><span class="sxs-lookup"><span data-stu-id="957dc-350">**Category:** set change</span></span>
    - <span data-ttu-id="957dc-351">\**严重性：\*\*\*中*</span><span class="sxs-lookup"><span data-stu-id="957dc-351">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="957dc-352">在 **信息** 快速选项卡上，选择 **新建 &gt; 注释** 以向网格添加注释。</span><span class="sxs-lookup"><span data-stu-id="957dc-352">On the **Information** FastTab, select **New &gt; Note** to add a note to the grid.</span></span>
1. <span data-ttu-id="957dc-353">在新注释的 **描述** 字段中，指示应从 BOM 中删除该物料 *D0003*。</span><span class="sxs-lookup"><span data-stu-id="957dc-353">In the **Description** field for the new note, indicate that item *D0003* should be deleted from the BOM.</span></span> <span data-ttu-id="957dc-354">如果您必须添加注释的详细信息，可以在 **注释** 字段中输入文本。</span><span class="sxs-lookup"><span data-stu-id="957dc-354">If you must add more information for the note, you can enter text in the **Notes** field.</span></span>

    <span data-ttu-id="957dc-355">![工程更改请求](media/eng-change-request.png "工程更改请求")</span><span class="sxs-lookup"><span data-stu-id="957dc-355">![Engineering change request](media/eng-change-request.png "Engineering change request")</span></span>

1. <span data-ttu-id="957dc-356">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-356">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="957dc-357">请注意，物料已自动添加到 **产品** 快速选项卡上，并且工程更改请求的来源（销售订单）已添加到 **来源** 快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="957dc-357">Notice that the item has automatically been added on the **Products** FastTab, and that the source of the engineering change request (the sales order) has been added on the **Source** FastTab.</span></span>

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a><span data-ttu-id="957dc-358">使用工程更改订单对产品进行更改</span><span class="sxs-lookup"><span data-stu-id="957dc-358">Make changes to the product by using an engineering change order</span></span>

<span data-ttu-id="957dc-359">销售人员知道产品很重要，并且专为客户而设计。</span><span class="sxs-lookup"><span data-stu-id="957dc-359">The sales clerk knows that the product is important and was designed especially for the customer.</span></span> <span data-ttu-id="957dc-360">因此，销售人员致电 *DEMF* 公司中的工程师来通知他们更改请求。</span><span class="sxs-lookup"><span data-stu-id="957dc-360">Therefore, the sales clerk calls an engineer in the *DEMF* company to notify them about the change request.</span></span> <span data-ttu-id="957dc-361">这样，工程师可以加快流程。</span><span class="sxs-lookup"><span data-stu-id="957dc-361">In this way, the engineer can speed up the process.</span></span>

<span data-ttu-id="957dc-362">工程师现在审查客户的请求并为产品创建更改订单。</span><span class="sxs-lookup"><span data-stu-id="957dc-362">The engineer now reviews the request from the customer and creates a change order for the product.</span></span>

1. <span data-ttu-id="957dc-363">因为工程师任职于 *DEMF* 公司，因此将法人设置为 *DEMF*。</span><span class="sxs-lookup"><span data-stu-id="957dc-363">Because the engineer works in the *DEMF* company, set the legal entity to *DEMF*.</span></span> <span data-ttu-id="957dc-364">（使用导航栏右侧的公司选择器。）</span><span class="sxs-lookup"><span data-stu-id="957dc-364">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="957dc-365">转到 **工程更改管理 &gt; 通用 &gt; 工程更改请求**。</span><span class="sxs-lookup"><span data-stu-id="957dc-365">Go to **Engineering change management &gt; Common &gt; Engineering change requests**.</span></span>
1. <span data-ttu-id="957dc-366">打开更改请求 *555*。</span><span class="sxs-lookup"><span data-stu-id="957dc-366">Open change request *555*.</span></span>
1. <span data-ttu-id="957dc-367">查看信息，然后审核更改。</span><span class="sxs-lookup"><span data-stu-id="957dc-367">Review the information, and then approve the change.</span></span> <span data-ttu-id="957dc-368">在操作窗格的 **更改请求** 选项卡上，在 **更改状态** 组中，选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="957dc-368">On the Action Pane, on the **Change request** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="957dc-369">转到 **工程更改管理 &gt; 通用 &gt; 工程更改订单**。</span><span class="sxs-lookup"><span data-stu-id="957dc-369">Go to **Engineering change management &gt; Common &gt; Engineering change orders**.</span></span>
1. <span data-ttu-id="957dc-370">在操作窗格上，选择 **新建** 以创建更改订单，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-370">On the Action Pane, select **New** to create a change order, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-371">\**更改订单：\*\*\*555*</span><span class="sxs-lookup"><span data-stu-id="957dc-371">**Change order:** *555*</span></span>
    - <span data-ttu-id="957dc-372">\**标题：\*\*\*Z0001 客户更改*</span><span class="sxs-lookup"><span data-stu-id="957dc-372">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="957dc-373">\**类别：\*\*\*客户更改*</span><span class="sxs-lookup"><span data-stu-id="957dc-373">**Category:** *Customer change*</span></span>
    - <span data-ttu-id="957dc-374">\**优先级：\*\*\*低*</span><span class="sxs-lookup"><span data-stu-id="957dc-374">**Priority:** *Low*</span></span>
    - <span data-ttu-id="957dc-375">\**严重性：\*\*\*中*</span><span class="sxs-lookup"><span data-stu-id="957dc-375">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="957dc-376">在 **受影响产品** 快速选项卡上，选择 **新建 &gt; 添加现有产品** 以向网格添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="957dc-376">On the **Impacted products** FastTab, select **New &gt; Add existing product** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="957dc-377">\**产品：\*\*\*Z0001*</span><span class="sxs-lookup"><span data-stu-id="957dc-377">**Product:** *Z0001*</span></span>
    - <span data-ttu-id="957dc-378">\**影响：\*\*\*新版本*</span><span class="sxs-lookup"><span data-stu-id="957dc-378">**Impact:** *New version*</span></span>

    <span data-ttu-id="957dc-379">![创建工程更改订单](media/eng-change-order.png "创建工程更改订单")</span><span class="sxs-lookup"><span data-stu-id="957dc-379">![Creating an engineering change order](media/eng-change-order.png "Creating an engineering change order")</span></span>

1. <span data-ttu-id="957dc-380">请注意，因为您将 **影响** 字段设置为 *新版本*，因此 **产品详细信息** 快速选项卡的 **详细信息** 选项卡上的 **新版本** 字段将显示新的版本号（对于此示例为 *V-02*）。</span><span class="sxs-lookup"><span data-stu-id="957dc-380">Notice that, because you set the **Impact** field to *New version*, the **New version** field on the **Details** tab of the **Product details** FastTab shows what the new version number will be (*V-02* for this example).</span></span>

    <span data-ttu-id="957dc-381">![工程更改订单的产品详细信息](media/eng-change-order-product-details.png "工程更改订单的产品详细信息")</span><span class="sxs-lookup"><span data-stu-id="957dc-381">![Product details for an engineering change order](media/eng-change-order-product-details.png "Product details for an engineering change order")</span></span>

1. <span data-ttu-id="957dc-382">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-382">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="957dc-383">在 **产品详细信息** 快速选项卡的 **物料清单** 选项卡上，选择 **行** 以打开产品 *Z0001* 的版本 *V-01* 的 BOM。</span><span class="sxs-lookup"><span data-stu-id="957dc-383">On the **Product details** FastTab, on the **Bill of material** tab, select **Lines** to open the BOM for version *V-01* of product *Z0001*.</span></span>

    <span data-ttu-id="957dc-384">![工程产品 BOM 行](media/eng-product-bom-lines.png "工程产品 BOM 行")</span><span class="sxs-lookup"><span data-stu-id="957dc-384">![Engineering product BOM lines](media/eng-product-bom-lines.png "Engineering product BOM lines")</span></span>

1. <span data-ttu-id="957dc-385">选择物料编号 *D0003* 的行，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="957dc-385">Select the line for item number *D0003*, and then, on the Action Pane, select **Delete**.</span></span> <span data-ttu-id="957dc-386">此行的 **更改类型** 字段的值将更改为 *已删除*。</span><span class="sxs-lookup"><span data-stu-id="957dc-386">The value of the **Change type** field for this line changes to *Deleted*.</span></span>
1. <span data-ttu-id="957dc-387">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="957dc-387">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="957dc-388">![已修改工程产品 BOM 行](media/eng-product-bom-lines-modified.png "已修改工程产品 BOM 行")</span><span class="sxs-lookup"><span data-stu-id="957dc-388">![Modified engineering product BOM lines](media/eng-product-bom-lines-modified.png "Modified engineering product BOM lines")</span></span>

1. <span data-ttu-id="957dc-389">关闭 **BOM 行** 页面以返回到 **工程更改订单** 页面。</span><span class="sxs-lookup"><span data-stu-id="957dc-389">Close the **BOM line** page to return to the **Engineering change order** page.</span></span>
1. <span data-ttu-id="957dc-390">请注意，在 **产品详细信息** 快速选项卡的 **物料清单** 选项卡上，BOM *Z0001* 的 **更改类型** 字段的值现在为 *已更改*。</span><span class="sxs-lookup"><span data-stu-id="957dc-390">On the **Product details** FastTab, on the **Bill of material** tab, notice that the value of the **Change type** field for BOM *Z0001* is now *Changed*.</span></span>

    <span data-ttu-id="957dc-391">![包含已更改 BOM 的工程更改订单](media/eng-change-order-changed-bom.png "包含已更改 BOM 的工程更改订单")</span><span class="sxs-lookup"><span data-stu-id="957dc-391">![Engineering change order that includes a changed BOM](media/eng-change-order-changed-bom.png "Engineering change order that includes a changed BOM")</span></span>

    <span data-ttu-id="957dc-392">现在，必须先审核订单，才能处理更改。</span><span class="sxs-lookup"><span data-stu-id="957dc-392">The order must now be approved before the changes can be processed.</span></span> <span data-ttu-id="957dc-393">处理更改后，将使用工程更改订单中包含的更改更新产品。</span><span class="sxs-lookup"><span data-stu-id="957dc-393">When the changes are processed, the products are updated with the changes that are included in the engineering change order.</span></span> <span data-ttu-id="957dc-394">对于此示例，已将创建工程更改订单的人指定为审批者。</span><span class="sxs-lookup"><span data-stu-id="957dc-394">For this example, the person who creates the engineering change order has been specified as the approver.</span></span>

1. <span data-ttu-id="957dc-395">在操作窗格的 **更改订单** 选项卡上，在 **更改状态** 组中，选择 **审核**。</span><span class="sxs-lookup"><span data-stu-id="957dc-395">On the Action Pane, on the **Change order** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="957dc-396">选择 **处理** 以更新产品的信息。</span><span class="sxs-lookup"><span data-stu-id="957dc-396">Select **Process** to update the product's information.</span></span>

## <a name="release-the-changed-product"></a><span data-ttu-id="957dc-397">发布更改的产品</span><span class="sxs-lookup"><span data-stu-id="957dc-397">Release the changed product</span></span>

<span data-ttu-id="957dc-398">现在，产品可以再次发布到 *USMF* 公司，然后发送给客户。</span><span class="sxs-lookup"><span data-stu-id="957dc-398">The product can now be released again to the *USMF* company and then sent to the customer.</span></span> <span data-ttu-id="957dc-399">若要直接从工程更改订单中发布产品，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="957dc-399">To release the product directly from the engineering change order, follow these steps.</span></span>

1. <span data-ttu-id="957dc-400">打开您在上一个练习中创建的工程更改订单（如果尚未打开）。</span><span class="sxs-lookup"><span data-stu-id="957dc-400">Open the engineering change order that you created in the previous exercise, if it isn't already open.</span></span>
1. <span data-ttu-id="957dc-401">在操作窗格的 **更改订单** 选项卡上，在 **产品发布** 组中，选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="957dc-401">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Search**.</span></span>
1. <span data-ttu-id="957dc-402">搜索结果显示已向哪些公司发布了受影响的产品。</span><span class="sxs-lookup"><span data-stu-id="957dc-402">The search results show which companies the affected products have been released to.</span></span> <span data-ttu-id="957dc-403">关闭搜索结果。</span><span class="sxs-lookup"><span data-stu-id="957dc-403">Close the search results.</span></span>
1. <span data-ttu-id="957dc-404">在操作窗格的 **更改订单** 选项卡上，在 **产品发布** 组中，选择 **视图** 以打开 **发布** 对话框，您可以在其中查看上一次搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="957dc-404">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **View** to open the **Releases** dialog box, where you can view the results of the previous search.</span></span>
1. <span data-ttu-id="957dc-405">选择要向其发布产品的每个公司。</span><span class="sxs-lookup"><span data-stu-id="957dc-405">Select each company that you want to release products to.</span></span>
1. <span data-ttu-id="957dc-406">选择 **确定** 以关闭 **发布** 对话框并返回到更改订单。</span><span class="sxs-lookup"><span data-stu-id="957dc-406">Select **OK** to close the **Releases** dialog box and return to the change order.</span></span>
1. <span data-ttu-id="957dc-407">在操作窗格的 **更改订单** 选项卡上，在 **产品发布** 组中，选择 **处理** 以将受影响的产品发布给所选公司。</span><span class="sxs-lookup"><span data-stu-id="957dc-407">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Process** to release the affected products to the selected companies.</span></span> <span data-ttu-id="957dc-408">或者，选择 **发布产品结构** 以启动发布流程。</span><span class="sxs-lookup"><span data-stu-id="957dc-408">Alternatively, select **Release product structure** to start the release process.</span></span>

## <a name="complete-the-change-order"></a><span data-ttu-id="957dc-409">完成更改订单</span><span class="sxs-lookup"><span data-stu-id="957dc-409">Complete the change order</span></span>

<span data-ttu-id="957dc-410">要将更改订单标记为已完成，指示没有其他操作，在操作窗格中选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="957dc-410">To mark the change order as completed, which indicates that no further actions remain, select **Complete** on the Action Pane.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
