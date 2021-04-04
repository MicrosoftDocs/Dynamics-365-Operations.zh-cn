---
title: 在 Finance 和 Supply Chain Management 中开具电子发票
description: 本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 099ebb56710e920f7b1453f32f23f59a80486ebf
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5486945"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a><span data-ttu-id="6aaca-103">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="6aaca-103">Issue electronic invoices in Finance and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6aaca-104">本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="6aaca-104">This topic explains how to issue electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management through the Electronic invoicing add-on.</span></span>


## <a name="feature-activation"></a><span data-ttu-id="6aaca-105">功能激活</span><span class="sxs-lookup"><span data-stu-id="6aaca-105">Feature activation</span></span>

<span data-ttu-id="6aaca-106">要通过电子开票附加产品开具电子发票，必须激活 Finance 和 Supply Chain Management 中的相应功能。</span><span class="sxs-lookup"><span data-stu-id="6aaca-106">To issue electronic invoices through the Electronic invoicing add-on, you must activate the Feature in Finance and Supply Chain Management.</span></span>

<span data-ttu-id="6aaca-107">每个功能都对应于一个特定的电子开票功能，该功能符合某个国家/地区的电子开票要求。</span><span class="sxs-lookup"><span data-stu-id="6aaca-107">Each feature corresponds to a specific electronic invoicing feature that complies with the electronic invoicing requirements for a country/region.</span></span>

<span data-ttu-id="6aaca-108">下表显示了电子开票附加产品可能支持的功能的列表。</span><span class="sxs-lookup"><span data-stu-id="6aaca-108">The following table shows the list of features that the Electronic invoicing add-on may support.</span></span>

