---
title: "在计算需求预测时，需从历史交易记录数据中删除离群值"
description: "本文描述如何从用于计算需求预测的历史数据中排除外离群值。 通过排除离群值，您可以提高预测准确性。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ce8ebaf32b30c57b307f0d8799660ba6b42365a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="0e1f4-104">在计算需求预测时，需从历史交易记录数据中删除离群值</span><span class="sxs-lookup"><span data-stu-id="0e1f4-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e1f4-105">本文描述如何从用于计算需求预测的历史数据中排除外离群值。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="0e1f4-106">通过排除离群值，您可以提高预测准确性。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="0e1f4-107">可以排除离群值以提高预测的精确度。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="0e1f4-108">这是可选任务。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-108">This is an optional task.</span></span> <span data-ttu-id="0e1f4-109">下面是流程的概述：</span><span class="sxs-lookup"><span data-stu-id="0e1f4-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="0e1f4-110">单击**主计划** &gt; **设置** &gt; **需求预测** &gt; **离群值删除**以打开**离群值删除**页，从中可以使用查询选择要排除的交易记录。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="0e1f4-111">选择查询申请的公司，然后输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="0e1f4-112">**查询日期**字段自动设置为当前日期。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="0e1f4-113">选中**有效**复选框可以从历史数据中排除由查询找到的交易记录。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="0e1f4-114">在您创建基准预测时，此设置将生效。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="0e1f4-115">在**离群值删除查询**页上，当计算基准预测时，您可以删除、添加和选择定义将被排除的交易记录的标准。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="0e1f4-116">例如，选择要排除的特定物料或订单交易记录。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="0e1f4-117">单击**显示交易记录**。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-117">Click **Display transactions**.</span></span> <span data-ttu-id="0e1f4-118">**离群值交易记录**页列出了满足查询中所定义标准的交易记录，并且在计算需求预测时，将从历史数据中排除此交易记录。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="0e1f4-119">**注释：** 您还可以创建基于现有查询的查询。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="0e1f4-120">选择要复制的查询，然后单击**复制**。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="0e1f4-121">**查询日期**字段标识版本。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="0e1f4-122">您可以按原样使用查询，也可以单击**编辑查询**修改条件。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="0e1f4-123">（可选）您可以修改新查询的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="0e1f4-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0e1f4-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="0e1f4-124">Additional resources</span></span>
--------

[<span data-ttu-id="0e1f4-125">需求预测简介</span><span class="sxs-lookup"><span data-stu-id="0e1f4-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="0e1f4-126">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="0e1f4-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




