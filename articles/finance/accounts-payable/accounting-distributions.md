---
title: 会计分配
description: 本主题提供有关会计分配的信息并介绍可用于处理它们的选项。
author: ShylaThompson
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7191e1e48283d2468155c84d408b030a7c50e4d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252161"
---
# <a name="accounting-distributions"></a><span data-ttu-id="869ed-103">会计分配</span><span class="sxs-lookup"><span data-stu-id="869ed-103">Accounting distributions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="869ed-104">本主题提供有关会计分配的信息并介绍可用于处理它们的选项。</span><span class="sxs-lookup"><span data-stu-id="869ed-104">This topic provides information about accounting distributions and describes the options that are available for processing them.</span></span> <span data-ttu-id="869ed-105">会计分配用于将原始凭证的货币金额分配到特定会计科目。</span><span class="sxs-lookup"><span data-stu-id="869ed-105">Accounting distributions are used to allocate monetary amounts for a source document to specific ledger accounts.</span></span> 

<span data-ttu-id="869ed-106">会计分配是由每个原始凭证使用和扩展的程序范围的功能，如采购订单、供应商发票、支出报表和普通发票。</span><span class="sxs-lookup"><span data-stu-id="869ed-106">Accounting distributions are a program-wide capability that is used and extended by each source document, such as a purchase order, vendor invoice, expense report, and free text invoice.</span></span> <span data-ttu-id="869ed-107">默认情况下，默认会计分配为每个原始凭证行和货币金额生成，并有条件地为修改启用。</span><span class="sxs-lookup"><span data-stu-id="869ed-107">By default, a default accounting distribution is generated for each source document line and monetary amount, and is conditionally enabled for modification.</span></span> 

> [!NOTE] 
> <span data-ttu-id="869ed-108">某些凭证还支持标题凭证货币金额，例如订单和发票的费用。</span><span class="sxs-lookup"><span data-stu-id="869ed-108">Some documents also support header document monetary amounts, such as charges for orders and invoices.</span></span> 

<span data-ttu-id="869ed-109">一般会计分配功能提供处理会计分配的以下选项：</span><span class="sxs-lookup"><span data-stu-id="869ed-109">The generic accounting distribution capabilities provide the following options for processing accounting distributions:</span></span>

