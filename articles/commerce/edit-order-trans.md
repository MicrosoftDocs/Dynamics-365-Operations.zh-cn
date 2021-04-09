---
title: 编辑并审计在线订单和异步客户订单交易记录
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计在线订单和异步客户订单交易记录。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 5113f7ac0d308076ebaa9daeca0929eb537e94ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792673"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="cf9cb-103">编辑并审计在线订单和异步客户订单交易记录</span><span class="sxs-lookup"><span data-stu-id="cf9cb-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf9cb-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑并审计在线订单和异步客户订单交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf9cb-105">概览</span><span class="sxs-lookup"><span data-stu-id="cf9cb-105">Overview</span></span>

<span data-ttu-id="cf9cb-106">在 Commerce 版本 10.0.5 和 10.0.6 中，增加了对编辑现金和结转交易记录（例如销售和退货）及现金管理交易记录（例如浮动条目和支付方式删除）的支持。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="cf9cb-107">在 Commerce 版本 10.0.7 中，增加了对编辑在线订单交易记录和异步客户订单交易记录的支持。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="cf9cb-108">编辑和审计订单交易记录</span><span class="sxs-lookup"><span data-stu-id="cf9cb-108">Edit and audit order transactions</span></span>

<span data-ttu-id="cf9cb-109">要在 Commerce Headquarters 中编辑和审计订单交易记录，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cf9cb-110">安装 [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="cf9cb-111">在 **零售参数** 页面、**客户订单** 选项卡、**订单** 快速选项卡上，为 **订单同步错误的保留代码** 指定保留代码。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="cf9cb-112">打开 **商店财务** 工作区。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="cf9cb-113">**在线订单同步错误** 和 **客户订单同步错误** 磁贴提供零售交易记录页面的预筛选视图。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="cf9cb-114">每个磁贴都显示对应订单类型中同步失败的交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="cf9cb-115">打开 **在线订单同步错误** 页面或 **客户订单同步错误** 页面。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="cf9cb-116">选择一条记录以查看同步错误详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="cf9cb-117">**同步状态** 快速选项卡提供以下错误详细信息：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="cf9cb-118">待定订单状态</span><span class="sxs-lookup"><span data-stu-id="cf9cb-118">Pending order status</span></span>
    - <span data-ttu-id="cf9cb-119">订单错误详细信息</span><span class="sxs-lookup"><span data-stu-id="cf9cb-119">Order error details</span></span>
    - <span data-ttu-id="cf9cb-120">修改日期和时间</span><span class="sxs-lookup"><span data-stu-id="cf9cb-120">Modified date and time</span></span>
    - <span data-ttu-id="cf9cb-121">重试计数</span><span class="sxs-lookup"><span data-stu-id="cf9cb-121">Retry count</span></span>

1. <span data-ttu-id="cf9cb-122">如果错误详细信息指示必须修复该记录，请选择 **Office 加载项**，然后选择 **编辑所选交易记录**。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="cf9cb-123">此时将打开一个 Excel 文件，其中显示了所选交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="cf9cb-124">如果正在编辑的交易记录是在线订单交易记录，则该 Excel 文件包含以下工作表：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="cf9cb-125">**交易记录** - 此工作表包含该交易记录的标头详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-126">**销售交易记录** - 此工作表包含该交易记录的行详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-127">**付款交易记录** - 此工作表包含该交易记录的付款行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-128">**折扣交易记录** - 此工作表包含该交易记录的折扣相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-129">**纳税交易记录** - 此工作表包含该交易记录的纳税相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-130">**费用交易记录** - 此工作表包含该交易记录的费用相关数据。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="cf9cb-131">如果正在编辑的交易记录是异步客户订单交易记录，则该 Excel 文件包含以下工作表：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="cf9cb-132">**行** - 此工作表包含该交易记录的标头和行详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-133">**付款** - 此工作表包含该交易记录的付款行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-134">**折扣** - 此工作表包含该交易记录的折扣相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-135">**纳税** - 此工作表包含该交易记录的纳税相关详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="cf9cb-136">**费用** - 此工作表包含该交易记录的费用相关数据。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="cf9cb-137">在 Excel 文件的 **待定订单状态** 字段中，输入 **正在编辑**，然后发布该更改。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="cf9cb-138">这样，可以防止正在以批处理模式运行的 **同步订单** 作业在处理过程中跳过此记录。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="cf9cb-139">在 Excel 文件中，修改相应的字段，然后使用 Dynamics Excel 加载项发布功能将数据重新上传到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="cf9cb-140">发布数据后，所做的更改将反映在系统中。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="cf9cb-141">在发布期间，将不会对用户所做的更改进行验证。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="cf9cb-142">通过选择标头级别更改的 **零售交易记录** 标头中的 **查看审计线索**，以及在相应交易记录页面的相关部分和记录中，可以查看所做更改的完整审计线索。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="cf9cb-143">例如，与销售行相关的所有更改都将显示在 **销售交易记录** 页面上，所有与付款相关的更改都将显示在 **付款交易记录** 页面上。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="cf9cb-144">将保持更改的以下审计详细信息：</span><span class="sxs-lookup"><span data-stu-id="cf9cb-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="cf9cb-145">修改日期和时间</span><span class="sxs-lookup"><span data-stu-id="cf9cb-145">Modified date and time</span></span>
    - <span data-ttu-id="cf9cb-146">字段</span><span class="sxs-lookup"><span data-stu-id="cf9cb-146">Field</span></span>
    - <span data-ttu-id="cf9cb-147">原值</span><span class="sxs-lookup"><span data-stu-id="cf9cb-147">Old value</span></span>
    - <span data-ttu-id="cf9cb-148">新值</span><span class="sxs-lookup"><span data-stu-id="cf9cb-148">New value</span></span>
    - <span data-ttu-id="cf9cb-149">修改者</span><span class="sxs-lookup"><span data-stu-id="cf9cb-149">Modified by</span></span>

1. <span data-ttu-id="cf9cb-150">在做出更改并发布后，请选择 **同步订单** 以立即启动同步过程。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="cf9cb-151">或者，您可以等待正在以批处理模式运行的同步过程完成，然后再处理该交易记录。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="cf9cb-152">默认情况下，成功同步订单后，将根据 Commerce 参数中定义的保留代码，将订单置于保留状态。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="cf9cb-153">必须先取消对订单的保留，然后才能进一步处理订单以进行履行或其他操作。</span><span class="sxs-lookup"><span data-stu-id="cf9cb-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf9cb-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="cf9cb-154">Additional resources</span></span>

[<span data-ttu-id="cf9cb-155">编辑并审计现金和结转及现金管理交易记录</span><span class="sxs-lookup"><span data-stu-id="cf9cb-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="cf9cb-156">编辑零售交易记录的财务维度</span><span class="sxs-lookup"><span data-stu-id="cf9cb-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="cf9cb-157">创建 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="cf9cb-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="cf9cb-158">将字段添加到 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="cf9cb-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]