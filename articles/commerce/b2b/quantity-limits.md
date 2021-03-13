---
title: 设置 B2B 电子商务站点的产品数量限制
description: 本主题介绍如何为企业到企业 (B2B) 电子商务站点设置产品数量限制。
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e70648da2cc1c526625b6e34fd0867d40abb5a85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035877"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="61913-103">设置 B2B 电子商务站点的产品数量限制</span><span class="sxs-lookup"><span data-stu-id="61913-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61913-104">本主题介绍如何为企业到企业 (B2B) 电子商务站点设置产品数量限制。</span><span class="sxs-lookup"><span data-stu-id="61913-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="61913-105">大多数产品都有一个定义其分组的度量单位。</span><span class="sxs-lookup"><span data-stu-id="61913-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="61913-106">分组将影响产品的销售方式。</span><span class="sxs-lookup"><span data-stu-id="61913-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="61913-107">有些产品可能还有额外的数量分组。</span><span class="sxs-lookup"><span data-stu-id="61913-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="61913-108">此分组确定产品是单个还是多个出售，以及是否有必须遵循的最小或最大订购数量限制。</span><span class="sxs-lookup"><span data-stu-id="61913-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="61913-109">数量限制功能可确保将 Microsoft Dynamics 365 Commerce 中配置的最小、最大、多个和标准数量（在默认订单设置或 Commerce 站点构建器站点设置中）应用于在电子商务站点上下的客户订单。</span><span class="sxs-lookup"><span data-stu-id="61913-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="61913-110">销售点 (POS) 和呼叫中心当前不支持产品数量限制。</span><span class="sxs-lookup"><span data-stu-id="61913-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="61913-111">很多零售商提供客户订单（也称特殊订单）选项，以满足各种产品和履行要求。</span><span class="sxs-lookup"><span data-stu-id="61913-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="61913-112">下面是一些典型方案：</span><span class="sxs-lookup"><span data-stu-id="61913-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="61913-113">客户希望特定变型的产品能够以几个的倍数销售。</span><span class="sxs-lookup"><span data-stu-id="61913-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="61913-114">客户希望从非购买产品的商店或位置取货。</span><span class="sxs-lookup"><span data-stu-id="61913-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="61913-115">但是，商店的包装标准不同于在线销售分配的包装标准。</span><span class="sxs-lookup"><span data-stu-id="61913-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="61913-116">客户想要购买限量版产品，该产品对可购买件数有最大数量限制。</span><span class="sxs-lookup"><span data-stu-id="61913-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="61913-117">在 Commerce headquarters 中打开默认订单设置功能</span><span class="sxs-lookup"><span data-stu-id="61913-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="61913-118">您必须先在 Commerce headquarters 中启用默认订单设置功能，然后才能够设置产品数量限制。</span><span class="sxs-lookup"><span data-stu-id="61913-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="61913-119">要打开默认订单设置功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="61913-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="61913-120">转到 **系统管理 \> 工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="61913-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="61913-121">找到并选择 **在客户订单中支持站点和默认订单设置** 功能。</span><span class="sxs-lookup"><span data-stu-id="61913-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="61913-122">在右窗格的底部，选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="61913-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="61913-123">定义数量设置</span><span class="sxs-lookup"><span data-stu-id="61913-123">Define quantity settings</span></span> 

<span data-ttu-id="61913-124">您可以在 **默认订单设置** 页面上定义数量设置。</span><span class="sxs-lookup"><span data-stu-id="61913-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="61913-125">要定义数量设置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="61913-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="61913-126">转到产品 **Retail 和 Commerce \> 产品和类别 \> 按类别发布的产品**。</span><span class="sxs-lookup"><span data-stu-id="61913-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="61913-127">选择一个已发布产品。</span><span class="sxs-lookup"><span data-stu-id="61913-127">Select a released product.</span></span>
1. <span data-ttu-id="61913-128">在操作窗格上，在 **管理库存** 选项卡上的 **订单设置** 组中，选择 **默认订单设置**。</span><span class="sxs-lookup"><span data-stu-id="61913-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="61913-129">在 **默认订单设置** 页上的 **销售订单** 快速选项卡上，在 **销售数量** 部分，设置产品销售数量：</span><span class="sxs-lookup"><span data-stu-id="61913-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="61913-130">**倍数** – 产品可以其倍数购买的数量。</span><span class="sxs-lookup"><span data-stu-id="61913-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="61913-131">**最小订单数量** – 必须购买的最少产品数量。</span><span class="sxs-lookup"><span data-stu-id="61913-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="61913-132">**最大订单数量** – 可以购买的最多产品数量。</span><span class="sxs-lookup"><span data-stu-id="61913-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="61913-133">**标准订单数量** – 选择产品时自动输入的默认数量。</span><span class="sxs-lookup"><span data-stu-id="61913-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="61913-134">在 Commerce 站点构建器中打开 B2B 订单数量限制功能</span><span class="sxs-lookup"><span data-stu-id="61913-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="61913-135">要在 Commerce 站点构建器中打开 B2B 订单数量限制功能，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="61913-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="61913-136">转到 **站点设置 \> 扩展**</span><span class="sxs-lookup"><span data-stu-id="61913-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="61913-137">在 **启用订单数量限制** 下，在下拉菜单中选择 **为 B2B 客户启用**。</span><span class="sxs-lookup"><span data-stu-id="61913-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="61913-138">更新的站点构建器设置仅在更新 app.settings.json 文件后才会生效。</span><span class="sxs-lookup"><span data-stu-id="61913-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="61913-139">有关详细信息，请参阅 [SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="61913-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61913-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="61913-140">Additional resources</span></span>

[<span data-ttu-id="61913-141">建立 B2B 电子商务站点</span><span class="sxs-lookup"><span data-stu-id="61913-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="61913-142">为 B2B 组织创建组织建模层次结构</span><span class="sxs-lookup"><span data-stu-id="61913-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="61913-143">在 B2B 电子商务站点上管理业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="61913-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="61913-144">配置 B2B 电子商务站点的客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="61913-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)
