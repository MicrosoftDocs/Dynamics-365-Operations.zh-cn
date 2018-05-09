---
title: "从交易记录科目和合计科目创建预算"
description: "本文提供基于合计科目创建预算的流程的概览。 还说明如果需要预算控制，如何启用合计科目的预算控制。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3b7c8031c40cf0ce3072577ac936aecc5de2a810
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="679c1-104">从交易记录科目和合计科目创建预算</span><span class="sxs-lookup"><span data-stu-id="679c1-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="679c1-105">本文提供基于合计科目创建预算的流程的概览。</span><span class="sxs-lookup"><span data-stu-id="679c1-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="679c1-106">还说明如果需要预算控制，如何启用合计科目的预算控制。</span><span class="sxs-lookup"><span data-stu-id="679c1-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="679c1-107">预算计划和预算登记条目文档允许对具有**合计**主科目类型的主科目编制预算。</span><span class="sxs-lookup"><span data-stu-id="679c1-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="679c1-108">实际只能过帐到交易记录主科目。</span><span class="sxs-lookup"><span data-stu-id="679c1-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="679c1-109">对于**从总帐生成预算计划**定期流程，在**源**选项卡上，您指定**合计**主科目类型作为条件。</span><span class="sxs-lookup"><span data-stu-id="679c1-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="679c1-110">在这种情况下，每个总计主科目将包括在目标预算计划中，并且，金额将等于所选主科目范围的总金额。</span><span class="sxs-lookup"><span data-stu-id="679c1-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="679c1-111">您可以激活**合计**类型的主科目的预算控制。</span><span class="sxs-lookup"><span data-stu-id="679c1-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="679c1-112">此功能通过使用预算组受支持。</span><span class="sxs-lookup"><span data-stu-id="679c1-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="679c1-113">对于每个总计主科目，应为预算组控制的预算必须在 **预算控制配置** 页创建。</span><span class="sxs-lookup"><span data-stu-id="679c1-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="679c1-114">您指定的条件必须包括总计主科目和科目范围。</span><span class="sxs-lookup"><span data-stu-id="679c1-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="679c1-115">若要加快创建预算组的过程，您可以利用预算控制组数据实体。</span><span class="sxs-lookup"><span data-stu-id="679c1-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="679c1-116">在报告中（例如在财务报表中）使用预算时，总计科目的预算总和由以下金额组成：</span><span class="sxs-lookup"><span data-stu-id="679c1-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="679c1-117">在合计科目间隔中的每个交易记录会计科目中创建的预算。</span><span class="sxs-lookup"><span data-stu-id="679c1-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="679c1-118">直接在合计科目上输入的预算金额。</span><span class="sxs-lookup"><span data-stu-id="679c1-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="679c1-119">因此，您可以为合计科目间隔中最重要的交易记录科目创建单独的预算，然后将剩余预算金额添加到合计科目。</span><span class="sxs-lookup"><span data-stu-id="679c1-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




