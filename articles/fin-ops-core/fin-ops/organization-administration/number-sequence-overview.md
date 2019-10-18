---
title: 编号规则概览
description: 编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。
author: MargoC
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c036a6bf315ddb4df93c43bb3aa2b9370c7fba36
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190066"
---
# <a name="number-sequences-overview"></a><span data-ttu-id="7a8b5-103">编号规则概览</span><span class="sxs-lookup"><span data-stu-id="7a8b5-103">Number sequences overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a8b5-104">编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="7a8b5-105">需要标识符的主数据记录或交易记录称为 *“参考”*。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="7a8b5-106">在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="7a8b5-107">我们建议您使用**组织管理**中的页面来设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="7a8b5-108">如果需要特定模块设置，您可以使用模块中的参数页面为该模块的参考指定编号规则。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="7a8b5-109">例如，在**应收账款**和**应付账款**中，可以设置编号规则组分配特定编号规则指定客户或供应商。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span>

<span data-ttu-id="7a8b5-110">在您设置编号规则时，必须指定“范围”，定义组织使用编号规则。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="7a8b5-111">该范围内可以是**共享**、**公司**、**法人**或**运营单位**。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="7a8b5-112">**法人**和**公司**范围可以与**会计日历期间**合并以创建更特定编号规则。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span>

<span data-ttu-id="7a8b5-113">编号规则格式包括段落。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="7a8b5-114">使用一个范围的编号规则而不是**共享**可以包含与该范围对应的段落。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="7a8b5-115">例如，具有**法人**范围的编号规则可能包含法人段落。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="7a8b5-116">通过包括编号规则格式的范围段落，您可以通过查看其编号标识特定记录的范围。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span>

<span data-ttu-id="7a8b5-117">除了对应于范围的段落，则编号规则格式可以包含**常量**和**字母数字**段。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="7a8b5-118">**常量**段包含不更改的一组字母，数字或符号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="7a8b5-119">**字母数字**段包含一组使用编号且递增的字母或数字。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="7a8b5-120">使用数字标志 ()\# 表示递增的编号，使用符号（&）表示递增的字母。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="7a8b5-121">例如，格式 \#\#\#\#\#\_2017 创建序列 00001\_2017、00002\_2017 等。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

## <a name="number-sequence-examples"></a><span data-ttu-id="7a8b5-122">编号规则示例</span><span class="sxs-lookup"><span data-stu-id="7a8b5-122">Number sequence examples</span></span>

<span data-ttu-id="7a8b5-123">以下示例说明如何使用段创建编号规则格式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="7a8b5-124">特别是，示例演示使用范围段落的影响。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="7a8b5-125">支出报表编号</span><span class="sxs-lookup"><span data-stu-id="7a8b5-125">Expense report numbers</span></span>

<span data-ttu-id="7a8b5-126">在以下示例中，支出报表编号可以为标题为**电缆装运**的法人设置。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span>

- <span data-ttu-id="7a8b5-127">**区域：** 出差和费用</span><span class="sxs-lookup"><span data-stu-id="7a8b5-127">**Area:** Travel and expense</span></span>
- <span data-ttu-id="7a8b5-128">**参考：** 支出报表编号</span><span class="sxs-lookup"><span data-stu-id="7a8b5-128">**Reference:** Expense report number</span></span>
- <span data-ttu-id="7a8b5-129">**作用域：** 法人</span><span class="sxs-lookup"><span data-stu-id="7a8b5-129">**Scope:** Legal entity</span></span>
- <span data-ttu-id="7a8b5-130">**法人：** CS</span><span class="sxs-lookup"><span data-stu-id="7a8b5-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="7a8b5-131">细分市场</span><span class="sxs-lookup"><span data-stu-id="7a8b5-131">Segments</span></span>  | <span data-ttu-id="7a8b5-132">段类型</span><span class="sxs-lookup"><span data-stu-id="7a8b5-132">Segment type</span></span> | <span data-ttu-id="7a8b5-133">值</span><span class="sxs-lookup"><span data-stu-id="7a8b5-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="7a8b5-134">段落 1</span><span class="sxs-lookup"><span data-stu-id="7a8b5-134">Segment 1</span></span> | <span data-ttu-id="7a8b5-135">法人</span><span class="sxs-lookup"><span data-stu-id="7a8b5-135">Legal entity</span></span> | <span data-ttu-id="7a8b5-136">CS</span><span class="sxs-lookup"><span data-stu-id="7a8b5-136">CS</span></span>        |
| <span data-ttu-id="7a8b5-137">段落 2</span><span class="sxs-lookup"><span data-stu-id="7a8b5-137">Segment 2</span></span> | <span data-ttu-id="7a8b5-138">定额</span><span class="sxs-lookup"><span data-stu-id="7a8b5-138">Constant</span></span>     | <span data-ttu-id="7a8b5-139">支出</span><span class="sxs-lookup"><span data-stu-id="7a8b5-139">-EXPENSE-</span></span> |
| <span data-ttu-id="7a8b5-140">段落 3</span><span class="sxs-lookup"><span data-stu-id="7a8b5-140">Segment 3</span></span> | <span data-ttu-id="7a8b5-141">字母数字</span><span class="sxs-lookup"><span data-stu-id="7a8b5-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="7a8b5-142">**格式编号的示例**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="7a8b5-142">**Example of formatted number**: CS-EXPENSE-0039</span></span>

