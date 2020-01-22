---
title: 监控预测准确性
description: 本主题介绍 Dynamics 365 Supply Chain Management 计算的预测准确性的类型，并说明如何可以查看准确性值。
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bc3673ba69a072d07b749ad41a1697d35abd48
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935529"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="89cd8-103">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="89cd8-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89cd8-104">本主题介绍 Microsoft Dynamics 365 Supply Chain Management 计算的预测准确性的类型，并说明如何可以查看准确性值。</span><span class="sxs-lookup"><span data-stu-id="89cd8-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="89cd8-105">Supply Chain Management 计算以下类型的预测准确性：</span><span class="sxs-lookup"><span data-stu-id="89cd8-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="89cd8-106">历史预测准确性，通过比较主计划使用的历史预测和历史需求。</span><span class="sxs-lookup"><span data-stu-id="89cd8-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="89cd8-107">若要查看历史预测准确性的值（绝对值和百分比值），请单击**需求预测详细信息**页的**显示准确性**。</span><span class="sxs-lookup"><span data-stu-id="89cd8-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="89cd8-108">用于生成预测的预测模型的估计精确性。</span><span class="sxs-lookup"><span data-stu-id="89cd8-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="89cd8-109">您可以在**需求预测详细信息**页的**模型详细信息 - MAPE** 下查看准确率百分比。</span><span class="sxs-lookup"><span data-stu-id="89cd8-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="89cd8-110">如果您使用需求预测 Microsoft Azure 机器学习，内部模型准确性的计算基于测试数据集。</span><span class="sxs-lookup"><span data-stu-id="89cd8-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="89cd8-111">若要指定测试数据集的规模，请在**需求预测参数**页上设置参数 **TEST\_SET\_SIZE\_PERCENT**。</span><span class="sxs-lookup"><span data-stu-id="89cd8-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="89cd8-112">例如，如果您将该值设置为 **20**，历史数据的最后 20% 将用于计算内部模型准确性。</span><span class="sxs-lookup"><span data-stu-id="89cd8-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="89cd8-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="89cd8-113">Additional resources</span></span>
--------

[<span data-ttu-id="89cd8-114">授权调整后的预测</span><span class="sxs-lookup"><span data-stu-id="89cd8-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="89cd8-115">在计算需求预测时，需从历史交易记录数据中删除离群值</span><span class="sxs-lookup"><span data-stu-id="89cd8-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



