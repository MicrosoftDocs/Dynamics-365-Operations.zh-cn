---
title: 延迟
description: 本主题提供有关主计划中的延期日期的信息。 如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34252e5cd9ee5151b1cba47975fc0cc612521a17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203840"
---
# <a name="delays"></a><span data-ttu-id="35a3a-104">延迟</span><span class="sxs-lookup"><span data-stu-id="35a3a-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35a3a-105">本主题提供有关主计划中的延期日期的信息。</span><span class="sxs-lookup"><span data-stu-id="35a3a-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="35a3a-106">如果主计划计算的最早履行日期在请求日期之后，延期日期是交易记录收到的实际到期日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="35a3a-107">主计划可以基于提前期、物料可用性、产能可用性以及各种计划参数计算交易记录的最早履行日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="35a3a-108">如果主计划计算早于当前日期的一个订单日期，订单不能准时履行。</span><span class="sxs-lookup"><span data-stu-id="35a3a-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="35a3a-109">因此，订单延期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="35a3a-110">在这种情况下，主计划从当前日期正推计划订单并包括提前期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="35a3a-111">这些提前期从任何更低级别构成物料开始。</span><span class="sxs-lookup"><span data-stu-id="35a3a-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="35a3a-112">该订单然后将收到一个延期的日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-112">The order then receives a delayed date.</span></span> <span data-ttu-id="35a3a-113">延期日期是基于当前数据的实际到期日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="35a3a-114">主计划还计算延迟的天数。</span><span class="sxs-lookup"><span data-stu-id="35a3a-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="35a3a-115">在某些情况下，您可以选择不计算延迟，例如，当用户了解他们可以通过选择备选交货模式加速提前期时。</span><span class="sxs-lookup"><span data-stu-id="35a3a-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="35a3a-116">您可以配置如何为覆盖范围组计算延迟。</span><span class="sxs-lookup"><span data-stu-id="35a3a-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="35a3a-117">然后您可以在以后将覆盖范围组附加到物料上。</span><span class="sxs-lookup"><span data-stu-id="35a3a-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="35a3a-118">在**主计划参数**页上，您可以设置延迟计算的开始时间。</span><span class="sxs-lookup"><span data-stu-id="35a3a-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="35a3a-119">如果在此时间后履行某一订单，则在该订单的延迟日期上加上一天的延迟。</span><span class="sxs-lookup"><span data-stu-id="35a3a-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="35a3a-120">在较早版本中，计算的延迟称为*先期备货消息*，延迟的日期称为*将来日期*，延期的交易记录称作为*将来设置的交易记录*。</span><span class="sxs-lookup"><span data-stu-id="35a3a-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="35a3a-121">具有多个 BOM 级别的生产设置中的有限延迟</span><span class="sxs-lookup"><span data-stu-id="35a3a-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="35a3a-122">在具有多个 BOM 级别的生产设置中处理延迟时，务必注意，主计划运行期间将仅使用延迟仅更新（在 BOM 结构中）项目正上方的项目。</span><span class="sxs-lookup"><span data-stu-id="35a3a-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="35a3a-123">首次运行主计划时，当批准或确定顶级计划订单时，将不为 BOM 结构中的其他项目应用延迟。</span><span class="sxs-lookup"><span data-stu-id="35a3a-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="35a3a-124">为了解决这项已知限制，可以在下次运行主计划之前批准（或确认）具有延迟的 BOM 结构最上层的生产订单。</span><span class="sxs-lookup"><span data-stu-id="35a3a-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="35a3a-125">这样，将保留延迟的已批准计划生产订单的延迟，并且相应更新所有基础组件。</span><span class="sxs-lookup"><span data-stu-id="35a3a-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="35a3a-126">也可以使用操作消息识别可以因为 BOM 结构中的其他延迟而移到以后的计划订单。</span><span class="sxs-lookup"><span data-stu-id="35a3a-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="35a3a-127">所需的日期</span><span class="sxs-lookup"><span data-stu-id="35a3a-127">Desired date</span></span>

<span data-ttu-id="35a3a-128">**计划订单**页面的**延期**选项卡下是计划订单的**所需的日期**。</span><span class="sxs-lookup"><span data-stu-id="35a3a-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="35a3a-129">计划订单的所需日期是延期的基准日期，这是等于从**净需求**计算出的**请求日期**的计算出的日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="35a3a-130">如果计划订单为 BOM 行、生产行或看板行，所需日期将基于**需求日期**，而**计划订单**页面中将不显示所需日期。</span><span class="sxs-lookup"><span data-stu-id="35a3a-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="35a3a-131">其他资源</span><span class="sxs-lookup"><span data-stu-id="35a3a-131">Additional resources</span></span>
--------

[<span data-ttu-id="35a3a-132">覆盖范围设置</span><span class="sxs-lookup"><span data-stu-id="35a3a-132">Coverage settings</span></span>](coverage-settings.md)
