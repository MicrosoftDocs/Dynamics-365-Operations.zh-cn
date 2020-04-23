---
title: 预订工作流概览
description: 此主题概要介绍预订工作流。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cb8b86ef0e2a1bd90590c8cc2a20e18e82ef9c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206580"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="68df5-103">预订工作流概览</span><span class="sxs-lookup"><span data-stu-id="68df5-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="68df5-104">您是一家提供照明设备维护预定的灯具公司的预订管理员。</span><span class="sxs-lookup"><span data-stu-id="68df5-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="68df5-105">一个客户联系您公司购买一年的照明设备维护预订。</span><span class="sxs-lookup"><span data-stu-id="68df5-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="68df5-106">设置预订</span><span class="sxs-lookup"><span data-stu-id="68df5-106">Setting up subscriptions</span></span>

<span data-ttu-id="68df5-107">若要设置预订，您必须首先为新的服务协议创建一个预订组，或者确认某一预订组存在。</span><span class="sxs-lookup"><span data-stu-id="68df5-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="68df5-108">如果存在某一预订组，则必须将它设置为每年对该客户开票，并且计入当年每个月的销售收入。</span><span class="sxs-lookup"><span data-stu-id="68df5-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="68df5-109">有关如何设置预订的详细信息，请参阅[设置预订组](set-up-subscription-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="68df5-110">在创建该预订组后，您可以创建预订。</span><span class="sxs-lookup"><span data-stu-id="68df5-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="68df5-111">有关如何创建服务预订的详细信息，请参阅[从预订组创建服务预订](create-service-subscriptions-from-subscription-group.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="68df5-112">创建和修改预订交易记录</span><span class="sxs-lookup"><span data-stu-id="68df5-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="68df5-113">在设置预定后，您为第一个开票期间（即一年）创建预订费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="68df5-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="68df5-114">交易记录的类型为**常规**。</span><span class="sxs-lookup"><span data-stu-id="68df5-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="68df5-115">因此，只能创建开始日期和结束日期对应于以前在**期间类型**窗体中创建的期间的预订交易记录。</span><span class="sxs-lookup"><span data-stu-id="68df5-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="68df5-116">有关费用交易记录的详细信息，请参阅[创建预订费用交易记录](create-subscription-fee-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="68df5-117">在您为客户设置预订后，记住对于您提供的服务的所有标价，双方已协商了 10% 的折扣。</span><span class="sxs-lookup"><span data-stu-id="68df5-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="68df5-118">因此，您必须降低已创建的交易记录费用的价格。</span><span class="sxs-lookup"><span data-stu-id="68df5-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="68df5-119">在当天的晚些时候，您客户的联系人给您打电话，指出尽管他们仍需要针对照明设备的服务协议，但它们计划在当年的下半年引入新的照明设备。</span><span class="sxs-lookup"><span data-stu-id="68df5-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="68df5-120">因此，他们只需截止到 2013 年 10 月的维护覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="68df5-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="68df5-121">为了减少针对客户的预订的月份数，您创建类型为**缩减天数**的新的预订费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="68df5-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="68df5-122">有关如何缩减天数的详细信息，请参阅[缩减预订费用天数](reduce-the-days-on-subscription-fees.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="68df5-123">开票和计入预订交易记录</span><span class="sxs-lookup"><span data-stu-id="68df5-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="68df5-124">您现在已完成了预订设置，并且可以针对预订为您的客户开票了。</span><span class="sxs-lookup"><span data-stu-id="68df5-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="68df5-125">有关如何为预订开票的详细信息，请参阅[为预订交易记录开票](invoice-subscription-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="68df5-126">两天后，您的客户打电话指出，该预订应按美元开票，而非按欧元开票。</span><span class="sxs-lookup"><span data-stu-id="68df5-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="68df5-127">因此，您创建一个贷方通知单，并且还按正确的币种创建一个新的预订交易记录。</span><span class="sxs-lookup"><span data-stu-id="68df5-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="68df5-128">有关如何贷记预订交易记录的详细信息，请参阅[贷记预订交易记录](credit-subscription-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="68df5-129">在每个月的月末，可将来自客户的预订的当月收入计入损益科目和 WIP 科目。</span><span class="sxs-lookup"><span data-stu-id="68df5-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="68df5-130">有关如何应计预订的收入的详细信息，请参阅[应计预订收入](accrue-subscription-revenue.md)。</span><span class="sxs-lookup"><span data-stu-id="68df5-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