| <span data-ttu-id="6aaca-109">姓名</span><span class="sxs-lookup"><span data-stu-id="6aaca-109">Name</span></span>                                              | <span data-ttu-id="6aaca-110">国家/地区</span><span class="sxs-lookup"><span data-stu-id="6aaca-110">Country/region</span></span> |
|---------------------------------------------------|----------------|
|<span data-ttu-id="6aaca-111">奥地利电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-111">Austrian electronic invoice</span></span>                        |<span data-ttu-id="6aaca-112">奥地利</span><span class="sxs-lookup"><span data-stu-id="6aaca-112">Austria</span></span>         |
|<span data-ttu-id="6aaca-113">比利时电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-113">Belgian electronic invoice</span></span>                         |<span data-ttu-id="6aaca-114">比利时</span><span class="sxs-lookup"><span data-stu-id="6aaca-114">Belgium</span></span>         |
|<span data-ttu-id="6aaca-115">NF-e (联邦) - 电子账单(巴西)</span><span class="sxs-lookup"><span data-stu-id="6aaca-115">NF-e  Federal - Brazilian electronic invoice</span></span>       |<span data-ttu-id="6aaca-116">巴西</span><span class="sxs-lookup"><span data-stu-id="6aaca-116">Brazil</span></span>          |
|<span data-ttu-id="6aaca-117">NFS-e - 巴西服务(城市)电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-117">NFS-e - Brazilian service (city) electronic invoice</span></span>|<span data-ttu-id="6aaca-118">巴西</span><span class="sxs-lookup"><span data-stu-id="6aaca-118">Brazil</span></span>          |
|<span data-ttu-id="6aaca-119">丹麦电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-119">Danish electronic invoice</span></span>                          |<span data-ttu-id="6aaca-120">丹麦</span><span class="sxs-lookup"><span data-stu-id="6aaca-120">Denmark</span></span>         |
|<span data-ttu-id="6aaca-121">埃及电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-121">Egyptian electronic invoice</span></span>                        |<span data-ttu-id="6aaca-122">埃及</span><span class="sxs-lookup"><span data-stu-id="6aaca-122">Egypt</span></span>           |
|<span data-ttu-id="6aaca-123">爱沙尼亚电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-123">Estonian electronic invoice</span></span>                        |<span data-ttu-id="6aaca-124">爱沙尼亚</span><span class="sxs-lookup"><span data-stu-id="6aaca-124">Estonia</span></span>         |
|<span data-ttu-id="6aaca-125">芬兰电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-125">Finnish electronic invoice</span></span>                         |<span data-ttu-id="6aaca-126">芬兰</span><span class="sxs-lookup"><span data-stu-id="6aaca-126">Finland</span></span>         |
|<span data-ttu-id="6aaca-127">法国电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-127">French electronic invoice</span></span>                          |<span data-ttu-id="6aaca-128">法国</span><span class="sxs-lookup"><span data-stu-id="6aaca-128">France</span></span>          |
|<span data-ttu-id="6aaca-129">德国电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-129">German electronic invoice</span></span>                          |<span data-ttu-id="6aaca-130">德国</span><span class="sxs-lookup"><span data-stu-id="6aaca-130">Germany</span></span>         |
|<span data-ttu-id="6aaca-131">PEPPOL - 全球电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-131">PEPPOL - Global electronic invoice</span></span>                 |<span data-ttu-id="6aaca-132">全局</span><span class="sxs-lookup"><span data-stu-id="6aaca-132">Global</span></span>          |
|<span data-ttu-id="6aaca-133">意大利电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-133">Italian electronic invoice</span></span>                         |<span data-ttu-id="6aaca-134">意大利</span><span class="sxs-lookup"><span data-stu-id="6aaca-134">Italy</span></span>           |
|<span data-ttu-id="6aaca-135">CFDI - 墨西哥电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-135">CFDI - Mexican electronic invoice</span></span>                  |<span data-ttu-id="6aaca-136">墨西哥</span><span class="sxs-lookup"><span data-stu-id="6aaca-136">Mexico</span></span>          |
|<span data-ttu-id="6aaca-137">荷兰电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-137">Dutch electronic invoice</span></span>                           |<span data-ttu-id="6aaca-138">荷兰</span><span class="sxs-lookup"><span data-stu-id="6aaca-138">Netherlands</span></span>     |
|<span data-ttu-id="6aaca-139">挪威电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-139">Norwegian electronic invoice</span></span>                       |<span data-ttu-id="6aaca-140">挪威</span><span class="sxs-lookup"><span data-stu-id="6aaca-140">Norway</span></span>          |
|<span data-ttu-id="6aaca-141">西班牙电子账单</span><span class="sxs-lookup"><span data-stu-id="6aaca-141">Spanish electronic invoice</span></span>                         |<span data-ttu-id="6aaca-142">西班牙</span><span class="sxs-lookup"><span data-stu-id="6aaca-142">Spain</span></span>           |

<span data-ttu-id="6aaca-143">在存在国家/地区本地化范围内支持的旧版电子开票功能时，如果激活其中一项功能，则会关闭旧功能，并允许通过电子开票附加产品开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="6aaca-143">When there is a legacy Electronic invoicing feature that is supported in a country/region's localizations scope, activating one of these features turns off the legacy feature and enables electronic invoices to be issued through the Electronic invoicing add-on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6aaca-144">启用电子开票附加产品集成功能后，默认情况下将禁用新电子开票体验。</span><span class="sxs-lookup"><span data-stu-id="6aaca-144">After the Electronic invoicing add-on integration feature is enabled, the new Electronic invoicing experience is turned off by default.</span></span> <span data-ttu-id="6aaca-145">您可以使用功能概念使用特定于国家/地区的功能选择性地为法人启用新体验。</span><span class="sxs-lookup"><span data-stu-id="6aaca-145">You can use the feature concept to selectively enable new experiences for legal entities using country/region-specific functionality.</span></span> <span data-ttu-id="6aaca-146">**全局** 选项针对表中未明确列出的其余县/地区控制新体验。</span><span class="sxs-lookup"><span data-stu-id="6aaca-146">The **Global** option controls the new experience for the remaining county/regions that aren't specifically listed in the table.</span></span>

