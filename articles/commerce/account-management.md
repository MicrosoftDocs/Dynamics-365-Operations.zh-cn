---
title: 帐户管理页和模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785368"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="15e8d-103">帐户管理页和模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="15e8d-104">此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。</span><span class="sxs-lookup"><span data-stu-id="15e8d-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15e8d-105">概览</span><span class="sxs-lookup"><span data-stu-id="15e8d-105">Overview</span></span>

<span data-ttu-id="15e8d-106">帐户管理指的是 Dynamics 365 Commerce 中一组用于管理与用户帐户有关的信息的页面。</span><span class="sxs-lookup"><span data-stu-id="15e8d-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="15e8d-107">帐户管理页包括帐户管理登陆页、用户个人资料页、用户地址页、订单历史记录页、订单详细信息页、会员页和愿望列表页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="15e8d-108">帐户管理登陆页</span><span class="sxs-lookup"><span data-stu-id="15e8d-108">Account management landing page</span></span>

<span data-ttu-id="15e8d-109">帐户管理登陆页使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="15e8d-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="15e8d-110">**内容放置** – 此模块是容器模块，其中包含帐户管理登陆页中的所有模块。</span><span class="sxs-lookup"><span data-stu-id="15e8d-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="15e8d-111">**帐户欢迎项** – 此模块用于提供帐户管理页中的欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="15e8d-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="15e8d-112">其中包括标题和磁贴大小属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="15e8d-113">**磁贴大小**属性定义模块在内容放置模块中的宽度。</span><span class="sxs-lookup"><span data-stu-id="15e8d-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="15e8d-114">值范围为 **1** 到 **12**，其中的 **12** 表示内容放置容器的完整宽度。</span><span class="sxs-lookup"><span data-stu-id="15e8d-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="15e8d-115">**帐户订单下达项** – 此模块用于提供用户帐户下达的订单数量的摘要。</span><span class="sxs-lookup"><span data-stu-id="15e8d-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="15e8d-116">其中包括标题、磁贴大小和“视图详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="15e8d-117">应该将此“视图详细信息”链接配置为重定向到订单历史记录页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="15e8d-118">**帐户个人资料放置项** – 此模块用于提供用户个人资料的摘要。</span><span class="sxs-lookup"><span data-stu-id="15e8d-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="15e8d-119">其中包括标题、磁贴大小和“视图详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="15e8d-120">应该将此“视图详细信息”链接配置为重定向到用户个人资料页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="15e8d-121">**帐户愿望列表项** – 此模块用于提供有关客户愿望列表的项的摘要。</span><span class="sxs-lookup"><span data-stu-id="15e8d-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="15e8d-122">例如，可能显示“您的愿望列表中有 10 项”。</span><span class="sxs-lookup"><span data-stu-id="15e8d-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="15e8d-123">其中包括标题、磁贴大小和“视图详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="15e8d-124">应该将此“视图详细信息”链接配置为重定向到愿望列表页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="15e8d-125">**帐户地址项** – 此模块用于提供用户地址的摘要。</span><span class="sxs-lookup"><span data-stu-id="15e8d-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="15e8d-126">例如，可能显示“您已向您的帐户添加了 2 个地址”。</span><span class="sxs-lookup"><span data-stu-id="15e8d-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="15e8d-127">其中包括标题、磁贴大小和“视图详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="15e8d-128">应该将此“视图详细信息”链接配置为重定向到用户地址页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="15e8d-129">**帐户会员项** – 此模块用于显示和链接到会员计划信息。</span><span class="sxs-lookup"><span data-stu-id="15e8d-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="15e8d-130">其中包括标题、磁贴大小和“成为会员”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="15e8d-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="15e8d-131">应该将此“视图详细信息”链接配置为重定向到会员页。</span><span class="sxs-lookup"><span data-stu-id="15e8d-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="15e8d-132">应该将“成为会员”链接配置为重定向到一个页面，用户可在其中加入会员计划。</span><span class="sxs-lookup"><span data-stu-id="15e8d-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="15e8d-133">订单历史记录页</span><span class="sxs-lookup"><span data-stu-id="15e8d-133">Order history page</span></span>

<span data-ttu-id="15e8d-134">订单历史记录页使用订单历史记录模块显示用户最近下达的所有订单。</span><span class="sxs-lookup"><span data-stu-id="15e8d-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="15e8d-135">订单详细信息</span><span class="sxs-lookup"><span data-stu-id="15e8d-135">Order details page</span></span>

<span data-ttu-id="15e8d-136">订单详细信息页提供每个订单的详细信息，可从订单历史记录页访问。</span><span class="sxs-lookup"><span data-stu-id="15e8d-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="15e8d-137">它使用订单详细信息模块，后者需要销售 ID 或交易 ID 才能检索订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="15e8d-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="15e8d-138">用户个人资料页</span><span class="sxs-lookup"><span data-stu-id="15e8d-138">User profile page</span></span>

<span data-ttu-id="15e8d-139">用户个人资料页显示用户帐户详细信息，如用户的姓名和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="15e8d-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="15e8d-140">它使用用户个人资料模块。</span><span class="sxs-lookup"><span data-stu-id="15e8d-140">It uses the user profile module.</span></span> <span data-ttu-id="15e8d-141">虽然不能删除电子邮件地址，但可以对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="15e8d-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="15e8d-142">用户地址页</span><span class="sxs-lookup"><span data-stu-id="15e8d-142">User address page</span></span>

<span data-ttu-id="15e8d-143">用户地址页显示与用户帐户关联的地址的列表。</span><span class="sxs-lookup"><span data-stu-id="15e8d-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="15e8d-144">用户在结帐期间提供这些地址，或直接将其添加到此页面中。</span><span class="sxs-lookup"><span data-stu-id="15e8d-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="15e8d-145">用户地址模块用于添加和编辑地址，设置主地址和在页面中显示现有地址。</span><span class="sxs-lookup"><span data-stu-id="15e8d-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="15e8d-146">愿望列表页</span><span class="sxs-lookup"><span data-stu-id="15e8d-146">Wish list page</span></span>

<span data-ttu-id="15e8d-147">愿望列表页显示已添加到客户的愿望列表的项。</span><span class="sxs-lookup"><span data-stu-id="15e8d-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="15e8d-148">它使用愿望列表模块显示愿望列表项。</span><span class="sxs-lookup"><span data-stu-id="15e8d-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="15e8d-149">会员页面</span><span class="sxs-lookup"><span data-stu-id="15e8d-149">Loyalty page</span></span>

<span data-ttu-id="15e8d-150">会员页供客户加入会员计划；如果客户已经是会员计划成员，则用于查看其计划详细信息。</span><span class="sxs-lookup"><span data-stu-id="15e8d-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="15e8d-151">也可以查看在最近交易中获得的积分和兑换的积分。</span><span class="sxs-lookup"><span data-stu-id="15e8d-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15e8d-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="15e8d-152">Additional resources</span></span>

[<span data-ttu-id="15e8d-153">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="15e8d-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="15e8d-154">容器模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="15e8d-155">购买框模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="15e8d-156">购物车模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="15e8d-157">结帐模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="15e8d-158">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="15e8d-159">页眉模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="15e8d-160">页脚模块</span><span class="sxs-lookup"><span data-stu-id="15e8d-160">Footer module</span></span>](author-footer-module.md)