---
title: "设置和处理重复发票"
description: "本文说明如何设置和处理重复发票。 如果您必须定期为客户开具相同金额的发票，可以使用重复发票。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c5fbe1791161b8d06cd1539b1717ba8690a8e05
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="a52b7-104">设置和处理重复发票</span><span class="sxs-lookup"><span data-stu-id="a52b7-104">Set up and process recurring invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a52b7-105">本文说明如何设置和处理重复发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="a52b7-106">如果您必须定期为客户开具相同金额的发票，可以使用重复发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="a52b7-107">创建重复执行普通发票的模板</span><span class="sxs-lookup"><span data-stu-id="a52b7-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="a52b7-108">若要定期就相同服务为客户开票，必须定义可以重新用于创建发票的普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="a52b7-109">此模板包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="a52b7-109">This template contains the following information:</span></span>

-   <span data-ttu-id="a52b7-110">标题信息，如税组、付款期限和付款方法</span><span class="sxs-lookup"><span data-stu-id="a52b7-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="a52b7-111">行信息，例如服务描述、收入帐户、单位价格和发票金额</span><span class="sxs-lookup"><span data-stu-id="a52b7-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="a52b7-112">装运或处理的费用</span><span class="sxs-lookup"><span data-stu-id="a52b7-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="a52b7-113">与财务维度信息一起的会计分配，例如成本中心和业务单位</span><span class="sxs-lookup"><span data-stu-id="a52b7-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="a52b7-114">实际上，您创建整个发票并将其保存为模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="a52b7-115">可以使用**重复发票**页设置模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="a52b7-116">将普通发票模板分配给客户并输入重复详细信息</span><span class="sxs-lookup"><span data-stu-id="a52b7-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="a52b7-117">在模板创建后，必须将该模板分配到您要为其开票的客户。</span><span class="sxs-lookup"><span data-stu-id="a52b7-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="a52b7-118">此外，必须指定发票使用的时间和频率。</span><span class="sxs-lookup"><span data-stu-id="a52b7-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="a52b7-119">您可以将在**客户**页的**发票**选项卡上分配模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="a52b7-120">将该模板添加到列表，并更新以下信息：</span><span class="sxs-lookup"><span data-stu-id="a52b7-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="a52b7-121">重复计费的开始日期和结束日期（可选）</span><span class="sxs-lookup"><span data-stu-id="a52b7-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="a52b7-122">重复计费的频率（例如，每天或每月一次）</span><span class="sxs-lookup"><span data-stu-id="a52b7-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="a52b7-123">最大计费金额（如果需要此信息）</span><span class="sxs-lookup"><span data-stu-id="a52b7-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="a52b7-124">客户有具有不同频率的多个模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="a52b7-125">生成重复发票</span><span class="sxs-lookup"><span data-stu-id="a52b7-125">Generate the recurring invoices</span></span>
<span data-ttu-id="a52b7-126">在**重复发票**页，存在处理重复发票模板的任务。</span><span class="sxs-lookup"><span data-stu-id="a52b7-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="a52b7-127">您指定发票日期和以及从中生成发票的模板。</span><span class="sxs-lookup"><span data-stu-id="a52b7-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="a52b7-128">发票将生成并且为处理的每个发票组分配单一重复执行 ID 号。</span><span class="sxs-lookup"><span data-stu-id="a52b7-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>
<span data-ttu-id="a52b7-129">过帐重复执行普通发票</span><span class="sxs-lookup"><span data-stu-id="a52b7-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="a52b7-130">在重复发票生成后，发票重复执行 ID 出现在**重复发票**页的过帐任务中。</span><span class="sxs-lookup"><span data-stu-id="a52b7-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="a52b7-131">您可以通过单击该链接查看重复执行 ID 的所有发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="a52b7-132">在您审查重复执行 ID 的发票时，您可以删除单个发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="a52b7-133">客户的重复执行设置将为该模板重置，以便它可在以后重新生成。</span><span class="sxs-lookup"><span data-stu-id="a52b7-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="a52b7-134">您可以过帐一个、许多或所有重复执行 ID 的发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="a52b7-135">如果启用工作流，您必须单击**提交**，然后才能过帐发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>
<span data-ttu-id="a52b7-136">打印重复执行普通发票</span><span class="sxs-lookup"><span data-stu-id="a52b7-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="a52b7-137">在重复发票过帐后，可以从普通发票列表页打印发票。</span><span class="sxs-lookup"><span data-stu-id="a52b7-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="a52b7-138">您可以打印选择的发票，或者可以选择要打印的发票范围。</span><span class="sxs-lookup"><span data-stu-id="a52b7-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>