## <a name="submit-electronic-documents"></a><span data-ttu-id="6aaca-147">提交电子单据</span><span class="sxs-lookup"><span data-stu-id="6aaca-147">Submit electronic documents</span></span>

<span data-ttu-id="6aaca-148">提交电子单据的流程表示 Finance 和 Supply Chain Management 与电子开票附加产品之间的单点通信。</span><span class="sxs-lookup"><span data-stu-id="6aaca-148">The process of submitting electronic documents represents the single point of communication between Finance and Supply Chain Management and the Electronic invoicing add-on.</span></span> <span data-ttu-id="6aaca-149">在每个提交事件期间，通信流都是双向的：</span><span class="sxs-lookup"><span data-stu-id="6aaca-149">During each submission event, the communication flows in both directions:</span></span>

- <span data-ttu-id="6aaca-150">**从 Finance 和 Supply Chain Management 到电子开票附加产品** – Finance 和 Supply Chain Management 将摘要发票发送到电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="6aaca-150">**From Finance and Supply Chain Management to the Electronic invoicing add-on** – Finance and Supply Chain Management send the abstract invoices to the Electronic invoicing add-on.</span></span> <span data-ttu-id="6aaca-151">根据需要，它们还发送配置为电子开票功能一部分的变量内容。</span><span class="sxs-lookup"><span data-stu-id="6aaca-151">As required, they also send the contents of variables that were configured as part of the electronic invoicing features.</span></span>
- <span data-ttu-id="6aaca-152">**从电子开票附加产品到 Finance 和 Supply Chain Management** – 根据电子开票功能，Finance 和 Supply Chain Management 从电子开票附加产品接收有关先前提交的发票处理结果的更新。</span><span class="sxs-lookup"><span data-stu-id="6aaca-152">**From the Electronic invoicing add-on to Finance and Supply Chain Management** – Depending on the electronic invoicing feature, Finance and Supply Chain Management receive updates from the Electronic invoicing add-on about the processing results of invoices that were previously submitted.</span></span> <span data-ttu-id="6aaca-153">另外还接收配置为电子开票功能一部分的变量内容。</span><span class="sxs-lookup"><span data-stu-id="6aaca-153">They also receive the contents of variables that were configured as part of the electronic invoicing features.</span></span>

<span data-ttu-id="6aaca-154">要将电子单据提交到电子开票附加产品，在 Finance 和 Supply Chain Management 中，转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 提交电子单据**。</span><span class="sxs-lookup"><span data-stu-id="6aaca-154">To submit electronic documents to the Electronic invoicing add-on, in Finance and Supply Chain Management, go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Submit electronic documents**.</span></span>

<span data-ttu-id="6aaca-155">起点是一个已过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="6aaca-155">The starting point is a posted invoice.</span></span> <span data-ttu-id="6aaca-156">此发票可以来自不同的来源，如销售订单、项目发票或普通发票。</span><span class="sxs-lookup"><span data-stu-id="6aaca-156">This invoice can come from different origins, such as sales orders, project invoices, or free text invoices.</span></span>

<span data-ttu-id="6aaca-157">提交流程可以手动运行，也可以在后台运行。</span><span class="sxs-lookup"><span data-stu-id="6aaca-157">The submission process can be run manually or in the background.</span></span>

