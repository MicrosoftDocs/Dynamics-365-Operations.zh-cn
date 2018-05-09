---
title: "会计日历、会计年度和期间"
description: "本文讨论会计日历、会计年度和期间以及如何为法人、固定资产和预算使用它们。"
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 33c358e5f522500cea05c9f85a84c519f8c7b845
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a><span data-ttu-id="9bbf1-103">会计日历、会计年度和期间</span><span class="sxs-lookup"><span data-stu-id="9bbf1-103">Fiscal calendars, fiscal years, and periods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bbf1-104">本文讨论会计日历、会计年度和期间以及如何为法人、固定资产和预算使用它们。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-104">This article discusses fiscal calendars, fiscal years and periods and how to utilize them for legal entities, fixed assets and budgeting.</span></span>

<span data-ttu-id="9bbf1-105">会计年度为组织的财务活动提供一个框架。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-105">Fiscal calendars provide a framework for the financial activity of an organization.</span></span> <span data-ttu-id="9bbf1-106">每个会计年度包含一个或多个会计年度，并且每个会计年度包含多个期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-106">Each fiscal calendar contains one or more fiscal years, and each fiscal year contains multiple periods.</span></span> <span data-ttu-id="9bbf1-107">会计年度可以基于一个 1 月 1 日到 12 月 31 日的日历年度，或者您选择的任意日期。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-107">Fiscal calendars can be based on a January 1 to December 31 calendar year, or on any dates that you select.</span></span> <span data-ttu-id="9bbf1-108">例如，选择在一年的 7 月 1 日开始并且在下一年的 6 月 30 日结束的会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-108">For example, some organizations select a fiscal calendar that starts on July 1 of one year and ends on June 30 of the following year.</span></span> 

<span data-ttu-id="9bbf1-109">没有限制您可以创建的会计日历的数量和没有限制为会计日历创建的会计年度的数量。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-109">There is no limit to the number of fiscal calendars that you can create, and no limit to the number of fiscal years that can be created for a fiscal calendar.</span></span> <span data-ttu-id="9bbf1-110">每个会计日历与您的组织无关，可以由多个组织法人使用。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-110">Each fiscal calendar is independent of your organization, and can be used by multiple legal entities in the organization.</span></span> <span data-ttu-id="9bbf1-111">例如，组织具有八个部门，并且每个部门是独立的法人。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-111">For example, an organization has eight departments and each department is a separate legal entity.</span></span> <span data-ttu-id="9bbf1-112">它们五个共享相同的会计日历和三种使用不同的会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-112">Five of them share the same fiscal calendar and three use different fiscal calendars.</span></span> <span data-ttu-id="9bbf1-113">您可以创建共享相同会计日历的五个法人的会计日历，然后创建其他法人的单独的会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-113">You can create one fiscal calendar for the five legal entities that share the same fiscal calendar, and then create separate fiscal calendars for the other legal entities.</span></span>

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a><span data-ttu-id="9bbf1-114">创建会计日历、会计年度和期间</span><span class="sxs-lookup"><span data-stu-id="9bbf1-114">Create fiscal calendars, fiscal years, and periods</span></span>
<span data-ttu-id="9bbf1-115">您可以在“会计日历”页上创建并且删除会计日历、会计年度和期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-115">You can create and delete fiscal calendars, fiscal years, and periods on the Fiscal calendars page.</span></span> <span data-ttu-id="9bbf1-116">您还可以划分现有期间和创建可用于结算某个会计年度的结转期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-116">You can also divide existing periods and create closing periods that can be used to close a fiscal year.</span></span> 

<span data-ttu-id="9bbf1-117">结算期间用于划分结算某个会计年度时生成的总账交易记录。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-117">A closing period is used to separate general ledger transactions that are generated when a fiscal year is closed.</span></span> <span data-ttu-id="9bbf1-118">当结算交易记录都处于一个会计期间时，很容易创建包括或排除不同类型结算条目的财务报表。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-118">When the closing transactions are in one fiscal period, it is easier to create financial statements that either include or exclude different types of closing entries.</span></span> <span data-ttu-id="9bbf1-119">如果将一个会计年度划分为 12 个会计期间，这结算期通常为第 13 期。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-119">If a fiscal year is divided into 12 fiscal periods, the closing period is usually the 13th period.</span></span> <span data-ttu-id="9bbf1-120">但是，可以从具有状态“未完成”的任何期间创建结算期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-120">However, a closing period can be created from any period that has a status of Open.</span></span> 

