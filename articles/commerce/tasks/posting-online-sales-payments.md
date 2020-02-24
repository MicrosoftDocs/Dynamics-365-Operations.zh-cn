---
title: 过帐联机销售和付款
description: 此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021724"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="deebf-103">过帐联机销售和付款</span><span class="sxs-lookup"><span data-stu-id="deebf-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="deebf-104">此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。</span><span class="sxs-lookup"><span data-stu-id="deebf-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="deebf-105">过帐联机销售和付款是包含两个阶段的流程。</span><span class="sxs-lookup"><span data-stu-id="deebf-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="deebf-106">提取 HQ 的在线商业交易记录数据。</span><span class="sxs-lookup"><span data-stu-id="deebf-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="deebf-107">同步订单以在 HQ 创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="deebf-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="deebf-108">可以通过运行 P 作业或通过创建重复执行批处理作业提取在线交易记录数据。</span><span class="sxs-lookup"><span data-stu-id="deebf-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="deebf-109">手动运行 P 作业</span><span class="sxs-lookup"><span data-stu-id="deebf-109">Manually running the P-job</span></span>

1. <span data-ttu-id="deebf-110">转至“所有工作区”>“Retail 和 Commerce IT”。</span><span class="sxs-lookup"><span data-stu-id="deebf-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="deebf-111">单击“配送计划”。</span><span class="sxs-lookup"><span data-stu-id="deebf-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="deebf-112">选择 P-0001。</span><span class="sxs-lookup"><span data-stu-id="deebf-112">Select P-0001.</span></span>
4. <span data-ttu-id="deebf-113">如果需要，调整渠道数据库组。</span><span class="sxs-lookup"><span data-stu-id="deebf-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="deebf-114">单击立即运行。</span><span class="sxs-lookup"><span data-stu-id="deebf-114">Click Run now.</span></span>
6. <span data-ttu-id="deebf-115">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="deebf-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="deebf-116">为重复执行的 P 作业排产</span><span class="sxs-lookup"><span data-stu-id="deebf-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="deebf-117">转至“所有工作区”>“Retail 和 Commerce IT”。</span><span class="sxs-lookup"><span data-stu-id="deebf-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="deebf-118">单击“配送计划”。</span><span class="sxs-lookup"><span data-stu-id="deebf-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="deebf-119">选择 P-0001。</span><span class="sxs-lookup"><span data-stu-id="deebf-119">Select P-0001.</span></span>
4. <span data-ttu-id="deebf-120">单击“创建批处理作业”。</span><span class="sxs-lookup"><span data-stu-id="deebf-120">Click Create batch job.</span></span>
5. <span data-ttu-id="deebf-121">单击“在后台运行”。</span><span class="sxs-lookup"><span data-stu-id="deebf-121">Click Run in the background.</span></span>
5. <span data-ttu-id="deebf-122">启用“批处理”。</span><span class="sxs-lookup"><span data-stu-id="deebf-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="deebf-123">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="deebf-123">Click Recurrence..</span></span>
7. <span data-ttu-id="deebf-124">选择“无结束日期”选项。</span><span class="sxs-lookup"><span data-stu-id="deebf-124">Select the No end date option.</span></span>
8. <span data-ttu-id="deebf-125">在“计数”字段中，输入运行之间以分钟为单位的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="deebf-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="deebf-126">通常为 5-10。</span><span class="sxs-lookup"><span data-stu-id="deebf-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="deebf-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-127">Click OK.</span></span>
10. <span data-ttu-id="deebf-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-128">Click OK.</span></span>

<span data-ttu-id="deebf-129">可以通过运行“同步订单”作业或创建重复执行批处理作业同步订单。</span><span class="sxs-lookup"><span data-stu-id="deebf-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="deebf-130">手动运行订单同步</span><span class="sxs-lookup"><span data-stu-id="deebf-130">Manually running order synchronization</span></span> 

