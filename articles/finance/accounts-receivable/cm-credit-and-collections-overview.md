---
title: 信用和收款概览
description: 此主题概要介绍信用和收款的功能。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6bba210bc282e031606acca4ad73e18d8b42167d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257625"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="f5ea5-103">信用和收款概览</span><span class="sxs-lookup"><span data-stu-id="f5ea5-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5ea5-104">您可以管理客户的信用额度，并在必要时执行收款活动。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="f5ea5-105">信用管理</span><span class="sxs-lookup"><span data-stu-id="f5ea5-105">Credit management</span></span>

<span data-ttu-id="f5ea5-106">客户信用管理使您可以根据创建的信用规则通过过帐流程管理信用限额和控制销售订单流程。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="f5ea5-107">信用管理流程可以包括以下任何步骤：</span><span class="sxs-lookup"><span data-stu-id="f5ea5-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="f5ea5-108">更新客户的信用属性，以提供有关其信用价值的其他信息。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="f5ea5-109">使用信用额度调整为客户创建信用额度。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="f5ea5-110">使用信用额度调整为客户创建临时信用额度。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="f5ea5-111">这样，您可以根据业务需求临时增加或减少客户信用额度。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="f5ea5-112">添加可能影响信用额度的信息，例如有关保险和担保的信息。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="f5ea5-113">创建将客户联系在一起的客户信用组，以便他们共享一个信用额度。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="f5ea5-114">为客户分配风险评分，然后使用评分通过信用额度调整为这些客户自动生成信用额度。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="f5ea5-115">根据风险、付款条件、信用额度、逾期金额和已用信用额度的百分比等因素，创建阻止规则，以在一个或多个过帐流程中暂停订单。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="f5ea5-116">管理暂停的销售订单列表，查看暂停的原因并缓解问题。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="f5ea5-117">下达销售订单，以便它们继续完成过帐流程。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="f5ea5-118">设置工作流来管理对信用额度更改和销售订单下达的批准。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="f5ea5-119">收款管理</span><span class="sxs-lookup"><span data-stu-id="f5ea5-119">Collections management</span></span>

<span data-ttu-id="f5ea5-120">**收款** 页会提供集中式视图，可在其中管理应收帐款收集信息。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="f5ea5-121">收款经理可以使用该集中式视图来管理收款。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="f5ea5-122">收款代理可以从使用预定义收款条件生成的客户列表或从 **客户** 页开始收款流程。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="f5ea5-123">在开始设置或使用收款前，应了解以下概念：</span><span class="sxs-lookup"><span data-stu-id="f5ea5-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="f5ea5-124">客户帐龄快照包含特定时间点的帐龄余额信息。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="f5ea5-125">收款客户池帮助您组织您的工作。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="f5ea5-126">收款代理可以有自己的客户池。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="f5ea5-127">列表页组织收款客户、活动和案例。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="f5ea5-128">客户的所有收款信息均在一个页面上，且您可以从该页面执行行动。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="f5ea5-129">可以在一个步骤中停征、复征或冲销利息和费用。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="f5ea5-130">可以在一个步骤中创建勾销交易记录。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="f5ea5-131">可以在一个步骤中处理资金不足 (NSF) 付款。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="f5ea5-132">有关这些概念的说明，请参见[收款管理关键概念](./cm-collections-concepts.md)。</span><span class="sxs-lookup"><span data-stu-id="f5ea5-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5ea5-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="f5ea5-133">Additional resources</span></span>

[<span data-ttu-id="f5ea5-134">客户信用管理参数设置</span><span class="sxs-lookup"><span data-stu-id="f5ea5-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="f5ea5-135">客户信用管理设置信息</span><span class="sxs-lookup"><span data-stu-id="f5ea5-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="f5ea5-136">为客户添加信用管理信息</span><span class="sxs-lookup"><span data-stu-id="f5ea5-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="f5ea5-137">客户信用组</span><span class="sxs-lookup"><span data-stu-id="f5ea5-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="f5ea5-138">客户信用额度调整</span><span class="sxs-lookup"><span data-stu-id="f5ea5-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="f5ea5-139">销售订单的信用保留</span><span class="sxs-lookup"><span data-stu-id="f5ea5-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="f5ea5-140">客户信用管理定期任务</span><span class="sxs-lookup"><span data-stu-id="f5ea5-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]