-   <span data-ttu-id="869ed-110">**分摊金额** – 查看和修改单独凭证标题行和任何子行的会计分配，例如税金或费用。</span><span class="sxs-lookup"><span data-stu-id="869ed-110">**Distribute amounts** – View and modify the accounting distributions for an individual document header or line and any child lines, such as taxes or charges.</span></span>
    -   <span data-ttu-id="869ed-111">对于顶部货币金额分配（父分配），主科目和财务维度可以在网格中的 Segmented Entry 控件中直接编辑。</span><span class="sxs-lookup"><span data-stu-id="869ed-111">For the top monetary amount distributions (parent distributions), the main account and financial dimensions might be editable directly in the segmented entry control in the grid.</span></span> <span data-ttu-id="869ed-112">延伸价格是这样一个父分配的典型示例。</span><span class="sxs-lookup"><span data-stu-id="869ed-112">The extended price is a typical example of such a parent distribution.</span></span>
    -   <span data-ttu-id="869ed-113">分配金额基于的凭证的条款币种。</span><span class="sxs-lookup"><span data-stu-id="869ed-113">The distributions amounts are based on the term currency for the document.</span></span> <span data-ttu-id="869ed-114">通常，此币种是交易记录币种。</span><span class="sxs-lookup"><span data-stu-id="869ed-114">Typically, this currency is the transaction currency.</span></span> <span data-ttu-id="869ed-115">会计和申报币种金额作为子分类帐会计的一部分生成。</span><span class="sxs-lookup"><span data-stu-id="869ed-115">Accounting and reporting currency amounts are generated as part of subledger accounting.</span></span>
    -   <span data-ttu-id="869ed-116">分配显示会计日期和会计事件。</span><span class="sxs-lookup"><span data-stu-id="869ed-116">The distributions display the accounting date and accounting event.</span></span> <span data-ttu-id="869ed-117">通常，会计事件设置为 **无**，直到凭证已过帐/记入日记帐。</span><span class="sxs-lookup"><span data-stu-id="869ed-117">Typically, the accounting event is set to **None** until the document is posted/journalized.</span></span> <span data-ttu-id="869ed-118">此时，会计事件将变为 **原始**。</span><span class="sxs-lookup"><span data-stu-id="869ed-118">At that point, the accounting event becomes **Original**.</span></span> <span data-ttu-id="869ed-119">在分配过帐后，就不能修改分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-119">After the distributions have been posted, you can't modify the distributions.</span></span>
    -   <span data-ttu-id="869ed-120">**分解** 按钮可以针对父分配启用。</span><span class="sxs-lookup"><span data-stu-id="869ed-120">**Split** button might be enabled for parent distributions.</span></span> <span data-ttu-id="869ed-121">**分解** 生成新的会计分配，并且，分解可以基于百分比、金额或数量。</span><span class="sxs-lookup"><span data-stu-id="869ed-121">**Split** generates new accounting distributions, and the split can be based on percentage, amount, or quantity.</span></span>
    -   <span data-ttu-id="869ed-122">**平均分配** 按钮可以与 **分解** 结合使用来在所有分配之间自动平均分配金额。</span><span class="sxs-lookup"><span data-stu-id="869ed-122">The **Distribute equally** button can be used in combination with **Split** to automatically allocate the amount equally across all distributions.</span></span>
    -   <span data-ttu-id="869ed-123">**重置** 按钮在多个分配存在时，可以针对父分配启用。</span><span class="sxs-lookup"><span data-stu-id="869ed-123">**Reset** button might be enabled for parent distributions when more than one distribution exists.</span></span> <span data-ttu-id="869ed-124">**重置** 通过删除所有现有分配和重新生成默认分配撤消对分配的所有手动修改。</span><span class="sxs-lookup"><span data-stu-id="869ed-124">**Reset** reverses any manual modification to the distribution by deleting all existing distributions and re-generating the default distributions.</span></span>
    -   <span data-ttu-id="869ed-125">所有子分配，例如折扣、费用和销售税，始终遵循父分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-125">Any child distribution, such as discount, charge, and sales tax, always follows the parent distribution.</span></span> <span data-ttu-id="869ed-126">您可以在 **引用** &gt; **父信息** 查看父/子关系。</span><span class="sxs-lookup"><span data-stu-id="869ed-126">You can view the parent/child relation at **Reference** &gt; **Parent information**.</span></span>
    -   <span data-ttu-id="869ed-127">主科目和财务维度还可能对子项是可编辑的。</span><span class="sxs-lookup"><span data-stu-id="869ed-127">The main account and financial dimension might also be editable for children.</span></span>
    -   <span data-ttu-id="869ed-128">会计分配的财务维度按照凭证可扩展的默认模式。</span><span class="sxs-lookup"><span data-stu-id="869ed-128">The financial dimensions on the accounting distributions follow a defaulting pattern that a document can extended.</span></span>
    -   <span data-ttu-id="869ed-129">差异匹配可能在匹配方案中生成，例如供应商发票和采购订单之间的匹配。</span><span class="sxs-lookup"><span data-stu-id="869ed-129">Variance distributions might be generated in matching scenarios, such as matching between a vendor invoice and a purchase order.</span></span> <span data-ttu-id="869ed-130">您可以在 **引用** &gt; **凭证信息** 中查看会计分配之间的匹配关系。</span><span class="sxs-lookup"><span data-stu-id="869ed-130">You can view the matching relations between accounting distribution at **Reference** &gt; **Document information**.</span></span>
    -   <span data-ttu-id="869ed-131">**更正** 按钮显示并针对支持更正的凭证启用。</span><span class="sxs-lookup"><span data-stu-id="869ed-131">**Correct** button appears and is enabled for documents that support corrections.</span></span> <span data-ttu-id="869ed-132">**更正** 创建新的分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-132">**Correct** creates new distributions.</span></span> <span data-ttu-id="869ed-133">首先，创建撤消原始分配的分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-133">First, distributions are created that reverse the original distributions.</span></span> <span data-ttu-id="869ed-134">不能修改这些分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-134">These distributions can't be modified.</span></span> <span data-ttu-id="869ed-135">接下来，创建新的正确会计分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-135">Next, new correct accounting distributions are created.</span></span> <span data-ttu-id="869ed-136">如果原始分配无法修改，这些分配可以修改。</span><span class="sxs-lookup"><span data-stu-id="869ed-136">These distributions can be modified if the original distributions could be modified.</span></span>
    -   <span data-ttu-id="869ed-137">当行与项目关联时，**项目详细信息** 按钮作为扩展启用。</span><span class="sxs-lookup"><span data-stu-id="869ed-137">The **Project details** button is enabled as an extension when a line is related to a project.</span></span> <span data-ttu-id="869ed-138">项目会计分配可以修改详细信息，例如融资来源和记录属性。</span><span class="sxs-lookup"><span data-stu-id="869ed-138">Project accounting distributions let you modify details such as the funding source and line property.</span></span>
    -   <span data-ttu-id="869ed-139">您可以在 **引用** 中查看当前凭证会计状态。</span><span class="sxs-lookup"><span data-stu-id="869ed-139">You can view the current document accounting status in **Reference**.</span></span> <span data-ttu-id="869ed-140">状态针对整个凭证，并指示凭证是在进行中或已完成。</span><span class="sxs-lookup"><span data-stu-id="869ed-140">The status is for the entire document, and indicates whether the document is in process or completed.</span></span>
