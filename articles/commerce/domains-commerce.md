---
title: Dynamics 365 Commerce 中的域
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中处理域。
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bafa49cc570ddf7e0ff9c3dcb1b6902fb341b790
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225781"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="d9785-103">Dynamics 365 Commerce 中的域</span><span class="sxs-lookup"><span data-stu-id="d9785-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9785-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中处理域。</span><span class="sxs-lookup"><span data-stu-id="d9785-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d9785-105">域是用于在 Web 浏览器中导航到 Dynamics 365 Commerce 站点的 Web 地址。</span><span class="sxs-lookup"><span data-stu-id="d9785-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="d9785-106">请使用所选域名服务器 (DNS) 提供商管理域。</span><span class="sxs-lookup"><span data-stu-id="d9785-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="d9785-107">发布站点时，整个 Dynamics 365 Commerce 站点构建器中都引用域协调站点的访问方法。</span><span class="sxs-lookup"><span data-stu-id="d9785-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="d9785-108">此主题介绍在 Commerce 站点的整个开发和启动生命周期中如何处理和引用域。</span><span class="sxs-lookup"><span data-stu-id="d9785-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="d9785-109">预配和支持的主机名</span><span class="sxs-lookup"><span data-stu-id="d9785-109">Provisioning and supported host names</span></span>

<span data-ttu-id="d9785-110">在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) 中预配电子商务环境时，电子商务预配屏幕上的 **支持的主机名** 框用于输入将与部署的 Commerce 环境关联的域。</span><span class="sxs-lookup"><span data-stu-id="d9785-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="d9785-111">这些域将是托管电子商务网站且面向客户的域名服务器 (DNS) 名称。</span><span class="sxs-lookup"><span data-stu-id="d9785-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="d9785-112">在此阶段输入域不会将该域的流量转移到 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="d9785-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="d9785-113">DNS CNAME 记录更新为对 Commerce 终结点使用某个域时，将把该域的流量仅路由到该 Commerce 终结点。</span><span class="sxs-lookup"><span data-stu-id="d9785-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d9785-114">可以在 **支持的主机名** 框中输入多个域，并使用分号分隔。</span><span class="sxs-lookup"><span data-stu-id="d9785-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="d9785-115">下图显示 LCS 电子商务预配屏幕，其中突出显示了 **支持的主机名** 框。</span><span class="sxs-lookup"><span data-stu-id="d9785-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![LCS 电子商务预配屏幕，其中突出显示了**支持的主机名**框](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="d9785-117">如果已进行了预配，可以创建服务请求以向环境添加更多域。</span><span class="sxs-lookup"><span data-stu-id="d9785-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="d9785-118">若要在 LCS 中创建服务请求，请在环境中转到 **支持 \> 支持问题**，然后选择 **提交事件**。</span><span class="sxs-lookup"><span data-stu-id="d9785-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="d9785-119">Commerce 生成的 URL</span><span class="sxs-lookup"><span data-stu-id="d9785-119">Commerce-generated URLs</span></span>

<span data-ttu-id="d9785-120">在预配 Dynamics 365 Commerce 电子商务环境时，Commerce 将生成充当环境的工作地址的 URL。</span><span class="sxs-lookup"><span data-stu-id="d9785-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="d9785-121">预配环境后，将在 LCS 中显示的电子商务站点链接中引用该 URL。</span><span class="sxs-lookup"><span data-stu-id="d9785-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="d9785-122">Commerce 生成的 URL 的格式为 `https://<e-commerce tenant name>.commerce.dynamics.com`，其中，电子商务租户名称为在 LCS 中为 Commerce 环境输入的名称。</span><span class="sxs-lookup"><span data-stu-id="d9785-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="d9785-123">也可以在沙盒环境中使用生产站点主机名。</span><span class="sxs-lookup"><span data-stu-id="d9785-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="d9785-124">在将站点从沙盒环境复制到生产时，此选项为理想选项。</span><span class="sxs-lookup"><span data-stu-id="d9785-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="d9785-125">站点设置</span><span class="sxs-lookup"><span data-stu-id="d9785-125">Site setup</span></span>

