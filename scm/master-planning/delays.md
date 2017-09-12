---
title: "延迟"
description: "本文提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="delays"></a><span data-ttu-id="4ef3e-104">延迟</span><span class="sxs-lookup"><span data-stu-id="4ef3e-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4ef3e-105">本文提供有关主计划中的延期日期的信息。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="4ef3e-106">如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="4ef3e-107">主计划可以基于提前期、物料可用性、产能可用性以及各种计划参数计算交易记录的最早履行日期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="4ef3e-108">如果主计划计算早于当前日期的一个订单日期，订单不能准时履行。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="4ef3e-109">因此，订单延期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="4ef3e-110">在这种情况下，主计划从当前日期正推计划订单并包括提前期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="4ef3e-111">这些提前期从任何更低级别构成物料开始。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="4ef3e-112">该订单然后将收到一个延期的日期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-112">The order then receives a delayed date.</span></span> <span data-ttu-id="4ef3e-113">延期日期是基于当前数据的实际到期日期。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="4ef3e-114">主计划还计算延迟的天数。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="4ef3e-115">在某些情况下，您可以选择不计算延迟，例如，当用户了解他们可以通过选择备选交货模式加速提前期时。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="4ef3e-116">您可以配置如何为覆盖范围组计算延迟。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="4ef3e-117">然后您可以在以后将覆盖范围组附加到物料上。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="4ef3e-118">在**主计划参数**页上，您可以设置延迟计算的开始时间。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="4ef3e-119">如果在此时间后履行某一订单，则在该订单的延迟日期上加上一天的延迟。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="4ef3e-120">**注意：**在较早版本中，计算的延迟称为*先期备货消息*，延迟的日期称为*将来日期*，延期的交易记录称作*为将来设置的交易记录*。</span><span class="sxs-lookup"><span data-stu-id="4ef3e-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="4ef3e-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ef3e-121">See also</span></span>
--------

[<span data-ttu-id="4ef3e-122">覆盖范围设置</span><span class="sxs-lookup"><span data-stu-id="4ef3e-122">Coverage settings</span></span>](coverage-settings.md)