-   <span data-ttu-id="869ed-141">**查看分配** – 查看凭证中所有行和货币金额的会计分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-141">**View distributions** – View the accounting distributions for all lines and monetary amounts on the document.</span></span> <span data-ttu-id="869ed-142">您无法从此视图修改会计分配。</span><span class="sxs-lookup"><span data-stu-id="869ed-142">You can't modify the accounting distributions from this view.</span></span>

<span data-ttu-id="869ed-143">在版本 10.0.13 中，添加了一项功能，可以验证会计分配表以确保正确设置新字段。</span><span class="sxs-lookup"><span data-stu-id="869ed-143">In version 10.0.13, a feature has been added that validates the accounting distribution table to ensure that new fields are properly set up.</span></span> <span data-ttu-id="869ed-144">此功能称为 **使用原始凭证会计框架对凭证数据进行附加验证**。</span><span class="sxs-lookup"><span data-stu-id="869ed-144">This feature is called **Enable additional validation of data for documents using the source document accounting framework**.</span></span> <span data-ttu-id="869ed-145">要使用此功能，必须使用 **功能管理** 工作区启用它。</span><span class="sxs-lookup"><span data-stu-id="869ed-145">To use the feature, you must enable it using the **Feature management** workspace.</span></span> <span data-ttu-id="869ed-146">要启用此功能，请在 **功能管理** 页的 **搜索** 字段中搜索功能名称，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="869ed-146">To enable the feature, search for the feature name in the **Search** field on the **Feature management** page, and then select **Enable now**.</span></span>

<span data-ttu-id="869ed-147">有关详细信息，请参阅[会计分配和供应商的子分类日记帐条目](accounting-distributions-subledger-journal-entries-vendor-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="869ed-147">For more information, see [Accounting distributions and subledger journal entries for vendor invoices](accounting-distributions-subledger-journal-entries-vendor-invoices.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]