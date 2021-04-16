---
title: Cookie 同意模块
description: 此主题介绍 cookie 同意模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795995"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="738a7-103">Cookie 同意模块</span><span class="sxs-lookup"><span data-stu-id="738a7-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="738a7-104">此主题介绍 cookie 同意模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="738a7-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="738a7-105">cookie 同意模块提示站点用户明确提供同意，以便允许跟踪浏览器 cookie 的任何功能或模块的 cookie。</span><span class="sxs-lookup"><span data-stu-id="738a7-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="738a7-106">站点用户在新浏览器会话中浏览站点时，需要此同意。</span><span class="sxs-lookup"><span data-stu-id="738a7-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="738a7-107">收到同意后，将进行跟踪，并且不会再次提示站点用户提供同意。</span><span class="sxs-lookup"><span data-stu-id="738a7-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="738a7-108">有关详细信息，请参阅 [Cookie 合规性](cookie-compliance.md)。</span><span class="sxs-lookup"><span data-stu-id="738a7-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="738a7-109">如果未收到用户 cookie 同意，页面中将不显示需要 cookie 同意的任何功能或模块。</span><span class="sxs-lookup"><span data-stu-id="738a7-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="738a7-110">例如，结帐模块、社交共享模块和首选商店模块全都需要 cookie 同意，并且如果未收到站点用户同意，将不显示。</span><span class="sxs-lookup"><span data-stu-id="738a7-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="738a7-111">可以在页面的页眉片段中配置 cookie 同意模块，以便在页面加载时实施该模块。</span><span class="sxs-lookup"><span data-stu-id="738a7-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="738a7-112">cookie 同意模块中应该包含明确的消息，以便告知站点用户站点中的 cookie 使用情况，还应提供站点隐私页面的链接。</span><span class="sxs-lookup"><span data-stu-id="738a7-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="738a7-113">下图突出显示了 cookie 同意消息和站点页面中显示的站点隐私政策页面的链接的示例。</span><span class="sxs-lookup"><span data-stu-id="738a7-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="738a7-114">![cookie 同意模块的示例](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="738a7-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="738a7-115">Cookie 同意模块属性</span><span class="sxs-lookup"><span data-stu-id="738a7-115">Cookie consent module properties</span></span>

| <span data-ttu-id="738a7-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="738a7-116">Property name</span></span>             | <span data-ttu-id="738a7-117">值</span><span class="sxs-lookup"><span data-stu-id="738a7-117">Value</span></span>                 | <span data-ttu-id="738a7-118">说明</span><span class="sxs-lookup"><span data-stu-id="738a7-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="738a7-119">富文本</span><span class="sxs-lookup"><span data-stu-id="738a7-119">Rich Text</span></span>                  | <span data-ttu-id="738a7-120">富文本</span><span class="sxs-lookup"><span data-stu-id="738a7-120">Rich Text</span></span> | <span data-ttu-id="738a7-121">指定富文本通知，以便通知用户，说明站点在使用浏览器 cookie，并且用户应该接受使用 cookie，站点才能完全正常运行。</span><span class="sxs-lookup"><span data-stu-id="738a7-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="738a7-122">链接</span><span class="sxs-lookup"><span data-stu-id="738a7-122">Links</span></span> | <span data-ttu-id="738a7-123">URL</span><span class="sxs-lookup"><span data-stu-id="738a7-123">URL</span></span> | <span data-ttu-id="738a7-124">可以将一个或多个链接添加到站点的隐私页面，以介绍站点中跟踪的 cookie 的类型。</span><span class="sxs-lookup"><span data-stu-id="738a7-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="738a7-125">向站点页面添加 cookie 同意模块</span><span class="sxs-lookup"><span data-stu-id="738a7-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="738a7-126">若要有效地将一个 cookie 同意模块添加到多个站点页面，可以将其添加到共享页面标题片段。</span><span class="sxs-lookup"><span data-stu-id="738a7-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="738a7-127">将标题片段添加到所有站点页面之后，站点用户首次浏览到任何站点页面时，将自动显示 cookie 同意通知。</span><span class="sxs-lookup"><span data-stu-id="738a7-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="738a7-128">有关标题片段和模块的详细信息，请参阅[标题模块](author-header-module.md)。</span><span class="sxs-lookup"><span data-stu-id="738a7-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="738a7-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="738a7-129">Additional resources</span></span>

[<span data-ttu-id="738a7-130">模块库概述</span><span class="sxs-lookup"><span data-stu-id="738a7-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="738a7-131">标题模块</span><span class="sxs-lookup"><span data-stu-id="738a7-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="738a7-132">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="738a7-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]