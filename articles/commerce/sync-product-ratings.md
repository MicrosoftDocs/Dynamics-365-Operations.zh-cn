---
title: 在 Dynamics 365 Commerce 中同步产品评分
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中同步产品评分。
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006277"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="dbdd3-103">在 Dynamics 365 Commerce 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="dbdd3-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbdd3-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中同步产品评分。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbdd3-105">概览</span><span class="sxs-lookup"><span data-stu-id="dbdd3-105">Overview</span></span>

<span data-ttu-id="dbdd3-106">若要在全渠道（如销售点 (POS)）中和在呼叫中心中使用产品评分，必须将评分和评价服务中的产品评分导入到 Commerce 渠道数据库中。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="dbdd3-107">当产品评分在全渠道中可用时，可以在客户与销售助理交互时，直接帮助客户。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="dbdd3-108">此主题介绍以下任务：</span><span class="sxs-lookup"><span data-stu-id="dbdd3-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="dbdd3-109">将 **产品评分同步作业** 配置为批处理作业来同步来自 **评分和评价服务** 的产品评分。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="dbdd3-110">验证产品评分同步的批处理作业是否成功。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="dbdd3-111">使产品评分在 POS 可用。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="dbdd3-112">配置批处理作业以同步产品评分</span><span class="sxs-lookup"><span data-stu-id="dbdd3-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbdd3-113">首先，确保安装 Dynamics 365 Commerce 版本 10.0.6 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="dbdd3-114">初始化商业调度</span><span class="sxs-lookup"><span data-stu-id="dbdd3-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="dbdd3-115">若要初始化商业调度，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="dbdd3-116">转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 初始化商业调度**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="dbdd3-117">也可以搜索“初始化商业调度”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="dbdd3-118">在 **初始化商业调度** 对话框中，确保 **删除现有配置** 选项设置为 **否**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="dbdd3-119">验证 RetailProductRating 子作业</span><span class="sxs-lookup"><span data-stu-id="dbdd3-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="dbdd3-120">若要验证是否存在 **RetailProductRating** 子作业，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="dbdd3-121">转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 调度子作业**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="dbdd3-122">也可以搜索“调度子作业”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="dbdd3-123">在子作业列表中，找到或搜索 **RetailProductRating** 子作业。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="dbdd3-124">下图显示 Commerce 中的子作业详细信息的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![RetailProductRating 子作业的详细信息](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="dbdd3-126">如果找不到 **RetailProductRating** 子作业，说明在初始化商业调度之前，您可能已运行了 **同步产品评分** 作业和 **1040 CDX** 作业。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="dbdd3-127">在此情况下，请执行以下步骤运行 **完全数据同步** 作业。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="dbdd3-128">转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 渠道数据库**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="dbdd3-129">也可以搜索“渠道数据库”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="dbdd3-130">选择要同步的渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="dbdd3-131">在操作窗格中，选择 **完全数据同步**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="dbdd3-132">在 **选择配送计划** 下拉对话框中，选择 **1040 - 产品**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="dbdd3-133">重复上一过程的步骤，以便验证是否已创建了 **RetailProductRating** 子作业。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="dbdd3-134">导入产品评分</span><span class="sxs-lookup"><span data-stu-id="dbdd3-134">Import product ratings</span></span>

<span data-ttu-id="dbdd3-135">若要将产品评分从评分和评价服务导入到 Commerce 中，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="dbdd3-136">转到 **Retail 和 Commerce \> 总部设置 \> 商业调度 \> 同步产品评分作业**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="dbdd3-137">也可以搜索“同步产品评分作业”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="dbdd3-138">在 **提取产品评分** 对话框的 **在后台运行** 快速选项卡中，选择 **重复执行**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="dbdd3-139">在 **定义重复项** 对话框中，设置重复执行模式。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="dbdd3-140">（建议值为两小时。）安排的重复周期不应低于一小时。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="dbdd3-141">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-141">Select **OK**.</span></span>
1. <span data-ttu-id="dbdd3-142">将 **批处理** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="dbdd3-143">此设置可帮助确保您可以审核日志和验证批处理作业的运行状态。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="dbdd3-144">选择 **确定** 安排批处理作业。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="dbdd3-145">下图显示 Commerce 中的批处理作业配置的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![配置同步产品评分批处理作业](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="dbdd3-147">验证产品评分同步批处理作业是否成功</span><span class="sxs-lookup"><span data-stu-id="dbdd3-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="dbdd3-148">若要验证 **同步产品评分** 批处理作业是否成功，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="dbdd3-149">转到 **Retail 和 Commerce \> 系统管理员 \> 查询 \> 批处理作业**，如果您在使用纯 Commerce 库存单位 (SKU)，则改为转到 **Retail 和 Commerce \> 查询和报表 \> 批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="dbdd3-150">也可以搜索“批处理作业”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="dbdd3-151">若要查看批处理作业的详细信息，请在批处理作业列表的 **作业描述** 列中，搜索包含“提取产品评分”的描述。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="dbdd3-152">选择作业 ID 以查看批处理作业详细信息，如计划的开始日期/时间和重复文本。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="dbdd3-153">下图显示当安排批处理作业以两小时的间隔运行时，Commerce 中的批处理作业详细信息的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![同步产品评分批处理作业的详细信息](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="dbdd3-155">使产品评分在 POS 可用</span><span class="sxs-lookup"><span data-stu-id="dbdd3-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="dbdd3-156">Dynamics 365 Commerce 中的评分和评价解决方案是全渠道解决方案。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="dbdd3-157">但是，默认情况下，POS 中不显示产品评分。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="dbdd3-158">若要在销售助理帮助店内客户时，帮助客户查看评分和评价，必须在 POS 中开启产品评分。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="dbdd3-159">若要在 POS 中开启产品评分，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="dbdd3-160">转到 **Retail 和 Commerce \> Commerce 设置 \> 参数 \> 商业参数**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="dbdd3-161">也可以搜索“商业参数”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="dbdd3-162">在 **配置参数** 选项卡中，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="dbdd3-163">输入名称（如 **RatingsAndReviews.EnableProductRatingsForRetailStores**），然后将值设置为 **true**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="dbdd3-164">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-164">Select **Save**.</span></span>
1. <span data-ttu-id="dbdd3-165">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="dbdd3-166">也可以搜索“配送计划”。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="dbdd3-167">在作业列表中，选择 **1110**（**全局配置**），然后选择 **立即运行**。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="dbdd3-168">作业成功运行之后，验证 POS 中现在是否显示产品评分。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="dbdd3-169">下图显示要在 POS 中开启产品评分所需商业参数配置的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![POS 中产品评分的商业参数配置](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="dbdd3-171">下图显示 POS 中的产品评分的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-171">The following illustration shows an example of product ratings at the POS.</span></span>

![POS 中的产品评分](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="dbdd3-173">下图显示呼叫中心渠道中的产品评分的示例。</span><span class="sxs-lookup"><span data-stu-id="dbdd3-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![呼叫中心渠道中的产品评分](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="dbdd3-175">其他资源</span><span class="sxs-lookup"><span data-stu-id="dbdd3-175">Additional resources</span></span>

[<span data-ttu-id="dbdd3-176">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="dbdd3-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="dbdd3-177">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="dbdd3-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="dbdd3-178">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="dbdd3-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="dbdd3-179">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="dbdd3-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
