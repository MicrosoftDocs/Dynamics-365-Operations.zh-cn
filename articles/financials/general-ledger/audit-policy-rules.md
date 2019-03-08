---
title: 审计策略规则
description: 您可以使用审核策略对支出报告、供应商发票和采购订单做出评估，从而确保它们都符合您所创建的策略规则。 根据您指定的作业安排，所有与审计策略相关的规则都是以批模式运行的。  每个策略过账都是某个策略规则类型的实例。 对于每个策略规则类型，一次仅有一个策略规则可以有效。
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18b8a1649a26ebacc34b828ed25ec9646dd438a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "310223"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="7d310-106">审计策略规则</span><span class="sxs-lookup"><span data-stu-id="7d310-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d310-107">您可以使用审核策略对支出报告、供应商发票和采购订单做出评估，从而确保它们都符合您所创建的策略规则。</span><span class="sxs-lookup"><span data-stu-id="7d310-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="7d310-108">根据您指定的作业安排，所有与审计策略相关的规则都是以批模式运行的。</span><span class="sxs-lookup"><span data-stu-id="7d310-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="7d310-109">每个策略过账都是某个策略规则类型的实例。</span><span class="sxs-lookup"><span data-stu-id="7d310-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="7d310-110">对于每个策略规则类型，一次仅有一个策略规则可以有效。</span><span class="sxs-lookup"><span data-stu-id="7d310-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="7d310-111">查询和查询类型</span><span class="sxs-lookup"><span data-stu-id="7d310-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="7d310-112">当您创建了审核策略规则时，您要首先选择一个策略规则类型。</span><span class="sxs-lookup"><span data-stu-id="7d310-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="7d310-113">该策略规则类型指定 Application Object Tree (AOT) 查询用作创建策略规则的起点。</span><span class="sxs-lookup"><span data-stu-id="7d310-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="7d310-114">它还指定用于策略规则的查询类型。</span><span class="sxs-lookup"><span data-stu-id="7d310-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="7d310-115">该查询确定了策略规则进行评估的原始凭证。</span><span class="sxs-lookup"><span data-stu-id="7d310-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="7d310-116">它还指定了原始凭证中选择文件供审核时使用的标识法人和日期的字段。</span><span class="sxs-lookup"><span data-stu-id="7d310-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="7d310-117">查询类型控制查询页和“审计策略规则”页中的默认字段。</span><span class="sxs-lookup"><span data-stu-id="7d310-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="7d310-118">下表显示了对审核策略规则可用的查询类型。</span><span class="sxs-lookup"><span data-stu-id="7d310-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d310-119">查询类型</span><span class="sxs-lookup"><span data-stu-id="7d310-119">Query type</span></span></th>
<th><span data-ttu-id="7d310-120">用途</span><span class="sxs-lookup"><span data-stu-id="7d310-120">Purpose</span></span></th>
<th><span data-ttu-id="7d310-121">更多信息</span><span class="sxs-lookup"><span data-stu-id="7d310-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d310-122">条件</span><span class="sxs-lookup"><span data-stu-id="7d310-122">Conditional</span></span></td>
<td><span data-ttu-id="7d310-123">根据指定值评估原始凭证属性。</span><span class="sxs-lookup"><span data-stu-id="7d310-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d310-124">聚合</span><span class="sxs-lookup"><span data-stu-id="7d310-124">Aggregate</span></span></td>
<td><span data-ttu-id="7d310-125">根据聚合数值策略规则评估多个原始凭证或原始凭证行。</span><span class="sxs-lookup"><span data-stu-id="7d310-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d310-126">抽样</span><span class="sxs-lookup"><span data-stu-id="7d310-126">Sampling</span></span></td>
<td><span data-ttu-id="7d310-127">随机选择原始凭证的指定百分比来评估策略违规情况。</span><span class="sxs-lookup"><span data-stu-id="7d310-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="7d310-128">当您选择此选项时，使用“审计策略规则”页指定随机选择供审核凭证的百分比。</span><span class="sxs-lookup"><span data-stu-id="7d310-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d310-129">复制</span><span class="sxs-lookup"><span data-stu-id="7d310-129">Duplicate</span></span></td>
<td><span data-ttu-id="7d310-130">评估原始凭证以确定是否在指定的字段中包含重复的条目。</span><span class="sxs-lookup"><span data-stu-id="7d310-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="7d310-131">当您选择此选项时，使用“审计策略规则”页指定针对重复条目对凭证进行评估时要添加到凭证选择日期范围的天数。</span><span class="sxs-lookup"><span data-stu-id="7d310-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d310-132">列表搜索</span><span class="sxs-lookup"><span data-stu-id="7d310-132">List search</span></span></td>
<td><span data-ttu-id="7d310-133">针对特定条目评估原始凭证。</span><span class="sxs-lookup"><span data-stu-id="7d310-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="7d310-134">查询的根凭证定义了正被审核的凭证。</span><span class="sxs-lookup"><span data-stu-id="7d310-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="7d310-135">查询必须是包括 Dirpartytable 表的参考的列表查询。</span><span class="sxs-lookup"><span data-stu-id="7d310-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="7d310-136">此选项只能与以下 AOT 查询一起使用：</span><span class="sxs-lookup"><span data-stu-id="7d310-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="7d310-137"><span class="ui">AuditPolicyExpenseList</span>（支出报表监控的员工）</span><span class="sxs-lookup"><span data-stu-id="7d310-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="7d310-138"><span class="ui">AuditPolicyPurchList</span>（采购订单监控的供应商）</span><span class="sxs-lookup"><span data-stu-id="7d310-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="7d310-139"><span class="ui">AuditPolicyVendInvoiceList</span>（供应商发票监控的供应商）</span><span class="sxs-lookup"><span data-stu-id="7d310-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="7d310-140">当您选择此选项时，在“审计策略规则”页中指定要监控的实体。</span><span class="sxs-lookup"><span data-stu-id="7d310-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d310-141">关键字搜索</span><span class="sxs-lookup"><span data-stu-id="7d310-141">Keyword search</span></span></td>
<td><span data-ttu-id="7d310-142">评估原始凭证以确定它们是否包含某些特定的单词。</span><span class="sxs-lookup"><span data-stu-id="7d310-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="7d310-143">当您选择此选项时，在“审计策略规则”页中输入要查找的字词。</span><span class="sxs-lookup"><span data-stu-id="7d310-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="7d310-144">“审计策略规则”页中也包含了选项让您指定表和字段用来评估您输入的单词。</span><span class="sxs-lookup"><span data-stu-id="7d310-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="7d310-145">共同参数</span><span class="sxs-lookup"><span data-stu-id="7d310-145">Common parameters</span></span>
<span data-ttu-id="7d310-146">某个特定审核策略的所有策略规则共享相同的批处理参数和相同的凭证选择日期范围。</span><span class="sxs-lookup"><span data-stu-id="7d310-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="7d310-147">在“审计策略规则”页中为该策略指定这些参数。</span><span class="sxs-lookup"><span data-stu-id="7d310-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="7d310-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="7d310-148">Additional resources</span></span>
--------

<span data-ttu-id="7d310-149">[审计政策违规记录和案例](audit-policy-violations-cases.md)
[定义原始单据的审计策略](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="7d310-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


