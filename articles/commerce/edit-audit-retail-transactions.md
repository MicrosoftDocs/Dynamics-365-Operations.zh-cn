---
title: 编辑和审计零售商店交易记录
description: 本主题将介绍用于编辑和审计商店交易记录的功能。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004381"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="dead4-103">编辑和审计零售商店交易记录</span><span class="sxs-lookup"><span data-stu-id="dead4-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="dead4-104">Dynamics 365 Commerce 客户使用第一方和第三方销售点 (POS) 应用程序。</span><span class="sxs-lookup"><span data-stu-id="dead4-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="dead4-105">借助第一方 POS 应用程序，可以通过批处理将渠道中的商店交易记录导入到 Headquarters。</span><span class="sxs-lookup"><span data-stu-id="dead4-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="dead4-106">借助第三方应用程序，可以通过集成将交易记录导入到 Headquarters。</span><span class="sxs-lookup"><span data-stu-id="dead4-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="dead4-107">在这两种情况下，将交易记录导入 Headquarters 中之后，都需要执行一致性检查过程，该过程对交易记录执行多个验证，以便仅将成功通过验证的交易记录导入到要在 Headquarters 中进行过账的对账单中。</span><span class="sxs-lookup"><span data-stu-id="dead4-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="dead4-108">商业交易记录会由于各种原因而验证失败。</span><span class="sxs-lookup"><span data-stu-id="dead4-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="dead4-109">例如，集成代码中的 Bug 或 POS 应用程序中的 Bug 可能会导致数据不一致，用户错误（例如在将产品同步到渠道之后删除该产品，或者对会计期间结账而不过账该期间的交易记录）也会导致数据不一致。</span><span class="sxs-lookup"><span data-stu-id="dead4-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="dead4-110">虽然这些交易记录会被标记并从对账单中排除，但是它们会干扰客户将每日销售过账到财务的每日流程。</span><span class="sxs-lookup"><span data-stu-id="dead4-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="dead4-111">在 Commerce 中，可以编辑验证失败的特定交易记录，同时保持对所有更改的审计。</span><span class="sxs-lookup"><span data-stu-id="dead4-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="dead4-112">编辑和审计交易记录</span><span class="sxs-lookup"><span data-stu-id="dead4-112">Edit and audit transactions</span></span>

<span data-ttu-id="dead4-113">在 Retail 版本 10.0.5 中，现金和结转交易记录（例如销售和退货）是唯一可以编辑的交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="dead4-114">不支持编辑客户订单或在线订单。</span><span class="sxs-lookup"><span data-stu-id="dead4-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="dead4-115">在 Retail 版本 10.0.6 及更高版本中，还支持编辑现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="dead4-116">安装 Dynamics Excel 加载项。</span><span class="sxs-lookup"><span data-stu-id="dead4-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="dead4-117">转至**商店财务**工作区。</span><span class="sxs-lookup"><span data-stu-id="dead4-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="dead4-118">**交易记录验证失败**磁贴提供在一个或多个规则中验证失败的交易记录窗体的预筛选视图。</span><span class="sxs-lookup"><span data-stu-id="dead4-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="dead4-119">打开该窗体。</span><span class="sxs-lookup"><span data-stu-id="dead4-119">Open the form.</span></span> <span data-ttu-id="dead4-120">单击验证失败的记录，然后依次单击 **Office 加载项**、**编辑所选交易记录**。</span><span class="sxs-lookup"><span data-stu-id="dead4-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="dead4-121">随即打开包含所选交易记录详细信息的一个 Excel 文件，其中包含以下工作表：</span><span class="sxs-lookup"><span data-stu-id="dead4-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="dead4-122">行：此工作表包含该交易记录的标头、产品行和相关数据。</span><span class="sxs-lookup"><span data-stu-id="dead4-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="dead4-123">付款：此工作表包含该交易记录的付款行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="dead4-124">折扣：此工作表包含该交易记录的折扣相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="dead4-125">纳税：此工作表包含该交易记录的纳税相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="dead4-126">费用：此工作表包含该交易记录的费用相关数据。</span><span class="sxs-lookup"><span data-stu-id="dead4-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="dead4-127">在 Excel 文件中，修改相应的字段，然后使用 Dynamics Excel 加载项发布功能将数据重新上传到 Headquarters。</span><span class="sxs-lookup"><span data-stu-id="dead4-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="dead4-128">发布后，所做的更改将反映在系统中。</span><span class="sxs-lookup"><span data-stu-id="dead4-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="dead4-129">在发布期间，将不会对用户所做的更改进行验证。</span><span class="sxs-lookup"><span data-stu-id="dead4-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="dead4-130">通过单击标头级别更改的**零售交易记录**标头中的**查看审计线索**以及在相应交易记录页面的相关部分和记录中，可以查看所做更改的完整审计线索。</span><span class="sxs-lookup"><span data-stu-id="dead4-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="dead4-131">例如，与销售行相关的所有更改将在**销售交易记录**页面上可见，与付款相关的更改将在**付款交易记录**页面上可见等等。针对更改而维护的审计详细信息如下。</span><span class="sxs-lookup"><span data-stu-id="dead4-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="dead4-132">修改日期和时间</span><span class="sxs-lookup"><span data-stu-id="dead4-132">Modified date and time</span></span>
   - <span data-ttu-id="dead4-133">字段</span><span class="sxs-lookup"><span data-stu-id="dead4-133">Field</span></span> 
   - <span data-ttu-id="dead4-134">原值</span><span class="sxs-lookup"><span data-stu-id="dead4-134">Old value</span></span>
   - <span data-ttu-id="dead4-135">新值</span><span class="sxs-lookup"><span data-stu-id="dead4-135">New value</span></span>
   - <span data-ttu-id="dead4-136">修改者</span><span class="sxs-lookup"><span data-stu-id="dead4-136">Modified by</span></span>

