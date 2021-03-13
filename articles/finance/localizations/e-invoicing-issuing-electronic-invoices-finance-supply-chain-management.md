---
title: 在 Finance 和 Supply Chain Management 中开具电子发票
description: 本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104349"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a><span data-ttu-id="427e9-103">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="427e9-103">Issue electronic invoices in Finance and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="427e9-104">本主题说明如何通过电子开票附加产品在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="427e9-104">This topic explains how to issue electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management through the Electronic invoicing add-on.</span></span>


## <a name="feature-activation"></a><span data-ttu-id="427e9-105">功能激活</span><span class="sxs-lookup"><span data-stu-id="427e9-105">Feature activation</span></span>

<span data-ttu-id="427e9-106">要开始通过电子开票附加产品开具电子发票，必须激活 Finance 和 Supply Chain Management 中的功能引用。</span><span class="sxs-lookup"><span data-stu-id="427e9-106">To start issuing electronic invoices through the Electronic invoicing add-on, it is necessary to activate the Feature reference in Finance and Supply Chain Management.</span></span>

<span data-ttu-id="427e9-107">每个功能引用对应于一个特定的电子开票功能，该功能符合某个国家/地区的电子开票要求。</span><span class="sxs-lookup"><span data-stu-id="427e9-107">Each Feature reference corresponds to a specific electronic invoicing feature that complies to the electronic invoicing requirements from a country/region.</span></span>

<span data-ttu-id="427e9-108">下表显示了电子开票附加产品支持的功能引用的列表。</span><span class="sxs-lookup"><span data-stu-id="427e9-108">The following table shows the list of feature References that the Electronic invoicing add-on supports.</span></span>

| <span data-ttu-id="427e9-109">功能引用</span><span class="sxs-lookup"><span data-stu-id="427e9-109">Feature reference</span></span> | <span data-ttu-id="427e9-110">姓名</span><span class="sxs-lookup"><span data-stu-id="427e9-110">Name</span></span>                                              | <span data-ttu-id="427e9-111">国家/地区</span><span class="sxs-lookup"><span data-stu-id="427e9-111">Country/region</span></span> |
|-------------------|---------------------------------------------------|----------------|
| <span data-ttu-id="427e9-112">BR-00053</span><span class="sxs-lookup"><span data-stu-id="427e9-112">BR-00053</span></span>          | <span data-ttu-id="427e9-113">NF-e 联邦 - 巴西电子发票</span><span class="sxs-lookup"><span data-stu-id="427e9-113">NF-e Federal - Brazilian electronic invoice</span></span>       | <span data-ttu-id="427e9-114">巴西</span><span class="sxs-lookup"><span data-stu-id="427e9-114">Brazil</span></span>         |
| <span data-ttu-id="427e9-115">BR-00095</span><span class="sxs-lookup"><span data-stu-id="427e9-115">BR-00095</span></span>          | <span data-ttu-id="427e9-116">NFS-e 巴西电子发票</span><span class="sxs-lookup"><span data-stu-id="427e9-116">NFS-e Brazilian electronic invoices</span></span>               | <span data-ttu-id="427e9-117">巴西</span><span class="sxs-lookup"><span data-stu-id="427e9-117">Brazil</span></span>         |
| <span data-ttu-id="427e9-118">DK-00001</span><span class="sxs-lookup"><span data-stu-id="427e9-118">DK-00001</span></span>          | <span data-ttu-id="427e9-119">向公共部门开具电子发票 (OIOUBL) – DK</span><span class="sxs-lookup"><span data-stu-id="427e9-119">E-invoicing to the public sector (OIOUBL) – DK</span></span>    | <span data-ttu-id="427e9-120">丹麦</span><span class="sxs-lookup"><span data-stu-id="427e9-120">Denmark</span></span>        |
| <span data-ttu-id="427e9-121">EG-00008</span><span class="sxs-lookup"><span data-stu-id="427e9-121">EG-00008</span></span>          | <span data-ttu-id="427e9-122">针对埃及的电子开单</span><span class="sxs-lookup"><span data-stu-id="427e9-122">E-invoicing for Egypt</span></span>                             | <span data-ttu-id="427e9-123">埃及</span><span class="sxs-lookup"><span data-stu-id="427e9-123">Egypt</span></span>          |
| <span data-ttu-id="427e9-124">ES-00025</span><span class="sxs-lookup"><span data-stu-id="427e9-124">ES-00025</span></span>          | <span data-ttu-id="427e9-125">向公共部门开具的电子发票</span><span class="sxs-lookup"><span data-stu-id="427e9-125">Electronic Invoice to the public sector</span></span>           | <span data-ttu-id="427e9-126">西班牙</span><span class="sxs-lookup"><span data-stu-id="427e9-126">Spain</span></span>          |
| <span data-ttu-id="427e9-127">EUR-00023</span><span class="sxs-lookup"><span data-stu-id="427e9-127">EUR-00023</span></span>         | <span data-ttu-id="427e9-128">向公共部门开具的欧盟电子发票</span><span class="sxs-lookup"><span data-stu-id="427e9-128">European Union E-invoicing to Public sector</span></span>       | <span data-ttu-id="427e9-129">欧洲</span><span class="sxs-lookup"><span data-stu-id="427e9-129">Europe</span></span>         |
| <span data-ttu-id="427e9-130">ITA-00036</span><span class="sxs-lookup"><span data-stu-id="427e9-130">ITA-00036</span></span>         | <span data-ttu-id="427e9-131">IT - 向公共部门开具电子发票 (FatturaPA)</span><span class="sxs-lookup"><span data-stu-id="427e9-131">IT - E-invoicing to the public sector (FatturaPA)</span></span> | <span data-ttu-id="427e9-132">意大利</span><span class="sxs-lookup"><span data-stu-id="427e9-132">Italy</span></span>          |
| <span data-ttu-id="427e9-133">MX-00010</span><span class="sxs-lookup"><span data-stu-id="427e9-133">MX-00010</span></span>          | <span data-ttu-id="427e9-134">电子开单 CFDI</span><span class="sxs-lookup"><span data-stu-id="427e9-134">E-invoicing CFDI</span></span>                                  | <span data-ttu-id="427e9-135">墨西哥</span><span class="sxs-lookup"><span data-stu-id="427e9-135">Mexico</span></span>         |
| <span data-ttu-id="427e9-136">MX-00016</span><span class="sxs-lookup"><span data-stu-id="427e9-136">MX-00016</span></span>          | <span data-ttu-id="427e9-137">电子开票 CFDI - 取消流程</span><span class="sxs-lookup"><span data-stu-id="427e9-137">E-invoicing CFDI - cancellation process</span></span>           | <span data-ttu-id="427e9-138">墨西哥</span><span class="sxs-lookup"><span data-stu-id="427e9-138">Mexico</span></span>         |

