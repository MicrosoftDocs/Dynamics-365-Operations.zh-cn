---
title: 收款管理关键概念
description: 这些主题定义了收款管理的关键概念。
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8bee320beb411a5ee0829a0e3170de0c7f293172
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440720"
---
# <a name="collections-management-key-concepts"></a><span data-ttu-id="f904b-103">收款管理关键概念</span><span class="sxs-lookup"><span data-stu-id="f904b-103">Collections management key concepts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f904b-104">在开始设置或使用收款前，应了解以下概念：</span><span class="sxs-lookup"><span data-stu-id="f904b-104">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="f904b-105">客户帐龄快照包含特定时间点的帐龄余额信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-105">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="f904b-106">收款客户池帮助您组织您的工作。</span><span class="sxs-lookup"><span data-stu-id="f904b-106">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="f904b-107">收款代理可以有自己的客户池。</span><span class="sxs-lookup"><span data-stu-id="f904b-107">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="f904b-108">列表页组织收款客户、活动和案例。</span><span class="sxs-lookup"><span data-stu-id="f904b-108">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="f904b-109">客户的所有收款信息均在一个页面上，且您可以从该页面执行行动。</span><span class="sxs-lookup"><span data-stu-id="f904b-109">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="f904b-110">可以在一个步骤中停征、复征或冲销利息和费用。</span><span class="sxs-lookup"><span data-stu-id="f904b-110">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="f904b-111">可以在一个步骤中创建勾销交易记录。</span><span class="sxs-lookup"><span data-stu-id="f904b-111">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="f904b-112">可以在一个步骤中处理资金不足 (NSF) 付款。</span><span class="sxs-lookup"><span data-stu-id="f904b-112">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="f904b-113">本主题描述了每个概念。</span><span class="sxs-lookup"><span data-stu-id="f904b-113">This topic describes each concept.</span></span>

## <a name="customer-aging-snapshots"></a><span data-ttu-id="f904b-114">客户帐龄快照</span><span class="sxs-lookup"><span data-stu-id="f904b-114">Customer aging snapshots</span></span>

<span data-ttu-id="f904b-115">一个帐龄快照包含特定时间点的客户的已计算帐龄余额。</span><span class="sxs-lookup"><span data-stu-id="f904b-115">An aging snapshot contains the calculated aged balances for a customer at a specific point in time.</span></span> <span data-ttu-id="f904b-116">此信息将显示在 **帐龄余额** 列表页和 **收款** 页上。</span><span class="sxs-lookup"><span data-stu-id="f904b-116">This information is shown on the **Aged balances** list page and the **Collections** page.</span></span> <span data-ttu-id="f904b-117">可以在收款列表页上查看信息之前，必须创建一个帐龄快照（**帐龄余额**、**收款活动** 和 **收款案例**）。</span><span class="sxs-lookup"><span data-stu-id="f904b-117">An aging snapshot must be created before you can view information on the collections list pages (**Aged balances**, **Collections activities**, and **Collections cases**).</span></span>

<span data-ttu-id="f904b-118">对于每个客户，一个帐龄快照具有对应于帐龄期间定义的每个帐龄期间的帐龄快照标题和记录详细信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-118">For each customer, an aging snapshot has an aging snapshot header and detail records that correspond to each aging period in the aging period definition.</span></span>

<span data-ttu-id="f904b-119">帐龄快照标题包含应付款总金额、信用额度、装箱单金额、销售订单金额、争执的交易记录编号和针对客户帐户争执的交易记录总金额。</span><span class="sxs-lookup"><span data-stu-id="f904b-119">The aging snapshot header contains the total amount that is due, credit limit, packing slip amount, sales order amount, number of disputed transactions, and total amount of the disputed transactions for the customer account.</span></span> <span data-ttu-id="f904b-120">客户的所有交易包括在这些金额的计算中。</span><span class="sxs-lookup"><span data-stu-id="f904b-120">All transactions for the customer are included in the calculation of these amounts.</span></span> <span data-ttu-id="f904b-121">应付款总金额、信用额度、装箱单金额和销售订单金额将在 **收款** 页上 **信用信息** 速见表中显示。</span><span class="sxs-lookup"><span data-stu-id="f904b-121">The total amount that is due, credit limit, packing slip amount, and sales order amount are shown in the **Credit information** FactBox on the **Collections** page.</span></span>

