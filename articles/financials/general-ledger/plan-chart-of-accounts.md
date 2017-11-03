---
title: "规划会计科目表"
description: "本文提供将帮助您为您的组织计划会计科目表的信息。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 038886f0a6e1c133a33ee34725eb20352e64341a
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="13675-103">规划会计科目表</span><span class="sxs-lookup"><span data-stu-id="13675-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="13675-104">本文提供将帮助您为您的组织计划会计科目表的信息。</span><span class="sxs-lookup"><span data-stu-id="13675-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="13675-105">若要跟踪和维护组织的财务信息，您可以设置会计科目表。</span><span class="sxs-lookup"><span data-stu-id="13675-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="13675-106">会计科目表是定义一个财务框架的帐户的集合。</span><span class="sxs-lookup"><span data-stu-id="13675-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="13675-107">要进一步跟踪这些帐户中的交易记录，可以添加名为财务维度的段。</span><span class="sxs-lookup"><span data-stu-id="13675-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="13675-108">例如，支出帐户可能包括名为“部门”、“成本中心”和“用途”的财务维度。</span><span class="sxs-lookup"><span data-stu-id="13675-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="13675-109">名为科目结构和高级规则的用户定义的规则确定财务维度如何附加到主科目和其他财务维度以及如何输入交易记录。</span><span class="sxs-lookup"><span data-stu-id="13675-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="13675-110">会计科目表是法人的总账科目的结构性列表。</span><span class="sxs-lookup"><span data-stu-id="13675-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="13675-111">此列表用于为主管机构和所有者准备财务报表。</span><span class="sxs-lookup"><span data-stu-id="13675-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="13675-112">这些科目将分组为不同科目类型，然后进一步合并为更大的类别。</span><span class="sxs-lookup"><span data-stu-id="13675-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="13675-113">在最一般的级别上，科目按利润和成本（营业科目）以及资产和负债（余额科目）进行分类。</span><span class="sxs-lookup"><span data-stu-id="13675-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="13675-114">会计科目表可由组织中的法人共享和使用。</span><span class="sxs-lookup"><span data-stu-id="13675-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="13675-115">法人使用的会计科目表在**分类帐**页中定义。</span><span class="sxs-lookup"><span data-stu-id="13675-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="13675-116">以下是在您计划您的组织的会计科目表的结构时必须考虑的若干因素：</span><span class="sxs-lookup"><span data-stu-id="13675-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="13675-117">您的组织所在的国家/地区的报告要求</span><span class="sxs-lookup"><span data-stu-id="13675-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="13675-118">您的法人的报告要求</span><span class="sxs-lookup"><span data-stu-id="13675-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="13675-119">外部组织和您的组织都需要的规范的程度</span><span class="sxs-lookup"><span data-stu-id="13675-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="13675-120">在**会计科目表**页创建会计科目表。</span><span class="sxs-lookup"><span data-stu-id="13675-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="13675-121">主科目可以从**会计科目表**页或**主科目**页创建。</span><span class="sxs-lookup"><span data-stu-id="13675-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="13675-122">您的主科目不应使用用作会计科目表分隔符的任何特殊字符。</span><span class="sxs-lookup"><span data-stu-id="13675-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="13675-123">如果您具有与您的会计科目表分隔符相同的特殊字符，您可能遇到不稳定性或在输入帐户和维度组合时需要始终使用查找或浮出。</span><span class="sxs-lookup"><span data-stu-id="13675-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="13675-124">有关详细信息，请参阅[创建主科目](tasks/create-account-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="13675-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="13675-125">最好是将主科目与主科目类别链接，以便您可以利用默认财务报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="13675-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="13675-126">因此，您可以迅速并轻松地设计和维护报表。</span><span class="sxs-lookup"><span data-stu-id="13675-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="13675-127">使用**配置科目结构**页创建科目结构。</span><span class="sxs-lookup"><span data-stu-id="13675-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="13675-128">科目结构定义有效组合。</span><span class="sxs-lookup"><span data-stu-id="13675-128">Account structures define valid combinations.</span></span> <span data-ttu-id="13675-129">这些组合和主科目一起形成了会计科目表。</span><span class="sxs-lookup"><span data-stu-id="13675-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="13675-130">有关详细信息，请参阅[创建科目结构](tasks/create-main-account.md)。</span><span class="sxs-lookup"><span data-stu-id="13675-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="13675-131">**法人覆盖**</span><span class="sxs-lookup"><span data-stu-id="13675-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="13675-132">并非所有主科目对所有法人均有效，部分维度可能只与特定时段相关。</span><span class="sxs-lookup"><span data-stu-id="13675-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="13675-133">在此情况中，”法人覆盖“部分可用于确定主科目应处于暂停状态的公司，谁是所有者，以及维度有效的时段。</span><span class="sxs-lookup"><span data-stu-id="13675-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="13675-134">共享级别的覆盖不能比法人级别的覆盖更加严格。</span><span class="sxs-lookup"><span data-stu-id="13675-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="13675-135">有关详细信息，请参阅以下主题：[财务维度](financial-dimensions.md)
[创建和分配高级规则结构](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="13675-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




