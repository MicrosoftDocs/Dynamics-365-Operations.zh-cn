---
title: 设置在线商店渠道
description: 本文提供有关在线商店渠道以及如何在 Dynamics 365 Commerce 中设置它们的信息。
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096886"
---
# <a name="set-up-an-online-store-channel"></a><span data-ttu-id="8a5e3-103">设置在线商店渠道</span><span class="sxs-lookup"><span data-stu-id="8a5e3-103">Set up an online store channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a5e3-104">本文提供有关在线商店渠道以及如何在 Dynamics 365 Commerce 中设置它们的信息。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-104">This article provides information about online store channels and how to set them up in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8a5e3-105">Commerce 支持多个零售渠道。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-105">Commerce supports multiple retail channels.</span></span> <span data-ttu-id="8a5e3-106">这些渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-106">These channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="8a5e3-107">在线商店为零售商提供在线形式，使其客户除零售商店外可从零售商的在线商店采购产品。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-107">Online stores give an online presence to a retailer, so that customers can purchase products from the retailer's online store in addition to its retail stores.</span></span> <span data-ttu-id="8a5e3-108">如果顾客在在线商店采购产品，产品可以邮寄给他们，或者客户可以在当地商店领取产品。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-108">If customers purchase products from the online store, those products can be shipped to them, or the customers can pick the products up at a local store.</span></span> 

<span data-ttu-id="8a5e3-109">可在 Commerce 客户端创建在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-109">You create an online store in the Commerce client.</span></span> <span data-ttu-id="8a5e3-110">此在线商店然后将发布到与 Commerce 集成的第三方在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-110">This online store is then published to a third-party online store that is integrated with Commerce.</span></span> <span data-ttu-id="8a5e3-111">第三方在线商店用作在线商店的店面 (UI)，并向您提供客户管理系统 (CMS) 和 UI 功能的选择。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-111">The third-party online store serves as the storefront (UI) for the online store, and gives you a choice of customer management system (CMS) and UI capabilities.</span></span> <span data-ttu-id="8a5e3-112">此类型的多个集成可用。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-112">Several integrations of this type are available.</span></span> 

<span data-ttu-id="8a5e3-113">您为在线商店定义的属性将控制在线商店的行为。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-113">The properties that you define for the online store control the behavior of the online store.</span></span> <span data-ttu-id="8a5e3-114">例如，您定义导航类别层次结构，并将其分配给在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-114">For example, you define the navigation category hierarchy and assign it to the online store.</span></span> <span data-ttu-id="8a5e3-115">将在线商店发布到第三方在线商店后，导航类别层次结构会显示在商店的在线版本中。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-115">When you publish the online store to the third-party online store, the navigation category hierarchy appears in the online version of the store.</span></span> <span data-ttu-id="8a5e3-116">购物者然后将导航类别层次结构用于浏览在线商店和搜索产品。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-116">Shoppers then use the navigation category hierarchy to browse the online store and search for products.</span></span> 

<span data-ttu-id="8a5e3-117">若要创建在线商店，您必须设置允许为商店处理交易记录的组件。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-117">To create an online store, you must set up the components that enable transactions to be processed for the store.</span></span> <span data-ttu-id="8a5e3-118">例如，您必须添加分类、应用属性和设置付款方式和装运方法。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-118">For example, you must add assortments, apply attributes, and set up payment methods and shipping methods.</span></span> <span data-ttu-id="8a5e3-119">还可以定义价格、促销、折扣、贸易协议和特定于在线商店的装运条件。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-119">You can also define prices, promotions, discounts, trade agreements, and shipping terms that are specific to the online store.</span></span> 

<span data-ttu-id="8a5e3-120">将在线商店发布到第三方在线商店后，您可以为在线商店创建产品目录。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-120">After you publish the online store to the third-party online store, you can create product catalogs for the online store.</span></span> <span data-ttu-id="8a5e3-121">目录中的产品就是在线商店中的产品清单。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-121">The products in the catalog become product listings in the online store.</span></span> <span data-ttu-id="8a5e3-122">顾客从在线商店采购产品时，系统会在客户端更新和同步可用库存。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-122">When a shopper purchases products from the online store, the available inventory is updated and synchronized in the client.</span></span> <span data-ttu-id="8a5e3-123">此外，还会为采购生成销售订单并发送到客户端，以便执行和处理订单。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-123">Additionally, sales orders are generated for the purchases, and are sent to the client for order fulfillment and processing.</span></span>

## <a name="set-up-an-online-store"></a><span data-ttu-id="8a5e3-124">设置在线商店</span><span class="sxs-lookup"><span data-stu-id="8a5e3-124">Set up an online store</span></span>

<span data-ttu-id="8a5e3-125">若要设置在线商店，必须完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-125">To set up an online store, you must complete the following tasks.</span></span>