<span data-ttu-id="f904b-122">对于在帐龄期间定义中的每个帐龄期间，都会在帐龄快照中创建详细信息记录。</span><span class="sxs-lookup"><span data-stu-id="f904b-122">For each aging period in the aging period definition, a detail record is created in the aging snapshot.</span></span> <span data-ttu-id="f904b-123">每条详细信息记录都包含帐龄期间 ID 和在帐龄期间日期内的交易记录的总金额。</span><span class="sxs-lookup"><span data-stu-id="f904b-123">Each detail record contains the ID of the aging period and the total amount of the transactions that have dates in the aging period.</span></span> <span data-ttu-id="f904b-124">交易记录分配给某个帐龄期间，例如 30 天前已到期。</span><span class="sxs-lookup"><span data-stu-id="f904b-124">Transactions are assigned to an aging period, such as 30 days past due.</span></span> <span data-ttu-id="f904b-125">该日期与创建帐龄快照时指定的 **帐龄截至** 日期值相关。</span><span class="sxs-lookup"><span data-stu-id="f904b-125">The date is relative to the **Aging as of** date value that you specify when you create the aging snapshot.</span></span> <span data-ttu-id="f904b-126">此信息将显示在 **帐龄余额列表** 页和 **收款** 页的 **帐龄余额** 速见表中。</span><span class="sxs-lookup"><span data-stu-id="f904b-126">This information is shown on the **Aged balances** list page and in the **Aged balances** FactBox on the **Collections** page.</span></span>

## <a name="collections-customer-pools"></a><span data-ttu-id="f904b-127">收款客户池</span><span class="sxs-lookup"><span data-stu-id="f904b-127">Collections customer pools</span></span>

<span data-ttu-id="f904b-128">客户池是定义一组客户记录的查询。</span><span class="sxs-lookup"><span data-stu-id="f904b-128">Customer pools are queries that define a group of customer records.</span></span> <span data-ttu-id="f904b-129">您可以使用这些分组的记录来查看所包含的客户帐户的信息，并管理它们的收款或帐龄流程。</span><span class="sxs-lookup"><span data-stu-id="f904b-129">You can use these grouped records to view information for the customer accounts that are included, and to manage collections or aging processes for them.</span></span> <span data-ttu-id="f904b-130">您可以使用客户池筛选收款列表页上的信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-130">You can use customer pools to filter information on the collections list pages.</span></span> <span data-ttu-id="f904b-131">也可以使用它们筛选创建帐龄快照时包含的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="f904b-131">You also can use them to filter the customer accounts that are included when aging snapshots are created.</span></span>

## <a name="collections-agents"></a><span data-ttu-id="f904b-132">收款代理</span><span class="sxs-lookup"><span data-stu-id="f904b-132">Collections agents</span></span>

<span data-ttu-id="f904b-133">默认情况下，用户可以查看收款列表页上的所有客户信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-133">By default, users can view all customer information on the collections list pages.</span></span> <span data-ttu-id="f904b-134">您可以使用收款代理记录确定可用于筛选收款列表页页和 **收款** 页中的信息的客户池。</span><span class="sxs-lookup"><span data-stu-id="f904b-134">Collections agent records let you determine the customer pools that can be used to filter information on the collections list pages and the **Collections** page.</span></span>

<span data-ttu-id="f904b-135">收款代理与客户进行协作以确保按时收到付款。</span><span class="sxs-lookup"><span data-stu-id="f904b-135">Collections agents work with customers to make sure that payments are collected in a timely manner.</span></span> <span data-ttu-id="f904b-136">他们是 **用户设置** 页上分配给用户的工作人员。</span><span class="sxs-lookup"><span data-stu-id="f904b-136">They are workers who are assigned to users on the **User setup** page.</span></span>

