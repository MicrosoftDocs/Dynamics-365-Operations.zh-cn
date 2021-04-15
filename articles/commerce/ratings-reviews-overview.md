---
title: 评分和评价概览
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的评分和评价。
author: gvrmohanreddy
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0788091755fb784621e972a0573f7004952e8e11
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792091"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="cf193-103">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="cf193-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cf193-104">此主题介绍 Microsoft Dynamics 365 Commerce 中的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="cf193-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf193-105">概览</span><span class="sxs-lookup"><span data-stu-id="cf193-105">Overview</span></span>

<span data-ttu-id="cf193-106">对于希望了解其他客户对产品的看法的电子商务客户来说，评分和评价至关重要。</span><span class="sxs-lookup"><span data-stu-id="cf193-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="cf193-107">它们还可以帮助消费者进行购买决定。</span><span class="sxs-lookup"><span data-stu-id="cf193-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="cf193-108">在 Dynamics 365 Commerce 中，零售商可通过评分和评价解决方案捕获客户对产品的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="cf193-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="cf193-109">然后，零售商可以显示自己电子商务网站中的平均评分和评价信息。</span><span class="sxs-lookup"><span data-stu-id="cf193-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="cf193-110">将在销售点 (POS) 和呼叫中心渠道中显示平均评分信息。</span><span class="sxs-lookup"><span data-stu-id="cf193-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="cf193-111">因此，销售助理可将其用于帮助用户做出决定。</span><span class="sxs-lookup"><span data-stu-id="cf193-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="cf193-112">评分和评价还可以充当反馈机制，供零售商用于提高产品质量，从而提高销售额。</span><span class="sxs-lookup"><span data-stu-id="cf193-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="cf193-113">Dynamics 365 Commerce 中的评分和评价功能是全渠道解决方案，在平台中本机提供。</span><span class="sxs-lookup"><span data-stu-id="cf193-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="cf193-114">评分和评价解决方案基于 Microsoft Azure 生成，可提供高度的可伸缩性和可靠性。</span><span class="sxs-lookup"><span data-stu-id="cf193-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="cf193-115">下图显示评分和评价解决方案在 Dynamics 365 Commerce 中如何工作。</span><span class="sxs-lookup"><span data-stu-id="cf193-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Dynamics 365 for Commerce 中的评分和评价](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="cf193-117">Dynamics 365 Commerce 中的评分和评价解决方案使用 Azure Cognitive Services 自动审查 40 种语言的猥亵词。</span><span class="sxs-lookup"><span data-stu-id="cf193-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="cf193-118">因为无需人员审核，所以降低了审查成本。</span><span class="sxs-lookup"><span data-stu-id="cf193-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="cf193-119">系统还提供审查者工具，可用于响应客户的疑虑、反馈和撤下请求，以及解决用户的数据申请。</span><span class="sxs-lookup"><span data-stu-id="cf193-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="cf193-120">评分和评价解决方案提供小组件，这些小组件在产品列表、搜索结果、产品详细信息页和其他位置显示评分汇总。</span><span class="sxs-lookup"><span data-stu-id="cf193-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="cf193-121">这些小组件显示完整的评价列表，还提供排序和筛选选项。</span><span class="sxs-lookup"><span data-stu-id="cf193-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="cf193-122">评分和评价解决方案还提供商业智能 (BI) 模板，该模板中包含一组度量，用于提供有关评分和评价的见解。</span><span class="sxs-lookup"><span data-stu-id="cf193-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="cf193-123">可以导出评分和评价数据，以便进行更深入的分析。</span><span class="sxs-lookup"><span data-stu-id="cf193-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf193-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="cf193-124">Additional resources</span></span>

[<span data-ttu-id="cf193-125">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="cf193-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="cf193-126">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="cf193-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="cf193-127">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="cf193-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="cf193-128">在 Dynamics 365 Commerce 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="cf193-128">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]