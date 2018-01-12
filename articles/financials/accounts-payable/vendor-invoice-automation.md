---
title: "供应商发票自动化"
description: "此主题说明对供应商发票（甚至是包括附件的发票）端到端自动化提供的功能。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04809337167741c30677844adad8addeaba303bc
ms.openlocfilehash: e55c4f6fb2168ec1a308c49545f372872610aff0
ms.contentlocale: zh-cn
ms.lasthandoff: 01/12/2018

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="d7c58-103">供应商发票自动化</span><span class="sxs-lookup"><span data-stu-id="d7c58-103">Vendor invoice automation</span></span>

<span data-ttu-id="d7c58-104">此主题说明对供应商发票（甚至是包括附件的发票）端到端自动化提供的功能。</span><span class="sxs-lookup"><span data-stu-id="d7c58-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="d7c58-105">想要优化其应付账款 (AP) 流程的组织通常将发票处理确定为应提高效率的优先流程领域。</span><span class="sxs-lookup"><span data-stu-id="d7c58-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="d7c58-106">在大多数情况下，这些组织将纸质发票的处理委托给第三方光学字符识别 (OCR) 服务提供商。</span><span class="sxs-lookup"><span data-stu-id="d7c58-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="d7c58-107">然后，他们收到机器可读的发票元数据和每张发票的扫描图像。</span><span class="sxs-lookup"><span data-stu-id="d7c58-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="d7c58-108">为了帮助实现自动化，生成了“最后一英里”解决方案以实现这些项目在发票系统中的使用。</span><span class="sxs-lookup"><span data-stu-id="d7c58-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="d7c58-109">Microsoft Dynamics 365 for Finance and Operations Enterprise 版本现在通过发票自动化解决方案实现此现成的“最后一英里”自动化。</span><span class="sxs-lookup"><span data-stu-id="d7c58-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="d7c58-110">解决方案环境</span><span class="sxs-lookup"><span data-stu-id="d7c58-110">Solution context</span></span>

<span data-ttu-id="d7c58-111">发票自动化解决方案支持标准界面，可以接受发票抬头和发票行的发票元数据，以及适用于发票的附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="d7c58-112">可能生成符合此界面的项目的任何外部系统将能够发送馈送到 Finance and Operations 进行发票和附件的自动化处理。</span><span class="sxs-lookup"><span data-stu-id="d7c58-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="d7c58-113">下图显示 Contoso 与 OCR 服务提供商合作进行供应商发票处理的集成示例场景。</span><span class="sxs-lookup"><span data-stu-id="d7c58-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="d7c58-114">Contoso 的供应商通过电子邮件将发票发送给服务提供商。</span><span class="sxs-lookup"><span data-stu-id="d7c58-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="d7c58-115">通过 OCR 处理，该服务提供商生成发票元数据（抬头和/或行）和发票的扫描图像。</span><span class="sxs-lookup"><span data-stu-id="d7c58-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="d7c58-116">然后，集成层将这些项目进行转换，使 Finance and Operations 可以使用它们。</span><span class="sxs-lookup"><span data-stu-id="d7c58-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![集成示例场景](media/vendor_invoice_automation_01.png)

<span data-ttu-id="d7c58-118">如果要求发票集成，上述场景可以存在多种变体。</span><span class="sxs-lookup"><span data-stu-id="d7c58-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="d7c58-119">数据迁移是使用此界面在 Finance and Operations 中创建发票和附件的另一个使用案例。</span><span class="sxs-lookup"><span data-stu-id="d7c58-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="d7c58-120">解决方案构成</span><span class="sxs-lookup"><span data-stu-id="d7c58-120">Solution components</span></span>

<span data-ttu-id="d7c58-121">解决方案足迹包括以下构成：</span><span class="sxs-lookup"><span data-stu-id="d7c58-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="d7c58-122">发票抬头、发票行和发票附件的数据实体</span><span class="sxs-lookup"><span data-stu-id="d7c58-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="d7c58-123">异常发票处理</span><span class="sxs-lookup"><span data-stu-id="d7c58-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="d7c58-124">发票中的并行附件查看器</span><span class="sxs-lookup"><span data-stu-id="d7c58-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="d7c58-125">此主题的其余内容提供关于这些解决方案构成的详细说明。</span><span class="sxs-lookup"><span data-stu-id="d7c58-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="d7c58-126">数据实体</span><span class="sxs-lookup"><span data-stu-id="d7c58-126">Data entities</span></span>

