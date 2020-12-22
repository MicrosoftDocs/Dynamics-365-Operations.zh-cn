---
title: 收入确认概览
description: 本主题提供有关收入确认功能的信息。 此功能提供了灵活框架，供您定义特定于公司的多元素订单收入价格和收入计划确认规则。
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458562"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="335bd-104">收入确认概览</span><span class="sxs-lookup"><span data-stu-id="335bd-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="335bd-105">收入确认功能不能通过功能管理来启用。</span><span class="sxs-lookup"><span data-stu-id="335bd-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="335bd-106">目前，您必须使用 Configuration Key 启用该功能。</span><span class="sxs-lookup"><span data-stu-id="335bd-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="335bd-107">如果公司销售多种元素，例如产品、服务、订阅等，则必须能够分解多元素订单，以便根据一组特定于公司和行业的准则来确认收入。</span><span class="sxs-lookup"><span data-stu-id="335bd-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="335bd-108">一般来说，收入确认流程可用于执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="335bd-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="335bd-109">分配收入，以确保根据多元素订单上的组件价值来确认合理的收入价格。</span><span class="sxs-lookup"><span data-stu-id="335bd-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="335bd-110">基于体现合同时间范围以及该段时间内收入确认百分比的收入计划来延期收入。</span><span class="sxs-lookup"><span data-stu-id="335bd-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="335bd-111">[如何在 Dynamics 365 Finance 中使用收入确认](https://youtu.be/v3amIsiqvoo) 视频（如上所示）包括在 YouTube 上提供的 [Finance and Operations 播放列表](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) 中。</span><span class="sxs-lookup"><span data-stu-id="335bd-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="335bd-112">收入确认功能提供了灵活框架，供您定义特定于公司的收入价格和收入计划确认规则。</span><span class="sxs-lookup"><span data-stu-id="335bd-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="335bd-113">已发布产品用于支持销售订单文档的收入确认。</span><span class="sxs-lookup"><span data-stu-id="335bd-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="335bd-114">已发布产品包含确定收入价格和收入计划所需的设置。</span><span class="sxs-lookup"><span data-stu-id="335bd-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="335bd-115">销售订单可能源自时间和材料项目。</span><span class="sxs-lookup"><span data-stu-id="335bd-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="335bd-116">公司可在不使用收入价格功能的情况下使用收入计划功能。</span><span class="sxs-lookup"><span data-stu-id="335bd-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="335bd-117">因此，销售订单行上的价格将作为收入或延期收入。</span><span class="sxs-lookup"><span data-stu-id="335bd-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="335bd-118">如果销售订单行上存在收入计划，则销售订单行上的价格将递延。</span><span class="sxs-lookup"><span data-stu-id="335bd-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="335bd-119">如果销售订单行上存在收入计划，则销售订单行上的价格将在开票时过帐至收入帐户。</span><span class="sxs-lookup"><span data-stu-id="335bd-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="335bd-120">收入价格在确认销售订单或过帐发票后进行计算。</span><span class="sxs-lookup"><span data-stu-id="335bd-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="335bd-121">如需在发票过帐之前预览收入价格，则必须确认销售订单。</span><span class="sxs-lookup"><span data-stu-id="335bd-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="335bd-122">在确认销售订单后，如果任何销售订单行具有收入计划，则还将创建预期收入计划。</span><span class="sxs-lookup"><span data-stu-id="335bd-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="335bd-123">在为销售订单开票后，预期收入计划将被删除并被实际收入确认计划替代。</span><span class="sxs-lookup"><span data-stu-id="335bd-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="335bd-124">每个销售订单行均维护收入确认计划详细信息。</span><span class="sxs-lookup"><span data-stu-id="335bd-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="335bd-125">因此，在完成合同义务后，收入确认经理可以查看详细信息并将销售订单行发放到收入。</span><span class="sxs-lookup"><span data-stu-id="335bd-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="335bd-126">每个期间结束时，收入确认经理可以创建收入日记帐来发放任何在其指定的日期当日或之前截止的计划行。</span><span class="sxs-lookup"><span data-stu-id="335bd-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="335bd-127">此收入日记帐不会立即过帐。</span><span class="sxs-lookup"><span data-stu-id="335bd-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="335bd-128">因此，收入确认经理可验证从延期收入向实际收入发放的金额是否正确。</span><span class="sxs-lookup"><span data-stu-id="335bd-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="335bd-129">如果合同发生变化，现有销售订单或新销售订单中添加了新的销售订单行，则可以运行重新分配流程以更正销售订单的所有行中的收入价格。</span><span class="sxs-lookup"><span data-stu-id="335bd-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
