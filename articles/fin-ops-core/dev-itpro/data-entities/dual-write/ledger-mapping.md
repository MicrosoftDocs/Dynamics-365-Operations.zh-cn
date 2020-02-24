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
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019659"
---
# <a name="integrated-ledger"></a><span data-ttu-id="fadf2-103">集成的分类账</span><span class="sxs-lookup"><span data-stu-id="fadf2-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="fadf2-104">在业务应用程序中，分类帐数据定义公司如何开展业务的核心设置。</span><span class="sxs-lookup"><span data-stu-id="fadf2-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="fadf2-105">例如，分类帐数据描述公司遵循的会计年度、交易所用的货币以及所使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="fadf2-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="fadf2-106">本主题介绍此核心财务数据的集成。</span><span class="sxs-lookup"><span data-stu-id="fadf2-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="fadf2-107">模板</span><span class="sxs-lookup"><span data-stu-id="fadf2-107">Templates</span></span>

<span data-ttu-id="fadf2-108">分类帐数据包括核心财务实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fadf2-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="fadf2-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="fadf2-109">Finance and Operations apps</span></span>      | <span data-ttu-id="fadf2-110">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="fadf2-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="fadf2-111">币种</span><span class="sxs-lookup"><span data-stu-id="fadf2-111">Currencies</span></span>                       | <span data-ttu-id="fadf2-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="fadf2-112">transactioncurrencies</span></span>
<span data-ttu-id="fadf2-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="fadf2-113">FiscalCalendar</span></span>                   | <span data-ttu-id="fadf2-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="fadf2-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="fadf2-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="fadf2-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="fadf2-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="fadf2-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="fadf2-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="fadf2-117">ExchRateType</span></span>                     | <span data-ttu-id="fadf2-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="fadf2-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="fadf2-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="fadf2-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="fadf2-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="fadf2-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="fadf2-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="fadf2-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="fadf2-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="fadf2-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="fadf2-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="fadf2-123">MainAccountCategory</span></span>              | <span data-ttu-id="fadf2-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="fadf2-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="fadf2-125">主科目</span><span class="sxs-lookup"><span data-stu-id="fadf2-125">MainAccount</span></span>                      | <span data-ttu-id="fadf2-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="fadf2-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="fadf2-127">分类帐</span><span class="sxs-lookup"><span data-stu-id="fadf2-127">Ledger</span></span>                           | <span data-ttu-id="fadf2-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="fadf2-128">msdyn\_ledgers</span></span>
<span data-ttu-id="fadf2-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="fadf2-129">ExchangeRates</span></span>                    | <span data-ttu-id="fadf2-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="fadf2-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="fadf2-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="fadf2-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="fadf2-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="fadf2-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="fadf2-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="fadf2-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="fadf2-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="fadf2-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="fadf2-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="fadf2-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="fadf2-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="fadf2-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="fadf2-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="fadf2-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="fadf2-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="fadf2-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




