---
title: 交货计划
description: 当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068a881a7fa9b19198bd3ad22988465be49c1fa3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555808"
---
# <a name="delivery-schedules"></a><span data-ttu-id="5e5e1-103">交货计划</span><span class="sxs-lookup"><span data-stu-id="5e5e1-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e5e1-104">当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="5e5e1-105">在请求在多个装运中交付订单或报价单上的数量时，使用交货计划。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="5e5e1-106">单独的装运由交货行表示。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="5e5e1-107">两个或多个交货行构成了一个交货计划。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="5e5e1-108">交货行可以有不同的交货日期、数量、交货方式以及站点和仓库等存储维度。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="5e5e1-109">**交货计划示例**</span><span class="sxs-lookup"><span data-stu-id="5e5e1-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="5e5e1-110">总订单（原始订单行）</span><span class="sxs-lookup"><span data-stu-id="5e5e1-110">Total order (original order line)</span></span> | <span data-ttu-id="5e5e1-111">600 把椅子</span><span class="sxs-lookup"><span data-stu-id="5e5e1-111">600 chairs</span></span>                               |
| <span data-ttu-id="5e5e1-112">请求的交货计划</span><span class="sxs-lookup"><span data-stu-id="5e5e1-112">Requested delivery schedule</span></span>       | <span data-ttu-id="5e5e1-113">每月 100 把椅子</span><span class="sxs-lookup"><span data-stu-id="5e5e1-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="5e5e1-114">请求的交货时间范围</span><span class="sxs-lookup"><span data-stu-id="5e5e1-114">Requested time frame for delivery</span></span> | <span data-ttu-id="5e5e1-115">6 个月，在每个月的第一天</span><span class="sxs-lookup"><span data-stu-id="5e5e1-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="5e5e1-116">在这种情况下，该客户请求跨六个月的期间按批处理 100 把椅子的方式完成 600 把椅子的发货。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="5e5e1-117">若要记录交货要求，您可创建一个交货计划。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="5e5e1-118">在交货计划页上，创建六个单独的交货行。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="5e5e1-119">每个交货行包含 100 把椅子，并指示这 100 把椅子的交货日期。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="5e5e1-120">在这种情况下，在连续六个月的每月第一天抵消每一行。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="5e5e1-121">在您创建一个交货计划时，原始订单行的类型将自动更改为**包含多个交货的订单行**。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="5e5e1-122">此类型的行称作业务行，并用图标标记。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="5e5e1-123">交货行由不同图标标记。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="5e5e1-124">如果更改交货行的数量，业务行将更新为交货计划的总数量。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="5e5e1-125">如果贸易协议为订单定义了总折扣，则交货计划可确保您的订单符合总订单折扣条件，即便订单拆分为单独的交货也是如此。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="5e5e1-126">具有交货的计划订单是比对交货行处理的。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="5e5e1-127">处理包括过帐装箱单、产品收据和开票。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="5e5e1-128">具有交货计划的订单和报价单的单据打印输出只显示交货行。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="5e5e1-129">它们不显示原始行（业务行）。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="5e5e1-130">**注意：** 此外，当您执行这些操作时，只显示交货行：</span><span class="sxs-lookup"><span data-stu-id="5e5e1-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="5e5e1-131">发布</span><span class="sxs-lookup"><span data-stu-id="5e5e1-131">Post</span></span>
-   <span data-ttu-id="5e5e1-132">复制页</span><span class="sxs-lookup"><span data-stu-id="5e5e1-132">Copy pages</span></span>
-   <span data-ttu-id="5e5e1-133">浏览列表页和报表</span><span class="sxs-lookup"><span data-stu-id="5e5e1-133">Browse list pages and reports</span></span>

<span data-ttu-id="5e5e1-134">当您确认销售报价单时，生成的销售订单显示整个交货计划，甚至是具有多个交货的订单行。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="5e5e1-135">此外，整个交货计划都显示在所有主要页面上，如销售订单、销售报价单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="5e5e1-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>



