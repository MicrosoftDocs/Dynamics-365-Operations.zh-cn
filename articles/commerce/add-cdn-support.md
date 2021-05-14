---
title: 添加对内容交付网络 (CDN) 的支持
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936822"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="b308e-103">添加对内容分发网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="b308e-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b308e-104">此主题介绍如何向 Microsoft Dynamics 365 Commerce 环境添加内容交付网络 (CDN)。</span><span class="sxs-lookup"><span data-stu-id="b308e-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="b308e-105">在 Dynamics 365 Commerce 中设置电子商务环境时，可将其配置为使用 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="b308e-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="b308e-106">您可以在电子商务环境的预配过程中启用自定义域。</span><span class="sxs-lookup"><span data-stu-id="b308e-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="b308e-107">也可以在预配过程完成后使用服务请求设置。</span><span class="sxs-lookup"><span data-stu-id="b308e-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="b308e-108">电子商务环境的预配过程将生成一个与该环境关联的主机名。</span><span class="sxs-lookup"><span data-stu-id="b308e-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="b308e-109">此主机名采用以下格式，其中，\<*e-commerce-tenant-name*\> 是您的环境的名称：</span><span class="sxs-lookup"><span data-stu-id="b308e-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="b308e-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="b308e-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="b308e-111">预配过程中生成的主机名或终结点仅支持 \*.commerce.dynamics.com 采用安全套接字层 (SSL) 证书。</span><span class="sxs-lookup"><span data-stu-id="b308e-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="b308e-112">不支持自定义域支持采用 SSL。</span><span class="sxs-lookup"><span data-stu-id="b308e-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="b308e-113">因此，必须在 CDN 中终止自定义的 SSL，并将流量从 CDN 转发到 Commerce 生成的主机名或终结点。</span><span class="sxs-lookup"><span data-stu-id="b308e-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="b308e-114">此外，Commerce 生成的终结点 (\*.commerce.dynamics.com) 还将提供 *统计信息*（JavaScript 或级联样式表 \[CSS\] 文件）。</span><span class="sxs-lookup"><span data-stu-id="b308e-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="b308e-115">仅当将 Commerce 生成的主机名或终结点放在 CDN 后面时，才可以缓存这些统计信息。</span><span class="sxs-lookup"><span data-stu-id="b308e-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="b308e-116">设置 SSL</span><span class="sxs-lookup"><span data-stu-id="b308e-116">Set up SSL</span></span>

<span data-ttu-id="b308e-117">在为 Commerce 环境预配提供自定义域或使用服务请求为环境提供自定义域之后，您需要与 Commerce 入职团队协作以计划 DNS 更改。</span><span class="sxs-lookup"><span data-stu-id="b308e-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="b308e-118">前面介绍过，生成的主机名或终结点仅支持对 \*.commerce.dynamics.com 使用 SSL 证书。</span><span class="sxs-lookup"><span data-stu-id="b308e-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="b308e-119">不支持自定义域支持采用 SSL。</span><span class="sxs-lookup"><span data-stu-id="b308e-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="b308e-120">CDN 服务</span><span class="sxs-lookup"><span data-stu-id="b308e-120">CDN services</span></span>

<span data-ttu-id="b308e-121">所有 CDN 服务都可以用于 Commerce 环境。</span><span class="sxs-lookup"><span data-stu-id="b308e-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="b308e-122">下面是两个示例：</span><span class="sxs-lookup"><span data-stu-id="b308e-122">Here are two examples:</span></span>

- <span data-ttu-id="b308e-123">**Microsoft Azure Front Door Service** – Azure CDN 解决方案。</span><span class="sxs-lookup"><span data-stu-id="b308e-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="b308e-124">有关 Azure Front Door Service 的详细信息，请参阅[Azure Front Door Service 文档](/azure/frontdoor/)。</span><span class="sxs-lookup"><span data-stu-id="b308e-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](/azure/frontdoor/).</span></span>
- <span data-ttu-id="b308e-125">**Akamai Dynamic Site Accelerator** – 有关详细信息，请参阅 [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)。</span><span class="sxs-lookup"><span data-stu-id="b308e-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="b308e-126">CDN 设置</span><span class="sxs-lookup"><span data-stu-id="b308e-126">CDN setup</span></span>

<span data-ttu-id="b308e-127">CDN 的设置过程通常包含下面的步骤：</span><span class="sxs-lookup"><span data-stu-id="b308e-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="b308e-128">添加前端主机。</span><span class="sxs-lookup"><span data-stu-id="b308e-128">Add a front-end host.</span></span>
1. <span data-ttu-id="b308e-129">配置后端池。</span><span class="sxs-lookup"><span data-stu-id="b308e-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="b308e-130">设置传递规则。</span><span class="sxs-lookup"><span data-stu-id="b308e-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="b308e-131">添加前端主机</span><span class="sxs-lookup"><span data-stu-id="b308e-131">Add a front-end host</span></span>