<span data-ttu-id="d7c58-127">数据包是指必须发送到 Finance and Operations 以便创建发票抬头、发票行和发票附件的工作单元。</span><span class="sxs-lookup"><span data-stu-id="d7c58-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="d7c58-128">以下数据实体用于构成数据包的项目：</span><span class="sxs-lookup"><span data-stu-id="d7c58-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="d7c58-129">供应商发票标题</span><span class="sxs-lookup"><span data-stu-id="d7c58-129">Vendor invoice header</span></span>
+ <span data-ttu-id="d7c58-130">供应商发票行</span><span class="sxs-lookup"><span data-stu-id="d7c58-130">Vendor invoice line</span></span>
+ <span data-ttu-id="d7c58-131">供应商发票文档附件</span><span class="sxs-lookup"><span data-stu-id="d7c58-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="d7c58-132">供应商发票文档附件是作为此功能的一部分而引进的新数据实体。</span><span class="sxs-lookup"><span data-stu-id="d7c58-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="d7c58-133">供应商发票抬头实体已经过修改以支持附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="d7c58-134">供应商发票行实体未针对此功能进行修改。</span><span class="sxs-lookup"><span data-stu-id="d7c58-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="d7c58-135">此主题不提供数据包的详细定义。</span><span class="sxs-lookup"><span data-stu-id="d7c58-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="d7c58-136">也不解释如何创建数据包。</span><span class="sxs-lookup"><span data-stu-id="d7c58-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="d7c58-137">有关此信息，请参阅 [数据实体和包框架](../../dev-itpro/data-entities/data-entities-data-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="d7c58-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="d7c58-138">要快速生成包括发票和附件的测试数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d7c58-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="d7c58-139">登录到 Finance and Operations 实例。</span><span class="sxs-lookup"><span data-stu-id="d7c58-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="d7c58-140">转到**应付账款** > **发票** > **待定供应商发票**。</span><span class="sxs-lookup"><span data-stu-id="d7c58-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="d7c58-141">创建具有行和附件的发票。</span><span class="sxs-lookup"><span data-stu-id="d7c58-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d7c58-142">附件必须是抬头附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-142">The attachments must be header attachments.</span></span> <span data-ttu-id="d7c58-143">目前，供应商发票文档附件实体不支持行附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="d7c58-144">打开**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="d7c58-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="d7c58-145">创建包括供应商发票抬头、供应商发票行和供应商发票文档附件实体的导出作业。</span><span class="sxs-lookup"><span data-stu-id="d7c58-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="d7c58-146">导出数据。</span><span class="sxs-lookup"><span data-stu-id="d7c58-146">Export the data.</span></span>
1. <span data-ttu-id="d7c58-147">将导出的数据下载为包。</span><span class="sxs-lookup"><span data-stu-id="d7c58-147">Download the exported data as a package.</span></span> <span data-ttu-id="d7c58-148">您现在可以使用包将数据导入到目标实例以用于测试目的。</span><span class="sxs-lookup"><span data-stu-id="d7c58-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="d7c58-149">确定发票的法人</span><span class="sxs-lookup"><span data-stu-id="d7c58-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="d7c58-150">通过数据包导入的发票可以通过两种方式与他们所属的法人关联：</span><span class="sxs-lookup"><span data-stu-id="d7c58-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="d7c58-151">处理发票的导入作业将其导入到在**数据管理**工作区中计划作业的相同公司。</span><span class="sxs-lookup"><span data-stu-id="d7c58-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="d7c58-152">换言之，作业的公司确定发票所属的公司。</span><span class="sxs-lookup"><span data-stu-id="d7c58-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="d7c58-153">将包含发票的数据包发送到 Finance and Operations 后，调用方（即在 Finance and Operations 以外运行的集成应用）可以在 HTTP 请求中明确记载公司 ID。</span><span class="sxs-lookup"><span data-stu-id="d7c58-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="d7c58-154">在这种情况下，在 Finance and Operations 中运行的处理作业的公司环境被覆盖，发票被导入到通过 HTTP 请求传递的公司。</span><span class="sxs-lookup"><span data-stu-id="d7c58-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="d7c58-155">此行为是标准数据管理行为。</span><span class="sxs-lookup"><span data-stu-id="d7c58-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="d7c58-156">此处仅出于完整性的目的在发票上下文中对其进行了解释。</span><span class="sxs-lookup"><span data-stu-id="d7c58-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="d7c58-157">异常处理</span><span class="sxs-lookup"><span data-stu-id="d7c58-157">Exception processing</span></span>

