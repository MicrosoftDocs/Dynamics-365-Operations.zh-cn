---
title: 电子商务站点概述
description: 本主题概述了 Microsoft Dynamics 365 Commerce 中对电子商务站点的支持。
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae220e98acbda99255beefea598d973dbaa22368
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997539"
---
# <a name="e-commerce-site-overview"></a><span data-ttu-id="99b09-103">电子商务站点概述</span><span class="sxs-lookup"><span data-stu-id="99b09-103">E-commerce site overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99b09-104">本主题概述了 Microsoft Dynamics 365 Commerce 中对电子商务站点的支持。</span><span class="sxs-lookup"><span data-stu-id="99b09-104">This topic provides an overview of the support for e-commerce sites in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="99b09-105">它包含有关如何在 Dynamics 365 Commerce 中初始化和管理电子商务在线商店的信息。</span><span class="sxs-lookup"><span data-stu-id="99b09-105">It includes information about how e-commerce online stores are initialized and managed in Dynamics 365 Commerce.</span></span> <span data-ttu-id="99b09-106">另外还提供了有关在线商店的详细信息以及有关如何设置和配置电子商务站点的详细信息的链接。</span><span class="sxs-lookup"><span data-stu-id="99b09-106">It also provides links to more information about online stores, and about how to set up and configure an e-commerce site.</span></span> <span data-ttu-id="99b09-107">尽管本主题涵盖许多基础知识，但并未涵盖设置生产电子商务站点所需的所有内容。</span><span class="sxs-lookup"><span data-stu-id="99b09-107">Although this topic covers many of the basics, it doesn't cover everything that is required to set up a production e-commerce site.</span></span> <span data-ttu-id="99b09-108">可在 Dynamics 365 Commerce 文档中找到更多高级主题。</span><span class="sxs-lookup"><span data-stu-id="99b09-108">More advanced topics can be found in the Dynamics 365 Commerce documentation.</span></span>

## <a name="online-store-channel"></a><span data-ttu-id="99b09-109">在线商店渠道</span><span class="sxs-lookup"><span data-stu-id="99b09-109">Online store channel</span></span>

<span data-ttu-id="99b09-110">您必须至少先设置一个在线商店渠道，才能在 Dynamics 365 Commerce 中构建站点。</span><span class="sxs-lookup"><span data-stu-id="99b09-110">Before you can build your site in Dynamics 365 Commerce, at least one online store channel must be set up.</span></span> <span data-ttu-id="99b09-111">有关详细信息，请参阅[设置在线渠道](channel-setup-online.md)。</span><span class="sxs-lookup"><span data-stu-id="99b09-111">For more information, see [Set up an online channel](channel-setup-online.md).</span></span> 

