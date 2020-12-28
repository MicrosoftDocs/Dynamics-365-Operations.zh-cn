---
title: 查看供应商发票自动化结果（预览）
description: 本主题说明了如何查看自动提交到工作流程中的供应商发票的状态。
author: abruer
manager: AnnBe
ms.date: 10/16/2020
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec49a621e24b6373532497b499e8b9d45c9bed14
ms.sourcegitcommit: 30c541426cf2037b768e3556e1b170a64991f64a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/17/2020
ms.locfileid: "4440925"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="283c9-103">查看供应商发票自动化结果</span><span class="sxs-lookup"><span data-stu-id="283c9-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="283c9-104">本主题说明了如何查看自动提交到工作流程中的供应商发票的状态。</span><span class="sxs-lookup"><span data-stu-id="283c9-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="283c9-105">将为每个导入的供应商发票维护自动化历史记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="283c9-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="283c9-106">根据您自动化的业务流程，**待定供应商发票** 页面显示 **自动化收货匹配状态** 和 **自动提交到工作流状态** 值。</span><span class="sxs-lookup"><span data-stu-id="283c9-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="283c9-107">您可以查看详细信息并制定计划以侧重于自动化步骤失败的发票。</span><span class="sxs-lookup"><span data-stu-id="283c9-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="283c9-108">然后，在更正问题后，您可以恢复导入的发票的自动化流程。</span><span class="sxs-lookup"><span data-stu-id="283c9-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="283c9-109">在编辑已提交的发票之前，必须暂停自动化流程。</span><span class="sxs-lookup"><span data-stu-id="283c9-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="283c9-110">如果必须暂停自动提交到工作流程中的发票，请在 **供应商发票** 页面上将 **包括在自动化流程中** 设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="283c9-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="283c9-111">然后，直到 **包括在自动化流程中** 设置为 **是**，才能运行自动化。</span><span class="sxs-lookup"><span data-stu-id="283c9-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="283c9-112">如果发票尚未在工作流系统中并且未被自动化流程使用，则可以暂停发票进行进一步自动化。</span><span class="sxs-lookup"><span data-stu-id="283c9-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="283c9-113">如果导入的发票执行提交到工作流程，则可以在 **供应商发票** 页面上查看其 **自动化状态** 值。</span><span class="sxs-lookup"><span data-stu-id="283c9-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="283c9-114">跟踪以下状态：</span><span class="sxs-lookup"><span data-stu-id="283c9-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="283c9-115">**已包括** – 在 **应付帐款参数** 页面上定义的自动化流程运行正常，但尚未完成。</span><span class="sxs-lookup"><span data-stu-id="283c9-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="283c9-116">**已暂停** – 在 **应付帐款参数** 页面上定义的自动化流程已运行，但流程中至少有一个步骤失败。</span><span class="sxs-lookup"><span data-stu-id="283c9-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="283c9-117">如果 **包括在自动化流程中** 字段设置为 **否**，还应用 **已暂停** 状态。</span><span class="sxs-lookup"><span data-stu-id="283c9-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="283c9-118">您可以通过选择 **查看最新结果** 来查看失败。</span><span class="sxs-lookup"><span data-stu-id="283c9-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="283c9-119">**在工作流中** – 导入的发票已通过自动提交到工作流程或手动提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="283c9-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="283c9-120">**工作流完成** – 已完成导入的发票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="283c9-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