## <a name="collections-list-pages"></a><span data-ttu-id="f904b-137">“收款列表”页</span><span class="sxs-lookup"><span data-stu-id="f904b-137">Collections list pages</span></span>

<span data-ttu-id="f904b-138">以下列表页帮助您组织收款信息：</span><span class="sxs-lookup"><span data-stu-id="f904b-138">The following list pages help you organize collections information:</span></span>

- <span data-ttu-id="f904b-139">**帐龄余额** – 此列表页上的列显示了各帐龄期间的客户余额和帐龄金额。</span><span class="sxs-lookup"><span data-stu-id="f904b-139">**Aged balances** – The columns on this list page show customer balances and aged amounts by aging period.</span></span> <span data-ttu-id="f904b-140">此信息存储在帐龄快照中。</span><span class="sxs-lookup"><span data-stu-id="f904b-140">This information is stored in an aging snapshot.</span></span> <span data-ttu-id="f904b-141">帐龄期间由所用的帐龄期间定义决定。</span><span class="sxs-lookup"><span data-stu-id="f904b-141">The aging periods are determined by the aging period definition that is used.</span></span> <span data-ttu-id="f904b-142">帐龄期间定义从客户池中提取（如果为池查询指定了客户池）。</span><span class="sxs-lookup"><span data-stu-id="f904b-142">The aging period definition is taken from the customer pool, if a customer pool was specified for the pool query.</span></span> <span data-ttu-id="f904b-143">如果池不具有帐龄期间定义，则使用 **应收帐款参数** 页中所指定的默认帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="f904b-143">If the pool doesn't have an aging period definition, the default aging period definition that is specified on the **Accounts receivable parameters** page is used.</span></span> <span data-ttu-id="f904b-144">如果默认帐龄期间定义未指定，则在 **帐龄期间定义** 页中使用第一个帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="f904b-144">If no default aging period definition is specified, the first aging period definition on the **Aging period definitions** page is used.</span></span>
- <span data-ttu-id="f904b-145">**收款活动** – 此列表页上的列显示的活动被标识为收款活动。</span><span class="sxs-lookup"><span data-stu-id="f904b-145">**Collections activities** – The columns on this list page show activities that are identified as collections activities.</span></span> <span data-ttu-id="f904b-146">这些活动是在 **收款** 页上创建的。</span><span class="sxs-lookup"><span data-stu-id="f904b-146">These activities are created on the **Collections** page.</span></span> <span data-ttu-id="f904b-147">您可以使用这些活动跟踪您所做的与收款相关联的工作。</span><span class="sxs-lookup"><span data-stu-id="f904b-147">You use activities to track the collections-related work that you do.</span></span>
- <span data-ttu-id="f904b-148">**收款案例** - 此列表页上的列显示属于具有 **收款** 案例类型的案例类别的案例信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-148">**Collections cases** – The columns on this list page show information for cases that belong to a case category that has a case type of **Collections**.</span></span>

### <a name="aging-snapshots"></a><span data-ttu-id="f904b-149">帐龄快照</span><span class="sxs-lookup"><span data-stu-id="f904b-149">Aging snapshots</span></span>

<span data-ttu-id="f904b-150">可以查看有关收集列表页的信息之前，必须创建一个帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="f904b-150">An aging snapshot must be created before you can view information on the collections list pages.</span></span> <span data-ttu-id="f904b-151">只为已经创建帐龄快照的客户显示信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-151">Information is shown only for customers that an aging snapshot has been created for.</span></span> <span data-ttu-id="f904b-152">可以进一步筛选列表页上显示的记录，如下所述：</span><span class="sxs-lookup"><span data-stu-id="f904b-152">The records that are shown on the list page can be filtered further, as described here:</span></span>