<span data-ttu-id="427e9-139">在存在支持国家/地区本地化范围的旧版电子开票功能的情况下，激活功能引用可以通过电子开票附加产品开具电子发票，同时关闭前一个功能。</span><span class="sxs-lookup"><span data-stu-id="427e9-139">In the cases where there is a legacy electronic invoicing feature, supported the country localizations scope, the activation of the Feature reference enables the issuing of electronic invoices through the Electronic invoicing add-on and turns-off the former feature.</span></span>

## <a name="submit-electronic-documents"></a><span data-ttu-id="427e9-140">提交电子单据</span><span class="sxs-lookup"><span data-stu-id="427e9-140">Submit electronic documents</span></span>

<span data-ttu-id="427e9-141">提交电子单据的流程表示 Finance 和 Supply Chain Management 与电子开票附加产品之间的单点通信。</span><span class="sxs-lookup"><span data-stu-id="427e9-141">The process of submitting electronic documents represents the single point of communication between Finance and Supply Chain Management and the Electronic invoicing add-on.</span></span> <span data-ttu-id="427e9-142">在每个提交事件期间，通信流都是双向的：</span><span class="sxs-lookup"><span data-stu-id="427e9-142">During each submission event, the communication flows in both directions:</span></span>

- <span data-ttu-id="427e9-143">**从 Finance 和 Supply Chain Management 到电子开票附加产品** – Finance 和 Supply Chain Management 将摘要发票发送到电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="427e9-143">**From Finance and Supply Chain Management to the Electronic invoicing add-on** – Finance and Supply Chain Management send the abstract invoices to the Electronic invoicing add-on.</span></span> <span data-ttu-id="427e9-144">根据需要，它们还发送配置为电子开票功能一部分的变量内容。</span><span class="sxs-lookup"><span data-stu-id="427e9-144">As required, they also send the contents of variables that were configured as part of the electronic invoicing features.</span></span>
- <span data-ttu-id="427e9-145">**从电子开票附加产品到 Finance 和 Supply Chain Management** – 根据电子开票功能，Finance 和 Supply Chain Management 从电子开票附加产品接收有关先前提交的发票处理结果的更新。</span><span class="sxs-lookup"><span data-stu-id="427e9-145">**From the Electronic invoicing add-on to Finance and Supply Chain Management** – Depending on the electronic invoicing feature, Finance and Supply Chain Management receive updates from the Electronic invoicing add-on about the processing results of invoices that were previously submitted.</span></span> <span data-ttu-id="427e9-146">另外还接收配置为电子开票功能一部分的变量内容。</span><span class="sxs-lookup"><span data-stu-id="427e9-146">They also receive the contents of variables that were configured as part of the electronic invoicing features.</span></span>

