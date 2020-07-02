---
title: Dynamics 365 Supply Chain Management 客户门户概述
description: 本主题介绍客户门户，并说明谁应该使用它及其如何工作。
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 709ba18be9e2edd5d0a7f143aaed5ef94f365b91
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456918"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a><span data-ttu-id="6413f-103">Dynamics 365 Supply Chain Management 客户门户概述</span><span class="sxs-lookup"><span data-stu-id="6413f-103">Customer portal for Dynamics 365 Supply Chain Management overview</span></span>

## <a name="what-is-the-customer-portal"></a><span data-ttu-id="6413f-104">什么是客户门户？</span><span class="sxs-lookup"><span data-stu-id="6413f-104">What is the Customer portal?</span></span>

<span data-ttu-id="6413f-105">现代供应链系统依赖于集成。</span><span class="sxs-lookup"><span data-stu-id="6413f-105">Modern supply chain systems rely on integration.</span></span> <span data-ttu-id="6413f-106">他们需要库存、客户需求和销售部门集成在一起，而不是各自位于单独的孤岛。</span><span class="sxs-lookup"><span data-stu-id="6413f-106">They require that inventory, customer demand, and sales departments be integrated instead of residing in separate silos.</span></span> <span data-ttu-id="6413f-107">客户门户可帮助运行 Microsoft Dynamics 365 Supply Chain Management 的组织增强这种集成，并更有效地让客户了解情况。</span><span class="sxs-lookup"><span data-stu-id="6413f-107">The Customer portal helps organizations that run Microsoft Dynamics 365 Supply Chain Management enhance this integration and more effectively keep their customers informed.</span></span>

