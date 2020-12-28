---
title: 审计策略违规记录和案例
description: 本文说明如何从审计政策规则违规生成审计案例。 它还包括有关审计策略使用文档选择日期范围的各个方式的信息。
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d14894d331037033b27fac3fd7ff98c5521eaf98
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440712"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="6b2c7-104">审计策略违规记录和案例</span><span class="sxs-lookup"><span data-stu-id="6b2c7-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b2c7-105">本文说明如何从审计政策规则违规生成审计案例。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="6b2c7-106">它还包括有关审计策略使用文档选择日期范围的各个方式的信息。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="6b2c7-107">审核案例如何生成</span><span class="sxs-lookup"><span data-stu-id="6b2c7-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="6b2c7-108">审核策略用于标识不符合定义和配置为审核策略规则的业务规则的支出报表、采购订单和供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="6b2c7-109">审核策略以批处理模式运行。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="6b2c7-110">在您运行审核策略时，为该策略的一部分的任何策略规则同时运行。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="6b2c7-111">每个政策规则评估一组文档。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="6b2c7-112">政策规则选择符合文档选择日期范围且符合指定条件的那些文档。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="6b2c7-113">例如，一项策略规则可能选择有超过50.00的餐费的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="6b2c7-114">其他政策规则可能选择特定供应商可支付的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="6b2c7-115">系统会针对在一组文档中选择的各个文档生成违规记录。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="6b2c7-116">该违规记录是特定文档不符合政策规则的记录，如发票 12345。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="6b2c7-117">分组多个跟踪违反记录以及与审核案例相关。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="6b2c7-118">默认情况下，由审核策略规则分组每个审核策略的案例。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="6b2c7-119">如果您需要，可以使用 **案例分组条件** 页选择其他分组条件。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="6b2c7-120">例如，可以按项目 ID 分组这些费用标题和按供应商帐户分组供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="6b2c7-121">在此情况下，具有相同的项目 ID 的所有支出标题违反在同一案例分组，以及具有相同供应商帐户的所有供应商发票在同一案例分组。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="6b2c7-122">对于基于 **重复** 查询类型的审核政策规则，违规记录不由政策规则或在 **案例分组条件** 页指定的条件分组。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="6b2c7-123">相反，由建立到审核策略规则的条件对它们进行分组。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="6b2c7-124">例如，如果策略规则评估相同金额、商人 ID 和日期的副本支出的支出报表，在这些字段中具有相同值的所有费用是一个情况。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="6b2c7-125">具有不同值的所有支出将作为单独案例。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="6b2c7-126">在审计案例生成后，使用案例管理的典型流程处理。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="6b2c7-127">文档选择日期范围</span><span class="sxs-lookup"><span data-stu-id="6b2c7-127">Document selection date ranges</span></span>
<span data-ttu-id="6b2c7-128">在运行审计策略时，每个策略规则选择具有在文档选择日期范围的一个日期的指定类型的文档。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="6b2c7-129">在 **附加选项** 页指定文档选择日期范围。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="6b2c7-130">许多文档具有多个与它们相关的日期。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="6b2c7-131">审核政策规则使用的日期字段在 **政策规则类型** 页上指定。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="6b2c7-132">这是一些审计策略使用文档选择日期范围的其他方式：</span><span class="sxs-lookup"><span data-stu-id="6b2c7-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="6b2c7-133">策略使用在文档选择日期范围的最后一天有效的每个策略规则的版本。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="6b2c7-134">可以在 **审计策略** 列表页查看每个政策规则的生效日期。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="6b2c7-135">策略使用与在单据选择日期范围的最后一天的策略相关的组织节点。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="6b2c7-136">当前与策略相关的组织节点仅在 **审计策略** 列表页中显示。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="6b2c7-137">对于基于 **列表搜索** 查询类型的策略规则，策略会评估在文档选择日期范围的最后一天有效的已监视实体的文件。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="6b2c7-138">有关类别策略规则的详细信息，请参阅[审计策略规则](audit-policy-rules.md) 。</span><span class="sxs-lookup"><span data-stu-id="6b2c7-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