- <span data-ttu-id="6aaca-158">**手动执行** – 对于手动执行，必须使用 **筛选器** 选项定义必须提交的文档范围。</span><span class="sxs-lookup"><span data-stu-id="6aaca-158">**Manual execution** – For manual execution, you must use the **Filter** option to define the range of documents that must be submitted.</span></span> <span data-ttu-id="6aaca-159">在 **筛选器** 页上，您可以配置自己的查询来选择必须提交的已过帐发票。</span><span class="sxs-lookup"><span data-stu-id="6aaca-159">On the **Filters** page, you can configure your own query to select the posted invoices that must be submitted.</span></span> <span data-ttu-id="6aaca-160">选择之后，您必须手动开始执行处理并等待它完成运行。</span><span class="sxs-lookup"><span data-stu-id="6aaca-160">After the selection is made, you must manually start execution of the processing and wait for it to finish running.</span></span> <span data-ttu-id="6aaca-161">处理完成后，操作中心中的消息将显示已成功提交的电子单据数。</span><span class="sxs-lookup"><span data-stu-id="6aaca-161">When the processing is completed, a message in the Action center shows the number of electronic documents that have been successfully submitted.</span></span>
- <span data-ttu-id="6aaca-162">**后台执行** – 后台执行运行，无需您登录或让提交对话框保持打开。</span><span class="sxs-lookup"><span data-stu-id="6aaca-162">**Background execution** – Background execution runs without requiring that you be signed in or keep the submission dialog box open.</span></span> <span data-ttu-id="6aaca-163">您可以计划流程的运行并定义执行频率。</span><span class="sxs-lookup"><span data-stu-id="6aaca-163">You can schedule the process to run and define the frequency of execution.</span></span>

## <a name="view-the-submission-logs"></a><span data-ttu-id="6aaca-164">查看提交日志</span><span class="sxs-lookup"><span data-stu-id="6aaca-164">View the submission logs</span></span>

<span data-ttu-id="6aaca-165">在 Finance 和 Supply Chain Management 中，您可以使用提交日志来查看处理向电子开票附加产品的提交的结果。</span><span class="sxs-lookup"><span data-stu-id="6aaca-165">In Finance and Supply Chain Management, you can use the submission logs to view the results of processing the submission to the Electronic invoicing add-on.</span></span> <span data-ttu-id="6aaca-166">转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 电子单据提交**，然后 **文档类型** 字段中，选择一个值来筛选日志显示的发票类型。</span><span class="sxs-lookup"><span data-stu-id="6aaca-166">Go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Electronic document submission**, and then, in the **Document type** field, select a value to filter the type of invoices that the logs show.</span></span>

<span data-ttu-id="6aaca-167">有三个可能的提交状态：</span><span class="sxs-lookup"><span data-stu-id="6aaca-167">There are three possible submission statuses:</span></span>

- <span data-ttu-id="6aaca-168">**已计划** – 电子开票附加产品已从 Finance 和 Supply Chain Management 收到提交，电子开票功能正在进行处理。</span><span class="sxs-lookup"><span data-stu-id="6aaca-168">**Scheduled** – The Electronic invoicing add-on received the submission from Finance and Supply Chain Management, and processing of the electronic invoicing feature is in progress.</span></span>
- <span data-ttu-id="6aaca-169">**已完成** – 电子开票附加产品已成功处理电子开票功能，因为它被配置为运行该功能。</span><span class="sxs-lookup"><span data-stu-id="6aaca-169">**Completed** – The Electronic invoicing add-on successfully processed the electronic invoicing feature as it was configured to run it.</span></span>
- <span data-ttu-id="6aaca-170">**失败** – 电子开票附加产品在处理电子开票功能期间遇到错误或因异常停止。</span><span class="sxs-lookup"><span data-stu-id="6aaca-170">**Failed** – The Electronic invoicing add-on encountered an error or was stopped by an exception during processing of the electronic invoicing feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6aaca-171">提交状态是指电子开票附加产品对电子开票功能执行的处理的状态。</span><span class="sxs-lookup"><span data-stu-id="6aaca-171">The submission status refers to the status of the processing that the Electronic invoicing add-on does on the electronic invoicing feature.</span></span> <span data-ttu-id="6aaca-172">不是电子发票本身的最终状态。</span><span class="sxs-lookup"><span data-stu-id="6aaca-172">It doesn't refer to the final status of the electronic invoice itself.</span></span>
>
> <span data-ttu-id="6aaca-173">例如，如果必须将电子发票提交到外部 Web 服务进行审核，提交状态可能是 **已完成**，但是电子发票的状态可能是 **已拒绝**。</span><span class="sxs-lookup"><span data-stu-id="6aaca-173">For example, if an electronic invoice must be submitted to an external web service for approval, the submission status might be **Completed**, but the status of the electronic invoice might be **Rejected**.</span></span> <span data-ttu-id="6aaca-174">在此例中，电子开票附加产品可以成功处理电子开票功能，因为它被配置为处理该功能。</span><span class="sxs-lookup"><span data-stu-id="6aaca-174">In this case, the Electronic invoicing add-on was able to successfully process the electronic invoicing feature as it's configured to process that feature.</span></span> <span data-ttu-id="6aaca-175">但是，电子发票被拒绝，因为它不符合 Web 服务为发票审核设定的条件。</span><span class="sxs-lookup"><span data-stu-id="6aaca-175">However, the electronic invoice was rejected because it didn't meet the criteria that the web service established for invoice approval.</span></span>

