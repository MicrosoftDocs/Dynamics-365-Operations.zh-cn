---
title: 应用度量单位设置
description: 本主题介绍度量单位设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c5750ae506978dfac842eebf4ba6036322bdd7f
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937566"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="919eb-103">应用度量单位设置</span><span class="sxs-lookup"><span data-stu-id="919eb-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="919eb-104">本主题介绍度量单位设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="919eb-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="919eb-105">产品可以按不同的单位出售，如“每个”、“对”和“一打”。</span><span class="sxs-lookup"><span data-stu-id="919eb-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="919eb-106">在 Commerce headquarters 中，可以为产品定义销售度量单位，并在电子商务站点上显示。</span><span class="sxs-lookup"><span data-stu-id="919eb-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="919eb-107">例如，如果零售商既单个销售又成打销售产品，则可以将可用的度量单位与其他产品信息一起显示。</span><span class="sxs-lookup"><span data-stu-id="919eb-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="919eb-108">在下图中的示例中，已在 Commerce headquarters 中为产品配置了销售度量单位 **ea**（每个）。</span><span class="sxs-lookup"><span data-stu-id="919eb-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![在 Commerce headquarters 中配置了度量单位的产品示例](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="919eb-110">从 Commerce 版本 10.0.19 开始提供应用和显示度量单位的支持。</span><span class="sxs-lookup"><span data-stu-id="919eb-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="919eb-111">度量单位设置</span><span class="sxs-lookup"><span data-stu-id="919eb-111">Unit of measure settings</span></span>

<span data-ttu-id="919eb-112">度量单位显示设置是在 Commerce 站点构建器中定义：**站点设置 \> 扩展 \> 为产品显示度量单位**。</span><span class="sxs-lookup"><span data-stu-id="919eb-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="919eb-113">支持三种设置：</span><span class="sxs-lookup"><span data-stu-id="919eb-113">There are three supported settings:</span></span>

- <span data-ttu-id="919eb-114">**不显示** – 选择此设置后，电子商务站点将不会为产品显示度量单位。</span><span class="sxs-lookup"><span data-stu-id="919eb-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="919eb-115">此行为是默认行为。</span><span class="sxs-lookup"><span data-stu-id="919eb-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="919eb-116">**在产品购买体验中显示** – 选择此设置后，度量单位将显示在产品详细信息、购物车、结帐、订单历史记录和订单详细信息页上。</span><span class="sxs-lookup"><span data-stu-id="919eb-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="919eb-117">**在产品浏览和购买体验中显示** – 选择此设置后，度量单位将显示在产品购买体验页面以及产品浏览体验期间。</span><span class="sxs-lookup"><span data-stu-id="919eb-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="919eb-118">作为此行为的一部分，度量单位将显示在搜索结果和产品集合模块中。</span><span class="sxs-lookup"><span data-stu-id="919eb-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="919eb-119">度量单位显示设置自 Commerce 版本 10.0.19 开始可用。</span><span class="sxs-lookup"><span data-stu-id="919eb-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="919eb-120">如果要从旧版本的 Commerce 更新，必须手动更新 appsettings.json 文件。</span><span class="sxs-lookup"><span data-stu-id="919eb-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="919eb-121">有关说明，请参阅 [SDK 和模块库更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)。</span><span class="sxs-lookup"><span data-stu-id="919eb-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="919eb-122">使用度量单位设置的模块</span><span class="sxs-lookup"><span data-stu-id="919eb-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="919eb-123">使用度量单位设置的模块包括购买框、愿望列表、购物车、购物车图标、搜索结果容器、产品集合、结帐和订单详细信息模块。</span><span class="sxs-lookup"><span data-stu-id="919eb-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="919eb-124">在下图的示例中，产品详细信息页 (PDP) 为产品显示了度量单位 (**ea**)。</span><span class="sxs-lookup"><span data-stu-id="919eb-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![显示度量单位的 PDP 示例](./media/Productunit-PDP.png)

<span data-ttu-id="919eb-126">在下图的示例中，产品集合模块为产品显示了度量单位 (**ea**)。</span><span class="sxs-lookup"><span data-stu-id="919eb-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![显示度量单位的产品集合模块的示例](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="919eb-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="919eb-128">Additional resources</span></span>

[<span data-ttu-id="919eb-129">模块库概览</span><span class="sxs-lookup"><span data-stu-id="919eb-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="919eb-130">购物车模块</span><span class="sxs-lookup"><span data-stu-id="919eb-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="919eb-131">购买框模块</span><span class="sxs-lookup"><span data-stu-id="919eb-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="919eb-132">帐户管理页面和模块</span><span class="sxs-lookup"><span data-stu-id="919eb-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="919eb-133">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="919eb-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
