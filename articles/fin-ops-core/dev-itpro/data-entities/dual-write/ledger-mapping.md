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
ms.openlocfilehash: d9bcec1d4bb0207a2c3e0d46f7661b666fea3736
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112206"
---
# <a name="integrated-ledger"></a><span data-ttu-id="34617-103">集成的分类账</span><span class="sxs-lookup"><span data-stu-id="34617-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="34617-104">在业务应用程序中，分类帐数据定义公司如何开展业务的核心设置。</span><span class="sxs-lookup"><span data-stu-id="34617-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="34617-105">例如，分类帐数据描述公司遵循的会计年度、交易所用的货币以及所使用的帐户。</span><span class="sxs-lookup"><span data-stu-id="34617-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="34617-106">本主题介绍此核心财务数据的集成。</span><span class="sxs-lookup"><span data-stu-id="34617-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="34617-107">模板</span><span class="sxs-lookup"><span data-stu-id="34617-107">Templates</span></span>

<span data-ttu-id="34617-108">分类帐数据包括核心财务实体映射的集合，这些映射在数据交互期间协同工作，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="34617-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="34617-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="34617-109">Finance and Operations apps</span></span>      | <span data-ttu-id="34617-110">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="34617-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="34617-111">说明</span><span class="sxs-lookup"><span data-stu-id="34617-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="34617-112">币种</span><span class="sxs-lookup"><span data-stu-id="34617-112">Currencies</span></span>                       | <span data-ttu-id="34617-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="34617-113">transactioncurrencies</span></span>            |
<span data-ttu-id="34617-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="34617-114">FiscalCalendar</span></span>                   | <span data-ttu-id="34617-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="34617-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="34617-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="34617-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="34617-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="34617-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="34617-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="34617-118">ExchRateType</span></span>                     | <span data-ttu-id="34617-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="34617-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="34617-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="34617-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="34617-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="34617-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="34617-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="34617-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="34617-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="34617-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="34617-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="34617-124">MainAccountCategory</span></span>              | <span data-ttu-id="34617-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="34617-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="34617-126">主科目</span><span class="sxs-lookup"><span data-stu-id="34617-126">MainAccount</span></span>                      | <span data-ttu-id="34617-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="34617-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="34617-128">分类帐</span><span class="sxs-lookup"><span data-stu-id="34617-128">Ledger</span></span>                           | <span data-ttu-id="34617-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="34617-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="34617-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="34617-130">ExchangeRates</span></span>                    | <span data-ttu-id="34617-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="34617-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="34617-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="34617-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="34617-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="34617-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="34617-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="34617-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="34617-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="34617-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="34617-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="34617-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="34617-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="34617-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="34617-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="34617-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="34617-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="34617-139">msdyn\_chartofaccounts</span></span>        |


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