<span data-ttu-id="9bbf1-121">当您创建一个结算期间时，选择一个具有状态“未完成”并具有您要使用的日期的期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-121">When you create a closing period, select a period that has a status of Open and that has the dates that you want to use.</span></span> <span data-ttu-id="9bbf1-122">新的结算期间将从现有期间中复制开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-122">The new closing period will copy the starting and ending dates from the existing period.</span></span> <span data-ttu-id="9bbf1-123">原始期间将继续存在。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-123">The original period will continue to exist.</span></span> <span data-ttu-id="9bbf1-124">例如，您选择了为该会计年度的最后一个期间并具有 8 月 1 日到 8 月 31 日这些日期的“期间 12”。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-124">For example, you select Period 12, which is the last period in the fiscal year, and that has dates of August 1 through August 31.</span></span> <span data-ttu-id="9bbf1-125">您为该结算期间输入了一个名词，如 “结算”。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-125">You enter a name for the closing period, such as Close.</span></span> <span data-ttu-id="9bbf1-126">当您创建了该新的结算期间后，现在您拥有原始期间和结算期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-126">After you create the new closing period, you now have the original period and the closing period.</span></span> <span data-ttu-id="9bbf1-127">都含有 8 月 1 日到 8 月 31 日的日期。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-127">Both have dates that start on August 1 and end on August 31.</span></span>

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a><span data-ttu-id="9bbf1-128">为分类帐、固定资产和预算期间选择会计日历</span><span class="sxs-lookup"><span data-stu-id="9bbf1-128">Select fiscal calendars for ledgers, fixed assets, and budget cycles</span></span>
<span data-ttu-id="9bbf1-129">会计日历用于固定资产折旧、财务交易记录和预算期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-129">Fiscal calendars are used with fixed asset depreciation, financial transactions, and budget cycles.</span></span> <span data-ttu-id="9bbf1-130">在您创建某一会计日历时，您可以为多个目的使用它。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-130">When you create a fiscal calendar, you can use it for multiple purposes.</span></span> <span data-ttu-id="9bbf1-131">您可以选择价值模型或折旧帐簿的会计日历以使其为固定资产日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-131">You can select a fiscal calendar for a value model or depreciation book to make it a fixed asset calendar.</span></span> <span data-ttu-id="9bbf1-132">您可以选择分类帐的会计日历以使其为分类帐日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-132">You can select a fiscal calendar for a ledger to make it a ledger calendar.</span></span> <span data-ttu-id="9bbf1-133">并且您可以选择预算期间的会计日历以使其为预算日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-133">And you can select a fiscal calendar for a budget cycle to make it a budget calendar.</span></span> <span data-ttu-id="9bbf1-134">您可以为所有这些使用相同的会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-134">You can use the same fiscal calendar for all of these.</span></span>

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a><span data-ttu-id="9bbf1-135">为您的法人选择某一会计日历</span><span class="sxs-lookup"><span data-stu-id="9bbf1-135">Select a fiscal calendar for your legal entity</span></span>

<span data-ttu-id="9bbf1-136">选择要为“分类帐”窗体中您的法人的分类帐使用的会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-136">Select the fiscal calendar that you want to use for the ledger for your legal entity in the Ledger form.</span></span> <span data-ttu-id="9bbf1-137">必须在“分类帐”页上为每个法人选择一个会计日历。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-137">A fiscal calendar must be selected on the Ledger page for every legal entity.</span></span> <span data-ttu-id="9bbf1-138">当您选择了一个会计日历之后，您可以针对属于会计年度一部分的任何期间在“分类帐日历”页上设置期间状态和权限。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-138">After a fiscal calendar is selected, you can set up period statuses and permissions on the Ledger calendar page for any of the periods that are part of a fiscal year.</span></span>

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a><span data-ttu-id="9bbf1-139">选择固定资产的会计日历</span><span class="sxs-lookup"><span data-stu-id="9bbf1-139">Select a fiscal calendar for fixed assets</span></span>

<span data-ttu-id="9bbf1-140">您可以为价值模型或折旧帐簿选择会计日历，并且该会计日历将由使用所选价值模型或折旧帐簿的固定资产使用。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-140">You can select a fiscal calendar for a value model or depreciation book, and that fiscal calendar will be used by the fixed assets that use the selected value model or depreciation book.</span></span> <span data-ttu-id="9bbf1-141">您可以从在“会计日历”页上定义的任何会计日历中进行选择。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-141">You can select from any fiscal calendar that is defined on the Fiscal calendars page.</span></span>

### <a name="define-budget-cycle-time-spans"></a><span data-ttu-id="9bbf1-142">定义预算周期跨度</span><span class="sxs-lookup"><span data-stu-id="9bbf1-142">Define budget cycle time spans</span></span>

<span data-ttu-id="9bbf1-143">预算期间是在期间使用预算的时间长度。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-143">Budget cycles are the length of time during which a budget is used.</span></span> <span data-ttu-id="9bbf1-144">预算期间可能包含一个会计年度或多个会计年度的一部分，例如一个两年一次的预算期间或一个三年一次的预算期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-144">Budget cycles can include part of a fiscal year or multiple fiscal years, such as a biennial budget cycle of two years or a triennial budget cycle of three years.</span></span> <span data-ttu-id="9bbf1-145">预算期间跨度定义在预算期间包括的期间的数量。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-145">The budget cycle time span defines the number of periods that are included in the budget cycle.</span></span> <span data-ttu-id="9bbf1-146">若要指定预算周期跨度，请使用“预算周期跨度”页。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-146">To specify the budget cycle time span, use the Budget cycle time spans page.</span></span>

## <a name="maintain-periods-for-your-organization"></a><span data-ttu-id="9bbf1-147">维护您的组织的期间</span><span class="sxs-lookup"><span data-stu-id="9bbf1-147">Maintain periods for your organization</span></span>
<span data-ttu-id="9bbf1-148">您可以使用“分类帐日历”页查看您的组织使用的会计日历、会计年度和期间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-148">You can use the Ledger calendar page to view the details of the fiscal calendar, fiscal years, and periods used by your organization.</span></span> <span data-ttu-id="9bbf1-149">您还可以更改该期间的状态和选择哪些用户都可以过帐会计科目交易记录到期间。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-149">You can also change the status of the periods and select which users can post accounting transactions to periods.</span></span> <span data-ttu-id="9bbf1-150">例如，在新期间的开始，当其他组只在新期间工作时，您可能希望一组用户在前一期间完成过帐财务交易记录。</span><span class="sxs-lookup"><span data-stu-id="9bbf1-150">For example, at the start of a new period, you might want a group of users to finish posting financial transactions in the previous period, while other groups work only in the new period.</span></span>






