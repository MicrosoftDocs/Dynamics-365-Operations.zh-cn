---
title: 添加对内容交付网络 (CDN) 的支持
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001614"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="3ddd8-103">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="3ddd8-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3ddd8-104">此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="3ddd8-105">概览</span><span class="sxs-lookup"><span data-stu-id="3ddd8-105">Overview</span></span>

<span data-ttu-id="3ddd8-106">在 Dynamics 365 Commerce 中设置电子商务环境时，可将其配置为支持 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="3ddd8-107">可以在电子商务环境的预配过程中启用自定义域。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="3ddd8-108">也可以在预配过程完成后使用服务请求设置。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="3ddd8-109">电子商务环境的预配过程将生成一个与该环境关联的主机名。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="3ddd8-110">此主机名采用以下格式，其中，*e-commerce-tenant-name* 是您的环境的名称：</span><span class="sxs-lookup"><span data-stu-id="3ddd8-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="3ddd8-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="3ddd8-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="3ddd8-112">预配过程中生成的主机名或终结点仅支持 \*.commerce.dynamics.com 采用安全套接字层 (SSL) 证书。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="3ddd8-113">不支持自定义域支持采用 SSL。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="3ddd8-114">因此，必须在 CDN 中终止自定义的 SSL，并将流量从 CDN 转发到 Commerce 生成的主机名或终结点。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="3ddd8-115">此外，Commerce 生成的终结点 (\*.commerce.dynamics.com) 还将提供*统计信息*（JavaScript 或级联样式表 \[CSS\] 文件）。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="3ddd8-116">仅当将 Commerce 生成的主机名或终结点放在 CDN 后面时，才可以缓存这些统计信息。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="3ddd8-117">设置 SSL</span><span class="sxs-lookup"><span data-stu-id="3ddd8-117">Set up SSL</span></span>

<span data-ttu-id="3ddd8-118">若要帮助确保设置 SSL，并且缓存统计信息，必须配置 CDN，使其与 Commerce 为您的环境生成的主机名关联。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="3ddd8-119">还必须仅为统计信息缓存以下模式：</span><span class="sxs-lookup"><span data-stu-id="3ddd8-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="3ddd8-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="3ddd8-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="3ddd8-121">为 Commerce 环境预配了提供自定义域或使用服务请求为环境提供了自定义域之后，请将自定义域指向 Commerce 生成的主机名或终结点。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="3ddd8-122">前面介绍过，生成的主机名或终结点仅支持对 \*.commerce.dynamics.com 使用 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="3ddd8-123">不支持自定义域支持采用 SSL。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="3ddd8-124">CDN 服务</span><span class="sxs-lookup"><span data-stu-id="3ddd8-124">CDN services</span></span>

<span data-ttu-id="3ddd8-125">所有 CDN 服务都可以用于 Commerce 环境。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="3ddd8-126">下面是两个示例：</span><span class="sxs-lookup"><span data-stu-id="3ddd8-126">Here are two examples:</span></span>