<span data-ttu-id="427e9-147">要将电子单据提交到电子开票附加产品，在 Finance 和 Supply Chain Management 中，转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 提交电子单据**。</span><span class="sxs-lookup"><span data-stu-id="427e9-147">To submit electronic documents to the Electronic invoicing add-on, in Finance and Supply Chain Management, go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Submit electronic documents**.</span></span>

<span data-ttu-id="427e9-148">起点是一个已过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="427e9-148">The starting point is a posted invoice.</span></span> <span data-ttu-id="427e9-149">此发票可以来自不同的来源，如销售订单、项目发票或普通发票。</span><span class="sxs-lookup"><span data-stu-id="427e9-149">This invoice can come from different origins, such as sales orders, project invoices, or free text invoices.</span></span>

<span data-ttu-id="427e9-150">提交流程可以手动运行，也可以在后台运行。</span><span class="sxs-lookup"><span data-stu-id="427e9-150">The submission process can be run manually or in the background.</span></span>

- <span data-ttu-id="427e9-151">**手动执行** – 对于手动执行，必须使用 **筛选器** 选项定义必须提交的文档范围。</span><span class="sxs-lookup"><span data-stu-id="427e9-151">**Manual execution** – For manual execution, you must use the **Filter** option to define the range of documents that must be submitted.</span></span> <span data-ttu-id="427e9-152">在 **筛选器** 页上，您可以配置自己的查询来选择必须提交的已过帐发票。</span><span class="sxs-lookup"><span data-stu-id="427e9-152">On the **Filters** page, you can configure your own query to select the posted invoices that must be submitted.</span></span> <span data-ttu-id="427e9-153">选择之后，您必须手动开始执行处理并等待它完成运行。</span><span class="sxs-lookup"><span data-stu-id="427e9-153">After the selection is made, you must manually start execution of the processing and wait for it to finish running.</span></span> <span data-ttu-id="427e9-154">处理完成后，操作中心中的消息将显示已成功提交的电子单据数。</span><span class="sxs-lookup"><span data-stu-id="427e9-154">When the processing is completed, a message in the Action center shows the number of electronic documents that have been successfully submitted.</span></span>
- <span data-ttu-id="427e9-155">**后台执行** – 后台执行运行，无需您登录或让提交对话框保持打开。</span><span class="sxs-lookup"><span data-stu-id="427e9-155">**Background execution** – Background execution runs without requiring that you be signed in or keep the submission dialog box open.</span></span> <span data-ttu-id="427e9-156">您可以计划流程的运行并定义执行频率。</span><span class="sxs-lookup"><span data-stu-id="427e9-156">You can schedule the process to run and define the frequency of execution.</span></span>

## <a name="view-the-submission-logs"></a><span data-ttu-id="427e9-157">查看提交日志</span><span class="sxs-lookup"><span data-stu-id="427e9-157">View the submission logs</span></span>

<span data-ttu-id="427e9-158">在 Finance 和 Supply Chain Management 中，您可以使用提交日志来查看处理向电子开票附加产品的提交的结果。</span><span class="sxs-lookup"><span data-stu-id="427e9-158">In Finance and Supply Chain Management, you can use the submission logs to view the results of processing the submission to the Electronic invoicing add-on.</span></span> <span data-ttu-id="427e9-159">转到 **组织管理 &gt; 定期 &gt; 电子单据 &gt; 电子单据提交**，然后 **文档类型** 字段中，选择一个值来筛选日志显示的发票类型。</span><span class="sxs-lookup"><span data-stu-id="427e9-159">Go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Electronic document submission**, and then, in the **Document type** field, select a value to filter the type of invoices that the logs show.</span></span>

<span data-ttu-id="427e9-160">有三个可能的提交状态：</span><span class="sxs-lookup"><span data-stu-id="427e9-160">There are three possible submission statuses:</span></span>

