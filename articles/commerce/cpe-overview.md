---
title: Commerce 预览环境概述
description: 此主题概述 Microsoft Dynamics 365 Commerce 预览环境。
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906062"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="08378-103">Commerce 预览环境概述</span><span class="sxs-lookup"><span data-stu-id="08378-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="08378-104">此主题概述 Microsoft Dynamics 365 Commerce 预览环境。</span><span class="sxs-lookup"><span data-stu-id="08378-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="08378-105">概览</span><span class="sxs-lookup"><span data-stu-id="08378-105">Overview</span></span>

<span data-ttu-id="08378-106">Commerce 预览环境是 Dynamics 365 Commerce 的一个可选的端到端预览环境，让潜在客户可以在 Commerce 产品向公众发布之前试用该产品。</span><span class="sxs-lookup"><span data-stu-id="08378-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="08378-107">除了一些不影响特性或功能的小限制外，Commerce 预览环境提供了完整的 Commerce 体验，客户和实现合作伙伴可以使用它来评估产品、提供反馈以及进行适应/差距分析。</span><span class="sxs-lookup"><span data-stu-id="08378-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="08378-108">Commerce 预览环境的限制</span><span class="sxs-lookup"><span data-stu-id="08378-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="08378-109">虽然 Commerce 预览环境提供了完整的 Commerce 特性和功能集，但仍存在一些小的限制：</span><span class="sxs-lookup"><span data-stu-id="08378-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="08378-110">尽管 Commerce 预览环境本身没有地理限制，但是环境的组件（例如 Retail Cloud Scale Unit (RCSU) 和电子商务应用程序）只能在美国预配。</span><span class="sxs-lookup"><span data-stu-id="08378-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="08378-111">Commerce 预览环境的使用限制在从预配电子商务之日起 30 天。</span><span class="sxs-lookup"><span data-stu-id="08378-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="08378-112">Commerce 预览环境只能在使用演示拓扑的环境中成功部署和初始化，环境的所有组件都部署在一个虚拟机 (VM) 中。</span><span class="sxs-lookup"><span data-stu-id="08378-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="08378-113">这种 OneBox VM 拓扑的主要限制是对于预览环境可以支持的并发用户数。</span><span class="sxs-lookup"><span data-stu-id="08378-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="08378-114">Commerce 预览环境只能在 Commerce 产品公开发布 (GA) 之前评估。</span><span class="sxs-lookup"><span data-stu-id="08378-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="08378-115">GA 之后将提供新的演示环境。</span><span class="sxs-lookup"><span data-stu-id="08378-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="08378-116">入门</span><span class="sxs-lookup"><span data-stu-id="08378-116">Get started</span></span>

<span data-ttu-id="08378-117">要预配 Commerce 预览环境，请参阅[预配 Commerce 预览环境](provisioning-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="08378-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08378-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="08378-118">Additional resources</span></span>

[<span data-ttu-id="08378-119">预配 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="08378-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="08378-120">配置 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="08378-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="08378-121">为 Commerce 预览环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="08378-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="08378-122">Commerce 预览环境常见问题</span><span class="sxs-lookup"><span data-stu-id="08378-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