<span data-ttu-id="d7c58-158">在供应商发票通过集成进入到 Finance and Operations 的场景中，应付账款团队成员必须可以通过简单的方法处理异常或失败的发票和使用失败的发票创建待定发票。</span><span class="sxs-lookup"><span data-stu-id="d7c58-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="d7c58-159">此供应商发票异常处理现在是 Finance and Operations 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d7c58-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="d7c58-160">异常列表页</span><span class="sxs-lookup"><span data-stu-id="d7c58-160">Exceptions list page</span></span>

<span data-ttu-id="d7c58-161">新的发票异常列表页在**应付账款** > **发票** > **导入功能** > **导入失败的供应商发票**中可用。</span><span class="sxs-lookup"><span data-stu-id="d7c58-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="d7c58-162">此页显示来自供应商发票抬头数据实体暂存表的所有供应商发票抬头记录。</span><span class="sxs-lookup"><span data-stu-id="d7c58-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="d7c58-163">请注意，您可以查看来自**数据管理**工作区的相同记录，您也可以在这里执行在异常处理功能中提供的相同操作。</span><span class="sxs-lookup"><span data-stu-id="d7c58-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="d7c58-164">但是，异常处理功能提供的 UI 针对功能用户进行了优化。</span><span class="sxs-lookup"><span data-stu-id="d7c58-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![异常列表页](media/vendor_invoice_automation_02.png)

<span data-ttu-id="d7c58-166">此列表页包括通过馈送进入的以下字段：</span><span class="sxs-lookup"><span data-stu-id="d7c58-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="d7c58-167">**公司** – 发票所属的公司</span><span class="sxs-lookup"><span data-stu-id="d7c58-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="d7c58-168">**错误消息** –数据管理框架签发的错误消息，用来解释无法创建发票的原因</span><span class="sxs-lookup"><span data-stu-id="d7c58-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="d7c58-169">**编号** - 发票编号</span><span class="sxs-lookup"><span data-stu-id="d7c58-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="d7c58-170">**发票帐户**</span><span class="sxs-lookup"><span data-stu-id="d7c58-170">**Invoice account**</span></span>
+ <span data-ttu-id="d7c58-171">**名称** - 供应商的名称</span><span class="sxs-lookup"><span data-stu-id="d7c58-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="d7c58-172">**供应商帐户**</span><span class="sxs-lookup"><span data-stu-id="d7c58-172">**Vendor account**</span></span>
+ <span data-ttu-id="d7c58-173">**采购订单** - 发票的采购订单 (PO) 编号</span><span class="sxs-lookup"><span data-stu-id="d7c58-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="d7c58-174">**过帐日期**</span><span class="sxs-lookup"><span data-stu-id="d7c58-174">**Posting date**</span></span>
+ <span data-ttu-id="d7c58-175">**发票日期**</span><span class="sxs-lookup"><span data-stu-id="d7c58-175">**Invoice date**</span></span>
+ <span data-ttu-id="d7c58-176">**发票描述**</span><span class="sxs-lookup"><span data-stu-id="d7c58-176">**Invoice description**</span></span>
+ <span data-ttu-id="d7c58-177">**币种**</span><span class="sxs-lookup"><span data-stu-id="d7c58-177">**Currency**</span></span>
+ <span data-ttu-id="d7c58-178">**日志**</span><span class="sxs-lookup"><span data-stu-id="d7c58-178">**Log**</span></span>
+ <span data-ttu-id="d7c58-179">**行参考** –来自外部系统的标识符</span><span class="sxs-lookup"><span data-stu-id="d7c58-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="d7c58-180">行参考不是发票 ID。</span><span class="sxs-lookup"><span data-stu-id="d7c58-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="d7c58-181">此列表页还具有预览窗格，您可以通过以下方式使用：</span><span class="sxs-lookup"><span data-stu-id="d7c58-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="d7c58-182">查看完整的错误消息，因而无需在网格中扩展**错误消息**列。</span><span class="sxs-lookup"><span data-stu-id="d7c58-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="d7c58-183">如果发票伴随任何附件，则可查看发票附件的完整列表。</span><span class="sxs-lookup"><span data-stu-id="d7c58-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="d7c58-184">列表页支持以下操作：</span><span class="sxs-lookup"><span data-stu-id="d7c58-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="d7c58-185">**编辑** –在编辑模式中打开异常记录，以便修复问题。</span><span class="sxs-lookup"><span data-stu-id="d7c58-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="d7c58-186">**选项** –访问在列表页提供的标准选项。</span><span class="sxs-lookup"><span data-stu-id="d7c58-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="d7c58-187">您可以使用**添加到工作区**选项将异常列表页作为列表或图块固定到您的工作区。</span><span class="sxs-lookup"><span data-stu-id="d7c58-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="d7c58-188">异常详细信息页</span><span class="sxs-lookup"><span data-stu-id="d7c58-188">Exception details page</span></span>