<span data-ttu-id="6413f-108">客户门户是一个 [Power Apps 门户](https://docs.microsoft.com/powerapps/maker/portals/overview)模板，让公司可以为与销售订单处理相关的场景创建一个面向外部的企业到企业 (B2B) 网站。</span><span class="sxs-lookup"><span data-stu-id="6413f-108">The Customer portal is a [Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) template that lets companies create an externally facing business-to-business (B2B) website for scenarios that are related to sales order processing.</span></span> <span data-ttu-id="6413f-109">此模板使用[双写入](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)、Supply Chain Management 和 Power Apps 门户支持外部企业客户从公司的 Dynamics 365 环境中查看和创建数据。</span><span class="sxs-lookup"><span data-stu-id="6413f-109">The template uses [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management, and Power Apps portals to enable external enterprise customers to view and create data from the company's Dynamics 365 environment.</span></span>

<span data-ttu-id="6413f-110">客户门户模板具有 Power Apps 的门户功能提供的所有自定义功能。</span><span class="sxs-lookup"><span data-stu-id="6413f-110">The Customer portal template has all the customization capabilities that the portals feature of Power Apps offers.</span></span> <span data-ttu-id="6413f-111">此模板可以轻松修改来表示公司的品牌、添加更多功能，以及更改用户体验。</span><span class="sxs-lookup"><span data-stu-id="6413f-111">The template can easily be modified to represent the company's brand, add increased functionality, and change the user experience.</span></span> <span data-ttu-id="6413f-112">此模板现在提供的所有功能都可以根据需要修改。</span><span class="sxs-lookup"><span data-stu-id="6413f-112">All the functionality that the template offers out of the box can be modified as desired.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6413f-113">单是模板本身，不能提供完整功能。</span><span class="sxs-lookup"><span data-stu-id="6413f-113">By itself, the template isn't expected to be completely functional.</span></span> <span data-ttu-id="6413f-114">对于希望创建面向外部的网站，以便企业客户可以与 Supply Chain Management 中的数据进行交互的客户，它只是充当一个使能者。</span><span class="sxs-lookup"><span data-stu-id="6413f-114">It just serves as an enabler for customers who want to create an externally facing website so that enterprise customers can engage with data from Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="6413f-115">客户门户文档面向将为 Supply Chain Management 安装设置客户门户的管理员、定制员和系统集成商。</span><span class="sxs-lookup"><span data-stu-id="6413f-115">The Customer portal documentation is directed at admins, customizers, and system integrators who will set up the Customer portal for a Supply Chain Management installation.</span></span> <span data-ttu-id="6413f-116">它使用术语_客户_和_用户_描述属于运行 Supply Chain Management 的组织的客户，以及将使用最终门户的人员。</span><span class="sxs-lookup"><span data-stu-id="6413f-116">It uses the terms _customer_ and _user_ to describe people who are customers of the organization that is running Supply Chain Management, and who will use the final portal itself.</span></span>

## <a name="video"></a><span data-ttu-id="6413f-117">视频</span><span class="sxs-lookup"><span data-stu-id="6413f-117">Video</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

<span data-ttu-id="6413f-118">[Dynamics 365 Supply Chain Management 中的客户门户模板概述](https://youtu.be/nPrqoLuHfV8)视频（上方所示）包含在 YouTube 上的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="6413f-118">The [Overview of the Customer portal template in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="who-should-use-it"></a><span data-ttu-id="6413f-119">谁应该使用它？</span><span class="sxs-lookup"><span data-stu-id="6413f-119">Who should use it?</span></span>

<span data-ttu-id="6413f-120">客户门户是为运行 Supply Chain Management 并具有以下特征的公司设计的：</span><span class="sxs-lookup"><span data-stu-id="6413f-120">The Customer portal is designed for companies that run Supply Chain Management and have these characteristics:</span></span>

- <span data-ttu-id="6413f-121">他们希望构建一个面向外部的网站，该网站将订单处理信息（如订单状态或帐户信息）直接从其 Supply Chain Management 系统传达到其企业客户。</span><span class="sxs-lookup"><span data-stu-id="6413f-121">They want to build an externally facing website that communicates order processing information (such as order status or account information) directly from their Supply Chain Management system to their enterprise customers.</span></span>
- <span data-ttu-id="6413f-122">他们正在从 Dynamics AX 2012 转移到 Supply Chain Management，以前使用 [AX 2012 客户自助服务门户](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal)。</span><span class="sxs-lookup"><span data-stu-id="6413f-122">They are transitioning from Dynamics AX 2012 to Supply Chain Management and previously used the [AX 2012 Customer self-service portal](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).</span></span>

<span data-ttu-id="6413f-123">以下类型的组织**不**是实施客户门户的理想候选人：</span><span class="sxs-lookup"><span data-stu-id="6413f-123">The following types of organizations are **not** good candidates for implementing the Customer portal:</span></span>

- <span data-ttu-id="6413f-124">希望为非企业客户构建网站的公司。</span><span class="sxs-lookup"><span data-stu-id="6413f-124">Companies that want to build a website for non-enterprise customers.</span></span> <span data-ttu-id="6413f-125">这些公司应该考虑创建 [Dynamics 365 Commerce 电子商务网站](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site)。</span><span class="sxs-lookup"><span data-stu-id="6413f-125">These companies should consider creating a [Dynamics 365 Commerce e-commerce website](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).</span></span>
- <span data-ttu-id="6413f-126">已经将现有 Power Apps 门户网站用于类似目的的公司。</span><span class="sxs-lookup"><span data-stu-id="6413f-126">Companies that are already using an existing Power Apps portals website for a similar purpose.</span></span> <span data-ttu-id="6413f-127">这些公司不会从客户门户获得任何其他好处。</span><span class="sxs-lookup"><span data-stu-id="6413f-127">These companies won't receive any additional benefits from the Customer portal.</span></span> <span data-ttu-id="6413f-128">客户门户作为模板提供，它充当希望在双写入、Supply Chain Management 和 Power Apps 门户之间“连接点”的客户的指南和起点。</span><span class="sxs-lookup"><span data-stu-id="6413f-128">The Customer portal is delivered as a template that acts as a guide and a starting point for customers who want to "connect the dots" between dual-write, Supply Chain Management, and Power Apps portals.</span></span> <span data-ttu-id="6413f-129">如果您已经设置了一个用于此目的的网站，使用客户门户模板重新预配该网站可能不会获得太多价值。</span><span class="sxs-lookup"><span data-stu-id="6413f-129">If you've already set up a website that serves this purpose, you might not gain much value from using the Customer portal template to re-provision that website.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="6413f-130">工作原理</span><span class="sxs-lookup"><span data-stu-id="6413f-130">How does it work?</span></span>

<span data-ttu-id="6413f-131">客户门户作为 Power Apps 门户模板提供。</span><span class="sxs-lookup"><span data-stu-id="6413f-131">The Customer portal is provided as a Power Apps portals template.</span></span> <span data-ttu-id="6413f-132">依赖 Power Apps 门户和双写入。</span><span class="sxs-lookup"><span data-stu-id="6413f-132">It depends on Power Apps portals and dual-write.</span></span>

<span data-ttu-id="6413f-133">[Power Apps 门户](https://docs.microsoft.com/powerapps/maker/portals/overview)是一项功能，让用户可以创建面向外部的网站，组织外部的人员可以登录到该网站。</span><span class="sxs-lookup"><span data-stu-id="6413f-133">[Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) is a feature that lets users create an externally facing website that people from outside the organization can sign in to.</span></span> <span data-ttu-id="6413f-134">创建门户几乎不需要编码。</span><span class="sxs-lookup"><span data-stu-id="6413f-134">Little to no coding is required to make portals.</span></span> <span data-ttu-id="6413f-135">客户门户是众多 [Dynamics 365 门户模板](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365)之一，可以从 Microsoft 获得。</span><span class="sxs-lookup"><span data-stu-id="6413f-135">The Customer portal is one of many [Dynamics 365 portal templates](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) that are available from Microsoft.</span></span>

<span data-ttu-id="6413f-136">[双写入](https://docs.microsoft.com/powerapps/maker/portals/overview)是一种自带的基础结构产品，提供 Dynamics 365 中的模型驱动应用与 Finance and Operations 应用之间的近实时交互。</span><span class="sxs-lookup"><span data-stu-id="6413f-136">[Dual-write](https://docs.microsoft.com/powerapps/maker/portals/overview) is an out-of-box infrastructure product that provides near-real-time interaction between model-driven apps in Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="6413f-137">双写入提供 Finance and Operations 应用与 Common Data Service 之间的双向集成。</span><span class="sxs-lookup"><span data-stu-id="6413f-137">Dual-write provides bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="6413f-138">因此，它可以提供应用之间的集成用户体验。</span><span class="sxs-lookup"><span data-stu-id="6413f-138">Therefore, it provides an integrated user experience across the apps.</span></span> <span data-ttu-id="6413f-139">客户门户依赖于与双写入同步的实体。</span><span class="sxs-lookup"><span data-stu-id="6413f-139">The Customer portal depends on entities that are synced with dual-write.</span></span> <span data-ttu-id="6413f-140">必须先对所有适当的实体启用双写入，才能在客户门户中显示来自 Supply Chain Management 的数据。</span><span class="sxs-lookup"><span data-stu-id="6413f-140">Before data from Supply Chain Management can be surfaced in the Customer portal, dual-write must be enabled for all the appropriate entities.</span></span>

<span data-ttu-id="6413f-141">![客户门户依赖关系](media/customer-portal-elements.png "客户门户依赖关系")</span><span class="sxs-lookup"><span data-stu-id="6413f-141">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="6413f-142">对于想要使用 Power Apps 门户构建面向外部的使用其 Supply Chain Management 安装中数据的网站的组织，客户门户充当一个起点。</span><span class="sxs-lookup"><span data-stu-id="6413f-142">The Customer portal acts as a starting point for organizations that want to use Power Apps portals to build an externally facing website that uses data from their Supply Chain Management installation.</span></span> <span data-ttu-id="6413f-143">它帮助组织连接双写入、Supply Chain Management 和 Power Apps 门户。</span><span class="sxs-lookup"><span data-stu-id="6413f-143">It helps organizations connect dual-write, Supply Chain Management, and Power Apps portals.</span></span>