- <span data-ttu-id="3ddd8-127">**Microsoft Azure Front Door Service** – Azure CDN 解决方案。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="3ddd8-128">有关 Azure Front Door Service 的详细信息，请参阅[Azure Front Door Service 文档](https://docs.microsoft.com/azure/frontdoor/)。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="3ddd8-129">**Akamai Dynamic Site Accelerator** – 有关详细信息，请参阅 [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="3ddd8-130">CDN 设置</span><span class="sxs-lookup"><span data-stu-id="3ddd8-130">CDN setup</span></span>

<span data-ttu-id="3ddd8-131">CDN 的设置过程通常包含下面的步骤：</span><span class="sxs-lookup"><span data-stu-id="3ddd8-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="3ddd8-132">添加前端主机。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-132">Add a front-end host.</span></span>
1. <span data-ttu-id="3ddd8-133">配置后端池。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="3ddd8-134">设置传递和缓存规则。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="3ddd8-135">添加前端主机</span><span class="sxs-lookup"><span data-stu-id="3ddd8-135">Add a front-end host</span></span>

<span data-ttu-id="3ddd8-136">可使用任何 CDN 服务，但是本主题中的示例则使用 Azure Front Door Service。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="3ddd8-137">有关如何设置 Azure Front Door Service 的信息，请参阅[快速入门：为高可用全局 Web 应用程序创建 Front Door](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="3ddd8-138">在 Azure Front Door Service 中配置后端池</span><span class="sxs-lookup"><span data-stu-id="3ddd8-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="3ddd8-139">若要在 Azure Front Door Service 中配置后端池，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3ddd8-140">向后端池添加 **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** 充当具有空后端主机标头的自定义主机。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="3ddd8-141">在**运行状况探测**下的**路径**字段中，输入 **/keepalive**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="3ddd8-142">在**间隔(秒)** 字段中，输入 **255**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="3ddd8-143">在**负载平衡**下，保留默认值。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="3ddd8-144">下图显示 Azure Front Door Service 中的**添加后端池**对话框。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![“添加后端池”对话框](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="3ddd8-146">在 Azure Front Door Service 中设置规则</span><span class="sxs-lookup"><span data-stu-id="3ddd8-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="3ddd8-147">若要在 Azure Front Door Service 中设置传递规则，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3ddd8-148">添加一个传递规则。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-148">Add a routing rule.</span></span>
1. <span data-ttu-id="3ddd8-149">在**名称**字段中，输入**默认**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="3ddd8-150">在**接受的协议**字段中，选择 **HTTP 和 HTTPS**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="3ddd8-151">在**前端主机**字段中，输入 **dynamics-ecom-tenant-name.azurefd.net**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="3ddd8-152">在**匹配模式**下的上方字段中，输入 **/\***。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="3ddd8-153">在**传递详细信息**下，将**传递类型**设置为**转发**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="3ddd8-154">在**后端池**字段中，选择 **ecom-backend**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="3ddd8-155">在**转发协议**字段组中，选择**匹配请求**选项。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="3ddd8-156">将 **URL 重写**选项设置为**禁用**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="3ddd8-157">将**缓存**选项设置为**禁用**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="3ddd8-158">若要在 Azure Front Door Service 中设置缓存规则，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3ddd8-159">添加一个缓存规则。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-159">Add a caching rule.</span></span>
1. <span data-ttu-id="3ddd8-160">在**名称**字段中，输入**统计信息**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="3ddd8-161">在**接受的协议**字段中，选择 **HTTP 和 HTTPS**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="3ddd8-162">在**前端主机**字段中，输入 **dynamics-ecom-tenant-name.azurefd.net**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="3ddd8-163">在**匹配模式**下的上方字段中，输入 **/\_msdyn365/\_scnr/\***。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="3ddd8-164">在**传递详细信息**下，将**传递类型**设置为**转发**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="3ddd8-165">在**后端池**字段中，选择 **ecom-backend**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="3ddd8-166">在**转发协议**字段组中，选择**匹配请求**选项。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="3ddd8-167">将 **URL 重写**选项设置为**禁用**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="3ddd8-168">将**缓存**选项设置为**禁用**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="3ddd8-169">在**查询字符串缓存行为**字段中，选择**缓存每个唯一 URL**。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="3ddd8-170">在**动态压缩**字段组中，选择**启用**选项。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="3ddd8-171">下图显示 Azure Front Door Service 中的**添加规则**对话框。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![“添加规则”对话框](./media/CDN_CachingRule.png)

<span data-ttu-id="3ddd8-173">部署此初始配置之后，必须将自定义域添加到 Azure Front Door Service 的配置中。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="3ddd8-174">若要添加自定义域（如 `www.fabrikam.com`），必须为该域配置一个规范名称 (CNAME)。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="3ddd8-175">下图显示 Azure Front Door Service 中的 **CNAME 配置**对话框。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![“CNAME 配置”对话框](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="3ddd8-177">如果要使用的域已激活且处于活动状态，请联系支持为 Azure Front Door Service 启用此域以设置测试。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="3ddd8-178">可使用 Azure Front Door Service 管理证书，也可以对自定义域使用您自己的证书。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="3ddd8-179">下图显示 Azure Front Door Service 中的**自定义域 HTTPS** 对话框。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![“自定义域 HTTPS”对话框](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="3ddd8-181">现在应该已经正确配置了您的 CDN，可将其用于您的 Commerce 站点。</span><span class="sxs-lookup"><span data-stu-id="3ddd8-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ddd8-182">其他资源</span><span class="sxs-lookup"><span data-stu-id="3ddd8-182">Additional resources</span></span>

[<span data-ttu-id="3ddd8-183">配置域名</span><span class="sxs-lookup"><span data-stu-id="3ddd8-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3ddd8-184">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="3ddd8-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3ddd8-185">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="3ddd8-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3ddd8-186">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="3ddd8-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3ddd8-187">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="3ddd8-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3ddd8-188">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="3ddd8-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3ddd8-189">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="3ddd8-189">Enable location-based store detection</span></span>](enable-store-detection.md)
