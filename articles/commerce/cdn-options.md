---
title: 内容分发网络实施选项
description: 本主题回顾了可用于 Microsoft Dynamics 365 Commerce 环境的内容分发网络 (CDN) 实施的不同选项。 这些选项包括由 Commerce 提供的 Azure Front Door 本机实例，以及客户拥有的 Azure Front Door 实例。
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9e98cf81f13b9181059bc96b95ac277a088311ea
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800703"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="b29b3-104">内容分发网络实施选项</span><span class="sxs-lookup"><span data-stu-id="b29b3-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b29b3-105">本主题回顾了可用于 Microsoft Dynamics 365 Commerce 环境的内容分发网络 (CDN) 实施的不同选项。</span><span class="sxs-lookup"><span data-stu-id="b29b3-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="b29b3-106">这些选项包括由 Commerce 提供的 Azure Front Door 本机实例，以及客户拥有的 Azure Front Door 实例。</span><span class="sxs-lookup"><span data-stu-id="b29b3-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="b29b3-107">当 Commerce 客户考虑在其 Commerce 环境中使用哪种 CDN 服务时，有若干种选择。</span><span class="sxs-lookup"><span data-stu-id="b29b3-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="b29b3-108">Commerce 随基本 Azure Front Door 支持一起发布，该支持可满足基本托管和自定义域要求。</span><span class="sxs-lookup"><span data-stu-id="b29b3-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="b29b3-109">对于需要加强控制和 Web 应用程序防火墙 (WAF) 等更具体的安全功能的公司，最佳选择可能是使用客户拥有的 Azure Front Door 实例或外部 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="b29b3-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="b29b3-110">以下三个 CDN 实施选项可用于 Commerce 环境：</span><span class="sxs-lookup"><span data-stu-id="b29b3-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="b29b3-111">Commerce 提供的 Azure Front Door 实例</span><span class="sxs-lookup"><span data-stu-id="b29b3-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="b29b3-112">客户拥有的 Azure Front Door 实例（用于加强控制和其他安全功能）</span><span class="sxs-lookup"><span data-stu-id="b29b3-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="b29b3-113">外部 CDN 服务</span><span class="sxs-lookup"><span data-stu-id="b29b3-113">An external CDN service</span></span>