<span data-ttu-id="7a8b5-143">您可以设置其他法人的类似的编号规则格式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="7a8b5-144">例如，对于称作**RW**的法人，如果您只更改法人段落的值，该格式的编号是 RW-EXPENSE-0039。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="7a8b5-145">您还可以更改其他法人的整数规则格式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="7a8b5-146">例如，您可以省略法人范围段落创建一个格式的编号，例如 Exp-0001。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="7a8b5-147">销售订单编号</span><span class="sxs-lookup"><span data-stu-id="7a8b5-147">Sales order numbers</span></span>

<span data-ttu-id="7a8b5-148">在以下示例中，销售订单编号为公司 ID**CEU**设置。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span>

- <span data-ttu-id="7a8b5-149">**区域：** 销售</span><span class="sxs-lookup"><span data-stu-id="7a8b5-149">**Area:** Sales</span></span>
- <span data-ttu-id="7a8b5-150">**参考：** 销售订单</span><span class="sxs-lookup"><span data-stu-id="7a8b5-150">**Reference:** Sales order</span></span>
- <span data-ttu-id="7a8b5-151">**作用域：** 公司</span><span class="sxs-lookup"><span data-stu-id="7a8b5-151">**Scope:** Company</span></span>
- <span data-ttu-id="7a8b5-152">**公司：** CEU</span><span class="sxs-lookup"><span data-stu-id="7a8b5-152">**Company:** CEU</span></span>

| <span data-ttu-id="7a8b5-153">细分市场</span><span class="sxs-lookup"><span data-stu-id="7a8b5-153">Segments</span></span>  | <span data-ttu-id="7a8b5-154">段落类型</span><span class="sxs-lookup"><span data-stu-id="7a8b5-154">Segment type</span></span> | <span data-ttu-id="7a8b5-155">值</span><span class="sxs-lookup"><span data-stu-id="7a8b5-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="7a8b5-156">段落 1</span><span class="sxs-lookup"><span data-stu-id="7a8b5-156">Segment 1</span></span> | <span data-ttu-id="7a8b5-157">定额</span><span class="sxs-lookup"><span data-stu-id="7a8b5-157">Constant</span></span>     | <span data-ttu-id="7a8b5-158">SO-</span><span class="sxs-lookup"><span data-stu-id="7a8b5-158">SO-</span></span>      |
| <span data-ttu-id="7a8b5-159">段落 2</span><span class="sxs-lookup"><span data-stu-id="7a8b5-159">Segment 2</span></span> | <span data-ttu-id="7a8b5-160">字母数字</span><span class="sxs-lookup"><span data-stu-id="7a8b5-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="7a8b5-161">**格式的编号的示例**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="7a8b5-161">**Example of formatted number**: SO-0029</span></span>

<span data-ttu-id="7a8b5-162">即使范围段落不包括在格式中，每个公司 ID 重新启动编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="7a8b5-163">如果为所有公司 ID 使用相同的格式，在每个公司使用相同的编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="7a8b5-164">例如，在每个公司使用销售订单编号 SO-0029。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="7a8b5-165">您还可以更改其他公司 IDs 的整数规则格式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="7a8b5-166">采购申请编号</span><span class="sxs-lookup"><span data-stu-id="7a8b5-166">Purchase requisition numbers</span></span>

<span data-ttu-id="7a8b5-167">在以下示例中，采购申请编号是组织范围的。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-167">In the following example, purchase requisition numbers are organization-wide.</span></span>

