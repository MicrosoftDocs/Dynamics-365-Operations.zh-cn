---
title: 交货计划
description: 当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193774"
---
# <a name="delivery-schedules"></a><span data-ttu-id="da64f-103">交货计划</span><span class="sxs-lookup"><span data-stu-id="da64f-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da64f-104">当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。</span><span class="sxs-lookup"><span data-stu-id="da64f-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="da64f-105">在请求在多个装运中交付订单或报价单上的数量时，使用交货计划。</span><span class="sxs-lookup"><span data-stu-id="da64f-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="da64f-106">单独的装运由交货行表示。</span><span class="sxs-lookup"><span data-stu-id="da64f-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="da64f-107">两个或多个交货行构成了一个交货计划。</span><span class="sxs-lookup"><span data-stu-id="da64f-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="da64f-108">交货行可以有不同的交货日期、数量、交货方式以及站点和仓库等存储维度。</span><span class="sxs-lookup"><span data-stu-id="da64f-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="da64f-109">**交货计划示例**</span><span class="sxs-lookup"><span data-stu-id="da64f-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="da64f-110">物料</span><span class="sxs-lookup"><span data-stu-id="da64f-110">Item</span></span>                              | <span data-ttu-id="da64f-111">值</span><span class="sxs-lookup"><span data-stu-id="da64f-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="da64f-112">总订单（原始订单行）</span><span class="sxs-lookup"><span data-stu-id="da64f-112">Total order (original order line)</span></span> | <span data-ttu-id="da64f-113">600 把椅子</span><span class="sxs-lookup"><span data-stu-id="da64f-113">600 chairs</span></span>                               |
| <span data-ttu-id="da64f-114">请求的交货计划</span><span class="sxs-lookup"><span data-stu-id="da64f-114">Requested delivery schedule</span></span>       | <span data-ttu-id="da64f-115">每月 100 把椅子</span><span class="sxs-lookup"><span data-stu-id="da64f-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="da64f-116">请求的交货时间范围</span><span class="sxs-lookup"><span data-stu-id="da64f-116">Requested time frame for delivery</span></span> | <span data-ttu-id="da64f-117">6 个月，在每个月的第一天</span><span class="sxs-lookup"><span data-stu-id="da64f-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="da64f-118">在这种情况下，该客户请求跨六个月的期间按批处理 100 把椅子的方式完成 600 把椅子的发货。</span><span class="sxs-lookup"><span data-stu-id="da64f-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="da64f-119">若要记录交货要求，您可创建一个交货计划。</span><span class="sxs-lookup"><span data-stu-id="da64f-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="da64f-120">在交货计划页上，创建六个单独的交货行。</span><span class="sxs-lookup"><span data-stu-id="da64f-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="da64f-121">每个交货行包含 100 把椅子，并指示这 100 把椅子的交货日期。</span><span class="sxs-lookup"><span data-stu-id="da64f-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="da64f-122">在这种情况下，在连续六个月的每月第一天抵消每一行。</span><span class="sxs-lookup"><span data-stu-id="da64f-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="da64f-123">在您创建一个交货计划时，原始订单行的类型将自动更改为 **包含多个交货的订单行**。</span><span class="sxs-lookup"><span data-stu-id="da64f-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="da64f-124">此类型的行称作业务行，并用图标标记。</span><span class="sxs-lookup"><span data-stu-id="da64f-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="da64f-125">交货行由不同图标标记。</span><span class="sxs-lookup"><span data-stu-id="da64f-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="da64f-126">如果更改交货行的数量，业务行将更新为交货计划的总数量。</span><span class="sxs-lookup"><span data-stu-id="da64f-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="da64f-127">如果贸易协议为订单定义了总折扣，则交货计划可确保您的订单符合总订单折扣条件，即便订单拆分为单独的交货也是如此。</span><span class="sxs-lookup"><span data-stu-id="da64f-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="da64f-128">具有交货的计划订单是比对交货行处理的。</span><span class="sxs-lookup"><span data-stu-id="da64f-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="da64f-129">处理包括过帐装箱单、产品收据和开票。</span><span class="sxs-lookup"><span data-stu-id="da64f-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="da64f-130">具有交货计划的订单和报价单的单据打印输出只显示交货行。</span><span class="sxs-lookup"><span data-stu-id="da64f-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="da64f-131">它们不显示原始行（业务行）。</span><span class="sxs-lookup"><span data-stu-id="da64f-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="da64f-132">**注意：** 此外，当您执行这些操作时，只显示交货行：</span><span class="sxs-lookup"><span data-stu-id="da64f-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="da64f-133">发布</span><span class="sxs-lookup"><span data-stu-id="da64f-133">Post</span></span>
-   <span data-ttu-id="da64f-134">复制页</span><span class="sxs-lookup"><span data-stu-id="da64f-134">Copy pages</span></span>
-   <span data-ttu-id="da64f-135">浏览列表页和报表</span><span class="sxs-lookup"><span data-stu-id="da64f-135">Browse list pages and reports</span></span>

<span data-ttu-id="da64f-136">当您确认销售报价单时，生成的销售订单显示整个交货计划，甚至是具有多个交货的订单行。</span><span class="sxs-lookup"><span data-stu-id="da64f-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="da64f-137">此外，整个交货计划都显示在所有主要页面上，如销售订单、销售报价单和采购订单。</span><span class="sxs-lookup"><span data-stu-id="da64f-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]