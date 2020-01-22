---
title: 集成的分类帐
description: 本主题介绍使用 Common Data Service 在 Finance and Operations 与其他 Dynamics 365 应用程序之间的分类帐数据的集成。
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853874"
---
# <a name="integrated-ledger"></a><span data-ttu-id="35eb7-103">集成的分类帐</span><span class="sxs-lookup"><span data-stu-id="35eb7-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35eb7-104">在业务应用程序中，分类帐数据定义公司如何开展业务的核心设置。</span><span class="sxs-lookup"><span data-stu-id="35eb7-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="35eb7-105">例如，分类帐数据描述公司遵循的会计年度、交易所用的货币以及所使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="35eb7-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="35eb7-106">本主题介绍此核心财务数据的集成。</span><span class="sxs-lookup"><span data-stu-id="35eb7-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="35eb7-107">模板</span><span class="sxs-lookup"><span data-stu-id="35eb7-107">Templates</span></span>

<span data-ttu-id="35eb7-108">分类帐数据包括核心财务实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="35eb7-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="35eb7-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="35eb7-109">Finance and Operations apps</span></span>      | <span data-ttu-id="35eb7-110">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="35eb7-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="35eb7-111">币种</span><span class="sxs-lookup"><span data-stu-id="35eb7-111">Currencies</span></span>                       | <span data-ttu-id="35eb7-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="35eb7-112">transactioncurrencies</span></span>
<span data-ttu-id="35eb7-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="35eb7-113">FiscalCalendar</span></span>                   | <span data-ttu-id="35eb7-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="35eb7-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="35eb7-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="35eb7-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="35eb7-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="35eb7-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="35eb7-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="35eb7-117">ExchRateType</span></span>                     | <span data-ttu-id="35eb7-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="35eb7-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="35eb7-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="35eb7-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="35eb7-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="35eb7-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="35eb7-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="35eb7-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="35eb7-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="35eb7-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="35eb7-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="35eb7-123">MainAccountCategory</span></span>              | <span data-ttu-id="35eb7-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="35eb7-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="35eb7-125">主科目</span><span class="sxs-lookup"><span data-stu-id="35eb7-125">MainAccount</span></span>                      | <span data-ttu-id="35eb7-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="35eb7-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="35eb7-127">分类帐</span><span class="sxs-lookup"><span data-stu-id="35eb7-127">Ledger</span></span>                           | <span data-ttu-id="35eb7-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="35eb7-128">msdyn\_ledgers</span></span>
<span data-ttu-id="35eb7-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="35eb7-129">ExchangeRates</span></span>                    | <span data-ttu-id="35eb7-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="35eb7-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="35eb7-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="35eb7-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="35eb7-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="35eb7-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="35eb7-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="35eb7-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="35eb7-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="35eb7-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="35eb7-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="35eb7-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="35eb7-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="35eb7-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="35eb7-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="35eb7-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="35eb7-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="35eb7-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