1. <span data-ttu-id="8a5e3-126">创建在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-126">Create the online store.</span></span>
2. <span data-ttu-id="8a5e3-127">将在线商店添加到相应组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-127">Add the online store to the appropriate organization hierarchies.</span></span>
3. <span data-ttu-id="8a5e3-128">添加包括在线商店中可用的产品的分类。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-128">Add assortments that include the products that are available in the online store.</span></span>
4. <span data-ttu-id="8a5e3-129">为在线商店分配或创建价格组。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-129">Assign or create price groups for the online store.</span></span>
5. <span data-ttu-id="8a5e3-130">设置在线商店可用的交货方式。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-130">Set up the modes of delivery that are available for the online store.</span></span>
6. <span data-ttu-id="8a5e3-131">分配在线商店接受的付款方式。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-131">Assign the payment methods that are accepted by the online store.</span></span>
7. <span data-ttu-id="8a5e3-132">如果您允许顾客在线订购产品，然后在当地商店领取，则将商店定位符组分配给在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-132">If you allow shoppers to order products online and then pick them up at a local store, assign store locator groups to the online store.</span></span>
8. <span data-ttu-id="8a5e3-133">将渠道、产品和销售订单的属性分配给在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-133">Assign attributes for channels, products, and sales orders to the online store.</span></span> <span data-ttu-id="8a5e3-134">渠道属性适用于整个在线商店，产品属性适用于在线商店中提供的产品，而销售订单属性适用于从在线商店生成的销售订单。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-134">Channel attributes apply to the whole online store, product attributes apply to the products that are offered in the online store, and sales order attributes apply to the sales orders that are generated from the online store.</span></span>
9. <span data-ttu-id="8a5e3-135">映射特性以定义决定这些特性在在线商店中的行为方式的属性。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-135">Map attributes to define the properties that determine how those attributes behave in the online store.</span></span> <span data-ttu-id="8a5e3-136">例如，属性可以定义为必需或可搜索。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-136">For example, attributes can be defined as required or searchable.</span></span>
10. <span data-ttu-id="8a5e3-137">发布在线商店以在您选择的第三方在线商店中生成商店结构。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-137">Publish the online store to generate the store structure on your choice of third-party online store.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8a5e3-138">在发布在线商店之前，必须为在线商店设置配送地。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-138">Before you publish the online store, you must set up a distribution location for it.</span></span>

## <a name="commerce-channel-navigation-hierarchies"></a><span data-ttu-id="8a5e3-139">Commerce 渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="8a5e3-139">Commerce channel navigation hierarchies</span></span>

<span data-ttu-id="8a5e3-140">必须先定义您用于在线商店的商业渠道导航层次结构，然后才能创建在线商店。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-140">Before you create an online store, you must define the commerce channel navigation hierarchy that you want to use for it.</span></span> <span data-ttu-id="8a5e3-141">渠道导航层次结构表示发布商店后显示在在线商店中的类别导航。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-141">The channel navigation hierarchy represents the category hierarchy that is displayed in the online store after the store is published.</span></span> <span data-ttu-id="8a5e3-142">将产品目录发布到在线商店时，目录中的产品会映射到渠道导航层次结构中的目录。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-142">When you publish product catalogs to the online store, the products in the catalog are mapped to the categories in the channel navigation hierarchy.</span></span> <span data-ttu-id="8a5e3-143">顾客然后使用该层次结构在在线商店中进行导航。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-143">Shoppers then use the hierarchy to navigate in the online store.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="8a5e3-144">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="8a5e3-144">Organization hierarchies</span></span>

<span data-ttu-id="8a5e3-145">组织层次结构用于构建商业渠道，其体现了构成您的公司的各个组织之间的关系。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-145">Organization hierarchies are used to structure commerce channels and to represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="8a5e3-146">设置在线商店时，您可以将这些商店添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-146">When you set up online stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="8a5e3-147">然后，商店共享用于分类、补货和报告的数据。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-147">The stores then share the data that is used for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="8a5e3-148">在您创建某一组织层次结构时，将目标分配给它。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-148">When you create an organization hierarchy, you assign a purpose to it.</span></span> <span data-ttu-id="8a5e3-149">目标指示层次结构如何在业务结构中使用。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-149">The purpose indicates how the hierarchy is used in the business structure.</span></span> <span data-ttu-id="8a5e3-150">您可以为商店运营创建一个组织层次结构，并使用层次结构为您的商店分类、补货和报告。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-150">You can create one organization hierarchy for your store operations, and use that hierarchy for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="8a5e3-151">或者，您可以为每个目标创建单独的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-151">Alternatively, you can create a separate organization hierarchy for each purpose.</span></span> <span data-ttu-id="8a5e3-152">您还可以创建具有相同目标的多个层次结构，然后将单独渠道分配给每个层次结构。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-152">You can also create multiple hierarchies that have the same purpose, and assign a separate channel to each one.</span></span> <span data-ttu-id="8a5e3-153">如果您计划将产品目录发布到在线商店，则您应该至少将在线商店添加到组织层次结构中以便进行分类。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-153">If you plan to publish product catalogs to the online store, you should, at a minimum, add the online store to an organization hierarchy for assortments.</span></span> <span data-ttu-id="8a5e3-154">目录中的产品是从分配给在线商店的分类中选择的。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-154">The products in a catalog are selected from the assortments that are assigned to the online store.</span></span> <span data-ttu-id="8a5e3-155">发布目录时，发布流程会将分配给在线商店的分类的有效日期与目录中包括的产品作比较，以便确定要使哪些产品在在线商店中可用。</span><span class="sxs-lookup"><span data-stu-id="8a5e3-155">When the catalog is published, the publishing process compares the effective dates for the assortment that is assigned to the online store with the products that are included in the catalog to determine which products to make available in the online store.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a5e3-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="8a5e3-156">Additional resources</span></span>

[<span data-ttu-id="8a5e3-157">配置域名</span><span class="sxs-lookup"><span data-stu-id="8a5e3-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8a5e3-158">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="8a5e3-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8a5e3-159">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="8a5e3-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8a5e3-160">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="8a5e3-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8a5e3-161">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="8a5e3-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8a5e3-162">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="8a5e3-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8a5e3-163">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="8a5e3-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8a5e3-164">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="8a5e3-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8a5e3-165">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="8a5e3-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8a5e3-166">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="8a5e3-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8a5e3-167">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="8a5e3-167">Enable location-based store detection</span></span>](enable-store-detection.md)
