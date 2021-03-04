---
title: 编辑并审计现金和结转及现金管理交易记录
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计现金和结转及现金管理交易记录。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: c809f379dbd6824542d0b1768cfbf44f37461f4c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010191"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a><span data-ttu-id="fc6c4-103">编辑并审计现金和结转及现金管理交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-103">Edit and audit cash and carry and cash management transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc6c4-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计现金和结转及现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-104">This topic describes how to edit and audit cash and carry and cash management transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc6c4-105">概览</span><span class="sxs-lookup"><span data-stu-id="fc6c4-105">Overview</span></span>

<span data-ttu-id="fc6c4-106">Dynamics 365 Commerce 客户使用第一方销售点 (POS) 应用程序和第三方 POS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-106">Dynamics 365 Commerce customers use both a first-party point of sale (POS) application and third-party POS applications.</span></span> <span data-ttu-id="fc6c4-107">使用第一方应用程序时，可以通过批处理将渠道中的商店交易记录导入到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-107">In the case of the first-party application, store transactions are pulled into Commerce headquarters from the channels through a batch process.</span></span> <span data-ttu-id="fc6c4-108">使用第三方应用程序时，可以通过集成将交易记录导入到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-108">In the case of third-party applications, transactions are pulled into Commerce headquarters through integration.</span></span> <span data-ttu-id="fc6c4-109">在这两种情况下，将交易记录导入到 Commerce Headquarters 后，必须执行一致性检查过程。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-109">In both cases, after transactions are pulled into Commerce headquarters, a consistency check process must be performed.</span></span> <span data-ttu-id="fc6c4-110">此过程对交易记录执行多项验证，并且只有已成功通过验证的交易记录才会导入到报表中，以便可以在 Commerce Headquarters 中对这些交易记录进行过帐。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-110">This process runs multiple validations on the transactions, and only transactions that are successfully validated are pulled into the statement so that they can be posted in Commerce headquarters.</span></span>

<span data-ttu-id="fc6c4-111">Commerce 交易记录可能会由于各种原因而验证失败。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-111">Commerce transactions might fail validation for various reasons.</span></span> <span data-ttu-id="fc6c4-112">集成代码或 POS 应用程序中的 Bug 可能会导致数据不一致。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-112">A bug in the integration code or in the POS application might cause inconsistent data.</span></span> <span data-ttu-id="fc6c4-113">另外，用户错误也可能会导致数据不一致。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-113">Alternatively, a user error might cause inconsistent data.</span></span> <span data-ttu-id="fc6c4-114">例如，用户在产品同步到渠道后删除了该产品，或者用户未过帐会计期间的交易记录即关闭了该期间。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-114">For example, a user deletes a product after it was synced to the channel, or a user closes a fiscal period without posting transactions for that period.</span></span> <span data-ttu-id="fc6c4-115">尽管这些交易记录已标记并从对帐单中排除，但是它们会干扰客户将每日销售过账到财务的每日流程。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-115">Although these transactions are flagged and are excluded from the statements, they can disrupt a customer's daily process of posting daily sales to the financials.</span></span> <span data-ttu-id="fc6c4-116">在 Commerce 中，可以编辑验证失败的交易记录，同时还保持对所有更改的审计。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-116">In Commerce, you can edit the transactions that fail validation while you also maintain an audit of all the changes.</span></span>

## <a name="edit-transactions"></a><span data-ttu-id="fc6c4-117">编辑交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-117">Edit transactions</span></span>

<span data-ttu-id="fc6c4-118">在 Commerce 版本 10.0.5 中，可以编辑的交易记录只有现金和结转交易记录，例如销售和退货。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-118">In Commerce version 10.0.5, the only transactions that can be edited are cash and carry transactions, such as sales and returns.</span></span> <span data-ttu-id="fc6c4-119">无法编辑客户订单和在线订单。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-119">Customer orders and online orders can't be edited.</span></span> <span data-ttu-id="fc6c4-120">在 Commerce 版本 10.0.6 和更高版本中，也可以编辑现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-120">In Commerce version 10.0.6 and later, cash management transactions can also be edited.</span></span>

