---
title: 自动化供应商开票流程概述
description: 本主题描述了自动化供应商发票处理的功能以及使用自动化流程的好处。
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2020
ms.locfileid: "3904999"
---
# <a name="automated-vendor-invoicing-processes-overview"></a><span data-ttu-id="e9091-103">自动化供应商开票流程概述</span><span class="sxs-lookup"><span data-stu-id="e9091-103">Automated vendor invoicing processes overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e9091-104">本主题描述了自动化供应商发票处理的功能以及使用自动化流程的好处。</span><span class="sxs-lookup"><span data-stu-id="e9091-104">This topic describes the capability for automating your vendor invoice processing and the benefits of using an automated process.</span></span> <span data-ttu-id="e9091-105">此功能包含在功能管理中启用的功能。</span><span class="sxs-lookup"><span data-stu-id="e9091-105">This capability consists of features that are turned on in Feature management.</span></span> <span data-ttu-id="e9091-106">这些功能仅适用于供应商发票，不适用于通过**发票日记帐**或**发票登记薄日记帐**页面处理的发票。</span><span class="sxs-lookup"><span data-stu-id="e9091-106">These features apply only to vendor invoices, not to invoices that are processed through the **Invoice journal** or **Invoice register journal** page.</span></span>

<span data-ttu-id="e9091-107">组织通常与第三方合作，使用光学字符识别 (OCR) 服务提供商处理纸质发票。</span><span class="sxs-lookup"><span data-stu-id="e9091-107">Organizations often work with third parties to process paper invoices by using an optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="e9091-108">服务提供商返回机器可读的发票元数据。</span><span class="sxs-lookup"><span data-stu-id="e9091-108">The service provider returns machine-readable invoice metadata.</span></span> <span data-ttu-id="e9091-109">为了帮助实现自动化，应付帐款自动化功能使您可以从应付帐款中使用这些项目。</span><span class="sxs-lookup"><span data-stu-id="e9091-109">To help with automation, the Accounts payable automation features let you consume these artifacts from Accounts payable.</span></span>

<span data-ttu-id="e9091-110">您可以自动化某些应付帐款供应商开票流程。</span><span class="sxs-lookup"><span data-stu-id="e9091-110">You can automate some Accounts payable vendor invoicing processes.</span></span> <span data-ttu-id="e9091-111">这些流程包括将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待定供应商发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="e9091-111">These processes include submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines.</span></span> <span data-ttu-id="e9091-112">自动化流程会显示有关供应商发票在每个流程中的进度信息。</span><span class="sxs-lookup"><span data-stu-id="e9091-112">The automated process shows information about the progress of a vendor invoice as it moves through each of the processes.</span></span> <span data-ttu-id="e9091-113">此功能可以帮助应付帐款职员和经理更有效地处理供应商发票。</span><span class="sxs-lookup"><span data-stu-id="e9091-113">This capability can help Accounts payable clerks and managers process vendor invoices more efficiently.</span></span> <span data-ttu-id="e9091-114">它还有助于减少手动输入和处理信息时可能发生的错误，并提高效率。</span><span class="sxs-lookup"><span data-stu-id="e9091-114">It also helps reduce the errors and inefficiencies that can occur when information is manually entered and processed.</span></span>

<span data-ttu-id="e9091-115">自动化流程可用于执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="e9091-115">The automation processes can be used to perform these tasks:</span></span>

- <span data-ttu-id="e9091-116">自动将导入的发票提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="e9091-116">Automatically submit imported invoices to the workflow system.</span></span>
- <span data-ttu-id="e9091-117">将物料收货与待定供应商发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="e9091-117">Match product receipts to pending vendor invoice lines.</span></span>
- <span data-ttu-id="e9091-118">在过帐供应商发票之前模拟过帐。</span><span class="sxs-lookup"><span data-stu-id="e9091-118">Simulate posting before a vendor invoice is posted.</span></span>
- <span data-ttu-id="e9091-119">快速有效地查看工作流历史记录。</span><span class="sxs-lookup"><span data-stu-id="e9091-119">Quickly and efficiently view workflow history.</span></span>
- <span data-ttu-id="e9091-120">查看和分析自动化供应商发票处理的结果。</span><span class="sxs-lookup"><span data-stu-id="e9091-120">View and analyze the results of automating vendor invoice processing.</span></span>

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a><span data-ttu-id="e9091-121">供应商发票自动化 – 将导入的供应商发票提交到工作流系统</span><span class="sxs-lookup"><span data-stu-id="e9091-121">Vendor invoice automation – Submit imported vendor invoices to the workflow system</span></span>

<span data-ttu-id="e9091-122">作为非接触式应付帐款开票流程的一部分，您可以让系统自动将导入的发票提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="e9091-122">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="e9091-123">该流程将以您指定的频率（每小时或每天）在后台运行。</span><span class="sxs-lookup"><span data-stu-id="e9091-123">The process will run in the background, at a frequency that you specify (either hourly or daily).</span></span> <span data-ttu-id="e9091-124">自动将导入的发票提交到工作流系统的功能要求您的流程以导入的发票开始。</span><span class="sxs-lookup"><span data-stu-id="e9091-124">The capability to automatically submit imported invoices to the workflow system requires that your process begin with an imported invoice.</span></span> <span data-ttu-id="e9091-125">为了确保整个发票处理流程都没有人工干预，工作流配置中必须包括自动化过帐任务。</span><span class="sxs-lookup"><span data-stu-id="e9091-125">To ensure that the invoice can be processed from start to finish without manual intervention, an automated posting task must be included in the workflow configuration.</span></span>