<span data-ttu-id="d7c58-189">开始编辑模式后，显示存在问题的发票的异常详细信息页。</span><span class="sxs-lookup"><span data-stu-id="d7c58-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="d7c58-190">如果有任何附件，发票和默认附件在异常详细信息页上并排显示。</span><span class="sxs-lookup"><span data-stu-id="d7c58-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![异常详细信息页](media/vendor_invoice_automation_03.png)

<span data-ttu-id="d7c58-192">在上图中，进入的供应商发票抬头不具有任何行。</span><span class="sxs-lookup"><span data-stu-id="d7c58-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="d7c58-193">因此，行部分为空。</span><span class="sxs-lookup"><span data-stu-id="d7c58-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="d7c58-194">异常详细信息页支持以下操作：</span><span class="sxs-lookup"><span data-stu-id="d7c58-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="d7c58-195">**创建待定发票** - 在异常处理过程中修复发票上的问题后，您可以单击此按钮创建待定发票。</span><span class="sxs-lookup"><span data-stu-id="d7c58-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="d7c58-196">创建待定发票在后台进行（作为异步操作）。</span><span class="sxs-lookup"><span data-stu-id="d7c58-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="d7c58-197">共享服务与基于组织的异常处理</span><span class="sxs-lookup"><span data-stu-id="d7c58-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="d7c58-198">异常列表页支持**数据管理**工作区支持处理暂存记录的标准安全结构。</span><span class="sxs-lookup"><span data-stu-id="d7c58-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="d7c58-199">发票导入作业可以通过以下方式受到保护：</span><span class="sxs-lookup"><span data-stu-id="d7c58-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="d7c58-200">按用户角色</span><span class="sxs-lookup"><span data-stu-id="d7c58-200">By user role</span></span>
+ <span data-ttu-id="d7c58-201">按用户</span><span class="sxs-lookup"><span data-stu-id="d7c58-201">By user</span></span>
+ <span data-ttu-id="d7c58-202">按法人</span><span class="sxs-lookup"><span data-stu-id="d7c58-202">By legal entity</span></span>

![按用户角色和法人受到保护的导入作业](media/vendor_invoice_automation_04.png)

