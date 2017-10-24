---
title: "授权调整后的预测"
description: "不必立即授权所有预测数据。 本文介绍如何指定为预测授权的期间。 还说明如何可以授权特定公司和预测模型的预测。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399a7a21ec71fe50e280ccb24699cda76d571990
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="5accf-105">授权调整后的预测</span><span class="sxs-lookup"><span data-stu-id="5accf-105">Authorize an adjusted forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5accf-106">不必立即授权所有预测数据。</span><span class="sxs-lookup"><span data-stu-id="5accf-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="5accf-107">本文介绍如何指定为预测授权的期间。</span><span class="sxs-lookup"><span data-stu-id="5accf-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="5accf-108">还说明如何可以授权特定公司和预测模型的预测。</span><span class="sxs-lookup"><span data-stu-id="5accf-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="5accf-109">不必立即授权所有预测数据。</span><span class="sxs-lookup"><span data-stu-id="5accf-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="5accf-110">您可以指定预测授权期间的开始和结束日期。</span><span class="sxs-lookup"><span data-stu-id="5accf-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="5accf-111">此功能可以锁定特定时段。</span><span class="sxs-lookup"><span data-stu-id="5accf-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="5accf-112">您指定的开始日期和结束日期必须对应预测生成的时段的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="5accf-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="5accf-113">如果需要调整，此系统强制执行此限制和自动调整日期。</span><span class="sxs-lookup"><span data-stu-id="5accf-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="5accf-114">在**授权**页的**详细信息**选项卡上，您可以查看最近生成的预测的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5accf-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="5accf-115">您可以选择公司和预测模型以授权要使用的预测。</span><span class="sxs-lookup"><span data-stu-id="5accf-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="5accf-116">默认情况下，网格包括为其创建预测需求的所有公司。</span><span class="sxs-lookup"><span data-stu-id="5accf-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="5accf-117">对于每个公司，对应于在主计划参数中设置的当前预测计划的预测模型将被预填写。</span><span class="sxs-lookup"><span data-stu-id="5accf-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="5accf-118">不过，您可以将此预测模型更改为属于该公司的任何预测模型。</span><span class="sxs-lookup"><span data-stu-id="5accf-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="5accf-119">如果预测需求数据没有为一个所选公司生成，将在导入时收到警告消息。</span><span class="sxs-lookup"><span data-stu-id="5accf-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="5accf-120">您知道复选框**保存对基准需求预测进行的手动调整**如何工作非常重要。</span><span class="sxs-lookup"><span data-stu-id="5accf-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="5accf-121">如果您已手动调整统计基准预测，则授权使用调整的值，即使清除此复选框也是如此。</span><span class="sxs-lookup"><span data-stu-id="5accf-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="5accf-122">但是，在此授权之后将放弃更改。</span><span class="sxs-lookup"><span data-stu-id="5accf-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="5accf-123">因此，下次预测生成时，该预测只是统计预测，不具有任何手动覆盖，即使选择了**转移对需求预测进行的手动调整**。</span><span class="sxs-lookup"><span data-stu-id="5accf-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="5accf-124">因此，您可以视**保存对基准需求预测进行的手动调整**复选框为可以保留或放弃所有手动更改的机制。</span><span class="sxs-lookup"><span data-stu-id="5accf-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="see-also"></a><span data-ttu-id="5accf-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="5accf-125">See also</span></span>
--------

[<span data-ttu-id="5accf-126">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="5accf-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="5accf-127">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="5accf-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