<span data-ttu-id="e9091-126">可以将与采购订单 (PO) 相关的发票以及包含非 PO 采购类别和非贮存行的发票自动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="e9091-126">'Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="e9091-127">手动输入的发票和通过**供应商协作开票**工作区创建的发票必须手动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="e9091-127">Invoices that are manually entered and invoices that are created via the **Vendor collaboration invoicing** workspace must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="e9091-128">自动化功能提供了一个灵活的框架，可让您定义公司特定的规则，以将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待定供应商发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="e9091-128">The automation feature provides a flexible framework that lets you define company-specific rules for submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines.</span></span>

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="e9091-129">供应商发票自动化 – 将物料收货与具有三向匹配政策的发票行进行匹配</span><span class="sxs-lookup"><span data-stu-id="e9091-129">Vendor invoice automation – Match product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="e9091-130">系统可以自动将过帐的物料收货与定义了三向匹配政策的发票行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="e9091-130">The system can automatically match posted product receipts to invoice lines that a three-way matching policy is defined for.</span></span> <span data-ttu-id="e9091-131">该流程将一直运行，直到匹配的物料收货数量等于发票数量。</span><span class="sxs-lookup"><span data-stu-id="e9091-131">The process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="e9091-132">作为此流程的一部分，您可以指定系统在得出流程失败的结论之前应尝试将物料收货与发票行进行匹配的最大次数。</span><span class="sxs-lookup"><span data-stu-id="e9091-132">As part of this process, you can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="e9091-133">该流程将以每小时或每天的频率在后台运行。</span><span class="sxs-lookup"><span data-stu-id="e9091-133">The process will run in the background, either hourly or daily.</span></span> <span data-ttu-id="e9091-134">您可以在将发票提交到工作流系统的流程中运行自动化匹配流程。</span><span class="sxs-lookup"><span data-stu-id="e9091-134">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="e9091-135">或者，您可以将其作为独立流程运行。</span><span class="sxs-lookup"><span data-stu-id="e9091-135">Alternatively, you can run it as a standalone process.</span></span>

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a><span data-ttu-id="e9091-136">供应商发票自动化 – 预验证供应商发票过帐</span><span class="sxs-lookup"><span data-stu-id="e9091-136">Vendor invoice automation – Pre-validate vendor invoice posting</span></span>

<span data-ttu-id="e9091-137">过帐模拟完成了供应商发票过帐流程中完成的验证步骤，但是没有更新任何帐户。</span><span class="sxs-lookup"><span data-stu-id="e9091-137">Posting simulation completes the validation steps that are done during the posting process for vendor invoices, but no accounts are updated.</span></span> <span data-ttu-id="e9091-138">若要运行该流程，您可以在**待定供应商发票**页面上选择一个或多个发票。</span><span class="sxs-lookup"><span data-stu-id="e9091-138">To run the process, you can select either a single invoice or multiple invoices on the **Pending vendor invoices** page.</span></span>

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a><span data-ttu-id="e9091-139">供应商发票自动化 – 用于查看供应商发票的工作流历史信息的增强体验</span><span class="sxs-lookup"><span data-stu-id="e9091-139">Vendor invoice automation – Enhanced experience for viewing workflow historical information for vendor invoices</span></span>

<span data-ttu-id="e9091-140">提供了易于阅读的供应商发票工作流历史记录视图。</span><span class="sxs-lookup"><span data-stu-id="e9091-140">An easy-to-read view of vendor invoice workflow history is provided.</span></span> <span data-ttu-id="e9091-141">可以直接从供应商发票访问供应商发票工作流历史记录。</span><span class="sxs-lookup"><span data-stu-id="e9091-141">Vendor invoice workflow history can be accessed directly from the vendor invoice.</span></span> <span data-ttu-id="e9091-142">因此，只需较少的点击即可找到该信息。</span><span class="sxs-lookup"><span data-stu-id="e9091-142">Therefore, fewer clicks are required to find that information.</span></span>

## <a name="vendor-invoice-automation--analytics-and-metrics"></a><span data-ttu-id="e9091-143">供应商发票自动化 – 分析和指标</span><span class="sxs-lookup"><span data-stu-id="e9091-143">Vendor invoice automation – Analytics and metrics</span></span>

<span data-ttu-id="e9091-144">通过**供应商发票条目**工作区，您可以专注于未通过自动化流程完成的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="e9091-144">The **Vendor invoice entry** workspace lets you focus on vendor invoices that didn't make it through the automated process.</span></span> <span data-ttu-id="e9091-145">工作区上的磁贴列出了有关未成功提交到工作流系统，未导入或未与产品收据进行匹配的供应商发票的信息。</span><span class="sxs-lookup"><span data-stu-id="e9091-145">Tiles on the workspace list information about vendor invoices that weren't successfully submitted to the workflow system, imported, or matched to product receipts.</span></span> <span data-ttu-id="e9091-146">还提供了 Microsoft Power BI 指标，以使应付帐款经理可以洞悉供应商发票自动化的效率。</span><span class="sxs-lookup"><span data-stu-id="e9091-146">Microsoft Power BI metrics are also provided to give Accounts payable managers insight into the efficiencies of vendor invoice automation.</span></span>