<span data-ttu-id="b29b3-114">所有这三个 CDN 实施选项都仅提供来自自定义域的动态 HTML 内容。</span><span class="sxs-lookup"><span data-stu-id="b29b3-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="b29b3-115">Commerce 会通过 Microsoft 托管的 CDN 自动处理所有 JavaScript、级联样式表 (CSS)、图像、视频和其他静态内容。</span><span class="sxs-lookup"><span data-stu-id="b29b3-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="b29b3-116">您选择的选项决定了可用的操作功能、控制功能和其他安全功能。</span><span class="sxs-lookup"><span data-stu-id="b29b3-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="b29b3-117">下图显示了 Commerce 体系结构的概览。</span><span class="sxs-lookup"><span data-stu-id="b29b3-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Commerce 体系结构概览](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="b29b3-119">有关如何为您的 Commerce 站点设置 Azure Front Door 实例的更多信息，请参见[添加 CDN 支持](add-cdn-support.md)。</span><span class="sxs-lookup"><span data-stu-id="b29b3-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="b29b3-120">使用 Commerce 提供的 Azure Front Door 实例</span><span class="sxs-lookup"><span data-stu-id="b29b3-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="b29b3-121">下表列出了使用 Commerce 提供的 Azure Front Door 实例来管理内容终结点的利弊。</span><span class="sxs-lookup"><span data-stu-id="b29b3-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="b29b3-122">优点</span><span class="sxs-lookup"><span data-stu-id="b29b3-122">Pros</span></span> | <span data-ttu-id="b29b3-123">缺点</span><span class="sxs-lookup"><span data-stu-id="b29b3-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="b29b3-124">该实例已包含在 Commerce 成本中。</span><span class="sxs-lookup"><span data-stu-id="b29b3-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="b29b3-125">因为实例是由 Commerce 团队管理的，所以需要的维护较少，并且有共享的设置步骤。</span><span class="sxs-lookup"><span data-stu-id="b29b3-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="b29b3-126">Azure 托管的基础结构具有可伸缩性、安全性和可靠性。</span><span class="sxs-lookup"><span data-stu-id="b29b3-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="b29b3-127">安全套接字层 (SSL) 证书需要一次性设置并且会自动更新。</span><span class="sxs-lookup"><span data-stu-id="b29b3-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="b29b3-128">Commerce 团队将监视实例是否有错误和异常。</span><span class="sxs-lookup"><span data-stu-id="b29b3-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="b29b3-129">WAF 不受支持。</span><span class="sxs-lookup"><span data-stu-id="b29b3-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="b29b3-130">没有特定的自定义或设置调整。</span><span class="sxs-lookup"><span data-stu-id="b29b3-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="b29b3-131">实例依靠 Commerce 团队进行更新或更改。</span><span class="sxs-lookup"><span data-stu-id="b29b3-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="b29b3-132">Apex 域需要一个单独的 Azure Front Door 实例，并且需要额外的工作才能将 apex 域与 Azure DNS 集成。</span><span class="sxs-lookup"><span data-stu-id="b29b3-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="b29b3-133">没有向客户提供有关每秒响应次数 (RPS) 或错误率的遥测。</span><span class="sxs-lookup"><span data-stu-id="b29b3-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="b29b3-134">下图显示了由 Commerce 提供的 Azure Front Door 实例的体系结构。</span><span class="sxs-lookup"><span data-stu-id="b29b3-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Commerce 提供的 Azure Front Door 实例](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="b29b3-136">使用客户拥有的 Azure Front Door 实例</span><span class="sxs-lookup"><span data-stu-id="b29b3-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="b29b3-137">下表列出了使用客户拥有的 Azure Front Door 实例来管理内容终结点的利弊。</span><span class="sxs-lookup"><span data-stu-id="b29b3-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="b29b3-138">优点</span><span class="sxs-lookup"><span data-stu-id="b29b3-138">Pros</span></span> | <span data-ttu-id="b29b3-139">缺点</span><span class="sxs-lookup"><span data-stu-id="b29b3-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="b29b3-140">设置既安全又易于管理。</span><span class="sxs-lookup"><span data-stu-id="b29b3-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="b29b3-141">Azure 托管的基础结构具有可伸缩性、安全性和可靠性。</span><span class="sxs-lookup"><span data-stu-id="b29b3-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="b29b3-142">该实例允许进行 WAF 集成和精细的规则控制，以实现针对您的站点专门调整的更高级别的安全性。</span><span class="sxs-lookup"><span data-stu-id="b29b3-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="b29b3-143">该实例允许更好地控制 SSL 证书（客户拥有的证书和由 Azure Front Door 托管的证书）和域链接。</span><span class="sxs-lookup"><span data-stu-id="b29b3-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="b29b3-144">如果该实例直接与 Azure DNS 配对，则该实例将提供一个 apex 域解决方案。</span><span class="sxs-lookup"><span data-stu-id="b29b3-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="b29b3-145">提供了遥测和警报。</span><span class="sxs-lookup"><span data-stu-id="b29b3-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="b29b3-146">SSL 证书需要一次性设置并且会自动更新。</span><span class="sxs-lookup"><span data-stu-id="b29b3-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="b29b3-147">此实例是自我托管型实例。</span><span class="sxs-lookup"><span data-stu-id="b29b3-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="b29b3-148">需要初步的知识提升。</span><span class="sxs-lookup"><span data-stu-id="b29b3-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="b29b3-149">下图显示了一个包含客户拥有的 Azure Front Door 实例的 Commerce 基础结构。</span><span class="sxs-lookup"><span data-stu-id="b29b3-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![包含客户拥有的 Azure Front Door 实例的 Commerce 基础结构](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="b29b3-151">使用外部 CDN 服务</span><span class="sxs-lookup"><span data-stu-id="b29b3-151">Use an external CDN service</span></span>

<span data-ttu-id="b29b3-152">下表列出了使用外部 CDN 服务管理内容终结点的利弊。</span><span class="sxs-lookup"><span data-stu-id="b29b3-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="b29b3-153">优点</span><span class="sxs-lookup"><span data-stu-id="b29b3-153">Pros</span></span> | <span data-ttu-id="b29b3-154">缺点</span><span class="sxs-lookup"><span data-stu-id="b29b3-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="b29b3-155">当现有域已经托管在外部 CDN 上时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="b29b3-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="b29b3-156">竞争对手的 CDN（例如 Akamai）可能具有更多的 WAF 功能。</span><span class="sxs-lookup"><span data-stu-id="b29b3-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="b29b3-157">需要单独的合同和额外的成本计算。</span><span class="sxs-lookup"><span data-stu-id="b29b3-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="b29b3-158">SSL 可能会产生额外费用。</span><span class="sxs-lookup"><span data-stu-id="b29b3-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="b29b3-159">由于该服务与 Azure 云结构是分开的，因此必须管理其他基础结构。</span><span class="sxs-lookup"><span data-stu-id="b29b3-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="b29b3-160">该服务可能需要在终结点和安全性设置上投入较多时间。</span><span class="sxs-lookup"><span data-stu-id="b29b3-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="b29b3-161">此服务是自我托管型服务。</span><span class="sxs-lookup"><span data-stu-id="b29b3-161">The service is self-managed.</span></span></li><li><span data-ttu-id="b29b3-162">此服务是自我监控型服务。</span><span class="sxs-lookup"><span data-stu-id="b29b3-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="b29b3-163">下图显示了包含外部 CDN 服务的 Commerce 基础结构。</span><span class="sxs-lookup"><span data-stu-id="b29b3-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![包含外部 CDN 服务的 Commerce 基础架构](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="b29b3-165">其他资源</span><span class="sxs-lookup"><span data-stu-id="b29b3-165">Additional resources</span></span>

[<span data-ttu-id="b29b3-166">添加对内容分发网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="b29b3-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
