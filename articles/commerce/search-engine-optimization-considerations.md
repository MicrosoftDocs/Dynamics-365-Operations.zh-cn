---
title: 站点的搜索引擎优化 (SEO) 注意事项
description: 此主题介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c4d1a4a1b14f7af1db1c53bd9ee1993cc9187609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254785"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="0fb19-103">站点的搜索引擎优化 (SEO) 注意事项</span><span class="sxs-lookup"><span data-stu-id="0fb19-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0fb19-104">此主题介绍从开发到生产的站点搜索引擎优化 (SEO) 注意事项。</span><span class="sxs-lookup"><span data-stu-id="0fb19-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="0fb19-105">正在开发的站点</span><span class="sxs-lookup"><span data-stu-id="0fb19-105">A site that is under development</span></span>

<span data-ttu-id="0fb19-106">正在开发某个站点时，所有站点页面应该具有 **NOINDEX** 和 **NOFOLLOW** 元标记，这样搜索引擎才不会为这些页面建立索引和将您的站点的开发版本存储到其缓存中。</span><span class="sxs-lookup"><span data-stu-id="0fb19-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="0fb19-107">若要执行此配置，必须向站点页模板添加默认元标记模块。</span><span class="sxs-lookup"><span data-stu-id="0fb19-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="0fb19-108">然后，默认元标记属性在页面编辑器中 SEO 属性部分内仍然可用。</span><span class="sxs-lookup"><span data-stu-id="0fb19-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="0fb19-109">可使用这些属性管理元标记。</span><span class="sxs-lookup"><span data-stu-id="0fb19-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="0fb19-110">软启动站点</span><span class="sxs-lookup"><span data-stu-id="0fb19-110">Soft launch of a site</span></span>

<span data-ttu-id="0fb19-111">“软启动”期间，将在完全启动之前将网站提供给一小部分受众或市场。</span><span class="sxs-lookup"><span data-stu-id="0fb19-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="0fb19-112">如果对网站执行软启动，应考虑保留 **NOINDEX** 元标记。</span><span class="sxs-lookup"><span data-stu-id="0fb19-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="0fb19-113">这样，有助于确保软启动继续仅对您要联系的一小部分受众开放。</span><span class="sxs-lookup"><span data-stu-id="0fb19-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="0fb19-114">生产中的站点</span><span class="sxs-lookup"><span data-stu-id="0fb19-114">A site that is in production</span></span>

<span data-ttu-id="0fb19-115">站点在生产中时，应确保正确标记所有站点页。</span><span class="sxs-lookup"><span data-stu-id="0fb19-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="0fb19-116">Microsoft Dynamics 365 Commerce 使用为页面输入的信息在该页中显示所有 SEO 信息。</span><span class="sxs-lookup"><span data-stu-id="0fb19-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="0fb19-117">以下模块提供此功能：类别页汇总、列表页汇总和产品页汇总。</span><span class="sxs-lookup"><span data-stu-id="0fb19-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="0fb19-118">为了优化搜索引擎索引编制，呈现框架同时使用 Dynamics 365 Commerce 中配置的 SEO 属性的信息和模块特定的信息。</span><span class="sxs-lookup"><span data-stu-id="0fb19-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="0fb19-119">对于生产中的站点，应确保 robots.txt 文件允许为您的整个站点进行索引编制，并且其中包含您发布的站点地图文档的链接。</span><span class="sxs-lookup"><span data-stu-id="0fb19-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="0fb19-120">您应该在 **站点设置 \> 启用站点地图** 中开启站点地图生成功能。</span><span class="sxs-lookup"><span data-stu-id="0fb19-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="0fb19-121">适用于内部预览、首先受众和所有受众的页面 SEO 设置</span><span class="sxs-lookup"><span data-stu-id="0fb19-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="0fb19-122">因为 Dynamics 365 Commerce 在可视页面构建器中支持已经过身份验证的“所见即所得”(WYSIWYG) 预览，所以作者可以准备自己的页面内容，不必担心信息对站点访问者可见。</span><span class="sxs-lookup"><span data-stu-id="0fb19-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="0fb19-123">如果必须发布某个页面，但是其公开性受到限制，则应采用 **NOINDEX** 元标记，从而让搜索引擎不为其建立索引。</span><span class="sxs-lookup"><span data-stu-id="0fb19-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="0fb19-124">然后，页面准备好对所有受众公开时，应该准备好所有基本 SEO 元数据，以便将搜索引擎索引编制的效率发挥到极致。</span><span class="sxs-lookup"><span data-stu-id="0fb19-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="0fb19-125">此外，还应该删除 **NOLIMIT** 元标记。</span><span class="sxs-lookup"><span data-stu-id="0fb19-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fb19-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="0fb19-126">Additional resources</span></span>

[<span data-ttu-id="0fb19-127">管理电子商务用户和角色</span><span class="sxs-lookup"><span data-stu-id="0fb19-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="0fb19-128">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="0fb19-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="0fb19-129">管理内容安全策略 (CSP)</span><span class="sxs-lookup"><span data-stu-id="0fb19-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]