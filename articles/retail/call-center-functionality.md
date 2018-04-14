---
title: "呼叫中心功能"
description: "本主题提供 Microsoft Dynamics 365 for Retail 中呼叫中心销售功能的概览。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: dd35e895cdfe402b9d22e710c7b0166eadf412ff
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="b4107-103">呼叫中心功能</span><span class="sxs-lookup"><span data-stu-id="b4107-103">Call center functionality</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="b4107-104">本文提供 Microsoft Dynamics 365 for Retail 中呼叫中心销售功能的概览。</span><span class="sxs-lookup"><span data-stu-id="b4107-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="b4107-105">Dynamics 365 for Retail 支持电话中心作为一类零售渠道。</span><span class="sxs-lookup"><span data-stu-id="b4107-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="b4107-106">在呼叫中心，工作人员通过电话接收客户的订单并创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="b4107-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="b4107-107">呼叫中心功能包括旨在简化接收电话订单并通过订单填写流程处理客户服务。</span><span class="sxs-lookup"><span data-stu-id="b4107-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="b4107-108">例如，呼叫中心员工可直接将付款信息输入到销售订单，并可以在提交订单前查看费用和付款的详细摘要。</span><span class="sxs-lookup"><span data-stu-id="b4107-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="b4107-109">工作人员还可以控制定价，以及在**“销售订单”**页中访问有关客户、产品和价格的各种数据。</span><span class="sxs-lookup"><span data-stu-id="b4107-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="b4107-110">此外，呼叫中心也增强了跟踪客户历史记录和订单状态的功能。</span><span class="sxs-lookup"><span data-stu-id="b4107-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="b4107-111">每个呼叫中心可以拥有自己的用户、付款方式、价格组、财务维度和交货方式。</span><span class="sxs-lookup"><span data-stu-id="b4107-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="b4107-112">当您创建呼叫中心时，可以配置这些选项。</span><span class="sxs-lookup"><span data-stu-id="b4107-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="b4107-113">此外，您还可以使用**“呼叫中心”**页来启用或禁用对呼叫中心唯一的以下功能组：</span><span class="sxs-lookup"><span data-stu-id="b4107-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="b4107-114">**订单完成** - 此组包括与**“销售订单”**页上的付款和订单完成相关的功能。</span><span class="sxs-lookup"><span data-stu-id="b4107-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="b4107-115">**直接销售** - 此组包括与源代码、脚本和目录请求相关的功能。</span><span class="sxs-lookup"><span data-stu-id="b4107-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="b4107-116">在呼叫中心设置中启用这些功能后，与呼叫中心关联的用户便可以在**“销售订单”**页上使用它们。</span><span class="sxs-lookup"><span data-stu-id="b4107-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="b4107-117">在可以使用这些功能之前，大多数功能都需要进行其他设置。</span><span class="sxs-lookup"><span data-stu-id="b4107-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="b4107-118">您必须先将这些用户作为呼叫中心用户添加到呼叫中心，然后这些用户才能创建呼叫中心订单。</span><span class="sxs-lookup"><span data-stu-id="b4107-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="b4107-119">此步骤将启用呼叫中心渠道特定配置和功能。</span><span class="sxs-lookup"><span data-stu-id="b4107-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="b4107-120">下面是变得可用的功能的一些示例：</span><span class="sxs-lookup"><span data-stu-id="b4107-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="b4107-121">引导式销售为远程销售脚本和产品图像提供了配置选项，以便在销售员接受订单时为其提供帮助和指导。</span><span class="sxs-lookup"><span data-stu-id="b4107-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="b4107-122">订单在销售员捕获至少一种付款方式后才能完成。</span><span class="sxs-lookup"><span data-stu-id="b4107-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="b4107-123">可配置追加销售和交叉销售规则来提示销售员将特定产品推销给客户。</span><span class="sxs-lookup"><span data-stu-id="b4107-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="b4107-124">销售员可为客户正在从中订购产品的目录捕获源代码。</span><span class="sxs-lookup"><span data-stu-id="b4107-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="b4107-125">销售员可将零售商添加优惠券到订单。</span><span class="sxs-lookup"><span data-stu-id="b4107-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="b4107-126">销售员可销售连续性计划。</span><span class="sxs-lookup"><span data-stu-id="b4107-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="b4107-127">可以手动或自动暂停订单，以指示需要先进行额外调查才能处理订单。</span><span class="sxs-lookup"><span data-stu-id="b4107-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





