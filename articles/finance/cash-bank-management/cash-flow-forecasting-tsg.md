---
title: 现金流预测设置故障排除
description: 本主题提供对配置现金流预测时可能有的问题的解答。 可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232481"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="1ea00-104">现金流预测设置故障排除</span><span class="sxs-lookup"><span data-stu-id="1ea00-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ea00-105">本主题提供对配置现金流预测时可能有的问题的解答。</span><span class="sxs-lookup"><span data-stu-id="1ea00-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="1ea00-106">可以解决有关现金流设置、现金流更新和现金流 Power BI 的常见问题 (FAQ)。</span><span class="sxs-lookup"><span data-stu-id="1ea00-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="1ea00-107">为什么只显示一个法人的现金流？</span><span class="sxs-lookup"><span data-stu-id="1ea00-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="1ea00-108">现金流预测是按法人配置和计算的。</span><span class="sxs-lookup"><span data-stu-id="1ea00-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="1ea00-109">Power BI 报表和 Finance insights 中的现金流预测功能显示结果。</span><span class="sxs-lookup"><span data-stu-id="1ea00-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="1ea00-110">必须为您要查看其预测的每个法人设置现金流预测。</span><span class="sxs-lookup"><span data-stu-id="1ea00-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="1ea00-111">查看所有法人中现金流预测的配置。</span><span class="sxs-lookup"><span data-stu-id="1ea00-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="1ea00-112">或者，查看所有法人的现金流预测的配置，确保其已按照您的期望设置。</span><span class="sxs-lookup"><span data-stu-id="1ea00-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="1ea00-113">为什么 Power BI 不显示所有现金流数据？</span><span class="sxs-lookup"><span data-stu-id="1ea00-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="1ea00-114">必须先完成几个步骤，现金流预测才能显示在 Power BI 视图中。</span><span class="sxs-lookup"><span data-stu-id="1ea00-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="1ea00-115">查看以下清单，确保每个步骤均已完成：</span><span class="sxs-lookup"><span data-stu-id="1ea00-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="1ea00-116">为每个法人设置现金流。</span><span class="sxs-lookup"><span data-stu-id="1ea00-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="1ea00-117">在总帐参数中，设置系统货币和系统汇率类型。</span><span class="sxs-lookup"><span data-stu-id="1ea00-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="1ea00-118">设置分类帐会计货币和汇率类型。</span><span class="sxs-lookup"><span data-stu-id="1ea00-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="1ea00-119">输入交易货币和会计货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="1ea00-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="1ea00-120">输入会计货币和系统货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="1ea00-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="1ea00-121">输入会计货币和每个银行货币之间的汇率。</span><span class="sxs-lookup"><span data-stu-id="1ea00-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="1ea00-122">为什么现金流 Power BI 在以前的版本中工作，但现在是空白的？</span><span class="sxs-lookup"><span data-stu-id="1ea00-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="1ea00-123">验证实体商店中的“现金流度量 V2”和“LedgerCovLiquidityMeasurement”度量是否已配置。</span><span class="sxs-lookup"><span data-stu-id="1ea00-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="1ea00-124">有关如何使用实体商店中的数据的详细信息，请参阅 [Power BI 与实体商店的集成](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)验证查看 Power BI 内容所需的所有步骤均已完成。</span><span class="sxs-lookup"><span data-stu-id="1ea00-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="1ea00-125">有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea00-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="1ea00-126">实体商店实体是否已刷新？</span><span class="sxs-lookup"><span data-stu-id="1ea00-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="1ea00-127">您必须定期刷新您的实体，以确保数据是最新的，而且准确。</span><span class="sxs-lookup"><span data-stu-id="1ea00-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="1ea00-128">要手动刷新特定实体，请转到 **系统管理 \> 设置 \> 实体商店**，选择实体，然后选择 **刷新**。</span><span class="sxs-lookup"><span data-stu-id="1ea00-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="1ea00-129">数据也可以自动更新。</span><span class="sxs-lookup"><span data-stu-id="1ea00-129">The data can also be updated automatically.</span></span> <span data-ttu-id="1ea00-130">在 **实体商店** 页上，将 **启用自动刷新** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="1ea00-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]