---
title: 帐户管理页面和模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206623"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="3aab5-103">帐户管理页面和模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3aab5-104">此主题介绍 Microsoft Dynamics 365 Commerce 中的帐户管理页和模块。</span><span class="sxs-lookup"><span data-stu-id="3aab5-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3aab5-105">帐户管理指的是 Dynamics 365 Commerce 中一组用于管理与用户帐户有关的信息的页面。</span><span class="sxs-lookup"><span data-stu-id="3aab5-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3aab5-106">帐户管理页包括帐户管理登陆页、用户个人资料页、用户地址页、订单历史记录页、订单详细信息页、会员页和愿望列表页。</span><span class="sxs-lookup"><span data-stu-id="3aab5-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="3aab5-107">帐户管理登陆页</span><span class="sxs-lookup"><span data-stu-id="3aab5-107">Account management landing page</span></span>

<span data-ttu-id="3aab5-108">帐户管理登陆页使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="3aab5-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="3aab5-109">**容器** - 所有帐户管理登录页面模块均应放置在容器中。</span><span class="sxs-lookup"><span data-stu-id="3aab5-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="3aab5-110">**帐户欢迎磁贴** – 此模块用于提供帐户管理页中的欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="3aab5-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="3aab5-111">它包括标题的属性。</span><span class="sxs-lookup"><span data-stu-id="3aab5-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="3aab5-112">**帐户通用磁贴** - 此模块可用于提供标题和指向帐户管理页面（例如“订单历史记录”或“我的个人资料”页面）的链接。</span><span class="sxs-lookup"><span data-stu-id="3aab5-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="3aab5-113">通用磁贴模块可用于为任何页面配置磁贴。</span><span class="sxs-lookup"><span data-stu-id="3aab5-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="3aab5-114">在 Fabrikam 中，此模块用于帐户管理登录页面上的“订单历史记录”和“我的个人资料”页面链接。</span><span class="sxs-lookup"><span data-stu-id="3aab5-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="3aab5-115">**帐户愿望列表磁贴** – 此模块用于提供客户愿望列表项的摘要。</span><span class="sxs-lookup"><span data-stu-id="3aab5-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="3aab5-116">例如，可能显示“您的愿望列表中有 10 项”。</span><span class="sxs-lookup"><span data-stu-id="3aab5-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="3aab5-117">其中包括标题和“查看详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="3aab5-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="3aab5-118">应该将此“查看详细信息”链接配置为重定向到愿望列表页。</span><span class="sxs-lookup"><span data-stu-id="3aab5-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="3aab5-119">**帐户地址磁贴** – 此模块用于提供用户地址的摘要。</span><span class="sxs-lookup"><span data-stu-id="3aab5-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="3aab5-120">例如，可能显示“您已向您的帐户添加了 2 个地址”。</span><span class="sxs-lookup"><span data-stu-id="3aab5-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="3aab5-121">其中包括标题和“查看详细信息”链接的属性。</span><span class="sxs-lookup"><span data-stu-id="3aab5-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="3aab5-122">应该将此“查看详细信息”链接配置为重定向到用户地址页。</span><span class="sxs-lookup"><span data-stu-id="3aab5-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="3aab5-123">**帐户会员磁贴** – 此模块用于显示和链接到会员计划信息。</span><span class="sxs-lookup"><span data-stu-id="3aab5-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="3aab5-124">此磁贴有两种状态：一种状态显示用于加入会员计划的链接（如果用户还不是会员）。</span><span class="sxs-lookup"><span data-stu-id="3aab5-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="3aab5-125">当用户已经是会员时，另一状态显示用于查看会员详细信息页面的链接。</span><span class="sxs-lookup"><span data-stu-id="3aab5-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="3aab5-126">属性包括标题、“注册”链接和“查看会员”链接。</span><span class="sxs-lookup"><span data-stu-id="3aab5-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="3aab5-127">应该将此“查看会员”链接配置为重定向到会员页。</span><span class="sxs-lookup"><span data-stu-id="3aab5-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="3aab5-128">应该将“注册”链接配置为重定向到一个页面，用户可在其中加入会员计划。</span><span class="sxs-lookup"><span data-stu-id="3aab5-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="3aab5-129">订单历史记录页</span><span class="sxs-lookup"><span data-stu-id="3aab5-129">Order history page</span></span>