- <span data-ttu-id="7a8b5-168">**区域：** 采购</span><span class="sxs-lookup"><span data-stu-id="7a8b5-168">**Area:** Purchase</span></span>
- <span data-ttu-id="7a8b5-169">**参考：** 采购申请</span><span class="sxs-lookup"><span data-stu-id="7a8b5-169">**Reference:** Purchase requisition</span></span>
- <span data-ttu-id="7a8b5-170">**作用域：** 共享</span><span class="sxs-lookup"><span data-stu-id="7a8b5-170">**Scope:** Shared</span></span>

| <span data-ttu-id="7a8b5-171">细分市场</span><span class="sxs-lookup"><span data-stu-id="7a8b5-171">Segments</span></span>  | <span data-ttu-id="7a8b5-172">段落类型</span><span class="sxs-lookup"><span data-stu-id="7a8b5-172">Segment type</span></span> | <span data-ttu-id="7a8b5-173">值</span><span class="sxs-lookup"><span data-stu-id="7a8b5-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="7a8b5-174">段落 1</span><span class="sxs-lookup"><span data-stu-id="7a8b5-174">Segment 1</span></span> | <span data-ttu-id="7a8b5-175">定额</span><span class="sxs-lookup"><span data-stu-id="7a8b5-175">Constant</span></span>     | <span data-ttu-id="7a8b5-176">需求</span><span class="sxs-lookup"><span data-stu-id="7a8b5-176">Req</span></span>      |
| <span data-ttu-id="7a8b5-177">段落 2</span><span class="sxs-lookup"><span data-stu-id="7a8b5-177">Segment 2</span></span> | <span data-ttu-id="7a8b5-178">字母数字</span><span class="sxs-lookup"><span data-stu-id="7a8b5-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="7a8b5-179">**格式的编号的示例**: Req0052</span><span class="sxs-lookup"><span data-stu-id="7a8b5-179">**Example of formatted number**: Req0052</span></span>

<span data-ttu-id="7a8b5-180">因为作用域是**共享**，因此编号规则格式在整个组织中使用。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="7a8b5-181">不能为组织的不同部分设置不同的编号规则格式。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-181">You cannot set up different number sequence formats for different parts of the organization.</span></span>

## <a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="7a8b5-182">编号规则的绩效注意事项</span><span class="sxs-lookup"><span data-stu-id="7a8b5-182">Performance considerations for number sequences</span></span>

<span data-ttu-id="7a8b5-183">考虑有关编号规则的配置如何在设置编号规则之前影响系统性能的以下信息。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="7a8b5-184">连续和间断的编号规则</span><span class="sxs-lookup"><span data-stu-id="7a8b5-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="7a8b5-185">编号规则可以是连续的或间断的。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="7a8b5-186">连续的编号规则无法跳过所有数字，但是，不能连续使用编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="7a8b5-187">某一间断编号规则的编号可以连续使用，但编号规则可以跳过编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="7a8b5-188">例如，如果用户取消交易记录，生成编号，但不使用。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="7a8b5-189">在一个连续编号规则，以后回收该编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="7a8b5-190">在一间断的编号规则，不使用该编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-190">In a non-continuous number sequence, the number is not used.</span></span>

<span data-ttu-id="7a8b5-191">连续编号规则通常是外部文档必需的，如采购订单、销售订单和发票。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="7a8b5-192">但是，连续编号规则可以冲销影响系统响应时间，因为系统必须每次从创建新文档或记录的数据库请求一个编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span>

<span data-ttu-id="7a8b5-193">如果您使用间断的编号规则，您可以在**编号规则**页的**性能**快速选项卡上启用**预分配**。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="7a8b5-194">当您指定编号数量预分配时，系统选择这些编号和在内存中存储它们。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="7a8b5-195">在使用了预分配的数量之后，新编号只从数据库请求。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span>

<span data-ttu-id="7a8b5-196">除非有一个管理要求您使用连续编号规则，我们建议您为更好的性能使用间断的编号规则。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="7a8b5-197">编号规则自动清除</span><span class="sxs-lookup"><span data-stu-id="7a8b5-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="7a8b5-198">如果电源故障、应用程序错误，或者其他意外故障的情况下，系统不能为连续编号规则自动回收编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="7a8b5-199">您可以运行清除流程手动或自动恢复丢失的编号。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span>

<span data-ttu-id="7a8b5-200">当您计划清除过程时，应仔细考虑服务器使用。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="7a8b5-201">我们建议您将清除作为批处理作业在非高峰期间执行。</span><span class="sxs-lookup"><span data-stu-id="7a8b5-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>
