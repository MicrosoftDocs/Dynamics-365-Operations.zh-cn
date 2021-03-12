---
title: 供应商协作开票工作区
description: 本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30e9012845838a4d1df5f1308740b356a64433e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993155"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="13bc8-103">供应商协作开票工作区</span><span class="sxs-lookup"><span data-stu-id="13bc8-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13bc8-104">本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="13bc8-105">**供应商协作开票** 工作区可用于查看供应商发票信息和使用工作流功能提交发票至此系统。</span><span class="sxs-lookup"><span data-stu-id="13bc8-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="13bc8-106">供应商协作开票工作区</span><span class="sxs-lookup"><span data-stu-id="13bc8-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="13bc8-107">汇总磁贴</span><span class="sxs-lookup"><span data-stu-id="13bc8-107">Summary tiles</span></span>

<span data-ttu-id="13bc8-108">**汇总** 磁贴提供了所选供应商的发票概览。</span><span class="sxs-lookup"><span data-stu-id="13bc8-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="13bc8-109">您可以按其状态查看发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="13bc8-110">草稿发票尚未提交到工作流。</span><span class="sxs-lookup"><span data-stu-id="13bc8-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="13bc8-111">已提交但未审核的发票为供应商已经提交，但未在应用程序中过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="13bc8-112">已审核但未付款的发票为已经过帐但尚未付清的发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="13bc8-113">已付款发票为已经在应用程序中全额付清的发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="13bc8-114">单击磁贴将打开 **发票列表** 页面的筛选视图。</span><span class="sxs-lookup"><span data-stu-id="13bc8-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="13bc8-115">表格式列表</span><span class="sxs-lookup"><span data-stu-id="13bc8-115">Tabular lists</span></span>

<span data-ttu-id="13bc8-116">在 **表格式列表** 部分，发票的状态按照与汇总磁贴类似的方式分解：草稿和已提交，未审核的列表。</span><span class="sxs-lookup"><span data-stu-id="13bc8-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="13bc8-117">在“草稿”状态，发票可以提交到工作流或删除。</span><span class="sxs-lookup"><span data-stu-id="13bc8-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="13bc8-118">最后一个表格式列表是用来查找发票的选项。</span><span class="sxs-lookup"><span data-stu-id="13bc8-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="13bc8-119">您可以在搜索时进行筛选，以便更快地进行搜索。</span><span class="sxs-lookup"><span data-stu-id="13bc8-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="13bc8-120">所有供应商发票列表页</span><span class="sxs-lookup"><span data-stu-id="13bc8-120">All vendor invoices list page</span></span>

<span data-ttu-id="13bc8-121">您可以在 **供应商协作发票** 列表页上查看所有已过帐和未过帐的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="13bc8-122">您可以使用此列表页查看发票的付款状态。</span><span class="sxs-lookup"><span data-stu-id="13bc8-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="13bc8-123">付款状态包括未过帐，未付款，部分支付和完全支付。</span><span class="sxs-lookup"><span data-stu-id="13bc8-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="13bc8-124">从采购订单创建新发票</span><span class="sxs-lookup"><span data-stu-id="13bc8-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="13bc8-125">您可以通过选择 **供应商协作开票** 工作区上的 **新建** 操作创建新的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="13bc8-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="13bc8-126">采购订单编号以及发票编号必须由供应商提供。</span><span class="sxs-lookup"><span data-stu-id="13bc8-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="13bc8-127">默认情况下，新发票上将显示供应商采购订单的所有行。</span><span class="sxs-lookup"><span data-stu-id="13bc8-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="13bc8-128">将供应商发票提交到工作流之前，可以编辑数量和成本信息。</span><span class="sxs-lookup"><span data-stu-id="13bc8-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="13bc8-129">提交发票前，您可以在发票上附加文件、附注、图片和 URL。</span><span class="sxs-lookup"><span data-stu-id="13bc8-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="13bc8-130">有关详细信息，请参阅[供应商与外部供应商的协作](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="13bc8-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