<span data-ttu-id="6aaca-176">提交日志包括以下附加功能：</span><span class="sxs-lookup"><span data-stu-id="6aaca-176">The submission logs include the following additional functions:</span></span>

- <span data-ttu-id="6aaca-177">**提交详细信息** – 查看主要提交的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6aaca-177">**Submission details** – View the details of the main submission.</span></span> <span data-ttu-id="6aaca-178">可视化显示在电子开票功能中配置的操作的完整执行日志。</span><span class="sxs-lookup"><span data-stu-id="6aaca-178">The visualization shows the complete execution log of the actions that are configured in the electronic invoicing feature.</span></span> <span data-ttu-id="6aaca-179">另外还允许用户下载在处理过程中创建的文件。</span><span class="sxs-lookup"><span data-stu-id="6aaca-179">It also lets users download the files that are created during the processing.</span></span> <span data-ttu-id="6aaca-180">在发票必须由外部 Web 服务审核的情况下，它让用户可以查看发票的状态。</span><span class="sxs-lookup"><span data-stu-id="6aaca-180">In scenarios where the invoice must be approved by an external web service, it lets users view the status of the invoice.</span></span>
- <span data-ttu-id="6aaca-181">**相关提交** – 查看子提交的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6aaca-181">**Related submissions** – View the details of child submissions.</span></span>
- <span data-ttu-id="6aaca-182">**取消提交** – 此功能在必须由外部 Web 服务审核电子发票的情况下启用特殊提交流程。</span><span class="sxs-lookup"><span data-stu-id="6aaca-182">**Cancel submissions** – This function enables a special submission process in scenarios where the electronic invoice must be approved by an external web service.</span></span> <span data-ttu-id="6aaca-183">它指示电子开票附加产品向 Web 服务发送一条特定消息，用于取消 Web 服务数据库中已审核电子发票的状态。</span><span class="sxs-lookup"><span data-stu-id="6aaca-183">It instructs the Electronic invoicing add-on to send the web service a specific message that is intended to cancel the status of an approved electronic invoice in the web service database.</span></span>
- <span data-ttu-id="6aaca-184">**重新提交文档** – 重新提交已经提交到电子开票附加产品的电子单据。</span><span class="sxs-lookup"><span data-stu-id="6aaca-184">**Resubmit document** – Resubmit an electronic document that has already been submitted to the Electronic invoicing add-on.</span></span> <span data-ttu-id="6aaca-185">将在 **提交详细信息** 页创建全新的日志。</span><span class="sxs-lookup"><span data-stu-id="6aaca-185">A whole new log is created on the **Submission details** page.</span></span>
- <span data-ttu-id="6aaca-186">**发送相关提交**</span><span class="sxs-lookup"><span data-stu-id="6aaca-186">**Send related submission**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