<span data-ttu-id="fc6c4-121">要在 Commerce Headquarters 中编辑交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-121">To edit transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fc6c4-122">安装 [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-122">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="fc6c4-123">在 Commerce Headquarters 中，打开 **商店财务** 工作区。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-123">In Commerce headquarters, open the **Store financials** workspace.</span></span> <span data-ttu-id="fc6c4-124">**交易记录验证失败** 磁贴提供在一个或多个验证规则中验证失败的交易记录页面的预筛选视图。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-124">The **Transaction validation failures** tile provides a prefiltered view of the transaction page that failed one or more validation rules.</span></span>
1. <span data-ttu-id="fc6c4-125">打开交易记录页面，选择验证失败的记录，选择 **Office 加载项**，然后选择 **编辑所选交易记录**。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-125">Open the transaction page, select the record that failed validation, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="fc6c4-126">此时将打开一个 Excel 文件，其中显示了所选交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-126">An Excel file that shows the details of the selected transaction is opened.</span></span> <span data-ttu-id="fc6c4-127">该文件包含以下工作表：</span><span class="sxs-lookup"><span data-stu-id="fc6c4-127">This file contains the following worksheets:</span></span>

    - <span data-ttu-id="fc6c4-128">**行** - 此工作表包含该交易记录的标头、产品行和相关数据。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-128">**Lines** – This worksheet has the header and product lines for the transaction, and related data for the transaction.</span></span>
    - <span data-ttu-id="fc6c4-129">**付款** - 此工作表包含该交易记录的付款行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-129">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="fc6c4-130">**折扣** - 此工作表包含该交易记录的折扣相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-130">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="fc6c4-131">**纳税** - 此工作表包含该交易记录的纳税相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-131">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="fc6c4-132">**费用** - 此工作表包含该交易记录的费用相关数据。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-132">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="fc6c4-133">在 Excel 文件中，修改相应的字段，然后使用 Dynamics Excel 加载项发布功能将数据重新上传到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-133">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="fc6c4-134">发布数据后，所做的更改将反映在系统中。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-134">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="fc6c4-135">在发布期间，将不会对用户所做的更改进行验证。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-135">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="fc6c4-136">通过选择标头级别更改的 **零售交易记录** 标头中的 **查看审计线索**，以及在相应交易记录页面的相关部分和记录中，可以查看所做更改的完整审计线索。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-136">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="fc6c4-137">例如，与销售行相关的所有更改都将显示在 **销售交易记录** 页面上，所有与付款相关的更改都将显示在 **付款交易记录** 页面上。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-137">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="fc6c4-138">将保持更改的以下审计详细信息：</span><span class="sxs-lookup"><span data-stu-id="fc6c4-138">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="fc6c4-139">修改日期和时间</span><span class="sxs-lookup"><span data-stu-id="fc6c4-139">Modified date and time</span></span>
    - <span data-ttu-id="fc6c4-140">字段</span><span class="sxs-lookup"><span data-stu-id="fc6c4-140">Field</span></span>
    - <span data-ttu-id="fc6c4-141">原值</span><span class="sxs-lookup"><span data-stu-id="fc6c4-141">Old value</span></span>
    - <span data-ttu-id="fc6c4-142">新值</span><span class="sxs-lookup"><span data-stu-id="fc6c4-142">New value</span></span>
    - <span data-ttu-id="fc6c4-143">修改者</span><span class="sxs-lookup"><span data-stu-id="fc6c4-143">Modified by</span></span>

1. <span data-ttu-id="fc6c4-144">在做出更改并发布后，请运行 **验证商店交易记录**，以验证这些更改是否一致和有效。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-144">After you've made and published your changes, run **Validate store transactions** to validate that those changes are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="fc6c4-145">只能编辑验证失败的交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-145">You can edit only transactions that failed validation.</span></span> <span data-ttu-id="fc6c4-146">如果要编辑通过验证的交易记录，请将该交易记录的验证状态更改为 **错误** 或者 **无**，然后发布该更改。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-146">If you want to edit a transaction that passed validation, change the validation status of the transaction to **Error** or **None**, and then publish the change.</span></span> <span data-ttu-id="fc6c4-147">接下来，可以编辑该交易记录的标头或者任何其他子记录中的数据，然后发布该标头或记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-147">You can then edit the data on the header or in any other child records of the transaction, and publish the header or records.</span></span>

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a><span data-ttu-id="fc6c4-148">批量编辑链接到对帐单的交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-148">Bulk-edit transactions that are linked to a statement</span></span>

<span data-ttu-id="fc6c4-149">Commerce 版本 10.0.6 及更高版本支持在对帐单级别批量编辑交易记录的选项。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-149">Commerce version 10.0.6 and later support the option to bulk-edit transactions at the statement level.</span></span>

<span data-ttu-id="fc6c4-150">要在 Commerce Headquarters 中批量编辑链接到对帐单的交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-150">To bulk-edit transactions that are linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fc6c4-151">打开 **对帐单** 页面，然后选择包含必须编辑的交易记录的对帐单。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-151">Open the **Statements** page, and select the statement that contains the transactions that must be edited.</span></span>
1. <span data-ttu-id="fc6c4-152">选择 **在 Microsoft Office 中打开** 按钮。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-152">Select the **Open in Microsoft Office** button.</span></span>
1. <span data-ttu-id="fc6c4-153">根据必须编辑的内容，选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="fc6c4-153">Depending on what must be edited, select one of the following options:</span></span>

    - <span data-ttu-id="fc6c4-154">**编辑现金和结转交易记录** - 通过此选项可以编辑对帐单中包含的所有现金和结转交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-154">**Edit cash and carry transactions** – This option lets you edit all the cash and carry transactions that are included in the statement.</span></span> <span data-ttu-id="fc6c4-155">提供了以下 Excel 工作表：</span><span class="sxs-lookup"><span data-stu-id="fc6c4-155">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="fc6c4-156">**交易记录** - 此工作表包含销售交易记录的所有标头级别信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-156">**Transaction** – This worksheet has all the header-level information for the sales transactions.</span></span>
        - <span data-ttu-id="fc6c4-157">**销售交易记录** - 此工作表包含销售交易记录的所有行级别信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-157">**Sales transaction** – This worksheet has all the line-level information for the sales transactions.</span></span>
        - <span data-ttu-id="fc6c4-158">**付款交易记录** - 此工作表包含销售交易记录的所有付款行信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-158">**Payment transactions** – This worksheet has all the payment line information for the sales transactions.</span></span>
        - <span data-ttu-id="fc6c4-159">**折扣交易记录** - 此工作表包含销售交易记录的所有折扣行信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-159">**Discount transactions** – This worksheet has all the discount line information for the sales transactions.</span></span>
        - <span data-ttu-id="fc6c4-160">**纳税交易记录** - 此工作表包含销售交易记录的所有纳税行信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-160">**Tax transactions** – This worksheet has all the tax line information for the sales transactions.</span></span>
        - <span data-ttu-id="fc6c4-161">**费用交易记录** - 此工作表包含销售交易记录的所有费用行信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-161">**Charge transactions** – This worksheet has all the charge line information for the sales transactions.</span></span>

    - <span data-ttu-id="fc6c4-162">**编辑现金管理交易记录** - 通过此选项可以编辑对帐单中包含的所有现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-162">**Edit cash management transactions** – This option lets you edit all the cash management transactions that are included in the statement.</span></span> <span data-ttu-id="fc6c4-163">提供了以下 Excel 工作表：</span><span class="sxs-lookup"><span data-stu-id="fc6c4-163">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="fc6c4-164">**交易记录** - 此工作表包含现金管理交易记录的所有标头级别信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-164">**Transaction** – This worksheet has all the header-level information for the cash management transactions.</span></span>
        - <span data-ttu-id="fc6c4-165">**银行支付交易记录** - 此工作表包含所有银行投箱交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-165">**Bank tender transactions** – This worksheet has all the bank drop transaction details.</span></span>
        - <span data-ttu-id="fc6c4-166">**金库支付交易记录** - 此工作表包含所有金库投箱交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-166">**Safe tender transactions** – This worksheet has all the safe drop transaction details.</span></span>
        - <span data-ttu-id="fc6c4-167">**钱币清点** - 此工作表包含所有钱币清点交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-167">**Tender declaration** – This worksheet has all the tender declaration transaction details.</span></span>
        - <span data-ttu-id="fc6c4-168">**收入 - 支出交易记录** - 此工作表包含所有收入 - 支出交易记录行详细信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-168">**Income-expense transaction** – This worksheet has all the income-expense transaction line details.</span></span>
        - <span data-ttu-id="fc6c4-169">**付款交易记录** - 此工作表包含 **付款账单** 操作以及收入 - 支出交易记录的所有付款相关信息。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-169">**Payment transactions** – This worksheet has all the payment-related information for the **Pay invoice** operation and the income-expense transaction.</span></span>

1. <span data-ttu-id="fc6c4-170">编辑所需交易记录。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-170">Edit the required transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fc6c4-171">发布批量编辑的交易记录时，将不会执行验证。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-171">Validations aren't done when you publish bulk-edited transactions.</span></span> <span data-ttu-id="fc6c4-172">您必须确保您的所有编辑都是准确的，并保持各工作表的数据真实可靠。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-172">You must make sure that all your edits are accurate, and that the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="fc6c4-173">例如，如果想要更改交易记录日期，以便可以管理结帐未结交易记录的会计或库存期间的方案，则您必须更改具有 **业务日期** 列的所有 Excel 工作表的日期。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-173">For example, if you want to change the transaction date, so that you can manage scenarios where the fiscal or inventory period for the open transactions is closed, you must change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="fc6c4-174">要在编辑交易记录之后对其进行验证，可以选择 **对帐单** 页面上的 **重新验证交易记录**。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-174">To validate transactions after they have been edited, you can select **Revalidate transactions** on the **Statements** page.</span></span> <span data-ttu-id="fc6c4-175">请等待验证作业运行完成，然后再过帐对帐单。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-175">Wait for the validation job to finish running before you post the statement.</span></span>

1. <span data-ttu-id="fc6c4-176">如果已经生成聚合值，请打开 **聚合交易记录** 页面，然后选择 **重新生成销售订单 xml**。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-176">If the aggregation has already been generated, open the **Aggregated transactions** page, and select **Regenerate sales order xml**.</span></span>

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a><span data-ttu-id="fc6c4-177">批量编辑未链接到对帐单的交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-177">Bulk-edit transactions that aren't linked to a statement</span></span>

<span data-ttu-id="fc6c4-178">Commerce 版本 10.0.10 及更高版本支持对验证失败但未链接到对帐单的交易记录进行批量编辑。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-178">Commerce version 10.0.10 and later support the option to bulk-edit transactions that fail validation but aren't linked to a statement.</span></span>

<span data-ttu-id="fc6c4-179">要在 Commerce Headquarters 中批量编辑未链接到对帐单的交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-179">To bulk-edit transactions that aren't linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fc6c4-180">打开 **所有商店** 页面，然后选择必须编辑其交易记录的商店。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-180">Open the **All stores** page, and select the store that transactions must be edited for.</span></span>
1. <span data-ttu-id="fc6c4-181">选择 **在 Microsoft Office 中打开** 按钮，然后选择 **编辑现金和结转交易记录**。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-181">Select the **Open in Microsoft Office** button, and then select **Edit cash and carry transactions**.</span></span>
1. <span data-ttu-id="fc6c4-182">编辑所需的交易记录，然后将其发布。</span><span class="sxs-lookup"><span data-stu-id="fc6c4-182">Edit the required transactions, and then publish them.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc6c4-183">其他资源</span><span class="sxs-lookup"><span data-stu-id="fc6c4-183">Additional resources</span></span>

[<span data-ttu-id="fc6c4-184">编辑并审计在线订单和异步客户订单交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-184">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="fc6c4-185">编辑零售交易记录的财务维度</span><span class="sxs-lookup"><span data-stu-id="fc6c4-185">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="fc6c4-186">创建 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-186">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="fc6c4-187">将字段添加到 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="fc6c4-187">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