- <span data-ttu-id="f904b-153">默认情况下，用户可以访问具有帐龄快照的所有客户。</span><span class="sxs-lookup"><span data-stu-id="f904b-153">By default, users have access to all customers who have an aging snapshot.</span></span>
- <span data-ttu-id="f904b-154">如果客户池存在，用户必须设置为收款帐户使用池筛选收集列表页上的信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-154">If customer pools exist, a user must be set up as a collections agent to use the pools to filter information on the collections list pages.</span></span> <span data-ttu-id="f904b-155">信息将限制为在所选客户池中所包含的客户。</span><span class="sxs-lookup"><span data-stu-id="f904b-155">Information is limited to the customers who are included in the selected customer pool.</span></span>
- <span data-ttu-id="f904b-156">如果用户设置为收款代理，则在收款列表页上只有为该收款代理选择的池可用。</span><span class="sxs-lookup"><span data-stu-id="f904b-156">If a user is set up as a collections agent, only the pools that are selected for that collections agent are available on the collections list pages.</span></span> <span data-ttu-id="f904b-157">如果在收款代理的 **收款代理** 页中选择了 **允许代理查看所有客户池** 选项，该代理可使用所有池。</span><span class="sxs-lookup"><span data-stu-id="f904b-157">If the **Allow agent to view all customer pools** option is selected on the **Collections agent** page for the collections agent, all pools are available for that agent.</span></span>

## <a name="collections-page"></a><span data-ttu-id="f904b-158">“收款”页</span><span class="sxs-lookup"><span data-stu-id="f904b-158">Collections page</span></span>

<span data-ttu-id="f904b-159">您可以使用 **收款** 页查看和管理催款信息、活动和客户案例，并可以对其采取相关操作。</span><span class="sxs-lookup"><span data-stu-id="f904b-159">You can use the **Collections** page to view, manage, and take action on collections information, activities, and cases for a customer.</span></span>

<span data-ttu-id="f904b-160">该页面的上部显示了所选客户的案例，中间部分显示了该客户的交易，而下部显示了该客户的活动。</span><span class="sxs-lookup"><span data-stu-id="f904b-160">The upper section of the page shows cases for the selected customer, the middle section shows transactions for the customer, and the lower section shows activities for the customer.</span></span> <span data-ttu-id="f904b-161">您可以创建收集案例跟踪一个或多个交易记录和活动的催款信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-161">You can create collections cases to track collections information for one or more transactions and activities.</span></span> <span data-ttu-id="f904b-162">在上部和下部中的信息可以按例筛选。</span><span class="sxs-lookup"><span data-stu-id="f904b-162">The information in the upper and lower sections can be filtered by case.</span></span>

<span data-ttu-id="f904b-163">FactBox 显示所选客户的帐龄余额和信用额度信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-163">FactBoxes show aged balances and credit limit information for the selected customer.</span></span> <span data-ttu-id="f904b-164">此信息存储在帐龄快照中。</span><span class="sxs-lookup"><span data-stu-id="f904b-164">This information is stored in the aging snapshot.</span></span> <span data-ttu-id="f904b-165">需要时，您可以更新当前信息的帐龄快照。</span><span class="sxs-lookup"><span data-stu-id="f904b-165">As you require, you can update the aging snapshot with current information.</span></span>

<span data-ttu-id="f904b-166">操作窗格包含用于查看所选客户、案例、交易记录或活动的相关信息的按钮。</span><span class="sxs-lookup"><span data-stu-id="f904b-166">The Action Pane contains buttons that let you view related information for the selected customer, case, transaction, or activity.</span></span> <span data-ttu-id="f904b-167">您还可以执行常用操作，如更改交易记录的收款状态，通过与电子邮件提供商集成发送电子邮件，偿还客户，处理 NSF 支付和勾销不可托收的余额。</span><span class="sxs-lookup"><span data-stu-id="f904b-167">You can also perform common actions, such as changing the collections status of a transaction, sending email through the integration with your email provider, reimbursing customers, processing NSF payments, and writing off uncollectible balances.</span></span>

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a><span data-ttu-id="f904b-168">停征、复征或冲销利息和费用</span><span class="sxs-lookup"><span data-stu-id="f904b-168">Waiving, reinstating, or reversing interest and fees</span></span>

