---
title: "在期间结束时关闭总帐"
description: "本主题介绍为总帐执行定期结算时通常完成的任务。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 723e7306a0ffd0fd1a396a7852d9e7aa76f381fb
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="39fc8-103">在期间结束时关闭总帐</span><span class="sxs-lookup"><span data-stu-id="39fc8-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39fc8-104">本主题介绍为总帐执行定期结算时通常完成的任务。</span><span class="sxs-lookup"><span data-stu-id="39fc8-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="39fc8-105">在“总帐”中，您可以为期间或年度完成结转过程。</span><span class="sxs-lookup"><span data-stu-id="39fc8-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="39fc8-106">结转流程为新期间准备系统。</span><span class="sxs-lookup"><span data-stu-id="39fc8-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="39fc8-107">若要为新的一年准备系统，您必须运行年终结算流程。</span><span class="sxs-lookup"><span data-stu-id="39fc8-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="39fc8-108">每个组织有为期间结束时执行的不同的流程和步骤。</span><span class="sxs-lookup"><span data-stu-id="39fc8-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="39fc8-109">以下是期间结束的某些可选步骤：</span><span class="sxs-lookup"><span data-stu-id="39fc8-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="39fc8-110">完成所有其他模块的所有任务，例如应收账款、应付账款和库存。</span><span class="sxs-lookup"><span data-stu-id="39fc8-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="39fc8-111">验证所有日记帐均已过帐。</span><span class="sxs-lookup"><span data-stu-id="39fc8-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="39fc8-112">运行外币重估来生成所有或有损益金额。</span><span class="sxs-lookup"><span data-stu-id="39fc8-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="39fc8-113">结算每个会计科目的交易记录。</span><span class="sxs-lookup"><span data-stu-id="39fc8-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="39fc8-114">处理任何所需分配。</span><span class="sxs-lookup"><span data-stu-id="39fc8-114">Process any required allocations.</span></span>
-   <span data-ttu-id="39fc8-115">手动过帐期间结束调整。</span><span class="sxs-lookup"><span data-stu-id="39fc8-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="39fc8-116">将交易记录记入日记帐，并审查**分类帐日记帐**报表。</span><span class="sxs-lookup"><span data-stu-id="39fc8-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="39fc8-117">通过使用合并公司或财务报告执行合并。</span><span class="sxs-lookup"><span data-stu-id="39fc8-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="39fc8-118">通过使用财务报告生成期间结束财务报表。</span><span class="sxs-lookup"><span data-stu-id="39fc8-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="39fc8-119">设置分类帐期间为**暂停**，以便没有进一步过帐发生。</span><span class="sxs-lookup"><span data-stu-id="39fc8-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="39fc8-120">您还可以在发生期间结束活动时限制期间到特定的用户组，以便更好地控制。</span><span class="sxs-lookup"><span data-stu-id="39fc8-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="39fc8-121">将期间设置为**永久关闭**不是一个好主意，因为您将无法重新打开已关闭的期间。</span><span class="sxs-lookup"><span data-stu-id="39fc8-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="39fc8-122">“财务期间结帐”工作区可用于组织和跟踪各种期间结束流程所需任务。</span><span class="sxs-lookup"><span data-stu-id="39fc8-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="39fc8-123">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="39fc8-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="39fc8-124">财务期间结帐工作区</span><span class="sxs-lookup"><span data-stu-id="39fc8-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="39fc8-125">年终结算</span><span class="sxs-lookup"><span data-stu-id="39fc8-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="39fc8-126">批量财务期间结帐</span><span class="sxs-lookup"><span data-stu-id="39fc8-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





