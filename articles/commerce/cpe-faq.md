---
title: Dynamics 365 Commerce 评估环境常见问题
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。
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
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599744"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="bc804-103">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="bc804-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bc804-104">本主题提供对有关 Microsoft Dynamics 365 Commerce 评估环境的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="bc804-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="bc804-105">**我们是否可以将 Commerce 评估环境用作当前实现 Retail 的客户的电子商务店面？**</span><span class="sxs-lookup"><span data-stu-id="bc804-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="bc804-106">编号</span><span class="sxs-lookup"><span data-stu-id="bc804-106">No.</span></span> <span data-ttu-id="bc804-107">Commerce 评估环境仅用于评估。</span><span class="sxs-lookup"><span data-stu-id="bc804-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="bc804-108">如果您需要针对实现 Retail 的客户的环境，请与 Microsoft 联系。</span><span class="sxs-lookup"><span data-stu-id="bc804-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="bc804-109">**可以使用 Commerce 评估环境在实现 Retail 的现有应用程序/环境基础上预配电子商务功能吗？**</span><span class="sxs-lookup"><span data-stu-id="bc804-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="bc804-110">不可以（通常）。</span><span class="sxs-lookup"><span data-stu-id="bc804-110">No (mostly).</span></span> <span data-ttu-id="bc804-111">Commerce 评估组件仅可用于与先决条件和预配指南中指定的配置匹配的环境。</span><span class="sxs-lookup"><span data-stu-id="bc804-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="bc804-112">此外，所需的基本演示数据在使用 10.0.8 之前的初始版本部署的环境中不可用。</span><span class="sxs-lookup"><span data-stu-id="bc804-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="bc804-113">**通过 Microsoft Dynamics Lifecycle Services (LCS) 在 Microsoft Azure 上部署 Commerce 评估环境会产生哪些成本？**</span><span class="sxs-lookup"><span data-stu-id="bc804-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="bc804-114">传统 Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce 总部演示环境（虚拟机 \[VM\]）将托管在 Azure 订阅中。</span><span class="sxs-lookup"><span data-stu-id="bc804-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="bc804-115">您可以使用 [Azure 定价计算器](https://azure.microsoft.com/pricing/calculator/)估算此成本。</span><span class="sxs-lookup"><span data-stu-id="bc804-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="bc804-116">其他组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）将作为服务型软件 (SaaS) 提供，由 Microsoft 托管。</span><span class="sxs-lookup"><span data-stu-id="bc804-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="bc804-117">**Commerce 评估环境当前支持哪些 Azure 地理位置？**</span><span class="sxs-lookup"><span data-stu-id="bc804-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="bc804-118">Commerce 评估环境只能在北美地区部署 。</span><span class="sxs-lookup"><span data-stu-id="bc804-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="bc804-119">**是否有具有完整的 OneBox 虚拟机 (VM) 选项的可下载虚拟硬盘 (VHD)？**</span><span class="sxs-lookup"><span data-stu-id="bc804-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="bc804-120">Dynamics 365 Commerce 和 Commerce Scale Unit 完全是服务型软件 (SaaS)，必须托管在云中。</span><span class="sxs-lookup"><span data-stu-id="bc804-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="bc804-121">**Commerce 评估环境可以使用多长时间？**</span><span class="sxs-lookup"><span data-stu-id="bc804-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="bc804-122">从 SaaS 组件（如 Commerce Scale Unit、Commerce 站点构建器和您的电子商务站点）预配之日起，Commerce 评估环境的期限为 30 天。</span><span class="sxs-lookup"><span data-stu-id="bc804-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="bc804-123">**我可以延长我的 Commerce 评估环境的时间限制吗？**</span><span class="sxs-lookup"><span data-stu-id="bc804-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="bc804-124">延长时限是标准之外的一个例外，会根据具体情况加以考虑。</span><span class="sxs-lookup"><span data-stu-id="bc804-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="bc804-125">您应该与 Microsoft 合作伙伴联系寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="bc804-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc804-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="bc804-126">Additional resources</span></span>

[<span data-ttu-id="bc804-127">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="bc804-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="bc804-128">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="bc804-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="bc804-129">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="bc804-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="bc804-130">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="bc804-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="bc804-131">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="bc804-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
