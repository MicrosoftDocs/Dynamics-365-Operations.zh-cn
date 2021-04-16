---
title: 将“目标客户到现金”数据从数据集成器迁移到双写入
description: 本主题介绍如何将“目标客户到现金”数据从数据集成器迁移到双写入。
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f6758fe366c2ea59dc75be2f1070650eb5c2f9fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750852"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a><span data-ttu-id="de475-103">将“目标客户到现金”数据从数据集成器迁移到双写入</span><span class="sxs-lookup"><span data-stu-id="de475-103">Migrate Prospect to cash data from Data Integrator to dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de475-104">要将“目标客户到现金”数据从数据集成器迁移到双写入，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="de475-104">To migrate your Prospect to cash data from Data Integrator to dual-write, follow these steps.</span></span>

1. <span data-ttu-id="de475-105">运行“目标客户到现金”数据集成器作业，执行最后一次完全同步。</span><span class="sxs-lookup"><span data-stu-id="de475-105">Run the Prospect to cash Data Integrator jobs to do one final full synchronization.</span></span> <span data-ttu-id="de475-106">这样，您可以确保两个系统（Finance and Operations 应用和客户互动应用）具有所有数据。</span><span class="sxs-lookup"><span data-stu-id="de475-106">In this way, you ensure that both systems (Finance and Operations apps and customer engagement apps) have all the data.</span></span>
2. <span data-ttu-id="de475-107">为帮助防止潜在的数据丢失，将“目标客户到现金”数据从 Microsoft Dynamics 365 Sales 导出到 Excel 文件或逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="de475-107">To help prevent potential data loss, export the Prospect to cash data from Microsoft Dynamics 365 Sales to an Excel file or a comma-separated values (CSV) file.</span></span> <span data-ttu-id="de475-108">从以下实体导出数据：</span><span class="sxs-lookup"><span data-stu-id="de475-108">Export data from the following entities:</span></span>

    - [<span data-ttu-id="de475-109">科目</span><span class="sxs-lookup"><span data-stu-id="de475-109">Account</span></span>](#account-table)
    - [<span data-ttu-id="de475-110">联系人</span><span class="sxs-lookup"><span data-stu-id="de475-110">Contact</span></span>](#contact-table)
    - [<span data-ttu-id="de475-111">账单</span><span class="sxs-lookup"><span data-stu-id="de475-111">Invoice</span></span>](#invoice-table)
    - <span data-ttu-id="de475-112">发票产品</span><span class="sxs-lookup"><span data-stu-id="de475-112">Invoice products</span></span>
    - [<span data-ttu-id="de475-113">订单</span><span class="sxs-lookup"><span data-stu-id="de475-113">Order</span></span>](#order-table)
    - [<span data-ttu-id="de475-114">订单产品</span><span class="sxs-lookup"><span data-stu-id="de475-114">Order products</span></span>](#order-products-table)
    - [<span data-ttu-id="de475-115">产品</span><span class="sxs-lookup"><span data-stu-id="de475-115">Products</span></span>](#products-table)
    - [<span data-ttu-id="de475-116">报价</span><span class="sxs-lookup"><span data-stu-id="de475-116">Quote</span></span>](#quote-and-quote-product-tables)
    - [<span data-ttu-id="de475-117">报价单产品</span><span class="sxs-lookup"><span data-stu-id="de475-117">Quote products</span></span>](#quote-and-quote-product-tables)

3. <span data-ttu-id="de475-118">从 Sales 环境中卸载“目标客户到现金”解决方案。</span><span class="sxs-lookup"><span data-stu-id="de475-118">Uninstall the Prospect to cash solution from the Sales environment.</span></span> <span data-ttu-id="de475-119">此步骤将删除“目标客户到现金”解决方案引入的列和相应的数据。</span><span class="sxs-lookup"><span data-stu-id="de475-119">This step removes the columns and corresponding data that the Prospect to cash solution introduced.</span></span>
4. <span data-ttu-id="de475-120">安装双写入解决方案。</span><span class="sxs-lookup"><span data-stu-id="de475-120">Install the dual-write solution.</span></span>
5. <span data-ttu-id="de475-121">为一个或多个法人在 Finance and Operations 应用和客户互动应用之间创建双写入连接。</span><span class="sxs-lookup"><span data-stu-id="de475-121">Create a dual-write connection between the Finance and Operations app and the customer engagement app for one or more legal entities.</span></span>
6. <span data-ttu-id="de475-122">启用双写入表映射，然后为所需的参考数据运行初始同步。</span><span class="sxs-lookup"><span data-stu-id="de475-122">Enable dual-write table maps, and run the initial synchronization for the required reference data.</span></span> <span data-ttu-id="de475-123">（有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。）所需数据的示例包括客户组、付款期限和付款计划。</span><span class="sxs-lookup"><span data-stu-id="de475-123">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) Examples of required data include customer groups, payment terms, and payment schedules.</span></span> <span data-ttu-id="de475-124">不要为需要初始化的表启用双写入映射，如客户、报价单、报价单行、订单和订单行表。</span><span class="sxs-lookup"><span data-stu-id="de475-124">Don't enable the dual-write maps for tables that require initialization, such as the account, quote, quote line, order, and order line tables.</span></span>
7. <span data-ttu-id="de475-125">在客户互动应用中，转到 **高级设置 \> 系统设置 \> 数据管理 \> 重复检测规则**，禁用所有规则。</span><span class="sxs-lookup"><span data-stu-id="de475-125">In the customer engagement app, go to **Advanced Settings \> System Settings \> Data Management \> Duplicate detection rules**, and disable all the rules.</span></span>
8. <span data-ttu-id="de475-126">初始化步骤 2 中列出的表。</span><span class="sxs-lookup"><span data-stu-id="de475-126">Initialize the tables that are listed in step 2.</span></span> <span data-ttu-id="de475-127">有关说明，请参阅本主题的其余章节。</span><span class="sxs-lookup"><span data-stu-id="de475-127">For instructions, see the remaining sections of this topic.</span></span>
9. <span data-ttu-id="de475-128">打开 Finance and Operations 应用，启用表映射，如客户、报价单、报价单行、订单和订单行表映射。</span><span class="sxs-lookup"><span data-stu-id="de475-128">Open the Finance and Operations app, and enable the table maps, such as the account, quote, quote line, order, and order line table maps.</span></span> <span data-ttu-id="de475-129">然后运行初始同步。</span><span class="sxs-lookup"><span data-stu-id="de475-129">Then run the initial synchronization.</span></span> <span data-ttu-id="de475-130">（有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。）此流程将同步来自 Finance and Operations 应用的其他信息，如处理状态、装运地址和账单地址、站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="de475-130">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) This process will sync additional information from the Finance and Operations app, such as processing status, shipping and billing addresses, sites, and warehouses.</span></span>

## <a name="account-table"></a><span data-ttu-id="de475-131">客户表</span><span class="sxs-lookup"><span data-stu-id="de475-131">Account table</span></span>

1. <span data-ttu-id="de475-132">在 **公司** 列中，输入公司名称，如 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="de475-132">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="de475-133">在 **关系类型** 列中，输入 **客户** 作为静态值。</span><span class="sxs-lookup"><span data-stu-id="de475-133">In the **Relationship Type** column, enter **Customer** as a static value.</span></span> <span data-ttu-id="de475-134">您可能不想在业务逻辑中将每个客户记录分类为客户。</span><span class="sxs-lookup"><span data-stu-id="de475-134">You might not want to classify every account record as a customer in your business logic.</span></span>
3. <span data-ttu-id="de475-135">在 **客户组 ID** 列中，从 Finance and Operations 应用输入客户组编号。</span><span class="sxs-lookup"><span data-stu-id="de475-135">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="de475-136">“目标客户到现金”解决方案的默认值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="de475-136">The default value from the Prospect to cash solution is **10**.</span></span>
4. <span data-ttu-id="de475-137">如果您使用的是“目标客户到现金”解决方案，没有任何 **客户编号** 自定义项，请在 **当事方编号** 列中输入 **客户编号** 值。</span><span class="sxs-lookup"><span data-stu-id="de475-137">If you're using the Prospect to cash solution without any customization of **Account Number**, enter an **Account Number** value in the **Party Number** column.</span></span> <span data-ttu-id="de475-138">如果有自定义项，并且您不知道当事方编号，请从 Finance and Operations 应用提取此信息。</span><span class="sxs-lookup"><span data-stu-id="de475-138">If there are customizations, and you don't know the party number, pull this information from the Finance and Operations app.</span></span>

## <a name="contact-table"></a><span data-ttu-id="de475-139">联系人表</span><span class="sxs-lookup"><span data-stu-id="de475-139">Contact table</span></span>

1. <span data-ttu-id="de475-140">在 **公司** 列中，输入公司名称，如 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="de475-140">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="de475-141">根据 CSV 文件中的 **IsActiveCustomer** 值设置以下列：</span><span class="sxs-lookup"><span data-stu-id="de475-141">Set the following columns, based on the **IsActiveCustomer** value in the CSV file:</span></span>

    - <span data-ttu-id="de475-142">如果 **IsActiveCustomer** 在 CSV 文件中设置为 **是**，则将 **适售** 列设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="de475-142">If **IsActiveCustomer** is set to **Yes** in the CSV file, set the **Sellable** column to **Yes**.</span></span> <span data-ttu-id="de475-143">在 **客户组 ID** 列中，从 Finance and Operations 应用输入客户组编号。</span><span class="sxs-lookup"><span data-stu-id="de475-143">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="de475-144">“目标客户到现金”解决方案的默认值为 **10**。</span><span class="sxs-lookup"><span data-stu-id="de475-144">The default value from the Prospect to cash solution is **10**.</span></span>
    - <span data-ttu-id="de475-145">如果 **IsActiveCustomer** 在 CSV 文件中设置为 **否**，则将 **适售** 列设置为 **否**，并将 **联系人** 列设置为 **客户**。</span><span class="sxs-lookup"><span data-stu-id="de475-145">If **IsActiveCustomer** is set to **No** in the CSV file, set the **Sellable** column to **No**, and set the **Contact For** column to **Customer**.</span></span>

3. <span data-ttu-id="de475-146">如果您使用的是“目标客户到现金”解决方案，没有对 **联系人编号** 的任何自定义项，请设置以下列：</span><span class="sxs-lookup"><span data-stu-id="de475-146">If you're using the Prospect to cash solution without any customization of **Contact Number**, set the following columns:</span></span>

    - <span data-ttu-id="de475-147">将联系人编号从 CSV 文件 (**msdynce\_contactnumber**) 迁移到 **联系人** 表 (**msdyn\_contactnumber**) 中的联系人编号。</span><span class="sxs-lookup"><span data-stu-id="de475-147">Migrate the contact number from the CSV file (**msdynce\_contactnumber**) to the contact number in the **Contact** table (**msdyn\_contactnumber**).</span></span>
    - <span data-ttu-id="de475-148">使用 **当事方编号** 列中 **联系人编号** 表中的值。</span><span class="sxs-lookup"><span data-stu-id="de475-148">Use values from the **Contact Number** table in the **Party Number** column.</span></span>
    - <span data-ttu-id="de475-149">使用 **客户编号/联系人 ID** 列中 **联系人编号** 表中的值。</span><span class="sxs-lookup"><span data-stu-id="de475-149">Use values from the **Contact Number** table in the **Account Number/Contact Person ID** column.</span></span>

## <a name="invoice-table"></a><span data-ttu-id="de475-150">发票表</span><span class="sxs-lookup"><span data-stu-id="de475-150">Invoice table</span></span>

<span data-ttu-id="de475-151">由于 **发票** 表中的数据被设计为单向流动，即从 Finance and Operations 应用到客户互动应用，所以不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="de475-151">Because data from the **Invoice** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="de475-152">运行初始同步，将所有必需的数据从 Finance and Operations 应用迁移到客户互动应用。</span><span class="sxs-lookup"><span data-stu-id="de475-152">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="de475-153">有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。</span><span class="sxs-lookup"><span data-stu-id="de475-153">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="order-table"></a><span data-ttu-id="de475-154">订单表</span><span class="sxs-lookup"><span data-stu-id="de475-154">Order table</span></span>

1. <span data-ttu-id="de475-155">在 **公司** 列中，输入公司名称，如 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="de475-155">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="de475-156">将 CSV 文件中的 **订单 ID** 列的值复制到 **销售订单编号** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-156">Copy the value of the **Order ID** column in the CSV file to the **Sales Order Number** column.</span></span>
3. <span data-ttu-id="de475-157">将 CSV 文件中的 **客户** 列的值复制到 **发票客户编号** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-157">Copy the value of the **Customer** column in the CSV file to the **Invoice customer number** column.</span></span>
4. <span data-ttu-id="de475-158">将 CSV 文件中的 **运达国家/地区** 列的值复制到 **运达国家/地区** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-158">Copy the value of the **Ship To Country/Region** column in the CSV file to the **Ship To Country/Region** column.</span></span> <span data-ttu-id="de475-159">此值的示例包括 **US** 和 **美国**。</span><span class="sxs-lookup"><span data-stu-id="de475-159">Examples of this value include **US** and **United States**.</span></span>
5. <span data-ttu-id="de475-160">设置 **要求收货日期** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-160">Set the **Requested Receipt Date** column.</span></span> <span data-ttu-id="de475-161">如果您没有使用收货日期，请使用 CSV 文件中的 **要求交货日期**、**履行日期** 和 **提交日期** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-161">If you aren't using a receipt date, use the **Requested Delivery Date**, **Date Fulfilled**, and **Date Submitted** columns in the CSV file.</span></span> <span data-ttu-id="de475-162">此值的一个示例是 **2020-03-27T00:00:00Z**。</span><span class="sxs-lookup"><span data-stu-id="de475-162">An example of this value is **2020-03-27T00:00:00Z**.</span></span>
6. <span data-ttu-id="de475-163">设置 **语言** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-163">Set the **Language** column.</span></span> <span data-ttu-id="de475-164">此值的一个示例是 **en-us**。</span><span class="sxs-lookup"><span data-stu-id="de475-164">An example of this value is **en-us**.</span></span>
7. <span data-ttu-id="de475-165">使用 **基于物料** 列设置 **订单类型** 列。</span><span class="sxs-lookup"><span data-stu-id="de475-165">Set the **Order Type** column by using the **Item-based** column.</span></span>

## <a name="order-products-table"></a><span data-ttu-id="de475-166">订单产品表</span><span class="sxs-lookup"><span data-stu-id="de475-166">Order products table</span></span>

- <span data-ttu-id="de475-167">在 **公司** 列中，输入公司名称，如 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="de475-167">In the **Company** column, enter the company name, such as **USMF**.</span></span>

## <a name="products-table"></a><span data-ttu-id="de475-168">产品表</span><span class="sxs-lookup"><span data-stu-id="de475-168">Products table</span></span>

<span data-ttu-id="de475-169">由于 **产品** 表中的数据被设计为单向流动，即从 Finance and Operations 应用到客户互动应用，所以不需要初始化。</span><span class="sxs-lookup"><span data-stu-id="de475-169">Because data from the **Products** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="de475-170">运行初始同步，将所有必需的数据从 Finance and Operations 应用迁移到客户互动应用。</span><span class="sxs-lookup"><span data-stu-id="de475-170">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="de475-171">有关详细信息，请参阅[初始同步注意事项](initial-sync-guidance.md)。</span><span class="sxs-lookup"><span data-stu-id="de475-171">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="quote-and-quote-product-tables"></a><span data-ttu-id="de475-172">报价单和报价单产品表</span><span class="sxs-lookup"><span data-stu-id="de475-172">Quote and Quote product tables</span></span>

<span data-ttu-id="de475-173">对于 **报价单** 表，请按照本主题前面的[订单表](#order-table)一节的说明操作。</span><span class="sxs-lookup"><span data-stu-id="de475-173">For the **Quote** table, follow the instructions in the [Order table](#order-table) section earlier in this topic.</span></span> <span data-ttu-id="de475-174">对于 **报价单产品** 表，请按照[订单产品表](#order-products-table)一节的说明操作。</span><span class="sxs-lookup"><span data-stu-id="de475-174">For the **Quote product** table, follow the instructions in the [Order products table](#order-products-table) section.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]