- <span data-ttu-id="427e9-161">**已计划** – 电子开票附加产品已从 Finance 和 Supply Chain Management 收到提交，电子开票功能正在进行处理。</span><span class="sxs-lookup"><span data-stu-id="427e9-161">**Scheduled** – The Electronic invoicing add-on received the submission from Finance and Supply Chain Management, and processing of the electronic invoicing feature is in progress.</span></span>
- <span data-ttu-id="427e9-162">**已完成** – 电子开票附加产品已成功处理电子开票功能，因为它被配置为运行该功能。</span><span class="sxs-lookup"><span data-stu-id="427e9-162">**Completed** – The Electronic invoicing add-on successfully processed the electronic invoicing feature as it was configured to run it.</span></span>
- <span data-ttu-id="427e9-163">**失败** – 电子开票附加产品在处理电子开票功能期间遇到错误或因异常停止。</span><span class="sxs-lookup"><span data-stu-id="427e9-163">**Failed** – The Electronic invoicing add-on encountered an error or was stopped by an exception during processing of the electronic invoicing feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="427e9-164">提交状态是指电子开票附加产品对电子开票功能执行的处理的状态。</span><span class="sxs-lookup"><span data-stu-id="427e9-164">The submission status refers to the status of the processing that the Electronic invoicing add-on does on the electronic invoicing feature.</span></span> <span data-ttu-id="427e9-165">不是电子发票本身的最终状态。</span><span class="sxs-lookup"><span data-stu-id="427e9-165">It doesn't refer to the final status of the electronic invoice itself.</span></span>
>
> <span data-ttu-id="427e9-166">例如，如果必须将电子发票提交到外部 Web 服务进行审核，提交状态可能是 **已完成**，但是电子发票的状态可能是 **已拒绝**。</span><span class="sxs-lookup"><span data-stu-id="427e9-166">For example, if an electronic invoice must be submitted to an external web service for approval, the submission status might be **Completed**, but the status of the electronic invoice might be **Rejected**.</span></span> <span data-ttu-id="427e9-167">在此例中，电子开票附加产品可以成功处理电子开票功能，因为它被配置为处理该功能。</span><span class="sxs-lookup"><span data-stu-id="427e9-167">In this case, the Electronic invoicing add-on was able to successfully process the electronic invoicing feature as it's configured to process that feature.</span></span> <span data-ttu-id="427e9-168">但是，电子发票被拒绝，因为它不符合 Web 服务为发票审核设定的条件。</span><span class="sxs-lookup"><span data-stu-id="427e9-168">However, the electronic invoice was rejected because it didn't meet the criteria that the web service established for invoice approval.</span></span>

<span data-ttu-id="427e9-169">提交日志包括以下附加功能：</span><span class="sxs-lookup"><span data-stu-id="427e9-169">The submission logs include the following additional functions:</span></span>

- <span data-ttu-id="427e9-170">**提交详细信息** – 查看主要提交的详细信息。</span><span class="sxs-lookup"><span data-stu-id="427e9-170">**Submission details** – View the details of the main submission.</span></span> <span data-ttu-id="427e9-171">可视化显示在电子开票功能中配置的操作的完整执行日志。</span><span class="sxs-lookup"><span data-stu-id="427e9-171">The visualization shows the complete execution log of the actions that are configured in the electronic invoicing feature.</span></span> <span data-ttu-id="427e9-172">另外还允许用户下载在处理过程中创建的文件。</span><span class="sxs-lookup"><span data-stu-id="427e9-172">It also lets users download the files that are created during the processing.</span></span> <span data-ttu-id="427e9-173">在发票必须由外部 Web 服务审核的情况下，它让用户可以查看发票的状态。</span><span class="sxs-lookup"><span data-stu-id="427e9-173">In scenarios where the invoice must be approved by an external web service, it lets users view the status of the invoice.</span></span>
- <span data-ttu-id="427e9-174">**相关提交** – 查看子提交的详细信息。</span><span class="sxs-lookup"><span data-stu-id="427e9-174">**Related submissions** – View the details of child submissions.</span></span>
- <span data-ttu-id="427e9-175">**取消提交** – 此功能在必须由外部 Web 服务审核电子发票的情况下启用特殊提交流程。</span><span class="sxs-lookup"><span data-stu-id="427e9-175">**Cancel submissions** – This function enables a special submission process in scenarios where the electronic invoice must be approved by an external web service.</span></span> <span data-ttu-id="427e9-176">它指示电子开票附加产品向 Web 服务发送一条特定消息，用于取消 Web 服务数据库中已审核电子发票的状态。</span><span class="sxs-lookup"><span data-stu-id="427e9-176">It instructs the Electronic invoicing add-on to send the web service a specific message that is intended to cancel the status of an approved electronic invoice in the web service database.</span></span>
- <span data-ttu-id="427e9-177">**重新提交文档** – 重新提交已经提交到电子开票附加产品的电子单据。</span><span class="sxs-lookup"><span data-stu-id="427e9-177">**Resubmit document** – Resubmit an electronic document that has already been submitted to the Electronic invoicing add-on.</span></span> <span data-ttu-id="427e9-178">将在 **提交详细信息** 页创建全新的日志。</span><span class="sxs-lookup"><span data-stu-id="427e9-178">A whole new log is created on the **Submission details** page.</span></span>
- <span data-ttu-id="427e9-179">**发送相关提交**</span><span class="sxs-lookup"><span data-stu-id="427e9-179">**Send related submission**</span></span>