6. <span data-ttu-id="dead4-137">在做出更改并发布后，请再次运行**验证商店交易记录**选项，以验证所做的更改是否一致和有效。</span><span class="sxs-lookup"><span data-stu-id="dead4-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="dead4-138">只能编辑验证失败的交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="dead4-139">如果要编辑通过验证的交易记录，请将要更改的交易记录的验证状态更改为**错误**或者**无**，之后您便可以编辑该交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="dead4-140">批量编辑交易记录</span><span class="sxs-lookup"><span data-stu-id="dead4-140">Bulk edit transactions</span></span>

<span data-ttu-id="dead4-141">在 Retail 版本 10.0.6 及更高版本中，支持在对账单级别对交易记录进行批量编辑的选项。</span><span class="sxs-lookup"><span data-stu-id="dead4-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="dead4-142">使用 Excel 加载项打开包含您要按照上述 1-3 步修改的交易记录的对账单。</span><span class="sxs-lookup"><span data-stu-id="dead4-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="dead4-143">选择以下选项之一。</span><span class="sxs-lookup"><span data-stu-id="dead4-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="dead4-144">**编辑现金和结转交易记录**。</span><span class="sxs-lookup"><span data-stu-id="dead4-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="dead4-145">通过此选项可以编辑对帐单中包括的所有现金和结转交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="dead4-146">提供了以下 Excel 工作表。</span><span class="sxs-lookup"><span data-stu-id="dead4-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="dead4-147">**交易记录**：此工作表包含销售交易记录的所有标头级别信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="dead4-148">**销售交易记录**：此工作表包含销售交易记录的所有行级别信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="dead4-149">**付款交易记录**：此工作表包含销售交易记录的所有付款行信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="dead4-150">**折扣交易记录**：此工作表包含销售交易记录的所有折扣行信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="dead4-151">**纳税交易记录**：此工作表包含销售交易记录的所有纳税行信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="dead4-152">**费用交易记录**：此工作表包含销售交易记录的所有费用行信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="dead4-153">**编辑现金管理交易记录**。</span><span class="sxs-lookup"><span data-stu-id="dead4-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="dead4-154">通过此选项可以编辑对帐单中包括的所有现金管理交易记录。</span><span class="sxs-lookup"><span data-stu-id="dead4-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="dead4-155">提供了以下 Excel 工作表。</span><span class="sxs-lookup"><span data-stu-id="dead4-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="dead4-156">**交易记录**：此工作表包含现金管理交易记录的所有标头级别信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="dead4-157">**存款支付交易记录**：此工作表包含所有银行投箱交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="dead4-158">**金库支付交易记录**：此工作表包含所有金库投箱交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="dead4-159">**钱币清点**：此工作表包含所有钱币清点交易记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="dead4-160">**收入-支出交易记录**：此工作表包含所有收入-支出交易记录行详细信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="dead4-161">**付款交易记录**：此工作表包含**付款发票**操作以及收入-支出交易记录的所有付款相关信息。</span><span class="sxs-lookup"><span data-stu-id="dead4-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="dead4-162">发布批量编辑的交易记录时，将不会执行验证。</span><span class="sxs-lookup"><span data-stu-id="dead4-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="dead4-163">您必须确保您的所有编辑都是准确的，并在工作表之间保持数据的真实度。</span><span class="sxs-lookup"><span data-stu-id="dead4-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="dead4-164">例如，如果想要更改交易记录日期，以管理结账未结交易记录的会计或库存期间的方案，则您需要更改具有**业务日期**列的所有 Excel 工作表的日期。</span><span class="sxs-lookup"><span data-stu-id="dead4-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="dead4-165">若要在编辑交易记录之后对其进行验证，可以使用**对账单**页面上的**重新验证交易记录**。</span><span class="sxs-lookup"><span data-stu-id="dead4-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
