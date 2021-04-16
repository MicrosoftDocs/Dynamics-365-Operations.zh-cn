---
title: 现金流预测设置故障排除
description: 本主题提供对配置现金流预测时可能有的问题的解答。 可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827306"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="ebcb1-104">现金流预测设置故障排除</span><span class="sxs-lookup"><span data-stu-id="ebcb1-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebcb1-105">本主题提供对配置现金流预测时可能有的问题的解答。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="ebcb1-106">可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="ebcb1-107">为什么只显示一个法人的现金流？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="ebcb1-108">现金流预测是按法人配置和计算的。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="ebcb1-109">Power BI 报表和 Finance insights 中的现金流预测功能显示结果。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="ebcb1-110">必须为您要查看其预测的每个法人设置现金流预测。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="ebcb1-111">查看所有法人中现金流预测的配置。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="ebcb1-112">或者，查看所有法人的现金流预测的配置，确保其已按照您的期望设置。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="ebcb1-113">为什么 Power BI 不显示所有现金流数据？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="ebcb1-114">必须先完成几个步骤，现金流预测才能显示在 Power BI 视图中。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="ebcb1-115">查看以下清单，确保每个步骤均已完成：</span><span class="sxs-lookup"><span data-stu-id="ebcb1-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="ebcb1-116">为每个法人设置现金流。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="ebcb1-117">在总帐参数中，设置系统货币和系统汇率类型。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="ebcb1-118">设置分类帐会计货币和汇率类型。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="ebcb1-119">输入交易货币和会计货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="ebcb1-120">输入会计货币和系统货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="ebcb1-121">输入会计货币和每个银行货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="ebcb1-122">为什么现金流 Power BI 在以前的版本中工作，但现在是空白的？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="ebcb1-123">验证实体商店中的“现金流度量 V2”和“LedgerCovLiquidityMeasurement”度量是否已配置。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="ebcb1-124">有关如何使用实体商店中的数据的详细信息，请参阅 [Power BI 与实体商店的集成](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="ebcb1-125">验证查看 Power BI 内容所需的所有步骤均已完成。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="ebcb1-126">有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="ebcb1-127">实体商店实体是否已刷新？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="ebcb1-128">您必须定期刷新您的实体，以确保数据是最新的，而且准确。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="ebcb1-129">要手动刷新特定实体，请转到 **系统管理 \> 设置 \> 实体商店**，选择实体，然后选择 **刷新**。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="ebcb1-130">数据也可以自动更新。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-130">The data can also be updated automatically.</span></span> <span data-ttu-id="ebcb1-131">在 **实体商店** 页上，将 **启用自动刷新** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="ebcb1-132">计算现金流量预测时应使用哪种计算方法？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="ebcb1-133">有两个重要的现金流量预测计算方法选项可供选择。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="ebcb1-134">**新** 选项将计算新单据和自上一批处理作业运行以来更改的单据的现金流量预测。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="ebcb1-135">此选项往往运行更快，因为它处理较小的单据子集。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="ebcb1-136">**总计** 选项将重新计算系统中每个单据的现金流量预测。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="ebcb1-137">此选项花费更多时间，因为它需要完成更多工作。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="ebcb1-138">如何提高现金流量预测定期批处理作业的性能？</span><span class="sxs-lookup"><span data-stu-id="ebcb1-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="ebcb1-139">我们建议您每天在非高峰时段使用 **新** 计算方法运行现金流量预测一次。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="ebcb1-140">我们建议每周六天使用此方法。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="ebcb1-141">然后，每周在活动量最少的一天使用 **总计** 计算方法运行现金流量预测一次。</span><span class="sxs-lookup"><span data-stu-id="ebcb1-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

