---
title: 会计分配
description: 本文提供有关会计分配的信息并介绍可用于处理它们的选项。 会计分配用于将原始凭证的货币金额分配到特定会计科目。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e9f185ac95371bb841e55184650b8089040676c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772252"
---
# <a name="accounting-distributions"></a><span data-ttu-id="d3843-104">会计分配</span><span class="sxs-lookup"><span data-stu-id="d3843-104">Accounting distributions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3843-105">本文提供有关会计分配的信息并介绍可用于处理它们的选项。</span><span class="sxs-lookup"><span data-stu-id="d3843-105">This article provides information about accounting distributions and describes the options that are available for processing them.</span></span> <span data-ttu-id="d3843-106">会计分配用于将原始凭证的货币金额分配到特定会计科目。</span><span class="sxs-lookup"><span data-stu-id="d3843-106">Accounting distributions are used to allocate monetary amounts for a source document to specific ledger accounts.</span></span> 

<span data-ttu-id="d3843-107">会计分配是由每个原始凭证使用和扩展的程序范围的功能，如采购订单、供应商发票、支出报表和普通发票。</span><span class="sxs-lookup"><span data-stu-id="d3843-107">Accounting distributions are a program-wide capability that is used and extended by each source document, such as a purchase order, vendor invoice, expense report, and free text invoice.</span></span> <span data-ttu-id="d3843-108">默认情况下，默认会计分配为每个原始凭证行和货币金额生成，并有条件地为修改启用。</span><span class="sxs-lookup"><span data-stu-id="d3843-108">By default, a default accounting distribution is generated for each source document line and monetary amount, and is conditionally enabled for modification.</span></span> 

> [!Note] 
> <span data-ttu-id="d3843-109">某些凭证还支持标题凭证货币金额，例如订单和发票的费用。</span><span class="sxs-lookup"><span data-stu-id="d3843-109">Some documents also support header document monetary amounts, such as charges for orders and invoices.</span></span> 

<span data-ttu-id="d3843-110">一般会计分配功能提供处理会计分配的以下选项：</span><span class="sxs-lookup"><span data-stu-id="d3843-110">The generic accounting distribution capabilities provide the following options for processing accounting distributions:</span></span>