<span data-ttu-id="f904b-169">您可以停征、复征或冲销全部利息单，或者利息单中包含的费用和交易记录利息。</span><span class="sxs-lookup"><span data-stu-id="f904b-169">You can waive, reinstate, or reverse whole interest notes, or the fees and transaction interest that are part of interest notes.</span></span> <span data-ttu-id="f904b-170">在 **所有客户** 列表页的操作窗格的 **收款** 选项卡上，选择 **利息单**、**交易记录利息** 或 **费用**。</span><span class="sxs-lookup"><span data-stu-id="f904b-170">On the **Collect** tab on the Action Pane of the **All customers** list page, select **Interest note**, **Transaction interest**, or **Fee**.</span></span>

<span data-ttu-id="f904b-171">这些调整仅影响包括的利息单、利息和费用。</span><span class="sxs-lookup"><span data-stu-id="f904b-171">These adjustments affect only interest notes, and the interest and fees that they include.</span></span> <span data-ttu-id="f904b-172">有关如何勾销所有客户欠款的信息，请参阅本主题的[创建勾销交易记录](#creating-write-off-transactions)部分。</span><span class="sxs-lookup"><span data-stu-id="f904b-172">For information about how to write off all the charges that a customer owes, see the [Creating write-off transactions](#creating-write-off-transactions) section of this topic.</span></span>

<span data-ttu-id="f904b-173">有关详细信息，请参阅创建具有范围的利息代码和处理利息。</span><span class="sxs-lookup"><span data-stu-id="f904b-173">For more information see, Create an interest code with a range and Process interest.</span></span>

## <a name="creating-write-off-transactions"></a><span data-ttu-id="f904b-174">创建勾销交易记录</span><span class="sxs-lookup"><span data-stu-id="f904b-174">Creating write-off transactions</span></span>

<span data-ttu-id="f904b-175">您可以在 **收款** 页和收款列表页上选择 **勾销** 来勾销坏帐。</span><span class="sxs-lookup"><span data-stu-id="f904b-175">You can write off bad debts by selecting **Write off** on the **Collections** page and the collections list pages.</span></span>

<span data-ttu-id="f904b-176">在勾销客户的交易记录时，该客户的所有交易记录会自动标记为结算。</span><span class="sxs-lookup"><span data-stu-id="f904b-176">When you write off transactions for a customer, all transactions for that customer are automatically marked for settlement.</span></span> <span data-ttu-id="f904b-177">已注销的金额取决于标记交易记录的净额、。</span><span class="sxs-lookup"><span data-stu-id="f904b-177">The amount that is written off depends on the net amount of the marked transactions.</span></span> <span data-ttu-id="f904b-178">勾销交易记录创建于普通日记帐中，它可以包括最多三种类型的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f904b-178">The write-off transaction is created in a general journal and can contain up to three types of journal lines:</span></span>

- <span data-ttu-id="f904b-179">日志行的第一类型包含客户删除物料。</span><span class="sxs-lookup"><span data-stu-id="f904b-179">The first type of journal line contains the customer write-off entry.</span></span> <span data-ttu-id="f904b-180">如果已标记的交易记录包含货币代码、维度和过帐配置文件的多个组合，则会为每个组合创建单独的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f904b-180">If the marked transactions contain multiple combinations of currency codes, dimensions, and posting profiles, a separate journal line is created for each combination.</span></span>
- <span data-ttu-id="f904b-181">日志行的第二类型包含总帐冲销条目。</span><span class="sxs-lookup"><span data-stu-id="f904b-181">The second type of journal line contains the general ledger write-off entry.</span></span> <span data-ttu-id="f904b-182">如果已标记的交易记录包含货币代码、维度和过帐配置文件的多个组合，则会为每个组合创建单独的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f904b-182">If the marked transactions contain multiple combinations of currency codes, dimensions, and posting profiles, a separate journal line is created for each combination.</span></span>
- <span data-ttu-id="f904b-183">日志行的第三类型包含增值税的总帐注销信息。</span><span class="sxs-lookup"><span data-stu-id="f904b-183">The third type of journal line contains the general ledger write-off information for sales taxes.</span></span> <span data-ttu-id="f904b-184">只有当在 **应收帐款参数** 页中选择 **单独的销售税** 选项后，才会创建此日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f904b-184">This journal line is created only if the **Separate sales tax** option is selected on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="f904b-185">如果已标记的交易记录包含销售税应付科目、维度和销售税代码的多个组合，则会为每个组合创建单独的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="f904b-185">If the marked transactions contain multiple combinations of sales tax payable accounts, dimensions, and sales tax codes, a separate journal line is created for each combination.</span></span> <span data-ttu-id="f904b-186">销帐交易记录在交易记录币种中创建。</span><span class="sxs-lookup"><span data-stu-id="f904b-186">The write-off transaction is created in the transaction currency.</span></span> <span data-ttu-id="f904b-187">有关详细信息，请参阅创建客户的勾销日记帐。</span><span class="sxs-lookup"><span data-stu-id="f904b-187">For more information see, Create a write-off journal for a customer.</span></span>

## <a name="process-nsf-payments"></a><span data-ttu-id="f904b-188">处理 NSF 支付</span><span class="sxs-lookup"><span data-stu-id="f904b-188">Process NSF payments</span></span>

<span data-ttu-id="f904b-189">您可以通过选择 **收款** 页上的 **NSF 支付** 来处理 NSF 支付。</span><span class="sxs-lookup"><span data-stu-id="f904b-189">You can process NSF payments by selecting **NSF payment** on the **Collections** page.</span></span> <span data-ttu-id="f904b-190">当您选择此按钮时，会取消付款。</span><span class="sxs-lookup"><span data-stu-id="f904b-190">When you select this button, the payment is canceled.</span></span> <span data-ttu-id="f904b-191">如果 NSF 费用应用于该客户，则可以在付款日记帐中创建费用交易记录。</span><span class="sxs-lookup"><span data-stu-id="f904b-191">If an NSF fee applies for the customer, a charge transaction is created in a payment journal.</span></span> <span data-ttu-id="f904b-192">该费用金额基于自动费用的设置。</span><span class="sxs-lookup"><span data-stu-id="f904b-192">The amount of the fee is based on the settings for the automatic charges.</span></span> <span data-ttu-id="f904b-193">适用于 NSF 支付的自动费用由受影响银行帐户的 **银行帐户** 页中选择的费用组指定。</span><span class="sxs-lookup"><span data-stu-id="f904b-193">The automatic charges that apply to NSF payments are specified by the charges group that is selected on the **Bank accounts** page for the affected bank account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f904b-194">其他资源</span><span class="sxs-lookup"><span data-stu-id="f904b-194">Additional resources</span></span>

[<span data-ttu-id="f904b-195">客户信用管理参数设置</span><span class="sxs-lookup"><span data-stu-id="f904b-195">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="f904b-196">客户信用管理设置信息</span><span class="sxs-lookup"><span data-stu-id="f904b-196">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="f904b-197">为客户添加信用管理信息</span><span class="sxs-lookup"><span data-stu-id="f904b-197">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="f904b-198">客户信用组</span><span class="sxs-lookup"><span data-stu-id="f904b-198">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="f904b-199">客户信用额度调整</span><span class="sxs-lookup"><span data-stu-id="f904b-199">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="f904b-200">销售订单的信用保留</span><span class="sxs-lookup"><span data-stu-id="f904b-200">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="f904b-201">客户信用管理定期任务</span><span class="sxs-lookup"><span data-stu-id="f904b-201">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
