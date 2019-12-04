---
title: 试算平衡表财务报表
description: 本文介绍试算平衡表的默认报表。 它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b48510febf5a5f9f4a01728b242d9750b3c62c2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771720"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="bfb92-104">试算平衡表财务报表</span><span class="sxs-lookup"><span data-stu-id="bfb92-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfb92-105">本文介绍试算平衡表的默认报表。</span><span class="sxs-lookup"><span data-stu-id="bfb92-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="bfb92-106">它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="bfb92-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="bfb92-107">默认试算平衡表</span><span class="sxs-lookup"><span data-stu-id="bfb92-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="bfb92-108">三个试算平衡表可用于财务报表。</span><span class="sxs-lookup"><span data-stu-id="bfb92-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="bfb92-109">默认报表</span><span class="sxs-lookup"><span data-stu-id="bfb92-109">Default report</span></span>                                 | <span data-ttu-id="bfb92-110">作用</span><span class="sxs-lookup"><span data-stu-id="bfb92-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb92-111">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="bfb92-112">提供所有帐户的余额信息，包括借方和贷方余额，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。</span><span class="sxs-lookup"><span data-stu-id="bfb92-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="bfb92-113">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="bfb92-114">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有其净差额。</span><span class="sxs-lookup"><span data-stu-id="bfb92-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="bfb92-115">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="bfb92-116">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有当年和过去一年的净差额。</span><span class="sxs-lookup"><span data-stu-id="bfb92-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="bfb92-117">构建基块</span><span class="sxs-lookup"><span data-stu-id="bfb92-117">Building blocks</span></span>
<span data-ttu-id="bfb92-118">试算平衡表财务报表使用以下构建基块。</span><span class="sxs-lookup"><span data-stu-id="bfb92-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="bfb92-119">默认报表</span><span class="sxs-lookup"><span data-stu-id="bfb92-119">Default report</span></span>                                 | <span data-ttu-id="bfb92-120">行定义</span><span class="sxs-lookup"><span data-stu-id="bfb92-120">Row definition</span></span>          | <span data-ttu-id="bfb92-121">列定义</span><span class="sxs-lookup"><span data-stu-id="bfb92-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="bfb92-122">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="bfb92-123">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-123">Trial Balance - Default</span></span> | <span data-ttu-id="bfb92-124">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="bfb92-125">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="bfb92-126">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-126">Trial Balance - Default</span></span> | <span data-ttu-id="bfb92-127">试算平衡表汇总 - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="bfb92-128">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="bfb92-129">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-129">Trial Balance - Default</span></span> | <span data-ttu-id="bfb92-130">各年汇总试算余额表 - 默认</span><span class="sxs-lookup"><span data-stu-id="bfb92-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="bfb92-131">行定义</span><span class="sxs-lookup"><span data-stu-id="bfb92-131">Row definition</span></span>

<span data-ttu-id="bfb92-132">行定义，试算平衡表 – 默认，包含拉取所有主科目的单行</span><span class="sxs-lookup"><span data-stu-id="bfb92-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="bfb92-133">因此，任何人都可以生成报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="bfb92-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="bfb92-134">在您查看报表时，您深化到单个行可以查看有关每个科目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bfb92-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="bfb92-135">您可以修改行定义，以便包括更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="bfb92-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="bfb92-136">若要修改“试算平衡表 – 默认”行定义，以便包括所有科目的行，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="bfb92-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="bfb92-137">单击**编辑**，然后单击**从维度插入行**。</span><span class="sxs-lookup"><span data-stu-id="bfb92-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="bfb92-138">**从维度插入行**命令允许您选择希望哪些维度在您的行定义中。</span><span class="sxs-lookup"><span data-stu-id="bfb92-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="bfb92-139">对于此行定义，则使用**主科目**。</span><span class="sxs-lookup"><span data-stu-id="bfb92-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="bfb92-140">确保**主科目**包含所有符号 (&)，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="bfb92-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="bfb92-141">行定义现在包含默认法人的所有主科目。</span><span class="sxs-lookup"><span data-stu-id="bfb92-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="bfb92-142">列定义</span><span class="sxs-lookup"><span data-stu-id="bfb92-142">Column definition</span></span>

<span data-ttu-id="bfb92-143">每个试算平衡表使用不同的列定义。</span><span class="sxs-lookup"><span data-stu-id="bfb92-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="bfb92-144">这些列定义包含不同的列类型以提供不同级别的详细信息和财务数据。</span><span class="sxs-lookup"><span data-stu-id="bfb92-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="bfb92-145">**试算平衡表 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="bfb92-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="bfb92-146">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="bfb92-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="bfb92-147">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="bfb92-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="bfb92-148">**ATTR (3)** – 属性：</span><span class="sxs-lookup"><span data-stu-id="bfb92-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="bfb92-149">交易记录日期</span><span class="sxs-lookup"><span data-stu-id="bfb92-149">Transaction Date</span></span>
        -   <span data-ttu-id="bfb92-150">凭证</span><span class="sxs-lookup"><span data-stu-id="bfb92-150">Voucher</span></span>
        -   <span data-ttu-id="bfb92-151">日记帐描述</span><span class="sxs-lookup"><span data-stu-id="bfb92-151">Journal Description</span></span>
    -   <span data-ttu-id="bfb92-152">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="bfb92-153">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="bfb92-154">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="bfb92-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="bfb92-155">**试算平衡表汇总 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="bfb92-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="bfb92-156">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="bfb92-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="bfb92-157">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="bfb92-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="bfb92-158">**ATTR** – 属性：</span><span class="sxs-lookup"><span data-stu-id="bfb92-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="bfb92-159">凭证</span><span class="sxs-lookup"><span data-stu-id="bfb92-159">Voucher</span></span>
    -   <span data-ttu-id="bfb92-160">**FD** – 期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="bfb92-161">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="bfb92-162">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="bfb92-163">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="bfb92-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="bfb92-164">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="bfb92-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="bfb92-165">**各年汇总试算余额表 – 默认：**</span><span class="sxs-lookup"><span data-stu-id="bfb92-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="bfb92-166">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="bfb92-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="bfb92-167">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="bfb92-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="bfb92-168">**ATTR** – 属性</span><span class="sxs-lookup"><span data-stu-id="bfb92-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="bfb92-169">凭证</span><span class="sxs-lookup"><span data-stu-id="bfb92-169">Voucher</span></span>
    -   <span data-ttu-id="bfb92-170">**FD** – 当前年度的期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="bfb92-171">**FD** – 只包含当前年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="bfb92-172">**FD** – 只包含当前年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="bfb92-173">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="bfb92-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="bfb92-174">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="bfb92-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="bfb92-175">**FD** – 只包含上一年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="bfb92-176">**FD** – 只包含上一年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="bfb92-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="bfb92-177">其他资源</span><span class="sxs-lookup"><span data-stu-id="bfb92-177">Additional resources</span></span>
--------

[<span data-ttu-id="bfb92-178">财务报告概览</span><span class="sxs-lookup"><span data-stu-id="bfb92-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="bfb92-179">查看财务报表</span><span class="sxs-lookup"><span data-stu-id="bfb92-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="bfb92-180">Dynamics 财务申报博客</span><span class="sxs-lookup"><span data-stu-id="bfb92-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