<span data-ttu-id="deebf-131">执行以下步骤，以便手动运行一次“同步订单”作业。</span><span class="sxs-lookup"><span data-stu-id="deebf-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="deebf-132">转至“所有工作区”>“商店财务”。</span><span class="sxs-lookup"><span data-stu-id="deebf-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="deebf-133">单击“同步订单”。</span><span class="sxs-lookup"><span data-stu-id="deebf-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="deebf-134">在“组织层次结构”字段中，选择“商店(按地区)”。</span><span class="sxs-lookup"><span data-stu-id="deebf-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="deebf-135">选择一个特定在线商店，如果您想要为一组商店创建批处理作业，则选择一个节点。</span><span class="sxs-lookup"><span data-stu-id="deebf-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="deebf-136">单击箭头以添加您的选择。</span><span class="sxs-lookup"><span data-stu-id="deebf-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="deebf-137">单击“后台运行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="deebf-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="deebf-138">禁用“批处理”</span><span class="sxs-lookup"><span data-stu-id="deebf-138">Disable Batch processing</span></span>
6. <span data-ttu-id="deebf-139">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="deebf-139">Click Recurrence.</span></span>
7. <span data-ttu-id="deebf-140">选择“结束日期”选项</span><span class="sxs-lookup"><span data-stu-id="deebf-140">Select End After option</span></span>
8. <span data-ttu-id="deebf-141">在“结束日期”字段中，输入 1。</span><span class="sxs-lookup"><span data-stu-id="deebf-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="deebf-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-142">Click OK.</span></span>
10. <span data-ttu-id="deebf-143">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="deebf-144">计划重复执行的订单同步</span><span class="sxs-lookup"><span data-stu-id="deebf-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="deebf-145">此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。</span><span class="sxs-lookup"><span data-stu-id="deebf-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="deebf-146">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="deebf-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="deebf-147">转至“所有工作区”>“商店财务”。</span><span class="sxs-lookup"><span data-stu-id="deebf-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="deebf-148">单击“同步订单”。</span><span class="sxs-lookup"><span data-stu-id="deebf-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="deebf-149">在“组织层次结构”字段中，选择“商店(按地区)”。</span><span class="sxs-lookup"><span data-stu-id="deebf-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="deebf-150">选择一个特定在线商店，如果您想要为一组商店创建批处理作业，则选择一个节点。</span><span class="sxs-lookup"><span data-stu-id="deebf-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="deebf-151">单击箭头以添加您的选择。</span><span class="sxs-lookup"><span data-stu-id="deebf-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="deebf-152">单击“后台运行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="deebf-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="deebf-153">启用“批处理”</span><span class="sxs-lookup"><span data-stu-id="deebf-153">Enable Batch processing</span></span>
6. <span data-ttu-id="deebf-154">单击“重复执行”。</span><span class="sxs-lookup"><span data-stu-id="deebf-154">Click Recurrence.</span></span>
7. <span data-ttu-id="deebf-155">选择“无结束日期”选项。</span><span class="sxs-lookup"><span data-stu-id="deebf-155">Select the No end date option.</span></span>
8. <span data-ttu-id="deebf-156">在“计数”字段中，输入运行之间以分钟为单位的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="deebf-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="deebf-157">通常为 2-20</span><span class="sxs-lookup"><span data-stu-id="deebf-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="deebf-158">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-158">Click OK.</span></span>
10. <span data-ttu-id="deebf-159">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="deebf-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="deebf-160">此流程中涉及的数据实体</span><span class="sxs-lookup"><span data-stu-id="deebf-160">Data entities involved in the process</span></span>

- <span data-ttu-id="deebf-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="deebf-161">RetailTransactionTable</span></span>
- <span data-ttu-id="deebf-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="deebf-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="deebf-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="deebf-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="deebf-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="deebf-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="deebf-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="deebf-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="deebf-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="deebf-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="deebf-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="deebf-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="deebf-171">RetailTransactionAttributeTrans</span></span>