<span data-ttu-id="99b09-112">在 Dynamics 365 Commerce 中，使用在线商店渠道建立产品、定价、语言、付款方式、交货方式、履行中心，以及应为客户提供的在线体验的其他方面。</span><span class="sxs-lookup"><span data-stu-id="99b09-112">In Dynamics 365 Commerce, you use an online store channel to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="99b09-113">只需设置一个在线商店渠道，便可以开始使用 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="99b09-113">Only one online store channel has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="99b09-114">但是，一个电子商务站点可以为多个在线商店提供在线体验。</span><span class="sxs-lookup"><span data-stu-id="99b09-114">However, a single e-commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="99b09-115">例如，如果设置多个在线商店来支持不同的地理区域，可以使用一组电子商务页面来提供每个商店定义的独特体验。</span><span class="sxs-lookup"><span data-stu-id="99b09-115">For example, if multiple online stores are set up to support different geographical regions, a single set of e-commerce pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="99b09-116">有关如何配置站点以支持多个在线商店的详细信息，请参阅[将在线站点与渠道关联](associate-site-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="99b09-116">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="99b09-117">设置在线商店后，可以将其与将用作您的在线店面的 Dynamics 365 Commerce 站点关联。</span><span class="sxs-lookup"><span data-stu-id="99b09-117">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="99b09-118">有关在线商店以及如何设置的详细信息，请参阅[设置在线商店](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores)。</span><span class="sxs-lookup"><span data-stu-id="99b09-118">For more information about online stores and how to set them up, see [Set up online stores](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="99b09-119">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="99b09-119">Deploy a new e-commerce tenant</span></span>

<span data-ttu-id="99b09-120">在电子商务站点初始化期间，系统会提示您输入域名。</span><span class="sxs-lookup"><span data-stu-id="99b09-120">During initialization of an e-commerce site, you're prompted for a domain name.</span></span> <span data-ttu-id="99b09-121">有关 Commerce 中的域的详细信息，请参阅[配置域名](configure-your-domain-name.md)和 [Dynamics 365 Commerce 中的域](domains-commerce.md)。</span><span class="sxs-lookup"><span data-stu-id="99b09-121">For more information about domains in Commerce, see [Configure your domain name](configure-your-domain-name.md) and [Domains in Dynamics 365 Commerce](domains-commerce.md).</span></span> <span data-ttu-id="99b09-122">若要使用 [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) 部署新的电子商务租户，请按照[部署新的电子商务租户](deploy-ecommerce-site.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="99b09-122">To deploy a new e-commerce tenant by using [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), follow the steps in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="99b09-123">在 LCS 中设置电子商务租户后，将提供指向 Commerce 站点构建器的链接。</span><span class="sxs-lookup"><span data-stu-id="99b09-123">After your e-commerce tenant is set up in LCS, a link to Commerce site builder will be provided.</span></span> <span data-ttu-id="99b09-124">然后，您可以使用 Commerce 站点构建器来初始化和配置您的电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="99b09-124">You can then use Commerce site builder to initialize and configure your e-commerce sites.</span></span>

## <a name="initialize-your-e-commerce-site"></a><span data-ttu-id="99b09-125">初始化电子商务站点</span><span class="sxs-lookup"><span data-stu-id="99b09-125">Initialize your e-commerce site</span></span>

<span data-ttu-id="99b09-126">从 LCS 启动 Commerce 站点构建器时，将显示 **站点** 页面。</span><span class="sxs-lookup"><span data-stu-id="99b09-126">When you start Commerce site builder from LCS, the **Sites** page appears.</span></span> <span data-ttu-id="99b09-127">该页面包括两个预配置的站点（**默认** 和 **Fabrikam**），如下图中的示例所示。</span><span class="sxs-lookup"><span data-stu-id="99b09-127">This page includes two preconfigured sites, **default** and **fabrikam**, as shown in the example in the following illustration.</span></span>

![Commerce 站点构建器中的站点页面](media/e-commerce-site-01.png)

<span data-ttu-id="99b09-129">当您选择其中一个站点时，系统会提示您选择域名、默认的在线商店渠道、所选渠道的受支持语言以及路径。</span><span class="sxs-lookup"><span data-stu-id="99b09-129">When you select one of these sites, you're prompted to select a domain name, a default online store channel, a supported language for the selected channel, and a path.</span></span> <span data-ttu-id="99b09-130">如果仅使用一个渠道，可以将路径保留为空白。</span><span class="sxs-lookup"><span data-stu-id="99b09-130">If only one channel is used, you can leave the path blank.</span></span> <span data-ttu-id="99b09-131">稍后可以在 Commerce 站点构建器中配置更多在线商店渠道或语言。</span><span class="sxs-lookup"><span data-stu-id="99b09-131">More online store channels or languages can be configured later in Commerce site builder.</span></span> <span data-ttu-id="99b09-132">每个附加的渠道或语言都需要唯一的路径。</span><span class="sxs-lookup"><span data-stu-id="99b09-132">Each additional channel or language will require a unique path.</span></span> <span data-ttu-id="99b09-133">例如，您有两个与单个站点相关联的在线渠道，并且该站点的域名为 `www.fabrikam.com`。</span><span class="sxs-lookup"><span data-stu-id="99b09-133">For example, you have two online channels that are associated with a single site, and the domain name for the site is `www.fabrikam.com`.</span></span> <span data-ttu-id="99b09-134">在这种情况下，一个渠道的路径可以是没有路径的默认值 (`https://www.fabrikam.com`)，第二个渠道可以设置为将具有 URL `https://www.fabrikam.com/site2` 的新路径，例如 **site2**。</span><span class="sxs-lookup"><span data-stu-id="99b09-134">In this case, the path for one channel can be the default value that has no path (`https://www.fabrikam.com`), and the second channel can be set to a new path, such as **site2**, that will have the URL `https://www.fabrikam.com/site2`.</span></span> <span data-ttu-id="99b09-135">下图显示 Commerce 站点构建器中的站点初始化对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="99b09-135">The following illustration shows an example of a site initialization dialog box in Commerce site builder.</span></span>

![Commerce 站点构建器中的站点初始化对话框](media/e-commerce-site-02.png)

<span data-ttu-id="99b09-137">**站点** 页面还包含 **新建站点** 按钮。</span><span class="sxs-lookup"><span data-stu-id="99b09-137">The **Sites** page also includes a **New site** button.</span></span> <span data-ttu-id="99b09-138">选择此按钮时显示的对话框类似于站点初始化对话框，但是它用于创建新站点。</span><span class="sxs-lookup"><span data-stu-id="99b09-138">The dialog box that appears when you select this button resembles the site initialization dialog box, but it's used to create a new site.</span></span> <span data-ttu-id="99b09-139">新站点为空白。</span><span class="sxs-lookup"><span data-stu-id="99b09-139">New sites are blank.</span></span> <span data-ttu-id="99b09-140">它们不包含通过 **默认** 和 **Fabrikam** 站点提供的相同默认模板、片段、页面和图像。</span><span class="sxs-lookup"><span data-stu-id="99b09-140">They don't include the same default templates, fragments, pages, and images that are provided with the **default** and **fabrikam** sites.</span></span> <span data-ttu-id="99b09-141">但是，您可以根据需要打开支持票证，以请求将默认内容的副本添加到新的空白站点。</span><span class="sxs-lookup"><span data-stu-id="99b09-141">However, as you require, you can open a support ticket to request that a copy of the default content be added to a new blank site.</span></span> <span data-ttu-id="99b09-142">有关详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。</span><span class="sxs-lookup"><span data-stu-id="99b09-142">For more information, see [Create an e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="99b09-143">初始化新站点后，将显示 Commerce 站点构建器 **主页**。</span><span class="sxs-lookup"><span data-stu-id="99b09-143">After a new site is initialized, the Commerce site builder **Home** page appears.</span></span> <span data-ttu-id="99b09-144">该页面包含指向常见操作和指导内容的链接，如下图中的示例所示。</span><span class="sxs-lookup"><span data-stu-id="99b09-144">This page includes links to common actions and guidance content, as shown in the example in the following illustration.</span></span>

![Commerce 站点构建器中的主页上的链接](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a><span data-ttu-id="99b09-146">修改在线商店渠道或将在线商店渠道添加到电子商务站点</span><span class="sxs-lookup"><span data-stu-id="99b09-146">Modify online store channels or add online store channels to an e-commerce site</span></span>

<span data-ttu-id="99b09-147">创建电子商务站点后，您可以按照[将电子商务站点与在线渠道关联](associate-site-online-store.md)中的步骤更改与之关联的渠道。</span><span class="sxs-lookup"><span data-stu-id="99b09-147">After an e-commerce site is created, you can change the channel that it's associated with by following the steps in [Associate an e-commerce site with an online channel](associate-site-online-store.md).</span></span> <span data-ttu-id="99b09-148">下图中的示例显示如何在 **渠道** 页面（**站点设置 \> 渠道**）上更改渠道操作单位编号 (OUN)。</span><span class="sxs-lookup"><span data-stu-id="99b09-148">The example in the following illustration shows how a channel operating unit number (OUN) can be changed on the **Channels** page (**Site settings \> Channels**).</span></span> <span data-ttu-id="99b09-149">完成更改后，请务必选择 **保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="99b09-149">After you've finished making a change, be sure to select **Save and publish**.</span></span> <span data-ttu-id="99b09-150">这样，您可以确保发布更改。</span><span class="sxs-lookup"><span data-stu-id="99b09-150">In this way, you ensure that the change is published.</span></span>

![Commerce 站点构建器中的渠道页面](media/e-commerce-site-04.png)

<span data-ttu-id="99b09-152">您可以通过选择 **添加渠道** 添加新渠道。</span><span class="sxs-lookup"><span data-stu-id="99b09-152">You can add new channels by selecting **Add a channel**.</span></span> <span data-ttu-id="99b09-153">若要将新语言添加到渠道，请选择该渠道，然后在显示的渠道对话框中选择 **添加区域设置**。</span><span class="sxs-lookup"><span data-stu-id="99b09-153">To add new languages to a channel, select the channel, and then select **Add a locale** in the channel dialog box that appears.</span></span> <span data-ttu-id="99b09-154">在区域设置显示在对话框中之前，必须在 Commerce 总部中为在线商店渠道预先配置它们。</span><span class="sxs-lookup"><span data-stu-id="99b09-154">Before locales can appear in the dialog box, they must be preconfigured for the online store channel in Commerce headquarters.</span></span>

![Commerce 站点构建器中的渠道对话框](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a><span data-ttu-id="99b09-156">设置 Azure B2C 租户</span><span class="sxs-lookup"><span data-stu-id="99b09-156">Set up an Azure B2C tenant</span></span>

<span data-ttu-id="99b09-157">Dynamics 365 Commerce 使用 Azure Active Directory (Azure AD) 企业对消费者 (B2C) 支持用户凭据和身份验证流。</span><span class="sxs-lookup"><span data-stu-id="99b09-157">Dynamics 365 Commerce uses Azure Active Directory (Azure AD) business-to-consumer (B2C) to support user credential and authentication flows.</span></span> <span data-ttu-id="99b09-158">有关如何设置 Azure B2C 租户的信息，请参阅[在 Commerce 中设置 B2C 租户](set-up-b2c-tenant.md)、[设置用户登录自定义页面](custom-pages-user-logins.md)和[在 Commerce 环境中配置多个 B2C 租户](configure-multi-b2c-tenants.md)。</span><span class="sxs-lookup"><span data-stu-id="99b09-158">For information about how to set up your Azure B2C tenant, see [Set up a B2C tenant in Commerce](set-up-b2c-tenant.md), [Set up custom pages for user sign-ins](custom-pages-user-logins.md), and [Configure multiple B2C tenants in a Commerce environment](configure-multi-b2c-tenants.md).</span></span>

## <a name="overview-of-the-default-site-pages"></a><span data-ttu-id="99b09-159">默认站点页面概述</span><span class="sxs-lookup"><span data-stu-id="99b09-159">Overview of the default site pages</span></span>

<span data-ttu-id="99b09-160">**默认** 和 **Fabrikam** 站点包括预配置的模板、片段和页面，以帮助您入门。</span><span class="sxs-lookup"><span data-stu-id="99b09-160">The **default** and **fabrikam** sites include preconfigured templates, fragments, and pages to help you get started.</span></span> <span data-ttu-id="99b09-161">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="99b09-161">For more information, see the following topics:</span></span>

- [<span data-ttu-id="99b09-162">主页概览</span><span class="sxs-lookup"><span data-stu-id="99b09-162">Home page overview</span></span>](quick-tour-home-page.md)
- [<span data-ttu-id="99b09-163">产品详细信息页面概述</span><span class="sxs-lookup"><span data-stu-id="99b09-163">Product details page overview</span></span>](quick-tour-pdp.md)
- [<span data-ttu-id="99b09-164">购物车和结帐页面概览</span><span class="sxs-lookup"><span data-stu-id="99b09-164">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)
- [<span data-ttu-id="99b09-165">帐户管理页面概览</span><span class="sxs-lookup"><span data-stu-id="99b09-165">Account management pages overview</span></span>](quick-tour-account-management.md)

## <a name="manage-site-settings"></a><span data-ttu-id="99b09-166">管理站点设置</span><span class="sxs-lookup"><span data-stu-id="99b09-166">Manage site settings</span></span>

<span data-ttu-id="99b09-167">有关如何管理站点设置的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="99b09-167">For information about how to manage your site settings, see the following topics:</span></span>

- [<span data-ttu-id="99b09-168">管理电子商务用户和角色</span><span class="sxs-lookup"><span data-stu-id="99b09-168">Manage e-commerce users and roles</span></span>](manage-ecommerce-users-roles.md)
- [<span data-ttu-id="99b09-169">站点的搜索引擎优化 (SEO) 注意事项</span><span class="sxs-lookup"><span data-stu-id="99b09-169">Search engine optimization (SEO) considerations for your site</span></span>](/search-engine-optimization-considerations.md)
- [<span data-ttu-id="99b09-170">管理内容安全策略 (CSP)</span><span class="sxs-lookup"><span data-stu-id="99b09-170">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
- [<span data-ttu-id="99b09-171">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="99b09-171">Select a site theme</span></span>](select-site-theme.md)

## <a name="manage-site-content"></a><span data-ttu-id="99b09-172">管理站点内容</span><span class="sxs-lookup"><span data-stu-id="99b09-172">Manage site content</span></span>

<span data-ttu-id="99b09-173">有关如何管理站点内容的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="99b09-173">For information about how to manage site content, see the following topics:</span></span>

- [<span data-ttu-id="99b09-174">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="99b09-174">Page model glossary</span></span>](page-elements-overview.md)
- [<span data-ttu-id="99b09-175">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="99b09-175">Document states and lifecycle</span></span>](document-states-overview.md)
- [<span data-ttu-id="99b09-176">模板和布局</span><span class="sxs-lookup"><span data-stu-id="99b09-176">Templates and layout</span></span>](templates-layouts-overview.md)
- [<span data-ttu-id="99b09-177">使用片段</span><span class="sxs-lookup"><span data-stu-id="99b09-177">Work with fragments</span></span>](work-with-fragments.md)
- [<span data-ttu-id="99b09-178">使用模块</span><span class="sxs-lookup"><span data-stu-id="99b09-178">Work with modules</span></span>](work-with-modules.md)
- [<span data-ttu-id="99b09-179">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="99b09-179">Digital asset management overview</span></span>](dam-overview.md)
- [<span data-ttu-id="99b09-180">模块库概览</span><span class="sxs-lookup"><span data-stu-id="99b09-180">Module library overview</span></span>](starter-kit-overview.md)

## <a name="additional-resources"></a><span data-ttu-id="99b09-181">其他资源</span><span class="sxs-lookup"><span data-stu-id="99b09-181">Additional resources</span></span>

[<span data-ttu-id="99b09-182">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="99b09-182">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="99b09-183">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="99b09-183">Deploy a new e-commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="99b09-184">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="99b09-184">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="99b09-185">配置域名</span><span class="sxs-lookup"><span data-stu-id="99b09-185">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="99b09-186">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="99b09-186">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="99b09-187">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="99b09-187">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="99b09-188">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="99b09-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