<span data-ttu-id="d9785-126">预配电子商务环境后，必须在 Commerce 站点构建器中设置站点，以将站点关联到工作 URL。</span><span class="sxs-lookup"><span data-stu-id="d9785-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="d9785-127">首次在站点构建器中设置站点时，将显示 **设置您的站点** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d9785-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="d9785-128">下图显示在您首次在站点构建器中访问名称为“default”的站点时，该站点的 **设置您的站点** 对话框。</span><span class="sxs-lookup"><span data-stu-id="d9785-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![**设置您的站点**对话框](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="d9785-130">可在站点构建器中使用 **选择域** 框将 LCS 中为您的站点提供的一个支持的主机名关联到您的站点。</span><span class="sxs-lookup"><span data-stu-id="d9785-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="d9785-131">可以将 **路径** 框保留为空，也可以添加将在工作 URL 中体现的一个额外的路径字符串。</span><span class="sxs-lookup"><span data-stu-id="d9785-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="d9785-132">如果将 **路径** 框保留为空，将把 Commerce 生成的基 URL 与站点构建器中正在设置的站点关联。</span><span class="sxs-lookup"><span data-stu-id="d9785-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="d9785-133">每个站点/域对的路径必须唯一。</span><span class="sxs-lookup"><span data-stu-id="d9785-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="d9785-134">在所选站点和域中，环境中只有一个站点可以使用空路径或与唯一路径字符串关联。</span><span class="sxs-lookup"><span data-stu-id="d9785-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="d9785-135">在设置站点期间添加到 **路径** 字段的所有字符串都将成为由 Commerce 生成且用于在 Web 浏览器中访问站点的基 URL 的子集。</span><span class="sxs-lookup"><span data-stu-id="d9785-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="d9785-136">在站点构建器的 **站点设置 \> 渠道** 配置部分中添加渠道时，此路径也称为 **匹配路径**。</span><span class="sxs-lookup"><span data-stu-id="d9785-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="d9785-137">例如，如果站点构建器中有一个站点在电子商务租户“xyz”中称为“fabrikam”，并且为该站点设置空路径，则可以通过在 Web 浏览器中直接转到 Commerce 生成的基 URL 来访问发布的站点内容：</span><span class="sxs-lookup"><span data-stu-id="d9785-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="d9785-138">或者，如果在设置同一个站点期间添加了路径“fabrikam”，则可以通过在 Web 浏览器中使用以下 URL 访问发布的站点内容：</span><span class="sxs-lookup"><span data-stu-id="d9785-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="d9785-139">页面和 URL</span><span class="sxs-lookup"><span data-stu-id="d9785-139">Pages and URLs</span></span>

<span data-ttu-id="d9785-140">为站点设置路径之后，站点构建器中与页面关联的所有 URL 将基于站点的工作 URL（即 Commerce 生成的 URL，或 Commerce 生成的 URL 加路径）构建。</span><span class="sxs-lookup"><span data-stu-id="d9785-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="d9785-141">如果通过在 **新建 URL** 对话框中从列表选择页面并输入该页面的 URL 路径在站点构建器中创建新 URL（**URLS /> +新建**），将把该 URL 与所选页面关联。</span><span class="sxs-lookup"><span data-stu-id="d9785-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="d9785-142">该 URL 路径值然后将追加到站点的工作 URL 以访问该页面，并在站点构建器中 **URL** 页面的 URL 列表内标示为 `./<URL path>`。</span><span class="sxs-lookup"><span data-stu-id="d9785-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="d9785-143">下图显示站点构建器中的 **新建 URL** 对话框，并突出显示了一个示例 URL 路径。</span><span class="sxs-lookup"><span data-stu-id="d9785-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![站点构建器中的**新建 URL** 对话框](./media/Domains_PageSetup2a.png)

<span data-ttu-id="d9785-145">下图显示站点构建器中的 **URL** 页面，并突出显示了列表中的一个示例 URL。</span><span class="sxs-lookup"><span data-stu-id="d9785-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![策略流中的“运行用户流”选项](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="d9785-147">站点构建器中的域</span><span class="sxs-lookup"><span data-stu-id="d9785-147">Domains in site builder</span></span>

<span data-ttu-id="d9785-148">设置站点时，可将支持的主机名值作为域关联。</span><span class="sxs-lookup"><span data-stu-id="d9785-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="d9785-149">选择支持的主机名值作为域时，可以看到整个站点构建器中引用所选域。</span><span class="sxs-lookup"><span data-stu-id="d9785-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="d9785-150">此域仅为 Commerce 环境内的引用，尚未将该域的流量转发到 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="d9785-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d9785-151">在站点构建器中处理站点时，如果为两个站点设置两个不同域，可以将 **?domain=** 属性追加到工作 URL 以在浏览器中访问发布的站点内容。</span><span class="sxs-lookup"><span data-stu-id="d9785-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="d9785-152">例如，已预配了环境“xyz”，并且已经创建了两个站点且已在站点构建器中关联：一个的域为 `www.fabrikam.com`，另一个的域为 `www.constoso.com`。</span><span class="sxs-lookup"><span data-stu-id="d9785-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="d9785-153">每个站点都是使用空路径设置的。</span><span class="sxs-lookup"><span data-stu-id="d9785-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="d9785-154">然后可以使用 **?domain=** 属性如下所示在 Web 浏览器中访问这两个站点：</span><span class="sxs-lookup"><span data-stu-id="d9785-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="d9785-155">如果在提供了多个域的环境中不指定域查询字符串，Commerce 将使用您提供的第一个域。</span><span class="sxs-lookup"><span data-stu-id="d9785-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="d9785-156">例如，如果路径“fabrikam”是在站点设置期间提供的第一个路径，则可以使用 URL `https://xyz.commerce.dynamics.com` 访问为 `www.fabrikam.com` 发布的站点内容站点。</span><span class="sxs-lookup"><span data-stu-id="d9785-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="d9785-157">生产中的流量转发</span><span class="sxs-lookup"><span data-stu-id="d9785-157">Traffic forwarding in production</span></span>

<span data-ttu-id="d9785-158">可以在 commerce.dynamics.com 终结点本身使用域查询字符串参数模拟多个域。</span><span class="sxs-lookup"><span data-stu-id="d9785-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="d9785-159">但是如果需要投入生产，则必须将自定义域的流量转发到 `<e-commerce tenant name>.commerce.dynamics.com` 终结点。</span><span class="sxs-lookup"><span data-stu-id="d9785-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="d9785-160">`<e-commerce tenant name>.commerce.dynamics.com` 终结点不支持自定义域安全套接字层 (SSL)，因此必须使用前门服务或内容交付网络 (CDN) 设置自定义域。</span><span class="sxs-lookup"><span data-stu-id="d9785-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="d9785-161">若要使用前门服务或 CDN 设置自定义域，有两个选择：</span><span class="sxs-lookup"><span data-stu-id="d9785-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="d9785-162">设置 Azure Front Door 之类前门服务以处理前端流量和连接到您的 Commerce 环境。</span><span class="sxs-lookup"><span data-stu-id="d9785-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="d9785-163">这样可以更好地控制域和证书管理以及更精细的安全策略。</span><span class="sxs-lookup"><span data-stu-id="d9785-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="d9785-164">使用 Commerce 提供的 Azure Front Door 实例。</span><span class="sxs-lookup"><span data-stu-id="d9785-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="d9785-165">这需要与 Dynamics 365 Commerce 团队协调操作以验证域和获取生产域的 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="d9785-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="d9785-166">有关如何直接设置 CDN 服务的信息，请参阅[添加对内容交付网络 (CDN) 的支持](add-cdn-support.md)。</span><span class="sxs-lookup"><span data-stu-id="d9785-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="d9785-167">若要使用 Commerce 提供的 Azure Front Door 实例，必须创建服务请求以获取 Commerce 入职团队的 CDN 设置协助。</span><span class="sxs-lookup"><span data-stu-id="d9785-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="d9785-168">您将需要提供公司名称、生产域、环境 ID 和生产电子商务租户名称。</span><span class="sxs-lookup"><span data-stu-id="d9785-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="d9785-169">您将需要确认这是现有域（用于当前活动站点）还是新域。</span><span class="sxs-lookup"><span data-stu-id="d9785-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="d9785-170">如果是新域，则一个步骤即可完成域验证和 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="d9785-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="d9785-171">如果是为现有网站提供支持的域，则需要执行多步流程来建立域验证和 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="d9785-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="d9785-172">此流程需要为期 7 个工作日的服务级别协议 (SLA) 以启用域，因为其中包含多个顺序步骤。</span><span class="sxs-lookup"><span data-stu-id="d9785-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="d9785-173">若要在 LCS 中创建服务请求，请在环境中转到 **支持 \> 支持问题**，然后选择 **提交事件**。</span><span class="sxs-lookup"><span data-stu-id="d9785-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="d9785-174">只有生产环境中才支持采用 SSL 的自定义域。</span><span class="sxs-lookup"><span data-stu-id="d9785-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="d9785-175">对于沙盒和用户接受度测试 (UAT) 之类非生产环境，请在 Web 浏览器中使用 Commerce 生成的 URL 访问发布的内容。</span><span class="sxs-lookup"><span data-stu-id="d9785-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="d9785-176">SSL 证书流程</span><span class="sxs-lookup"><span data-stu-id="d9785-176">SSL certificate process</span></span>

<span data-ttu-id="d9785-177">如果提交了服务请求，Commerce 团队将与您协商以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d9785-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="d9785-178">对于新域：</span><span class="sxs-lookup"><span data-stu-id="d9785-178">For new domains:</span></span>
- <span data-ttu-id="d9785-179">Commerce 团队将设置 Azure Front Door 实例（由 Commerce 托管）。</span><span class="sxs-lookup"><span data-stu-id="d9785-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="d9785-180">然后，Commerce 团队将提供 CNAME 记录以指向您的自定义域。</span><span class="sxs-lookup"><span data-stu-id="d9785-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="d9785-181">更新 CNAME 记录后，Commerce 托管的 Azure Front Door 实例可以验证域所有权和获取 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="d9785-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="d9785-182">对于现有/活动域：</span><span class="sxs-lookup"><span data-stu-id="d9785-182">For existing/active domains:</span></span>
- <span data-ttu-id="d9785-183">Commerce 团队将指示您添加要向您的域 DNS 提供商提供的 `afdverify.<custom-domain>` CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="d9785-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="d9785-184">完成后，Commerce 团队将把该域添加到 Azure Front Door 实例，并提供可添加到该域的 DNS 的更多 DNS TXT 记录。</span><span class="sxs-lookup"><span data-stu-id="d9785-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="d9785-185">完成后 TXT 记录之后，Commerce 团队将完成将设置 SSL 证书的域的 Azure Front Door 更新。</span><span class="sxs-lookup"><span data-stu-id="d9785-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="d9785-186">Apex 域</span><span class="sxs-lookup"><span data-stu-id="d9785-186">Apex domains</span></span>

<span data-ttu-id="d9785-187">Commerce 提供的 Azure Front Door 实例不支持 apex 域（其中不包含子域的根域）。</span><span class="sxs-lookup"><span data-stu-id="d9785-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="d9785-188">Apex 需要 IP 地址才能解析，而 Commerce Azure Front Door 实例只能采用虚拟终结点。</span><span class="sxs-lookup"><span data-stu-id="d9785-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="d9785-189">若要使用 apex 域，有两种选择：</span><span class="sxs-lookup"><span data-stu-id="d9785-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="d9785-190">**选项 1** - 使用您的 DNS 提供程序将 apex 域重定向到“www”域。</span><span class="sxs-lookup"><span data-stu-id="d9785-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="d9785-191">例如，fabrikam.com 重定向到 `www.fabrikam.com`，其中，`www.fabrikam.com` 是指向 Commerce 托管的 Azure Front Door 实例的 CNAME 记录。</span><span class="sxs-lookup"><span data-stu-id="d9785-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="d9785-192">**选项 2** - 自行设置 CDN/前门实例以托管 apex 域。</span><span class="sxs-lookup"><span data-stu-id="d9785-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d9785-193">如果使用的是 Azure Front Door，还必须在同一订阅中设置 Azure DNS。</span><span class="sxs-lookup"><span data-stu-id="d9785-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="d9785-194">Azure DNS 中托管的 apex 域可作为别名记录指向您的 Azure Front Door。</span><span class="sxs-lookup"><span data-stu-id="d9785-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="d9785-195">这是唯一解决方案，因为 apex 域必须始终指向 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="d9785-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="d9785-196">其他资源</span><span class="sxs-lookup"><span data-stu-id="d9785-196">Additional resources</span></span>

  [<span data-ttu-id="d9785-197">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="d9785-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="d9785-198">设置在线商店渠道</span><span class="sxs-lookup"><span data-stu-id="d9785-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="d9785-199">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="d9785-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="d9785-200">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="d9785-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="d9785-201">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="d9785-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="d9785-202">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="d9785-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="d9785-203">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="d9785-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="d9785-204">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="d9785-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="d9785-205">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="d9785-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="d9785-206">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="d9785-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="d9785-207">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="d9785-207">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]