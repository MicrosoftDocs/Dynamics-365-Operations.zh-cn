---
title: 试算平衡表财务报表
description: 本文介绍试算平衡表的默认报表。 它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。
author: jinniew
ms.date: 05/26/2021
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
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103650"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="54ca8-104">试算平衡表财务报表</span><span class="sxs-lookup"><span data-stu-id="54ca8-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54ca8-105">本文介绍试算平衡表的默认报表。</span><span class="sxs-lookup"><span data-stu-id="54ca8-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="54ca8-106">它还介绍这些报表的关联构建块，以及如何修改这些报表以符合您的业务需求。</span><span class="sxs-lookup"><span data-stu-id="54ca8-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="54ca8-107">默认试算平衡表</span><span class="sxs-lookup"><span data-stu-id="54ca8-107">Default trial balance reports</span></span>

<span data-ttu-id="54ca8-108">三个试算平衡表可用于财务报表。</span><span class="sxs-lookup"><span data-stu-id="54ca8-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="54ca8-109">默认报表</span><span class="sxs-lookup"><span data-stu-id="54ca8-109">Default report</span></span>                                 | <span data-ttu-id="54ca8-110">作用</span><span class="sxs-lookup"><span data-stu-id="54ca8-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ca8-111">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="54ca8-112">提供所有帐户的余额信息，包括借方和贷方余额，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。</span><span class="sxs-lookup"><span data-stu-id="54ca8-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="54ca8-113">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="54ca8-114">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有其净差额。</span><span class="sxs-lookup"><span data-stu-id="54ca8-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="54ca8-115">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="54ca8-116">提供所有帐户的余额信息，包括期初和期末余额，以及借方和贷方余额还有当年和过去一年的净差额。</span><span class="sxs-lookup"><span data-stu-id="54ca8-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="54ca8-117">构建基块</span><span class="sxs-lookup"><span data-stu-id="54ca8-117">Building blocks</span></span>
<span data-ttu-id="54ca8-118">试算平衡表财务报表使用以下构建基块。</span><span class="sxs-lookup"><span data-stu-id="54ca8-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="54ca8-119">默认报表</span><span class="sxs-lookup"><span data-stu-id="54ca8-119">Default report</span></span>                                 | <span data-ttu-id="54ca8-120">行定义</span><span class="sxs-lookup"><span data-stu-id="54ca8-120">Row definition</span></span>          | <span data-ttu-id="54ca8-121">列定义</span><span class="sxs-lookup"><span data-stu-id="54ca8-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="54ca8-122">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="54ca8-123">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-123">Trial Balance - Default</span></span> | <span data-ttu-id="54ca8-124">试算平衡表(明细) - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="54ca8-125">试算平衡表汇总 – 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="54ca8-126">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-126">Trial Balance - Default</span></span> | <span data-ttu-id="54ca8-127">试算平衡表汇总 - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="54ca8-128">各年汇总试算余额表 – 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="54ca8-129">试算平衡表 - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-129">Trial Balance - Default</span></span> | <span data-ttu-id="54ca8-130">各年汇总试算余额表 - 默认</span><span class="sxs-lookup"><span data-stu-id="54ca8-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="54ca8-131">在 Financial Reporting 中运行 **试算平衡表** 报表时，请务必在 **设置** 选项卡中选中 **显示没有金额的行** 和 **显示没有活动行的报表** 的复选框。</span><span class="sxs-lookup"><span data-stu-id="54ca8-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="54ca8-132">行定义</span><span class="sxs-lookup"><span data-stu-id="54ca8-132">Row definition</span></span>

<span data-ttu-id="54ca8-133">行定义，试算平衡表 – 默认，包含拉取所有主科目的单行</span><span class="sxs-lookup"><span data-stu-id="54ca8-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="54ca8-134">因此，任何人都可以生成报表，而不必进行任何修改。</span><span class="sxs-lookup"><span data-stu-id="54ca8-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="54ca8-135">在您查看报表时，您深化到单个行可以查看有关每个科目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="54ca8-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="54ca8-136">您可以修改行定义，以便包括更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="54ca8-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="54ca8-137">若要修改“试算平衡表 – 默认”行定义，以便包括所有科目的行，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="54ca8-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="54ca8-138">单击 **编辑**，然后单击 **从维度插入行**。</span><span class="sxs-lookup"><span data-stu-id="54ca8-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="54ca8-139">**从维度插入行** 命令允许您选择希望哪些维度在您的行定义中。</span><span class="sxs-lookup"><span data-stu-id="54ca8-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="54ca8-140">对于此行定义，则使用 **主科目**。</span><span class="sxs-lookup"><span data-stu-id="54ca8-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="54ca8-141">确保 **主科目** 包含所有符号 (&)，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="54ca8-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="54ca8-142">行定义现在包含默认法人的所有主科目。</span><span class="sxs-lookup"><span data-stu-id="54ca8-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="54ca8-143">列定义</span><span class="sxs-lookup"><span data-stu-id="54ca8-143">Column definition</span></span>

