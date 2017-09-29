---
title: "供应商协作开票工作区"
description: "本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f9b8cc1ee7f8c8bed79bac3ca6a6856d9101aad
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="6889c-103">供应商协作开票工作区</span><span class="sxs-lookup"><span data-stu-id="6889c-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6889c-104">本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="6889c-105">“**供应商协作开票**”工作区可用于查看供应商发票信息和使用工作流功能提交发票至 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition。</span><span class="sxs-lookup"><span data-stu-id="6889c-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="6889c-106">供应商协作开票工作区</span><span class="sxs-lookup"><span data-stu-id="6889c-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="6889c-107">汇总磁贴</span><span class="sxs-lookup"><span data-stu-id="6889c-107">Summary tiles</span></span>

<span data-ttu-id="6889c-108">**汇总**磁贴提供了所选供应商的发票概览。</span><span class="sxs-lookup"><span data-stu-id="6889c-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="6889c-109">您可以按其状态查看发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="6889c-110">草稿发票尚未提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="6889c-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="6889c-111">已提交但未审核的发票为供应商已经提交，但未在 Finance and Operations 中过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="6889c-112">已审核但未付款的发票为已经在 Finance and Operations 中过帐但尚未付清的发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="6889c-113">已付款发票为已经在 Finance and Operations 中全额付清的发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="6889c-114">单击磁贴将打开“**发票列表**”页面的筛选视图。</span><span class="sxs-lookup"><span data-stu-id="6889c-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="6889c-115">表格式列表</span><span class="sxs-lookup"><span data-stu-id="6889c-115">Tabular lists</span></span>

<span data-ttu-id="6889c-116">在“**表格式列表**”部分，发票的状态按照与汇总磁贴类似的方式分解：草稿和已提交，未审核的列表。</span><span class="sxs-lookup"><span data-stu-id="6889c-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="6889c-117">在“草稿”状态，发票可以提交到工作流或删除。</span><span class="sxs-lookup"><span data-stu-id="6889c-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="6889c-118">最后一个表格式列表是用来查找发票的选项。</span><span class="sxs-lookup"><span data-stu-id="6889c-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="6889c-119">您可以在搜索时进行筛选，以便更快地进行搜索。</span><span class="sxs-lookup"><span data-stu-id="6889c-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="6889c-120">所有供应商发票列表页</span><span class="sxs-lookup"><span data-stu-id="6889c-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="6889c-121">您可以在**供应商协作发票**列表页上查看所有已过帐和未过帐的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="6889c-122">您可以使用此列表页查看发票的付款状态。</span><span class="sxs-lookup"><span data-stu-id="6889c-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="6889c-123">付款状态包括未过帐，未付款，部分支付和完全支付。</span><span class="sxs-lookup"><span data-stu-id="6889c-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="6889c-124">从采购订单创建新发票</span><span class="sxs-lookup"><span data-stu-id="6889c-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="6889c-125">您可以通过选择“**供应商协作开票**”工作区上的“**新建**”操作创建新的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="6889c-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="6889c-126">采购订单编号以及发票编号必须由供应商提供。</span><span class="sxs-lookup"><span data-stu-id="6889c-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="6889c-127">默认情况下，新发票上将显示供应商采购订单的所有行。</span><span class="sxs-lookup"><span data-stu-id="6889c-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="6889c-128">将供应商发票提交到工作流之前，可以编辑数量和成本信息。</span><span class="sxs-lookup"><span data-stu-id="6889c-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="6889c-129">提交发票前，您可以在发票上附加文件、附注、图片和 URL。</span><span class="sxs-lookup"><span data-stu-id="6889c-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="6889c-130">有关详细信息，请参阅[通过使用供应商门户与供应商协作](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span><span class="sxs-lookup"><span data-stu-id="6889c-130">For more information, see [Collaborating with vendors by using the Vendor portal](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span></span>




