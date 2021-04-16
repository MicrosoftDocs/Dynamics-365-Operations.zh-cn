---
title: 试算平衡表财务报表
description: 本文介绍试算平衡表的默认报表。 它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a9902471101b752c4b09d8ae28eb673743b7a53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816923"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="504f6-104">试算平衡表财务报表</span><span class="sxs-lookup"><span data-stu-id="504f6-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="504f6-105">本文介绍试算平衡表的默认报表。</span><span class="sxs-lookup"><span data-stu-id="504f6-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="504f6-106">它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="504f6-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="504f6-107">默认试算平衡表</span><span class="sxs-lookup"><span data-stu-id="504f6-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="504f6-108">三个试算平衡表可用于财务报表。</span><span class="sxs-lookup"><span data-stu-id="504f6-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="504f6-109">默认报表</span><span class="sxs-lookup"><span data-stu-id="504f6-109">Default report</span></span>                                 | <span data-ttu-id="504f6-110">作用</span><span class="sxs-lookup"><span data-stu-id="504f6-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="504f6-111">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="504f6-112">提供所有帐户的余额信息，包括借方和贷方余额，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。</span><span class="sxs-lookup"><span data-stu-id="504f6-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="504f6-113">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="504f6-114">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有其净差额。</span><span class="sxs-lookup"><span data-stu-id="504f6-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="504f6-115">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="504f6-116">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有当年和过去一年的净差额。</span><span class="sxs-lookup"><span data-stu-id="504f6-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="504f6-117">构建基块</span><span class="sxs-lookup"><span data-stu-id="504f6-117">Building blocks</span></span>
<span data-ttu-id="504f6-118">试算平衡表财务报表使用以下构建基块。</span><span class="sxs-lookup"><span data-stu-id="504f6-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="504f6-119">默认报表</span><span class="sxs-lookup"><span data-stu-id="504f6-119">Default report</span></span>                                 | <span data-ttu-id="504f6-120">行定义</span><span class="sxs-lookup"><span data-stu-id="504f6-120">Row definition</span></span>          | <span data-ttu-id="504f6-121">列定义</span><span class="sxs-lookup"><span data-stu-id="504f6-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="504f6-122">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="504f6-123">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-123">Trial Balance - Default</span></span> | <span data-ttu-id="504f6-124">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="504f6-125">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="504f6-126">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-126">Trial Balance - Default</span></span> | <span data-ttu-id="504f6-127">试算平衡表汇总 - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="504f6-128">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="504f6-129">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-129">Trial Balance - Default</span></span> | <span data-ttu-id="504f6-130">各年汇总试算余额表 - 默认</span><span class="sxs-lookup"><span data-stu-id="504f6-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="504f6-131">行定义</span><span class="sxs-lookup"><span data-stu-id="504f6-131">Row definition</span></span>

<span data-ttu-id="504f6-132">行定义，试算平衡表 – 默认，包含拉取所有主科目的单行</span><span class="sxs-lookup"><span data-stu-id="504f6-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="504f6-133">因此，任何人都可以生成报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="504f6-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="504f6-134">在您查看报表时，您深化到单个行可以查看有关每个科目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="504f6-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="504f6-135">您可以修改行定义，以便包括更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="504f6-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="504f6-136">若要修改“试算平衡表 – 默认”行定义，以便包括所有科目的行，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="504f6-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="504f6-137">单击 **编辑**，然后单击 **从维度插入行**。</span><span class="sxs-lookup"><span data-stu-id="504f6-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="504f6-138">**从维度插入行** 命令允许您选择希望哪些维度在您的行定义中。</span><span class="sxs-lookup"><span data-stu-id="504f6-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="504f6-139">对于此行定义，则使用 **主科目**。</span><span class="sxs-lookup"><span data-stu-id="504f6-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="504f6-140">确保 **主科目** 包含所有符号 (&)，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="504f6-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="504f6-141">行定义现在包含默认法人的所有主科目。</span><span class="sxs-lookup"><span data-stu-id="504f6-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="504f6-142">列定义</span><span class="sxs-lookup"><span data-stu-id="504f6-142">Column definition</span></span>

<span data-ttu-id="504f6-143">每个试算平衡表使用不同的列定义。</span><span class="sxs-lookup"><span data-stu-id="504f6-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="504f6-144">这些列定义包含不同的列类型以提供不同级别的详细信息和财务数据。</span><span class="sxs-lookup"><span data-stu-id="504f6-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="504f6-145">**试算平衡表 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="504f6-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="504f6-146">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="504f6-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="504f6-147">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="504f6-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="504f6-148">**ATTR (3)** – 属性：</span><span class="sxs-lookup"><span data-stu-id="504f6-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="504f6-149">交易记录日期</span><span class="sxs-lookup"><span data-stu-id="504f6-149">Transaction Date</span></span>
        -   <span data-ttu-id="504f6-150">凭证</span><span class="sxs-lookup"><span data-stu-id="504f6-150">Voucher</span></span>
        -   <span data-ttu-id="504f6-151">日记帐描述</span><span class="sxs-lookup"><span data-stu-id="504f6-151">Journal Description</span></span>
    -   <span data-ttu-id="504f6-152">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="504f6-153">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="504f6-154">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="504f6-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="504f6-155">**试算平衡表汇总 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="504f6-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="504f6-156">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="504f6-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="504f6-157">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="504f6-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="504f6-158">**ATTR** – 属性：</span><span class="sxs-lookup"><span data-stu-id="504f6-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="504f6-159">凭证</span><span class="sxs-lookup"><span data-stu-id="504f6-159">Voucher</span></span>
    -   <span data-ttu-id="504f6-160">**FD** – 期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="504f6-161">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="504f6-162">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="504f6-163">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="504f6-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="504f6-164">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="504f6-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="504f6-165">**各年汇总试算余额表 – 默认：**</span><span class="sxs-lookup"><span data-stu-id="504f6-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="504f6-166">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="504f6-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="504f6-167">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="504f6-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="504f6-168">**ATTR** – 属性</span><span class="sxs-lookup"><span data-stu-id="504f6-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="504f6-169">凭证</span><span class="sxs-lookup"><span data-stu-id="504f6-169">Voucher</span></span>
    -   <span data-ttu-id="504f6-170">**FD** – 当前年度的期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="504f6-171">**FD** – 只包含当前年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="504f6-172">**FD** – 只包含当前年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="504f6-173">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="504f6-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="504f6-174">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="504f6-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="504f6-175">**FD** – 只包含上一年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="504f6-176">**FD** – 只包含上一年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="504f6-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="504f6-177">其他资源</span><span class="sxs-lookup"><span data-stu-id="504f6-177">Additional resources</span></span>
--------

[<span data-ttu-id="504f6-178">财务报告概览</span><span class="sxs-lookup"><span data-stu-id="504f6-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="504f6-179">查看财务报表</span><span class="sxs-lookup"><span data-stu-id="504f6-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="504f6-180">Dynamics 财务申报博客</span><span class="sxs-lookup"><span data-stu-id="504f6-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]