<span data-ttu-id="b308e-132">可使用任何 CDN 服务，但是本主题中的示例则使用 Azure Front Door Service。</span><span class="sxs-lookup"><span data-stu-id="b308e-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="b308e-133">有关如何设置 Azure Front Door Service 的信息，请参阅[快速入门：为高可用全局 Web 应用程序创建 Front Door](/azure/frontdoor/quickstart-create-front-door)。</span><span class="sxs-lookup"><span data-stu-id="b308e-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="b308e-134">在 Azure Front Door 服务中配置后端池</span><span class="sxs-lookup"><span data-stu-id="b308e-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="b308e-135">若要在 Azure Front Door 服务中配置后端池，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b308e-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="b308e-136">将 **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** 添加到后端池作为自定义主机，其后端主机标头与 **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** 相同。</span><span class="sxs-lookup"><span data-stu-id="b308e-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="b308e-137">在 **负载平衡** 下，保留默认值。</span><span class="sxs-lookup"><span data-stu-id="b308e-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="b308e-138">禁用后端池的运行状况检查。</span><span class="sxs-lookup"><span data-stu-id="b308e-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="b308e-139">下图显示 Azure Front Door 服务中输入了后端主机名的 **添加后端** 对话框。</span><span class="sxs-lookup"><span data-stu-id="b308e-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![“添加后端池”对话框](./media/CDN_BackendPool.png)

<span data-ttu-id="b308e-141">下图显示 Azure Front Door 服务中具有默认负载均衡值的 **添加后端池** 对话框。</span><span class="sxs-lookup"><span data-stu-id="b308e-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![“添加后端池”对话框（续）](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="b308e-143">当为 Commerce 设置自己的 Azure Front Door 服务时，请确保禁用 **运行状况探测**。</span><span class="sxs-lookup"><span data-stu-id="b308e-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="b308e-144">在 Azure Front Door Service 中设置规则</span><span class="sxs-lookup"><span data-stu-id="b308e-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="b308e-145">若要在 Azure Front Door Service 中设置传递规则，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b308e-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="b308e-146">添加一个传递规则。</span><span class="sxs-lookup"><span data-stu-id="b308e-146">Add a routing rule.</span></span>
1. <span data-ttu-id="b308e-147">在 **名称** 字段中，输入 **默认**。</span><span class="sxs-lookup"><span data-stu-id="b308e-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="b308e-148">在 **接受的协议** 字段中，选择 **HTTP 和 HTTPS**。</span><span class="sxs-lookup"><span data-stu-id="b308e-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="b308e-149">在 **前端主机** 字段中，输入 **dynamics-ecom-tenant-name.azurefd.net**。</span><span class="sxs-lookup"><span data-stu-id="b308e-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="b308e-150">在 **匹配模式** 下的上方字段中，输入 **/\***。</span><span class="sxs-lookup"><span data-stu-id="b308e-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="b308e-151">在 **传递详细信息** 下，将 **传递类型** 设置为 **转发**。</span><span class="sxs-lookup"><span data-stu-id="b308e-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="b308e-152">在 **后端池** 字段中，选择 **ecom-backend**。</span><span class="sxs-lookup"><span data-stu-id="b308e-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="b308e-153">在 **转发协议** 字段组中，选择 **匹配请求** 选项。</span><span class="sxs-lookup"><span data-stu-id="b308e-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="b308e-154">将 **URL 重写** 选项设置为 **禁用**。</span><span class="sxs-lookup"><span data-stu-id="b308e-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="b308e-155">将 **缓存** 选项设置为 **禁用**。</span><span class="sxs-lookup"><span data-stu-id="b308e-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="b308e-156">如果要使用的域已激活且处于活动状态，请从 [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) 中的 **支持** 磁贴创建支持票证来获取后续步骤的帮助。</span><span class="sxs-lookup"><span data-stu-id="b308e-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="b308e-157">有关详细信息，请参阅[获取对 Finance and Operations 应用或 Lifecycle Services (LCS) 的支持](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)。</span><span class="sxs-lookup"><span data-stu-id="b308e-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="b308e-158">如果您的域是新域，而不是预先存在的活动域，您可以将自定义域添加到 Azure Front Door 服务的配置中。</span><span class="sxs-lookup"><span data-stu-id="b308e-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="b308e-159">这将使 Web 流量可以通过 Azure Front Door 实例定向到您的站点。</span><span class="sxs-lookup"><span data-stu-id="b308e-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="b308e-160">若要添加自定义域（如 `www.fabrikam.com`），必须为该域配置一个规范名称 (CNAME)。</span><span class="sxs-lookup"><span data-stu-id="b308e-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="b308e-161">下图显示 Azure Front Door Service 中的 **CNAME 配置** 对话框。</span><span class="sxs-lookup"><span data-stu-id="b308e-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![“CNAME 配置”对话框](./media/CNAME_Configuration.png)

<span data-ttu-id="b308e-163">可使用 Azure Front Door Service 管理证书，也可以对自定义域使用您自己的证书。</span><span class="sxs-lookup"><span data-stu-id="b308e-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="b308e-164">下图显示 Azure Front Door Service 中的 **自定义域 HTTPS** 对话框。</span><span class="sxs-lookup"><span data-stu-id="b308e-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![“自定义域 HTTPS”对话框](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="b308e-166">有关将自定义域添加到 Azure Front Door 的详细说明，请参阅[将自定义域添加到 Front Door](/azure/frontdoor/front-door-custom-domain)。</span><span class="sxs-lookup"><span data-stu-id="b308e-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="b308e-167">现在应该已经正确配置了您的 CDN，可将其用于您的 Commerce 站点。</span><span class="sxs-lookup"><span data-stu-id="b308e-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b308e-168">其他资源</span><span class="sxs-lookup"><span data-stu-id="b308e-168">Additional resources</span></span>

[<span data-ttu-id="b308e-169">内容交付网络实施选项</span><span class="sxs-lookup"><span data-stu-id="b308e-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]