-   <span data-ttu-id="d3843-111">**分摊金额** – 查看和修改单独凭证标题行和任何子行的会计分配，例如税金或费用。</span><span class="sxs-lookup"><span data-stu-id="d3843-111">**Distribute amounts** – View and modify the accounting distributions for an individual document header or line and any child lines, such as taxes or charges.</span></span>
    -   <span data-ttu-id="d3843-112">对于顶部货币金额分配（父分配），主科目和财务维度可以在网格中的 Segmented Entry 控件中直接编辑。</span><span class="sxs-lookup"><span data-stu-id="d3843-112">For the top monetary amount distributions (parent distributions), the main account and financial dimensions might be editable directly in the segmented entry control in the grid.</span></span> <span data-ttu-id="d3843-113">延伸价格是这样一个父分配的典型示例。</span><span class="sxs-lookup"><span data-stu-id="d3843-113">The extended price is a typical example of such a parent distribution.</span></span>
    -   <span data-ttu-id="d3843-114">分配金额基于的凭证的条款币种。</span><span class="sxs-lookup"><span data-stu-id="d3843-114">The distributions amounts are based on the term currency for the document.</span></span> <span data-ttu-id="d3843-115">通常，此币种是交易记录币种。</span><span class="sxs-lookup"><span data-stu-id="d3843-115">Typically, this currency is the transaction currency.</span></span> <span data-ttu-id="d3843-116">会计和申报币种金额作为子分类帐会计的一部分生成。</span><span class="sxs-lookup"><span data-stu-id="d3843-116">Accounting and reporting currency amounts are generated as part of subledger accounting.</span></span>
    -   <span data-ttu-id="d3843-117">分配显示会计日期和会计事件。</span><span class="sxs-lookup"><span data-stu-id="d3843-117">The distributions display the accounting date and accounting event.</span></span> <span data-ttu-id="d3843-118">通常，会计事件设置为**无**，直到凭证已过帐/记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="d3843-118">Typically, the accounting event is set to **None** until the document is posted/journalized.</span></span> <span data-ttu-id="d3843-119">此时，会计事件将变为**原始**。</span><span class="sxs-lookup"><span data-stu-id="d3843-119">At that point, the accounting event becomes **Original**.</span></span> <span data-ttu-id="d3843-120">在分配过帐后，就不能修改分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-120">After the distributions have been posted, you can't modify the distributions.</span></span>
    -   <span data-ttu-id="d3843-121">**分解**按钮可以针对父分配启用。</span><span class="sxs-lookup"><span data-stu-id="d3843-121">**Split** button might be enabled for parent distributions.</span></span> <span data-ttu-id="d3843-122">**分解**生成新的会计分配，并且，分解可以基于百分比、金额或数量。</span><span class="sxs-lookup"><span data-stu-id="d3843-122">**Split** generates new accounting distributions, and the split can be based on percentage, amount, or quantity.</span></span>
    -   <span data-ttu-id="d3843-123">**平均分配**按钮可以与**分解**结合使用来在所有分配之间自动平均分配金额。</span><span class="sxs-lookup"><span data-stu-id="d3843-123">The **Distribute equally** button can be used in combination with **Split** to automatically allocate the amount equally across all distributions.</span></span>
    -   <span data-ttu-id="d3843-124">**重置**按钮在多个分配存在时，可以针对父分配启用。</span><span class="sxs-lookup"><span data-stu-id="d3843-124">**Reset** button might be enabled for parent distributions when more than one distributions exists.</span></span> <span data-ttu-id="d3843-125">**重置**通过删除所有现有分配和重新生成默认分配撤消对分配的所有手动修改。</span><span class="sxs-lookup"><span data-stu-id="d3843-125">**Reset** reverses any manual modification to the distribution by deleting all existing distributions and re-generating the default distributions.</span></span>
    -   <span data-ttu-id="d3843-126">所有子分配，例如折扣、费用和销售税，始终遵循父分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-126">Any child distribution, such as discount, charge, and sales tax, always follows the parent distribution.</span></span> <span data-ttu-id="d3843-127">您可以在**引用** &gt; **父信息**查看父/子关系。</span><span class="sxs-lookup"><span data-stu-id="d3843-127">You can view the parent/child relation at **Reference** &gt; **Parent information**.</span></span>
    -   <span data-ttu-id="d3843-128">主科目和财务维度还可能对子项是可编辑的。</span><span class="sxs-lookup"><span data-stu-id="d3843-128">The main account and financial dimension might be editable for children too.</span></span>
    -   <span data-ttu-id="d3843-129">会计分配的财务维度按照凭证可扩展的默认模式。</span><span class="sxs-lookup"><span data-stu-id="d3843-129">The financial dimensions on the accounting distributions follow a defaulting pattern that a document can extended.</span></span> <span data-ttu-id="d3843-130">有关详细信息，请参阅相关文章。</span><span class="sxs-lookup"><span data-stu-id="d3843-130">For more details, see the related articles.</span></span>
    -   <span data-ttu-id="d3843-131">差异匹配可能在匹配方案中生成，例如供应商发票和采购订单之间的匹配。</span><span class="sxs-lookup"><span data-stu-id="d3843-131">Variance distributions might be generated in matching scenarios, such as matching between a vendor invoice and a purchase order.</span></span> <span data-ttu-id="d3843-132">您可以在**引用** &gt; **凭证信息**中查看会计分配之间的匹配关系。</span><span class="sxs-lookup"><span data-stu-id="d3843-132">You can view the matching relations between accounting distribution at **Reference** &gt; **Document information**.</span></span>
    -   <span data-ttu-id="d3843-133">**更正**按钮显示并针对支持更正的凭证启用。</span><span class="sxs-lookup"><span data-stu-id="d3843-133">**Correct** button appears and is enabled for documents that support corrections.</span></span> <span data-ttu-id="d3843-134">**更正**创建新的分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-134">**Correct** creates new distributions.</span></span> <span data-ttu-id="d3843-135">首先，创建撤消原始分配的分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-135">First, distributions are created that reverse the original distributions.</span></span> <span data-ttu-id="d3843-136">不能修改这些分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-136">These distributions can't be modified.</span></span> <span data-ttu-id="d3843-137">接下来，创建新的正确会计分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-137">Next, new correct accounting distributions are created.</span></span> <span data-ttu-id="d3843-138">如果原始分配无法修改，这些分配可以修改。</span><span class="sxs-lookup"><span data-stu-id="d3843-138">These distributions can be modified if the original distributions could be modified.</span></span>
    -   <span data-ttu-id="d3843-139">当行与项目关联时，**项目详细信息**按钮作为扩展启用。</span><span class="sxs-lookup"><span data-stu-id="d3843-139">The **Project details** button is enabled as an extension when a line is related to a project.</span></span> <span data-ttu-id="d3843-140">项目会计分配可以修改详细信息，例如融资来源和记录属性。</span><span class="sxs-lookup"><span data-stu-id="d3843-140">Project accounting distributions let you modify details such as the funding source and line property.</span></span>
    -   <span data-ttu-id="d3843-141">您可以在**引用**中查看当前凭证会计状态。</span><span class="sxs-lookup"><span data-stu-id="d3843-141">You can view the current document accounting status in **Reference**.</span></span> <span data-ttu-id="d3843-142">状态针对整个凭证，并指示凭证是在进行中或已完成。</span><span class="sxs-lookup"><span data-stu-id="d3843-142">The status is for the entire document, and indicates whether the document is in process or completed.</span></span>
-   <span data-ttu-id="d3843-143">**查看分配** – 查看凭证中所有行和货币金额的会计分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-143">\*\* View distributions\*\* – View the accounting distributions for the all lines and monetary amounts on the document.</span></span> <span data-ttu-id="d3843-144">您无法从此视图修改会计分配。</span><span class="sxs-lookup"><span data-stu-id="d3843-144">You can't modify the accounting distributions from this view.</span></span>


<span data-ttu-id="d3843-145">有关详细信息，请参阅[会计分配和供应商的子分类日记帐条目](accounting-distributions-subledger-journal-entries-vendor-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="d3843-145">For more information, see [Accounting distributions and subledger journal entries for vendor invoices](accounting-distributions-subledger-journal-entries-vendor-invoices.md).</span></span>


