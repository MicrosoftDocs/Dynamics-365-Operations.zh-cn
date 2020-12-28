---
title: Dynamics 365 Commerce 评估环境概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 评估环境。
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410380"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="6b9c5-103">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="6b9c5-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b9c5-104">此主题概述 Microsoft Dynamics 365 Commerce 评估环境。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="6b9c5-105">Commerce 评估环境不是公开发布的服务，它根据请求授予合作伙伴和客户使用权。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="6b9c5-106">有关详细信息，请联系您的 Microsoft 合作伙伴联系人。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="6b9c5-107">概览</span><span class="sxs-lookup"><span data-stu-id="6b9c5-107">Overview</span></span>

<span data-ttu-id="6b9c5-108">Commerce 评估环境是 Dynamics 365 Commerce 的一个可选的端到端环境，让合作伙伴和潜在客户可以试用 Commerce 产品。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="6b9c5-109">评估环境已部分预配置，以减少所需的预配后步骤。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="6b9c5-110">除了一些不影响特性或功能的小限制外，Commerce 评估环境提供了完整的 Commerce 体验，客户和实现合作伙伴可以使用它来评估产品、提供反馈以及进行适应/差距分析。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="6b9c5-111">Commerce 评估环境的限制</span><span class="sxs-lookup"><span data-stu-id="6b9c5-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="6b9c5-112">虽然 Commerce 评估环境提供了完整的 Commerce 特性和功能集，但仍存在一些小的限制：</span><span class="sxs-lookup"><span data-stu-id="6b9c5-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="6b9c5-113">尽管 Commerce 评估环境本身没有地理限制，但是环境的组件（例如 Retail Cloud Scale Unit (RCSU) 和电子商务应用程序）应只在美国预配。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="6b9c5-114">Commerce 评估环境的使用限制在从预配电子商务之日起 30 天。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="6b9c5-115">Commerce 评估环境只能在使用演示拓扑的环境中成功部署和初始化，环境的所有组件都部署在一个云托管的虚拟机 (VM) 中。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="6b9c5-116">这种拓扑的主要限制是对于环境可以支持的并发用户数。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="6b9c5-117">开始</span><span class="sxs-lookup"><span data-stu-id="6b9c5-117">Get started</span></span>

<span data-ttu-id="6b9c5-118">要预配 Commerce 评估环境，请参阅[预配 Commerce 评估环境](provisioning-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="6b9c5-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b9c5-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="6b9c5-119">Additional resources</span></span>

[<span data-ttu-id="6b9c5-120">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="6b9c5-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="6b9c5-121">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="6b9c5-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="6b9c5-122">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="6b9c5-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="6b9c5-123">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="6b9c5-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="6b9c5-124">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="6b9c5-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
