---
title: "总帐和财务报表主页"
description: "使用总帐定义和管理法人的财务记录。 总帐是借方和贷方登记条目。 这些条目进行分类使用在会计科目表中列出的科目。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="4e034-105">总帐</span><span class="sxs-lookup"><span data-stu-id="4e034-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4e034-106">使用总帐定义和管理法人的财务记录。</span><span class="sxs-lookup"><span data-stu-id="4e034-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="4e034-107">总帐是借方和贷方登记条目。</span><span class="sxs-lookup"><span data-stu-id="4e034-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="4e034-108">这些条目进行分类使用在会计科目表中列出的科目。</span><span class="sxs-lookup"><span data-stu-id="4e034-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="4e034-109">分配是基于分配规则将金额分配到一个或多个帐户或帐户/维度组合的过程。</span><span class="sxs-lookup"><span data-stu-id="4e034-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="4e034-110">存在两种类型的分配：固定和可变。</span><span class="sxs-lookup"><span data-stu-id="4e034-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="4e034-111">您还可以在结算会计科目之间的交易记录和重估原币金额。</span><span class="sxs-lookup"><span data-stu-id="4e034-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="4e034-112">在某一会计年度结束时，您必须为下一会计年度准备您的科目，并且关闭当前会计年度。</span><span class="sxs-lookup"><span data-stu-id="4e034-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="4e034-113">您可以使用合并功能以合并若干子公司的财务结果为唯一的合并公司的财务结果。</span><span class="sxs-lookup"><span data-stu-id="4e034-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="4e034-114">这些子公司可以存在于相同的 Microsoft Dynamics 365 for Finance and Operations 数据库中或在单独的数据库中。</span><span class="sxs-lookup"><span data-stu-id="4e034-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="4e034-115">销售税</span><span class="sxs-lookup"><span data-stu-id="4e034-115">Sales tax</span></span>
<span data-ttu-id="4e034-116">每个公司都需要向各种税务主管机构缴纳税款。</span><span class="sxs-lookup"><span data-stu-id="4e034-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="4e034-117">规则和比率根据国家/地区、省/市/自治区、县和城市而改变。</span><span class="sxs-lookup"><span data-stu-id="4e034-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="4e034-118">此外，当税务主管部门更改它们的要求时，必须定期更新规则。</span><span class="sxs-lookup"><span data-stu-id="4e034-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="4e034-119">增值税代码包含您收取以及支付给主管机构的金额数的信息。</span><span class="sxs-lookup"><span data-stu-id="4e034-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="4e034-120">当您设置增值税代码时，您定义了必须收取的金额或百分比。</span><span class="sxs-lookup"><span data-stu-id="4e034-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="4e034-121">您还定义了将这些金额或百分比应用到交易记录金额中的各种方法。</span><span class="sxs-lookup"><span data-stu-id="4e034-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="4e034-122">本节中的主题提供了如何针对您的税务主管机构要求的方法和比率设置增值税的信息。</span><span class="sxs-lookup"><span data-stu-id="4e034-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







