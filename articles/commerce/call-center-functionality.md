---
title: 呼叫中心销售功能
description: 本主题提供 Dynamics 365 Commerce 中呼叫中心销售功能的概览。
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d188138654ba20d8393ed4bca8124a65402daff2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991432"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="144d9-103">呼叫中心销售功能</span><span class="sxs-lookup"><span data-stu-id="144d9-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="144d9-104">在 Dynamics 365 Commerce 中，呼叫中心是一种可在应用程序中定义的渠道。</span><span class="sxs-lookup"><span data-stu-id="144d9-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="144d9-105">通过为呼叫中心实体定义特定渠道，可以让系统将特定数据默认值和订单处理默认值与呼叫中心渠道用户创建的销售订单绑定。</span><span class="sxs-lookup"><span data-stu-id="144d9-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="144d9-106">呼叫中心功能包括高级价格和促销、目录、礼品卡、会员计划，以及优惠券。</span><span class="sxs-lookup"><span data-stu-id="144d9-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="144d9-107">销售点 (POS) 应用程序也可以利用呼叫中心订单为跨渠道订单履行方案提供支持。</span><span class="sxs-lookup"><span data-stu-id="144d9-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="144d9-108">请务必注意，虽然呼叫中心模块可以在 Commerce 外部供其他行业利用，但是尚未针对在企业到企业 (B2B) 订单处理方案或订单有大量销售行的方案中的使用优化呼叫中心应用程序的当前版本。</span><span class="sxs-lookup"><span data-stu-id="144d9-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="144d9-109">建议除了直接面向消费者的典型交易记录处理之外，还希望利用呼叫中心功能处理订单的用户花费足够时间测试和验证启用呼叫中心功能是否可以满足功能需求和性能需求。</span><span class="sxs-lookup"><span data-stu-id="144d9-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="144d9-110">除了支持创建订单，呼叫中心模块还提供易用的客户服务应用程序，因此用户可以更轻松地找到客户帐户和查看所有相关客户订单和属性。</span><span class="sxs-lookup"><span data-stu-id="144d9-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="144d9-111">此客户服务屏幕旨在让用户快速访问与订单有关的数据，从而让他们可以回答从客户处收到且与订单有关的最常见问题。</span><span class="sxs-lookup"><span data-stu-id="144d9-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="144d9-112">此页提供指向与设置、配置和功能性使用呼叫中心功能有关的相关文档的链接。</span><span class="sxs-lookup"><span data-stu-id="144d9-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="144d9-113">配置呼叫中心</span><span class="sxs-lookup"><span data-stu-id="144d9-113">Configure the call center</span></span>

[<span data-ttu-id="144d9-114">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="144d9-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="144d9-115">配置订单处理</span><span class="sxs-lookup"><span data-stu-id="144d9-115">Configure order processing</span></span>

[<span data-ttu-id="144d9-116">设置和处理呼叫中心欺诈预警</span><span class="sxs-lookup"><span data-stu-id="144d9-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="144d9-117">配置和使用呼叫中心订单保留</span><span class="sxs-lookup"><span data-stu-id="144d9-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="144d9-118">配置付款处理</span><span class="sxs-lookup"><span data-stu-id="144d9-118">Configure payment processing</span></span>

[<span data-ttu-id="144d9-119">呼叫中心付款方式</span><span class="sxs-lookup"><span data-stu-id="144d9-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="144d9-120">配置交货方式</span><span class="sxs-lookup"><span data-stu-id="144d9-120">Configure delivery modes</span></span>

[<span data-ttu-id="144d9-121">配置呼叫中心交货方式和费用</span><span class="sxs-lookup"><span data-stu-id="144d9-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="144d9-122">配置直接营销</span><span class="sxs-lookup"><span data-stu-id="144d9-122">Configure direct marketing</span></span>

[<span data-ttu-id="144d9-123">呼叫中心目录</span><span class="sxs-lookup"><span data-stu-id="144d9-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="144d9-124">设置 Recency、频率和货币 (RFM) 分析</span><span class="sxs-lookup"><span data-stu-id="144d9-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="144d9-125">配置连续性计划</span><span class="sxs-lookup"><span data-stu-id="144d9-125">Configure continuity programs</span></span>

[<span data-ttu-id="144d9-126">设置呼叫中心的连续性计划</span><span class="sxs-lookup"><span data-stu-id="144d9-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