<span data-ttu-id="54ca8-144">每个试算平衡表使用不同的列定义。</span><span class="sxs-lookup"><span data-stu-id="54ca8-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="54ca8-145">这些列定义包含不同的列类型以提供不同级别的详细信息和财务数据。</span><span class="sxs-lookup"><span data-stu-id="54ca8-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="54ca8-146">**试算平衡表 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="54ca8-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="54ca8-147">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="54ca8-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="54ca8-148">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="54ca8-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="54ca8-149">**ATTR (3)** – 属性：</span><span class="sxs-lookup"><span data-stu-id="54ca8-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="54ca8-150">交易记录日期</span><span class="sxs-lookup"><span data-stu-id="54ca8-150">Transaction Date</span></span>
        -   <span data-ttu-id="54ca8-151">凭证</span><span class="sxs-lookup"><span data-stu-id="54ca8-151">Voucher</span></span>
        -   <span data-ttu-id="54ca8-152">日记帐描述</span><span class="sxs-lookup"><span data-stu-id="54ca8-152">Journal Description</span></span>
    -   <span data-ttu-id="54ca8-153">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="54ca8-154">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="54ca8-155">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="54ca8-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="54ca8-156">**试算平衡表汇总 – 默认列类型：**</span><span class="sxs-lookup"><span data-stu-id="54ca8-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="54ca8-157">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="54ca8-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="54ca8-158">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="54ca8-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="54ca8-159">**ATTR** – 属性：</span><span class="sxs-lookup"><span data-stu-id="54ca8-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="54ca8-160">凭证</span><span class="sxs-lookup"><span data-stu-id="54ca8-160">Voucher</span></span>
    -   <span data-ttu-id="54ca8-161">**FD** – 期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="54ca8-162">**FD** – 只包含借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="54ca8-163">**FD** – 只包含贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="54ca8-164">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="54ca8-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="54ca8-165">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="54ca8-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="54ca8-166">**各年汇总试算余额表 – 默认：**</span><span class="sxs-lookup"><span data-stu-id="54ca8-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="54ca8-167">**ACCT** – 科目代码</span><span class="sxs-lookup"><span data-stu-id="54ca8-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="54ca8-168">**DESC** – 行定义的描述</span><span class="sxs-lookup"><span data-stu-id="54ca8-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="54ca8-169">**ATTR** – 属性</span><span class="sxs-lookup"><span data-stu-id="54ca8-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="54ca8-170">凭证</span><span class="sxs-lookup"><span data-stu-id="54ca8-170">Voucher</span></span>
    -   <span data-ttu-id="54ca8-171">**FD** – 当前年度的期初余额财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="54ca8-172">**FD** – 只包含当前年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="54ca8-173">**FD** – 只包含当前年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="54ca8-174">**CALC** – 净差额</span><span class="sxs-lookup"><span data-stu-id="54ca8-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="54ca8-175">**CALC** – 期末余额</span><span class="sxs-lookup"><span data-stu-id="54ca8-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="54ca8-176">**FD** – 只包含上一年度的借方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="54ca8-177">**FD** – 只包含上一年度的贷方的财务数据</span><span class="sxs-lookup"><span data-stu-id="54ca8-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54ca8-178">其他资源</span><span class="sxs-lookup"><span data-stu-id="54ca8-178">Additional resources</span></span>

[<span data-ttu-id="54ca8-179">财务报告概览</span><span class="sxs-lookup"><span data-stu-id="54ca8-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="54ca8-180">查看财务报表</span><span class="sxs-lookup"><span data-stu-id="54ca8-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="54ca8-181">Dynamics 财务申报博客</span><span class="sxs-lookup"><span data-stu-id="54ca8-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