<span data-ttu-id="d7c58-204">如果对发票导入作业配置安全性，异常列表页将遵守这些设置。</span><span class="sxs-lookup"><span data-stu-id="d7c58-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="d7c58-205">用户将仅能够看到此设置允许他们看到的发票异常记录。</span><span class="sxs-lookup"><span data-stu-id="d7c58-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="d7c58-206">例如，Contoso 已决定按法人处理发票异常。</span><span class="sxs-lookup"><span data-stu-id="d7c58-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="d7c58-207">因此，发票导入作业上的安全性配置方式使法人中的用户 A 仅可看到法人 A 中的发票异常，而法人 B 中的用户仅可看到法人 B 中的发票异常。此设置支持对发票异常管理的职责划分。</span><span class="sxs-lookup"><span data-stu-id="d7c58-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="d7c58-208">Contoso 还可以决定不强制执行任何安全性，因此相同用户可以处理所有法人的发票异常。</span><span class="sxs-lookup"><span data-stu-id="d7c58-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="d7c58-209">此设置至此和发票异常管理的共享服务场景。</span><span class="sxs-lookup"><span data-stu-id="d7c58-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="d7c58-210">并行附件查看器</span><span class="sxs-lookup"><span data-stu-id="d7c58-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="d7c58-211">为了帮助您轻松查看供应商发票的附件，在开票流程中使用的以下页提供一个附件查看器：</span><span class="sxs-lookup"><span data-stu-id="d7c58-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="d7c58-212">**异常处理**</span><span class="sxs-lookup"><span data-stu-id="d7c58-212">**Exception handling**</span></span>
+ <span data-ttu-id="d7c58-213">**待定供应商发票**页（在发票审核流程中也可用）</span><span class="sxs-lookup"><span data-stu-id="d7c58-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="d7c58-214">**发票日记帐**查询页（用于过帐的发票）</span><span class="sxs-lookup"><span data-stu-id="d7c58-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="d7c58-215">这是附件查看器提供的主要功能：</span><span class="sxs-lookup"><span data-stu-id="d7c58-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="d7c58-216">查看文档管理支持的所有附件类型（文件、图像、URL 和注释）</span><span class="sxs-lookup"><span data-stu-id="d7c58-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="d7c58-217">显示多页 TIFF 文件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="d7c58-218">对图像文件执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d7c58-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="d7c58-219">突出显示图像的某些部分。</span><span class="sxs-lookup"><span data-stu-id="d7c58-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="d7c58-220">阻止图像的某些部分。</span><span class="sxs-lookup"><span data-stu-id="d7c58-220">Block parts of the image.</span></span>
  + <span data-ttu-id="d7c58-221">添加图像注释。</span><span class="sxs-lookup"><span data-stu-id="d7c58-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="d7c58-222">缩放图像。</span><span class="sxs-lookup"><span data-stu-id="d7c58-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="d7c58-223">平移图像。</span><span class="sxs-lookup"><span data-stu-id="d7c58-223">Pan the image.</span></span>
  + <span data-ttu-id="d7c58-224">撤销和重新执行操作。</span><span class="sxs-lookup"><span data-stu-id="d7c58-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="d7c58-225">适应图像大小。</span><span class="sxs-lookup"><span data-stu-id="d7c58-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="d7c58-226">这些操作仅对图像文件（JPEG、TIFF、PNG 等）可用。</span><span class="sxs-lookup"><span data-stu-id="d7c58-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="d7c58-227">您通过这些操作对图像进行的任何更改均保存到图像文件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="d7c58-228">目前，附件查看器不包括版本控制和审核功能。</span><span class="sxs-lookup"><span data-stu-id="d7c58-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="d7c58-229">默认附件</span><span class="sxs-lookup"><span data-stu-id="d7c58-229">Default attachment</span></span>

<span data-ttu-id="d7c58-230">如果供应商发票具有多个附件，您可以在**附件**页将其中一个文档设置为默认附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="d7c58-231">**为默认附件**选项是作为此功能的一部分添加的一个新选项。</span><span class="sxs-lookup"><span data-stu-id="d7c58-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="d7c58-232">此选项也在供应商发票单据附件数据实体中公开。</span><span class="sxs-lookup"><span data-stu-id="d7c58-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="d7c58-233">因此，可以通过集成设置默认附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="d7c58-234">仅一个单据可以设置为默认附件。</span><span class="sxs-lookup"><span data-stu-id="d7c58-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="d7c58-235">将单据设置为默认附件后，在打开发票时会自动显示在附件查看器中。</span><span class="sxs-lookup"><span data-stu-id="d7c58-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="d7c58-236">如果您没有将任何单据设置为默认附件，则在打开发票时，查看器不会自动显示任何单据。</span><span class="sxs-lookup"><span data-stu-id="d7c58-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="d7c58-237">显示/隐藏发票附件</span><span class="sxs-lookup"><span data-stu-id="d7c58-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="d7c58-238">在**异常处理**、**待定发票**和**发票日记帐**查询页面提供的新按钮让您能够显示或隐藏附件查看器。</span><span class="sxs-lookup"><span data-stu-id="d7c58-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="d7c58-239">安全性</span><span class="sxs-lookup"><span data-stu-id="d7c58-239">Security</span></span>

