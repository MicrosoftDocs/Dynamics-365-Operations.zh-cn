---
title: "计划您的会计科目表"
description: "本主题提供将帮助您为您的组织计划会计科目表的信息。"
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3f8d97fc42cde9053b0552fc1dfe8e6de0f5e03b
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="cc738-103">计划您的会计科目表</span><span class="sxs-lookup"><span data-stu-id="cc738-103">Plan your chart of accounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="cc738-104">本主题提供将帮助您为您的组织计划会计科目表的信息。</span><span class="sxs-lookup"><span data-stu-id="cc738-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="cc738-105">若要跟踪和维护组织的财务信息，您可以设置会计科目表。</span><span class="sxs-lookup"><span data-stu-id="cc738-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="cc738-106">会计科目表是定义一个财务框架的帐户的集合。</span><span class="sxs-lookup"><span data-stu-id="cc738-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="cc738-107">若要进一步跟踪这些科目中的交易记录，可添加细分市场。</span><span class="sxs-lookup"><span data-stu-id="cc738-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="cc738-108">这些细分市场称为财务维度。</span><span class="sxs-lookup"><span data-stu-id="cc738-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="cc738-109">例如，支出帐户可能包括名为“部门”、“成本中心”和“用途”的财务维度。</span><span class="sxs-lookup"><span data-stu-id="cc738-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="cc738-110">用户定义的规则确定财务维度如何附加到主科目和其他财务维度以及如何输入交易记录。</span><span class="sxs-lookup"><span data-stu-id="cc738-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="cc738-111">这些用户定义的规则称为科目结构和高级规则。</span><span class="sxs-lookup"><span data-stu-id="cc738-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="cc738-112">会计科目表是法人的总账科目的结构性列表。</span><span class="sxs-lookup"><span data-stu-id="cc738-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="cc738-113">此列表用于为主管机构和所有者准备财务报表。</span><span class="sxs-lookup"><span data-stu-id="cc738-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="cc738-114">这些科目首先将分组为不同科目类型，然后进一步合并为更大的类别。</span><span class="sxs-lookup"><span data-stu-id="cc738-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="cc738-115">在最一般的级别上，科目按利润和成本（营业科目）以及资产和负债（余额科目）进行分类。</span><span class="sxs-lookup"><span data-stu-id="cc738-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="cc738-116">会计科目表可由组织中的法人共享和使用。</span><span class="sxs-lookup"><span data-stu-id="cc738-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="cc738-117">法人使用的会计科目表在**分类帐**页中定义。</span><span class="sxs-lookup"><span data-stu-id="cc738-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="cc738-118">以下是在您计划您的组织的会计科目表的结构时必须考虑的若干因素：</span><span class="sxs-lookup"><span data-stu-id="cc738-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="cc738-119">您的组织所在的国家或地区的报告要求</span><span class="sxs-lookup"><span data-stu-id="cc738-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="cc738-120">您的法人的报告要求</span><span class="sxs-lookup"><span data-stu-id="cc738-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="cc738-121">外部组织和您的组织都需要的规范的程度</span><span class="sxs-lookup"><span data-stu-id="cc738-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="cc738-122">在**会计科目表**页创建会计科目表。</span><span class="sxs-lookup"><span data-stu-id="cc738-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="cc738-123">可以从**会计科目表**页或**主科目**页创建主科目。</span><span class="sxs-lookup"><span data-stu-id="cc738-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="cc738-124">您的主科目不应使用用作会计科目表分隔符的任何特殊字符。</span><span class="sxs-lookup"><span data-stu-id="cc738-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="cc738-125">否则，您可能遇到不稳定性，或者可能在输入科目和维度的组合时必须使用查找或对话框。</span><span class="sxs-lookup"><span data-stu-id="cc738-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="cc738-126">有关详细信息，请参阅[创建主科目](tasks/create-main-account.md)。</span><span class="sxs-lookup"><span data-stu-id="cc738-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cc738-127">在 Microsoft Dynamics for Finance and Operations 版本 8.0（2018 年 4 月）中，可从**总帐参数**页修改会计科目表分隔符。</span><span class="sxs-lookup"><span data-stu-id="cc738-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="cc738-128">最好是将主科目与主科目类别链接，以便您可以利用默认财务报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="cc738-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="cc738-129">因此，您可以迅速并轻松地设计和维护报表。</span><span class="sxs-lookup"><span data-stu-id="cc738-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="cc738-130">在**配置科目结构**页创建科目结构。</span><span class="sxs-lookup"><span data-stu-id="cc738-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="cc738-131">科目结构定义有效组合。</span><span class="sxs-lookup"><span data-stu-id="cc738-131">Account structures define valid combinations.</span></span> <span data-ttu-id="cc738-132">这些组合和主科目一起形成了会计科目表。</span><span class="sxs-lookup"><span data-stu-id="cc738-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="cc738-133">有关详细信息，请参阅[创建科目结构](tasks/create-account-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="cc738-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="cc738-134">**法人覆盖**</span><span class="sxs-lookup"><span data-stu-id="cc738-134">**Legal entity overrides**</span></span>

<span data-ttu-id="cc738-135">并非所有主科目对所有法人均有效，部分主科目可能只与特定时段相关。</span><span class="sxs-lookup"><span data-stu-id="cc738-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="cc738-136">在这种情况下，您可以使用**法人替代**部分识别应为其暂停主科目的公司、所有者以及维度有效的期间。</span><span class="sxs-lookup"><span data-stu-id="cc738-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="cc738-137">共享级别的替代不能比法人级别的替代更加严格。</span><span class="sxs-lookup"><span data-stu-id="cc738-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="cc738-138">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="cc738-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="cc738-139">财务维度</span><span class="sxs-lookup"><span data-stu-id="cc738-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="cc738-140">创建和分配高级规则结构</span><span class="sxs-lookup"><span data-stu-id="cc738-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)