<span data-ttu-id="3aab5-130">订单历史记录页使用订单历史记录模块显示用户最近下达的所有订单。</span><span class="sxs-lookup"><span data-stu-id="3aab5-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="3aab5-131">订单详细信息</span><span class="sxs-lookup"><span data-stu-id="3aab5-131">Order details page</span></span>

<span data-ttu-id="3aab5-132">订单详细信息页提供每个订单的详细信息，可从订单历史记录页访问。</span><span class="sxs-lookup"><span data-stu-id="3aab5-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="3aab5-133">它使用订单详细信息模块，后者需要销售 ID 或交易 ID 才能检索订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="3aab5-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="3aab5-134">用户个人资料页</span><span class="sxs-lookup"><span data-stu-id="3aab5-134">User profile page</span></span>

<span data-ttu-id="3aab5-135">用户个人资料页显示用户帐户详细信息，如用户的姓名和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="3aab5-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="3aab5-136">它使用用户个人资料详细信息和用户个人资料编辑模块。</span><span class="sxs-lookup"><span data-stu-id="3aab5-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="3aab5-137">虽然不能删除电子邮件地址，但可以对其进行编辑。</span><span class="sxs-lookup"><span data-stu-id="3aab5-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="3aab5-138">用户个人资料页面还显示用户首选项，使用户可以选择加入或退出某些功能，例如建议列表的个性化。</span><span class="sxs-lookup"><span data-stu-id="3aab5-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="3aab5-139">用户地址页</span><span class="sxs-lookup"><span data-stu-id="3aab5-139">User address page</span></span>

<span data-ttu-id="3aab5-140">用户地址页显示与用户帐户关联的地址的列表。</span><span class="sxs-lookup"><span data-stu-id="3aab5-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="3aab5-141">用户在结帐期间提供这些地址，或直接将其添加到此页面中。</span><span class="sxs-lookup"><span data-stu-id="3aab5-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="3aab5-142">用户地址模块用于添加和编辑地址，设置主地址和在页面中显示现有地址。</span><span class="sxs-lookup"><span data-stu-id="3aab5-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="3aab5-143">愿望列表页</span><span class="sxs-lookup"><span data-stu-id="3aab5-143">Wish list page</span></span>

<span data-ttu-id="3aab5-144">愿望列表页显示已添加到客户的愿望列表的项。</span><span class="sxs-lookup"><span data-stu-id="3aab5-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="3aab5-145">它使用愿望列表模块显示愿望列表项。</span><span class="sxs-lookup"><span data-stu-id="3aab5-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="3aab5-146">会员页面</span><span class="sxs-lookup"><span data-stu-id="3aab5-146">Loyalty page</span></span>

<span data-ttu-id="3aab5-147">如果客户已经是会员计划成员，则会员页可供客户查看会员详细信息。</span><span class="sxs-lookup"><span data-stu-id="3aab5-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="3aab5-148">也可以查看在最近交易中获得的积分和兑换的积分。</span><span class="sxs-lookup"><span data-stu-id="3aab5-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="3aab5-149">该页面使用会员详细信息模块来展示会员详细信息。</span><span class="sxs-lookup"><span data-stu-id="3aab5-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="3aab5-150">要加入会员计划，可以用会员注册和会员条款模块创建一个市场营销页面。</span><span class="sxs-lookup"><span data-stu-id="3aab5-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="3aab5-151">如果用户不是会员计划的成员，则这些模块将使用户能够注册。</span><span class="sxs-lookup"><span data-stu-id="3aab5-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3aab5-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="3aab5-152">Additional resources</span></span>

[<span data-ttu-id="3aab5-153">模块库概述</span><span class="sxs-lookup"><span data-stu-id="3aab5-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3aab5-154">容器模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3aab5-155">购买框模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3aab5-156">购物车模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3aab5-157">结帐模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3aab5-158">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3aab5-159">页眉模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3aab5-160">页脚模块</span><span class="sxs-lookup"><span data-stu-id="3aab5-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]