<span data-ttu-id="d7c58-240">附件查看器中的以下操作通过基于角色的安全性进行控制：</span><span class="sxs-lookup"><span data-stu-id="d7c58-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="d7c58-241">突出显示</span><span class="sxs-lookup"><span data-stu-id="d7c58-241">Highlighting</span></span>
+ <span data-ttu-id="d7c58-242">锁定</span><span class="sxs-lookup"><span data-stu-id="d7c58-242">Block</span></span>
+ <span data-ttu-id="d7c58-243">批注</span><span class="sxs-lookup"><span data-stu-id="d7c58-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="d7c58-244">待定供应商发票页</span><span class="sxs-lookup"><span data-stu-id="d7c58-244">Pending vendor invoices page</span></span>

<span data-ttu-id="d7c58-245">以下权限提供对附件查看器执行突出显示、锁定和批注操作的只读访问权限或读/写访问权限：</span><span class="sxs-lookup"><span data-stu-id="d7c58-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="d7c58-246">**维护供应商发票图像** –此权限提供读/写访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="d7c58-247">**查看供应商发票图像** –此权限提供只读访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="d7c58-248">以下职责提供对附件查看器执行以下操作的只读访问权限或读/写访问权限：</span><span class="sxs-lookup"><span data-stu-id="d7c58-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="d7c58-249">**维护供应商发票** - 维护供应商发票图像权限被分配到此职责。</span><span class="sxs-lookup"><span data-stu-id="d7c58-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="d7c58-250">**查询供应商发票状态** - 查看供应商发票图像权限被分配到此职责。</span><span class="sxs-lookup"><span data-stu-id="d7c58-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="d7c58-251">以下角色提供对附件查看器执行以下操作的只读访问权限或读/写访问权限：</span><span class="sxs-lookup"><span data-stu-id="d7c58-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="d7c58-252">**应付账款职员**和**应付账款经理** – 维护供应商发票职责被分配到这些角色。</span><span class="sxs-lookup"><span data-stu-id="d7c58-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="d7c58-253">**应付账款职员**、**应付账款经理**、**应付账款的集中付款员**和 **应付账款付款职员** – 查询供应商发票状态职责被分配到这些角色。</span><span class="sxs-lookup"><span data-stu-id="d7c58-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="d7c58-254">发票异常详细信息页</span><span class="sxs-lookup"><span data-stu-id="d7c58-254">Invoice exception details page</span></span>

<span data-ttu-id="d7c58-255">以下权限提供对附件查看器执行突出显示、锁定和批注操作的只读访问权限或读/写访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="d7c58-256">本节提及的这些角色创造性地提供对附件查看器中的发票图像的只读访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="d7c58-257">如果某个角色必须具有对图像的写入访问权限，您可以使用此处描述的权限和职责对该角色授予写入访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="d7c58-258">**维护供应商发票抬头实体图像** – 此权限提供对附件查看器中的发票图像的读/写访问权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="d7c58-259">**查看供应商发票抬头实体图像** – 此权限提供对附件查看器中的发票图像的只读视图。</span><span class="sxs-lookup"><span data-stu-id="d7c58-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="d7c58-260">以下职责提供对附件查看器执行以下操作的只读访问权限：</span><span class="sxs-lookup"><span data-stu-id="d7c58-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="d7c58-261">**维护供应商发票** - 维护供应商发票抬头实体图像权限被分配到此职责。</span><span class="sxs-lookup"><span data-stu-id="d7c58-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="d7c58-262">以下角色提供对附件查看器执行以下操作的只读访问权限：</span><span class="sxs-lookup"><span data-stu-id="d7c58-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="d7c58-263">**应付账款职员**和**应付账款经理** – 维护供应商发票职责被分配到这些角色。</span><span class="sxs-lookup"><span data-stu-id="d7c58-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="d7c58-264">默认情况下，如果用户角色提供对任何页面的编辑权限，则用户还将拥有对附件查看器执行突出显示、锁定和批注操作的编辑权限。</span><span class="sxs-lookup"><span data-stu-id="d7c58-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="d7c58-265">但是，如果有些场景中要求特定角色对页面（而不是附件查看器）具有编辑权限，则上述列表中的相应权限可用来满足该使用案例。</span><span class="sxs-lookup"><span data-stu-id="d7c58-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

