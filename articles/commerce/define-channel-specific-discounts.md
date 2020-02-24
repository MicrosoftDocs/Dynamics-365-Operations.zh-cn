---
title: 定义渠道特定的折扣
description: 零售商通常为不同渠道设置不同折扣。 此主题审查您为特定渠道创建折扣所需了解的概念。
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021698"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="17143-104">定义特定于渠道的折扣</span><span class="sxs-lookup"><span data-stu-id="17143-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17143-105">此主题审查您为特定渠道创建折扣所需了解的概念。</span><span class="sxs-lookup"><span data-stu-id="17143-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="17143-106">渠道特定的折扣</span><span class="sxs-lookup"><span data-stu-id="17143-106">Channel-specific discounts</span></span>

<span data-ttu-id="17143-107">零售商通常为不同渠道提供不同折扣。</span><span class="sxs-lookup"><span data-stu-id="17143-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="17143-108">这样做可以应对市场情况或对付竞争零售商。</span><span class="sxs-lookup"><span data-stu-id="17143-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="17143-109">Commerce 使用价格组来定义渠道特定的折扣。</span><span class="sxs-lookup"><span data-stu-id="17143-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="17143-110">价格组可分配给以下一个或多个实体：渠道、目录、隶属关系和会员计划。</span><span class="sxs-lookup"><span data-stu-id="17143-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="17143-111">本文讨论渠道，不过，相同的概念适用于目录折扣、隶属关系折扣和会员折扣。</span><span class="sxs-lookup"><span data-stu-id="17143-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="17143-112">价格组</span><span class="sxs-lookup"><span data-stu-id="17143-112">Price groups</span></span>

<span data-ttu-id="17143-113">[![价格组](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="17143-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="17143-114">上图说明可以位于交易记录上的实体（渠道、目录、隶属关系、客户、会员卡）和可以配置的不同折扣类型之间的关系。</span><span class="sxs-lookup"><span data-stu-id="17143-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="17143-115">所有交易记录都在渠道中进行，因此，要确保渠道存在于交易记录上。</span><span class="sxs-lookup"><span data-stu-id="17143-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="17143-116">剩余的实体是可选的。</span><span class="sxs-lookup"><span data-stu-id="17143-116">The remaining entities are optional.</span></span> <span data-ttu-id="17143-117">在每个主数据页上，都有一个指向相关价格组的链接，您可以根据需要在其中查看和添加价格组。</span><span class="sxs-lookup"><span data-stu-id="17143-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="17143-118">价格组用于将四个不同类型的实体关联到折扣、价格调整和贸易协议。</span><span class="sxs-lookup"><span data-stu-id="17143-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="17143-119">我们建议您针对如何命名价格组以使其组织有序规划一种策略。</span><span class="sxs-lookup"><span data-stu-id="17143-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="17143-120">一个选项是使用字母或数字前缀或后缀来区分不同类型。</span><span class="sxs-lookup"><span data-stu-id="17143-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="17143-121">例如，渠道价格组的 1-xxxxx 和目录价格组的 2-xxxxx。</span><span class="sxs-lookup"><span data-stu-id="17143-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="17143-122">有四个查询页侧重于每个可以具有与其关联的折扣的商业实体。</span><span class="sxs-lookup"><span data-stu-id="17143-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="17143-123">**渠道价格组** - 此页显示每个价格组的彼此链接的渠道和折扣的列表。</span><span class="sxs-lookup"><span data-stu-id="17143-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="17143-124">**目录价格组** – 此页显示每个价格组的彼此链接的目录和折扣的列表。</span><span class="sxs-lookup"><span data-stu-id="17143-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="17143-125">**会员价格组** – 此页显示每个价格组的彼此链接的会员计划和折扣的列表。</span><span class="sxs-lookup"><span data-stu-id="17143-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="17143-126">**隶属关系价格组** – 此页显示每个价格组的彼此链接的隶属关系和折扣的列表。</span><span class="sxs-lookup"><span data-stu-id="17143-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="17143-127">渠道折扣设置示例</span><span class="sxs-lookup"><span data-stu-id="17143-127">Example channel discount set up</span></span>

<span data-ttu-id="17143-128">以下示例说明在设置渠道折扣中涉及的任务。</span><span class="sxs-lookup"><span data-stu-id="17143-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="17143-129">对于本示例，您有一个名为**Houston**的渠道，您打算创建名为**返回学校**的新折扣。</span><span class="sxs-lookup"><span data-stu-id="17143-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="17143-130">由于价格和折扣策略包括渠道折扣的可能性，因此在您创建渠道时，您始终创建渠道特定的价格组。</span><span class="sxs-lookup"><span data-stu-id="17143-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="17143-131">您可以有价格组**Houston-PG**，它分配给**Houston**渠道。</span><span class="sxs-lookup"><span data-stu-id="17143-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="17143-132">在您创建新的**返回学校**折扣后，需要单击**折扣**页顶部的**价格组**。</span><span class="sxs-lookup"><span data-stu-id="17143-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="17143-133">**折扣价格组**页将打开。</span><span class="sxs-lookup"><span data-stu-id="17143-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="17143-134">接下来，单击**新建**，选择**Houston-PG**价格组。</span><span class="sxs-lookup"><span data-stu-id="17143-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="17143-135">现在您可以启用折扣并将其推送到渠道。</span><span class="sxs-lookup"><span data-stu-id="17143-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17143-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="17143-136">Additional resources</span></span>

[<span data-ttu-id="17143-137">价格调整和折扣</span><span class="sxs-lookup"><span data-stu-id="17143-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
